---
title: "Krea Patch - Copy-Paste Sheet v001"
doc_type: "operational"
status: "ready"
owner: "Arturo / Parco"
version: "0.2"
last_updated: "2026-04-28"
language: "es"
tags: ["krea", "patch", "copy-paste", "node-editor", "tree-architecture"]
---

# Krea Patch v001 — Copy-Paste Sheet

Arquitectura de árbol: 1 nodo raíz fijo → 13 nodos de shot → 13 nodos de output.
Los prompts y negativos vienen directo del PDF del tratamiento v1.0.

---

## ARQUITECTURA — CÓMO SE VE EN KREA

```
                        [ NODO RAÍZ — Master Context ]
                                      |
          ┌──────────────────────────────────────────────────────┐
          |          |          |          |         |           |
      [SHOT 01]  [SHOT 02]  [SHOT 03]  [SHOT 04]  [SHOT 05]  [SHOT 06]
          |          |          |          |         |           |
      [OUT 01]   [OUT 02]   [OUT 03]   [OUT 04]   [OUT 05]   [OUT 06]

          ┌──────────────────────────────────────────────────────┐
          |          |          |          |         |           |         |
      [SHOT 07]  [SHOT 08]  [SHOT 09]  [SHOT 10]  [SHOT 11]  [SHOT 13] [SHOT 14]
          |          |          |          |         |           |         |
      [OUT 07]   [OUT 08]   [OUT 09]   [OUT 10]   [OUT 11]   [OUT 13] [OUT 14]
```

Shots 12 (overlay AE), 15 (parallax AE) y 16 (cierre AE) no van en Krea — van en After Effects.

---

## CÓMO ARMARLO EN KREA — PASO A PASO

### Antes de empezar

Abre `https://www.krea.ai/nodes/` en tu canvas. Asegúrate de tener el canvas limpio o el que ya tienes abierto.

---

### PASO 1 — Crea el Nodo Raíz

Haz **clic derecho en el canvas vacío** → agrega un nodo tipo **"Text"** o **"Prompt"**.

Copia y pega el contenido del **NODO RAÍZ** de la sección de abajo.

Ponle label: `MASTER ROOT — T1 Mundial`.

Este nodo no se toca nunca. Es el ancla de todo.

---

### PASO 2 — Agrega referencias visuales (Image nodes)

Haz clic derecho → **"Image"** o **"Upload Image"** node.

Sube tus referencias aquí (las que descargues en `02_references/visual/`).

- **Style/look** (cine, color, composición) → conéctalo al Nodo Raíz o directo al nodo Output de cada shot.
- **Contenido** (personaje, locación, comercio) → conéctalo al nodo del shot específico.
- Si hay slider de **weight/influence** → ponlo en **0.3–0.5** para el primer batch. No al máximo.

---

### PASO 3 — Crea los nodos de shot (uno por cada toma)

Para cada shot:

1. Haz clic derecho → agrega nodo **"Text"** o **"Prompt"**.
2. Copia el contenido del shot correspondiente (sección de abajo).
3. **Conecta el Nodo Raíz a este nodo** — arrastra el cable de salida del Nodo Raíz a la entrada del nodo del shot.
4. Ponle label: ej. `SHOT 01 — Cortina`.

Repite para los 13 shots.

Un mismo Nodo Raíz puede conectarse a todos los shot nodes en paralelo — solo arrastra 13 cables desde el mismo nodo raíz.

---

### PASO 4 — Crea los nodos de output (uno por cada toma)

Para cada shot:

1. Haz clic derecho → agrega nodo **"Generate"** o **"Image Output"**.
2. Conéctalo al nodo del shot correspondiente.
3. Configura:
   - **Aspect ratio:** 16:9
   - **Resolution:** la más baja disponible — thumbnail / draft (512px o 768px)
   - **Batch:** 4 variantes mínimo por corrida
   - **Seed:** aleatorio en el primer batch

---

### PASO 5 — Primer batch

