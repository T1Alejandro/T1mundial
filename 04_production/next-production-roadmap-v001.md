---
title: "Next Production Roadmap"
doc_type: "roadmap"
status: "draft"
owner: "Arturo / Parco"
reviewers: []
version: "0.1"
last_updated: "2026-05-06"
language: "es"
audience: ["internal", "creative", "production"]
tags: ["ai-video", "stills", "consistency", "motion-tests", "tooling"]
source_of_truth: "local-project"
confidence: "medium"
related_docs:
  - "production-pipeline.md"
  - "stills-to-animation-pipeline.md"
  - "figma-weave-motion-sprint-01.md"
  - "global-motion-rules-v001.md"
  - "camera-animation-bible-36-v001.md"
  - "edit-decision-map-v001.md"
  - "bridge-frame-policy-v001.md"
  - "preflight-01-06-v001.md"
  - "transition-preflight-chat-prompt-v001.md"
  - "wave-figma-first-6-prompt-pack-v001.md"
  - "weave-first-6-manual-patch-v001.md"
  - "weave-first-6-flow-blueprint-v001.json"
  - "../03_creative/prompts/chatgpt-master-rack-36-v004.md"
  - "../02_references/visual/Stills T1mundial"
---

# Next Production Roadmap

## MSBP

- Estado: el patch no quedo armado en Krea, Higgsfield ni ComfyUI, pero el prompt maestro usado toma por toma en ChatGPT funciono y produjo la base visual consistente.
- Asset base: carpeta `02_references/visual/Stills T1mundial` con stills numerados `01.png` a `36.png`; las 36 tomas ya son oficiales.
- Hallazgo tecnico: casi todos los stills estan en `1672x941`; `29.png` esta en `1376x768`. Todos funcionan como 16:9 aproximado para pruebas image-to-video.
- Cambio de fase: ya no estamos en look-dev inicial; estamos entrando a produccion de motion tests, continuidad, versiones de guion y herramienta final por toma.
- Duracion: abierta/arbitraria por ahora; el ritmo lo van a definir VO, montaje y calidad de los motion tests.
- VO: no existe todavia; conviene prototiparla rapido en ElevenLabs en paralelo.
- Pantallas T1: se resolveran por fotomontaje/post con stills reales de las plataformas, no como UI generada por AI.

## Hipotesis De Produccion

La consistencia no debe depender de un solo patch magico. Debe depender de un sistema:

1. Prompt maestro como ADN visual.
2. Still aprobado por toma como ancla.
3. Referencias por bloque narrativo para continuidad.
4. Motion prompt corto por toma, no reescritura completa.
5. QA legal/visual antes de pasar al corte.
6. Versionado estricto para que cada variacion de guion pueda regenerarse sin perder el look.

## Objetivo Inmediato

Convertir los 36 stills en un paquete de produccion animable:

- Contact sheet final.
- Matriz de continuidad por personaje, locacion, color, vestuario y objeto.
- Prompt corto de movimiento por toma.
- 3 a 5 motion tests prioritarios.
- Decision de herramienta por tipo de toma.
- Primer rough cut con scratch VO, aunque algunas tomas sigan como stills.
- Primer satelite de video para mostrar consistencia y potencial sin esperar al master final.

## Orden Recomendado

### 1. Auditoria De Stills

Revisar cada still y marcar:

- Aprobado visual.
- Riesgo legal.
- Riesgo AI.
- Riesgo de movimiento.
- Necesita limpieza.
- Necesita remake.
- Puede entrar directo a motion test.

Salida esperada:

- `04_production/still-audit-t1mundial-v001.md`
- Validacion rapida de las primeras 6 tomas para entrar a Wave/Figma.

### 2. Motion Test Sprint 01: Figma Weave / Wave

Primera herramienta a probar: Figma Weave / Wave, por su promesa de canvas nodal, ramas de versiones y control visual por referencias.

No probar las 36 tomas todavia. Probar primero la microsecuencia de apertura:

| Shot | Por que probarlo |
|---|---|
| 01 | Apertura, textura metal, tono inicial. |
| 02 | Rima visual con futbol, tunel, uniformes ficticios sin marcas. |
| 03 | Continuidad del joven, mochila roja, ascenso urbano. |
| 04 | Rima deportiva del ascenso, concreto, tachones y estadio. |
| 05 | Identidad facial del joven, calle abierta, determinacion. |
| 06 | Transformacion a estadio, escala y continuidad del mismo joven. |

Salida esperada:

