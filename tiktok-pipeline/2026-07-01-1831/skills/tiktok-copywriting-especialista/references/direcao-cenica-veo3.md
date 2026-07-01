# Regras Cruciais de Direção Cênica, Enquadramento e Cortes (Otimizado para Google Veo 3)

## Princípios Fundamentais de Prompt para Veo 3
- **Front-Load o Sujeito:** O Veo 3 pesa as primeiras palavras do prompt muito mais. Coloque o sujeito e a ação principal logo no início.
- **Uma Ação por Clipe:** Não tente forçar múltiplas transformações no mesmo bloco. Se precisa mudar o estado de um objeto, use um Jump Cut entre blocos.
- **Descreva o Que EXISTE, Não o Que Não Existe:** Nunca escreva "sem produto" ou "produto fora de quadro" — se o produto não está na cena, simplesmente não o mencione.
- **Linguagem Mecânica, Não de Resultado:** Para ações físicas, use verbos de processo ("abre", "fecha", "segura") em vez de verbos de resultado/transformação ("revela", "expõe", "mostra o interior").

## Regras de Cena

1. **Câmera 100% Fixa + Ambiente Ancorado por Nome de Imagem:** Tripé estático — sem movimento, pan, zoom ou mudança de ângulo. A âncora de contexto em TODOS os blocos deve ser a frase fixa: **"o mesmo ambiente, background e enquadramento, da foto de referência da personagem enviada ([NOME_DA_FOTO_PERSONAGEM]), sem nenhuma alteração"**. É PROIBIDO descrever o ambiente em texto.

2. **Áudio Padronizado:** O campo de áudio em TODOS os blocos deve ser: **"Acústica de sala comum, som de microfone amador de celular. Fala rápida, natural e assertiva."**

3. **Imagem Única de Personagem por Lote:** Uma só foto de personagem/ambiente para todo o lote. O produto pode ter múltiplas imagens de referência por estado (fechado, aberto).

4. **Abstração de Características Físicas:** Não descreva roupas, cabelos, cores, formatos de frasco. Refira-se como "a personagem que está na foto de referência" e "o produto que está na imagem de referência [estado/id]".

5. **Constância de Estado do Produto por Bloco (Anti-Alucinação Veo 3):** O estado do produto não pode mudar dentro de um bloco, EXCETO pela ação única e limpa de abrir/fechar (ver regra 5a). Se o bloco começa com produto fechado, ele permanece fechado até que haja uma ação explícita de abertura.

5a. **Ação de Abertura/Fechamento do Produto (Linguagem Limpa para Veo 3):** Quando o roteiro exigir que a personagem abra o produto dentro de um bloco:
   - Use APENAS verbos mecânicos simples: **"abre o produto brevemente"** e **"fecha o produto novamente"**.
   - Referencie diretamente a imagem de referência do estado correspondente: **"(referência [ID_ABERTO])"** e **"(referência [ID_FECHADO])"**.
   - É **TERMINANTEMENTE PROIBIDO** usar qualquer verbo ou expressão que implique transformação, revelação ou surgimento de um componente novo: ~~"revela"~~, ~~"revelando"~~, ~~"expondo"~~, ~~"mostrando o conta-gotas"~~, ~~"a tampa é removida revelando"~~, ~~"expõe o mecanismo"~~. Essas expressões causam morphing mid-clip no Veo 3 porque inferem que o componente não existia antes.
   - **Fórmula correta:** *"a personagem abre o produto brevemente (referência ebla_aberto.png), com ambas as mãos estáveis e focadas exclusivamente no produto. Em seguida fecha o produto novamente (referência ebla_fechado.png)."*

6. **Jump Cuts Inter-Blocos:** Qualquer mudança de estado de objeto só ocorre na virada exata entre blocos, via corte seco.

7. **Proibição de Aplicação:** A personagem JAMAIS passa o produto no rosto, pele ou mãos. Apenas exibe.

8. **Mão Livre — Regra Anti-Alucinação:** A personagem só aponta para baixo com a mão livre quando o produto estiver FECHADO e estável na outra mão. PROIBIDO gesticular com mão livre enquanto o produto estiver aberto.

9. **Blocos SEM Produto — Regra Anti-Fantasma (Crítica para Veo 3):**
   - Se um bloco não usa imagem de produto (`imagem_produto_usada: "nenhuma"`), o campo `prompt` desse bloco **NÃO PODE conter nenhuma palavra que se refira ao produto** — nem "produto", nem "frasco", nem "sérum", nem "fora de quadro", nem "sem produto", nem "Jump Cut (produto)". O produto simplesmente **não existe** naquele prompt. Apenas a personagem e a fala devem ser descritas.
   - Para garantir uma transição fluida na narrativa, o **bloco anterior** (que continha o produto) deve incluir ao final de suas RUBRICAS a instrução: *"Ao final da fala, a personagem abaixa a mão e o produto sai de quadro naturalmente."*

10. **Contexto Dedicado por Bloco:** Cada bloco deve carregar sua própria ancoragem de ambiente (com o nome da foto) e áudio padronizado.

11. **Reveal Ancorado à Fala:** A entrada do produto em quadro e qualquer troca de estado só ocorrem quando a fala passa a se referir ao produto — nunca antes.

11a. **Lei das Deixas Verbais (Anti-Contradição Crítica):** Sempre que a fala contiver "isso aqui", "esse aqui", "ó", "olha aqui" ou variações, o produto OBRIGATORIAMENTE está em quadro naquele exato momento. É PROIBIDO escrever deixa de exibição com `imagem_produto_usada: "nenhuma"`.

12. **Negative Prompt Obrigatório:** Todo prompt de todo bloco termina com: `NEGATIVE PROMPT: não colocar legendas ou ícones no vídeo, não colocar nenhum tipo de botão ou link no vídeo.`
