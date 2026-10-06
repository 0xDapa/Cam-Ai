# Bitácora — 2026-10-06 ~18:00–18:01 VET

## Feedback de David (~18:00)
Rechazó **CRM V5 hard**. Capturas del dashboard. Gist: quizás YOLO es el problema, pero esto está **estupidalmente mal** — **"bentos"**, **"apretón"**, **"pagues el hueco"** son basura y **no dan info usable**.

Quiere:
1. Decisiones en **español claro** (tú Venezuela) — sin slang / metáfora.
2. **Dark mode only** (`#0f1115`). Sin light.
3. Ocupación por hora **más visual** con hover.
4. Sin ventas inventadas.

## Aclaración (~18:01)
**No basta “más limpio”.** Escribir como para un **niño de 5 años** que quiere saberlo todo pero no conoce jerga: gente, mesa, nevera, hora, quedarse, irse. **~8 palabras máx por chip.** Sin slang.

Web **HTML interactiva**:
- Hover/tap barras ocupación → hora + cuántas personas
- Tap chips del plan → una razón corta (“por qué”)
- Tap mesa / nevera / rebote → explicación corta
Dark mode sigue obligatorio.

## Acción
- Brief: `retail-vision/briefs/GROK_BUILD_CRM_DARK_PLAIN_V6.md`
- Addendum: `retail-vision/outbox/GROK_V6_ADDENDUM_SIMPLE_INTERACTIVE.md`
- RESULT: `retail-vision/outbox/RESULT_CRM_DARK_PLAIN_V6.md`
- Reuso YOLO: `runs/web_12h_kitchendive/` (NO re-YOLO)
- Grok fresco `--always-approve` (un solo writer); CRM `:8765` + túnel existente
