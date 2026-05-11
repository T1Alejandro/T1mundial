---
title: "Transition Preflight Risk Framework"
doc_type: "qa-framework"
status: "draft"
owner: "Arturo / Parco"
reviewers: []
version: "0.1"
last_updated: "2026-05-06"
language: "es"
audience: ["internal", "creative", "production"]
tags: ["transition", "preflight", "risk", "ai-video", "qa"]
source_of_truth: "local-project"
confidence: "medium"
related_docs:
  - "figma-weave-motion-sprint-01.md"
  - "wave-figma-first-6-prompt-pack-v001.md"
---

# Transition Preflight Risk Framework

## Objetivo

Antes de gastar creditos en video, evaluar si dos stills tienen alta probabilidad de transicionar bien y que tipo de instruccion necesita el modelo.

## Score De Riesgo

Calificar cada categoria de 0 a 5:

- `0`: sin riesgo.
- `1`: bajo.
- `2`: manejable.
- `3`: medio, requiere prompt preciso.
- `4`: alto, requiere puente visual o frame intermedio.
- `5`: muy alto, no conviene pedir transicion directa.

## Categorias

| Categoria | Pregunta | Riesgo alto si... |
|---|---|---|
| Composicion | Los encuadres comparten eje, escala o direccion? | Cambia mucho el eje de camara. |
| Geometria | Hay lineas, paredes, suelo o formas que puedan hacer match? | No hay formas comunes. |
| Sujeto | Hay parte del cuerpo/objeto que pueda conectar? | Cambia sujeto, escala o posicion. |
| Camara | El movimiento fisico entre ambas es posible? | Requiere teletransportacion visual. |
| Plan de camara | Hay un movimiento principal concreto para resolver el match? | Solo hay idea conceptual, no trayectoria ejecutable. |
| Luz | La direccion/intensidad de luz rima? | Cambia de luz sin puente natural. |
| Color | La paleta conecta? | Cambia tono/color radicalmente. |
| Textura | Hay material que pueda transformarse? | No hay material puente. |
| Accion | Hay una accion que justifique el cambio? | Solo se parece conceptualmente. |
| Riesgo legal | Puede inventar marcas/texto durante la transicion? | Hay ropa, estadio, senaletica o pantallas. |
| Fallback IA | El modelo podria resolver con fade/cut/dissolve? | No hay instruccion de continuidad fisica. |

## Interpretacion

| Total | Riesgo | Decision |
|---:|---|---|
| 0-10 | Bajo | Transicion directa viable. |
| 11-20 | Medio | Transicion viable con prompt especifico. |
| 21-30 | Alto | Crear frame puente o limitar a match cut corto. |
| 31-50 | Muy alto | No hacer transicion directa; usar edicion/post. |

## Politica De Transicion

Cuando el riesgo sea medio o alto:

- Prohibir fade, dissolve, crossfade, hard cut, black frame y flash.
- Indicar punto fisico de match: pies, manos, puerta, pared, suelo, linea de luz, objeto.
- Priorizar transformacion de objetos/espacios, no disolucion de fondo.
- Pedir continuidad de camara: tilt, dolly, pan, push-in, pull-back, rack focus.
- Definir plan de camara ejecutable: punto de inicio, direccion, punto de llegada y elemento que hace match.
- Pedir "one continuous impossible physical shot".
- Si hay cuerpos, limitar morphing corporal y mover camara/entorno.
- Si hay fondos muy distintos, usar textura puente: pared, piso, luz, sombra, polvo, metal, concreto.

## Prompt De Evaluacion Para IA Visual

Usar con dos imagenes adjuntas:

```text
Evalua estas dos imagenes como first frame y last frame para una transicion de video AI.

Necesito saber si el modelo probablemente podra hacer una transicion cinematografica continua sin usar fade, dissolve, hard cut, black frame ni morphing caotico.

Califica de 0 a 5 cada categoria:
1. composicion
2. geometria
3. sujeto
4. camara
5. plan de camara ejecutable
6. luz
7. color
8. textura
9. accion
10. riesgo legal/texto/logos
11. riesgo de fallback generico de IA

Despues dame:
- score total
- riesgo: bajo / medio / alto / muy alto
- punto fisico de match recomendado
- movimiento de camara recomendado
- que NO pedir
- prompt corto recomendado para la transicion
- si hace falta frame puente
```

## Registro De Transiciones

| Pair | Score | Riesgo | Punto de match | Movimiento recomendado | Necesita frame puente | Resultado real |
|---|---:|---|---|---|---|---|
| 01 -> 02 | TBD | Medio | pies / piso / lineas de luz | tilt/travelling descendente + dolly bajo | No por ahora | V001 fade; V002 medio dissolve de fondo |
