---
title: "L01 Tienda Don Rafael Blocking Map v010 Prompt"
doc_type: "image-generation-prompt"
status: "ready"
owner: "Arturo / Parco"
version: "0.1"
last_updated: "2026-05-17"
language: "es"
tags: ["v08", "don-rafael", "l01", "blocking-map", "centro-historico", "seedance-reference"]
source_of_truth: "local-project"
related_assets:
  - "../../../07_assets/locations/model-sheets v03/L01-tienda-pequena-centro-historico-location-sheet-v009-approved.png"
  - "../../../07_assets/locations/blocking-maps/L_Tienda-pequena-centro-historico-blocking-map.png"
---

# L01 Tienda Don Rafael — Blocking Map v010

## Objetivo

Generar un nuevo map sheet de la tienda de Don Rafael que sea mas util para Seedance/Higgsfield:

- Planta clara de la tienda en formato 16:9.
- Sensacion de tienda pequena del Centro Historico CDMX.
- Mostrador en forma de L literal bien definido, como la letra "L" vista desde arriba; solo el palo corto/base de la L toca la pared derecha visual del plano.
- Orientacion cardinal con rosa de los vientos.
- Secuencia operativa coherente segun el recorrido de Don Rafael: desde entrada SUR hacia fondo NORTE.
- Estetica de corte de planta tecnico, similar al mapa aprobado anterior: linework limpio, casi monocromo, no render colorido.
- Version interna de produccion, no un frame cinematografico final.

## Nota De Vocabulario

La "brujula" en una lamina/mapa se puede pedir como:

- **rosa de los vientos**
- **compass rose**
- **north arrow**
- **orientation compass**

Para este caso pedir: **small compass rose / north arrow in the upper right corner, labeled in Spanish: N, S, O, E**.

## Prompt Principal Para ChatGPT Images

