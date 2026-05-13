---
title: "Claude Prompt - PRD Infografía Legal T1 Mundial"
doc_type: "prompt"
status: "draft"
owner: "Arturo / Parco"
version: "0.1"
last_updated: "2026-05-12"
language: "es"
audience: ["claude-code", "legal", "creative", "production"]
tags: ["legal", "infographic", "prd", "pdf", "ai-video"]
---

# Prompt Para Claude

Copia y pega esto en Claude Code desde `/Users/parco/T1mundial`:

```text
Actúa como productor ejecutivo, legal operations designer, director editorial y diseñador de información. Necesito convertir el proyecto T1 Mundial en una ficha legal interna tipo infografía premium.

Objetivo:
Crear una ficha legal de 3 páginas para revisión interna T1. Debe explicar el proyecto, mostrar el rack visual, y hacer visibles todos los cuidados/negativos legales que se están considerando antes de animar y antes del master final.

No quiero un documento corporativo pesado. Quiero una infografía editorial limpia: mucho aire, jerarquía clara, callouts, líneas que apunten a zonas del rack, copy corto, y lectura rápida para legal interno.

Inspiración visual:
- infografías editoriales tipo Behance / rough sketch process,
- Apple/Figma minimal,
- New York Times Magazine,
- producción cinematográfica premium,
- ficha técnica legal clara.

Repo:
`/Users/parco/T1mundial`

Lee primero:
1. `05_legal/t1-mundial-legal-review-brief-v001.md`
2. `05_legal/legal-checklist.md`
3. `04_production/qa/qa-checklist.md`
4. `03_creative/shot-list/current-rack-36-v005.md`
5. `00_admin/source-materials/t1-hero-film-mundial-2026-tratamiento.txt`
6. Si puedes leerlo: `00_admin/source-materials/T1_v06_Feedback_Frame_por_Frame.docx`

Assets importantes:
- Rack consolidado: `02_references/visual/Storiboard Rack OK.png`
- Stills individuales: `02_references/visual/Stills T1mundial/01.png` a `36.png`
- Model sheets aprobadas: `07_assets/characters/model-sheets/approved/` y `07_assets/locations/model-sheets/approved/`

Contexto:
T1 Mundial es un hero film cinematográfico AI-first. El proyecto ya tiene stills, narrativa, model sheets, prompts, folders y pipeline. Está entrando a producción de motion. El rack vigente tiene 36 stills, aunque el corte final puede quedar en 34-36 tomas por edición, calidad y revisión legal.

Necesito que produzcas:

1. Un PRD de diseño para la ficha legal:
   `05_legal/t1-mundial-legal-infographic-prd-v001.md`

2. Una versión Markdown de la ficha ya maquetada como 3 páginas:
   `05_legal/t1-mundial-legal-infographic-brief-v001.md`

Estructura de la ficha:

Página 1: Contexto del proyecto
- Qué es T1 Mundial.
- Qué busca comunicar.
- Qué NO busca hacer.
- Guion/VO en versión breve.
- Decisión legal principal: avanzar a motion con revisión frame por frame.

Página 2: Rack visual + callouts
- Usar placeholder para `02_references/visual/Storiboard Rack OK.png`.
- Indicar callouts alrededor del rack:
  - uniformes ficticios,
  - sin escudos ni marcas deportivas,
  - multitudes no oficiales,
  - comercios sin marcas reales,
  - pantallas con UI T1 en post,
  - estadio ficticio,
  - cierre sin claims oficiales,
  - revisión frame por frame.

Página 3: Negativos y checklist
- Todos los negativos legales en bullets claros.
- Checklist de revisión interna.
- Criterios de aprobación.
- Qué se debe corregir antes de master.

Tono:
Claro, sobrio, interno, no alarmista. Debe transmitir control. No debe sonar a paranoia ni a defensa reactiva.

Copy clave:
- “Inspirado en el contexto cultural del futbol; no asociado a torneo, federación o selección.”
- “El rack visual es punto de partida. El master se aprueba frame por frame.”
- “La regla es simple: si una toma abre duda legal, se ajusta, se reemplaza o no entra.”
- “Las pantallas se resuelven con UI T1 propia en post.”
- “Todo asset final debe ser trazable.”

Restricciones:
- No afirmes que legal ya aprobó nada.
- No elimines la necesidad de revisión legal profesional.
- No uses términos protegidos como parte del mensaje creativo, solo en secciones de negativos/prohibidos.
- No conviertas la ficha en un memo largo.
- No satures con texto.

Entrega los dos archivos Markdown y deja placeholders claros para imagen/rack si no puedes renderizar PDF.
```

