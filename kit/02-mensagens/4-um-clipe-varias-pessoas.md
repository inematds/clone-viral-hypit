# Mensagem 4 — Um clipe de UGC, várias pessoas novas

UGC é aquele vídeo com cara de "gravado no celular por um cliente": selfie, fala direta, cenário de casa.

Coloque na pasta: o clipe (**menos de 15 segundos, uma pessoa só**, seu ou com direito de refazer) e o arquivo
`characters.json` (modelo em `../03-modelos/characters.json`, com personagens **fictícios**). Cole:

> /hypit Quero um clipe de UGC de 8 segundos refeito com personagens diferentes, uma versão por personagem do
> characters.json. Cada personagem ganha uma foto de identidade feita pelo GPT Image 2.5, e depois o MiniMax H3
> Recast coloca essa pessoa no clipe em 1080p, mantendo os movimentos, a câmera e o tempo.
> Me mostre o plano e o preço total de todas as versões e não construa nada.

## Por que cada parte está aí

- **`/hypit`** no início, para o Claude usar a skill do Hypit.
- **Qual clipe e quais personagens**: o clipe e o `characters.json`.
- **Os modelos**: GPT Image 2.5 para a foto de identidade; MiniMax H3 Recast para colocar a pessoa no clipe.
- **A resolução**: 1080p.
- **"Me mostre o plano e o preço total … e não construa nada."** Com várias versões, o custo multiplica. Aqui a
  frase importa mais ainda.

## O que costuma acontecer

- **O filtro de segurança bloqueia uma foto às vezes.** Uma das rodadas volta com `content_policy_violation`.
  Não é erro do Hypit: o modelo recusou a descrição. Suavize a descrição daquele personagem (menos detalhe de corpo,
  roupa mais comum) e rode só aquela de novo. Peça ao Claude para conferir **cada** rodada e apontar qual falhou.
- **O primeiro preço pode ser um chute.** Se o Claude disser que é estimativa, peça: "confira o preço real nas
  páginas do fal". Pela tabela de 21/10/2026: 8 clipes de Recast em 1080p ≈ **US$ 28,80**, mais alguns centavos
  das fotos.

## Quanto custa (aproximado)

- 1 clipe de 8 s em 1080p no Recast: 8 × US$ 0,45 = **US$ 3,60**.
- 7 versões: 7 × US$ 3,60 ≈ **US$ 25,20**. 8 versões: ≈ **US$ 28,80**.
- Fotos de identidade: centavos cada.

Arquivo de uma rodada de Recast para um personagem: `../03-modelos/recast-um-personagem.svml`.

## Regra

Personagem fictício, sempre. Não descreva uma pessoa real ("parecida com fulano"). E não use clipe de outra pessoa
sem direito de refazer.
