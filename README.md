# Clone viral com o seu rosto — Hypit + Claude Code + fal

[![Clone viral com o seu rosto](guia/assets/banner.jpg)](https://inematds.github.io/clone-viral-hypit/guia/)

**🇧🇷 [Português](README.md) · 🇺🇸 [English](README.en.md) · 🇪🇸 [Español](README.es.md)**

## O que é

Este é um kit gratuito do INEMA, em português, com mensagens prontas para colar no Claude Code, modelos de arquivo,
checklists e uma tabela de preços. Ele ensina a usar o Hypit, uma ferramenta aberta de vídeo, para refazer um clipe
curto com o seu próprio rosto, fazer a versão em outra língua ou trocar a pessoa por personagens fictícios. Serve
para quem faz marketing ou cria conteúdo e quer testar várias versões de um anúncio sem gravar de novo. Você precisa
do Claude Code, de uma conta no fal com alguns dólares de crédito, de um clipe seu e de duas fotos do seu rosto.

## 📖 Guia de uso

Guia completo (landing + passo a passo): **https://inematds.github.io/clone-viral-hypit/guia/**

Vídeo explicativo do kit: **https://inematds.github.io/clone-viral-hypit/videos/**

## Para quem é

- **Marketing e tráfego pago:** um clipe vira 5 a 10 versões para testar com pouca verba antes de gravar de verdade.
- **Criadores de conteúdo:** a mesma cena em outra língua, ou com você no lugar do apresentador, sem câmera nem estúdio.

## As três peças

- **[Hypit](https://github.com/hypit-ai/hypit)** — ferramenta aberta que roda dentro do Claude Code: lê o seu vídeo,
  planeja um novo, pede aos modelos as imagens e os clipes, põe legendas e monta tudo no seu computador.
- **[fal](https://fal.ai)** — serviço onde rodam os modelos de imagem e de vídeo. Você paga por imagem e por segundo.
- **Claude Code** — você pede em texto; ele escreve os arquivos do Hypit e mostra o plano e o preço antes de gastar.

**O Hypit não vem neste repositório.** A licença dele não permite empacotar; o próprio Claude instala a partir do
repositório oficial.

## Os 3 passos

1. **Instalar** — uma mensagem instala o Hypit só no projeto e liga o fal lendo a `FAL_KEY` do ambiente (uns 6 min).
2. **Refazer com o seu rosto** — primeiro e último quadro com o seu rosto, depois os 8 segundos entre eles.
3. **Conferir, corrigir e fazer versões** — rosto, mãos e texto; modelos premium; outra língua; personagens fictícios.

Toda mensagem termina com **"Me mostre o plano e o preço e não construa nada."** — a frase que faz o Claude orçar e
parar antes de gastar crédito.

## Preços (aproximados, pela tabela de 21/10/2026)

| O quê | Custo aproximado |
|---|---|
| Primeira versão com o seu rosto (Seedream 5 Lite + MiniMax H3 768p) | US$ 0,71 |
| Versão premium (GPT Image 2.5 + MiniMax H3 Max 1080p) | ~US$ 2 |
| Versão em outra língua | ~US$ 2 |
| MiniMax H3 Recast 1080p (US$ 0,45/s) | US$ 3,60 por clipe de 8 s · lote de 8 ≈ US$ 28,80 |
| Higgsfield Genjutsu 1080p (US$ 1,632/s, comparação) | US$ 13,06 por clipe · lote de 8 ≈ US$ 104,50 |

Preço muda: confira as páginas antes de gastar. Recast e Genjutsu são modelos diferentes; só o preço foi comparado.
Fontes e detalhes em [`kit/05-precos-e-links.md`](kit/05-precos-e-links.md).

## ⚠️ A regra ética

**Use só o seu rosto, ou um rosto que você tem permissão por escrito para usar. Use só clipes seus, ou clipes que
você tem direito de refazer.** Nada de pessoa famosa, de colega sem autorização ou de vídeo alheio. Os personagens do
kit são fictícios. Se o anúncio parece depoimento, avise que é conteúdo gerado por IA.

## O processo, do início ao fim

Quem faz: 🧠 você no Claude Code · ⚙️ Hypit/script · 🤖 modelos no fal.

| # | Passo | O que fazer | Quem faz |
|---|---|---|---|
| 1 | Preparar | Criar a pasta do projeto com `references/meu-clipe.mp4`, `rosto-1.jpg`, `rosto-2.jpg` ([`kit/01-instalacao/1-o-que-precisa.md`](kit/01-instalacao/1-o-que-precisa.md)) | 🧠 |
| 2 | Guardar a chave | `export FAL_KEY="..."` no `~/.zshrc`/`~/.bashrc`, abrir terminal novo; nunca no chat ([`3-chave-fal-segura.md`](kit/01-instalacao/3-chave-fal-segura.md)) | 🧠 |
| 3 | Instalar | Colar a mensagem de instalação no Claude Code ([`2-mensagem-de-instalacao.md`](kit/01-instalacao/2-mensagem-de-instalacao.md)); o Hypit é instalado com `npx skills add hypit-ai/hypit` (sem `-g`) e `@hypit/hypit` | 🧠 → ⚙️ |
| 4 | Orçar o primeiro clipe | Colar a mensagem 1 ([`kit/02-mensagens/1-refazer-com-seu-rosto.md`](kit/02-mensagens/1-refazer-com-seu-rosto.md)); o Claude escreve o `.svml` e mostra plano e preço | 🧠 → ⚙️ |
| 5 | Gerar as imagens | Dizer "pode construir as imagens"; os 2 quadros com o seu rosto saem do fal | 🤖 |
| 6 | Conferir as imagens | Rosto, mãos, texto ([`kit/04-checklists/confira-antes-de-corrigir.md`](kit/04-checklists/confira-antes-de-corrigir.md)) | 🧠 |
| 7 | Gerar o vídeo | Dizer "pode construir o clipe"; o fal gera os 8 s e o Hypit monta no seu computador | 🤖 → ⚙️ |
| 8 | Corrigir | Mensagem 2 (premium), orçar, conferir, construir | 🧠 → 🤖 |
| 9 | Fazer versões | Mensagem 3 (outra língua) e/ou 4 (personagens fictícios do `characters.json`) | 🧠 → 🤖 → ⚙️ |
| 10 | Testar | Rodar as versões como um teste só e ficar com as que retêm mais ([`teste-com-7-versoes.md`](kit/04-checklists/teste-com-7-versoes.md)) | 🧠 |

### Onde ficam o guia e o vídeo deste repositório

| Peça | Onde | Quem faz |
|---|---|---|
| Guia (PT/EN/ES) | `guia/index.html`, `guia/en/`, `guia/es/` → https://inematds.github.io/clone-viral-hypit/guia/ | 🧠 (sessão INEMA) → ⚙️ GitHub Pages via Actions |
| Vídeo explicativo | arquivo final fora do repo; publicado como release `video-v1.0.0` (MP4 + SRT) e player em `videos/` → https://inematds.github.io/clone-viral-hypit/videos/ | ⚙️ `python3 scripts/publica.py` |

## Estrutura do kit

```
kit/
├── 00-COMECE-AQUI.md
├── 01-instalacao/
│   ├── 1-o-que-precisa.md
│   ├── 2-mensagem-de-instalacao.md
│   └── 3-chave-fal-segura.md
├── 02-mensagens/
│   ├── 1-refazer-com-seu-rosto.md
│   ├── 2-corrigir-com-premium.md
│   ├── 3-nova-lingua.md
│   └── 4-um-clipe-varias-pessoas.md
├── 03-modelos/
│   ├── README.md
│   ├── characters.json
│   ├── hypit.runtime.example.json
│   ├── refazer-com-seu-rosto.svml
│   └── recast-um-personagem.svml
├── 04-checklists/
│   ├── confira-antes-de-corrigir.md
│   ├── 3-erros.md
│   └── teste-com-7-versoes.md
└── 05-precos-e-links.md
guia/        página de uso (PT, en/, es/)
videos/      player do vídeo explicativo
scripts/     publica.py (sobe o vídeo como release e gera o player)
```

## Licença do Hypit (resumo)

O Hypit usa a "Hypit Open Source License" (Apache-2.0 com condições). Em resumo: uso livre para o seu trabalho e o
de clientes, também comercial; não pode operar como serviço hospedado ou multi-inquilino para terceiros; não pode
vender nem empacotar o Hypit ou derivados; precisa manter o nome e o logo. O que você cria é seu; os termos dos
provedores de modelo continuam valendo. Leia a licença completa em https://github.com/hypit-ai/hypit.

## Licença deste kit

[MIT](LICENSE) — vale só para o texto, os modelos de arquivo e os scripts do INEMA.

---

Conteúdo aberto e gratuito do **[INEMA.CLUB](https://inema.club)**.
