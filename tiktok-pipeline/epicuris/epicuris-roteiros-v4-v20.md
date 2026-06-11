# Epicuris — CONTINUAÇÃO DO LOTE (V4–V20) — para rodar no Cowork

**Skill:** `au4-ugc-express` (versão com pipeline intercalada + progresso.json + coleta na página)
**Comando de retomada:** "retoma o lote do Epicuris pelo progresso.json" — a skill lê
`tiktok-pipeline/epicuris/progresso.json` no repo `joaopssantos01/claude-uploads` e segue do próximo pendente.

## Estado atual (2026-06-11T23:10Z)
| Vídeo | Status | Observação |
|---|---|---|
| V1 | ✅ gerado + dublado | híbrido: original 0–3.7s (hook) e 9.6–15s; Amandoca no meio (atempo 0.93) |
| V2 | ✅ gerado + dublado | híbrido: original 0–3.3s (hook); Amandoca 3.3–15s (atempo 0.96) |
| V3 | ✅ gerado + dublado | full-dub (personagem não articula em câmera); atempo 1.15 |
| V4–V20 | ⏳ pendentes | payloads completos abaixo |

URLs S3 dos brutos V1–V3 (válidas 7 dias) e estado-fonte: `tiktok-pipeline/epicuris/progresso.json`.

## Operação (resumo pro Cowork)
1. Página: `https://www.au4.ai/criativos/ugc-seedance` (extensão **Au4 UGC Filler** instalada; checar `data-au4-filler === 'ready'`).
2. Por vídeo: postMessage `AU4_UGC_FILL` com o payload → conferir `data-au4-fill-status` (resolution FAIL em 720p é falso-positivo) → conferir Duration=**15s** → clicar **Generate UGC (Seedance)** via JS.
3. **Coleta na própria página "Video ready"**: `read_network_requests` filtro `wasabisys` (clicar Download MP4 só se a URL não aparecer) → registrar no `progresso.json` → **New video** pro próximo.
4. **Pipeline intercalada**: enquanto N renderiza (~7min), dublar o N−1 com a `tiktok-dublagem-amandoca` (Modo B = híbrido com dry-run; texto = corpo+CTA do roteiro, sem o hook). Atualizar `progresso.json` a cada transição.
5. Sessão caiu pro login → aguardar ~20s e re-navegar; não parar o lote.
6. **Custo**: ~98–113 créditos/vídeo com avatar.

**productImageUrl (todos):** `https://raw.githubusercontent.com/joaopssantos01/claude-uploads/main/tiktok-pipeline/2026-06-11-2046/epicuris-essencia-exfoliante.jpg`

**Face refs Carla (rotação V4=ref1, V5=ref2, V6=ref3, V7=ref1...):**
1. `https://raw.githubusercontent.com/joaopssantos01/claude-uploads/main/personagens/carla/carla-ref-principal.jpg`
2. `https://uxmajgriujjsosuxpzyt.supabase.co/storage/v1/object/public/generated-images/or_1781117113705_5urxmw5.png`
3. `https://uxmajgriujjsosuxpzyt.supabase.co/storage/v1/object/public/generated-images/or_1781117326937_9ofeba0.png`

---

## V4 — Unboxing · A3·B2·C1 · Sofá · F-C · M-5-Unboxing · CTA-retorno · Carla-1 · 47 palavras

**productName:** Epicuris
**Opening hook:** "Esse esfoliante tá bombando no TikTok e ele acabou de chegar aqui."
**videoType:** Unboxing | **tone:** Authentic | **duration:** 15s
**faceImageUrl:** Carla-1

```
benefício + angulo de abordagem: ângulo: first impression — chegou hoje, testei na hora · público: pele opaca sem viço que estraga qualquer maquiagem · benefício central: dissolve comedonas fechados sem inflamar
A embalagem nunca é rasgada — o produto sai pelo conta-gotas apertando levemente a pera da pipeta.

gancho visual de abertura: o quadro mostra um sofá vazio por um instante; a Carla entra correndo e se joga de costas no sofá, quicando levemente nas almofadas, e senta de golpe olhando para o produto que já está sobre a mesinha de centro em destaque; ela o pega com as duas mãos. Câmera fixa de frente para o sofá. A queda no sofá é divertida e segura; o produto permanece intacto na mesinha até ela pegá-lo.

narração:
[fala em câmera — APENAS esta frase de abertura, ~2-3s, personagem olha pra câmera e fala]: "Esse esfoliante tá bombando no TikTok e ele acabou de chegar aqui."
[voice over — TODO o restante do vídeo. A partir daqui a personagem NÃO fala mais em nenhum momento — apenas manuseia, aplica e demonstra o produto em silêncio enquanto a narração corre por cima]: "Passei o conta-gotas no rosto, textura aguinha, absorveu super rápido. O diferencial: ele dissolve comedonas fechados, esses pontinhos que não saem espremendo sem inflamar. Incrível. Usa direitinho e volta aqui me contar. Carrinho laranja, ó."

Nenhum icone, texto ou legenda deve aparecer no vídeo
```

