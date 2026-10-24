# 1. O que você precisa

1. **Claude Code** instalado e funcionando no seu plano do Claude.
2. **Node.js 22.15 ou mais novo** (o Hypit roda com `npx`). Se não tiver, o Claude avisa e ajuda a instalar.
3. **Uma conta no fal** (https://fal.ai) com alguns dólares de crédito. US$ 5 dão para a primeira versão e alguns testes.
4. **Um clipe curto que seja seu** (ou que você tem direito de refazer), **de 8 a 10 segundos** (as mensagens
   usam os primeiros 8 s; se o seu for mais curto, troque "8 segundos" na mensagem pela duração real).
5. **Duas fotos nítidas do seu rosto**: uma de frente e uma levemente de lado. Sem óculos escuros, sem mão na boca, com luz boa.
6. **Google Chrome** no computador. O Hypit usa o Chrome para desenhar legendas e telas; apontando para o Chrome
   que você já tem, nada grande precisa ser baixado.

## Como organizar a pasta

Crie uma pasta vazia para o projeto e, dentro dela, uma pasta `references/`:

```
meu-clone/
└── references/
    ├── meu-clipe.mp4      ← o clipe que você vai refazer
    ├── rosto-1.jpg        ← foto de frente
    └── rosto-2.jpg        ← foto levemente de lado
```

Você **não** precisa tirar os quadros do clipe: o Claude extrai o primeiro e o último quadro e salva em `references/`
(por exemplo `meu-clipe-primeiro-quadro.png`) quando você manda a mensagem 1.

Para a mensagem 4 (personagens), ponha o clipe de UGC como `references/meu-ugc.mp4` e o `characters.json` na raiz da
pasta (`meu-clone/characters.json`).

Depois guarde a chave do fal (próximo arquivo, `3-chave-fal-segura.md`) e mande a mensagem de instalação
(`2-mensagem-de-instalacao.md`).
