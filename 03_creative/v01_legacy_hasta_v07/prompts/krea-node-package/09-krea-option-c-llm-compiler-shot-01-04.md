# Krea Option C: LLM Compiler Flow For Shots 01-04

Prompt autocontenido para pedirle al agente de Krea que arme la Opcion C: un nodo LLM como compilador de prompts, Line Splitter y 4 generadores de imagen.

```text
Construye la Opcion C en Krea Nodes: un workflow modular con LLM como compilador de prompts para generar 4 keyframes cinematograficos 16:9: SHOT 01, SHOT 02, SHOT 03 y SHOT 04.

IMPORTANTE:
No ejecutes los generadores de imagen todavia.
Primero arma el canvas y dejalo listo para revisar.
Si necesitas ejecutar el LLM para producir las 4 lineas de prompt, avisame primero el costo y espera mi aprobacion.
No uses video, enhance, upscale ni variantes masivas.

OBJETIVO:
Mantener una sola biblia editable de estilo/casting/wardrobe y usar un LLM para comprimirla en 4 prompts finales, uno por toma, dentro del limite de caracteres.

ESTRUCTURA VISUAL DEL CANVAS:

Columna 1:
- TEXT_BIBLE_GLOBAL
- TEXT_LLM_FORMAT_RULES

Columna 2:
- LLM_PROMPT_COMPILER

Columna 3:
- LINE_SPLITTER

Columna 4:
- IMAGE_GEN_SHOT_01
- IMAGE_GEN_SHOT_02
- IMAGE_GEN_SHOT_03
- IMAGE_GEN_SHOT_04

Columna 5:
- KEYFRAME_01
- KEYFRAME_02
- KEYFRAME_03
- KEYFRAME_04

CONEXIONES:
TEXT_BIBLE_GLOBAL + TEXT_LLM_FORMAT_RULES -> LLM_PROMPT_COMPILER
LLM_PROMPT_COMPILER outputText -> LINE_SPLITTER
LINE_SPLITTER line_0 -> IMAGE_GEN_SHOT_01
LINE_SPLITTER line_1 -> IMAGE_GEN_SHOT_02
LINE_SPLITTER line_2 -> IMAGE_GEN_SHOT_03
LINE_SPLITTER line_3 -> IMAGE_GEN_SHOT_04
Each image generator outputs one 16:9 keyframe.

TEXT_LLM_FORMAT_RULES:
You are a cinematic image prompt compiler. Convert the bible and shot descriptions into exactly 4 final prompts, one prompt per line, in this order: SHOT 01, SHOT 02, SHOT 03, SHOT 04. Do not use bullets, numbering, headings, markdown, quotes, or extra commentary. Each line must be one complete prompt and must stay under 1200 characters. Each line must include the shared cinematic look, relevant casting, wardrobe when needed, the specific shot action, and compact negative restrictions. Do not generate visible text, logos, brands, real teams, official uniforms, famous landmarks, public figures, or real athlete likenesses.

TEXT_BIBLE_GLOBAL:
Global cinematic look: soft photographic tone, independent auteur cinema, not commercial advertising, gentle analog film roll-off, lifted blacks, no crushed shadows, soft highlights, fine cinematic grain, natural/practical light, less contrast, more atmosphere, more silence, tactile realism, slightly nostalgic contemporary feeling, 35mm/50mm lens feeling, medium to shallow depth of field, clean legible composition, no aggressive HDR, no stock look.

Color and texture: natural unsaturated greens, warm golden-hour yellows, soft cool shadows, red accent #DA3B2B only where specified, visible tactile textures including metal, skin, fabric, cardboard, concrete, grass, dust and haze. No patriotic cliches, no flags, no national emblems.

Casting: people in commerce/city scenes and the main green football team should have realistic Mexican / Latin American physiognomies with natural diversity of skin tones, ages, body types and regional features. Do not caricature, exoticize or stereotype them. Do not make anyone look like a public figure, celebrity or real athlete. Referees and opposing white/blue players, if they appear later, do not need to be Mexican / Latin American.

Wardrobe for main fictional football team: green jersey with two white graphic lines, white shorts, red socks #DA3B2B, no logos, no crests, no official identity. Jersey fabric may have subtle abstract geometric textile texture loosely inspired by pre-Hispanic pattern language, without recognizable symbols or archaeological glyphs.

Global negative: no text, no captions, no subtitles, no shot numbers, no labels, no titles, no panel borders, no watermarks, no logos, no brands, no trademarks, no sports brands, no three stripes, no literal pre-Hispanic symbols, no recognizable archaeological glyphs, no real teams, no official uniforms, no real football kits, no national team, no FIFA, no World Cup, no stadium names, no recognizable stadium architecture, no sponsor boards, no branded ball, no branded boots, no real athlete likeness, no celebrity likeness, no public figure likeness, no famous landmarks, no flag overlay, no national emblem, no eagle, no stock look, no HDR overprocessing, no plastic skin, no waxy faces, no distorted anatomy, no malformed hands, no artifacts, no chaotic morphing, no fake cinematic blur, no excessive lens flares.

SHOT 01: A small Mexican shop in a historic city center at dawn. A metal roll-up shutter is opening, seen from a low three-quarter frontal angle. A partially visible silhouetted Mexican / Latin American person lifts the shutter. Warm golden light enters from below. The metal texture is the visual protagonist. Static camera, quiet suspended atmosphere, soft natural light, tactile realism. No signage, no readable text, no logo.

SHOT 02: A fictional Mexican / Latin American football player walking through a stadium tunnel. Low camera close to the ground. Only legs, shin guards and silhouettes are visible. Strong backlight at the end of the tunnel. Uniform: green jersey with two white graphic lines, white shorts, red socks #DA3B2B, no logos, no crests, no official identity. Jersey fabric has subtle abstract geometric texture, not literal symbols. Same ascending light energy as Shot 01.

SHOT 03: A young Mexican / Latin American person seen from behind ascending stairs toward the surface. A #DA3B2B backpack is the visual protagonist, strongly contrasting with the neutral environment. Centered medium rear framing, stair lines guide the eye. Railings and side walls create symmetry and direction. Soft frontal natural light at the top of the stairs. Open background with sky and vegetation slightly out of focus. Paused but determined movement, feeling of progress and transition into a new stage.

SHOT 04: A fictional Mexican / Latin American football player ascending from the tunnel toward the field. Low rear angle focused on legs and cleats. Concrete stairs create forward motion lines. Background opens into a full stadium with blurred crowd. Soft stadium backlight ahead. Uniform: green jersey with two white graphic lines, white shorts, red socks #DA3B2B, no logos, no crests, no official identity. Medium depth of field, subject dominant, captured in an ascending step, transition from backstage to main stage.

WHAT I NEED NOW:
1. Build this node layout clearly and spatially clean.
2. Do not run image generation.
3. If running the LLM compiler costs compute, ask before running it.
4. Tell me if any prompt output exceeds the character limit.
5. Keep the workflow editable so I can change the bible once and regenerate prompt lines later.
```

