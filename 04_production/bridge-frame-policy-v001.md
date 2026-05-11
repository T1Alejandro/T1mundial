---
title: "Bridge Frame Policy"
doc_type: "production-rule"
status: "draft"
owner: "Arturo / Parco"
reviewers: []
version: "0.1"
last_updated: "2026-05-06"
language: "es"
audience: ["internal", "creative", "production"]
tags: ["bridge-frame", "transition", "preflight", "ai-video"]
source_of_truth: "transition-preflight-chat-prompt-v001.md"
confidence: "medium"
related_docs:
  - "transition-preflight-chat-prompt-v001.md"
  - "global-motion-rules-v001.md"
  - "edit-decision-map-v001.md"
---

# Bridge Frame Policy

## Regla

No crear frame puente por ajustes menores.

Crear o proponer frame puente solo si:

- El score de riesgo es `24+`.
- El cambio de composicion/camara/fondo es demasiado grande.
- No hay punto fisico de match claro.
- El modelo probablemente resolveria con fade/dissolve/crossfade.
- La transicion es importante para narrativa y no conviene resolverla con corte editorial.

## Si No Hace Falta

Si el par tiene match claro:

- pies
- manos
- piso
- pared
- lineas
- luz
- textura
- silueta
- direccion de movimiento

Entonces no crear bridge frame. Usar prompt de video o corte editorial.

## Output Del Preflight

Cuando el preflight recomiende bridge frame, debe entregar:

1. razon concreta
2. descripcion visual
3. prompt de imagen
4. como usarlo: `A -> bridge -> B`
5. riesgo que resuelve

## Ejemplo

```text
Pair: 05 -> 06
Frame puente: si
Razon: mismo personaje frontal, pero el cambio de fondo ciudad -> estadio es alto y puede caer en dissolve.
Bridge: mismo joven en contraluz, fondo urbano empezando a abrirse en geometria de gradas ficticias, sin fade, sin logos.
Uso: 05 -> bridge -> 06
```
