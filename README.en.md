# Viral clone with your face — Hypit + Claude Code + fal

[![Viral clone with your face](guia/assets/banner-en.jpg)](https://inematds.github.io/clone-viral-hypit/guia/en/)

**🇧🇷 [Português](README.md) · 🇺🇸 [English](README.en.md) · 🇪🇸 [Español](README.es.md)**

## What it is

This is a free INEMA kit, in Portuguese, with ready-to-paste messages for Claude Code, file templates,
checklists and a price table. It teaches you how to use Hypit, an open video tool, to redo a short clip
with your own face, make the version in another language, or swap the person for fictional characters. It is meant
for people who do marketing or create content and want to test several versions of an ad without filming again. You need
Claude Code, a fal account with a few dollars of credit, a clip of your own and two photos of your face.

## 📖 User guide

Full guide (landing + step by step): **https://inematds.github.io/clone-viral-hypit/guia/en/**

Explainer video for the kit: **https://inematds.github.io/clone-viral-hypit/videos/**

## Who it's for

- **Marketing and paid traffic:** one clip becomes 5 to 10 versions to test on a small budget before filming for real.
- **Content creators:** the same scene in another language, or with you in place of the presenter, with no camera or studio.

## The three pieces

- **[Hypit](https://github.com/hypit-ai/hypit)** — open tool that runs inside Claude Code: it reads your video,
  plans a new one, asks the models for the images and clips, adds subtitles and assembles everything on your computer.
- **[fal](https://fal.ai)** — service where the image and video models run. You pay per image and per second.
- **Claude Code** — you ask in text; it writes the Hypit files and shows the plan and the price before spending.

**Hypit is not included in this repository.** Its license does not allow bundling it; Claude itself installs it from the
official repository.

## The 3 steps

1. **Install** — one message installs Hypit in the project only and connects fal by reading the `FAL_KEY` from the environment (about 6 min).
2. **Redo it with your face** — first and last frame with your face, then the 8 seconds between them.
3. **Check, fix and make versions** — face, hands and text; premium models; another language; fictional characters.

Every message ends with **"Show me the plan and the price and don't build anything."** — the sentence that makes Claude quote a price and
stop before spending credit.

## Prices (approximate, from the 10/21/2026 price table)

| What | Approximate cost |
|---|---|
| First version with your face (Seedream 5 Lite + MiniMax H3 768p) | US$0.71 |
| Premium version (GPT Image 2.5 + MiniMax H3 Max 1080p) | ~US$2 |
| Version in another language | ~US$2 |
| MiniMax H3 Recast 1080p (US$0.45/s) | US$3.60 per 8 s clip · batch of 8 ≈ US$28.80 |
| Higgsfield Genjutsu 1080p (US$1.632/s, for comparison) | US$13.06 per clip · batch of 8 ≈ US$104.50 |

Prices change: check the pages before spending. Recast and Genjutsu are different models; only the price was compared.
Sources and details in [`kit/05-precos-e-links.md`](kit/05-precos-e-links.md) (the kit is in Portuguese).

## ⚠️ The ethical rule

**Use only your own face, or a face you have written permission to use. Use only your own clips, or clips you
have the right to redo.** No famous people, no colleagues without authorization, no other people's videos. The characters in the
kit are fictional. If the ad looks like a testimonial, disclose that it is AI-generated content.

## The process, from start to finish

Who does it: 🧠 you in Claude Code · ⚙️ Hypit/script · 🤖 models on fal.

| # | Step | What to do | Who does it |
|---|---|---|---|
| 1 | Prepare | Create the project folder with `references/meu-clipe.mp4`, `rosto-1.jpg`, `rosto-2.jpg` ([`kit/01-instalacao/1-o-que-precisa.md`](kit/01-instalacao/1-o-que-precisa.md)) | 🧠 |
| 2 | Store the key | `export FAL_KEY="..."` in `~/.zshrc`/`~/.bashrc`, open a new terminal; never in the chat ([`3-chave-fal-segura.md`](kit/01-instalacao/3-chave-fal-segura.md)) | 🧠 |
| 3 | Install | Paste the installation message into Claude Code ([`2-mensagem-de-instalacao.md`](kit/01-instalacao/2-mensagem-de-instalacao.md)); Hypit is installed with `npx skills add hypit-ai/hypit` (without `-g`) and `@hypit/hypit` | 🧠 → ⚙️ |
| 4 | Quote the first clip | Paste message 1 ([`kit/02-mensagens/1-refazer-com-seu-rosto.md`](kit/02-mensagens/1-refazer-com-seu-rosto.md)); Claude writes the `.svml` and shows the plan and price | 🧠 → ⚙️ |
| 5 | Generate the images | Say "you can build the images"; the 2 frames with your face come out of fal | 🤖 |
| 6 | Check the images | Face, hands, text ([`kit/04-checklists/confira-antes-de-corrigir.md`](kit/04-checklists/confira-antes-de-corrigir.md)) | 🧠 |
| 7 | Generate the video | Say "you can build the clip"; fal generates the 8 s and Hypit assembles it on your computer | 🤖 → ⚙️ |
| 8 | Fix | Message 2 (premium), quote, check, build | 🧠 → 🤖 |
| 9 | Make versions | Message 3 (another language) and/or 4 (fictional characters from `characters.json`) | 🧠 → 🤖 → ⚙️ |
| 10 | Test | Run the versions as a single test and keep the ones that retain the most ([`teste-com-7-versoes.md`](kit/04-checklists/teste-com-7-versoes.md)) | 🧠 |

### Where the guide and video of this repository live

| Piece | Where | Who does it |
|---|---|---|
| Guide (PT/EN/ES) | `guia/index.html`, `guia/en/`, `guia/es/` → https://inematds.github.io/clone-viral-hypit/guia/en/ | 🧠 (INEMA session) → ⚙️ GitHub Pages via Actions |
| Explainer video | final file outside the repo; published as release `video-v1.0.0` (MP4 + SRT) and player in `videos/` → https://inematds.github.io/clone-viral-hypit/videos/ | ⚙️ `python3 scripts/publica.py` |

## Kit structure

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
guia/        usage page (PT, en/, es/)
videos/      explainer video player
scripts/     publica.py (uploads the video as a release and generates the player)
```

## Hypit license (summary)

Hypit uses the "Hypit Open Source License" (Apache-2.0 with conditions). In short: free use for your own work and
that of clients, including commercial; it may not be operated as a hosted or multi-tenant service for third parties; it may not be
sold or bundled, nor may Hypit or derivatives; you must keep the name and the logo. What you create is yours; the terms of the
model providers still apply. Read the full license at https://github.com/hypit-ai/hypit.

## License of this kit

[MIT](LICENSE) — applies only to the INEMA text, file templates and scripts.

---

Open and free content from **[INEMA.CLUB](https://inema.club)**.