---

## V5 — Review · A4·B1·C3 · Tropeço entrada · F-D · M-4-Segredo · CTA-urgência · Carla-2 · 55 palavras

**productName:** Epicuris
**Opening hook:** "Ninguém te conta que tem esfoliante que hidrata ENQUANTO esfoleia — olha isso."
**videoType:** Review | **tone:** Authentic | **duration:** 15s
**faceImageUrl:** Carla-2

```
benefício + angulo de abordagem: ângulo: PENTAVITIN = ímã que limpa e hidrata ao mesmo tempo · público: pele oleosa com comedonas que inflamam · benefício central: esfoliação + hidratação simultâneas (PENTAVITIN 72h)

gancho visual de abertura: o vídeo abre com o quadro vazio e parado por um segundo, mostrando só o cenário; de repente a Carla entra tropeçando pela lateral do quadro, se segura no batente da porta para não cair, ri envergonhada da própria atrapalhação, ajeita a roupa e caminha até a câmera mostrando o produto que estava na bancada. Câmera fixa. O tropeço é leve e cômico, sem queda completa e sem machucado.

narração:
[fala em câmera — APENAS esta frase de abertura, ~2-3s, personagem olha pra câmera e fala]: "Ninguém te conta que tem esfoliante que hidrata ENQUANTO esfoleia — olha isso."
[voice over — TODO o restante do vídeo. A partir daqui a personagem NÃO fala mais em nenhum momento — apenas manuseia, aplica e demonstra o produto em silêncio enquanto a narração corre por cima]: "O Epicuris tem PENTAVITIN, ativo que gruda na pele feito ímã e hidrata por setenta e duas horas. Você esfoleia os poros sem perder hidratação. Pra pele oleosa com cravo é ideal. Tá no carrinho laranja — aproveita antes que volte ao preço normal."

Nenhum icone, texto ou legenda deve aparecer no vídeo
```

---

## V6 — Unboxing · A3·B1·C2 · Objeto voa · F-C · M-5-Unboxing · CTA-convite · Carla-3 · 50 palavras

**productName:** Epicuris
**Opening hook:** "Olha o que chegou: a essência exfoliante que encheu meu TikTok!"
**videoType:** Unboxing | **tone:** Energetic | **duration:** 15s
**faceImageUrl:** Carla-3

```
benefício + angulo de abordagem: ângulo: first impression — chegou hoje, testei na hora · público: pele oleosa com comedonas que inflamam · benefício central: pele visivelmente mais suave e uniforme com uso consistente
A embalagem nunca é rasgada — o produto sai pelo conta-gotas apertando levemente a pera da pipeta.

gancho visual de abertura: o vídeo começa com a Carla de frente para a câmera quando, de repente, um objeto leve entra voando pela lateral do quadro e passa rente ao rosto dela, fazendo a câmera dar um tranco rápido; ela se assusta de leve, ri, pega o Epicuris Essência Exfoliante e o segura em destaque na frente da câmera. Câmera fixa (apenas o tranco rápido no momento do impacto). O objeto passa de leve, sem bater de verdade na Carla, e o produto fica intacto.

narração:
[fala em câmera — APENAS esta frase de abertura, ~2-3s, personagem olha pra câmera e fala]: "Olha o que chegou: a essência exfoliante que encheu meu TikTok!"
[voice over — TODO o restante do vídeo. A partir daqui a personagem NÃO fala mais em nenhum momento — apenas manuseia, aplica e demonstra o produto em silêncio enquanto a narração corre por cima]: "Passei ontem à noite e a pele acordou incrível de suave. Textura aguinha, zero resíduo, não ardeu nem ressecou. A diferença na textura deu pra sentir já de manhã. Dá uma olhada no carrinho laranja, vale cada centavo."

Nenhum icone, texto ou legenda deve aparecer no vídeo
```

---

## V7 — Review · A1·B2·C2 · Produto jogado · F-B · M-1-Exclusão · CTA-desafio · Carla-1 · 57 palavras

**productName:** Epicuris
**Opening hook:** "Tá com aqueles pontinhos brancos que não saem nem com base?"
**videoType:** Review | **tone:** Authentic | **duration:** 15s
**faceImageUrl:** Carla-1

