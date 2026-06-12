# Contrato da API Au4 (capturado via interceptor — sessão 2026-06-12)

## Base
- API base: https://api.au4.ai
- Front (Next.js) em https://www.au4.ai — ApiClient loga no console, polla /api/user/credits a cada ~60s
- Auth: Bearer token em localStorage.auth_token (+ cookie auth-token). Header: Authorization: Bearer <token>
- IDs no formato cuid (ex.: cmqb8l9360659qn0konvq9qk7), ~25 chars

## Fluxo de geração (3 chamadas)
1. POST /api/images/upload  (x2: produto + avatar)
   - multipart/form-data (body de 17 chars no log = boundary; é FormData)
   - resp 201: { id, url(357c), thumbnailUrl, dimensions{width,height,aspectRatio}, fileSize, status }
   - url é do s3.us-east-1.wasabisys.com (storage da Au4)

2. POST /ugc-video
   - body JSON:
     {
       productName: string,
       productDescription: string,
       productImageUrl: string,   // url do upload (wasabi au4)
       avatarImageUrl: string,    // url do upload (wasabi au4)
       videoType: "review"|"unboxing",        // LOWERCASE (form mostra Review/Unboxing)
       language: "pt-BR",
       tone: "authentic"|"energetic"|...,      // LOWERCASE
       customHook: string,
       mode: "seedance",
       seedanceDuration: 15,                   // number
       seedanceResolution: "720p",
       seedanceGenerateAudio: true,
       seedanceAspectRatio: "9:16"
     }
   - resp 201: { id, userId, productName, ... status, progress, ... } (cuid no id)

3. GET /ugc-video/{id}  (polling de status)
   - resp 200, campos relevantes:
     - status: "GENERATING_VIDEO" (+ progress: 0-100) -> ... -> (final: COMPLETED/DONE, confirmar)
     - videoUrl: null enquanto gera; preenchido quando pronto (provável signed wasabi)
     - frameUrl/frame2Url/frame3Url: frames intermediários
     - errorMessage: pra falha
     - creditsUsed: custo real
     - selectedScript, scripts, seedanceVideoPrompt: a IA escreve os beats
   - status enums vistos no bundle: ERROR, FAILED (demais num chunk não baixado)

## Outros endpoints observados
- GET /api/user/credits           (saldo; pollado a cada 60s)
- GET /api/task-queue/has-pending?taskType=UGC_STANDARD
- GET /ugc-video?page=1&limit=20  (lista)
- GET /users/me, /billing/info, /notifications, /notifications/summary

## CORS / sessão
- Chamada fetch manual ao api.au4.ai DE DENTRO da página (console) -> "Failed to fetch"
  (o front passa, minha chamada não; provável preflight/origem). 
  IMPLICAÇÃO: um worker externo (Node) NÃO tem o problema de CORS do browser —
  CORS é restrição de browser. Node/cURL chamando api.au4.ai direto com o Bearer
  deve funcionar (a API em si responde; o bloqueio foi do contexto da página).
  -> CONFIRMAR no worker: bater /users/me com o token e ver se 200.

## Token / login
- Auto-login (extensão v4): preenche form de login e dá requestSubmit; token cai no
  localStorage.auth_token. Não capturei o POST de login ainda (não expirou nesta sessão).
- Para o worker headless: precisamos do POST de login (email/senha -> token).
  Endpoint provável: POST /auth/login ou /users/login (CONFIRMAR capturando 1 logout->login).
