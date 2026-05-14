# Character Storytime + Motion Board System — v008 v001

## Nota Interna

No pegar esta sección en Higgsfield. Sirve solo para ordenar el flujo de producción.

El objetivo es crear una ficha tipo storyboard / storytime por personaje principal para definir movimiento, cámara, cortes, rotaciones, acciones y continuidad antes de generar video.

Esto complementa las fichas visuales individuales:

- `character-model-sheet-visual-system-v008-v001.md` fija identidad, cuerpo, rostro, vestuario y props.
- Este documento fija cómo se mueve, qué hace, cómo lo mira la cámara y cómo se corta.

## Flujo Correcto

1. Aprobar model sheet visual individual del personaje.
2. Crear storytime / motion board del personaje.
3. Elegir 1-3 paneles clave como keyframes still 16:9.
4. Convertir cada panel aprobado en motion prompt.
5. Animar solo con identidad, vestuario, locación y cámara aprobados.

## Formato Visual Para Nosotros

Crear UNA imagen horizontal tipo storyboard cinematográfico para un personaje.

Composición recomendada:

- Hero still grande arriba o a la izquierda: 40% del layout.
- 6 a 9 paneles storyboard pequeños: 60% del layout.
- 90% imagen, máximo 10% texto.
- Puede incluir flechas visuales de movimiento, líneas de cámara, encuadres y notas mínimas.
- Si aparece texto, debe ser pequeño y funcional; no debe dominar.
- Los textos completos de cámara y acción van en este documento, no dentro de la imagen generada.

Cada panel debe definir:

- escala de plano,
- ángulo de cámara,
- dirección de movimiento del personaje,
- movimiento de cámara,
- continuidad del prop,
- emoción,
- punto de corte.

## Prompt Pegable — Header Maestro Para Storytime Boards

Copiar desde `FORMATO VISUAL:` hasta `PERSONAJE Y SECUENCIA:` y después pegar el bloque del personaje elegido.

```text
FORMATO VISUAL:
Crea UNA imagen horizontal grande tipo cinematic storytime / motion storyboard board para un personaje del hero film T1 v08: "El atleta del comercio mexicano".

TIPO DE PIEZA:
No es una imagen final ni un rack de personajes. Es una ficha de dirección cinematográfica para controlar narrativa, cámara, movimiento y continuidad.

La imagen debe tener layout limpio tipo storyboard de producción. 90% imagen, máximo 10% texto. Fondo claro/crema, paneles limpios, separación fina. Incluir un hero still cinematográfico grande y 6 a 9 paneles pequeños con variaciones de cámara, movimiento y continuidad. Los paneles deben sentirse como previsualización de una secuencia de video, no como collage casual.

REGLAS VISUALES:
- Mantener al personaje idéntico en todos los paneles.
- Mantener mismo vestuario, edad, rostro, pelo, complexión y props.
- Mostrar flechas de dirección de cámara o acción solo si son visuales y discretas.
- No llenar la imagen de texto.
- Priorizar storyboard visual: postura, gesto, trayectoria, rotación, cámara y continuidad.
- Cada panel debe ser cinematográfico, 16:9 o cercano a 16:9.

CONCEPTO:
"El atleta del comercio mexicano". El comerciante mexicano se filma con precisión, disciplina, concentración y dignidad de atleta de élite, pero sin deporte explícito. No hay fútbol, estadio, balón, cancha, árbitro, jugador, jersey, uniforme deportivo, escuela ni niños jugando. La épica vive en abrir la tienda, cobrar, empacar, analizar, entregar, vender y conectar negocios.

LOOK:
Cine independiente mexicano contemporáneo. Sobrio, elegante, humano, aspiracional-real. Más cine autoral que publicidad comercial. Fotografía suave, contraste medio, negros ligeramente levantados, altas luces con roll-off analógico, grano fino cinematográfico, textura real, lente 35mm/50mm, profundidad de campo media a shallow.

PALETA:
Dorado amanecer, ámbar suave, terracota suave, ocres nobles, marrones cálidos, blancos cremosos, negro suave. Rojo T1 #DA3B2B solo como acento natural y controlado. Sin verde dominante, sin tricolor, sin azul-blanco-rojo.

PANTALLAS Y BRANDING:
No generar logos T1. No generar UI final. No generar dashboards legibles. No generar stickers con palabras. No generar puntos/cruces de tracking. Pantallas, tablets, laptops, terminales y smartphones deben quedar lisos para post: blanco suave, gris claro, negro mate o reflejo óptico real.

LIMPIEZA:
Todo nuevo, limpio, cuidado e impecable. Realismo sí, suciedad no. Textura sí, deterioro no.

NEGATIVE PROMPT:
no text-dominant layout, no giant text blocks, no logos, no brands, no readable UI, no dashboard, no tracking dots, no tracking crosses, no soccer, no football, no futbol, no ball, no balon, no stadium, no estadio, no cancha, no referee, no player, no jersey, no sports uniform, no FIFA, no World Cup, no Mundial, no Mexico 2026, no flags, no patriotic styling, no green-white-red dominant palette, no famous landmarks, no stock look, no plastic skin, no distorted hands, no extra fingers, no malformed faces, no dirty floors, no grime, no rust, no peeling paint, no clutter.

PERSONAJE Y SECUENCIA:
```

