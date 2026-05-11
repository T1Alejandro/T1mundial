---
title: "Preflight 01-06"
doc_type: "preflight"
status: "draft"
owner: "Arturo / Parco"
reviewers: []
version: "0.1"
last_updated: "2026-05-06"
language: "es"
audience: ["internal", "creative", "production", "editorial"]
tags: ["preflight", "sequence", "first-six", "transitions", "ai-video"]
source_of_truth: "chatgpt-master-rack-36-v004.md"
confidence: "medium"
related_docs:
  - "edit-decision-map-v001.md"
  - "transition-preflight-chat-prompt-v001.md"
  - "global-motion-rules-v001.md"
---

# Preflight 01-06

## Donde Se Evalua El Preflight

MVP recomendado:

1. En un chat visual con las stills adjuntas.
2. Usando `transition-preflight-chat-prompt-v001.md`.
3. Guardando el resultado en este archivo.

No hace falta construir software todavia. Si despues se vuelve repetitivo, se puede automatizar.

## Lectura De Secuencia

Las primeras 6 tomas no necesitan ser una sola mega-transicion continua. Funcionan como montaje paralelo:

- `01`: comercio abre.
- `02`: futbol entra al tunel.
- `03`: joven asciende escaleras.
- `04`: jugador asciende escaleras hacia campo.
- `05`: joven emerge a ciudad.
- `06`: joven se imagina/entra al estadio.

## Pregunta Sobre Escaleras En 02

No necesariamente hace falta que `02` tenga escaleras.

Motivo:

- `02` rima con `01` por simetria, camara baja, silueta y luz ascendente.
- `03` y `04` son la rima fuerte de escaleras/ascenso.
- Si metemos escaleras en `02`, podemos contaminar la claridad de su funcion: tunel, piernas, contraluz, pre-entrada.

Decision provisional:

```text
Mantener 02 como tunel bajo sin forzar escaleras.
Usar 03 -> 04 como match cut principal de escaleras/ascenso.
```

## Pair Analysis 01-06

| Pair | Funcion | Riesgo | Decision MVP | Punto de match | Render AI? | Nota |
|---|---|---|---|---|---|---|
| 01 -> 02 | Comercio abre / futbol entra | Medio | Probar match transition o match cut | pies, piso, luz, lineas verticales | Si | Rechazar todo fade/semi-fade. |
| 02 -> 03 | Futbol avanza / joven asciende | Medio | Corte editorial por avance hacia luz | direccion de avance, silueta, contraluz | No inicial | Mejor no forzar morph; probar corte en edicion. |
| 03 -> 04 | Joven sube / jugador sube | Bajo | Match cut principal | escaleras, espalda, piernas, ascenso | Opcional | Aqui vive la rima fuerte de escaleras. |
| 04 -> 05 | Jugador emerge / joven emerge | Medio | Corte editorial | idea de emergencia a espacio abierto | No inicial | Puede resolverse con ritmo/audio. |
| 05 -> 06 | Joven calle / joven estadio | Alto | Transformacion o corte con impacto | mismo rostro, mirada arriba, contra-picada | Si, con cuidado | Posible frame puente si hace dissolve. |

## Prioridad De Render MVP

1. `01 -> 02`: porque ya se probo y esta cerca.
2. `03 -> 04`: porque deberia ser la transicion mas natural.
3. `05 -> 06`: porque es la mas ambiciosa y define si Wave/Figma sirve para cambio de realidad.

No renderizar todavia:

- `02 -> 03`
- `04 -> 05`

Primero probarlos como cortes editoriales en rough cut.

## Prompt Para Evaluar 01-06 En Chat Visual

```text
Adjunto las tomas 01 a 06 en orden. Evalua la secuencia editorialmente.

No quiero que todas las uniones sean transiciones generativas. Quiero decidir cuales deben ser:
- corte directo
- match cut
- cut on action
- transicion fisica AI
- frame puente
- post/edicion

Prohibido recomendar fade, semi fade, dissolve, semi dissolve, crossfade, black frame o transicion generica.

Pon especial atencion a:
1. si 02 necesita escaleras o funciona mejor como tunel bajo
2. si 03 -> 04 debe ser la rima principal de escaleras
3. si 05 -> 06 necesita frame puente

Devuelve una tabla con pair, riesgo, decision editorial, punto de match, movimiento recomendado, si se renderiza en AI o solo en edicion.
```