Corre **Shot 01** y **Shot 03** primero. Son los que mejor anclan el look (uno fío/metálico, uno cálido/humano).

Si los dos funcionan visualmente, el look del proyecto está encontrado. Corre el resto.

---

### PASO 6 — Guarda outputs

Naming para guardar localmente:

```
t1mundial_krea_shot-01_var-a_v001_20260428.png
t1mundial_krea_shot-01_var-b_v001_20260428.png
t1mundial_krea_shot-03_var-a_v001_20260428.png
```

Carpeta: `04_production/krea-stills/thumbnails/`

---

## CONTENIDO DE LOS NODOS — COPIA EXACTO

---

### NODO RAÍZ — Master Context
> Un solo nodo. Todo lo fijo va aquí. Nunca se modifica entre shots.

```
CONCEPT: A cinematic 75-second hero film where a female voice narrates two interwoven worlds — fictional generic soccer preparation and Mexican merchants preparing their businesses. The thesis: when Mexico plays, all Mexico plays. Eleven on the field, millions in their businesses. One country, one team, everything connected in one. Every shot must feel like cinema and must earn its place. Barra de calidad: Apple narrated in Spanish. Spotify Wrapped with cinematic epic. Each frame must be earned.

BRAND: T1 brand film. Mexican commerce ecosystem. Connected businesses — payments, shipping, storefront, dashboards. Daily operators. Practical technology. Humanized technology. Quiet confidence. Premium but grounded. Cinematic brand language. Not a normal commercial. Not stock footage. Not corporate. Not sports broadcast.

CINEMA LOOK: cinematic realism, anamorphic lens, shallow depth of field, 24fps film still, natural light, controlled contrast, premium documentary texture, elegant color grading, tactile materials, dust particles in air, atmospheric depth, warm human dignity, Mexican light quality, Roma by Alfonso Cuaron texture reference, Apple brand film emotional tone, no generic stock look, no overprocessed AI gloss, no plastic skin, no fake HDR

OUTPUT: thumbnail exploration, small cinematic still, 16:9 horizontal frame, clean composition, readable at small size, designed to become image-to-video input later, no text overlays, generate multiple variations, keyframe candidate quality

LEGAL HARD NEGATIVES — ALWAYS ACTIVE: no FIFA, no World Cup, no Copa del Mundo, no Mundial, no Mexico 2026, no Seleccion Mexicana, no El Tri, no FMF crest, no national team uniform, no official soccer kit, no Adidas, no Nike, no Puma, no Under Armour, no sports brand logos, no real team crest, no real player likeness, no celebrity likeness, no recognizable stadium, no Estadio Azteca, no BBVA, no Akron, no Visa, no Mastercard, no AMEX, no Mercado Pago, no Clip, no Stripe, no PayPal, no Shopify, no Mercado Libre, no Amazon, no Walmart, no DHL, no FedEx, no UPS, no Estafeta, no Coca-Cola, no Telcel, no Bimbo, no real product packaging, no readable real business names, no trademarks, no distorted text, no weird hands, no malformed faces, no broken physics
```

---

### SHOT 01 — Hook: La cortina
> 0:00–0:05 · Higgsfield + Veo

```
SHOT PROMPT: Cinematic dawn shot, slow upward reveal of metal rolling shutter at a small Mexican shop in a historic city center, golden hour sunlight backlighting dust particles in the air, warm tones, anamorphic lens, shallow depth of field, 24fps, hyperrealistic, the camera is static at medium height waiting for the reveal, ambient morning sound, no people visible yet, original architecture inspired by Mexico City centro historico, no recognizable brand names or logos visible anywhere, no signs with real business names, generic Spanish-language signage only if necessary, original character store

COMPOSITION VARIANTS:
Variant A: symmetrical front view, shutter one-third open, golden light spilling from street level
Variant B: low angle near the ground, thin line of warm light visible under the shutter only
Variant C: medium side angle, textured painted wall, dust and metal detail, interior hidden
Variant D: closer crop on shutter texture and metal rivets, interior darkness behind, cinematic suspense

SHOT-SPECIFIC NEGATIVES: no logos, no brands, no trademarks, no real product packaging, no Coca-Cola, no Telcel, no recognizable signs, no celebrities, no real people likeness, no FIFA, no Adidas, no Nike, no Mexican national team jersey
```

