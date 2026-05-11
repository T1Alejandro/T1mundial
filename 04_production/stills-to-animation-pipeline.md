---
title: "Stills to Animation Pipeline"
doc_type: "playbook"
status: "draft"
owner: "Arturo / Parco"
reviewers: []
version: "0.1"
last_updated: "2026-04-28"
review_due: "2026-04-30"
language: "es"
audience: ["internal", "creative", "production"]
tags: ["stills", "animation", "pipeline", "ai-video"]
ai_use_cases: ["pipeline-planning", "shot-production"]
source_of_truth: "local-project"
confidence: "medium"
assumptions: []
related_docs:
  - "krea-node-stills-workflow.md"
  - "production-pipeline.md"
---

# Stills to Animation Pipeline

## Fase 1: Thumbnail

Objetivo: variedad rápida.

- Tamaño pequeño.
- Muchas opciones.
- Sin obsesión por detalle.
- Enfoque en composición, emoción y lectura.

Salida:

- Contact sheet por toma.
- 3-5 favoritos por shot crítico.

## Fase 2: Keyframe

Objetivo: imagen base animable.

- Upscale 16:9.
- Limpieza de texto y marcas.
- UI T1 propia.
- Personajes consistentes.
- Evaluación legal.

Salida:

- 1-2 keyframes por toma.

## Fase 3: Motion Test

Objetivo: validar si la imagen puede moverse.

- Animar 3-5 segundos.
- Probar cámara, gesto y continuidad.
- No buscar final todavía.

Salida:

- Motion test aprobado o descartado.

## Fase 4: Shot Candidate

Objetivo: toma candidata para rough cut.

- Duración cercana a final.
- Ritmo compatible con VO.
- Export para edición.
- Revisión AI/legal.

Salida:

- Shot candidate en `04_production/ai-generations/selected`.

## Fase 5: Final Shot

Objetivo: toma lista para master.

- Color y comp.
- Legal aprobado.
- Sin artefactos AI.
- Export a specs del timeline.

Salida:

- Shot final en `04_production/ai-generations/final`.

## Regla de avance

Ningún shot pasa de still a animación si:

- No tiene still aprobado.
- Tiene riesgo legal sin resolver.
- No aporta a la historia.
- No se lee rápido.
- Parece genérico.

