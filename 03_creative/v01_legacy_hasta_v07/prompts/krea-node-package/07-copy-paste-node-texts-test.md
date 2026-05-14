# Copy/Paste Node Texts: Test 5 Keyframes

Este archivo es para copiar textos exactos en nodos o campos de prompt. No depende de que el agente lea otros archivos.

## Node: GLOBAL_STYLE

```text
Cinematic 16:9 still frame. Soft photographic tone. Independent auteur cinema feeling, not commercial advertising. Gentle analog film roll-off, lifted blacks, no crushed shadows, soft highlights, fine cinematic grain. Natural light first, practical light second. Less contrast, more atmosphere, quiet visual rhythm, tactile realism, slightly nostalgic but contemporary. 35mm / 50mm lens feeling, medium to shallow depth of field, clean legible composition, no aggressive HDR, no stock look.
```

## Node: COLOR_TEXTURE

```text
Natural unsaturated greens. Warm golden-hour yellows. Soft cool shadows. Red accent #DA3B2B. Dark green and warm gold only for abstract generic digital surfaces. Visible tactile textures: metal, skin, fabric, cardboard, fruit, concrete, grass, dust, haze. Jerseys may have subtle abstract geometric textile texture loosely inspired by pre-Hispanic pattern language, without recognizable symbols or archaeological glyphs.
```

## Node: WARDROBE

```text
Main fictional football team: green jersey with two white graphic lines, white shorts, red socks #DA3B2B, no logos, no crest, no official identity. Opposing fictional football team: white jersey, blue shorts, white socks, no logos, no crest. Referees: fluorescent green shirt, black shorts, no logos, no insignia. Goalkeeper if needed later: solid yellow uniform, no visible identity.
```

## Node: GENERIC_DIGITAL_SCREENS

```text
Generic abstract digital surfaces only. Screens should feel real inside the scene and usable for later montage or adjustment. Use abstract blocks, empty fields, soft cards, simple visual hierarchy, white/red/dark green/warm gold accents when appropriate. No readable text, no numbers, no app icons, no brand marks, no final UX, no QR codes, no labels.
```

## Node: GLOBAL_NEGATIVE

```text
no text, no captions, no subtitles, no shot numbers, no labels, no titles, no panel borders, no watermarks, no logos, no brands, no trademarks, no sports brands, no nike, no adidas, no puma, no under armour, no three stripes, no literal pre-Hispanic symbols, no recognizable archaeological glyphs, no real teams, no official uniforms, no real football kits, no national team, no Mexican national team logo, no FMF crest, no El Tri, no FIFA, no World Cup, no Copa del Mundo, no Mundial, no Mexico 2026, no stadium names, no recognizable stadium architecture, no Estadio Azteca, no sponsor boards, no branded ball, no branded boots, no real athlete likeness, no celebrity likeness, no payment brands, no Visa, no Mastercard, no AMEX, no Mercado Pago, no Clip, no Stripe, no PayPal, no Shopify, no Mercado Libre, no Amazon, no copied UI, no fake UI clones, no generated final UX, no readable phone screen, no readable laptop screen, no readable tablet screen, no app icons, no UI labels, no UI numbers, no QR codes, no alcoholic drinks, no beer, no wine, no liquor, no cocktail glasses, no real shipping logos, no FedEx, no DHL, no UPS, no Estafeta, no Coca-Cola, no Telcel, no Bimbo, no famous landmarks, no flag overlay, no national emblem, no eagle, no political map borders, no city labels, no map pins, no satellite UI, no stock look, no HDR overprocessing, no plastic skin, no waxy faces, no distorted anatomy, no extra fingers, no malformed hands, no broken wrists, no artifacts, no chaotic morphing, no fake cinematic blur, no excessive lens flares
```

## Shot Node: SHOT_01_PROMPT

```text
Small Mexican shop in a historic city center at dawn. A metal roll-up shutter is opening, seen from a low three-quarter frontal angle. A partially visible silhouetted person lifts the shutter. Warm golden light enters from below. The metal texture is the visual protagonist. Static camera, quiet suspended atmosphere, soft natural light, tactile realism, lifted blacks, soft highlights, fine grain. No signage, no text, no logo.
```

## Shot Node: SHOT_07_PROMPT

```text
Close-up of hands shaking between players from two fictional football teams before kickoff. In the blurred background, four referees stand in line wearing fluorescent green shirts and black shorts, no logos. Main team wears green jerseys with two white graphic lines, white shorts, red socks #DA3B2B. Opposing team wears white jerseys, blue shorts, white socks. Tense pre-kickoff mood, hands as point of union and preparation, stadium background blurred, no official football identity.
```

## Shot Node: SHOT_17_PROMPT

```text
Close over-the-right-shoulder shot of hands holding a vertical smartphone inside a sneaker and sports accessories shop. The phone shows a generic abstract digital screen for later montage: clean white and red abstract blocks, empty fields, simple hierarchy, no readable text, no numbers, no icons, no labels, no final UX. Finger interacting with the screen. Background softly blurred: sneakers, football shirts, caps, warm afternoon light from the shop entrance. One pair of sneakers in #DA3B2B on an acrylic shelf.
```

## Shot Node: SHOT_29_PROMPT

```text
Hands holding a vertical smartphone over a table with Mexican food: tacos, limes, salsas and non-alcoholic drinks softly blurred. The phone shows a generic abstract digital confirmation screen: centered composition, simple success-like structure without recognizable icon, no readable text, no numbers, no labels, no final UX. Thumb ready to continue. Warm natural and practical light, organic texture, feeling of instant achievement.
```

## Shot Node: SHOT_34_PROMPT

```text
Minimal almost-black final frame. Earth seen from space in a sober cinematic composition with a large amount of negative space. Mexico is perceived only as a very faint warm glow of lights, without political outline, without literal map, without labels, without satellite UI. Quiet cosmic scale, premium abstract emotional closing, no logo, no text, not patriotic poster, not informative satellite image.
```

## Suggested Final Prompt Composition Per Shot

Si Krea pide un solo prompt por imagen, combinar asi:

```text
[SHOT_XX_PROMPT]

Apply:
[GLOBAL_STYLE]
[COLOR_TEXTURE]
[WARDROBE if football shot]
[GENERIC_DIGITAL_SCREENS if screen shot]

Negative:
[GLOBAL_NEGATIVE]
```
