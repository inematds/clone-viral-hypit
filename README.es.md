# Clone viral con tu rostro — Hypit + Claude Code + fal

[![Clone viral con tu rostro](guia/assets/banner-es.jpg)](https://inematds.github.io/clone-viral-hypit/guia/es/)

**🇧🇷 [Português](README.md) · 🇺🇸 [English](README.en.md) · 🇪🇸 [Español](README.es.md)**

## Qué es

Este es un kit gratuito del INEMA, en portugués, con mensajes listos para pegar en Claude Code, plantillas de archivo,
listas de verificación y una tabla de precios. Enseña a usar Hypit, una herramienta abierta de video, para rehacer un clip
corto con tu propio rostro, hacer la versión en otro idioma o reemplazar a la persona por personajes ficticios. Sirve
para quienes trabajan en marketing o crean contenido y quieren probar varias versiones de un anuncio sin grabar de nuevo. Necesitas
Claude Code, una cuenta en fal con algunos dólares de crédito, un clip tuyo y dos fotos de tu rostro.

## 📖 Guía de uso

Guía completa (landing + paso a paso): **https://inematds.github.io/clone-viral-hypit/guia/es/**

Video explicativo del kit: **https://inematds.github.io/clone-viral-hypit/videos/**

## Para quién es

- **Marketing y tráfico pago:** un clip se convierte en 5 a 10 versiones para probar con poco presupuesto antes de grabar de verdad.
- **Creadores de contenido:** la misma escena en otro idioma, o contigo en el lugar del presentador, sin cámara ni estudio.

## Las tres piezas

- **[Hypit](https://github.com/hypit-ai/hypit)** — herramienta abierta que corre dentro de Claude Code: lee tu video,
  planifica uno nuevo, pide a los modelos las imágenes y los clips, pone subtítulos y monta todo en tu computadora.
- **[fal](https://fal.ai)** — servicio donde corren los modelos de imagen y de video. Pagas por imagen y por segundo.
- **Claude Code** — pides en texto; él escribe los archivos de Hypit y muestra el plan y el precio antes de gastar.

**Hypit no viene en este repositorio.** Su licencia no permite empaquetarlo; el propio Claude lo instala desde el
repositorio oficial.

## Los 3 pasos

1. **Instalar** — un mensaje instala Hypit solo en el proyecto y conecta fal leyendo la `FAL_KEY` del entorno (unos 6 min).
2. **Rehacer con tu rostro** — primer y último cuadro con tu rostro, y luego los 8 segundos entre ellos.
3. **Revisar, corregir y hacer versiones** — rostro, manos y texto; modelos premium; otro idioma; personajes ficticios.

Todo mensaje termina con **"Muéstrame el plan y el precio y no construyas nada."** — la frase que hace que Claude presupueste y
se detenga antes de gastar crédito.

## Precios (aproximados, según la tabla del 21/10/2026)

| Qué | Costo aproximado |
|---|---|
| Primera versión con tu rostro (Seedream 5 Lite + MiniMax H3 768p) | US$ 0,71 |
| Versión premium (GPT Image 2.5 + MiniMax H3 Max 1080p) | ~US$ 2 |
| Versión en otro idioma | ~US$ 2 |
| MiniMax H3 Recast 1080p (US$ 0,45/s) | US$ 3,60 por clip de 8 s · lote de 8 ≈ US$ 28,80 |
| Higgsfield Genjutsu 1080p (US$ 1,632/s, comparación) | US$ 13,06 por clip · lote de 8 ≈ US$ 104,50 |

El precio cambia: revisa las páginas antes de gastar. Recast y Genjutsu son modelos distintos; solo se comparó el precio.
Fuentes y detalles en [`kit/05-precos-e-links.md`](kit/05-precos-e-links.md) (el kit está en portugués).

## ⚠️ La regla ética

**Usa solo tu rostro, o un rostro que tengas permiso por escrito para usar. Usa solo clips tuyos, o clips que
tengas derecho a rehacer.** Nada de personas famosas, de colegas sin autorización ni de videos ajenos. Los personajes del
kit son ficticios. Si el anuncio parece un testimonio, avisa que es contenido generado por IA.

## El proceso, de principio a fin

Quién lo hace: 🧠 tú en Claude Code · ⚙️ Hypit/script · 🤖 modelos en fal.

| # | Paso | Qué hacer | Quién lo hace |
|---|---|---|---|
| 1 | Preparar | Crear la carpeta del proyecto con `references/meu-clipe.mp4`, `rosto-1.jpg`, `rosto-2.jpg` ([`kit/01-instalacao/1-o-que-precisa.md`](kit/01-instalacao/1-o-que-precisa.md)) | 🧠 |
| 2 | Guardar la clave | `export FAL_KEY="..."` en el `~/.zshrc`/`~/.bashrc`, abrir una terminal nueva; nunca en el chat ([`3-chave-fal-segura.md`](kit/01-instalacao/3-chave-fal-segura.md)) | 🧠 |
| 3 | Instalar | Pegar el mensaje de instalación en Claude Code ([`2-mensagem-de-instalacao.md`](kit/01-instalacao/2-mensagem-de-instalacao.md)); Hypit se instala con `npx skills add hypit-ai/hypit` (sin `-g`) y `@hypit/hypit` | 🧠 → ⚙️ |
| 4 | Presupuestar el primer clip | Pegar el mensaje 1 ([`kit/02-mensagens/1-refazer-com-seu-rosto.md`](kit/02-mensagens/1-refazer-com-seu-rosto.md)); Claude escribe el `.svml` y muestra plan y precio | 🧠 → ⚙️ |
| 5 | Generar las imágenes | Decir "puedes construir las imágenes"; los 2 cuadros con tu rostro salen de fal | 🤖 |
| 6 | Revisar las imágenes | Rostro, manos, texto ([`kit/04-checklists/confira-antes-de-corrigir.md`](kit/04-checklists/confira-antes-de-corrigir.md)) | 🧠 |
| 7 | Generar el video | Decir "puedes construir el clip"; fal genera los 8 s y Hypit lo monta en tu computadora | 🤖 → ⚙️ |
| 8 | Corregir | Mensaje 2 (premium), presupuestar, revisar, construir | 🧠 → 🤖 |
| 9 | Hacer versiones | Mensaje 3 (otro idioma) y/o 4 (personajes ficticios del `characters.json`) | 🧠 → 🤖 → ⚙️ |
| 10 | Probar | Correr las versiones como una sola prueba y quedarte con las que retienen más ([`teste-com-7-versoes.md`](kit/04-checklists/teste-com-7-versoes.md)) | 🧠 |

### Dónde están la guía y el video de este repositorio

| Pieza | Dónde | Quién lo hace |
|---|---|---|
| Guía (PT/EN/ES) | `guia/index.html`, `guia/en/`, `guia/es/` → https://inematds.github.io/clone-viral-hypit/guia/es/ | 🧠 (sesión INEMA) → ⚙️ GitHub Pages vía Actions |
| Video explicativo | archivo final fuera del repo; publicado como release `video-v1.0.0` (MP4 + SRT) y reproductor en `videos/` → https://inematds.github.io/clone-viral-hypit/videos/ | ⚙️ `python3 scripts/publica.py` |

## Estructura del kit

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

## Licencia de Hypit (resumen)

Hypit usa la "Hypit Open Source License" (Apache-2.0 con condiciones). En resumen: uso libre para tu trabajo y el
de tus clientes, también comercial; no puede operarse como servicio alojado o multiinquilino para terceros; no se puede
vender ni empaquetar Hypit o derivados; hay que mantener el nombre y el logo. Lo que creas es tuyo; los términos de los
proveedores de modelos siguen vigentes. Lee la licencia completa en https://github.com/hypit-ai/hypit.

## Licencia de este kit

[MIT](LICENSE) — vale solo para el texto, las plantillas de archivo y los scripts del INEMA.

---

Contenido abierto y gratuito de **[INEMA.CLUB](https://inema.club)**.