```
benefício + angulo de abordagem: ângulo: comedonas fechados ≠ cravo comum — dissolve de dentro · público: pele opaca sem viço que estraga qualquer maquiagem · benefício central: pele visivelmente mais suave e uniforme com uso consistente

gancho visual de abertura: o vídeo começa com a Carla deitada no sofá, de olhos quase fechados; de repente o produto é jogado de fora do quadro em direção a ela, que abre os olhos e o pega no ar com as duas mãos, sorrindo surpresa, e senta para mostrá-lo. Câmera fixa. O lançamento é suave e curto; o produto é pego com firmeza e não cai nem abre no movimento.

narração:
[fala em câmera — APENAS esta frase de abertura, ~2-3s, personagem olha pra câmera e fala]: "Tá com aqueles pontinhos brancos que não saem nem com base?"
[voice over — TODO o restante do vídeo. A partir daqui a personagem NÃO fala mais em nenhum momento — apenas manuseia, aplica e demonstra o produto em silêncio enquanto a narração corre por cima]: "São comedonas fechados — e esfoliante de grão não resolve. O Epicuris Essência Exfoliante é líquido, penetra no poro e dissolve por dentro. Com uso consistente a pele fica bem mais suave e uniforme. Testa e me conta se não é tudo isso. Tá no carrinho laranja."

Nenhum icone, texto ou legenda deve aparecer no vídeo
```

---

## V8 — Unboxing · A3·B2·C4 · Close extremo · F-C · M-5-Unboxing · CTA-cumplicidade · Carla-2 · 54 palavras

**productName:** Epicuris
**Opening hook:** "Chegou o Epicuris Essência Exfoliante — e esse não é esfoliante qualquer não."
**videoType:** Unboxing | **tone:** Authentic | **duration:** 15s
**faceImageUrl:** Carla-2

```
benefício + angulo de abordagem: ângulo: first impression — chegou hoje, testei na hora · público: pele opaca sem viço que estraga qualquer maquiagem · benefício central: renovação celular → viço, tom uniforme, make assenta melhor
A embalagem nunca é rasgada — o produto sai pelo conta-gotas apertando levemente a pera da pipeta.

gancho visual de abertura: o vídeo abre com um close extremo na pele da bochecha da Carla, tão perto que a textura da pele preenche o quadro por um instante; a câmera então recua suavemente revelando a Carla, que pega o produto e começa a aplicar as gotinhas justamente naquela região. Câmera fixa após o recuo. Movimento de aproximação curto e estável, sem distorção; o produto entra em cena já recuado.

narração:
[fala em câmera — APENAS esta frase de abertura, ~2-3s, personagem olha pra câmera e fala]: "Chegou o Epicuris Essência Exfoliante — e esse não é esfoliante qualquer não."
[voice over — TODO o restante do vídeo. A partir daqui a personagem NÃO fala mais em nenhum momento — apenas manuseia, aplica e demonstra o produto em silêncio enquanto a narração corre por cima]: "Esse aqui trabalha na renovação celular. A pele fica com viço, tom mais uniforme, e a maquiagem começa a assentar de outro jeito. Já testei — e gente, a diferença na textura é real. Você vai me agradecer depois — carrinho laranja, corre lá."

Nenhum icone, texto ou legenda deve aparecer no vídeo
```

---

## V9 — Review · A2·B1·C3 · Queda · F-A · M-1-Exclusão · CTA-escassez · Carla-3 · 48 palavras

**productName:** Epicuris
**Opening hook:** "Meninas com pele oleosa, NÃO podem usar qualquer esfoliante — resseca e piora."
**videoType:** Review | **tone:** Authentic | **duration:** 15s
**faceImageUrl:** Carla-3

```
benefício + angulo de abordagem: ângulo: a camada invisível que destrói a make — serum exfoliante vs esfoliante de grão · público: pele oleosa com comedonas que inflamam · benefício central: esfoliação + hidratação simultâneas (PENTAVITIN 72h)

gancho visual de abertura: o vídeo começa com a Carla correndo de forma desajeitada em direção à câmera, ela tropeça e cai sentada no chão de maneira leve e cômica, sem se machucar; ela ri da própria queda, ajeita o cabelo, se recompõe sentada no chão e só então pega o produto que já estava ao lado dela no chão. Câmera fixa como celular apoiado. O movimento é leve e cômico, sem perigo; o produto não participa da queda e nunca cai.

narração:
[fala em câmera — APENAS esta frase de abertura, ~2-3s, personagem olha pra câmera e fala]: "Meninas com pele oleosa, NÃO podem usar qualquer esfoliante — resseca e piora."
[voice over — TODO o restante do vídeo. A partir daqui a personagem NÃO fala mais em nenhum momento — apenas manuseia, aplica e demonstra o produto em silêncio enquanto a narração corre por cima]: "Esfoliante de grão irrita e resseca ainda mais. O Epicuris Essência Exfoliante é diferente — fórmula líquida, com PENTAVITIN que hidrata enquanto esfoleia. Pra pele oleosa é o ideal. Tá no carrinho laranja, aproveita antes que acabe."

Nenhum icone, texto ou legenda deve aparecer no vídeo
```

