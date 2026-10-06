# Brief — CRM web longest (≥5h / ~12h Kitchen DIVE) — Grok Build 4.7

## Goal
David wants a **super complete** owner CRM on the **longest web video** (min 5 hours). Implement via Grok Build only. Primary clip: `data/youtube_long/retail_fixed_kitchendive_BxzeQbHGsMk_12h.mp4` (~11.9 h, YouTube BxzeQbHGsMk). Repo docs: GitHub `0xDapa/Cam-Ai` (`docs/metricas-seleccionadas.md`).

## You must
1. Run YOLO (+ tracking, zones mesa/nevera/entrada, dwell, occupancy series) on the full ~12h file into `runs/web_12h_kitchendive/` (CPU yolov8n stride 8 imgsz 640 OK; long run expected).
2. Rebuild phone CRM as **primary case** this video: limpia, UI suave, visual, entendible, **no jerga técnica**. Classify sections clearly (Qué pasó / Cuándo / Zonas / Decidir / Video / Mapa / Límites).
3. Surface selected metrics from Cam-Ai docs (aforo, picos con hora, valles, permanencia + buckets, rebote <15s, por zona, heatmaps, embudo zonas, franjas, sugerencia de personal por franja). **≤5 action cards** económicas claras + bloque “Esto no sabemos”.
4. Never invent sales/compras/tickets; no age/gender/identity.
5. Spanish Venezuela (tú). Restart CRM on `:8765`; keep/update `runs/crm_demo.url` tunnel.
6. Tests green; commit; write `outbox/RESULT_CRM_WEB_LONGEST_V1.md` with URL, visit counts, peak, actions, commit hash.
7. Optionally append a short bitácora note under `/workspace/Cam-Ai/bitacora/` and push to origin if git remote works.

## Forbidden
- Ending turn with only a plan sentence (every reply must include tool calls until RESULT exists)
- Using the old 3h cut as primary
- Jev, inventing purchases, dumping raw percentiles as the hero UI

## Done when
RESULT file exists, CRM HTTP 200 local + tunnel, phone layout readable, ≥5h analysis reflected in UI.
