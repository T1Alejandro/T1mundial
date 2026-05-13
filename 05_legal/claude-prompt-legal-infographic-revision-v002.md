---
title: "Claude Prompt - Revision Infografia Legal T1 Mundial v002"
doc_type: "prompt"
status: "draft"
owner: "Arturo / Parco"
version: "0.2"
last_updated: "2026-05-12"
language: "es"
audience: ["claude-code", "legal", "creative", "production"]
tags: ["legal", "infographic", "revision", "prd", "ai-video"]
---

# Prompt De Corrección Para Claude

```text
Necesito que corrijas y rehagas la ficha legal infográfica de T1 Mundial con mucha más precisión factual.

IMPORTANTE:
La versión anterior funciona como estructura visual, pero tiene errores que NO pueden pasar a legal:

1. No inventes guion/VO. Usa el guion real del tratamiento o una versión condensada fiel.
2. No digas "rack aprobado legalmente" ni "aprobado visualmente" si no está aprobado por legal. Usa "rack vigente" o "source of truth visual".
3. No conviertas el proyecto en una pieza sobre "pantallas" o transmisión. T1 Mundial conecta preparación deportiva ficticia y comercios mexicanos / ecosistema T1.
4. No dejes los negativos genéricos. Usa la lista completa de negativos legales y visuales.
5. No trates el feedback v06 como pendiente viejo; úsalo como aprendizaje incorporado al criterio actual.

Trabaja desde:
`/Users/parco/T1mundial`

Lee y usa como fuentes principales:

1. `05_legal/t1-mundial-legal-review-brief-v001.md`
2. `05_legal/legal-checklist.md`
3. `04_production/qa/qa-checklist.md`
4. `03_creative/shot-list/current-rack-36-v005.md`
5. `00_admin/source-materials/t1-hero-film-mundial-2026-tratamiento.txt`
6. `00_admin/source-materials/T1_v06_Feedback_Frame_por_Frame.docx`

Assets:

- Rack consolidado: `02_references/visual/Storiboard Rack OK.png`
- Stills vigentes: `02_references/visual/Stills T1mundial/01.png` a `36.png`

Rehaz estos dos archivos:

1. `05_legal/t1-mundial-legal-infographic-prd-v002.md`
2. `05_legal/t1-mundial-legal-infographic-brief-v002.md`

Formato deseado:
Ficha interna de 3 páginas, pensada para legal interno T1.

Página 1 - Contexto

Debe decir:

- T1 Mundial es un hero film AI-first de 60-75s aproximados.
- Rack vigente: 36 stills.
- Corte final esperado: 34-36 tomas según edición, calidad y legal.
- La pieza conecta futbol ficticio y comercio mexicano.
- No busca asociación oficial con FIFA, Copa del Mundo, Selección Mexicana, FMF, clubes, jugadores, marcas deportivas, estadios reales ni transmisiones oficiales.
- El guion evita términos protegidos.

Usa una condensación fiel del guion real, por ejemplo:

"Hay días que no son como los demás. Días donde uno se prepara para algo grande. Donde cada movimiento cuenta. Hay quien estudia al rival. Hay quien estudia el mercado. Hoy todo México juega. Once en la cancha. Millones en las suyas. Todo México es uno. Todo en uno. T1."

Página 2 - Rack visual + callouts

Debe incluir placeholder grande para:

`02_references/visual/Storiboard Rack OK.png`

Callouts alrededor del rack:

- Uniformes ficticios: sin escudos, sponsors, números oficiales ni marcas.
- Multitudes no oficiales: ropa civil/diversa, sin jerseys homogéneos de selección.
- Estadio ficticio: no replicar arquitectura reconocible.
- Comercio sin marcas reales: tiendas, empaques y fondos limpios.
- Pantallas: UI T1 propia en post, sin apps o medios de pago de terceros.
- Cierre: sin claims oficiales, sin asociación con torneo.
- Motion: cada clip se revisa después de animar, porque AI puede inventar logos/texto.
- Master final: revisión frame por frame obligatoria.

Página 3 - Negativos completos + checklist

Incluye los negativos completos de:
`05_legal/t1-mundial-legal-review-brief-v001.md`

Debe cubrir explícitamente:

- No FIFA.
- No World Cup.
- No Copa del Mundo.
- No Mundial en contexto deportivo.
- No México 2026 en contexto deportivo.
- No Selección Mexicana.
- No El Tri.
- No FMF.
- No escudos oficiales.
- No trofeo oficial.
- No mascota oficial.
- No slogans oficiales.
- No uniformes oficiales.
- No combinación dominante verde + blanco + rojo que evoque Selección.
- No marcas deportivas.
- No estadios reales.
- No atletas reales o celebridades.
- No marcas de pagos, marketplaces, paquetería o consumo.
- No UI de terceros.
- No QR real.
- No texto inventado o ilegible.
- No música o samples sin licencia.
- No voces sin cesión/comercial rights.

Tono:

- Claro.
- Sobrio.
- Legal interno.
- No alarmista.
- No defensivo.
- Visualmente limpio.
- Copy corto.

Copy clave:

- "Inspirado en el contexto cultural del futbol; no asociado a torneo, federación o selección."
- "El rack visual es punto de partida. El master se aprueba frame por frame."
- "Si una toma abre duda legal, se ajusta, se reemplaza o no entra."
- "Las pantallas se resuelven con UI T1 propia en post."
- "Todo asset final debe ser trazable."

Restricciones:

- No inventes texto creativo.
- No afirmes aprobación legal.
- No uses términos protegidos como mensaje de campaña; solo en secciones de negativos/prohibidos.
- No hagas un memo largo.
- No satures de texto.
- No ocultes que el documento no sustituye revisión legal profesional.

Entrega los archivos Markdown v002.
```

