# Step 01 — Character + Location Sheet Validation v001

## Objetivo

Validar el character + location sheet 6x2 de T1 v08 antes de producir keyframes o motion.

Nota de direccion actual:

Antes del 6x2 resumen, producir y aprobar fichas individuales tipo production model sheet para cada personaje. Estas fichas deben ser 90% imagen y 10% texto maximo, con cuerpo completo 360, detalles de cabeza, vestuario, props, entorno y prompt base.

Prompt para fichas individuales:

`03_creative/v02_v08_commerce_athlete/prompts/character-model-sheet-visual-system-v008-v001.md`

Prompt para storytime / motion boards por personaje:

`03_creative/v02_v08_commerce_athlete/prompts/character-storytime-motion-board-system-v008-v001.md`

El sheet 6x2 queda como resumen posterior. Debe fijar continuidad visual para:

- 5 personajes principales.
- 1 frame macro de manos diversas.
- 6 locaciones base.
- Paleta v08.
- Limpieza extrema.
- Superficies preparadas para post.
- Riesgo legal/ambush en cero.

## Fuente Para Generar

Prompt maestro para resumen 6x2:

`03_creative/v02_v08_commerce_athlete/prompts/higgsfield-character-location-sheet-v008.md`

Prompts individuales de respaldo:

`03_creative/v02_v08_commerce_athlete/prompts/character-location-sheet-prompts-v008-v001.md`

Prompt nuevo para fichas visuales 90/10:

`03_creative/v02_v08_commerce_athlete/prompts/character-model-sheet-visual-system-v008-v001.md`

Prompt nuevo para boards de movimiento:

`03_creative/v02_v08_commerce_athlete/prompts/character-storytime-motion-board-system-v008-v001.md`

## Gate 00 — Fichas Individuales 90/10

Debe pasar todo antes del 6x2:

- [ ] Una ficha individual por Don Rafael, Dona Carmen, Miguel, Sofia y Lupita.
- [ ] Una ficha macro para manos diversas.
- [ ] Cada ficha es 90% imagen y maximo 10% texto.
- [ ] Incluye cuerpo completo 360: frontal, 3/4, perfil y posterior.
- [ ] Incluye cabeza/rostro en varios angulos: frontal, perfil, 3/4, angulo bajo, mirada dinamica y vista superior suave.
- [ ] Incluye vestuario y accesorios en macro.
- [ ] Incluye props/herramientas del personaje.
- [ ] Incluye un still hero del personaje en su entorno.
- [ ] Incluye entorno principal y materiales.
- [ ] Incluye paleta visual.

Fallo automatico si:

- La ficha parece solo una foto de actividad.
- El texto domina mas que la imagen.
- No hay vistas 360 o no hay cuerpo completo.
- No hay detalles de rostro/vestuario/props.

## Gate 00B — Storytime / Motion Boards

Debe pasar todo antes de animar cualquier toma:

- [ ] Una ficha storyboard/motion board por personaje principal.
- [ ] Cada board mantiene identidad, vestuario, props y locación del model sheet aprobado.
- [ ] Cada board define 6-9 paneles de movimiento.
- [ ] Cada panel especifica visualmente dirección de acción, ángulo de cámara y escala de plano.
- [ ] Hay al menos un hero still por personaje.
- [ ] Hay paneles macro para manos/props.
- [ ] Hay punto de corte o transición sugerida por gesto.
- [ ] El board funciona como dirección de video, no solo como collage bonito.

Fallo automatico si:

- La IA tendría que adivinar la acción.
- No se entiende hacia dónde se mueve el personaje.
- No hay cámara definida.
- Hay cambios de identidad entre paneles.
- Hay texto dominante en vez de narrativa visual.

## Resultado Esperado

Una sola imagen horizontal grande en cuadricula exacta:

- 6 columnas x 2 filas.
- 12 frames totales.
- Todos los frames 16:9.
- Sin texto, nombres, numeros, labels, captions, logos, marcas de agua ni UI final.
- Separacion minima y uniforme.
- Lectura de izquierda a derecha y de arriba hacia abajo.

## Orden Obligatorio De Frames

| Frame | Tipo | Debe Mostrar |
|---:|---|---|
| 01 | Personaje | Don Rafael |
| 02 | Personaje | Dona Carmen |
| 03 | Personaje | Miguel |
| 04 | Personaje | Sofia |
| 05 | Personaje | Lupita |
| 06 | Personaje / macro | Manos diversas |
| 07 | Locacion | Tienda pequena Centro Historico |
| 08 | Locacion | Tianguis limpio |
| 09 | Locacion | Bodega / taller DTC |
| 10 | Locacion | Workspace moderno Sofia |
| 11 | Locacion | Tienda de provincia Lupita |
| 12 | Locacion abstracta | Mexico nocturno T1 |

## Gate 01 — Layout

Debe pasar todo:

- [ ] Cuadricula exacta 6x2.
- [ ] 12 frames, no mas, no menos.
- [ ] Frames del mismo tamano.
- [ ] Cada frame se siente 16:9 cinematografico.
- [ ] Sin collage irregular.
- [ ] Sin texto ni labels dentro de ningun frame.

Fallo automatico si:

- Aparece cualquier numero, titulo, caption, logo, watermark o UI.
- El layout no es 6x2 exacto.
- Hay frames de distintos tamanos.

