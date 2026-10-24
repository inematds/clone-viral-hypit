# Mensagem 2 — Corrigir o que ficou falso, com modelos premium

Depois de conferir a primeira versão (`../04-checklists/confira-antes-de-corrigir.md`), cole:

> /hypit O rosto e o texto da cena estão com cara de falso. Refaça com modelos premium: GPT Image 2.5 na qualidade
> máxima para três quadros (início, meio e fim), para o movimento não sair do trilho, e MiniMax H3 Max em 1080p
> para dois clipes de uns 4 segundos cada. Mantenha todos os prompts iguais, mudando só o modelo.
> Me mostre o plano e o preço e não construa nada.

## O que muda nessa correção

- **Modelo de imagem mais forte:** GPT Image 2.5 na qualidade máxima, que respeita melhor o rosto e o texto.
- **Um quadro do meio:** com início, meio e fim, o modelo de vídeo tem menos para adivinhar e o rosto escorrega menos.
- **Dois clipes de ~4 s** em vez de um de 8 s, cada um entre dois quadros vizinhos.
- **Vídeo em 1080p.**

## Por que "mantenha os prompts iguais"

Se você muda o modelo **e** o prompt ao mesmo tempo, não sabe o que melhorou. Mudando só o modelo, dá para
comparar com a primeira versão.

## Quanto custa (aproximado)

Por volta de **US$ 2** pelos preços de tabela lidos em 21/10/2026.

## Observação

O Hypit roda esses modelos premium pelo mesmo pacote Provider do fal. Se o Claude disser que falta o pacote de
modelo (por exemplo, para GPT Image 2.5 ou para o H3 Max), peça para ele criar o pacote e ligar no
`hypit.runtime.json` — e mostrar o plano antes.
