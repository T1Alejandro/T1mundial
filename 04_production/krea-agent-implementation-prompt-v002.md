---
title: "Krea Agent Implementation Prompt v002"
doc_type: "operational"
status: "ready"
owner: "Arturo / Parco"
version: "0.2"
last_updated: "2026-04-29"
language: "es"
tags: ["krea", "agent", "node-editor", "copy-paste"]
---

# Krea Agent Implementation Prompt v002

Copia el bloque completo de abajo y pégalo en el agente de Krea.

---

## PROMPT CORTO - SOLO ESTRUCTURA DEL FLUJO

Usa este si quieres preguntarle al agente de Krea cómo conviene armar el flujo sin meterle todavía todo el proyecto creativo.

```text
I want to build a practical Krea Node Editor workflow for an AI-generated cinematic video.

I already have these production inputs ready:
- a synopsis
- an emotional tone / style direction
- a full voiceover script
- prompts for 16 individual shots
- visual style references to attach
- some shot-specific references for characters, locations, UI or objects

Please use your actual knowledge of Krea Node Editor and the tools available in this canvas. Do not invent node types or features that do not exist here. If something is not possible in Krea, say so clearly and suggest the closest practical alternative.

I need you to recommend and, if possible, build the best node workflow for this situation.

Key question:
What is the best node structure in Krea when the goal is to create a video shot by shot, and the creative material already exists outside Krea?

Please decide whether it is better to:
- create reusable text/context nodes
- create one final prompt per shot
- use text concatenation if available
- paste the full final prompt manually into each generation node
- attach references globally or shot by shot
- start with still/keyframe generation before video
- build all 16 shots at once or start with a smaller anchor set

Important constraints:
- The workflow should be practical, not overly complex.
- It should let me keep consistency across all 16 shots.
- It should let me attach style references without over-influencing every shot.
- It should support shot-specific references when needed.
- It should include a place for legal/quality negative instructions, either inside the final prompt or in a negative prompt field if Krea supports one.
- Do not create a separate negative-prompt node unless that exists in this Krea canvas.
- Prioritize a workflow that helps generate cinematic stills/keyframes first, then video candidates.

Please give me:
1. The recommended node structure.
2. The exact node labels I should use.
3. What should go in each node.
4. Which nodes should connect to which.
5. Where style references should be attached.
6. Where shot-specific references should be attached.
7. Where legal/negative instructions should go.
8. Whether to start with all 16 shots or only 3 anchor shots.
9. What the first test batch should generate.

If you can create the node workflow directly in this canvas, please do it. If you cannot create it directly, give me the simplest copy-paste implementation plan.
```

---

## PROMPT PARA PEGAR EN KREA