---

## V10 — Unboxing · A3·B1·C4 · Cambalhota · F-C · M-5-Unboxing · CTA-frete · Carla-1 · 57 palavras

**productName:** Epicuris
**Opening hook:** "Gente, o Epicuris chegou e eu preciso te mostrar essa textura!"
**videoType:** Unboxing | **tone:** Excited | **duration:** 15s
**faceImageUrl:** Carla-1

```
benefício + angulo de abordagem: ângulo: first impression — chegou hoje, testei na hora · público: pele oleosa com comedonas que inflamam · benefício central: renovação celular → viço, tom uniforme, make assenta melhor
A embalagem nunca é rasgada — o produto sai pelo conta-gotas apertando levemente a pera da pipeta.

gancho visual de abertura: o vídeo começa com a Carla dando uma cambalhota divertida sobre o tapete em direção à câmera, terminando sentada de pernas cruzadas de frente para a câmera, despenteada e rindo; ela ajeita o cabelo e pega o produto que já estava no chão à sua frente. Câmera fixa como celular apoiado. O movimento é leve e cômico, sem perigo; o produto não participa da cambalhota e nunca cai.

narração:
[fala em câmera — APENAS esta frase de abertura, ~2-3s, personagem olha pra câmera e fala]: "Gente, o Epicuris chegou e eu preciso te mostrar essa textura!"
[voice over — TODO o restante do vídeo. A partir daqui a personagem NÃO fala mais em nenhum momento — apenas manuseia, aplica e demonstra o produto em silêncio enquanto a narração corre por cima]: "Sério, é de cair o queixo. Textura aguinha, pipetinha de dosagem perfeita — absorve em segundos. O ativo acelera a renovação celular, então a pele vai ficando com viço. Pra pele oleosa é incrível. Por menos de quarenta no carrinho laranja — comprando dois o frete é grátis."

Nenhum icone, texto ou legenda deve aparecer no vídeo
```

---

## V11 — Review · A4·B2·C2 · Escorregão · F-D · M-4-Segredo · CTA-salva · Carla-2 · 48 palavras

**productName:** Epicuris
**Opening hook:** "Esse ativo do Epicuris gruda na pele feito ímã — pode acreditar."
**videoType:** Review | **tone:** Authentic | **duration:** 15s
**faceImageUrl:** Carla-2

```
benefício + angulo de abordagem: ângulo: PENTAVITIN = ímã que limpa e hidrata ao mesmo tempo · público: pele opaca sem viço que estraga qualquer maquiagem · benefício central: pele visivelmente mais suave e uniforme com uso consistente

gancho visual de abertura: o vídeo começa com a Carla deslizando de meias pelo chão liso do quarto, entrando no quadro pela lateral em alta velocidade, derrapando e quase perdendo o equilíbrio na frente da câmera; ela se segura, solta uma risada de alívio e pega o produto na cômoda ao lado. Câmera fixa. O escorregão é cômico e leve, ela não cai no chão e o produto fica seguro na cômoda durante todo o movimento.

narração:
[fala em câmera — APENAS esta frase de abertura, ~2-3s, personagem olha pra câmera e fala]: "Esse ativo do Epicuris gruda na pele feito ímã — pode acreditar."
[voice over — TODO o restante do vídeo. A partir daqui a personagem NÃO fala mais em nenhum momento — apenas manuseia, aplica e demonstra o produto em silêncio enquanto a narração corre por cima]: "É o PENTAVITIN, que funciona como ímã de hidratação: arrasta a impureza e ainda deixa a barreira intacta. Com uso consistente a pele opaca fica visivelmente mais uniforme. Salva esse vídeo e anota. Tá no carrinho laranja."

Nenhum icone, texto ou legenda deve aparecer no vídeo
```

---

## V12 — Unboxing · A3·B2·C3 · Sofá · F-C · M-5-Unboxing · CTA-retorno · Carla-3 · 53 palavras

**productName:** Epicuris
**Opening hook:** "Tô abrindo o Epicuris Essência Exfoliante ao vivo — já testei no dia."
**videoType:** Unboxing | **tone:** Authentic | **duration:** 15s
**faceImageUrl:** Carla-3