```text
Create a clean 16:9 HD production blocking map sheet for a small traditional shop in the Historic Center of Mexico City, owned by Don Rafael.

This is not a cinematic still. It is an overhead orthographic production map / floor plan used for film blocking and AI video continuity.

STYLE:
Precise architectural top-down floor plan / production blocking map, clean technical linework, white background, thin black/gray ink lines, very light warm gray material hints only, minimal shading, almost monochrome, sparse red accent only for the shutter and folded red cloth. It should feel like a clean plan-cut drawing from the approved bible/map, not a colorful game render, not an isometric render, not a fully colored illustration, not photorealistic.

LOCATION IDENTITY:
Small dignified Mexican shop in Centro Historico CDMX. Traditional but recently cared for. Clean tezontle / reddish cantera facade at the street entrance, red metal rolling shutter at the south side, warm dawn light direction entering from the street. Interior is modest, clean, human, premium-real, not touristy, not luxury boutique, not old/dirty.

ORIENTATION / SCREEN DIRECTION:
Add a small clean compass rose / north arrow in the upper right corner outside the floor plan, labeled in Spanish with cardinal letters: N, S, O, E. Use O for Oeste, not W.
North is the back wall of the shop.
South is the street entrance and red metal shutter.
Important production convention for this sheet: the visual RIGHT wall / screen-right wall is the wall where the SHORT horizontal base of the L counter touches the wall.
Only the short base of the L touches the visual right wall. The long vertical leg of the L does NOT touch the wall; it sits inward/left of that wall.
The opposite visual left wall has tall shelves.
The open aisle remains in the center / interior side of the shop.

FLOOR PLAN:
Show a narrow rectangular shop, longer north-south than east-west.
South side: street entrance with red metal rolling shutter, centered doorway, threshold from Centro Historico sidewalk.
Visual left wall: continuous tall shelving from south to north, clean glass/wood shelves with small generic hair/barber/care products, no readable labels.
North wall: back shelving / storage display, clean and organized.
Counter geometry: create a literal uppercase "L" shaped wooden service counter in plan view, same orientation as the typed letter "L".
Only the SHORT horizontal base of the L is attached to / touches the visual RIGHT wall of the floor plan.
The long vertical leg of the L runs north-south on the INNER/LEFT end of that short base, away from the wall.
The short horizontal base of the L runs from the long vertical leg toward the visual RIGHT wall, along the SOUTH/FRONT side of the counter area.
Do not attach the long vertical leg to the wall.
Do not mirror, rotate or flip the L into a J shape.
It must read exactly like this shape from above, with the short base touching the right wall at its far right end:
|
|
|____|
     right wall touch point
Leave a clear aisle from the south entrance into the shop and toward the inside of the L counter.

DEVICE / PROP LAYOUT ON THE LONG VERTICAL LEG OF THE L COUNTER:
Place the hero objects on the long vertical north-south leg of the literal L-shaped counter. The objects must sit on the long vertical leg, not on the bottom horizontal base, except for small secondary papers if needed.

Important: separate object POSITION from object ORIENTATION.

POSITION ON THE LONG COUNTER LEG:
Do not use normal page-reading order for the props. Use the physical route of Don Rafael through the shop.
Because Don Rafael enters from the SOUTH/front and moves toward the NORTH/back, arrange the hero objects along the long vertical leg from SOUTH to NORTH / front to back:
1. South/front position, closest to the short horizontal base/return: folded red cloth / pano rojo next to the small notebook / libreta and pen with red clip.
2. Middle position: generic smart POS terminal with integrated receipt printer, white body, black blank screen, small red accent, no logo, no UI, no readable numbers, no receipt text.
3. North/back position: small clean laptop / computer, screen blank or matte dark, no UI, no text, no icons.

OBJECT ORIENTATION ON THE COUNTER SURFACE:
The pen is horizontal on the counter: click button / cap end toward the visual RIGHT / WEST side, writing tip pointing toward the visual LEFT / EAST side, toward the laptop and POS terminal.

The laptop/computer is open on the counter but it must face the wall, not the entrance or customer aisle.
Use this strict left-to-right / west-to-east cross-section across the counter:
SCREEN/DISPLAY -> KEYBOARD -> EMPTY COUNTER / SELLER-SIDE GAP -> RIGHT WALL.
The display panel is on the visual LEFT / WEST side of the laptop, the keyboard is immediately to its visual RIGHT / EAST side, and the empty seller-side gap continues toward the right wall. The laptop display faces EAST / toward the right wall. It must not face the central aisle, customer side or entrance. Screen must be blank or matte dark, no UI, no text, no icons.

The POS terminal is horizontal on the counter: screen/front/keypad face oriented toward the visual RIGHT / WEST side, thicker base / receipt-printer end toward the visual LEFT / EAST side. If keypad buttons are visible, they must be blank button shapes with no readable numbers; orient the keypad as if a person standing on the visual right / west side of the terminal could use it. Do not generate actual numbers, labels or payment symbols.

Make the devices proportional and believable, not oversized. The POS terminal should be compact handheld scale, not a tablet on a stand.

BLOCKING:
Add subtle floor arrows or simple path marks showing Don Rafael's movement:
Start outside/south at the shutter -> step through threshold -> continue north along central aisle -> turn east toward the L-shaped counter -> stop at counter.
Keep arrows minimal and production-map style.

OUTPUT:
One single 16:9 image. The map should be centered with generous margin. The floor plan should be clean enough to use as a reference image for Seedance/Higgsfield.

NEGATIVE:
no cinematic camera view, no perspective room render, no isometric video game map, no colorful render, no saturated wood, no fully colored bottles, no realistic product rows, no character portrait, no people, no crowd, no logos, no brands, no readable product labels, no payment brand, no Visa, no Mastercard, no QR code, no UI, no dashboard, no app icons, no text blocks inside the shop, no messy labels, no dirty shop, no rust, no trash, no graffiti, no broken walls, no tourist souvenirs, no flags, no soccer, no football, no stadium, no ball, no famous landmark, no luxury boutique, no tech startup, no cluttered market.
```

