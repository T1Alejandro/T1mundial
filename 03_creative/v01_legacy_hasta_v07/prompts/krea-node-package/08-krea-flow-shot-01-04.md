# Krea Flow Prompt: Shots 01-04

Prompt autocontenido para pedirle al agente de Krea Nodes que arme un flujo limpio para las tomas 01 a 04.

```text
Quiero armar un workflow modular y espacialmente limpio en Krea Nodes para generar 4 keyframes cinematograficos 16:9: SHOT 01, SHOT 02, SHOT 03 y SHOT 04.

IMPORTANTE:
No ejecutes generaciones todavia.
Primero proponme el plan de workflow y costo estimado.
No uses video, enhance, upscale, variantes masivas ni pasos caros hasta que yo lo apruebe.
No asumas contexto externo. Todo lo necesario esta en este mensaje.

OBJETIVO:
Crear un flujo base editable para generar 4 keyframes individuales, uno por toma. No quiero una imagen 2x2 ni una hoja de contactos en esta etapa. Quiero nodos bien organizados para despues generar, revisar y editar cada toma por separado.

ESTRUCTURA DE CANVAS:
Organiza el canvas de izquierda a derecha:

1. Bloques globales compartidos a la izquierda:
   - GLOBAL_STYLE
   - COLOR_TEXTURE
   - CASTING
   - WARDROBE
   - GLOBAL_NEGATIVE

2. Prompts especificos por toma al centro:
   - SHOT_01_PROMPT
   - SHOT_02_PROMPT
   - SHOT_03_PROMPT
   - SHOT_04_PROMPT

3. Generadores de imagen por toma a la derecha:
   - IMAGE_GEN_SHOT_01
   - IMAGE_GEN_SHOT_02
   - IMAGE_GEN_SHOT_03
   - IMAGE_GEN_SHOT_04

4. Outputs finales al extremo derecho:
   - KEYFRAME_01
   - KEYFRAME_02
   - KEYFRAME_03
   - KEYFRAME_04

REGLA DE NODOS:
Cada toma debe tener su propio generador de imagen. No metas todas las tomas en un solo generador. Quiero poder editar una toma sin afectar las demas.

Si Krea permite conectar nodos de texto/contexto globales a cada generador, usalo.
Si no lo permite, deja los bloques globales como notas/secciones claras y copia el contenido global dentro de cada generador correspondiente.

GLOBAL_STYLE:
Cinematic 16:9 still frame. Soft photographic tone. Independent auteur cinema feeling, not commercial advertising. Gentle analog film roll-off, lifted blacks, no crushed shadows, soft highlights, fine cinematic grain. Natural light first, practical light second. Less contrast, more atmosphere, more silence, more texture than digital sharpness. Slightly nostalgic but contemporary. 35mm / 50mm lens feeling, medium to shallow depth of field, clean legible composition, no aggressive HDR, no stock look.

COLOR_TEXTURE:
Natural unsaturated greens. Warm golden-hour yellows. Soft cool shadows. Red accent #DA3B2B only where specified. Visible tactile textures: metal, skin, fabric, cardboard, concrete, grass, dust, haze. No patriotic cliches, no flags, no national emblems.

CASTING:
People in commerce/city scenes and the main green football team should have realistic Mexican / Latin American physiognomies, with natural diversity of skin tones, ages, body types and regional features. Do not caricature, exoticize or stereotype them. Do not make anyone look like a public figure, celebrity or real athlete.

Exception: referees and players from an opposing white/blue team, if they appear later, do not need to be Mexican / Latin American.

WARDROBE:
Main fictional football team: green jersey with two white graphic lines, white shorts, red socks #DA3B2B. No logos, no crests, no official identity. Jersey fabric may have subtle abstract geometric textile texture loosely inspired by pre-Hispanic pattern language, without recognizable symbols or archaeological glyphs.

GLOBAL_NEGATIVE:
no text, no captions, no subtitles, no shot numbers, no labels, no titles, no panel borders, no watermarks, no logos, no brands, no trademarks, no sports brands, no nike, no adidas, no puma, no under armour, no three stripes, no literal pre-Hispanic symbols, no recognizable archaeological glyphs, no real teams, no official uniforms, no real football kits, no national team, no Mexican national team logo, no FMF crest, no El Tri, no FIFA, no World Cup, no Copa del Mundo, no Mundial, no Mexico 2026, no stadium names, no recognizable stadium architecture, no Estadio Azteca, no sponsor boards, no branded ball, no branded boots, no real athlete likeness, no celebrity likeness, no public figure likeness, no famous landmarks, no flag overlay, no national emblem, no eagle, no stock look, no HDR overprocessing, no plastic skin, no waxy faces, no distorted anatomy, no extra fingers, no malformed hands, no broken wrists, no artifacts, no chaotic morphing, no fake cinematic blur, no excessive lens flares

SHOT_01_PROMPT:
A small Mexican shop in a historic city center at dawn. A metal roll-up shutter is opening, seen from a low three-quarter frontal angle. A partially visible silhouetted Mexican / Latin American person lifts the shutter. Warm golden light enters from below. The metal texture is the visual protagonist. Static camera, quiet suspended atmosphere, soft natural light, tactile realism. No signage, no readable text, no logo.

SHOT_02_PROMPT:
A fictional Mexican / Latin American football player walking through a stadium tunnel. Low camera close to the ground. Only legs, shin guards and silhouettes are visible. Strong backlight at the end of the tunnel. Uniform: green jersey with two white graphic lines, white shorts, red socks #DA3B2B, no logos, no crests, no official identity. Jersey fabric has subtle abstract geometric texture, not literal symbols. Same ascending light energy as Shot 01.

SHOT_03_PROMPT:
A young Mexican / Latin American person seen from behind ascending stairs toward the surface. A #DA3B2B backpack is the visual protagonist, strongly contrasting with the neutral environment. Centered medium rear framing, stair lines guide the eye. Railings and side walls create symmetry and direction. Soft frontal natural light at the top of the stairs. Open background with sky and vegetation slightly out of focus. Paused but determined movement, feeling of progress and transition into a new stage.

SHOT_04_PROMPT:
A fictional Mexican / Latin American football player ascending from the tunnel toward the field. Low rear angle focused on legs and cleats. Concrete stairs create forward motion lines. Background opens into a full stadium with blurred crowd. Soft stadium backlight ahead. Uniform: green jersey with two white graphic lines, white shorts, red socks #DA3B2B, no logos, no crests, no official identity. Medium depth of field, subject dominant, captured in an ascending step, transition from backstage to main stage.

WHAT I NEED FROM YOU NOW:
1. Propose the simplest editable workflow for these 4 keyframes.
2. Tell me which parts cost compute before running anything.
3. Recommend the cheaper calibration path first.
4. Keep the canvas spatially clean and easy to understand.
5. Do not execute until I approve.
```