## Variante Barata Sin LLM

Si prefieres evitar incluso el costo del LLM, puedes pegar estos prompts directamente en 4 generadores de imagen. Esto pierde modularidad, pero es mas barato y mas directo.

### IMAGE_GEN_SHOT_01

```text
Cinematic 16:9 still, soft photographic auteur cinema, lifted blacks, soft highlights, fine grain, natural/practical light, less contrast, tactile realism, 35mm/50mm feel, no stock look. Small Mexican shop in a historic city center at dawn. A metal roll-up shutter opens from a low three-quarter frontal angle. A partially visible silhouetted Mexican/Latin American person lifts it. Warm golden light enters from below. Metal texture is the visual protagonist, quiet suspended atmosphere. No text, signage, logos, brands, watermarks, HDR, plastic skin, distorted anatomy, famous landmarks.
```

### IMAGE_GEN_SHOT_02

```text
Cinematic 16:9 still, soft photographic auteur cinema, lifted blacks, soft highlights, fine grain, natural/practical light, less contrast, tactile realism, 35mm/50mm feel, no stock look. A fictional Mexican/Latin American football player walks through a stadium tunnel, low camera near the ground, only legs, shin guards and silhouettes visible, strong backlight at tunnel end. Green jersey with two white graphic lines, white shorts, red socks #DA3B2B, no logos or crests, subtle abstract geometric jersey texture. No real teams, official kits, brands, text, stadium names, HDR, distorted anatomy.
```

### IMAGE_GEN_SHOT_03

```text
Cinematic 16:9 still, soft photographic auteur cinema, lifted blacks, soft highlights, fine grain, natural light, less contrast, tactile realism, 35mm/50mm feel, no stock look. A young Mexican/Latin American person seen from behind ascends stairs toward the surface. A #DA3B2B backpack is the visual protagonist against a neutral environment. Centered medium rear framing, railings and stairs create symmetry and direction. Soft light at the top, sky and vegetation slightly out of focus, paused but determined transition. No text, labels, logos, brands, famous landmarks, HDR, plastic skin.
```

### IMAGE_GEN_SHOT_04

```text
Cinematic 16:9 still, soft photographic auteur cinema, lifted blacks, soft highlights, fine grain, practical stadium light, less contrast, tactile realism, 35mm/50mm feel, no stock look. A fictional Mexican/Latin American football player ascends from tunnel to field, low rear angle focused on legs and cleats. Concrete stairs create forward motion lines; background opens to a full stadium with blurred crowd and soft backlight. Green jersey with two white graphic lines, white shorts, red socks #DA3B2B, no logos or crests. No real teams, official kits, text, sponsor boards, stadium names, HDR, distorted anatomy.
```

