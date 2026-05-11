---
title: "Full Production Template System"
doc_type: "playbook"
status: "draft"
owner: "Arturo / Parco"
reviewers: []
version: "0.1"
last_updated: "2026-04-28"
review_due: "2026-04-29"
language: "es"
audience: ["internal", "creative", "production"]
tags: ["template-system", "production", "krea", "higgsfield", "elevenlabs"]
ai_use_cases: ["production-system", "workflow"]
source_of_truth: "treatment-v1"
confidence: "high"
assumptions:
  - "El PDF del tratamiento es el source of truth."
related_docs:
  - "../03_creative/prompts/templates/shot-prompt-template.md"
  - "../03_creative/prompts/templates/krea-node-template.md"
---

# Full Production Template System

## Decision

No exploramos desde cero cada toma. Usamos un sistema fijo de plantillas y cambiamos solo la variable de toma.

## Flujo completo

```text
PDF Treatment Source of Truth
  -> Shot Prompt Template
  -> Krea Node Template
  -> Thumbnail Batch
  -> Contact Sheet
  -> Selection Scorecard
  -> Keyframe Upscale
  -> Higgsfield Character / Look Consistency
  -> ElevenLabs Timing / Voice Flow
  -> Motion Test
  -> Rough Cut MVP
  -> Final Shot
```

## Que cambia por toma

- Shot ID.
- Accion especifica.
- Camara/composicion.
- Objetos principales.
- Riesgo legal especifico.
- Variantes de composicion.

## Que NO cambia

- Tesis del film.
- Voz T1.
- Barra cinematografica.
- Negativos legales.
- Output inicial como thumbnail.
- Scorecard de seleccion.
- Naming convention.
- Regla: no animar sin still aprobado.

## Templates base

| Template | Uso |
|---|---|
| `03_creative/prompts/templates/shot-prompt-template.md` | Ficha universal de toma. |
| `03_creative/prompts/templates/krea-node-template.md` | Graph reusable para Krea. |
| `03_creative/prompts/krea-patch-v001.md` | Patch maestro ya poblado con shots prioritarios. |
| `03_creative/prompts/shot-01-cortina-template.md` | Primera toma lista para Krea. |
| `03_creative/prompts/shot-03-tianguis-template.md` | Toma comercio lista para Krea. |

## Loop de iteracion

1. Generar 12-24 thumbnails.
2. Guardar en `04_production/krea-stills/thumbnails`.
3. Hacer contact sheet.
4. Puntuar con scorecard.
5. Pasar 3-5 a `selected`.
6. Upscale 1-2 a keyframe.
7. Revisar legal.
8. Motion test.
9. Rough cut.

## Naming

```text
t1mundial_krea_shot-##_variant-##_v###_yyyymmdd.png
t1mundial_keyframe_shot-##_v###_yyyymmdd.png
t1mundial_motiontest_shot-##_v###_yyyymmdd.mp4
```

## Primer fire

Empezar con:

- Shot 01 - Cortina.
- Shot 03 - Tianguis QR.

Razones:

- Shot 01 define el tono cinematografico del film.
- Shot 03 define si T1/comercio se siente humano, mexicano y premium.