## Gate 02 — Concepto v08

Debe pasar todo:

- [ ] Se entiende "El atleta del comercio mexicano".
- [ ] Los comerciantes se ven precisos, dignos y concentrados.
- [ ] No parece comercial corporativo ni stock photo.
- [ ] No hay futbol, Mundial, estadio, cancha, balon, porteria, arbitro, jugador, jersey ni uniforme deportivo.
- [ ] No hay escuela ni ninos jugando.

Fallo automatico si:

- Cualquier elemento sugiere futbol/evento masivo/patrocinio oficial.
- El sheet parece rack escolar o version anti-ambush vieja.

## Gate 03 — Cast Principal

| Personaje | Checklist |
|---|---|
| Don Rafael | 55-60, comerciante Centro Historico, pelo entrecano, manos trabajadas, mirada digna, camisa oscura, tienda pequena limpia, amanecer. |
| Dona Carmen | 45, tianguis, pelo recogido, sonrisa serena, delantal limpio, frutas calidas, terminal/superficie lisa sin logo. |
| Miguel | 35, empacador DTC, delgado atletico, concentrado, camiseta negra/gris, cajas kraft limpias, bodega ordenada. |
| Sofia | 32, founder DTC, pelo negro lacio, mirada analitica, workspace moderno, laptop lisa, cuaderno/clip/acento rojo. |
| Lupita | 50, tienda de provincia, calidez maternal, elegancia digna, rebozo terracota/rojo/marron, tablet lisa. |
| Manos diversas | Macro creible, distintas edades/tonos, dinero abstracto mexicano, caja, etiqueta, terminal, libreta; manos anatomicas. |

Fallo automatico si:

- Los personajes parecen celebridades, modelos perfectos o caricaturas.
- Hay piel plastica, manos deformes, dedos extra o anatomia rota.
- Un personaje no coincide con edad/rol/locacion.

## Gate 04 — Locaciones

Debe pasar todo:

- [ ] Tienda Centro Historico limpia, digna, sin monumentos reconocibles.
- [ ] Tianguis limpio, frutas frescas, paleta calida, verde no dominante.
- [ ] Bodega DTC ordenada, cajas nuevas, cero desorden.
- [ ] Workspace moderno mexicano, no Silicon Valley generico.
- [ ] Tienda provincia limpia, artesanal contemporanea, sin folclor turistico.
- [ ] Mexico nocturno abstracto, no mapa politico literal, sin labels ni bandera.

Fallo automatico si:

- Se ve pobreza visual, abandono, deterioro, humedad, oxido, polvo pesado o suciedad.
- Aparecen monumentos, banderas, simbolos oficiales o marcas reales.

## Gate 05 — Branding Para Post

Debe pasar todo:

- [ ] No logos T1 generados por AI.
- [ ] No UI final generada.
- [ ] No dashboards legibles.
- [ ] No stickers con palabras.
- [ ] No QR legible.
- [ ] No tracking dots, crosses, markers ni placeholders tecnicos.
- [ ] Pantallas lisas: blanco suave, gris claro, negro mate o reflejo optico real.
- [ ] Rojo T1 `#DA3B2B` aparece solo como acento natural: costura, vivo, cinta lisa, etiqueta sin texto, franja, cuaderno, clip, prop.

Fallo automatico si:

- Hay logos inventados.
- Hay texto pseudo-AI.
- Hay pantalla con UI falsa o marcas de tracking.

## Gate 06 — Paleta Y Limpieza

Debe pasar todo:

- [ ] Mundo calido mexicano: dorado, ambar, terracota suave, ocres, marrones calidos, blancos cremosos, negro suave.
- [ ] Rojo T1 visible pero no dominante.
- [ ] Cero dominante verde.
- [ ] Cero tricolor verde-blanco-rojo.
- [ ] Cero azul-blanco-rojo.
- [ ] Todo se ve nuevo, limpio, cuidado e impecable.
- [ ] Textura real sin deterioro.

Fallo automatico si:

- La imagen se va a cafe sucio, sepia, arena, tierra o pobreza visual.
- Hay mugre, polvo, manchas, grietas, oxido, cables, desorden o ropa manchada.

## Tabla De Revision

| Frame | Pasa | Problemas | Accion |
|---:|---|---|---|
| 01 Don Rafael |  |  |  |
| 02 Dona Carmen |  |  |  |
| 03 Miguel |  |  |  |
| 04 Sofia |  |  |  |
| 05 Lupita |  |  |  |
| 06 Manos diversas |  |  |  |
| 07 Tienda Centro Historico |  |  |  |
| 08 Tianguis |  |  |  |
| 09 Bodega DTC |  |  |  |
| 10 Workspace Sofia |  |  |  |
| 11 Tienda provincia Lupita |  |  |  |
| 12 Mexico nocturno |  |  |  |

## Decision

Estado del sheet:

- [ ] Aprobado para prompts por toma.
- [ ] Aprobado con ajustes menores.
- [ ] Rehacer frames especificos.
- [ ] Rehacer sheet completo.

Notas:

-

## Siguiente Paso Si Aprueba

Pasar a Step 02:

Crear 14 prompts separados, uno por toma, preservando:

- Identidad del cast principal aprobado.
- Vestuario.
- Locaciones.
- Paleta.
- Limpieza.
- Superficies lisas para post.
- Negativos legales.
