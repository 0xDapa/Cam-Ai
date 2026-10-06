# Bitácora — 2026-10-06 ~17:44 VET

## Feedback de David
Aclaró: el problema **NO** es solo si el UI se ve bien — **los DATOS son basura**. Labels como **"bongo"** y **"nudo"** no tienen sentido; muchas métricas son ruido raro sin info de decisión.

## Reglas (superficie de datos)
- Quitar zonas/etiquetas que un dueño de kiosco VE no entendería (bongo, nudo, jerga, auto-nombres).
- Mostrar solo: ocupación por hora de reloj; mesa vs nevera; rebote &lt;15s vs ≥2min / ≥5min; las 5 acciones de reloj de V4.
- Métrica rara / sparse / sin explicación → ocultar. Ruido = borrado del CRM.
- Sin ventas inventadas. Español tú.

## Acción
Addendum en `retail-vision/briefs/GROK_BUILD_CRM_VIDEO_CENTER_V5.md` + `outbox/GROK_V5_ADDENDUM_NOISE.md`.
Grok V5 (pid 733651, early) killed; relaunch fresco con brief actualizado → pid en `outbox/grok_crm_video_center_v5.pid`.
RESULT sigue: `outbox/RESULT_CRM_VIDEO_CENTER_V5.md`.
