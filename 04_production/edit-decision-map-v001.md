---
title: "Edit Decision Map"
doc_type: "editorial-map"
status: "draft"
owner: "Arturo / Parco"
reviewers: []
version: "0.1"
last_updated: "2026-05-06"
language: "es"
audience: ["internal", "creative", "production", "editorial"]
tags: ["editing", "sequence", "transitions", "ai-video", "mvp"]
source_of_truth: "local-project"
confidence: "medium"
related_docs:
  - "global-motion-rules-v001.md"
  - "bridge-frame-policy-v001.md"
  - "transition-preflight-chat-prompt-v001.md"
  - "preflight-01-06-v001.md"
  - "figma-weave-motion-sprint-01.md"
---

# Edit Decision Map

## Objetivo

Tener vision de secuencia completa antes de renderizar todas las tomas. No todas las uniones deben ser transiciones generativas continuas. Algunas deben ser cortes de edicion.

## Filosofia

La pregunta no es solo:

```text
Como hago que toma A se transforme en toma B?
```

La pregunta editorial es:

```text
Que tipo de union necesita la historia en este punto?
```

Opciones:

- Corte directo.
- Match cut.
- Cut on action.
- J-cut / L-cut de audio.
- Whip pan.
- Occlusion wipe fisico.
- Rack focus transition.
- Morph material/controlado.
- Frame puente.
- Transicion AI first frame / last frame.
- Toma independiente con corte en post.

## Reglas Editoriales

- Si dos tomas ya riman visualmente, probar match cut o cut on action antes de forzar morph.
- Si la transicion AI usa fade/dissolve, rechazar.
- Si el match directo es alto riesgo, crear frame puente.
- Si la toma es fuerte por si sola, no obligarla a transicionar.
- Si Seedance entiende "cut" o "match cut", usarlo como herramienta editorial, no solo como morph.
- Mantener ritmo: no todas las tomas necesitan movimiento complejo.

## Mapa 01-06

| Union | Funcion narrativa | Decision inicial | Motivo | Riesgo | Prompt/editorial note |
|---|---|---|---|---|---|
| 01 -> 02 | Comercio abre / futbol entra al tunel | Match transition o match cut por pies/piso | Rima de luz y avance | Medio | Si falla morph fisico, cortar en el punto de pies/piso. |
| 02 -> 03 | Futbolista avanza / joven asciende | Corte directo o match por avance hacia luz | Ambas son ascenso hacia superficie/escenario | Medio | Cut on forward motion. No necesita morph. |
| 03 -> 04 | Joven sube escaleras / jugador sube tunel | Match cut fuerte | Misma accion de ascenso desde atras | Bajo | Cortar cuando el pie pisa escalon; mantener eje trasero. |
| 04 -> 05 | Jugador emerge / joven en ciudad | Corte editorial | Cambio de mundo; no forzar transformacion | Medio | Usar respiracion/silencio o audio bridge. |
| 05 -> 06 | Joven ciudad / joven estadio | Transformacion controlada o cut with impact | Mismo personaje frontal, cambio de fondo | Alto | Probar background replacement por escala/tilt; si hace fade, usar corte con sonido. |

## Prompt De Secuencia Para IA

Usar cuando se adjunten varias stills:

```text
Actua como editor cinematografico y supervisor de AI video.

Estas son tomas consecutivas de una secuencia. No quiero que todas se conviertan en morph/transicion generativa. Quiero que decidas editorialmente la mejor union entre cada toma.

Para cada par, dime si conviene:
- corte directo
- match cut
- cut on action
- occlusion wipe fisico
- morph material/controlado
- frame puente
- first frame / last frame AI transition
- resolver en post

Prohibido recomendar fade, dissolve, crossfade, black frame o transicion generica.

Para cada par entrega:
1. decision editorial
2. razon
3. punto exacto de corte o match
4. movimiento de camara
5. prompt corto si se renderiza en AI
6. si conviene no renderizar la transicion y cortar en edicion
```

## Tracker 36 Tomas

| Pair | Decision | Riesgo | Render AI? | Frame puente? | Estado | Notas |
|---|---|---|---|---|---|---|
| 01 -> 02 | Match transition / match cut | Medio | Si | No por ahora | En prueba | Rechazar fade/dissolve. |
| 02 -> 03 | Cut on motion | Medio | Opcional | No | Pendiente | Puede ser corte editorial. |
| 03 -> 04 | Match cut | Bajo | Opcional | No | Pendiente | Muy buena rima de ascenso. |
| 04 -> 05 | Corte editorial | Medio | No inicial | No | Pendiente | Cambio de mundo. |
| 05 -> 06 | Transformacion/corte con impacto | Alto | Probar | Posible | Pendiente | Mismo personaje, fondo cambia. |
