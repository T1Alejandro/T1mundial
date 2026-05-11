---
title: "Krea Agent Prompt — T1 Mundial Patch v001"
doc_type: "operational"
status: "ready"
owner: "Arturo / Parco"
version: "0.1"
last_updated: "2026-04-28"
---

# Krea Agent Prompt

Copia todo el bloque de abajo y pégalo en el chat del agente de Krea.

---

## PROMPT PARA EL AGENTE DE KREA

```
I need you to build a node graph in this canvas for a cinematic brand film project called T1 Mundial. Here is the exact architecture and content for each node.

ARCHITECTURE:
- 1 Master Root text node (fixed context, never changes)
- For Shot 01 only to start: 1 Shot Base text node + 4 Variant text nodes (A, B, C, D) + 4 Image Generate nodes (one per variant)
- The Master Root connects to the Shot Base node
- The Shot Base node connects to all 4 Variant nodes
- Each Variant node connects to its own Image Generate node
- Each Image Generate node uses the Shot-Specific Negative in its negative prompt field

MASTER ROOT NODE — label it "MASTER ROOT — T1 Mundial":
CONCEPT: A cinematic 75-second hero film where a female voice narrates two interwoven worlds — fictional generic soccer preparation and Mexican merchants preparing their businesses. The thesis: when Mexico plays, all Mexico plays. Eleven on the field, millions in their businesses. One country, one team, everything connected in one. Every shot must feel like cinema and must earn its place. Quality bar: Apple narrated in Spanish. Each frame must be earned.
BRAND: T1 brand film. Mexican commerce ecosystem. Connected businesses — payments, shipping, storefront, dashboards. Daily operators. Practical technology. Humanized technology. Quiet confidence. Premium but grounded. Cinematic brand language. Not a normal commercial. Not stock footage. Not corporate. Not sports broadcast.
CINEMA LOOK: cinematic realism, anamorphic lens, shallow depth of field, 24fps film still, natural light, controlled contrast, premium documentary texture, elegant color grading, tactile materials, dust particles in air, atmospheric depth, warm human dignity, Mexican light quality, Roma by Alfonso Cuaron texture reference, Apple brand film emotional tone, no generic stock look, no overprocessed AI gloss, no plastic skin, no fake HDR
OUTPUT: thumbnail exploration, small cinematic still, 16:9 horizontal frame, clean composition, readable at small size, designed to become image-to-video input later, no text overlays, generate multiple variations, keyframe candidate quality

SHOT BASE NODE — label it "SHOT 01 — Cortina Base":
Cinematic dawn shot, slow upward reveal of metal rolling shutter at a small Mexican shop in a historic city center, golden hour sunlight backlighting dust particles in the air, warm tones, anamorphic lens, shallow depth of field, 24fps, hyperrealistic, the camera is static at medium height waiting for the reveal, no people visible yet, original architecture inspired by Mexico City centro historico, no recognizable brand names or logos visible anywhere, no signs with real business names, original character store

VARIANT A NODE — label it "Variant A":
symmetrical front view, shutter one-third open, golden light spilling from street level

VARIANT B NODE — label it "Variant B":
low angle near the ground, thin line of warm light visible under the shutter only

VARIANT C NODE — label it "Variant C":
medium side angle, textured painted wall, dust and metal detail, store interior hidden

VARIANT D NODE — label it "Variant D":
closer crop on shutter texture and metal rivets, interior darkness behind, cinematic suspense

IMAGE GENERATE NODES — one per variant:
- Aspect ratio: 16:9
- Resolution: thumbnail / draft (lowest available)
- Batch: 4 images per generate node
- Negative prompt for all 4 generate nodes: no logos, no brands, no trademarks, no real product packaging, no Coca-Cola, no Telcel, no recognizable signs, no celebrities, no real people likeness, no FIFA, no Adidas, no Nike, no Mexican national team jersey, no distorted hands, no malformed faces

Connect everything in this order:
MASTER ROOT → SHOT 01 BASE → VARIANT A → IMAGE GENERATE A
                            → VARIANT B → IMAGE GENERATE B
                            → VARIANT C → IMAGE GENERATE C
                            → VARIANT D → IMAGE GENERATE D

Start with only Shot 01. Once I approve the look from the outputs, I will give you the content for the remaining 12 shots to expand the graph.
```
