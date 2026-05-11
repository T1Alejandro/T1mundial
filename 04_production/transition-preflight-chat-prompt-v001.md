---
title: "Transition Preflight Chat Prompt"
doc_type: "prompt-pack"
status: "draft"
owner: "Arturo / Parco"
reviewers: []
version: "0.1"
last_updated: "2026-05-06"
language: "es"
audience: ["internal", "creative", "production"]
tags: ["preflight", "transition", "chatgpt", "claude", "mvp"]
source_of_truth: "transition-preflight-risk-framework-v001.md"
confidence: "medium"
related_docs:
  - "global-motion-rules-v001.md"
  - "transition-preflight-risk-framework-v001.md"
  - "bridge-frame-policy-v001.md"
---

# Transition Preflight Chat Prompt

## Uso MVP

Abrir un chat nuevo en ChatGPT, Claude o una IA visual. Adjuntar las stills en orden y pegar este prompt.

Para primeras 6 tomas:

```text
Adjunto 6 stills en orden: 01, 02, 03, 04, 05, 06.
```

## Prompt

```text
Actua como supervisor de transiciones AI-video, director de fotografia y editor.

Voy a adjuntar N stills en orden narrativo. Tu tarea es evaluar ANTES de renderizar si cada transicion entre pares consecutivos puede funcionar sin fade, dissolve, crossfade, corte, pantalla negra o truco generico.

REGLA GLOBAL:
No se permiten fades de ningun tipo: no fade, no semi fade, no dissolve, no semi dissolve, no crossfade, no opacity blend, no background dissolve, no black frame, no white flash, no slideshow transition, no generic transition.

Las transiciones deben resolverse con:
- movimiento fisico de camara
- match por pies, manos, objetos, paredes, piso, lineas, sombras, luz, textura o silueta
- occlusion natural
- morph controlado de materiales/geometria
- match cut espacial
- frame puente si hace falta

Evalua cada par consecutivo:
01 -> 02
02 -> 03
03 -> 04
etc.

Para cada par entrega una tabla con:
1. Pair
2. Score de riesgo 0-50
3. Riesgo: bajo / medio / alto / muy alto
4. Punto fisico de match recomendado
5. Movimiento de camara recomendado
6. Que debe transformarse o hacer morph controlado
7. Que NO debe hacer el modelo
8. Si necesita frame puente: si/no
9. Prompt corto recomendado para video AI
10. Si recomiendas frame puente, prompt de imagen para crear ese frame puente

Score:
- 0-10 bajo
- 11-20 medio
- 21-30 alto
- 31-50 muy alto

Despues dame:
- ranking de las transiciones mas viables
- ranking de las mas peligrosas
- cual deberia renderizar primero para MVP
- reglas nuevas que deban entrar al Global Motion Rules

MOVIMIENTO DE CAMARA:
Siempre propone un movimiento principal de camara, concreto y ejecutable. No digas solo "camara cinematografica".

Elige uno cuando aplique:
- travelling vertical hacia abajo
- travelling vertical hacia arriba
- dolly in
- dolly out
- dolly bajo hacia adelante
- tilt down
- tilt up
- pan lateral
- whip pan
- handheld contenido
- rack focus
- occlusion wipe fisico
- push-in frontal
- pull-back frontal
- match cut sin transicion generativa

Para cada movimiento explica:
- punto de inicio
- direccion
- punto de llegada
- que elemento hace el match
- si requiere que el modelo mantenga first frame/last frame exactos

Ejemplo de buen output:
`Movimiento: travelling vertical hacia abajo. Inicio en manos/silueta levantando la cortina. Baja por torso y piernas hasta pies/piso. El match ocurre en pies + lineas del piso + luz dorada, que se transforman en pies del jugador + piso del tunel.`

Importante:
No propongas fades. No propongas dissolves. No propongas crossfades. Si el match es dificil, recomienda frame puente, occlusion o camera move mas simple.

REGLA DE FRAME PUENTE:
No recomiendes crear una imagen puente por ajustes menores. Solo recomienda frame puente si:
- el score de riesgo es 24 o mas, o
- el cambio de composicion/camara/fondo es demasiado grande para una transicion fisica limpia, o
- la unica alternativa probable seria fade/dissolve/crossfade, o
- falta un punto fisico de match claro.

Si el match es bajo o medio y tiene un punto fisico claro, NO recomiendes imagen puente. Da solo prompt de video.

Si recomiendas frame puente, no generes la imagen automaticamente a menos que te lo pida explicitamente. Primero entrega:
- razon concreta
- descripcion visual del frame puente
- prompt de imagen
- como se usaria: A -> bridge -> B
```

## Output Esperado

```text
PAIR: 01 -> 02
Riesgo: medio / 18
Match: pies + piso + lineas verticales + luz dorada
Camara: tilt/travelling descendente + dolly bajo
Morph permitido: metal/piso/luz a concreto/tunel/contraluz
Prohibido: fade, dissolve, semi-transparent background blend
Frame puente: no, pero puede ayudar
Prompt corto: ...
Prompt frame puente: no aplica
```

## Decision MVP

- Renderizar primero pares de riesgo bajo/medio.
- Si un par es alto, crear frame puente antes de gastar video.
- Si un par es muy alto, resolver en edicion/post o cambiar orden narrativo.