```
benefício + angulo de abordagem: ângulo: first impression — chegou hoje, testei na hora · público: pele opaca sem viço que estraga qualquer maquiagem · benefício central: esfoliação + hidratação simultâneas (PENTAVITIN 72h)
A embalagem nunca é rasgada — o produto sai pelo conta-gotas apertando levemente a pera da pipeta.

gancho visual de abertura: o quadro mostra um sofá vazio por um instante; a Carla entra correndo e se joga de costas no sofá, quicando levemente nas almofadas, e senta de golpe olhando para o produto que já está sobre a mesinha de centro em destaque; ela o pega com as duas mãos. Câmera fixa de frente para o sofá. A queda no sofá é divertida e segura; o produto permanece intacto na mesinha até ela pegá-lo.

narração:
[fala em câmera — APENAS esta frase de abertura, ~2-3s, personagem olha pra câmera e fala]: "Tô abrindo o Epicuris Essência Exfoliante ao vivo — já testei no dia."
[voice over — TODO o restante do vídeo. A partir daqui a personagem NÃO fala mais em nenhum momento — apenas manuseia, aplica e demonstra o produto em silêncio enquanto a narração corre por cima]: "Pele apagada, sem viço? O diferencial desse aqui é o PENTAVITIN — esfoleia e ainda hidrata por setenta e duas horas. Então você não sai ressecada. A pele ficou incrível à noite. Usa direitinho e volta aqui me contar. Carrinho laranja, ó."

Nenhum icone, texto ou legenda deve aparecer no vídeo
```

---

## V13 — Review · A1·B1·C4 · Tropeço entrada · F-E · M-3-Tutorial · CTA-urgência · Carla-1 · 59 palavras

**productName:** Epicuris
**Opening hook:** "Como eu melhorei a textura da pele oleosa em casa — salva esse."
**videoType:** Review | **tone:** Authentic | **duration:** 15s
**faceImageUrl:** Carla-1

```
benefício + angulo de abordagem: ângulo: comedonas fechados ≠ cravo comum — dissolve de dentro · público: pele oleosa com comedonas que inflamam · benefício central: renovação celular → viço, tom uniforme, make assenta melhor

gancho visual de abertura: o vídeo abre com o quadro vazio e parado por um segundo, mostrando só o cenário; de repente a Carla entra tropeçando pela lateral do quadro, se segura no batente da porta para não cair, ri envergonhada da própria atrapalhação, ajeita a roupa e caminha até a câmera mostrando o produto que estava na bancada. Câmera fixa. O tropeço é leve e cômico, sem queda completa e sem machucado.

narração:
[fala em câmera — APENAS esta frase de abertura, ~2-3s, personagem olha pra câmera e fala]: "Como eu melhorei a textura da pele oleosa em casa — salva esse."
[voice over — TODO o restante do vídeo. A partir daqui a personagem NÃO fala mais em nenhum momento — apenas manuseia, aplica e demonstra o produto em silêncio enquanto a narração corre por cima]: "Comedor fechado é diferente de cravo — e esse aqui trabalha exatamente nisso. O Epicuris Essência Exfoliante remove as células mortas e acelera a renovação celular. Com o tempo a pele ganha viço. Uma gotinha toda noite. Tá no carrinho laranja — aproveita antes que volte ao preço normal."

Nenhum icone, texto ou legenda deve aparecer no vídeo
```

---

## V14 — Unboxing · A3·B1·C1 · Objeto voa · F-C · M-5-Unboxing · CTA-convite · Carla-2 · 53 palavras

**productName:** Epicuris
**Opening hook:** "Esse aqui chegou hoje e eu já não consigo parar de aplicar."
**videoType:** Unboxing | **tone:** Authentic | **duration:** 15s
**faceImageUrl:** Carla-2

```
benefício + angulo de abordagem: ângulo: first impression — chegou hoje, testei na hora · público: pele oleosa com comedonas que inflamam · benefício central: dissolve comedonas fechados sem inflamar
A embalagem nunca é rasgada — o produto sai pelo conta-gotas apertando levemente a pera da pipeta.

gancho visual de abertura: o vídeo começa com a Carla de frente para a câmera quando, de repente, um objeto leve entra voando pela lateral do quadro e passa rente ao rosto dela, fazendo a câmera dar um tranco rápido; ela se assusta de leve, ri, pega o Epicuris Essência Exfoliante e o segura em destaque na frente da câmera. Câmera fixa (apenas o tranco rápido no momento do impacto). O objeto passa de leve, sem bater de verdade na Carla, e o produto fica intacto.

narração:
[fala em câmera — APENAS esta frase de abertura, ~2-3s, personagem olha pra câmera e fala]: "Esse aqui chegou hoje e eu já não consigo parar de aplicar."
[voice over — TODO o restante do vídeo. A partir daqui a personagem NÃO fala mais em nenhum momento — apenas manuseia, aplica e demonstra o produto em silêncio enquanto a narração corre por cima]: "Epicuris Essência Exfoliante. Textura de água, penetra no poro fundo, e o diferencial é que dissolve comedonas fechados — esses que ficam embaixo da pele e inflamam quando você espreme. Já me convenceu. Dá uma olhada no carrinho laranja, vale cada centavo."

Nenhum icone, texto ou legenda deve aparecer no vídeo
```

