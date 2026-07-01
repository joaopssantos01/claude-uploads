# Formato de Saída Obrigatório (JSON)

```json
{
  "produto": "Sérum Facial Niacinamida 10% Nano - Ebla",
  "duracao_solicitada": "40s",
  "imagem_referencia_personagem_ambiente": "especialista_consultorio_1.png",
  "imagens_produto_referencia": [
    {"id": "ebla_fechado.png", "estado": "fechado"},
    {"id": "ebla_aberto.png", "estado": "aberto"}
  ],
  "mecanismo_unico_pesquisado": "Nano Niacinamida a 10% — penetra profundamente nas camadas da pele pra regulá a produção de melanina nos melanócitos, uniformizando o tom e clareando manchas sem sensibilizá a barreira cutânea.",
  "storytelling_arquetipo": "2 - Cliente que Tentou Tudo",
  "insights_de_referencia": [
    "Gancho por dor nomeada nos primeiros 2s",
    "CTA de escassez com frete grátis como gatilho principal"
  ],
  "gancho_escolhido": "Ninguém te fala isso, mas eu te falo...",
  "cta_escolhido": "Ó, o link tá bem aqui no carrinho. Vê se pra você ainda tá com frete grátis.",
  "texto_completo_copy": "Ninguém te fala isso, mas eu te falo — aquela mancha que não sai de jeito nenhum tem os dias contados. Eu atendo pessoas que chegam no consultório quase chorando de frustração porque já testaram cinco produtos diferentes, gastaram uma fortuna e a pele continua marcada do mesmo jeito. Aí eu indico esse sérum aqui, ó, porque a nano niacinamida de dez por cento penetra profundo pra regulá a melanina sem descascá a pele. Se você num cuidá disso hoje, amanhã você vai tentá disfarçá tudo com base pesada e odiá o resultado. Ó, o link tá bem aqui no carrinho. Vê se pra você ainda tá com frete grátis.",
  "roteiros": [
    {
      "id": "v1",
      "titulo": "Cliente que Tentou Tudo — Nano Niacinamida Anti-Manchas",
      "duracao_total": "40s",
      "estrutura": {
        "blocos": [
          {
            "bloco": 1,
            "papel": "Gancho / Dor Nomeada",
            "imagem_produto_usada": "ebla_fechado.png",
            "prompt": "[CONTEXTO: o mesmo ambiente, background e enquadramento, da foto de referência da personagem enviada (especialista_consultorio_1.png), sem nenhuma alteração.] [ÁUDIO: Acústica de sala comum, som de microfone amador de celular. Fala rápida, natural e assertiva.] [FALA INTEGRAL DO PERSONAGEM: 'Ninguém te fala isso, mas eu te falo — aquela mancha que não sai de jeito nenhum tem os dias contados, ó.'] [AÇÕES INTEGRADAS COM A FALA (RUBRICAS): No início da fala, a personagem olha fixa pra câmera com expressão séria. Ao pronunciar 'ó', o produto fechado (referência ebla_fechado.png) entra em quadro seguro com firmeza por uma mão. A mão livre aponta sutilmente pra baixo. Ao final da fala, a personagem abaixa a mão e o produto sai de quadro naturalmente.] NEGATIVE PROMPT: não colocar legendas ou ícones no vídeo, não colocar nenhum tipo de botão ou link no vídeo."
          },
          {
            "bloco": 2,
            "papel": "Storytelling — Arquétipo 2: Cliente que Tentou Tudo",
            "imagem_produto_usada": "nenhuma",
            "prompt": "[CONTEXTO: o mesmo ambiente, background e enquadramento, da foto de referência da personagem enviada (especialista_consultorio_1.png), sem nenhuma alteração.] [ÁUDIO: Acústica de sala comum, som de microfone amador de celular. Fala rápida, natural e assertiva.] [FALA INTEGRAL DO PERSONAGEM: 'Eu atendo pessoas que chegam no consultório quase chorando de frustração porque já testaram cinco produtos diferentes, gastaram uma fortuna e a pele continua marcada do mesmo jeito.'] [AÇÕES INTEGRADAS COM A FALA (RUBRICAS): A personagem gesticula levemente com as mãos expressando compreensão e empatia.] NEGATIVE PROMPT: não colocar legendas ou ícones no vídeo, não colocar nenhum tipo de botão ou link no vídeo."
          },
          {
            "bloco": 3,
            "papel": "Mecanismo Único — Nano Niacinamida 10%",
            "imagem_produto_usada": "ebla_fechado.png → ebla_aberto.png → ebla_fechado.png",
            "prompt": "[CONTEXTO: o mesmo ambiente, background e enquadramento, da foto de referência da personagem enviada (especialista_consultorio_1.png), sem nenhuma alteração.] [ÁUDIO: Acústica de sala comum, som de microfone amador de celular. Fala rápida, natural e assertiva.] [FALA INTEGRAL DO PERSONAGEM: 'Aí eu indico esse sérum aqui, ó, porque a nano niacinamida de dez por cento penetra profundo pra regulá a melanina sem descascá a pele.'] [AÇÕES INTEGRADAS COM A FALA (RUBRICAS): Ao falá 'indico esse sérum aqui', o produto fechado (referência ebla_fechado.png) entra em quadro, seguro com firmeza por uma mão. Ao falá 'ó', a personagem abre o produto brevemente (referência ebla_aberto.png), com ambas as mãos estáveis e focadas exclusivamente no produto. Em seguida fecha o produto novamente (referência ebla_fechado.png). Ao falá 'resultado', a mão livre aponta sutilmente pra baixo.] NEGATIVE PROMPT: não colocar legendas ou ícones no vídeo, não colocar nenhum tipo de botão ou link no vídeo."
          },
          {
            "bloco": 4,
            "papel": "CTA — Aversão à Perda + Escassez Real",
            "imagem_produto_usada": "ebla_fechado.png",
            "prompt": "[CONTEXTO: o mesmo ambiente, background e enquadramento, da foto de referência da personagem enviada (especialista_consultorio_1.png), sem nenhuma alteração.] [ÁUDIO: Acústica de sala comum, som de microfone amador de celular. Fala rápida, natural e assertiva.] [FALA INTEGRAL DO PERSONAGEM: 'Se você num cuidá disso hoje, amanhã você vai tentá disfarçá tudo com base pesada e odiá o resultado. Ó, o link tá bem aqui no carrinho. Vê se pra você ainda tá com frete grátis.'] [AÇÕES INTEGRADAS COM A FALA (RUBRICAS): A personagem segura o produto fechado (referência ebla_fechado.png) estável na mão. Ao pronunciar 'Ó, o link tá bem aqui no carrinho', a mão livre aponta pra baixo de forma limpa. A especialista finaliza com um sorriso tranquilo e mantém a pose.] NEGATIVE PROMPT: não colocar legendas ou ícones no vídeo, não colocar nenhum tipo de botão ou link no vídeo."
          }
        ]
      }
    }
  ]
}
```
