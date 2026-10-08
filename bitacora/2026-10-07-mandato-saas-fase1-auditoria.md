# 2026-10-07 — Mandato SaaS de David · Fase 1: auditoría + P0 eventos

## Qué pidió David
Convertir CamAI de dashboard de cámaras a plataforma de inteligencia operativa para tiendas, minimarkets, supermercados y farmacias (Venezuela). Datos fiables, nada inventado, auditar qué significan las 1.910 "visitas", Grok Build como constructor, entregas pequeñas y probadas. "YOLOv8 funciona pero la información es pobre; hay más modelos viables, no te rindas."
Texto guardado en `retail-vision/briefs/DAVID_MANDATO_SAAS_2026-10-07.md`.

## Hallazgos clave de la auditoría
- **1.910 "visitas" = tramos de seguimiento, no personas.** 9.733 ids de ByteTrack + 3.105 cajas sueltas → 2.478 cadenas → 1.910 que duran ≥ 1 s. Incluye personal y regresos. Solo 491 nacen en la puerta; 461 nacen a mitad del cuadro. Rango honesto de llegadas: ~930–1.650.
- El titular de la V13 "70 % se fue en menos de 1 minuto" está inflado por cortes del tracker (30 % de los tramos duran < 10 s).
- A ojo: con poca gente el conteo es bueno; con local lleno el tracker se queda corto 30–50 %.
- El "video de supermercado de 1 h" es un recorrido con cámara en mano: inservible (contó fotos de un cartel como personas).
- Cola de caja: no fiable en Kitchen DIVE; parcialmente factible en Aisle Life (cámara detrás de la caja); imposible en el recorrido.
- Ultralytics/YOLOv8 es AGPL-3.0: decisión de licencia pendiente antes de vender.
- Rendimiento: 6–9 min de CPU por hora de video (stride 8), RAM pico ~1 GB en 2 min de video.

## Qué se hizo
- Tag `v13-claridad`, rama `saas-p0`, V13 y demo intactas.
- Documentos en retail-vision: CAMAI_AUDIT, CAMAI_ARCHITECTURE, CAMAI_ROADMAP, CAMAI_IMPLEMENTATION_LOG, CAMAI_VALIDATION.
- P0 delegado a Grok Build: base de datos de eventos (SQLite lista para Postgres), exportador del run de 12 h, métrica de fragmentación, pruebas.

## Cierre Fase 1 (~10:00 PM VET)
- David pidió arquitectura híbrida (Motor A detector+tracker, B reglas/temporal, C VLM local en clips) y todo en esta máquina → esquema v3 agnóstico al detector: `evidence_source` por evento, detector/tracker por trabajo, tabla `vlm_interpretation` (abstención, solo local).
- Commits en retail-vision rama `saas-p0`: 95492e2 (BD de eventos + rango de fragmentación), fecde99 (esquema agnóstico + VLM aparte). 75 pruebas pasan. V13 intacta (tag `v13-claridad`), :8765 responde 200.
- El 12 h quedó en SQLite: 59.866 eventos, 33 métricas; llegadas estimadas 926–1.646 (inferencia sin validar).
- Tunnelmole gratuito murió dos veces (12 h y caída); nuevo enlace en `runs/crm_demo.url`.