## Variante Limpia Para Seedance

Usar esta si el mapa se va a subir directamente como referencia de locacion en Seedance. Tiene menos texto para evitar que el modelo intente copiar labels.

```text
Create a clean 16:9 HD overhead orthographic production blocking map for Don Rafael's small shop in the Historic Center of Mexico City.

Precise top-down floor plan / production blocking map, white background, thin black and gray linework, almost monochrome, minimal shading, very light warm gray material hints only. Sparse red accent only for the shutter and folded red cloth. No people. Not colorful, not isometric, not a game render.

Add only one small compass rose / north arrow outside the floor plan in the upper right corner, labeled in Spanish with cardinal letters N, S, O, E. Use O for Oeste, not W.
North = back wall. South = street entrance with red metal rolling shutter. For this production sheet, West = visual right wall / screen-right wall, where the L-shaped counter is attached. Visual left wall has shelves.

The shop is a narrow rectangle, longer north-south than east-west. South side has centered entrance and red rolling shutter. Visual left wall has continuous tall clean shelves. North wall has back shelving.

Create a literal uppercase "L" shaped wooden service counter in plan view, same orientation as the typed letter "L". Only the short horizontal base of the L touches the visual right wall / screen-right wall at its far right end. The long vertical leg does NOT touch the wall; it sits inward/left of the wall, rising north-south from the left end of the short base. Do not attach the long vertical leg to the wall. Do not rotate it into a mirrored J shape.

Clear aisle from entrance into the shop and toward the inside of the L counter.

On the long north-south leg of the L counter, arrange props by Don Rafael's physical route, not by normal page-reading order. From south/front to north/back: folded red cloth next to small notebook with red pen, then compact generic white smart POS terminal with blank black screen and small red accent, then small clean laptop/computer with blank matte screen. Keep these objects on the long counter surface, matching the approved earlier map composition. Do not place hero objects on the short return except small secondary papers if needed.

Object orientation is west-east even though the object sequence is north-south.

The pen is horizontal: click button / cap end toward the visual right / west side, writing tip pointing toward the visual left / east side.

The laptop/computer is open but faces the wall, not the entrance or customer aisle. Use this strict left-to-right / west-to-east order across the counter: screen/display, then keyboard, then empty counter / seller-side gap, then right wall. The display panel is on the visual left / west side of the laptop, the keyboard is immediately to its visual right / east side, and the display faces east toward the right wall. Screen blank or matte dark, no UI, no text, no icons.

The POS terminal is horizontal: screen/front/keypad face oriented toward the visual right / west side, thicker base / receipt-printer end toward the visual left / east side. Keypad buttons may appear only as blank button shapes, no readable numbers, no labels, no UI.

Include subtle minimal path arrows showing movement from outside south entrance, through threshold, north along central aisle, then east to the L counter.

Clean production map, not a cinematic still, not a perspective render.

Negative: no people, no logos, no brands, no readable labels, no text blocks, no UI, no QR, no payment brand, no dirty shop, no rust, no trash, no graffiti, no flags, no soccer, no stadium, no famous landmarks, no luxury boutique, no clutter, no colorful render, no isometric game map, no saturated wood, no fully colored product bottles.
```

## Uso Recomendado En Seedance

Para una toma dentro de la tienda:

```text
Use @image1 as the exact first frame / shot composition.
Use @image2 only for Don Rafael identity.
Use @image3 only for shop layout and blocking. It is a map, not a visual style frame. Do not copy map labels, arrows, compass or diagram marks into the cinematic video.
```

Si se usa este map sheet, el prompt de video debe prohibir:

```text
no map labels, no diagram arrows, no compass copied into the scene, no floor-plan marks, no text, no UI, no logos
```
