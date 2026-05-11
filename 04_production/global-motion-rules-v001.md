---
title: "Global Motion Rules"
doc_type: "prompt-bible"
status: "draft"
owner: "Arturo / Parco"
reviewers: []
version: "0.1"
last_updated: "2026-05-06"
language: "es"
audience: ["internal", "creative", "production"]
tags: ["motion", "transition", "negative-rules", "ai-video", "mvp"]
source_of_truth: "local-project"
confidence: "medium"
related_docs:
  - "transition-preflight-risk-framework-v001.md"
  - "edit-decision-map-v001.md"
  - "figma-weave-motion-sprint-01.md"
  - "../03_creative/prompts/chatgpt-master-rack-36-v004.md"
---

# Global Motion Rules

## Filosofia MVP

El objetivo no es resolver todo perfecto en AI. El objetivo es encontrar rapido que tomas/transiciones son viables, cuales necesitan prompt mas preciso, cuales necesitan frame puente y cuales conviene resolver en post.

Regla de produccion:

```text
No gastar renders caros hasta saber el riesgo de transicion.
```

## Motion Positive Rules

Priorizar:

- Movimiento fisico de camara.
- Match por pies, manos, objetos, paredes, piso, lineas, sombras, luz, polvo, textura o silueta.
- Occlusion natural: una pared, puerta, cortina, cuerpo, sombra, objeto o cambio de plano tapa el frame y revela el siguiente espacio.
- Morph controlado de materiales y geometria: metal a concreto, piso a tunel, pared a grada, luz de cortina a contraluz de estadio.
- Continuidad de eje de camara.
- Continuidad de direccion de movimiento.
- Match cut espacial.
- One continuous impossible physical shot.
- Si el match es dificil: usar frame puente antes de forzar una transicion directa.

## Motion Hard Negatives

Prohibido en todas las herramientas:

```text
no fade, no fade out, no fade in, no semi fade, no dissolve, no semi dissolve, no crossfade, no opacity blend, no semi-transparent background blend, no background dissolve, no black frame, no white flash, no hard cut disguised as transition, no generic transition, no slideshow transition, no montage transition, no abstract wipe, no easy transition, no lazy transition, no scene dissolving into another scene, no background fading away, no music unless requested, no score, no trailer music, no beat, no announcer, no voiceover unless requested
```

## Si El Modelo No Puede Resolver

No permitir que invente fade. Debe escoger una de estas salidas:

1. Movimiento de camara mas simple.
2. Match por objeto o textura.
3. Occlusion fisica.
4. Frame puente.
5. Mantener first frame y hacer solo camera move.

Prompt rule:

```text
If the transition is difficult, do not use fade, dissolve, crossfade or opacity blending. Instead, solve through physical occlusion, matching geometry, material transformation, or reduce the motion to a simpler camera move.
```

## Audio Rules

Default:

```text
audio off
```

Si se genera audio:

- Solo ambiente natural.
- Room tone.
- Pasos.
- Cortina metalica.
- Ambiencia distante.
- Sonido incidental diegetico.

Prohibido:

```text
no music, no score, no soundtrack, no trailer music, no beat, no cinematic boom, no announcer, no voiceover, no chant, no crowd song
```

## Regla Para N Tomas

Para una secuencia de N tomas, no evaluar solo toma por toma. Evaluar pares:

```text
01 -> 02
02 -> 03
03 -> 04
04 -> 05
05 -> 06
```

Despues evaluar tripletas si hay transicion compleja:

```text
01 -> 02 -> 03
03 -> 04 -> 05
04 -> 05 -> 06
```

Cada pair debe tener:

- punto fisico de match
- movimiento de camara recomendado
- riesgo de fade/dissolve
- necesidad de frame puente
- prompt corto de transicion

## Prompt Block Reutilizable

Pegar en cualquier herramienta de video:

```text
GLOBAL MOTION RULES:
Do not use fade, fade out, fade in, dissolve, crossfade, opacity blend, semi-transparent background blend, black frame, white flash, hard cut, slideshow transition, montage transition or generic transition. Never solve the transition by fading one scene into another.

Solve transitions only through physical camera movement, occlusion, matching geometry, matching body parts, matching objects, material transformation, light continuity, shadow continuity, floor lines, wall lines, texture, depth of field or a clear match cut. If the transition is too difficult, simplify the camera movement or require an intermediate bridge frame. Keep it as one continuous impossible physical shot.

Audio off by default. If audio is generated, use only natural ambience and incidental diegetic sound. No music, no score, no beat, no voiceover, no announcer.
```
