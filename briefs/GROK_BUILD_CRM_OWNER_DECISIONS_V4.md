# Brief — CRM dueño V4: decisiones económicas reales (12h)

## Por qué
David (dueño/productor): el CRM actual del 12h es **demasiado pobre**. Dos tarjetas flojas (“refuerza en picos” / “no contrates por conteo”) **no permiten ninguna decisión importante**. Arregla eso. **Tú (Grok Build) escribes el CRM.** El orquestador no.

## Datos (NO re-correr YOLO si ya está completo)
- Run: `runs/web_12h_kitchendive/` (metrics, dwell_visits, heatmap, preview, summary)
- Video: ~11.9h Kitchen DIVE BxzeQbHGsMk, 1910 visitas, pico 11 ~21:05, rebote <15s = 827, zonas mesa/nevera/entrada
- Repo métricas: `/workspace/Cam-Ai/docs/metricas-seleccionadas.md`
- Teléfono: conservar túnel; URL en `runs/crm_demo.url`

## Qué debe sentir el dueño al abrir el teléfono
En **30 segundos** debe poder decir: “mañana de noche hago X, Y y Z” con horario y por qué en plata — sin jerga, sin percentiles, sin YOLO.

Hero = **Plan para mañana** (noche→mañana de este video), no un resumen de métricas.

## Decisiones obligatorias (3 a 5 tarjetas, todas accionables)
Cada tarjeta: **Acción concreta** | **Cuándo (hora de reloj)** | **Evidencia en 1 línea** | **En plata (sin inventar ventas)** | opcional **Qué no hacer**.

Debe cubrir al menos estos temas (reformúlalos limpio):

1. **Plan de personal por franja** (noche / madrugada / mañana): cuántas manos en la **mesa**, no “refuerza un poco”. Usa picos y minutos casi vacíos. Separar “abrir con fuerza” vs “madrugada flaca”.
2. **Preparación / stock de bentos antes del pico nocturno** (presión de servicio): si mucha gente se junta 21:23–22:03 y hay permanencias largas en mesa, la decisión es *alista producto y manos ANTES*, no reaccionar en el pico.
3. **Nevera = de paso**: no asignar persona a cuidar nevera; mesa es el cuello. Evidencia de embudo zonas (solo nevera ≈ 0–1).
4. **Rebote alto (<15s)**: qué cambia el dueño en la puerta/mesa (cartel, fila, bentos visibles al entrar, no contratar por 1910). Traducir 827/1910 a “casi la mitad no se quedó a comprar tiempo”.
5. **Madrugada**: bajar costo de personal cuando el local estuvo ~73 min con ≤1 persona — turno flaco sin desatender apertura de mañana.

Opcional 5ª: comparar “visitas que se quedan ≥5 min” vs rebote — esas son las que justifican manos en mesa.

## UI (suave, limpia, no técnica)
- Secciones claras: Plan mañana | Cuándo (barras/hora) | Zonas (embudo en lenguaje humano) | Decidir | Video | Mapa | Límites
- Timeline visual “a esta hora haz esto” (noche→mañana)
- Números enteros; horas de reloj; sin promedios con coma como héroe
- Español Venezuela (tú)
- Phone-first; menú legible

## Prohibido
- Inventar compras, tickets, conversión a venta, edad, género, identidades
- Dejar solo 2 tarjetas genéricas
- Meter jerga (YOLO, percentil, p50, track)
- Re-analizar el video entero si el run ya está completo (reusa JSON)
- Terminar el turno solo con un plan en prosa: **cada reply debe incluir tool calls hasta que exista** `outbox/RESULT_CRM_OWNER_DECISIONS_V4.md`

## Done when
- RESULT escrito con: URL teléfono, 3–5 acciones, evidencia, commit, tests OK, confirmación caso=12h
- CRM local + túnel HTTP 200
- Bitácora corta en `/workspace/Cam-Ai/bitacora/` + push si puedes