---

## V15 — Review · A2·B2·C1 · Close extremo · F-B · M-1-Exclusão · CTA-desafio · Carla-3 · 54 palavras

**productName:** Epicuris
**Opening hook:** "Tá com aquela pele cinzenta sem viço que não reage a nada?"
**videoType:** Review | **tone:** Authentic | **duration:** 15s
**faceImageUrl:** Carla-3

```
benefício + angulo de abordagem: ângulo: a camada invisível que destrói a make — células mortas vs serum exfoliante · público: pele opaca sem viço que estraga qualquer maquiagem · benefício central: dissolve comedonas fechados sem inflamar

gancho visual de abertura: o vídeo abre com um close extremo na pele da bochecha da Carla, tão perto que a textura da pele preenche o quadro por um instante; a câmera então recua suavemente revelando a Carla, que pega o produto e começa a aplicar as gotinhas justamente naquela região. Câmera fixa após o recuo. Movimento de aproximação curto e estável, sem distorção; o produto entra em cena já recuado.

narração:
[fala em câmera — APENAS esta frase de abertura, ~2-3s, personagem olha pra câmera e fala]: "Tá com aquela pele cinzenta sem viço que não reage a nada?"
[voice over — TODO o restante do vídeo. A partir daqui a personagem NÃO fala mais em nenhum momento — apenas manuseia, aplica e demonstra o produto em silêncio enquanto a narração corre por cima]: "Pode ser camada de célula morta travando tudo. O Epicuris Essência Exfoliante dissolve esse acúmulo e desobstrói os poros — fórmula líquida, não irrita. A pele vai ficando mais viva. Testa e me conta se não é tudo isso. Tá no carrinho laranja."

Nenhum icone, texto ou legenda deve aparecer no vídeo
```

---

## V16 — Unboxing · A4·B1·C2 · Produto jogado · F-D · M-5-Unboxing · CTA-cumplicidade · Carla-1 · 54 palavras

**productName:** Epicuris
**Opening hook:** "Esse esfoliante hidrata por setenta e duas horas enquanto limpa os poros."
**videoType:** Unboxing | **tone:** Authentic | **duration:** 15s
**faceImageUrl:** Carla-1

```
benefício + angulo de abordagem: ângulo: PENTAVITIN = ímã que limpa e hidrata ao mesmo tempo · público: pele oleosa com comedonas que inflamam · benefício central: pele visivelmente mais suave e uniforme com uso consistente
A embalagem nunca é rasgada — o produto sai pelo conta-gotas apertando levemente a pera da pipeta.

gancho visual de abertura: o vídeo começa com a Carla deitada no sofá, de olhos quase fechados; de repente o produto é jogado de fora do quadro em direção a ela, que abre os olhos e o pega no ar com as duas mãos, sorrindo surpresa, e senta para mostrá-lo. Câmera fixa. O lançamento é suave e curto; o produto é pego com firmeza e não cai nem abre no movimento.

narração:
[fala em câmera — APENAS esta frase de abertura, ~2-3s, personagem olha pra câmera e fala]: "Esse esfoliante hidrata por setenta e duas horas enquanto limpa os poros."
[voice over — TODO o restante do vídeo. A partir daqui a personagem NÃO fala mais em nenhum momento — apenas manuseia, aplica e demonstra o produto em silêncio enquanto a narração corre por cima]: "É o PENTAVITIN do Epicuris Essência Exfoliante — gruda na pele como ímã, esfoleia e mantém a hidratação. Você não sai com a pele áspera. Já testei — textura incrível, pele bem mais suave depois. Você vai me agradecer depois — carrinho laranja, corre lá."

Nenhum icone, texto ou legenda deve aparecer no vídeo
```

---

## V17 — Review · A1·B2·C3 · Queda · F-D · M-4-Segredo · CTA-escassez · Carla-2 · 50 palavras

**productName:** Epicuris
**Opening hook:** "Ninguém te conta: comedor fechado e cravo precisam de tratamentos diferentes."
**videoType:** Review | **tone:** Authentic | **duration:** 15s
**faceImageUrl:** Carla-2