## Plantilla Técnica Por Panel

Usar esta tabla para diseñar cada motion board antes de pedir imagen:

| Panel | Plano | Cámara | Acción | Movimiento | Corte |
|---:|---|---|---|---|---|
| 01 | Establishing / hero | Define eje y lente | Acción inicial | Cámara o personaje | Corte a detalle |
| 02 | Medium | Mantener eje | Preparación | Pan/track/push | Corte por gesto |
| 03 | Close-up | Macro/OTS/lateral | Mano/prop | Micro movimiento | Match cut |
| 04 | Wide/medium | Cambio controlado | Acción principal | Seguimiento | Corte a reacción |
| 05 | Close-up rostro | 35/50mm | Mirada/emoción | Push-in leve | Corte a prop |
| 06 | Macro prop | 50/100mm | Interacción | Tilt/pan corto | Corte por contacto |
| 07 | Motion beat | Bajo/lateral/OTS | Desplazamiento | Dolly/handheld suave | Corte a resolución |
| 08 | Hero resolve | Frontal/3-4 | Cierre de gesto | Cámara estable | Hold |
| 09 | Insert final | Macro/abstract | Prop/espacio | Pausa | Salida |

## Don Rafael — Storytime Board

Función narrativa:
Ritual de apertura. El atleta del comercio se prepara cada mañana cuando abre.

Duración sugerida:
12 segundos, tomas 01-03 del spot.

Secuencia:

| Panel | Plano | Cámara | Acción | Movimiento | Corte |
|---:|---|---|---|---|---|
| 01 | Hero exterior | 35mm, baja frontal | Don Rafael frente a cortina metálica limpia al amanecer | Cámara quieta, él respira y mira arriba | Corte al agarre |
| 02 | Close-up manos | 50mm, frontal bajo | Manos agarran barra de cortina | Micro push-in | Corte por tensión |
| 03 | Medium bajo | 35mm, frontal | Levanta cortina en movimiento digno | Shutter sube, luz entra | Match con luz interior |
| 04 | Over shoulder derecho | 35mm | Entra a tienda | Tracking suave detrás del hombro | Corte a pies |
| 05 | Low feet shot | 50mm bajo | Zapatos cruzan umbral limpio | Cámara acompaña paso | Corte a mostrador |
| 06 | Medium interior | 35mm lateral | Se acerca al mostrador | Pan lateral lento | Corte a manos |
| 07 | Macro manos | 100mm | Coloca terminal lisa en madera | Push-in corto | Corte a libreta |
| 08 | Macro prop | 100mm | Alinea libreta y pluma con clip rojo | Movimiento mínimo preciso | Hold |
| 09 | Hero close-up | 50mm | Mira la tienda lista | Push-in muy lento | Salida a siguiente personaje |

Prompt de imagen storyboard:

```text
Don Rafael, Mexican man 55-60, small shop owner in generic historic downtown, salt-and-pepper hair, dignified gaze, dark navy shirt, dark gray trousers, small red cloth accent. Create a cinematic storytime board showing his morning opening ritual in 9 panels: exterior low frontal shutter, hands gripping shutter, shutter rising with dawn light, over-the-shoulder entering shop, feet crossing threshold, side move to counter, macro placing blank white terminal, macro aligning notebook and red-clip pen, final dignified close-up. Warm golden dawn, clean metal shutter, immaculate shop, no logos, no UI, no text-dominant layout.
```

## Doña Carmen — Storytime Board

Función narrativa:
Cobro y entrega como gesto perfecto. Precisión amable en tianguis.

