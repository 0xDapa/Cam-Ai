# Cam AI

Visión por cámara para dueños y gerentes de comercios y restaurantes (Venezuela primero).

**Qué hace:** analiza grabaciones largas (batch) con detección de personas y zonas, y entrega un CRM limpio con pocas decisiones económicas claras — no una lluvia de métricas.

**Qué no hace:** no guarda identidades, no estima edad ni género, no inventa ventas ni tickets.

## Cómo trabajan los agentes

- Código del pipeline: repo hermano / workspace `retail-vision` (YOLO + CRM demo).
- Aquí viven **bitácoras**, **briefs** para Grok Build y la **selección de métricas**.
- El CRM lo implementa **Grok Build (Grok 4.7)** a partir de un brief; el orquestador no escribe la UI.

## Enlaces útiles

- Video caso actual (web): Kitchen DIVE ~12 h — YouTube `BxzeQbHGsMk`
- CRM demo (túnel): ver `retail-vision/runs/crm_demo.url`
