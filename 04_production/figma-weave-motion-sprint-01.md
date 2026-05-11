---
title: "Figma Weave Motion Sprint 01"
doc_type: "test-plan"
status: "draft"
owner: "Arturo / Parco"
reviewers: []
version: "0.1"
last_updated: "2026-05-06"
language: "es"
audience: ["internal", "creative", "production"]
tags: ["figma-weave", "wave", "weavy", "motion-test", "ai-video", "consistency"]
source_of_truth: "local-project"
confidence: "medium"
related_docs:
  - "next-production-roadmap-v001.md"
  - "still-audit-t1mundial-v001.md"
  - "global-motion-rules-v001.md"
  - "camera-animation-bible-36-v001.md"
  - "edit-decision-map-v001.md"
  - "transition-preflight-chat-prompt-v001.md"
  - "weave-first-6-manual-patch-v001.md"
  - "weave-first-6-flow-blueprint-v001.json"
  - "wave-figma-first-6-prompt-pack-v001.md"
  - "../03_creative/prompts/chatgpt-master-rack-36-v004.md"
  - "../02_references/visual/Stills T1mundial"
---

# Figma Weave Motion Sprint 01

## Objetivo

Probar si Figma Weave / Wave puede sostener consistencia visual usando los primeros 6 stills oficiales como anclas y generar una microsecuencia cinematografica consistente.

## Criterio De Exito

El sprint funciona si logramos:

- 6 clips cortos consistentes.
- Movimiento cinematografico con camara dinamica.
- Sin texto, marcas, logos, equipos reales ni UI generada.
- Rostros, vestuario, locaciones y color cercanos al still.
- Un rough cut mostrable de apertura, aunque no sea master final.

## Set Inicial Confirmado

| Shot | Archivo | Funcion en satelite | Movimiento sugerido |
|---|---|---|---|
| 01 | `02_references/visual/Stills T1mundial/01.png` | Apertura / tono | Push-in lento, textura metal, respiracion de luz. |
| 02 | `02_references/visual/Stills T1mundial/02.png` | Mundo futbol | Dolly lateral o low-angle push, profundidad de campo. |
| 03 | `02_references/visual/Stills T1mundial/03.png` | Joven / ascenso urbano | Dolly trasero ascendente, mochila roja como ancla. |
| 04 | `02_references/visual/Stills T1mundial/04.png` | Rima futbol / ascenso al campo | Dolly bajo desde atras, tachones y concreto. |
| 05 | `02_references/visual/Stills T1mundial/05.png` | Joven emerge a la ciudad | Push-in frontal leve, contra-picada suave, rostro estable. |
| 06 | `02_references/visual/Stills T1mundial/06.png` | Transformacion a estadio | Push-in frontal con tilt minimo hacia gradas, escala creciente. |

## Setup Del Canvas

Seguir el patch manual:

```text
04_production/weave-first-6-manual-patch-v001.md
```

Crear un proyecto/canvas con estos bloques:

1. Reference board con los 36 stills oficiales.
2. Global style node con el ADN del prompt maestro.
3. Negative prompt global.
4. Motion direction node.
5. Un branch por toma: `shot-01` a `shot-06`.
6. Output comparativo por toma: `v001`, `v002`, `v003`.
7. Review board con winners y rechazos.
8. Timeline board para revisar continuidad 01-06 en secuencia.

## Global Style Node

```text
Cinematic Mexican commerce and football parallel world, grounded realism, authorial commercial film, natural light, warm practicals, soft analog highlight rolloff, fine grain, lifted blacks, textured skin, fabric, metal, cardboard, concrete, grass, dust in the air, restrained color, human dignity, emotional but not patriotic, no stock advertising look.
```

## Motion Direction Node

```text
Create cinematic camera movement from the provided still reference. Preserve the original composition, character identity, wardrobe, environment, lighting, color palette and lens language. Use dynamic but controlled film movement: slow push-in, subtle dolly, short pan, rack focus, natural handheld tension, shallow depth of field, realistic motion blur. Keep movement elegant and purposeful. Do not invent new objects, logos, text, UI, brands, team symbols or readable screens.
```

## Negative Motion Node

```text
no text, no captions, no labels, no logos, no brands, no trademarks, no readable screen, no generated UI, no app icons, no numbers, no map labels, no sports brand marks, no official uniforms, no real team symbols, no FIFA, no World Cup, no Mexico 2026, no national flag, no national emblem, no celebrity likeness, no real athlete likeness, no distorted hands, no extra fingers, no warped faces, no flicker, no chaotic morphing, no fake blur, no excessive lens flare, no plastic skin, no HDR look.
```

## Prompt Base Por Toma

Usar el paquete final:

```text
04_production/wave-figma-first-6-prompt-pack-v001.md
```

El prompt pack ya contiene los prompts especificos de `shot-01` a `shot-06`, todos en ingles para maximizar compatibilidad con modelos de video dentro de Weave.

## Matriz De Evaluacion

| Clip | Respeta still | Camara | Identidad | Legal | Pantallas | Artefactos | Costo/creditos | Veredicto |
|---|---|---|---|---|---|---|---|---|
| shot-01-v001 | TBD | TBD | TBD | TBD | TBD | TBD | TBD | TBD |
| shot-02-v001 | TBD | TBD | TBD | TBD | TBD | TBD | TBD | TBD |
| shot-03-v001 | TBD | TBD | TBD | TBD | TBD | TBD | TBD | TBD |
| shot-04-v001 | TBD | TBD | TBD | TBD | TBD | TBD | TBD | TBD |
| shot-05-v001 | TBD | TBD | TBD | TBD | TBD | TBD | TBD | TBD |
| shot-06-v001 | TBD | TBD | TBD | TBD | TBD | TBD | TBD | TBD |

## Decision Despues Del Sprint

- Si Weave sostiene consistencia: producir satelite completo ahi.
- Si Weave sirve para organizar pero no para final: usarlo como board/orquestador y exportar tomas ganadoras desde el modelo que mejor funcione.
- Si Weave consume demasiados creditos: limitarlo a tomas hero y usar Seedance/Kling/Runway para variaciones.
- Si la AI rompe pantallas: bloquear pantallas blancas y resolver todo en post.