Duración sugerida:
8 segundos, tomas 04-05.

Secuencia:

| Panel | Plano | Cámara | Acción | Movimiento | Corte |
|---:|---|---|---|---|---|
| 01 | Hero puesto | 35mm, frontal 3/4 | Doña Carmen organiza frutas | Cámara estable, fondo vivo desenfocado | Corte a mano |
| 02 | Macro fruta | 50/100mm | Mano acomoda mandarina/jitomate | Tilt suave | Corte a terminal |
| 03 | OTS cliente | 50mm | Cliente acerca smartphone liso a terminal lisa | Cámara lateral | Corte por contacto |
| 04 | Close-up terminal | Macro | Terminal y smartphone se acercan | Micro push | Match cut a rostro |
| 05 | Close-up rostro | 50mm | Doña Carmen sonríe apenas, concentrada | Push-in leve | Corte a producto |
| 06 | Medium | 35mm | Toma bolsa/caja limpia de fruta | Pan con manos | Corte a entrega |
| 07 | Close-up entrega | 50mm lateral | Entrega producto a cliente | Movimiento de manos preciso | Hold |
| 08 | Hero resolve | 35mm | Doña Carmen vuelve al puesto | Cámara estable, gesto sereno | Salida |

Prompt de imagen storyboard:

```text
Doña Carmen, Mexican woman 45, clean tianguis fruit seller, white blouse, dark apron with subtle T1 red piping, serene smile. Create a cinematic storytime board in 8 panels: arranging fruit, macro fruit hand, customer OTS with blank smartphone and blank terminal, macro contactless payment, calm face close-up, picking clean fruit bag, precise handoff, final serene hero pose at clean fruit stand. Warm natural market light, no green dominance, no logos, no readable text, no QR, no clutter.
```

## Miguel — Storytime Board

Función narrativa:
Disciplina física y precisión de empaque.

Duración sugerida:
8 segundos, tomas 06-07.

Secuencia:

| Panel | Plano | Cámara | Acción | Movimiento | Corte |
|---:|---|---|---|---|---|
| 01 | Hero bodega | 35mm, baja 3/4 | Miguel frente a mesa limpia | Push-in lento | Corte a caja |
| 02 | Macro manos | 100mm | Dobla producto/prenda | Tilt con manos | Corte a caja |
| 03 | Medium lateral | 50mm | Mete producto en caja kraft | Pan corto | Corte al cierre |
| 04 | Macro caja | 100mm | Cierra solapas | Match por línea de cartón | Corte a cinta |
| 05 | Close-up cutter/cinta | Macro | Toma cinta roja lisa o blanca lisa | Movimiento rápido controlado | Corte a sellado |
| 06 | Macro sellado | 100mm | Cinta cruza caja limpia | Dolly lateral corto | Corte a etiqueta |
| 07 | Macro etiqueta | 100mm | Pega etiqueta sin texto | Micro push | Corte a rostro |
| 08 | Hero resolve | 50mm | Miguel mira caja lista | Cámara estable, respiración leve | Salida |

Prompt de imagen storyboard:

```text
Miguel, Mexican man 35, lean athletic DTC packer, black/charcoal shirt with tiny red seam, clean organized packing workshop. Create an 8-panel cinematic storytime board: hero at worktable, macro folding product, placing product into kraft box, closing box flaps, grabbing clean red/plain tape, sealing box in a precise lateral motion, applying blank label, final focused hero pose with finished package. Cool functional window light, immaculate warehouse, no logos, no text, no clutter.
```

## Sofía — Storytime Board

Función narrativa:
Estrategia, lectura de mercado, decisión.

Duración sugerida:
8 segundos, tomas 08-09.

Secuencia:

| Panel | Plano | Cámara | Acción | Movimiento | Corte |
|---:|---|---|---|---|---|
| 01 | Hero workspace | 35mm, frontal 3/4 | Sofía frente a laptop lisa | Push-in lento | Corte a pantalla |
| 02 | OTS derecho | 50mm | Mira pantalla gris/blanca lisa | Cámara detrás hombro | Corte a ojos |
| 03 | Close-up ojos | 50mm | Ojos analíticos escanean | Micro push | Corte a manos |
| 04 | Macro manos | 100mm | Teclea con precisión | Cámara fija, dedos en foco | Corte a cuaderno |
| 05 | Macro cuaderno | 100mm | Pluma clip rojo toca hoja sin texto legible | Tilt suave | Corte a producto |
| 06 | Insert producto | 50mm | Acomoda producto de emprendimiento | Pan corto | Corte a rostro |
| 07 | Medium | 35mm | Decide, respira, mira de nuevo laptop | Cámara estable | Corte final |
| 08 | Hero resolve | 50mm | Cierra gesto con seguridad tranquila | Push-in mínimo | Salida |