---

### SHOT 02 — Match cut: El túnel
> 0:05–0:10 · Veo 3.1

```
SHOT PROMPT: Cinematic shot of a soccer team walking through a stadium tunnel toward a bright field, low angle showing only legs and shin guards, players wearing solid green jerseys with NO logos, NO crest, NO sponsor, NO brand markings whatsoever, plain green fabric only, generic black shorts, white athletic socks, the tunnel is lit from the end by powerful stadium floodlights creating silhouettes, fictional generic soccer team, original characters not based on any real player, anamorphic lens, shallow depth of field, 24fps, hyperrealistic, dust particles in light beams

COMPOSITION VARIANTS:
Variant A: only legs and boots visible from ground level, bright tunnel light as destination
Variant B: back silhouettes of players walking toward field light, no faces
Variant C: close-up of boots stepping over the tunnel-to-field threshold line
Variant D: team shadow projected on tunnel wall, dramatic, no faces visible

SHOT-SPECIFIC NEGATIVES: no Mexican national team logo, no FIFA logo, no Adidas, no Nike, no Puma, no team crest, no national emblem, no World Cup logo, no recognizable kit design, no real player faces, no celebrity likeness, no Mexico shield, no Tri logo
```

---

### SHOT 03 — La señora del tianguis
> 0:10–0:15 · Seedance 2.0 + Higgsfield Soul Cast

```
SHOT PROMPT: Vibrant Mexican popular market mid-morning, woman vendor in her mid-40s with warm calm smile working her fruit and vegetable stall, she holds a small generic payment terminal in her hand, customer extends a smartphone to scan a QR code on the terminal screen, the QR code displays a clean abstract geometric design with no recognizable logo, the terminal screen is custom generic UI in dark green and gold tones, dolly camera move forward, natural market lighting with warm tones, fictional original character, hyperrealistic, anamorphic lens, 24fps, the woman wears a simple apron, the stall has fresh produce in baskets

COMPOSITION VARIANTS:
Variant A: close-up of vendor hands holding terminal, QR visible, fruit softly blurred in background
Variant B: medium portrait of vendor behind produce stall, customer phone entering from foreground
Variant C: over-the-shoulder customer scan, vendor face warm and calm in focus
Variant D: low counter-level view with fruit baskets, terminal and phone as hero objects

SHOT-SPECIFIC NEGATIVES: no Mercado Pago logo, no Clip terminal, no SR Pago, no Visa, no Mastercard, no real bank logos, no real payment processor branding, no recognizable QR brand, no Coca-Cola signs in background, no Telcel, no Bimbo packaging, no real product brands on display
```

---

### SHOT 04 — Match cut: El medio campo
> 0:15–0:20 · Kling 3.0

```
SHOT PROMPT: Soccer midfielder in solid green jersey with no logos receiving and distributing a ball with a quick first touch, low angle ground level camera following the ball movement, subtle slow motion at the moment of contact, packed stadium crowd blurred in background, anamorphic lens, golden hour stadium lights, fictional generic player not based on any real athlete, original character, jersey is plain green with NO crest NO sponsor NO brand marks, generic ball with no brand visible, hyperrealistic, 24fps

COMPOSITION VARIANTS:
Variant A: ball at contact point, foot and shin guard in sharp focus, crowd blurred behind
Variant B: ground-level wide, player distributing ball to left, stadium lights overhead
Variant C: bullet time freeze at moment of first touch, ball slightly deformed from contact
Variant D: follow-the-ball perspective, feet and turf at ground level, depth of field

SHOT-SPECIFIC NEGATIVES: no Mexican national team logo, no Adidas ball, no Nike ball, no FIFA ball, no real player likeness, no team crest, no World Cup branding, no celebrity faces, no recognizable stadium architecture
```

