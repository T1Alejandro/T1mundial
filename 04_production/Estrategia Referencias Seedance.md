---
title: "Seedance Reference Strategy MB"
doc_type: "motion-brief"
status: "draft"
owner: "Arturo / Parco"
version: "0.1"
last_updated: "2026-05-17"
language: "es"
tags: ["seedance", "motion-tests", "reference-images", "consistency", "v08"]
source_of_truth: "local-project"
related_docs:
  - "../HANDS-UP.md"
  - "v08-shot-production-pack-v001.md"
  - "../03_creative/v02_v08_commerce_athlete/prompts/Motion Don Rafael Apertura.md"
---

# Seedance Reference Strategy MB

## Diagnostico Corto

La prueba de Don Rafael entrando al negocio confirma que Seedance puede funcionar bien para el bloque de apertura si se le da un ancla visual clara.

El riesgo no esta en usar referencias. El riesgo esta en usar una referencia equivocada como fuente principal:

- Un grid/storyboard completo ayuda a entender accion y continuidad, pero cada panel queda pequeno y puede bajar precision de rostro, manos, textura y layout.
- Un still unico de baja resolucion puede dar buen encuadre, pero no alcanza para blindar identidad ni locacion.
- Prompt-only sirve para explorar, pero no es la ruta recomendada para continuidad de personaje en un spot largo.

## Regla Recomendada

Para cada toma importante, usar referencias con roles separados:

1. `image1` = primer frame exacto o still base de la toma.
2. `image2` = character sheet del personaje.
3. `image3` = location sheet o mapa de bloqueo.
4. `image4` = storyboard/sequence sheet solo si el movimiento es complejo.
5. `image5` = ultimo frame aprobado de la toma anterior, solo cuando haya continuidad directa.

No mandar todas las imagenes siempre. Mandar solo las que cumplen una funcion clara.

## Cuando Usar Grid / Storyboard

Usar grid/storyboard como referencia secundaria cuando:

- La accion tiene varios beats.
- Hay que explicar direccion de movimiento.
- La camara debe ir de A a B.
- Hay bloqueo espacial dificil.

No usar grid/storyboard como unica referencia principal cuando:

- La identidad facial es critica.
- Las manos o props son criticos.
- La locacion debe mantenerse exacta.
- La UI o producto T1 deben conservarse limpios.

## Mejor Workflow Para T1

### Fase 1: Clip Por Toma

Producir clips de 4 a 8 segundos por toma. Aunque Seedance pueda generar hasta 15 segundos, para este spot conviene editar una secuencia larga con clips cortos aprobados.

### Fase 2: Continuidad Entre Tomas

Cuando una toma conecta directamente con otra:

- Exportar o capturar el ultimo frame aprobado.
- Usarlo como referencia secundaria en la toma siguiente.
- No intentar que Seedance resuelva todo el spot como una sola generacion.

### Fase 3: Ensamble Editorial

Armar el video largo en Premiere / DaVinci / AE:

- Clips cortos aprobados.
- VO y musica.
- UI T1 en post.
- Logo y slogan reales.
- Color y cleanup legal.

## Test A/B Recomendado Para Don Rafael

Hacer tres renders comparables de 5 a 7 segundos, mismo prompt base:

| Test | Referencias | Que mide |
|---|---|---|
| A | `image1` still final + prompt | Baseline: cuanto conserva desde un frame unico. |
| B | `image1` still + `image2` character sheet + `image3` location/map | Mejor opcion probable para identidad + locacion. |
| C | `image1` still + `image2` character + `image3` location/map + `image4` storyboard | Si el storyboard mejora movimiento o si contamina detalle. |

Ganador no es el mas espectacular. Ganador es el que mantiene:

- Mismo Don Rafael.
- Misma tienda.
- Misma cortina roja.
- Misma entrada/counter/layout.
- Manos naturales.
- Movimiento fisico creible.
- Cero logos/textos inventados.

## Template Prompt Don Rafael

