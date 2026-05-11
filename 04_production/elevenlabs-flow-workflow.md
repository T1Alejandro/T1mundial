---
title: "ElevenLabs Flow Workflow"
doc_type: "playbook"
status: "draft"
owner: "Arturo / Parco"
reviewers: []
version: "0.1"
last_updated: "2026-04-28"
review_due: "2026-04-30"
language: "es"
audience: ["internal", "creative", "audio", "production"]
tags: ["elevenlabs", "voice", "flows", "audio", "timing"]
ai_use_cases: ["voice-direction", "audio-prototyping", "timing"]
source_of_truth: "local-project"
confidence: "medium"
assumptions:
  - "La voz final probablemente se diseñará con ElevenLabs."
related_docs:
  - "tool-stack.md"
  - "../03_creative/treatment-summary.md"
---

# ElevenLabs Flow Workflow

## Objetivo

Diseñar primero la voz, intención y timing antes de cerrar edición. La voz debe guiar el ritmo emocional del film, no solo narrarlo encima.

## Principio

La voz debe sonar diseñada, humana y dirigida. Nunca debe sentirse como lectura plana de texto.

## Flow recomendado

### 1. Flow de casting

Crear variantes por textura:

- Mujer mexicana grave-cálida.
- Voz neutra madura.
- Voz íntima, casi documental.
- Voz épica contenida.
- Voz más joven, pero seria.

Guardar en:

- `04_production/audio/elevenlabs/casting`

### 2. Flow de intención

Probar el mismo guion con tres intenciones:

- Íntima: inicio silencioso, casi confesión.
- Determinada: build con pulso y claridad.
- Épica controlada: cierre fuerte, sin gritar.

### 3. Flow de timing

Separar el guion por bloques:

| Bloque | Tiempo | Intención |
|---|---:|---|
| Hook | 0:00-0:05 | Silencio. |
| Apertura | 0:05-0:20 | Pausada, íntima. |
| Build | 0:20-0:48 | Firme, creciente. |
| Revelación | 0:48-1:08 | Emocional, controlada. |
| Silencio | 1:08-1:12 | Sin voz. |
| Cierre | 1:12-1:20 | Susurro firme. |

### 4. Flow de microdirección

Cada frase debe tener una nota:

- Respirar antes.
- Pausa después.
- Subir intención.
- Bajar volumen.
- No sonar deportiva.
- No sonar institucional.

### 5. Flow de selección

Evaluar cada salida:

- ¿Suena mexicana sin caricatura?
- ¿Tiene calidez?
- ¿Tiene gravedad?
- ¿Puede sostener silencio?
- ¿Emociona sin gritar?
- ¿La dicción es clara en celular?
- ¿Evita tono de comercial deportivo?

### 6. Flow legal / derechos

Guardar evidencia:

- Voz/modelo usado.
- Configuración.
- Fecha de generación.
- Texto exacto.
- Términos de uso aplicables.
- Export final WAV/48 kHz.

## Entregables de voz

- `voice_casting_contact_sheet.md`: notas y ranking de voces.
- `scratch_vo_v001.wav`: primer timing completo.
- `scratch_vo_v002.wav`: timing ajustado a MVP.
- `final_vo_candidate_v001.wav`: candidato final.
- `final_vo_approved.wav`: voz aprobada.

## Estructura local

- `04_production/audio/elevenlabs/casting`
- `04_production/audio/elevenlabs/timing`
- `04_production/audio/elevenlabs/final-candidates`
- `04_production/audio/elevenlabs/approved`
- `04_production/audio/elevenlabs/legal-evidence`

