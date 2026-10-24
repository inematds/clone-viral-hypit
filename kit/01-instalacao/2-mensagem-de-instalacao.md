# 2. A mensagem de instalação (cole no Claude Code)

Abra o terminal **na pasta do projeto** (a que tem `references/`), inicie o Claude Code e cole:

> Instale o Hypit nesta pasta. Instale a skill do Hypit de github.com/hypit-ai/hypit só para este projeto, e o
> comando hypit pelo npm. Depois ligue o fal para as imagens e os clipes rodarem no fal: o Hypit não vem com o
> fal, então escreva um pequeno pacote Provider do projeto em packages/provider-fal que leia a minha FAL_KEY do
> ambiente e nunca grave a chave em arquivo. A FAL_KEY já está definida. Aponte o renderizador de páginas do
> Hypit para o Chrome que eu já tenho instalado. Me mostre o plano primeiro e depois confira se tudo funciona.

## O que costuma acontecer

- O Claude lê o README do Hypit e instala a skill **só neste projeto**: `npx skills add hypit-ai/hypit`
  (**sem** o `-g`, que instalaria para todos os projetos do computador).
- O pacote do npm se chama **`@hypit/hypit`** (não `hypit`). O comando roda como `npx hypit …`.
- O fal entra por um pequeno pacote Provider e pelo arquivo de runtime `hypit.runtime.json`
  (exemplo em `../03-modelos/hypit.runtime.example.json`).
- Ele aponta o renderizador de páginas para o Chrome que você já tem, para não baixar um navegador inteiro.
- Leva por volta de **6 minutos**, sem você digitar comando.

## Pegadinhas comuns

- **`npm pkg set` grava `true` como texto.** Quando o Claude marca uma opção booleana no `package.json`, o valor
  pode sair como `"true"` (string). A correção é rodar de novo com `--json`
  (`npm pkg set chave=true --json`). Se ele não perceber sozinho, mostre isto.
- **Skill instalada no lugar errado.** Se aparecer `-g` no comando, peça para instalar só no projeto.
- **Chave no arquivo.** Se o Claude sugerir colocar a chave num `.env` dentro do projeto ou no `hypit.runtime.json`,
  diga não: o runtime só guarda o **nome** da variável (`FAL_KEY`), nunca o valor.

## Dica de segurança

Deixe o Claude **pedir permissão antes de rodar comandos**. Não ligue nenhum modo "automático" para trabalho
pago. Diga sim para ler e conferir; diga sim para construir só depois de ver o preço.
