---
title: "Weave First 6 Manual Patch"
doc_type: "patch-guide"
status: "draft"
owner: "Arturo / Parco"
reviewers: []
version: "0.1"
last_updated: "2026-05-06"
language: "es"
audience: ["internal", "creative", "production"]
tags: ["figma-weave", "wave", "manual-patch", "nodes", "motion-test"]
source_of_truth: "https://app.weavy.ai/flow"
confidence: "medium"
related_docs:
  - "wave-figma-first-6-prompt-pack-v001.md"
  - "weave-first-6-flow-blueprint-v001.json"
  - "figma-weave-motion-sprint-01.md"
---

# Weave First 6 Manual Patch

## Estado Del Import JSON

No encontre en la documentacion publica de Figma Weave un formato oficial para importar un workflow completo desde JSON.

Lo que si esta documentado:

- Los workflows se construyen con nodos conectados por inputs/outputs.
- Se agregan nodos desde el menu lateral, Tab o click derecho.
- El `Import Node` acepta archivos de imagen/video/audio/GLB.
- El `Export Node` exporta imagen o video.
- Los flows compartidos pueden duplicarse desde Weave.
- Hay `Text Iterator` e `Image Iterator`, pero para este sprint conviene no batchar hasta validar que prompt e imagen se emparejan correctamente.

Por eso el archivo `weave-first-6-flow-blueprint-v001.json` es blueprint, no import garantizado.

## Patch Recomendado

Armar 6 branches paralelos:

```text
Import Still 01 -> Video Model 01 -> Preview 01 -> Export 01
Import Still 02 -> Video Model 02 -> Preview 02 -> Export 02
Import Still 03 -> Video Model 03 -> Preview 03 -> Export 03
Import Still 04 -> Video Model 04 -> Preview 04 -> Export 04
Import Still 05 -> Video Model 05 -> Preview 05 -> Export 05
Import Still 06 -> Video Model 06 -> Preview 06 -> Export 06
```

Mantener los prompts como `Text Nodes` separados para cada toma.

## Modelos A Probar Dentro De Weave

### Primera pasada

Usar `Seedance 2.0 Reference` si esta disponible en el canvas.

Motivo:

- Esta orientado a referencia.
- Deberia funcionar bien para movimiento cinematografico desde still.
- En la tabla oficial aparece dentro de los modelos de video disponibles en Weave.

Settings sugeridos:

```text
aspect ratio: 16:9
duration: 4s
resolution: 720p
versions: 1 per shot
audio: off
```

### Fallback dentro de Weave

Si `Seedance 2.0 Reference` no respeta el still:

1. `Veo 3.1 Image to Video`
2. `Runway Gen-4 Turbo`
3. `Kling 2.5 First & Last Frame`

No cambiar de modelo hasta haber visto los 6 `v001`.

## Nodos Globales

Crear estos tres text nodes al lado izquierdo del canvas:

### Global Style

```text
Cinematic Mexican commerce and football parallel world, grounded realism, authorial film language, soft analog highlight rolloff, fine grain, lifted blacks, textured skin, fabric, metal, concrete, grass, dust and haze, natural light first, practical light second, restrained warm-gold and cool-shadow palette, red accent #DA3B2B only where present in the reference, emotional but not patriotic, never stock advertising.
```

### Global Motion

```text
Animate from the provided still reference as a strict keyframe anchor. Preserve the original composition, lens language, character identity, wardrobe, environment, lighting and color. Use cinematic camera movement: controlled push-in, dolly, short pan, rack focus, shallow depth of field, natural motion blur, and purposeful atmospheric movement. Keep the shot elegant, grounded and realistic. Do not invent story elements.
```

### Global Negative

```text
no text, no captions, no subtitles, no labels, no titles, no watermarks, no logos, no brands, no trademarks, no sports brands, no official uniforms, no real football kits, no national team, no FIFA, no World Cup, no Mexico 2026, no real team symbols, no stadium names, no recognizable stadium architecture, no branded ball, no branded boots, no real athlete likeness, no celebrity likeness, no payment brands, no readable screen, no generated UI, no app icons, no UI labels, no UI numbers, no QR codes, no flag overlay, no national emblem, no eagle, no political map borders, no city labels, no map pins, no stock look, no HDR overprocessing, no plastic skin, no waxy faces, no distorted anatomy, no extra fingers, no malformed hands, no broken wrists, no artifacts, no chaotic morphing, no fake blur, no excessive lens flares, no heavy grime, no abandonment, no neglect, no destroyed walls.
```

## Orden De Armado

1. Crear nuevo file en `app.weavy.ai/flow`.
2. Importar `01.png` a `06.png` con seis `Import Nodes`.
3. Crear seis `Text Nodes`, uno por prompt de toma desde `wave-figma-first-6-prompt-pack-v001.md`.
4. Agregar seis video model nodes, uno por toma.
5. Conectar cada still al input de imagen/reference/first frame del modelo.
6. Conectar cada prompt al input `Prompt`.
7. Pegar o conectar `Global Negative` al campo `Negative Prompt` si el modelo lo expone.
8. Setear cada modelo a `16:9`, `4s`, `720p`, audio off.
9. Correr solamente `shot-01-v001`.
10. Si shot 01 respeta el still, correr `shot-02` a `shot-06`.
11. Exportar cada video con nombre local.
12. Registrar resultado en `04_production/ai-generations/motion-tests/shot-##/notes.md`.

## Naming De Export

```text
t1mundial_shot-01_wave-seedance-ref_motion-v001_20260506.mp4
t1mundial_shot-02_wave-seedance-ref_motion-v001_20260506.mp4
t1mundial_shot-03_wave-seedance-ref_motion-v001_20260506.mp4
t1mundial_shot-04_wave-seedance-ref_motion-v001_20260506.mp4
t1mundial_shot-05_wave-seedance-ref_motion-v001_20260506.mp4
t1mundial_shot-06_wave-seedance-ref_motion-v001_20260506.mp4
```

## Reglas De Iteracion

- Si cambia rostro o identidad: reducir accion, pedir "micro movement only", cambiar a modelo image-to-video mas fiel.
- Si inventa marcas/texto: reforzar negative y revisar zonas de ropa, balon, estadio y ciudad.
- Si hace morphing: pedir camera move only, no object transformation.
- Si se ve como zoom digital barato: pedir "physical dolly camera, not digital zoom".
- Si falla el movimiento humano: congelar personaje y mover camara/luz/atmosfera.
- Si el costo sube: correr solo 01, 03 y 05 antes de las 6.

## Prueba Minima

Antes de producir las 6, correr solo:

```text
shot-01-v001
```

Si el resultado respeta composicion y no mete marcas/texto, correr:

```text
shot-02-v001
shot-03-v001
shot-04-v001
shot-05-v001
shot-06-v001
```

## Fuentes Oficiales Consultadas

- Figma Weave docs: Understanding Nodes.
- Figma Weave docs: Helpers Overview.
- Figma Weave docs: Video Models Comparison.
- Figma Weave docs: Creating Files / Sharing Files / Iterators.
