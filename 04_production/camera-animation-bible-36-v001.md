---
title: "Biblia De Animacion Y Camara 36"
doc_type: "motion-bible"
status: "draft"
owner: "Arturo / Parco"
reviewers: []
version: "0.1"
last_updated: "2026-05-07"
language: "es"
audience: ["internal", "creative", "production"]
tags: ["camera", "animation", "motion", "transitions", "ai-video", "36-shots"]
source_of_truth: "../03_creative/prompts/chatgpt-master-rack-36-v004.md"
confidence: "medium"
related_docs:
  - "global-motion-rules-v001.md"
  - "edit-decision-map-v001.md"
  - "transition-preflight-chat-prompt-v001.md"
  - "wave-figma-first-6-prompt-pack-v001.md"
---

# Biblia De Animacion Y Camara 36

## Uso

Este documento es la biblia de animacion/camara entre stills.

Regla simple:

- Para animar una toma individual, usar `MOVIMIENTO DE TOMA`.
- Para conectar dos tomas, usar `TRANSICION A SIGUIENTE`.
- Para preflight, usar estas mismas intenciones como criterio.

## Reglas Globales De Movimiento

```text
Animar solamente desde la referencia still proporcionada. Preservar composicion, altura de camara, sensacion de distancia focal, lineas de perspectiva, blocking, direccion de luz, balance de color, proporciones del sujeto, geometria del entorno, vestuario e identidad.

No fade, no semi fade, no dissolve, no semi dissolve, no crossfade, no opacity blend, no black frame, no white flash, no transicion generica.

El movimiento debe estar motivado fisicamente: dolly, tilt, pan, rack focus, occlusion, match cut, cut on action, transformacion material, continuidad de luz, lineas de piso, lineas de pared, sombras, textura o silueta.

Realismo temporal: timing natural, inercia con peso, no movimiento hiperactivo, no speed ramps, no extremidades flotantes, no morph AI gelatinoso.

Audio apagado por default.
```

## Toma 01

Still:

```text
02_references/visual/Stills T1mundial/01.png
```

### Movimiento De Toma

```text
Camara baja frontal. Push-in fisico muy lento, casi imperceptible. La cortina metalica sube sutilmente. La luz calida del amanecer respira por la abertura inferior. Particulas de polvo se mueven suavemente en la luz. Mantener composicion simetrica, silenciosa y suspendida.
```

### Transicion A Siguiente: 01 -> 02

Decision:

```text
Transicion AI por match fisico o match cut.
```

Plan de camara:

```text
Travelling / tilt vertical hacia abajo. Empezar en la silueta centrada levantando la cortina metalica. Bajar por torso y piernas hacia los pies y el piso. Matchear lineas del piso, luz dorada y pies con los pies del futbolista y el piso del tunel. Continuar como dolly bajo hacia adelante dentro del tunel oscuro de estadio.
```

Transformacion permitida:

```text
cortina metalica / piso de tienda / luz dorada -> tunel de concreto / piernas de futbolista / contraluz
```

Negativos duros:

```text
no fade, no semi fade, no dissolve, no opacity blend, no background dissolve
```

## Toma 02

Still:

```text
02_references/visual/Stills T1mundial/02.png
```

### Movimiento De Toma

```text
Dolly bajo hacia adelante a ras de suelo dentro de un tunel de estadio oscuro y cerrado. Mantener el estadio apenas visible como contraluz abstracto. Las piernas del jugador se mueven lento y natural. Tela y haze del tunel se mueven sutilmente. No revelar todavia la escala completa del estadio.
```

### Transicion A Siguiente: 02 -> 03

Decision:

```text
Preferir corte editorial o corte sobre movimiento hacia adelante. No forzar morph salvo que el preflight lo apruebe.
```

Plan de camara:

```text
Cortar del avance del futbolista hacia la luz del tunel al joven subiendo escaleras hacia la luz de la superficie. Matchear direccion de avance, silueta centrada y geometria de muros. Si se intenta transicion AI, usar lineas de pared del tunel y contraluz como occlusion fisica hacia muros de escalera y luz de ocaso.
```

Transformacion permitida:

```text
paredes de tunel / contraluz / avance hacia adelante -> paredes de escalera / luz de ocaso / ascenso
```

Negativos duros:

```text
no fade, no dissolve, no crossfade, no black frame
```

## Toma 03

Still:

```text
02_references/visual/Stills T1mundial/03.png
```

### Movimiento De Toma

```text
Tracking trasero centrado. Dolly lento hacia arriba siguiendo al joven que sube las escaleras. La mochila roja se balancea sutilmente. Una corriente calida leve mueve la hoodie y las correas de la mochila cerca de los escalones superiores. Preservar color de ocaso y simetria de escaleras.
```

### Transicion A Siguiente: 03 -> 04

Decision:

```text
Match cut fuerte. Transicion AI opcional.
```

Plan de camara:

```text
Cortar sobre pisada. Matchear el ascenso trasero del joven en escaleras con el ascenso trasero del futbolista por escaleras de concreto en el tunel. Preservar eje trasero centrado, geometria de escalones y movimiento ascendente.
```

Transformacion permitida:

```text
lineas de escaleras urbanas / ropa negra / movimiento de mochila roja -> escaleras de concreto / piernas de futbolista / calcetas rojas
```

Negativos duros:

```text
no fade, no dissolve, no morph corporal gelatinoso
```

## Toma 04

Still:

```text
02_references/visual/Stills T1mundial/04.png
```

### Movimiento De Toma

```text
Dolly bajo trasero hacia arriba. Foco en piernas, tachones sin marca y escaleras de concreto. La luz del estadio florece suavemente al frente. El espacio se abre gradualmente, a diferencia de la toma 02 mas oscura y cerrada.
```

### Transicion A Siguiente: 04 -> 05

Decision:

```text
Preferir corte editorial. No forzar morph AI al inicio.
```

Plan de camara:

```text
Cortar del jugador emergiendo hacia la luz del campo al joven ya emergido en espacio urbano abierto. Usar match conceptual: backstage a escenario y abajo a aire libre. Un puente de audio, respiracion o silencio puede sostener el corte.
```

Transformacion permitida:

```text
no recomendada como morph directo en MVP
```

Negativos duros:

```text
no fade, no dissolve, no transicion generica
```

## Toma 05

Still:

```text
02_references/visual/Stills T1mundial/05.png
```

### Movimiento De Toma

```text
Push-in frontal muy lento desde altura de pecho o ligeramente abajo. El joven permanece quieto, respirando natural. Preservar identidad facial exacta, ropa negra, mochila roja y fondo urbano abierto.
```

### Transicion A Siguiente: 05 -> 06

Decision:

```text
Transformacion de alto riesgo o corte con impacto. Considerar frame puente si el preflight lo recomienda.
```

Plan de camara:

```text
El push-in frontal continua mientras el joven mira hacia arriba. La geometria del fondo detras de la cabeza se expande desde fachadas anonimas de ciudad hacia gradas de estadio ficticio. Usar escala vertical, direccion de mirada y luz suave sobre el rostro como punto de match. Si el modelo intenta hacer fade, detener y usar frame puente o corte editorial.
```

Transformacion permitida:

```text
fachadas urbanas / banqueta abierta / mirada hacia arriba -> gradas de estadio / atmosfera humana de multitud / misma luz en rostro
```

Negativos duros:

```text
no fade, no semi fade, no dissolve, no background dissolve, no tono de publicidad heroica
```

## Toma 06

Still:

```text
02_references/visual/Stills T1mundial/06.png
```

### Movimiento De Toma

```text
Push-in frontal lento con tilt sutil hacia arriba. El joven respira y mira hacia arriba con asombro y determinacion. Luces de estadio y atmosfera de multitud se mueven sutilmente detras. La emocion se mantiene intima y humana, no como espectaculo triunfalista.
```

### Transicion A Siguiente: 06 -> 07

Decision:

```text
Usar wipe organico de la toma 07.
```

Plan de camara:

```text
Sostener la mirada ascendente del joven y permitir que una silueta oscura en movimiento cruce el cuadro y ocluya casi toda la imagen, preparando el wipe organico de la toma 07.
```

Transformacion permitida:

```text
fondo de estadio / mirada del joven -> wipe de silueta oscura / ruptura entre realidades
```

Negativos duros:

```text
no fade, no dissolve, no black frame
```

## Tomas 07-36

Estado:

```text
Pendiente pase de biblia de movimiento.
```

Siguiente paso:

```text
Extender esta misma estructura toma por toma:
- Still
- Movimiento De Toma
- Transicion A Siguiente
- Decision
- Plan de camara
- Transformacion permitida
- Negativos duros
```
