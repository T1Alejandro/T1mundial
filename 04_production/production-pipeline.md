---
title: "Production Pipeline"
doc_type: "playbook"
status: "draft"
owner: "Producer / PM"
reviewers: ["Creative Director", "Editor", "Legal PI"]
version: "0.1"
last_updated: "2026-04-28"
review_due: "2026-05-01"
language: "es"
audience: ["internal", "production", "creative", "ops"]
tags: ["pipeline", "ai-video", "post-production"]
ai_use_cases: ["workflow-planning", "handoff"]
source_of_truth: "local-project"
confidence: "medium"
assumptions: []
related_docs:
  - "tool-stack.md"
  - "next-production-roadmap-v001.md"
---

# Production Pipeline

## Flujo de punta a punta

1. Brief y referencias.
2. Shot prompt template basado 100% en el PDF.
3. Krea node graph para thumbnails y look development.
4. ElevenLabs flow para casting, intención y timing de voz.
5. Contact sheets por toma crítica.
6. Selección de thumbnails.
7. Upscale a keyframes.
8. Curaduría técnica, creativa y legal de stills.
9. Motion tests desde keyframes aprobados.
10. Image-to-video / text-to-video solo para tomas con still aprobado.
11. Ensamble en rough cut con scratch VO y música temporal.
12. Segunda ronda de generación.
13. Picture lock.
14. Música final, sound design y mezcla.
15. Color, comp, tipografía y logo.
16. Revisión legal frame por frame.
17. Masters y derivados.
18. Upload programado y tracking.

## Regla de templates

No se crea un prompt desde cero por toma. Se usa:

- `03_creative/prompts/templates/shot-prompt-template.md`
- `03_creative/prompts/templates/krea-node-template.md`

Solo cambia el `SHOT VARIABLE NODE` y las `COMPOSITION VARIANTS`, siempre basadas en el PDF del tratamiento.

## Naming convention

Usar este patrón:

`t1mundial_shot-##_descripcion_modelo_v###_yyyymmdd.ext`

Ejemplos:

- `t1mundial_shot-01_cortina_higgsfield_v001_20260428.mp4`
- `t1mundial_shot-07_dashboard-krea_still_v003_20260429.png`
- `t1mundial_master-75s_prores_v001_20260524.mov`

## Orden local para renders

Los archivos pesados pueden mantenerse localmente dentro del proyecto:

- `04_production/krea-stills/thumbnails`
- `04_production/krea-stills/selected`
- `04_production/krea-stills/keyframes`
- `04_production/krea-stills/contact-sheets`
- `04_production/ai-generations/raw`
- `04_production/ai-generations/selected`
- `04_production/ai-generations/approved-creative`
- `04_production/ai-generations/approved-legal`
- `04_production/ai-generations/final`
- `04_production/ai-generations/rejected`
- `04_production/renders/work-in-progress`
- `04_production/renders/review`
- `04_production/renders/approved`
- `04_production/renders/final`
- `04_production/audio/elevenlabs/casting`
- `04_production/audio/elevenlabs/timing`
- `04_production/audio/elevenlabs/final-candidates`
- `04_production/audio/elevenlabs/approved`
- `08_deliverables/exports/youtube`
- `08_deliverables/exports/shorts`
- `08_deliverables/exports/feeds`

## Estados de asset

- `raw`: salida directa del modelo o captura sin revisar.
- `selected`: seleccionado para pruebas.
- `approved-creative`: aprobado por dirección creativa.
- `approved-legal`: aprobado por legal.
- `final`: entra al master.
- `rejected`: descartado con razón documentada.

## Revisión obligatoria

Cada asset que pueda entrar al corte debe tener:

- Prompt o fuente.
- Modelo/herramienta.
- Fecha de generación.
- Owner.
- Estado.
- Razón de selección.
- Checklist legal.