- 1 version inicial por toma, sin variaciones todavia.
- Clips de 3 a 5 segundos.
- Revision de continuidad 01-06 en secuencia.
- Notas de alcance real: consistencia, creditos/costo, facilidad de repetir versiones, calidad de export y nivel de control.

### 3. VO Scratch Sprint 01

Crear una voz temporal rapido para dirigir ritmo y emocion:

- 3 opciones de casting en ElevenLabs.
- 1 guion scratch corto.
- 1 version mas cinematografica / contenida.
- 1 version mas directa para video satelite.
- Export WAV o MP3 para rough cut.

La voz no tiene que ser final. Su trabajo es ordenar duracion, silencios y energia.

### 4. Herramientas Por Rol

| Rol | Mejor uso | Riesgo |
|---|---|---|
| ChatGPT / imagen | Crear stills consistentes y variaciones del lenguaje visual. | No resuelve movimiento final. |
| Krea / Weavy / Figma Weave | Canvas nodal, iteracion, mezcla de modelos, control visual por referencias. | Puede ser excelente para organizar, pero hay que validar export, costo y control real de video. |
| Higgsfield | Tests rapidos de imagen a video, lifestyle/cine si respeta referencia. | Puede deformar identidad o inventar marcas si el prompt se abre. |
| ComfyUI | Control avanzado, reproducibilidad, nodos, IP/control/reference workflows. | Alto costo de setup; conviene solo si necesitamos control fino o pipeline local repetible. |
| Runway / Kling / Seedance / Veo / Sora | Generacion de movimiento segun tipo de toma. | La consistencia cambia por modelo; hay que evaluarlos con el mismo still. |
| After Effects / DaVinci / Premiere | Ensamble, comp de pantallas, color, logo, legal cleanup. | Requiere separar que es AI y que es post. |

## Direccion De Movimiento

El movimiento buscado es cinematografico y dinamico, no solo "foto que respira":

- Paneos suaves con intencion narrativa.
- Push-in y pull-back controlados.
- Rack focus y profundidad de campo.
- Handheld contenido cuando aporte tension humana.
- Orbitas o parallax solo en tomas donde la geometria lo soporte.
- Movimiento de personajes limitado si la AI rompe identidad o manos.
- Desenfoque de movimiento natural, no blur falso excesivo.

Regla: si el movimiento destruye continuidad, se prefiere comp/post con still animado antes que un clip espectacular pero incoherente.

## Regla De Decision De Herramienta

No elegir herramienta por hype. Elegir por resultado en estos criterios:

1. Respeta el still inicial.
2. Mantiene rostro, ropa, locacion y encuadre.
3. No inventa texto, logos ni marcas.
4. Mueve solo lo necesario.
5. No rompe manos, fisica ni pantallas.
6. Exporta a specs utiles para edicion.
7. Permite repetir variaciones sin empezar desde cero.

## Sistema De Versiones

Usar esta estructura para la siguiente fase:

```text
04_production/ai-generations/motion-tests/shot-##/
04_production/ai-generations/motion-tests/shot-##/refs/
04_production/ai-generations/motion-tests/shot-##/exports/
04_production/ai-generations/motion-tests/shot-##/notes.md
```

Naming:

```text
t1mundial_shot-##_motion-test_tool-v###_yyyymmdd.mp4
t1mundial_shot-##_motion-prompt_tool-v###_yyyymmdd.md
```

## Respuestas Confirmadas

- Las 36 stills son oficiales.
- Duracion abierta por ahora.
- No hay VO todavia.
- Primera prueba de video: Figma Weave / Wave con las primeras 6 tomas oficiales.
- Movimiento: cinematografico dinamico, con angulos, paneos, zooms/push-ins, rack focus y profundidad de campo.
- Pantallas T1: fotomontaje/post con stills reales de plataformas provistos por Arturo.

## Preguntas Abiertas

1. El satelite de primeras 6 debe llevar VO desde el primer rough o solo musica/ambiente?
2. Tono de VO preferido: mujer grave calida, hombre documental, voz joven sobria, o sin genero marcado?
3. La voz habla como marca T1, como narrador documental, o como comerciante/founder?
4. Hay presupuesto/creditos maximos para el primer sprint en Figma Weave?
5. En Seedance, que tomas salieron mas brutales y con que ajustes?
6. Hay que armar tambien version vertical 9:16 para satelites/redes?

## Proximo Paso Concreto

Ejecutar `wave-figma-first-6-prompt-pack-v001.md` en Figma Weave / Wave: generar `v001` de las tomas 01-06, revisar continuidad en secuencia y solo despues iterar `v002` en las tomas que fallen.
