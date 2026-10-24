# 3. Como guardar a FAL_KEY com segurança

A chave do fal é dinheiro: quem tiver a chave gasta o seu crédito. Faça isto **uma vez**, antes da mensagem de instalação.

## Passo a passo

1. No fal (https://fal.ai), abra o painel e crie uma **API key**. Copie.
2. Guarde como variável de ambiente `FAL_KEY` no arquivo de perfil do seu terminal:
   - **Mac** (zsh): `~/.zshrc`
   - **Linux** (bash): `~/.bashrc`

   Abra o arquivo num editor de texto e acrescente uma linha no fim:

   ```bash
   export FAL_KEY="cole-aqui-a-sua-chave"
   ```

3. **Feche e abra o terminal** (ou rode `source ~/.zshrc` / `source ~/.bashrc`) para carregar a chave.
4. Confira, **sem mostrar o valor**:

   ```bash
   [ -n "$FAL_KEY" ] && echo "FAL_KEY carregada" || echo "FAL_KEY não encontrada"
   ```

5. Só então abra o Claude Code na pasta do projeto.

## As regras

- **Nunca cole a chave no chat**, nem no Claude. O Hypit lê a chave do seu computador; o Claude não precisa vê-la.
- **Nunca grave a chave em arquivo do projeto** (`.env` do projeto, `hypit.runtime.json`, código). O runtime guarda só
  o nome `FAL_KEY`.
- **Nunca rode `echo $FAL_KEY`** com o Claude olhando: o valor aparece no histórico da conversa.
- Se a chave vazar (print, chat, commit), **apague-a no painel do fal e crie outra**.
- Ponha um **limite de gasto** no fal, se a sua conta permitir, e coloque pouco crédito no começo.