```
benefício + angulo de abordagem: ângulo: comedonas fechados ≠ cravo comum — dissolve de dentro · público: pele opaca sem viço que estraga qualquer maquiagem · benefício central: esfoliação + hidratação simultâneas (PENTAVITIN 72h)

gancho visual de abertura: o vídeo começa com a Carla correndo de forma desajeitada em direção à câmera, ela tropeça e cai sentada no chão de maneira leve e cômica, sem se machucar; ela ri da própria queda, ajeita o cabelo, se recompõe sentada no chão e só então pega o produto que já estava ao lado dela no chão. Câmera fixa como celular apoiado. O movimento é leve e cômico, sem perigo; o produto não participa da queda e nunca cai.

narração:
[fala em câmera — APENAS esta frase de abertura, ~2-3s, personagem olha pra câmera e fala]: "Ninguém te conta: comedor fechado e cravo precisam de tratamentos diferentes."
[voice over — TODO o restante do vídeo. A partir daqui a personagem NÃO fala mais em nenhum momento — apenas manuseia, aplica e demonstra o produto em silêncio enquanto a narração corre por cima]: "Cravo abre e sai; comedor fechado fica embaixo da pele e precisa de fórmula líquida que penetre. O Epicuris Essência Exfoliante faz exatamente isso — e com PENTAVITIN a pele sai hidratada. Tá no carrinho laranja, aproveita antes que acabe."

Nenhum icone, texto ou legenda deve aparecer no vídeo
```

---

## V18 — Unboxing · A2·B2·C2 · Cambalhota · F-A · M-5-Unboxing · CTA-frete · Carla-3 · 59 palavras

**productName:** Epicuris
**Opening hook:** "Não esperava que essa essência fosse deixar a pele assim de cara."
**videoType:** Unboxing | **tone:** Authentic | **duration:** 15s
**faceImageUrl:** Carla-3

```
benefício + angulo de abordagem: ângulo: a camada invisível que destrói a make — células mortas vs serum exfoliante · público: pele opaca sem viço que estraga qualquer maquiagem · benefício central: pele visivelmente mais suave e uniforme com uso consistente
A embalagem nunca é rasgada — o produto sai pelo conta-gotas apertando levemente a pera da pipeta.

gancho visual de abertura: o vídeo começa com a Carla dando uma cambalhota divertida sobre o tapete em direção à câmera, terminando sentada de pernas cruzadas de frente para a câmera, despenteada e rindo; ela ajeita o cabelo e pega o produto que já estava no chão à sua frente. Câmera fixa como celular apoiado. O movimento é leve e cômico, sem perigo; o produto não participa da cambalhota e nunca cai.

narração:
[fala em câmera — APENAS esta frase de abertura, ~2-3s, personagem olha pra câmera e fala]: "Não esperava que essa essência fosse deixar a pele assim de cara."
[voice over — TODO o restante do vídeo. A partir daqui a personagem NÃO fala mais em nenhum momento — apenas manuseia, aplica e demonstra o produto em silêncio enquanto a narração corre por cima]: "É o Epicuris Essência Exfoliante — chega na camada de célula morta que deixa a pele opaca e dissolve. Com uso constante a textura fica visivelmente mais suave e uniforme. Chegou hoje e já senti. Por menos de quarenta no carrinho laranja — comprando dois o frete é grátis."

Nenhum icone, texto ou legenda deve aparecer no vídeo
```

---

## V19 — Review · A4·B1·C4 · Escorregão · F-D · M-4-Segredo · CTA-salva · Carla-1 · 52 palavras

**productName:** Epicuris
**Opening hook:** "Você conhece o PENTAVITIN? Limpa e ainda acelera a renovação da pele."
**videoType:** Review | **tone:** Authentic | **duration:** 15s
**faceImageUrl:** Carla-1

```
benefício + angulo de abordagem: ângulo: PENTAVITIN = ímã que limpa e hidrata ao mesmo tempo · público: pele oleosa com comedonas que inflamam · benefício central: renovação celular → viço, tom uniforme, make assenta melhor

gancho visual de abertura: o vídeo começa com a Carla deslizando de meias pelo chão liso do quarto, entrando no quadro pela lateral em alta velocidade, derrapando e quase perdendo o equilíbrio na frente da câmera; ela se segura, solta uma risada de alívio e pega o produto na cômoda ao lado. Câmera fixa. O escorregão é cômico e leve, ela não cai no chão e o produto fica seguro na cômoda durante todo o movimento.

narração:
[fala em câmera — APENAS esta frase de abertura, ~2-3s, personagem olha pra câmera e fala]: "Você conhece o PENTAVITIN? Limpa e ainda acelera a renovação da pele."
[voice over — TODO o restante do vídeo. A partir daqui a personagem NÃO fala mais em nenhum momento — apenas manuseia, aplica e demonstra o produto em silêncio enquanto a narração corre por cima]: "É o ativo do Epicuris Essência Exfoliante — gruda na pele, dissolve impureza e ativa o metabolismo celular. Com o tempo, pele oleosa ganha viço e textura mais uniforme. Uso toda noite. Salva esse vídeo e anota — tá no carrinho laranja."

Nenhum icone, texto ou legenda deve aparecer no vídeo
```