```text
FORMAT:
Single cinematic image-to-video shot. Duration 5-7 seconds. 16:9. 24 fps. No audio.

REFERENCE ROLES:
Use @image1 as the exact first frame and main composition anchor.
Use @image2 only to preserve Don Rafael identity: same age, face, hair, body type, posture, clothing and dignified calm expression.
Use @image3 only to preserve the store layout, facade, red metal shutter, warm dawn light, shelves, central aisle and right-side counter.
Use @image4 only as motion/storyboard guidance if attached. Do not copy the grid layout into the video.

ACTION:
Don Rafael enters his clean historic downtown shop at dawn. He crosses the threshold slowly and naturally, moving with the calm ritual of an older shopkeeper opening his lifelong business. The camera performs a subtle slow push-in from the entrance toward the interior. Keep the action restrained and physical.

CAMERA:
One continuous shot. No cuts. No angle changes. No fast pan. No orbit. No jump. Subtle handheld or dolly push-in only.

CONTINUITY LOCK:
Keep the same Don Rafael from @image2. Keep the same clothing. Keep the same store from @image3. Keep the same red shutter, warm dawn light, shelves, central aisle and right-side counter. Do not redesign the space.

STYLE:
Contemporary Mexican independent cinema. Premium-real, sober, human, clean, dignified. Warm golden dawn, medium contrast, lifted blacks, analog highlight rolloff, fine film grain, real texture of metal, stone, wood and glass.

NEGATIVE:
no different person, no age change, no face morphing, no different clothing, no different store, no layout change, no extra people, no crowd, no dirty shop, no rust, no graffiti, no trash, no luxury boutique, no showroom, no text, no captions, no subtitles, no logos, no watermark, no invented UI, no sports, no soccer, no football, no stadium, no ball, no flags, no cuts, no fade, no dissolve, no hyperactive motion, no distorted hands, no malformed face.
```

## Decision Operativa

La mejor ruta para consistencia no es "mas imagenes siempre"; es "menos imagenes, mejor etiquetadas".

Para T1, la combinacion mas fuerte probablemente es:

`still base de toma + character sheet + location/map + prompt corto con roles`

El storyboard/grid se usa solo como ayuda de movimiento, no como fuente visual principal.

## Prompt Para Consultar A Claude / ChatGPT / Otros Modelos

Usar este bloque para pedir una segunda opinion tecnica sin tener que reexplicar el proyecto.

```text
Estamos produciendo un hero film cinematografico de 60-90s para T1. No queremos una sola generacion larga; queremos clips consistentes por toma, ensamblados en edicion.

El caso actual es Don Rafael, hombre mexicano de 55-60, comerciante de Centro Historico, entrando a su tienda al amanecer. Ya tenemos:

1. Character sheet HD de Don Rafael.
2. Location sheet HD de la tienda.
3. Blocking/location map HD de la tienda.
4. Un storyboard/grid o sequence sheet que explica la accion.
5. Algunos stills/frame base de baja o media resolucion.

Queremos usar Higgsfield / Seedance para generar clips de 4-8 segundos con la mejor consistencia posible de personaje, locacion, layout, manos, cortina, luz y direccion de arte.

Pregunta principal:
Cual es el mejor workflow practico para generar cada toma con maxima consistencia?

Opciones que estamos evaluando:

A. Prompt-only, sin imagenes.
B. Solo un still/frame base 16:9 como first frame.
C. First frame 16:9 + character sheet + location sheet/map.
D. First frame 16:9 + character sheet + location sheet/map + storyboard/grid.
E. Usar solo last frame de la toma anterior para continuar la siguiente.
F. Usar last frame de la toma anterior + character sheet + location sheet/map.

Necesitamos una recomendacion concreta:

1. Que imagenes adjuntar para la primera toma?
2. Que imagenes adjuntar para tomas siguientes?
3. Cuando usar character sheet?
4. Cuando usar location sheet o blocking map?
5. Cuando usar storyboard/grid?
6. Cuando usar first frame y last frame?
7. Conviene regenerar stills HD 16:9 por toma antes de animar?
8. Conviene producir clips de 4-8s o intentar clips de 15s?
9. Como escribir el prompt para que cada imagen tenga un rol especifico?
10. Cuales son los errores mas probables que rompen continuidad?

Restricciones:

- No inventar logos, texto, UI, dashboards, QR ni marcas.
- No cambiar edad, rostro, ropa ni cuerpo de Don Rafael.
- No redisenar la tienda.
- No ensuciar ni deteriorar el negocio.
- No agregar gente extra.
- No usar futbol, estadio, balon, uniforme, bandera ni Mundial.
- Mantener cine mexicano contemporaneo, premium-real, sobrio, humano, limpio y digno.

Devuelve:

1. Workflow recomendado paso a paso.
2. Stack de referencias ideal para una toma nueva.
3. Stack de referencias ideal para una toma que continua la anterior.
4. Prompt template breve para Seedance/Higgsfield.
5. Criterio de aprobacion/rechazo.
```
