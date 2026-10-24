# Comece aqui — Clone viral com o seu rosto (Hypit + Claude Code + fal)

Kit do INEMA, em português, para refazer um clipe curto **com o seu próprio rosto**, fazer a versão em
outra língua ou trocar a pessoa por personagens fictícios — tudo pedindo em texto para o Claude Code.

- **Hypit** é a ferramenta aberta que planeja e monta o vídeo no seu computador: https://github.com/hypit-ai/hypit
- **fal** (https://fal.ai) é o serviço onde rodam os modelos de imagem e de vídeo. Você paga por imagem e por segundo de vídeo.
- **Claude Code** conversa com você, escreve os arquivos do Hypit e mostra o plano e o preço antes de gastar.

Este kit é **só texto**: mensagens prontas para colar no Claude, modelos de arquivo, checklists e a tabela de
preços. O Hypit **não vem aqui dentro** (a licença dele não permite empacotar). Você instala pelo repositório
oficial, e o próprio Claude faz isso por você no passo 1.

## A regra ética (antes de tudo)

> **Use só o seu rosto, ou um rosto que você tem permissão por escrito para usar.**
> **Use só clipes seus, ou clipes que você tem direito de refazer.**

Nada de rosto de famoso, de colega sem autorização ou de vídeo alheio "porque viralizou". Os personagens do
arquivo `03-modelos/characters.json` são **fictícios** de propósito.

## O caminho, em ordem

| # | O que fazer | Arquivo |
|---|---|---|
| 1 | Instalar (uns 6 minutos, sem digitar comando) | `01-instalacao/` |
| 2 | Refazer o clipe com o seu rosto | `02-mensagens/1-refazer-com-seu-rosto.md` |
| 3 | Conferir o que ficou com cara de falso | `04-checklists/confira-antes-de-corrigir.md` |
| 4 | Corrigir com modelos premium | `02-mensagens/2-corrigir-com-premium.md` |
| 5 | Fazer versões: outra língua ou outras pessoas | `02-mensagens/3-nova-lingua.md` e `4-um-clipe-varias-pessoas.md` |
| 6 | Usar as versões num teste de anúncio | `04-checklists/teste-com-7-versoes.md` |
| 7 | Evitar os 3 erros | `04-checklists/3-erros.md` |

Preços e links: `05-precos-e-links.md`. Modelos de arquivo (SVML, runtime, personagens): `03-modelos/`.

## A frase que protege o seu dinheiro

Termine **toda** mensagem de trabalho com:

> **Me mostre o plano e o preço e não construa nada.**

Com ela, o Claude lê o pedido, monta o plano, calcula quanto vai custar no fal e **para**. Só depois que você
olhar o plano e o preço e disser "pode fazer" é que ele gasta crédito. Sem essa frase, um pedido mal entendido
pode virar dez clipes pagos antes de você perceber.

## O que esperar (sem promessa)

Não é mágica. O rosto às vezes escorrega, a mão fica dura, letreiro vira letra sem sentido. Você confere
quadro a quadro. A vantagem é que, depois de montado o primeiro, um rosto novo ou uma língua nova é uma
mensagem a mais, não um dia de gravação.

Os custos citados no kit são **aproximados, calculados pelos preços de tabela lidos em 21/10/2026**. Confira as
páginas do fal antes de gastar: preço muda.
