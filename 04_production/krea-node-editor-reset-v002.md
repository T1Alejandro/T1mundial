---
title: "Krea Node Editor Reset v002"
doc_type: "operational"
status: "draft"
owner: "Arturo / Parco"
version: "0.1"
last_updated: "2026-04-29"
language: "es"
tags: ["krea", "node-editor", "reset", "16-shots", "video"]
---

# Krea Node Editor Reset v002

## Respuesta corta

Lo mejor en Krea Node Editor, si ya tienes sinopsis, tono, guion, prompts de 16 tomas y referencias de estilo, es construir un sistema por capas:

1. Un bloque maestro fijo.
2. Un bloque de estilo visual fijo.
3. Un bloque legal/negativo fijo como texto reusable dentro del prompt final.
4. Un bloque de referencias visuales separado por tipo.
5. Un nodo independiente por toma.
6. Un output independiente por toma.

No conviene meter todo en un solo prompt gigante. Tampoco conviene conectar todas las referencias a todas las tomas con el mismo peso. Eso vuelve el resultado confuso, repetitivo y menos controlable.

---

## Qué sí debe convertirse en nodo

Del brief completo, solo una parte debe entrar al Node Editor. Krea necesita instrucciones visuales, no todo el documento estratégico.

Conviene convertir en nodos:

- Concepto creativo.
- Tesis.
- Sinopsis cinematográfica resumida.
- Tono emocional.
- Reglas de look cinematográfico.
- Reglas legales y negativos, integradas al prompt maestro o al prompt final de cada toma.
- Prompts de cada toma.
- Referencias visuales de estilo, locación, personaje o UI.

No conviene convertir en nodos:

- Objetivo de awareness.
- Plan de distribución en YouTube.
- Duraciones derivadas.
- Codec de entrega.
- Especificaciones de mezcla de audio.
- Cesión de derechos de locutora.
- Stack completo de herramientas.
- Notas legales de producción que no afecten directamente la imagen.
- Guion completo de voice over como texto literal en todos los shots.

Ese material sí debe vivir en el proyecto de carpetas, porque guía la producción completa, pero no ayuda a Krea a generar mejores imágenes si se mete entero al canvas.

Regla simple: si la información cambia lo que se ve en pantalla, puede ser nodo. Si cambia cómo se produce, distribuye, edita, licencia o entrega el video, debe quedarse como documento de producción.

---

## Arquitectura recomendada

```text
[00 MASTER CONTEXT]
        |
        +--> [01 STORY / SINOPSIS]
        +--> [02 TONE / EMOTIONAL RULES]
        +--> [03 CINEMA LOOK]
        +--> [04 LEGAL / NEGATIVE TEXT BLOCK]
        +--> [05 STYLE REFERENCES]
                |
                v
        [CONCAT / PROMPT FINAL POR TOMA]
                |
        +--> [SHOT 01 FINAL PROMPT] --> [OUT 01]
        +--> [SHOT 02 FINAL PROMPT] --> [OUT 02]
        +--> [SHOT 03 FINAL PROMPT] --> [OUT 03]
        +--> [SHOT 04 FINAL PROMPT] --> [OUT 04]
        +--> [SHOT 05 FINAL PROMPT] --> [OUT 05]
        +--> [SHOT 06 FINAL PROMPT] --> [OUT 06]
        +--> [SHOT 07 FINAL PROMPT] --> [OUT 07]
        +--> [SHOT 08 FINAL PROMPT] --> [OUT 08]
        +--> [SHOT 09 FINAL PROMPT] --> [OUT 09]
        +--> [SHOT 10 FINAL PROMPT] --> [OUT 10]
        +--> [SHOT 11 FINAL PROMPT] --> [OUT 11]
        +--> [SHOT 12 FINAL PROMPT] --> [OUT 12]
        +--> [SHOT 13 FINAL PROMPT] --> [OUT 13]
        +--> [SHOT 14 FINAL PROMPT] --> [OUT 14]
        +--> [SHOT 15 FINAL PROMPT] --> [OUT 15]
        +--> [SHOT 16 FINAL PROMPT] --> [OUT 16]
```

Este árbol sirve para generar stills, keyframes o clips por toma. La lógica es: mismo mundo narrativo, mismo tono, misma protección legal, pero cada toma conserva su intención propia.

