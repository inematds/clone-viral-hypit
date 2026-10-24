# CLAUDE.md — clone-viral-hypit

Kit do INEMA (documentação, sem código do Hypit) para refazer um clipe curto com o próprio rosto usando o Hypit
dentro do Claude Code, com os modelos rodando no fal.

## Regras do repo

- **Autor de todo commit:** `inematds <inematds@gmail.com>` (author e committer). Conferir `git config user.email` antes de commitar.
- **Push:** remoto SSH `git@github.com:inematds/clone-viral-hypit.git` (o token HTTPS da conta inematds não tem escopo `workflow`).
- **Não incluir código do Hypit** no repo: a licença dele não permite empacotar. Só link para https://github.com/hypit-ai/hypit.
- **Sem fonte de terceiros:** nada de link para vídeo, curso ou autor de onde a ideia veio. O kit é do INEMA.
- **Não afirmar que o INEMA rodou o pipeline.** Custos são aproximados, pelos preços de tabela lidos em 21/10/2026.
- **Ética:** só o próprio rosto ou rosto com permissão; só clipes próprios ou com direito de refazer. Nada de pessoa real famosa nos exemplos.
- **PT é a fonte.** EN/ES (README e guia) só pelo tradutor central `inema-traduz`.
- Antes do push: `grep -riE "youtube\.com/watch|sk[o]ol|an[d]y|ai vi[d]eo lab|no[c]ode|refer[eê]ncia da aula" --exclude-dir=.git .` tem que voltar vazio.
- Mudou o fluxo? Atualizar a seção "O processo, do início ao fim" do README no mesmo commit.

## Self-learning

When I correct you, or you catch yourself making a mistake: before continuing, add the lesson as a one-line rule at the TOP of [LESSONS.md](LESSONS.md) (not here), so it never happens again.

## Lessons

As lições ficam em [LESSONS.md](LESSONS.md). Ler antes de mexer no kit ou no guia.
