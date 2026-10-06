# Bitácora — 2026-10-06 ~19:30 VET

## Feedback de David (CRM V7)
«Esta mejor pero asimétrico en los lados y sin tanta congruencia en los datos, la parte de personal por horas es rara.»

Mejoras respecto a V6 (AM/PM, glass, data real) — pero:
1. **Lados asimétricos** — izquierda y derecha no se ven equilibrados.
2. **Datos poco congruentes** — los números no cuentan la misma historia entre sí (ocupación / personal / rebote / mesa).
3. **Personal por horas raro** — franjas tipo 8:43 PM–10:23 PM / 2:43–4:03 AM y saltos 3→2→1→2→2 que no se leen claros.

## Acción
- Brief: `retail-vision/briefs/GROK_BUILD_CRM_SYMMETRY_STAFF_V8.md`
- RESULT: `retail-vision/outbox/RESULT_CRM_SYMMETRY_STAFF_V8.md`
- Reuso YOLO: `runs/web_12h_kitchendive/` (NO re-YOLO)
- Mantener V7 wins: AM/PM only, liquid-glass dark, sin slang, sin En vivo/LIDAR/YOLO theater, sin ventas inventadas
- Grok fresco `--always-approve` (un solo writer); CRM `:8765` + túnel existente
- Screenshots: `outbox/crm_v8_desktop.png`, `outbox/crm_v8_mobile.png`
