# Bitácora — 2026-10-06 ~18:00 VET

## Feedback de David
Rechazó **CRM V5 hard**. Capturas del dashboard (video centro + chips + ocupación). Gist: quizás YOLO es el problema, pero esto está **estupidalmente mal** — **"bentos"**, **"apretón"**, **"pagues el hueco"** son basura y **no dan info usable**.

Quiere:
1. Decisiones en **español claro** (tú Venezuela) — sin slang / metáfora.
2. **Dark mode only** (`#0f1115`, cards oscuras, texto claro). Sin light.
3. Ocupación por hora **más visual** — SVG/barras; hover = hora + máx. personas + tip (refuerza / normal / baja).
4. Sin ventas inventadas.

## Acción
- Brief: `retail-vision/briefs/GROK_BUILD_CRM_DARK_PLAIN_V6.md`
- RESULT esperado: `retail-vision/outbox/RESULT_CRM_DARK_PLAIN_V6.md`
- Reuso YOLO: `runs/web_12h_kitchendive/` (NO re-YOLO)
- Layout V5 (video centro + lados) se mantiene; chips reescritos literal; tema dark; occupancy con tooltip
- Grok fresco `--always-approve` (un solo writer); CRM `:8765` + túnel existente
