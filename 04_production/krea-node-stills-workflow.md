---
title: "Krea Node Stills Workflow"
doc_type: "playbook"
status: "draft"
owner: "Arturo / Parco"
reviewers: []
version: "0.1"
last_updated: "2026-04-28"
review_due: "2026-04-30"
language: "es"
audience: ["internal", "creative", "production"]
tags: ["krea", "nodes", "stills", "thumbnails", "look-dev"]
ai_use_cases: ["look-development", "keyframe-generation", "thumbnail-testing"]
source_of_truth: "local-project"
confidence: "medium"
assumptions:
  - "Krea se usará primero para explorar stills/keyframes y thumbnails antes de animar."
related_docs:
  - "production-pipeline.md"
  - "../03_creative/shot-list/shot-tracker.md"
---

# Krea Node Stills Workflow

## Objetivo

Construir el look and feel del hero film con stills pequeños y rápidos antes de gastar tiempo en video. La prioridad es encontrar composición, luz, color, textura, personajes y lenguaje cinematográfico.

## Principio

Primero thumbnails. Luego keyframes. Luego upscale. Luego animación.

No animar una toma hasta que su still base se sienta correcto.

## Flujo por nodos

### 1. Nodo de identidad T1

Incluir contexto fijo:

- T1 es comercio mexicano conectado.
- Cine, no comercial.
- Épica cotidiana, no patriotismo obvio.
- Dignidad del comerciante.
- Tecnología humanizada.
- Cero marcas reales.
- Cero referencias directas a Mundial, FIFA, Selección o uniformes oficiales.

### 2. Nodo de toma

Definir:

- Shot ID.
- Momento narrativo.
- Acción.
- Emoción.
- Riesgo legal.
- Referencias visuales permitidas.
- Lo que debe quedar fuera.

### 3. Nodo de composición

Explorar variaciones:

- Close-up.
- Medium shot.
- Wide shot.
- Low angle.
- Over shoulder.
- Split/world overlap.
- Static cinematic frame.

### 4. Nodo de luz y color

Explorar:

- Amanecer dorado.
- Mercado cálido natural.
- Bodega fría funcional.
- Estadio con floodlights.
- Noche aérea con México iluminado.
- Contraste rojo/verde sutil sin parecer bandera literal.

### 5. Nodo de textura

Buscar:

- Piel real.
- Polvo en aire.
- Metal, cartón, concreto, tela, cancha.
- UI limpia y propia.
- Profundidad anamórfica.

### 6. Nodo de salida thumbnail

Generar grids rápidos:

- Tamaño sugerido: 512px o 768px lado largo.
- 12-24 variantes por toma crítica.
- Guardar en `04_production/krea-stills/thumbnails`.

### 7. Nodo de selección

Cada thumbnail se evalúa con:

- ¿Se entiende en 2 segundos?
- ¿Se siente cinematográfico?
- ¿Tiene alma mexicana sin cliché?
- ¿Tiene riesgo legal?
- ¿Puede animarse?
- ¿Aporta al paralelo comercio/futbol?

### 8. Nodo de upscale / keyframe

Solo los seleccionados pasan a:

- 16:9 4K keyframe.
- 9:16 test si puede funcionar para shorts.
- Still limpio para image-to-video.
- Guardar en `04_production/krea-stills/keyframes`.

## Estructura local

- `04_production/krea-stills/thumbnails`
- `04_production/krea-stills/selected`
- `04_production/krea-stills/keyframes`
- `04_production/krea-stills/rejected`
- `04_production/krea-stills/contact-sheets`

## Toma mínima para primer batch

Empezar con estas tomas:

| Shot | Por qué |
|---|---|
| 01 Cortina | Define tono inicial. |
| 02 Túnel | Define riesgo futbol/legal. |
| 03 Tianguis QR | Define comercio y humanidad. |
| 07 Founder dashboard | Define UI T1. |
| 11 Portero/transacción | Define clímax. |
| 12 Fusión estadio mercado | Define ambición visual. |
| 13 México iluminado | Define cierre épico. |

## Output esperado del Sprint 0

- 80-150 thumbnails.
- 15-25 stills seleccionados.
- 7-10 keyframes upscaleados.
- Primer contact sheet por toma.
- Criterios de look aprobados.