```text
I want you to help me implement a practical Krea Node Editor workflow for a cinematic AI-generated brand film called "T1 Hero Film".

Important: use your actual knowledge of Krea Node Editor and the tools available in this canvas. Do not invent node types or features that do not exist here. If something I ask is not possible in Krea, tell me clearly and choose the closest workable alternative.

My goal is not to document the project. My goal is to build a usable node workflow that lets me generate cinematic stills/keyframes or video candidates shot by shot.

PROJECT CONTEXT
This is a cinematic 60-90 second hero film for T1, created for a Mexican audience during a major football moment. The creative idea connects two worlds: a fictional generic sports team preparing for the biggest match of their lives, and Mexican merchants preparing their businesses. Both worlds should feel like one shared national motion.

Creative thesis: when Mexico plays, all Mexico plays. Eleven on the field, millions in their businesses. One country. One team. Everything moving at the same time, everything connected in one.

The film must feel like cinema, not like a commercial. Emotional reference: Apple-style narration in Spanish, Spotify Wrapped with cinematic epic scale, and intense visual momentum in key moments. Every frame must earn its place.

VISUAL TONE
Epic but human. Mexican without postcard cliches. Premium but grounded. Emotional without melodrama. Energetic without becoming sports broadcast. Technology must feel useful, human and integrated into real commerce, never futuristic for its own sake.

CINEMA LOOK
Cinematic realism, premium documentary texture, anamorphic lens language, 24fps film still, shallow depth of field, controlled contrast, natural Mexican light, atmospheric depth, tactile materials, subtle film grain, elegant color grading, realistic skin, real fabric, dust in the air, metal, cardboard, concrete, fruit, turf and glass surfaces.

Avoid generic stock footage, overprocessed HDR, plastic AI skin, waxy faces, fake cinematic blur, chaotic composition, random neon, excessive lens flares, distorted text, unreadable UI, malformed hands, inconsistent faces and broken physics.

LEGAL AND QUALITY CONSTRAINTS
Always avoid: FIFA, World Cup, Copa del Mundo, Mundial, Mexico 2026, official tournament identity, official federation identity, Seleccion Mexicana, El Tri, FMF crest, national team uniform, official soccer kit, real club kit, real team crest, recognizable stadium, Estadio Azteca, BBVA, Akron, official sports broadcast graphics.

Always avoid: Adidas, Nike, Puma, Under Armour, sports brand logos, branded football boots, branded ball, real athlete likeness, celebrity likeness, recognizable player face, copied kit design, official sponsor layout.

Always avoid: Visa, Mastercard, AMEX, Mercado Pago, Clip, Stripe, PayPal, Shopify, Mercado Libre, Amazon, Walmart, DHL, FedEx, UPS, Estafeta, Coca-Cola, Telcel, Bimbo, real product packaging, real business names, visible trademarks, copied software UI, real bank logos, real payment processor branding.

Always avoid: distorted text, malformed typography, unreadable brand marks, weird hands, extra fingers, broken wrists, malformed faces, inconsistent character identity, melted objects, broken physics, flickering UI, fake QR brand, AI artifacts. If text appears, it must be generic, minimal, clean and legally safe.

WHAT I NEED YOU TO BUILD
Please build the simplest reliable node workflow possible in this canvas.

Preferred approach if supported:
1. Create reusable text/context blocks for:
   - Master context
   - Tone
   - Cinema look
   - Legal/quality constraints
   - Reference instructions
2. Create a reusable structure for each shot:
   - Shot-specific prompt
   - Optional attached references
   - Final generation/output node
3. If text concatenation is supported, concatenate Master + Tone + Cinema Look + Shot Prompt + Legal Constraints into the final prompt.
4. If text concatenation is not supported, create a practical workflow where I can copy the final combined prompt into each generation node.
5. Do not create a separate "negative prompt node" unless Krea actually supports that in this canvas. If negative prompts are only a field inside a generation node, place the legal/quality constraints there or include them in the final prompt text.

START SMALL
Do not build all 16 shots first. Start with only 3 anchor shots so we can validate the visual system:

SHOT 01 - La cortina / Opening commerce moment
Cinematic dawn shot, slow upward reveal of a metal rolling shutter at a small Mexican shop in a historic city center. Golden hour sunlight backlights dust particles in the air. Warm tones. Static medium-low camera. No people visible yet. Original architecture inspired by Mexico City historic center, but no recognizable location, no real business names, no brands, no logos, no trademarks. Mood: silence, anticipation, the first breath of match day and business day.

SHOT 03 - La señora del tianguis / Human commerce moment
Vibrant Mexican popular market at mid-morning. A Mexican woman vendor around 45 years old, warm calm expression, working at her fruit and vegetable stall. She holds a small generic payment terminal. A customer extends a smartphone to scan a QR code. The QR code is a clean abstract geometric design with no recognizable logo. The terminal UI is custom and generic, dark green and warm gold tones. Fresh produce in baskets. Natural market lighting. Cinematic dignity, not stock footage.

SHOT 02 - El tunel / Generic football preparation moment
Cinematic stadium tunnel shot with a fictional generic football team walking toward bright field light. Low angle, silhouettes or legs only, plain solid green jerseys with no logos, no crest, no sponsor, no brand marks, no national identity. Generic black shorts, white athletic socks, unbranded boots, fictional characters, no real player likeness. Stadium should feel generic and unrecognizable.

OUTPUT SETTINGS
Use 16:9 horizontal.
Start with low or medium resolution for thumbnails/contact sheets.
Generate multiple variations per shot if possible.
Prioritize still/keyframe quality before video.
Do not upscale or animate until the still feels visually strong.

REFERENCES
I may attach visual references. Use them only as inspiration for mood, composition, materials, color, lighting, character type or interface tone. Do not copy logos, layouts, jerseys, stadiums, packaging, product identities, software interfaces or real commercial identities from the references. If a reference is legally risky, tell me and reduce or avoid its influence.

DELIVERABLE FROM YOU
After building or proposing the workflow, explain briefly:
1. What node structure you used.
2. What was possible in Krea.
3. What was not possible or should be done manually.
4. Where I should paste shot prompts or attach references.
5. What I should generate first.

Please proceed with the most practical implementation available in this Krea canvas.
```