---

### SHOT 05 — Bodega empacando
> 0:20–0:25 · Seedance 2.0

```
SHOT PROMPT: Interior of a small Mexican working-class warehouse or workshop, man in his mid-30s methodically packing an ecommerce order, his hands close a plain unbranded brown cardboard box and apply a generic shipping label freshly printed from a thermal printer, the label has only abstract barcode and generic text in Spanish, no carrier logo visible, cold functional fluorescent and natural lighting through windows, macro detail on hands and packaging, anamorphic lens, shallow depth of field, hyperrealistic, fictional original character, simple work clothes, the workspace is clean and organized

COMPOSITION VARIANTS:
Variant A: macro on hands folding box flaps, thermal printer in soft background
Variant B: medium shot of man at packing table, organized shelves behind
Variant C: close-up of label being applied, barcode and generic Spanish text only
Variant D: wider workspace view showing organized scale of operation, no logos anywhere

SHOT-SPECIFIC NEGATIVES: no FedEx, no DHL, no Estafeta, no Mercado Libre, no Amazon, no UPS, no carrier logos, no real shipping company branding, no Mercado Envios, no 99 Minutos, no recognizable courier branding, no real product packaging visible, no celebrity likeness
```

---

### SHOT 06 — Match cut: El defensa
> 0:25–0:30 · Kling 3.0

```
SHOT PROMPT: Macro detail of soccer defender hands wrapping athletic tape around shin guards in a stadium locker room, the same hand motion as closing a box, warm locker room lighting, blurred lockers and gear in background, anamorphic lens, hyperrealistic, original character athlete not based on any real player, no team logos visible on equipment, generic athletic gear, plain solid green jersey hanging slightly visible in background with NO logos NO crest NO brand marks, 24fps

COMPOSITION VARIANTS:
Variant A: extreme macro on tape wrapping hands, warm orange locker room light
Variant B: medium shot, player seated on bench, motion of taping in progress
Variant C: over-shoulder view, locker room atmosphere behind, focus on shin guard
Variant D: hands isolated against dark background with single warm key light

SHOT-SPECIFIC NEGATIVES: no Adidas, no Nike, no Puma, no Under Armour, no team logos, no national crest, no FIFA branding, no World Cup, no real player faces, no recognizable kit
```

---

### SHOT 07 — Founder DTC
> 0:30–0:35 · Veo 3.1

```
SHOT PROMPT: Modern aspirational workspace in a trendy Mexican urban neighborhood, young Mexican woman entrepreneur in her early 30s focused on her laptop reviewing a clean custom dashboard with green and gold accent UI, the screen shows abstract sales data and metrics in a custom-designed interface that looks original and proprietary, plants on shelves, natural daylight, minimalist branded products in background with no real brand visible, ceramic coffee cup, fictional original character, hyperrealistic, anamorphic lens, shallow depth of field, 24fps, the UI on screen is custom design in dark green and gold tones, no recognizable software interface

COMPOSITION VARIANTS:
Variant A: over-shoulder view, laptop dashboard clearly visible, warm window light from left
Variant B: profile portrait, dashboard glowing subtly in midground, plants and light behind
Variant C: close-up hand on trackpad, dashboard metrics softly blurred, shallow depth
Variant D: wider workspace environmental shot, product samples and laptop as context

SHOT-SPECIFIC NEGATIVES: no Shopify interface, no Mercado Libre dashboard, no Amazon Seller Central, no Google Analytics, no Stripe dashboard, no real software UI, no Apple logo on laptop visible, no Mac logo, no recognizable brand on coffee cup, no celebrity likeness
```

---

### SHOT 08 — Match cut: El delantero
> 0:35–0:40 · Kling 3.0

