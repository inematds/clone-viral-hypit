# Preços e links

> **Preços de tabela lidos em 21/10/2026. Eles mudam.** Abra as páginas antes de gastar. Os valores do kit são
> aproximados e calculados a partir dessas tabelas; o INEMA não mediu esses custos rodando o pipeline.

## Tabela

| O quê | Preço (21/10/2026) | Fonte |
|---|---|---|
| MiniMax H3 Recast no fal | US$ 0,30/s em 768p; **US$ 0,45/s em 1080p** (imagens de referência sem custo) | https://fal.ai/models/minimax/h3-max/recast |
| Um clipe de Recast de 8 s em 1080p | **US$ 3,60** | conta: 8 × US$ 0,45 |
| Lote de 8 clipes de Recast em 1080p | **≈ US$ 28,80** | conta: 8 × US$ 3,60 |
| GPT Image 2.5 (edição) no fal | cerca de US$ 0,006 a US$ 0,055 por imagem, conforme a qualidade, mais cerca de US$ 0,01 por imagem de referência | https://fal.ai/models/openai/gpt-image-2.5/sunburst/edit |
| Higgsfield Genjutsu (comparação) | US$ 0,318/s em 480p; US$ 0,681/s em 720p; **US$ 1,632/s em 1080p**, antes de descontos | https://open.higgsfield.ai/models/higgsfield/genjutsu/motion-transfer/v1.0/playground |
| Um clipe de Genjutsu de 8 s em 1080p | **≈ US$ 13,06** | conta: 8 × US$ 1,632 |
| Lote de 8 clipes de Genjutsu em 1080p | **≈ US$ 104,50** | conta: 8 × US$ 13,06 |
| Hypit | grátis (código aberto, licença própria) | https://github.com/hypit-ai/hypit |
| Claude Code | o seu plano do Claude | https://claude.com/claude-code |

## Quanto sai cada etapa (aproximado, pela tabela de 21/10/2026)

| Etapa | Modelos | Custo aproximado |
|---|---|---|
| Primeira versão com o seu rosto | Seedream 5 Lite + MiniMax H3 768p | **US$ 0,71** |
| Versão premium | GPT Image 2.5 máx. + MiniMax H3 Max 1080p, 3 quadros | **~US$ 2** |
| Nova língua | tradução, voz, Whisper, lip sync, legenda | **~US$ 2** |
| Cada personagem (Recast 8 s 1080p) | GPT Image 2.5 + H3 Recast | **US$ 3,60** + centavos da foto |

## Recast × Genjutsu

Em 1080p, o preço de tabela do Genjutsu é cerca de **3,6 vezes** o do Recast (lote de 8: US$ 104,50 contra
US$ 28,80). São **modelos diferentes** e a **qualidade não foi comparada** aqui: a tabela compara só preço.

## Licença do Hypit (resumo — leia a licença completa no repositório dele)

- Uso livre para o seu trabalho e para trabalho de clientes, **inclusive comercial**.
- **Não** pode operar o Hypit como serviço hospedado ou multi-inquilino para terceiros.
- **Não** pode vender, empacotar ou redistribuir o Hypit (ou derivado) com fins comerciais.
- **Manter** o nome, o logo e os créditos do Hypit onde ele os mostra.
- O que você cria é seu; os termos dos provedores de modelo (fal etc.) continuam valendo.