Nota verificada: no asumir que Krea tiene un nodo especial de "negative prompt". En la documentación oficial de Krea Nodes, los nodos tienen inputs, parámetros y outputs; el prompt text puede vivir como parámetro del nodo de generación, y existen utilidades de texto como LLM Call y Concat Text. Por eso, los negativos legales deben tratarse como un bloque de texto reusable que se concatena o se pega dentro del prompt final de cada toma, o como nota operativa en el canvas.

---

## Nodos listos para copiar en Krea

Usa estos textos tal cual. La idea es que no tengas que resolver el brief dentro de Krea, solo armar el canvas.

### 00 MASTER CONTEXT

Label sugerido: `00 MASTER CONTEXT - T1 Hero Film`

```text
This is a cinematic 60-90 second AI-generated hero film for T1, designed as the central YouTube campaign piece for a Mexican audience during the biggest football moment of the year. The film builds massive brand awareness by connecting two worlds: a fictional national sports team preparing for the most important match of their lives, and Mexican merchants preparing their businesses for the same collective moment.

Creative thesis: when Mexico plays, all Mexico plays. Eleven on the field, millions in their businesses. One country. One team. Everything moving at the same time, everything connected in one.

The film must feel like cinema, not like a commercial. Emotional reference: Apple-style narration in Spanish, Spotify Wrapped with cinematic epic scale, and intense visual momentum in key moments. Every frame must earn its place.

The world is premium but grounded: real Mexican commerce, everyday operators, payments, orders, dashboards, shops, markets, warehouses, teamwork, pressure, discipline and collective motion. Technology must feel useful, human and integrated into life, never futuristic for its own sake.

The film must never feel like generic stock footage, a sports broadcast, a corporate ad, a patriotic cliche, a fake AI demo, or a direct reference to any official tournament, federation, team, player, stadium, sports brand, payment brand, retailer or logistics company.
```

### 01 STORY / SINOPSIS

Label sugerido: `01 STORY - Cinematic Synopsis`

```text
Dawn breaks in Mexico. A metal shutter slowly rises at a small Mexican shop while, in another undefined place, a stadium tunnel glows and a fictional team in plain green walks toward the light. A female voiceover begins, but every line can refer either to athletes or merchants.

The camera flows between both worlds: a market vendor charges a customer with a QR code, a midfielder distributes the ball, a warehouse operator packs orders, a defender wraps his wrist and adjusts his shin guards. A young entrepreneur reviews invoices and dashboards, a striker studies the opponent on a tablet, a store owner manages sales across channels, and the bench warms up.

The rhythm accelerates through brutal match cuts: shoelaces become packing tape, rolling balls become coins and payment terminals, green turf becomes green produce. In the climax, a goalkeeper saves a penalty in impossible slow motion while a transaction is approved on screen. The commerce is protected. The goal is protected.

Then both worlds collapse into one. The stadium becomes a market. The stands become stalls. Fans become merchants and buyers. The camera zooms out until Mexico appears from above, illuminated from within: every business is a flickering light. Millions of lights. One country.

After three seconds of silence and a heartbeat, clean typography appears: Todo Mexico es uno. Todo en uno. T1. Logo. Fade to black.
```

### 02 TONE / EMOTIONAL RULES

Label sugerido: `02 TONE - Emotional Rules`

```text
Tone rules: epic but human, intimate before it becomes massive, Mexican without postcard cliches, emotional without melodrama, premium without feeling cold, energetic without becoming sports TV.

The film should feel like quiet pressure building toward a national moment. Every character is preparing with discipline. Merchants and players are treated with the same dignity. A business opening, a payment terminal, a packed order and a dashboard should feel as important as a tunnel walk, a first touch, a defensive ritual or a penalty save.

The voiceover energy is calm, low, warm and deliberate at the start, then grows in intensity without shouting. The images must preserve poetic ambiguity: each moment should be readable as business preparation and match preparation at the same time.

Avoid comedy, parody, exaggerated patriotism, obvious flag symbolism, overused Mexican stereotypes, tourist imagery, generic corporate optimism, fake futuristic interfaces, glossy AI perfection, and empty spectacle.
```

### 03 CINEMA LOOK