Prompt de imagen storyboard:

```text
Sofía, Mexican woman 32, DTC founder, black straight hair, modern workspace, minimal black/white outfit with subtle red seam. Create an 8-panel cinematic storytime board: hero at laptop, over-the-right-shoulder blank screen, analytical eyes close-up, precise typing macro, red-clip pen on notebook with no readable text, product insert, decision moment, final confident hero close-up. Elegant cool natural window light, clean Mexican urban workspace, blank screens only, no logos, no UI.
```

## Lupita — Storytime Board

Función narrativa:
Comercio regional, calidez, control multicanal sugerido.

Duración sugerida:
8 segundos, tomas 10-11.

Secuencia:

| Panel | Plano | Cámara | Acción | Movimiento | Corte |
|---:|---|---|---|---|---|
| 01 | Hero tienda | 35mm, frontal 3/4 | Lupita en mostrador | Cámara estable cálida | Corte a producto |
| 02 | Macro cerámica/textil | 50/100mm | Mano acomoda producto artesanal | Tilt suave | Corte a rostro |
| 03 | Close-up rostro | 50mm | Mira a cliente con calidez | Push-in leve | Corte a tablet |
| 04 | OTS tablet | 50mm | Revisa tablet lisa | Cámara hombro derecho | Corte a dedo |
| 05 | Macro dedo/tablet | 100mm | Dedo toca pantalla lisa | Micro push | Corte a etiqueta |
| 06 | Insert etiqueta roja | 100mm | Etiqueta roja sin texto cerca de caja | Cámara fija | Corte a entrega |
| 07 | Medium entrega | 35mm | Entrega producto o bolsa limpia | Pan corto con manos | Hold |
| 08 | Hero resolve | 50mm | Lupita queda en tienda, segura | Luz cálida, cámara estable | Salida |

Prompt de imagen storyboard:

```text
Lupita, Mexican woman 50, dignified provincial shop owner, dark dress, terracotta/red/maroon rebozo, discreet red earring, clean contemporary artisan shop. Create an 8-panel cinematic storytime board: hero at counter, macro arranging ceramic/textile product, warm face close-up, over-the-shoulder blank tablet, finger touching blank tablet, red blank label insert, clean product handoff, final dignified hero pose. Warm afternoon light, premium-real store, no tourist folklore, no logos, no readable text.
```

## Manos Diversas — Storytime Board

Función narrativa:
Millones de manos, precisión colectiva, país conectado.

Duración sugerida:
10-12 segundos, toma 12.

Secuencia:

| Panel | Plano | Cámara | Acción | Movimiento | Corte |
|---:|---|---|---|---|---|
| 01 | Macro manos 1 | 100mm | Contar dinero abstracto mexicano | Micro push | Match por mano |
| 02 | Macro manos 2 | 100mm | Cerrar caja kraft | Lateral corto | Match por cartón |
| 03 | Macro manos 3 | 100mm | Pegar etiqueta sin texto | Push-in | Match por rojo |
| 04 | Macro manos 4 | 100mm | Tocar terminal lisa | Corte por contacto | Match por pantalla |
| 05 | Macro manos 5 | 100mm | Doblar prenda | Tilt suave | Match por tela |
| 06 | Macro manos 6 | 100mm | Acomodar fruta | Pan corto | Match por color |
| 07 | Macro manos 7 | 100mm | Firmar nota ilegible | Cámara fija | Match por pluma |
| 08 | Hero collage controlled | 50mm | Varias manos en composición limpia | Hold colectivo | Salida a México nocturno |

Prompt de imagen storyboard:

```text
Diverse Mexican hands, different ages and skin tones, premium-real macro storytime board in 8 panels: counting abstract Mexican-inspired bills with no denominations, closing kraft box, applying blank red/white label, touching blank terminal, folding textile, arranging fresh fruit, signing illegible note, final clean composition of many precise hands. Real skin texture, correct anatomy, warm/cool mixed cinematic light, no logos, no readable text, no clutter, no dirt.
```