```
SHOT PROMPT: Soccer striker in plain solid green training jersey studying tactical video on a tablet in an analysis room, same concentrated posture as the entrepreneur in previous shot, the tablet shows abstract play patterns and tactical diagrams, no real player faces visible on the screen, tactical whiteboard behind with chalk arrows and X marks, warm focused lighting, fictional original athlete, anamorphic lens, shallow depth of field, hyperrealistic, 24fps

COMPOSITION VARIANTS:
Variant A: mirror of founder posture — striker leaning forward over tablet, same angle
Variant B: profile view showing whiteboard tactical diagram in background
Variant C: close-up on tablet screen showing abstract movement patterns, no faces
Variant D: over-shoulder view, whiteboard arrows and player silhouette in foreground

SHOT-SPECIFIC NEGATIVES: no real player faces on tablet, no recognizable team logos, no FIFA branding, no real team crests, no Mexican national team logo, no real coach likeness, no Adidas, no Nike, no celebrity faces
```

---

### SHOT 09 — Tienda de provincia
> 0:40–0:45 · Seedance 2.0

```
SHOT PROMPT: Charming provincial Mexican shop interior, woman shop owner in her 50s managing sales on a tablet, customer in background leaving with a purchase, warm afternoon light streaming through colonial-style architecture window in background showing generic colonial Mexican street, the shop sells artisan furniture or contemporary Mexican clothing, no recognizable real-world products, original character, hyperrealistic, anamorphic lens, 24fps, the tablet shows a custom multi-channel sales dashboard with green and gold UI, abstract not literal data

COMPOSITION VARIANTS:
Variant A: medium shot, owner with tablet, customer exiting in soft background
Variant B: wide interior showing shop character, owner as part of her world
Variant C: close-up tablet with dashboard, owner hands, colonial window behind
Variant D: doorway framing shop interior with afternoon light and street visible

SHOT-SPECIFIC NEGATIVES: no famous Mexican landmarks, no real brand products, no Shopify UI, no celebrity likeness, no recognizable software interface, no Catedral de Guadalajara, no specific recognizable monument in window
```

---

### SHOT 10 — Banca calentando
> 0:45–0:48 · Kling 3.0

```
SHOT PROMPT: Soccer substitutes warming up on the sideline at night under stadium floodlights, synchronized stretching and dynamic warmup, all in plain solid green training jerseys with NO logos NO crests NO brand marks, plain athletic shorts, lateral dolly camera following the bench line, hyperrealistic, anamorphic lens, 24fps, fictional original characters not based on any real players, motivational team energy, stadium lights creating strong contrast

COMPOSITION VARIANTS:
Variant A: lateral dolly along bench line, players doing synchronized stretch
Variant B: low angle looking up at players jumping jacks against stadium floodlights
Variant C: close formation shot showing team solidarity from medium distance
Variant D: silhouette line of players against bright stadium light, dramatic contrast

SHOT-SPECIFIC NEGATIVES: no team logos, no national crest, no Adidas, no Nike, no Puma, no real player faces, no celebrity likeness, no FIFA branding
```

---

### SHOT 11 — El portero / T1Score
> 0:48–0:55 · Veo 3.1 + Higgsfield Cinema Studio

```
SHOT PROMPT: Extreme slow motion shot of a soccer goalkeeper in plain solid green-yellow gradient jersey with NO logos NO crest, diving athletically toward the upper corner of the goal to deflect a shot in the final millisecond, his fingertips graze the ball pushing it just over the crossbar, dust particles flying, dramatic stadium floodlights, intense focused expression, fictional original character not based on any real goalkeeper, hyperrealistic, anamorphic lens, 24fps with slow motion ramping, the goal net is plain white with no sponsor visible

COMPOSITION VARIANTS:
Variant A: goalkeeper fully horizontal in air, ball near gloves, stadium lights behind
Variant B: extreme close-up glove touching ball, abstract approval light reflected on glove
Variant C: low angle from goal line looking up at diving goalkeeper silhouette
Variant D: abstract — gloved hands as main subject, stadium floodlights as background stars

SHOT-SPECIFIC NEGATIVES: no Memo Ochoa likeness, no real goalkeeper faces, no Adidas, no Nike, no team crest, no Mexican national team kit, no FIFA branding, no World Cup, no celebrity likeness, no distorted hands or face
```