Label sugerido: `03 CINEMA LOOK - Visual Language`

```text
cinematic realism, premium documentary texture, anamorphic lens language, 24fps film still, shallow depth of field, controlled contrast, natural Mexican light, atmospheric depth, tactile materials, subtle film grain, elegant color grading, realistic skin, real fabric, real dust in the air, real metal, cardboard, concrete, fruit, turf and glass surfaces.

Lighting should feel motivated and cinematic: warm dawn light for openings, natural market warmth, cold functional warehouse light, clean laptop glow, stadium floodlights with haze, and a final aerial glow made of millions of business lights. Color should be rich but restrained, with deep greens, warm golds, practical whites, concrete neutrals and occasional red accents, never a literal flag treatment.

Compositions must be clean, readable at thumbnail size and strong enough to become image-to-video keyframes. Prefer controlled camera grammar: slow reveal, dolly forward, low angle, over-the-shoulder, macro detail, match cut composition, vertiginous zoom out only at the climax.

Avoid generic stock footage, overprocessed HDR, plastic AI skin, waxy faces, fake cinematic blur, chaotic composition, random neon, excessive lens flares, distorted text, unreadable UI, malformed hands, inconsistent faces and broken physics.
```

### 04 LEGAL / NEGATIVE TEXT BLOCK

Este bloque no debe entenderse como un "negative prompt node" separado, a menos que la interfaz de Krea que estés usando lo muestre explícitamente.

La forma más segura es integrarlo de una de estas tres maneras:

1. Dentro del prompt maestro.
2. Dentro del prompt final de cada toma.
3. Como bloque de texto reusable que se concatena antes de generar.

Debe incluir todo lo prohibido:

- Marcas reales.
- Logos.
- Uniformes oficiales.
- Selecciones nacionales.
- Estadios reconocibles.
- Jugadores reales.
- Celebridades.
- UI copiada.
- Texto deformado.

Este bloque es más importante de lo que parece. En una pieza con futbol y pagos, los riesgos legales aparecen rápido.

Label sugerido: `04 LEGAL NEGATIVES - Reusable Text Block`

```text
LEGAL AND QUALITY CONSTRAINTS - ALWAYS APPLY:
No FIFA, no World Cup, no Copa del Mundo, no Mundial, no Mexico 2026, no official tournament identity, no national federation identity, no Seleccion Mexicana, no El Tri, no FMF crest, no national team uniform, no official soccer kit, no real club kit, no real team crest, no recognizable stadium, no Estadio Azteca, no BBVA, no Akron, no official sports broadcast graphics.

No Adidas, no Nike, no Puma, no Under Armour, no sports brand logos, no branded football boots, no branded ball, no real athlete likeness, no celebrity likeness, no recognizable player face, no copied kit design, no official sponsor layout.

No Visa, no Mastercard, no AMEX, no Mercado Pago, no Clip, no Stripe, no PayPal, no Shopify, no Mercado Libre, no Amazon, no Walmart, no DHL, no FedEx, no UPS, no Estafeta, no Coca-Cola, no Telcel, no Bimbo, no real product packaging, no real business names, no visible trademarks, no copied software UI, no real bank logos, no real payment processor branding.

No distorted text, no malformed typography, no unreadable brand marks, no weird hands, no extra fingers, no broken wrists, no malformed faces, no inconsistent character identity, no melted objects, no broken physics, no flickering UI, no fake QR brand, no AI artifacts. If text appears, it must be generic, minimal, clean and legally safe.
```

### 05 STYLE REFERENCES

Label sugerido: `05 REFERENCES - How To Attach Images`

```text
STYLE REFS: luz, color, textura, cine, mood.
CONTENT REFS: locación, personaje, objeto, comercio, estadio, bodega.
BRAND/UI REFS: pantallas, terminales, dashboards, color T1, diseño propio.
```

Regla práctica:

- Referencias de estilo: peso bajo o medio.
- Referencias de personaje/locación: peso medio.
- Referencias de UI/marca: peso controlado y solo en tomas que lo necesiten.

No conectes una referencia de mercado a una toma de estadio si no aporta algo específico.

Copy-paste note for Krea:

```text
Use attached references with controlled influence. Style references guide color, light, lens, texture and cinematic mood. Content references guide specific locations, characters, objects or business environments only for the relevant shot. Brand/UI references guide original T1-like screens, payment terminals, dashboards and interface tone only in shots that show technology.

Do not copy logos, layouts, jerseys, stadiums, product packaging, software interfaces or real commercial identities from the references. Treat references as inspiration for mood, composition and material quality, not as objects to reproduce exactly.
```

---

## Prompt final simple si no usas Concat Text

Si Krea se vuelve más cómodo pegando un solo texto por toma, usa este orden dentro de cada prompt final:

```text
[00 MASTER CONTEXT]

[02 TONE - Emotional Rules]

[03 CINEMA LOOK - Visual Language]

[SHOT-SPECIFIC PROMPT]

[04 LEGAL NEGATIVES - Reusable Text Block]
```

No metas la sinopsis completa en todos los shots si el prompt se siente pesado. Para generar imagen o video, normalmente basta con Master + Tone + Look + Shot + Legal.

---

## Estructura por toma

Cada toma debe tener su propio nodo con esta forma:

```text
SHOT ID:
SHOT NAME:
NARRATIVE FUNCTION:
ACTION:
CAMERA:
LIGHT:
COMPOSITION:
STYLE NOTES:
CONTINUITY NOTES:
SHOT-SPECIFIC NEGATIVES:
```

Ejemplo de estructura:

```text
SHOT ID: 01
SHOT NAME: La cortina
NARRATIVE FUNCTION: abrir el video con anticipación y despertar comercial.
ACTION: una cortina metálica de una tienda mexicana empieza a subir al amanecer.
CAMERA: static medium-low camera, slow upward reveal, cinematic 16:9.
LIGHT: warm golden dawn light, dust particles, soft contrast.
COMPOSITION: symmetrical storefront, no visible logos, no readable real names.
STYLE NOTES: premium documentary realism, tactile metal texture, quiet tension.
CONTINUITY NOTES: first image of the film, must feel like the beginning of a match day.
SHOT-SPECIFIC NEGATIVES: no brands, no trademark signs, no distorted text, no people yet.
```

---

## Mejor forma de trabajar las 16 tomas

No generes las 16 tomas al mismo tiempo desde el primer intento.

Orden recomendado:

1. Generar 3 tomas ancla.
2. Aprobar look.
3. Generar 5 tomas críticas.
4. Ajustar continuidad.
5. Generar el resto.
6. Seleccionar keyframes.
7. Pasar a video o image-to-video.

### Primeras tomas ancla

Empieza con:

| Tipo | Por qué importa |
|---|---|
| Apertura | Define tono, textura y promesa. |
| Comercio humano | Define alma mexicana y marca. |
| Futbol genérico | Define riesgo legal y energía deportiva. |

Si estas tres funcionan, el resto del sistema tiene base.

---

## Configuración sugerida para outputs

### Exploración

```text
Aspect ratio: 16:9
Resolution: baja o media
Batch: 4 a 8 variantes por toma
Goal: thumbnails/contact sheet
```

### Selección

```text
Aspect ratio: 16:9
Resolution: alta
Batch: 2 a 4 variantes refinadas
Goal: keyframe candidato
```

### Video

```text
Use only approved keyframes.
Do not animate weak stills.
Keep movement simple, motivated and cinematic.
Prefer camera movement over chaotic subject movement.
```

---

## Cómo usar las referencias

### Sí

- Una referencia global de look.
- Una referencia específica por toma cuando haga falta.
- Referencias de UI solo en tomas con pantallas.
- Referencias de personaje solo cuando se busque continuidad.

### No

- No adjuntar 20 imágenes a todos los shots.
- No usar referencias con logos visibles sin limpiarlas.
- No usar frames de marcas, equipos o jugadores reales como referencia directa.
- No dejar que una referencia domine una toma que necesita otra emoción.

---

## Regla de oro

El node editor debe funcionar como una sala de dirección, no como un cajón de prompts.

Cada nodo tiene un trabajo:

- El master mantiene la película unida.
- El tono mantiene la emoción.
- El look mantiene la imagen.
- Los negativos protegen legalmente.
- Las referencias orientan.
- Cada shot decide qué pasa en pantalla.

Si un nodo no tiene un trabajo claro, se elimina.