---

## V20 — Unboxing · A2·B1·C2 · Sofá · F-A · M-5-Unboxing · CTA-retorno · Carla-2 · 57 palavras

**productName:** Epicuris
**Opening hook:** "Meninas, pele oleosa NÃO pode usar qualquer esfoliante — esse eu aprovei."
**videoType:** Unboxing | **tone:** Authentic | **duration:** 15s
**faceImageUrl:** Carla-2

```
benefício + angulo de abordagem: ângulo: a camada invisível que destrói a make — serum exfoliante vs esfoliante de grão · público: pele oleosa com comedonas que inflamam · benefício central: pele visivelmente mais suave e uniforme com uso consistente
A embalagem nunca é rasgada — o produto sai pelo conta-gotas apertando levemente a pera da pipeta.

gancho visual de abertura: o quadro mostra um sofá vazio por um instante; a Carla entra correndo e se joga de costas no sofá, quicando levemente nas almofadas, e senta de golpe olhando para o produto que já está sobre a mesinha de centro em destaque; ela o pega com as duas mãos. Câmera fixa de frente para o sofá. A queda no sofá é divertida e segura; o produto permanece intacto na mesinha até ela pegá-lo.

narração:
[fala em câmera — APENAS esta frase de abertura, ~2-3s, personagem olha pra câmera e fala]: "Meninas, pele oleosa NÃO pode usar qualquer esfoliante — esse eu aprovei."
[voice over — TODO o restante do vídeo. A partir daqui a personagem NÃO fala mais em nenhum momento — apenas manuseia, aplica e demonstra o produto em silêncio enquanto a narração corre por cima]: "É o Epicuris Essência Exfoliante — esfoleia suave sem ressecar. A pele fica mais suave com uso constante, sem vermelhidão nem ardência. Pra quem tem medo de esfoliante — é esse. Chegou hoje, já testei. Por menos de quarenta no carrinho laranja — comprando dois o frete é grátis."

Nenhum icone, texto ou legenda deve aparecer no vídeo
```

---

## Checklist de aprovação

| # | Tipo | Família | Modelo | Hook Visual | CTA | Carla | Palavras | ✓ |
|---|------|---------|--------|-------------|-----|-------|----------|---|
| 1 | Review | D-Segredo | M4 | Queda | escassez | 1 | 47 | |
| 2 | Unboxing | C-Choque | M5 | Cambalhota | frete | 2 | 50 | |
| 3 | Review | A-Exclusão | M1 | Escorregão | salva | 3 | 50 | |
| 4 | Unboxing | C-Choque | M5 | Sofá | retorno | 1 | 47 | |
| 5 | Review | D-Segredo | M4 | Tropeço entrada | urgência | 2 | 55 | |
| 6 | Unboxing | C-Choque | M5 | Objeto voa | convite | 3 | 50 | |
| 7 | Review | B-Pergunta | M1 | Produto jogado | desafio | 1 | 57 | |
| 8 | Unboxing | C-Choque | M5 | Close extremo | cumplicidade | 2 | 54 | |
| 9 | Review | A-Exclusão | M1 | Queda | escassez | 3 | 48 | |
| 10 | Unboxing | C-Choque | M5 | Cambalhota | frete | 1 | 57 | |
| 11 | Review | D-Segredo | M4 | Escorregão | salva | 2 | 48 | |
| 12 | Unboxing | C-Choque | M5 | Sofá | retorno | 3 | 53 | |
| 13 | Review | E-Transformação | M3 | Tropeço entrada | urgência | 1 | 59 | |
| 14 | Unboxing | C-Choque | M5 | Objeto voa | convite | 2 | 53 | |
| 15 | Review | B-Pergunta | M1 | Close extremo | desafio | 3 | 54 | |
| 16 | Unboxing | D-Segredo | M5 | Produto jogado | cumplicidade | 1 | 54 | |
| 17 | Review | D-Segredo | M4 | Queda | escassez | 2 | 50 | |
| 18 | Unboxing | A-Exclusão | M5 | Cambalhota | frete | 3 | 59 | |
| 19 | Review | D-Segredo | M4 | Escorregão | salva | 1 | 52 | |
| 20 | Unboxing | A-Exclusão | M5 | Sofá | retorno | 2 | 57 | |

**Custo estimado:** 20 × ~113 créditos = **~2.260 créditos**
**productImageUrl:** `https://raw.githubusercontent.com/joaopssantos01/claude-uploads/main/tiktok-pipeline/2026-06-11-2046/epicuris-essencia-exfoliante.jpg`
