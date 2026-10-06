# Grok Build: batch YOLO on long restaurant/commerce clips + owner intelligence

## Goal
As long fixed restaurant/commerce videos land under `data/youtube_long/`, run YOLOv8n CPU (stride 8) batch, compute dwell/zones/occupancy, and fold **owner-decision** Spanish CRM cards (máx 3 acciones, movement only, no invented sales). Prefer newest lives/VODs ≥90min. Queue multiple runs; one heavy writer at a time.

## Inputs (discover dynamically)
- `data/youtube_long/retail_live_*.mp4` when duration ≥90min
- `data/youtube_long/retail_fixed_*.mp4` not yet in `runs/`
- Skip handheld tour `retail_1h_nLHlQ8FBaqI.mp4` unless no better fixed left
- Already done: `fixed_3h_kitchendive` — enrich only if dwell pipeline says so

## Deliverables
1. Per-clip `runs/<id>/` with metrics, heatmap, dwell_visits, turno_descripcion
2. CRM primary = best restaurant case with decision value; keep tunnel
3. `outbox/RESULT_BATCH_RESTAURANT_YOLO_V1.md` progress log (append-safe)
4. $0, no Jev, no push. Local commits OK.

## Intelligence layer (Grok)
From measured movement only: staffing windows, service pressure (long dwells), zone path insights. Honest “no sabemos ventas”.

## Done when
At least one new ≥90min restaurant live/VOD fully analyzed into owner CRM beyond Kitchen DIVE 3h VOD; batch script/docs so orchestrator can keep feeding clips.