---

### SHOT 13 — La fusión estadio-mercado
> 0:55–1:02 · Higgsfield Cinema Studio + Kling 3.0

```
SHOT PROMPT: A grand cinematic morphing shot where a packed soccer stadium gradually transforms into a vibrant crowded Mexican market in a single continuous take with no cuts, the stadium seats organically morph into market stalls, the crowd of fans gradually transforms into merchants and customers in everyday clothes, the soccer pitch becomes a plaza of commerce, slow 360 degree camera rotation, surreal but plausible transformation, magical realism, hyperrealistic, anamorphic lens, golden hour lighting, no logos visible anywhere, no real brand stalls, no recognizable products, fictional generic Mexican market, 24fps

COMPOSITION VARIANTS:
Variant A: wide establishing shot of stadium-market hybrid, both worlds coexisting in one frame
Variant B: mid-transformation frame — stands becoming market stalls, halfway between worlds
Variant C: ground level in the merged space — field line becoming market walkway
Variant D: overhead or high angle showing the full transformation in deep perspective

SHOT-SPECIFIC NEGATIVES: no real brand products, no Coca-Cola umbrellas, no Telcel banners, no Mercado Libre signs, no real Mexican market vendor uniforms, no celebrity faces, no team merchandise, no FIFA branding, no real stadium architecture, no Azteca specific shape, no recognizable monument
```

---

### SHOT 14 — México iluminado
> 1:02–1:08 · Veo 3.1 + Higgsfield

```
SHOT PROMPT: Vertiginous zoom out from a Mexican market scene up into the night sky, revealing the entire country of Mexico from above as a constellation of glowing warm yellow and gold points of light scattered across the geographic shape of Mexico, each light representing an active business, organic twinkling pattern like an inverted starfield, cinematic scale, dramatic but emotional, the geographic outline of Mexico becomes visible as the lights cluster, anamorphic lens, hyperrealistic, 24fps, no city names visible, no political borders highlighted, just the organic shape and glow

COMPOSITION VARIANTS:
Variant A: full country silhouette made entirely of warm connected lights on dark background
Variant B: closer aerial view showing individual city clusters connecting into country shape
Variant C: dark negative space dominant, glowing Mexico shape minimal and poetic, high contrast
Variant D: subtle network lines of light connecting individual points across the country shape

SHOT-SPECIFIC NEGATIVES: no city name labels, no political map elements, no flag overlay, no national emblem, no eagle symbol, no Mexican flag colors as overlay, no FIFA logo, no World Cup elements, no specific city skylines identifiable
```

---

## SCORECARD — evalúa cada thumbnail antes de seleccionar

Solo pasan a upscale/keyframe los que sumen **24/30 o más** y tengan Legal en 5.

| Criterio | Pregunta | Score 1–5 |
|---|---|---|
| Lectura | ¿Se entiende la escena en 2 segundos? | |
| Cine | ¿Se siente como film, no como stock? | |
| T1 | ¿Se conecta a comercio / T1? | |
| Legal | ¿Cero riesgo visible de marca o likeness? | |
| Animable | ¿Puede convertirse en motion test? | |
| Emoción | ¿Tiene energía, dignidad o silencio? | |

---

## SHOTS QUE NO VAN EN KREA

| Shot | Por qué | Herramienta |
|---|---|---|
| Shot 12 — Transacción protegida | Overlay gráfico 100% diseño T1 | After Effects |
| Shot 15 — Silencio / latido | Parallax sutil sobre frame fijo de Shot 14 | After Effects |
| Shot 16 — Cierre slogan + logo | Tipografía animada + logo T1 | After Effects |
