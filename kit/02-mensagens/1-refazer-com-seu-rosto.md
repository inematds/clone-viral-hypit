# Mensagem 1 — Refazer o clipe com o seu rosto

Na pasta `references/`: o clipe (`meu-clipe.mp4`) e as duas fotos (`rosto-1.jpg`, `rosto-2.jpg`). Cole no Claude Code:

> /hypit Refaça os primeiros 8 segundos de references/meu-clipe.mp4 com o meu rosto, usando references/rosto-1.jpg e
> references/rosto-2.jpg. Pegue o primeiro e o último quadro do clipe e coloque o meu rosto nos dois, mantendo a
> mesma pose, a mesma sala e a mesma luz. Depois faça o clipe de 8 segundos entre esses dois quadros. Divida em
> duas rodadas, primeiro as imagens e depois o clipe, para eu conferir as imagens antes de pagar o vídeo.
> Me mostre o plano e o preço e não construa nada.

## Por que cada parte está aí

- **`/hypit` no início:** faz o Claude usar a skill do Hypit, e não improvisar um script próprio.
- **Primeiros 8 segundos:** clipe curto erra menos e custa menos.
- **Primeiro e último quadro:** o modelo de vídeo recebe o começo e o fim já com o seu rosto e só "preenche" o meio.
- **Duas rodadas:** as imagens custam centavos; o vídeo custa mais. Conferir as imagens antes evita pagar um clipe
  com rosto errado.
- **"Me mostre o plano e o preço e não construa nada."** É a frase mais importante (veja abaixo).

## Como o Hypit monta (o arquivo que o Claude escreve)

Um exemplo limpo está em `../03-modelos/refazer-com-seu-rosto.svml`. Em resumo:

- **4 entradas:** as 2 fotos do rosto + o primeiro e o último quadro do clipe.
- **2 trabalhos de imagem:** um por quadro. O prompt diz o que trocar e o que manter:
  "troque só o apresentador; mantenha a loja, a luz e a pose".
- **1 trabalho de vídeo:** preenche os 8 segundos entre os dois quadros. Descreva o movimento por trechos
  (0–3 s, 3–5 s, 5–8 s).

## Quanto custa (aproximado)

Com Seedream 5 Lite nas imagens e MiniMax H3 em 768p no vídeo, rodando no fal, a primeira versão sai por
**cerca de US$ 0,71** pelos preços de tabela lidos em 21/10/2026.

## O que costuma acontecer

A primeira versão não é ruim, mas o rosto pode ficar um pouco diferente do seu, e **texto na cena vira letra sem
sentido** (uma placa "CEREAL" pode virar "CENLIL"). Por isso o próximo passo é conferir
(`../04-checklists/confira-antes-de-corrigir.md`) antes de corrigir.

## Por que "Me mostre o plano e o preço e não construa nada" é a frase mais importante

O Claude, quando entende o pedido, tende a ir direto ao trabalho. No Hypit, "trabalho" é chamar modelos pagos no
fal. Essa frase transforma o pedido em **orçamento**: ele lê, planeja, calcula o custo, mostra e **para**. Você
confere três coisas — se ele entendeu o clipe certo, se os modelos e a resolução são os que você pediu e se o preço
cabe — e só então responde "pode construir". Se o preço vier como estimativa, peça para ele conferir na página de
preços do fal antes de seguir.
