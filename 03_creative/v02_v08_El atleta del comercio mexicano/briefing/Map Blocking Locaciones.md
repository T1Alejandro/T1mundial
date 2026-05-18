---
title: "Map Blocking Locaciones"
doc_type: "location-blocking"
status: "active-draft"
owner: "Arturo / Parco"
version: "0.1"
last_updated: "2026-05-18"
language: "es"
project: "T1 v08 - El atleta del comercio mexicano"
source_of_truth: false
parent_source: "Master Production Biblia.md"
---

# Map Blocking Locaciones

Este documento agrega la capa que falta entre location sheet y storyboard: planta, eje, recorrido, posiciones de camara y reglas de continuidad espacial.

No reemplaza la ficha visual aprobada de locacion. La ficha visual define look, arquitectura, materiales y paleta. Esta ficha define como se puede mover una persona y una camara dentro de ese espacio sin romper la geografia.

## Regla Operativa

Antes de generar un sequence board, keyframes o motion para una toma con desplazamiento fisico, deben existir tres cosas:

1. Character sheet aprobado.
2. Location sheet aprobado.
3. Location blocking sheet aprobado.

Si falta la planta o el eje, la IA tiende a reinventar el local entre paneles: cambia el mostrador, cruza el eje, teletransporta al personaje o transforma el interior.

## Convenciones

- Norte de planta: fondo del local.
- Sur de planta: calle / entrada / cortina.
- Izquierda y derecha se definen desde la camara base mirando desde calle hacia interior.
- Screen direction principal: Don Rafael avanza de sur a norte, de entrada a mostrador.
- Eje de accion: linea recta entrada -> pasillo central -> mostrador.
- Camara base segura: lado calle, ligeramente baja, mirando hacia interior.
- Cruce de eje: prohibido salvo que se declare como movimiento fisico visible de camara.

## Plantilla Reusable Por Locacion

```text
ID / Nombre:

Uso narrativo:

Ficha visual aprobada:

Personajes que usan esta locacion:

Planta fija:
[diagrama simple con entrada, objetos fijos, zonas transitables y zonas prohibidas]

Objetos fijos:
- Entrada:
- Mostrador / mesa principal:
- Estantes / racks:
- Ventanas / fuentes de luz:
- Props permanentes:

Eje de accion:

Screen direction permitida:

Screen direction prohibida:

Ruta principal del personaje:

Posiciones de camara permitidas:
- C01:
- C02:
- C03:

Posiciones de camara prohibidas:

Luz:

Reglas de continuidad:

Riesgos frecuentes:

Negativos especificos:
```

---

# L01 — Tienda Pequena Centro Historico

## Uso Narrativo

Ritual de apertura de Don Rafael. La toma debe sentirse como el inicio de una jornada: cortina cerrada, apertura fisica, umbral, entrada al local y primer paso hacia el interior.

## Referencias Aprobadas

- Personaje: Don Rafael, character sheet aprobado.
- Locacion: L01, tienda pequena del Centro Historico, location sheet aprobada.
- Blocking map aprobado: `07_assets/locations/blocking-maps/L_Tienda-pequena-centro-historico-blocking-map.png`

No usar otras imagenes para resolver arquitectura, layout, fachada, interior, ropa o identidad.
Para geometria, posicion de mostrador, anaqueles, pasillo vendedor, props y orientacion de dispositivos, el blocking map aprobado manda sobre cualquier descripcion escrita si hubiera duda.

## Planta Fija Activa

Vista desde arriba. La calle esta abajo. El fondo del local esta arriba.

```text
                         FONDO DEL LOCAL / NORTE

        ┌────────────────────────────────────────────┐
        │                                            │
        │        ANAQUEL FONDO CON PRODUCTO ORDENADO │
        │                                            │
        │  ANAQUEL IZQ.                              │
        │                                            │
        │              PASILLO CENTRAL               │
        │                                            │
        │                         PARED DERECHA      │
        │                         LIMPIA             │
        │                                            │
        │               ┌──────────────┐     │        │
        │               │ MOSTRADOR    │     │        │
        │               │ LARGO        │     │        │
        │               │ terminal     │     │        │
        │               │ pano rojo    │     │        │
        │               │ libreta      │     │        │
        │               │ pluma        │     │        │
        │               └──────────────┴─────┘        │
        │                    PASILLO VENDEDOR         │
        │                                            │
        └─────────────── CORTINA Y ENTRADA ──────────┘

                         CALLE / SUR
```

Regla activa de caja L01:

- No hay anaquel derecho corrido.
- La pared derecha queda limpia.
- La caja lateral derecha tiene forma de L, no isla y no C.
- La barra larga corre norte-sur y queda separada de la pared derecha para crear un pasillo vendedor.
- El brazo corto/base de la L queda al sur/frente y toca o llega hasta la pared derecha.
- El acceso al pasillo vendedor queda por el extremo posterior/norte abierto de la L, no por la entrada.
- La secuencia operativa de props sobre la barra larga sigue el recorrido fisico de Don Rafael, de sur a norte: pluma -> libreta -> pano rojo -> terminal punto de venta.

## Objetos Fijos

- Cortina metalica: al sur, plano frontal del local, se abre verticalmente.
- Entrada / umbral: mismo eje que cortina, conecta calle con pasillo central.
- Mostrador: caja lateral derecha en forma de L. La barra larga corre norte-sur y queda separada de la pared derecha; el brazo corto/base toca o llega a la pared derecha hacia el sur/frente.
- Anaqueles: pared izquierda y fondo, ordenados, sin marcas legibles. No hay anaquel derecho corrido.
- Piso: limpio, continuo, con lineas de perspectiva hacia el fondo.
- Luz principal: amanecer desde la calle, entra desde el sur hacia el norte.
- Props de mostrador: sobre la barra larga de la L, de sur a norte por recorrido fisico: pluma, luego libreta, luego pano rojo, luego terminal punto de venta.
- Orientacion de dispositivo: la terminal punto de venta es un rectangulo horizontal OESTE-ESTE sobre la profundidad del mostrador. Pantalla a la izquierda/OESTE, botones a la derecha/ESTE; el frente de uso mira hacia la pared derecha vacia, no hacia el pasillo central ni hacia cliente.

## Eje De Accion

Eje principal:

```text
CALLE -> CORTINA / UMBRAL -> PASILLO CENTRAL -> MOSTRADOR
```

La camara debe permanecer del mismo lado de este eje durante la apertura y entrada. El movimiento puede cambiar de exterior a interior, pero debe sentirse como continuidad fisica, no como salto a otra tienda.

## Screen Direction

Permitida:

- Don Rafael avanza de calle hacia interior.
- En paneles exteriores, su espalda o tres cuartos mira hacia la cortina.
- En paneles de entrada, la luz queda detras o lateral desde la entrada.
- En paneles interiores, la cortina abierta queda detras de el o al fondo sur coherente.

Prohibida:

- Don Rafael abriendo la cortina desde adentro.
- Don Rafael cambiando de lado del mostrador sin mostrar el cruce.
- Mostrador que aparece a izquierda en un panel y a derecha en otro sin justificacion.
- Entrada que cambia de fondo a lateral sin movimiento de camara declarado.
- Interior que se vuelve mas profundo, mas ancho o con otra arquitectura entre paneles.

## Ruta De Don Rafael Para Toma 01

```text
P01: espera afuera frente a cortina cerrada.
P02: se acerca a la barra inferior.
P03: manos toman la cortina.
P04: levanta primeros centimetros.
P05: cortina sube a media altura.
P06: reajusta manos sin cambiar posicion espacial.
P07: termina apertura.
P08: baja manos.
P09: respira mirando calle/luz.
P10: gira hacia interior.
P11: cruza umbral.
P12-P16: primer paso hacia pasillo central / interior listo.
```

Para el sequence board especifico de apertura, no hace falta llegar hasta mostrador. El mostrador puede revelarse como profundidad ordenada, pero el objetivo de la toma 01 es abrir y entrar.

## Posiciones De Camara Permitidas

```text
                         FONDO / NORTE

        ┌────────────────────────────────────────────┐
        │                                            │
        │                  C04                       │
        │          interior frontal controlado       │
        │                                            │
        │                                            │
        │                  ruta                      │
        │                                            │
        │        ┌──────────────────────────┐        │
        │        │        mostrador         │        │
        │        └──────────────────────────┘        │
        │                                            │
        └─────────────── entrada / cortina ──────────┘
             C02                 C01              C03
          calle izq.        calle frontal      calle der.

                         CALLE / SUR
```

- C01 / calle frontal baja: camara principal para apertura. Segura para paneles 01-10.
- C02 / calle izquierda tres cuartos: permitida si mantiene la misma fachada y no invierte direccion.
- C03 / calle derecha tres cuartos: permitida como variacion leve, no alternar con C02 dentro del mismo sequence board.
- C04 / interior mirando hacia entrada: usar solo despues de cruzar umbral o como panel final. Debe sentirse como cambio fisico posterior, no como corte arbitrario.

## Camara Recomendada Para Sequence Board 4x4 De Toma 01

Mantener C01 como base durante la mayor parte de la secuencia. Usar un push-in fisico muy sutil:

```text
Paneles 01-04: C01 exterior, plano amplio/medio bajo, Don Rafael de espalda o 3/4.
Paneles 05-08: C01 exterior mas cerca, cortina sube, interior se revela.
Paneles 09-12: C01 / umbral, camara acompana elevacion y respiracion.
Paneles 13-16: C01 empuja hacia umbral; Don Rafael gira y da primer paso hacia interior.
```

No saltar a C04 salvo que se quiera cerrar con interior hacia entrada. Para esta toma, la opcion mas estable es no cruzar eje y no invertir POV.

## Lentes

- 35mm para exteriores, apertura e interior revelado.
- 50mm para momentos medios de manos/cuerpo, sin cerrar demasiado.
- Evitar macro extremo en este sequence board: la toma debe leerse como accion continua y espacial.

## Luz

- Amanecer bajo desde calle / sur.
- Luz dorada entra por debajo de cortina y luego por la apertura.
- El interior recibe luz calida progresivamente.
- No cambiar a luz nocturna, luz fria dominante ni sol alto.

## Reglas De Continuidad Para Prompt

Usar este bloque dentro de cualquier prompt de Toma 01:

```text
LOCATION BLOCKING LOCK:
Use a fixed floor plan. The metal shutter and entrance are always at the front/south side of the shop. The left wall and back wall have shelves; the right wall stays clean. The clean wooden counter is a right-side L-shaped cashier counter, fixed in the same position across all panels: long leg north-south separated from the right wall, short/front leg closing toward the right wall. Dawn light always enters from the street through the shutter/entrance. Don Rafael starts outside, opens the shutter from outside, then turns and takes his first step inside. Keep the same camera side and same screen direction: street -> shutter -> threshold -> interior. Do not cross the axis. Do not reverse the shop. Do not move the counter, shelves, entrance, shutter, props or light direction between panels.
```

## Negativos Especificos De Blocking

```text
no camera axis crossing, no reversed shop layout, no counter switching sides, no shelves changing walls, no opening shutter from inside, no Don Rafael already inside before opening, no teleporting across threshold, no inconsistent entrance position, no changing shutter design, no changing interior depth, no different shop architecture between panels, no prop teleporting, no object moving by itself, no abrupt angle change, no disconnected montage, no random POV from inside unless physically motivated after entering
```

## Checklist De Aprobacion L01

- La cortina siempre pertenece a la misma fachada.
- Don Rafael siempre abre desde afuera.
- La luz de amanecer siempre viene desde la calle.
- La entrada no cambia de lado.
- El interior se revela progresivamente, no aparece como otro set.
- El mostrador y anaqueles se mantienen fijos si aparecen.
- El movimiento se lee de calle a interior.
- No hay cruce de eje ni inversion de screen direction.
- No hay paneles que parezcan otra toma, otra tienda u otro actor.

## Decisiones De Planta L01

Estas decisiones sustituyen las iteraciones viejas de planta. No copiar versiones anteriores.

- El mapa L01 activo es una planta arquitectonica pura: sin camaras, conos, ruta, personaje ni diagrama de accion.
- El local es angosto y profundo, con calle al sur y fondo al norte.
- Los anaqueles van solo en pared izquierda y fondo. La pared derecha queda limpia para caja, pasillo vendedor y muro.
- La caja lateral derecha es una L funcional: barra larga norte-sur separada de pared derecha; brazo corto/base al sur/frente tocando o llegando a pared derecha.
- El pasillo vendedor se accede por el extremo posterior/norte abierto de la L, no por la entrada.
- Los props principales van sobre la barra larga, siguiendo el recorrido fisico sur -> norte: pluma -> libreta -> pano rojo -> terminal punto de venta.
- La terminal punto de venta es un rectangulo horizontal OESTE-ESTE sobre la profundidad del mostrador. Pantalla a la izquierda/OESTE, botones a la derecha/ESTE; el frente de uso mira hacia la pared derecha vacia, no hacia pasillo central, entrada ni cliente.
- El storyboard define camara y recorrido de Don Rafael despues. El mapa solo fija arquitectura y objetos.

---

# Prompts Pegables — L01

## 01 — Prompt Para Crear Mapa Tecnico / Blocking Map L01 Activo

Usar primero en una ventana nueva, sin adjuntar imagenes. Este prompt debe ser autocontenido.

```text
Haz una imagen horizontal 16:9 de un plano de planta arquitectonico tecnico para una tienda pequena tradicional del Centro Historico de Ciudad de Mexico, zona Donceles/Zocalo, propiedad de Don Rafael.

La imagen debe ser SOLO vista superior. Debe verse como floor plan arquitectonico limpio. No debe ser render, no debe ser fachada, no debe ser storyboard, no debe ser moodboard, no debe parecer diagrama de camaras.

No uses imagenes de referencia para este mapa. La planta debe nacer del arquetipo de local tradicional angosto del Centro Historico, tipo Donceles, no de una boutique contemporanea.

OBJETIVO:
Crear un plano de planta claro para continuidad cinematografica, no una imagen bonita, no un moodboard, no una escena final.
La imagen debe servir para entender solo la arquitectura de la tienda, la posicion de la caja en L, el pasillo central, el anaquel izquierdo, el anaquel de fondo, la pared derecha limpia, el pasillo vendedor y el acceso a caja.

FORMATO:
- Una sola imagen horizontal 16:9.
- Estilo plano arquitectonico de planta, limpio, simple y legible.
- Fondo blanco o gris claro limpio.
- Muros en lineas negras mas gruesas, mobiliario en lineas grises finas.
- SOLO vista superior. Solo floor plan tecnico.
- El plano de planta debe ocupar todo el canvas.
- No incluir fachadas, elevaciones, cortes, vistas laterales, vistas isometricas, perspectivas 3D, thumbnails, renders, miniaturas ni paneles secundarios.
- No crear una lamina de arquitectura con multiples vistas.
- Todo debe ser limpio, tecnico, ordenado y facil de leer, parecido a un plano arquitectonico.

IMPORTANTE SOBRE TEXTO:
Sin texto dentro de la imagen salvo una rosa de los vientos pequena. Evitar palabras, numeros, titulos, labels largos, captions, UI o metadata.

ORIENTACION:
Agregar una rosa de los vientos pequena y limpia fuera de la planta, en la esquina superior derecha, con letras cardinales en espanol: N, S, O, E. Usar O de Oeste, no W.
Norte = fondo del local.
Sur = calle / entrada / cortina metalica.

PLANTA FIJA:
La calle esta al sur, en la parte inferior del plano.
El fondo del local esta al norte, en la parte superior del plano.
La cortina metalica y entrada estan al sur, en el frente del local.
El local es pequeno, rectangular, limpio y profundo.
Hay anaquel alto y continuo en pared izquierda, y anaquel/vitrina de fondo. La pared derecha no debe tener anaquel; queda limpia y reservada para caja, pasillo vendedor y muro.
Los anaqueles deben verse como muebles/vitrinas anchos, limpios y casi vacios. En el plano de planta no hace falta dibujar toda la mercancia; puede haber solo una insinuacion minima de productos.
Anaquel izquierdo: vitrina/anaquel continuo de sur a norte, pegado a pared izquierda, con pocas formas simples que sugieran productos de cabello/barba/cuidado personal, sin logos ni etiquetas legibles.
Anaquel de fondo: vitrina/anaquel continuo en pared norte/fondo, limpio y ordenado, casi vacio, sin puerta visible y sin saturacion de objetos.
La prioridad es arquitectura clara, no inventario.
Hay un pasillo central transitable desde la entrada hacia el interior.
Hay un mostrador de madera cuidado en el lado derecho, cerca de la entrada o a media profundidad, como caja funcional de tienda tradicional. El mostrador debe tener forma de L, no de C. La barra larga corre paralela al eje largo del local, de sur a norte, y queda separada de la pared derecha para formar un pasillo vendedor estrecho. El brazo corto/base de la L queda hacia el sur/frente, cierra el frente de la caja y toca o llega hasta la pared derecha. Toda la caja en L es un solo mueble continuo de la misma altura: barra larga y brazo corto comparten una sola cubierta superior al mismo nivel. No dibujar desnivel, escalon, banca, plataforma, pedestal, doble nivel ni modulo bajo. No debe haber acceso directo a la caja desde la entrada. No debe ser una isla central. El extremo posterior/norte de la L queda abierto hacia el fondo para que el vendedor pueda pasar detras de la barra; no dibujar puerta, vano, arco ni entrada formal. El pasillo central del cliente debe quedar libre.
Sobre el mostrador deben indicarse props como formas geometricas simples, sin texto, siempre en orden sur/frente hacia norte/fondo: pluma, libreta, pano rojo, terminal punto de venta.

PROPS / ELEMENTOS FIJOS SOBRE LA BARRA LARGA:
Colocar todos los props principales sobre la barra larga norte-sur de la L, no sobre el brazo corto/base. La disposicion se lee por recorrido fisico desde SUR/frente hacia NORTE/fondo, igual que en el blocking map aprobado. No usar lectura normal de pagina.

1. Pluma:
- Posicion: extremo SUR/frente de la barra larga, cerca del brazo corto/base de la L.
- Orientacion: horizontal de oeste a este sobre la profundidad del counter.
- Boton/capuchon/clip rojo: hacia OESTE / lado del pasillo central.
- Punta de escritura: hacia ESTE / pared derecha / pasillo vendedor.
- Sin texto, sin marca, sin logo.

2. Libreta:
- Posicion: inmediatamente al NORTE de la pluma, todavia en la zona SUR/frente de la barra larga.
- Forma: libreta pequena cerrada, limpia, sin texto visible.
- Orientacion: alineada con el eje de la barra o ligeramente vertical norte-sur; debe sentirse apoyada de forma ordenada sobre el counter.
- No generar escritura, numeros, notas ni etiquetas.

3. Pano rojo:
- Posicion: inmediatamente al NORTE de la libreta, antes de la terminal punto de venta.
- Forma: pano rojo T1 doblado, pequeno, como acento de color.
- Orientacion: levemente diagonal, siempre sobre la barra larga y sin invadir el brazo corto/base.
- Sin logo, sin texto, sin patron.

4. Terminal punto de venta:
- Posicion: zona MEDIA/NORTE de la barra larga, al NORTE del pano rojo; despues de la terminal queda superficie libre de counter hacia el fondo.
- Forma: terminal punto de venta generica tipo handheld con la forma fisica de la referencia: cuerpo blanco, carcasa/laterales o cubierta posterior en rojo T1 #DA3B2B, pantalla frontal negra vacia y teclado fisico integrado. No copiar logos, UI ni texto de referencia.
- Orientacion: rectangulo horizontal OESTE-ESTE sobre la profundidad del counter, no vertical norte-sur.
- Direccion: pantalla a la izquierda/OESTE y botones a la derecha/ESTE; el frente de uso completo mira hacia ESTE, hacia la pared derecha vacia y el pasillo vendedor. No mira hacia pasillo central, entrada ni cliente.
- Botones: formas vacias sin numeros legibles, sin marcas, sin simbolos de pago y sin UI.
- Tamano: escala handheld compacta, no tablet grande, no pantalla en pedestal.
Resumen de orden sur-norte sobre la barra larga:
pluma -> libreta -> pano rojo -> terminal punto de venta.
No incluir a Don Rafael. No incluir monitos, siluetas, puntos de personaje ni recorrido de personaje.

ESTRUCTURA DEL PLANO:
La calle queda abajo.
El fondo del local queda arriba.
La entrada estrecha y cortina metalica quedan abajo.
Los anaqueles/vitrinas altos, anchos y continuos van pegados a pared izquierda y fondo. La pared derecha queda libre de anaqueles.
La mercancia visible debe ser minima o apenas sugerida, sin logos legibles y sin llenar los compartimentos. El mapa debe mostrar la ubicacion de muebles y circulacion, no una lista de objetos.
El pasillo central queda libre desde entrada hasta fondo.
La caja lateral derecha queda cerca de la entrada o a media profundidad, con forma de L.
La caja no es isla central.
La caja no bloquea el pasillo central.
La barra larga esta separada de la pared derecha por un pasillo vendedor claro.
El brazo corto de la L queda hacia la entrada, cierra el frente de la caja y llega hasta la pared derecha.
La barra larga y el brazo corto tienen exactamente la misma altura y la misma cubierta superior continua. No hay segundo nivel, escalon, banca, base baja, plataforma ni bloque inferior.
No debe existir acceso a la caja desde la entrada.
La L queda abierta en su extremo posterior hacia el fondo del local, como espacio libre de paso para el vendedor. No dibujar puerta ni convertir el mostrador en forma de C.
El fondo no tiene puerta visible. El fondo debe resolverse como anaquel/vitrina continuo, limpio y casi vacio.
Los props de caja quedan sobre la barra larga, en orden sur a norte: pluma, libreta, pano rojo, terminal punto de venta. No poner los props principales sobre el brazo corto salvo papeles secundarios pequenos.
La terminal punto de venta sigue la misma orientacion general: rectangulo horizontal OESTE-ESTE, pantalla a la izquierda/OESTE y botones a la derecha/ESTE; el frente de uso mira hacia la pared derecha, no hacia entrada, cliente ni pasillo central.

PERSONAJE:
No mostrar personaje. No mostrar monito de Don Rafael. No mostrar siluetas humanas. No mostrar puntos de recorrido.

CAMARAS:
No mostrar camaras. No mostrar conos de vision. No mostrar flechas de camara. Las camaras se definiran despues en el location sheet y en el storyboard.

LUZ:
No mostrar flechas de luz. La luz se definira despues en el location sheet. La planta solo debe fijar arquitectura.

LOOK DEL MAPA:
Tecnico, minimalista, preciso, clean architectural floor plan, top-view-only store floor plan, thin furniture lines, thicker wall lines, grayscale only. Mobiliario claro y simplificado, casi sin mercancia dibujada.

NEGATIVO:
no cinematic final frame, no realistic photo scene, no colorful render, no isometric game map, no character portrait, no detailed person, no full body person, no realistic Don Rafael, no person icon, no human silhouette, no people crowd, no route dots, no character path, no red route, no arrows, no camera icons, no camera cones, no light cones, no yellow cones, no moodboard, no collage, no storyboard panels, no facade view, no elevation drawing, no side view, no section drawing, no isometric view, no perspective view, no 3D cutaway, no thumbnails, no secondary panels, no multi-view architecture board, no central island counter, no C-shaped counter, no stepped counter, no two-level counter, no double-height counter, no split-level cashier counter, no lower short arm, no bench-like counter arm, no platform counter, no pedestal block, no counter door, no counter gate, no formal doorway behind counter, no boutique showroom island, no gourmet store island, no luxury retail layout, no open concept showroom, no counter blocking central aisle, no long bar fully attached to right wall with no seller space, no access to counter from entrance, no front opening in counter, no blocked access behind counter, no right wall fully occupied by shelves in the counter area, no terminal point of sale facing customer aisle, no laptop, no computer, no tablet, no monitor, no keyboard, no arbitrary cameras, no camera axis crossing, no messy diagram, no clutter, no overloaded shelves, no tiny-object overload, no every shelf fully packed, no detailed inventory, no product catalog, no excessive text, no captions, no labels, no numbers if avoidable, no UI, no metadata, no logo, no brand, no soccer, no football, no ball, no stadium, no flags, no famous landmarks, no dirty shop, no grime, no trash, no rust, no peeling paint, no abandoned look, no confusing camera positions, no crossed camera axis, no reversed shop layout.
```

## 02 — Prompt Para Crear Location Sheet Visual L01 Desde Mapa

Usar con el blocking map aprobado como unica imagen de referencia.

Blocking map aprobado:
`07_assets/locations/blocking-maps/L_Tienda-pequena-centro-historico-blocking-map.png`

```text
Haz una imagen horizontal 16:9 de location sheet visual cinematografico para una tienda pequena tradicional del Centro Historico de Ciudad de Mexico, zona Donceles/Zocalo.

Usa la imagen adjunta del plano de planta como referencia estricta y unica.
La imagen final debe traducir ese mapa a una ficha visual cinematografica de la misma tienda.
No inventes otra planta.
No cambies la posicion de entrada, cortina, anaqueles, pasillo central, caja lateral en L, pasillo vendedor ni fondo.
El mapa manda sobre cualquier descripcion escrita si hubiera duda.
La prioridad absoluta es que cada panel respete la geometria del mapa. Si la imagen se ve bonita pero cambia la planta, el resultado es incorrecto.
La pared derecha debe permanecer limpia, sin anaquel corrido, porque esa zona pertenece a caja en L y pasillo vendedor.
La caja debe leerse como caja lateral en L en los paneles interiores y de entrada. No convertirla en barra recta, isla, mostrador boutique, mostrador central ni mueble rectangular largo.
El brazo corto de la L hacia la entrada debe verse en planos amplios/interiores para que se entienda que no hay acceso frontal a la caja.
Toda la caja en L debe leerse como un solo mueble continuo de mostrador, con la misma altura en la barra larga y en el brazo corto. La cubierta superior debe estar al mismo nivel en toda la L. No hay desnivel, escalon, banca, plataforma, pedestal, doble nivel ni modulo mas bajo.

La tienda debe sentirse como comercio real de toda la vida: humilde, honesto, funcional, bien barrido, cuidado y recientemente mantenido.
No debe sentirse lujosa, boutique, showroom, gourmet ni retail caro.
Tradicional no significa antiguo ni deteriorado: el mobiliario debe verse actual, limpio, sencillo y bien mantenido. Los anaqueles deben ser anchos y legibles, tipo vitrina sencilla con vidrio limpio y estructura de madera clara o media. No deben parecer muebles viejos de madera oscura ni anticuario.

Fachada:
Fachada de piedra volcanica rojiza tipo tezontle o cantera rojiza del Centro Historico, limpia y bien mantenida, combinada con marco claro de cantera o pintura neutra.
La cortina metalica debe ser de color rojo T1 #DA3B2B, muy sobrio e integrado naturalmente al local.
Debe tener un rotulo comercial antiguo colocado arriba de la cortina o sobre el marco superior.
Texto exacto del rotulo: "LA NACIONAL".
El rotulo debe verse en los paneles exteriores: sobrio, pintado a mano o en azulejo/esmalte, artesanal, local y digno.
No usar tipografia digital moderna, no neon, no lona publicitaria contemporanea, no branding corporativo, no logos, no marcas reales, no publicidad.

Mercancia:
La tienda vende articulos para cabello, barba y cuidado personal: peines, cepillos, brochas, navajas, tijeras, maquinas de corte, pomadas, geles, ceras, tintes, ligas, pasadores y accesorios pequenos. Los productos deben verse reales, humildes, ordenados y sin marcas legibles.
Importante: la mercancia debe ser minimal y aireada. No llenar todos los anaqueles. Usar pocos grupos de producto bien acomodados, con espacios vacios visibles entre objetos. Priorizar claridad visual sobre cantidad de objetos.
Evitar que los productos pequenos se vuelvan ruido visual. Mostrar familias de producto reconocibles, no cientos de objetos miniatura.
Incluir pocos peines, cepillos, brochas, navajas, tijeras, pomadas, geles y maquinas de corte como grupos reconocibles y espaciados. Los anaqueles, mostrador, piso y fachada deben verse limpios, recientes y cuidados.

OBJETIVO:
Crear una ficha visual de locacion, no un storyboard.
La imagen debe fijar look, arquitectura, materiales, luz, limpieza, paleta y continuidad visual de la tienda basada en el mapa.

FORMATO:
- Una sola imagen horizontal 16:9.
- Location sheet visual de produccion, limpio y cinematografico.
- Grilla limpia, ordenada y visual, estrictamente regular.
- Todos los thumbnails/paneles deben tener exactamente las mismas dimensiones, misma proporcion horizontal, mismo margen exterior y misma separacion interna.
- Sin titulos, captions, labels, logos ni marcas de agua. Unico texto permitido: rotulo tradicional de fachada con texto exacto "LA NACIONAL".
- No collage irregular. No paneles grandes mezclados con paneles pequenos. No mosaico libre. No variar tamanos de thumbnails.
- Paneles cinematograficos limpios, no catalogo de productos.

ESTRUCTURA SUGERIDA:
Crear una grilla estricta de 4 columnas por 4 filas, 16 paneles totales.
Los 16 paneles deben ser thumbnails horizontales identicos en tamano y proporcion. Ningun panel debe ocupar doble ancho, doble alto, ni romper la reticula.
Cada thumbnail debe tener el mismo ancho, el mismo alto, el mismo borde/margen y la misma separacion con los demas thumbnails.
Todos los paneles deben parecer stills cinematograficos horizontales de la misma tienda.
No dejar paneles vacios.

Asignacion obligatoria de vistas por panel:
Panel 1: fachada exterior en plano amplio diagonal de calle al amanecer, cortina cerrada, rotulo "LA NACIONAL" visible, sin personas.
Panel 2: fachada exterior frontal simetrica, cortina cerrada roja T1, marco de cantera/tezontle limpio, rotulo "LA NACIONAL" visible.
Panel 3: fachada frontal con cortina abierta o a media altura, vista desde calle hacia interior, revelando pasillo central, anaquel izquierdo, fondo y caja lateral derecha en L.
Panel 4: detalle exterior del rotulo "LA NACIONAL" y cortina roja T1, material de fachada limpio, amanecer consistente.

Panel 5: vista desde la calle/umbral hacia interior, con entrada completa, pasillo central libre, anaquel izquierdo, anaquel de fondo, pared derecha limpia y caja en L; debe verse el brazo corto cerrando hacia la entrada.
Panel 6: vista interior desde la entrada hacia fondo, ligeramente cargada al lado izquierdo para leer anaqueles de pared izquierda y profundidad del local.
Panel 7: vista interior desde entrada hacia fondo, ligeramente cargada al lado derecho para leer pared derecha limpia, barra larga separada del muro y pasillo vendedor estrecho.
Panel 8: vista interior tres cuartos desde pasillo central hacia la caja en L, mostrando barra larga norte-sur, brazo corto sur/frente y cubierta continua de la misma altura.

Panel 9: vista interior amplia desde entrada hacia fondo, con pasillo central libre y anaquel de fondo visible; repetir la misma geometria del mapa, sin cambiar caja ni anaqueles.
Panel 10: vista interior desde pasillo central junto al anaquel izquierdo, mirando hacia fondo y caja; debe sentirse local angosto y profundo.
Panel 11: vista interior hacia la barra larga desde el pasillo central, mostrando props sobre la barra en orden sur/frente a norte/fondo: pluma, libreta, pano rojo, terminal punto de venta.
Panel 12: vista cercana superior/diagonal de la barra larga y brazo corto de la L, mostrando que toda la cubierta del mostrador esta al mismo nivel, sin escalon ni modulo bajo.

Panel 13: detalle de vitrina/anaquel izquierdo con pocos productos de cabello/barba/cuidado personal, ordenados, con espacios vacios y sin marcas legibles.
Panel 14: detalle de otra seccion del anaquel izquierdo o anaquel de fondo, con peines, cepillos, brochas, pomadas, navajas o maquinas de corte, sin saturacion.
Panel 15: detalle de props sobre la barra larga: pluma, libreta, pano rojo y terminal punto de venta en el orden correcto; terminal horizontal OESTE-ESTE, pantalla a la izquierda/OESTE y botones a la derecha/ESTE, frente de uso hacia pared derecha.
Panel 16: detalle del anaquel de fondo o textura de materiales interiores: madera clara/media, vidrio limpio, piso impecable, luz dorada consistente y mercancia espaciada.

Todos los paneles deben mantener la misma planta, misma iluminacion, misma paleta, misma fachada, mismo mobiliario, misma mercancia y misma continuidad espacial. La primera fila debe conservar el caracter de fachada aprobada: comercio tradicional digno, tezontle/cantera rojiza, cortina roja T1, rotulo exacto "LA NACIONAL".

GEOMETRIA OBLIGATORIA:
Entrada y cortina metalica al frente, en la calle.
Interior rectangular, angosto y profundo.
Anaqueles altos, anchos y profundos en pared izquierda y fondo, tipo vitrina sencilla con vidrio limpio y estructura de madera clara o media. No debe haber anaquel en pared derecha.
Anaquel o producto ordenado al fondo con articulos de cabello, barba y cuidado personal, colocado en grupos simples con espacios vacios visibles.
Pasillo central libre desde entrada hacia fondo.
Mostrador lateral derecho tipo caja, con forma de L, no isla central.
La barra larga corre paralela al eje largo del local y queda separada de la pared derecha para formar un pasillo vendedor estrecho.
El brazo corto de la L queda hacia la entrada, cierra el frente de la caja y llega hasta la pared derecha.
No debe haber acceso directo a la caja desde la entrada.
El mostrador no es una isla: solo la barra larga queda separada del muro; el brazo corto cierra contra la pared derecha.
El paso al pasillo vendedor ocurre por el extremo posterior abierto de la L, hacia el fondo del local, no por el frente. No dibujar puerta ni vano.
La caja no debe convertirse en mostrador rectangular simple ni barra lineal. Debe mantener dos brazos: barra larga norte-sur y brazo corto sur/frente conectado hacia pared derecha.
La barra larga y el brazo corto tienen exactamente la misma altura, el mismo espesor visual de tapa y una sola cubierta continua. El brazo corto no es banca, no es escalon, no es plataforma, no es pedestal y no es modulo bajo.
En vistas desde la entrada, debe verse el pasillo central libre a la izquierda de la caja y el pasillo vendedor estrecho al lado derecho/detras de la barra larga.
Los props fijos de caja deben respetar el mapa: sobre la barra larga, de sur/frente a norte/fondo van pluma, libreta, pano rojo, terminal punto de venta.
La terminal punto de venta debe mirar hacia la pared derecha vacia / este. No mira hacia el pasillo central, la entrada ni el cliente.
Terminal punto de venta: objeto compacto tipo handheld con la forma fisica de la referencia: cuerpo blanco, carcasa/laterales o cubierta posterior en rojo T1 #DA3B2B, pantalla frontal negra vacia y teclado fisico integrado. En planta debe leerse como rectangulo horizontal OESTE-ESTE sobre la profundidad del mostrador, no como rectangulo vertical norte-sur. Pantalla a la izquierda/OESTE, botones a la derecha/ESTE; el frente de uso completo mira hacia el este/pared derecha. No copiar logos, UI ni texto de referencia. No mostrar numeros, marcas, simbolos de pago ni UI.

DISPOSICION OBLIGATORIA DE ELEMENTOS SOBRE LA BARRA:
La barra larga corre de SUR/frente a NORTE/fondo. Todos los elementos principales van sobre esa barra larga, no sobre el brazo corto de la L. El orden es fijo y exacto: 1 pluma, 2 libreta, 3 pano rojo, 4 terminal punto de venta.

1. Pluma:
- Posicion: extremo SUR/frente de la barra larga, cerca del brazo corto/base de la L.
- Orientacion: horizontal de oeste a este sobre la profundidad del mostrador.
- Boton/capuchon/clip rojo hacia OESTE / pasillo central.
- Punta de escritura hacia ESTE / pared derecha / pasillo vendedor.
- Sin texto, sin marca, sin logo.

2. Libreta:
- Posicion: inmediatamente al NORTE de la pluma, aun en zona SUR/frente de la barra larga.
- Forma: libreta pequena cerrada, limpia, sin texto visible.
- Orientacion: alineada con el eje de la barra o ligeramente vertical norte-sur.
- No generar escritura, numeros, notas ni etiquetas.

3. Pano rojo:
- Posicion: inmediatamente al NORTE de la libreta, antes de la terminal punto de venta.
- Forma: pano rojo T1 doblado, pequeno, como acento de color.
- Orientacion: levemente diagonal, siempre sobre la barra larga y sin invadir el brazo corto/base.
- Sin logo, sin texto, sin patron.

4. Terminal punto de venta:
- Posicion: zona MEDIA/NORTE de la barra larga, al NORTE del pano rojo; despues de la terminal queda superficie libre de mostrador hacia el fondo.
- Forma: terminal punto de venta generica tipo handheld con la forma fisica de la referencia: cuerpo blanco, carcasa/laterales o cubierta posterior en rojo T1 #DA3B2B, pantalla frontal negra vacia y teclado fisico integrado. No copiar logos, UI ni texto de referencia.
- Orientacion: rectangulo horizontal OESTE-ESTE sobre la profundidad del mostrador, no vertical norte-sur.
- Direccion: pantalla a la izquierda/OESTE y botones a la derecha/ESTE; el frente de uso completo mira hacia ESTE, hacia la pared derecha vacia y el pasillo vendedor. No mira hacia pasillo central, entrada ni cliente.
- Botones: formas vacias sin numeros legibles, sin marcas, sin simbolos de pago y sin UI.
- Tamano: escala handheld compacta, no tablet grande, no pantalla en pedestal.

No agregar computadora, laptop, tablet, monitor ni teclado sobre el mostrador.
Luz de amanecer entra desde la calle hacia el interior.
La iluminacion debe ser la misma en los 16 paneles: misma hora de amanecer, misma direccion de luz desde sur/calle hacia norte/fondo, misma temperatura dorada suave, misma exposicion, mismo contraste y misma calidad de sombra. No cambiar a mediodia, tarde, noche, luz artificial dominante ni HDR.

CONTINUIDAD OBLIGATORIA:
Misma tienda en todos los paneles.
Misma fachada.
Misma cortina metalica.
Mismo mostrador en L.
Mismo anaquel izquierdo y mismo anaquel de fondo con la misma mercancia de cabello/barba, siempre ordenada y poco saturada.
Misma iluminacion en todos los paneles: amanecer suave, luz dorada desde la calle/sur hacia el interior/norte, misma direccion, misma intensidad, misma temperatura de color, misma exposicion y mismo contraste.
Misma paleta.
Mismo estado limpio, cuidado, humilde, digno y funcional.
Mismo estado nuevo, ordenado y recientemente mantenido.
Misma planta del mapa en todos los paneles.
Mismas posiciones relativas: entrada al frente, anaquel izquierdo, anaquel de fondo, pared derecha limpia, pasillo central libre, mostrador en L dentro del local, brazo corto de la L cerrando hacia entrada, pasillo vendedor detras de caja.
Misma altura continua del mostrador en L: barra larga y brazo corto al mismo nivel, sin escalon, sin banca, sin plataforma y sin modulo bajo.
Misma orientacion de terminal punto de venta: rectangulo horizontal OESTE-ESTE, pantalla a la izquierda/OESTE y botones a la derecha/ESTE; frente de uso hacia pared derecha vacia, no hacia pasillo central, entrada ni cliente.
Misma disposicion de props sobre la barra larga: desde sur/frente hacia norte/fondo, pluma, libreta, pano rojo, terminal punto de venta.
Las vistas deben respetar la geometria del mapa.

LOOK:
Cine independiente mexicano contemporaneo. Sobrio, humano, cercano, honesto y digno. Fotografia suave, contraste medio, negros ligeramente levantados, altas luces con roll-off analogico, grano fino cinematografico. Luz dorada de amanecer. Textura real de metal limpio, concreto cuidado, madera sencilla clara o media, anaqueles/vitrinas de vidrio limpio, laminado limpio y productos de cabello/barba ordenados con aire visual. El local debe sentirse tradicional por escala, oficio y fachada, no por mobiliario viejo.

ESTADO DEL MUNDO:
Todo debe verse limpio, cuidado, recientemente mantenido y en excelente estado. Realismo si, suciedad no. Textura si, deterioro no.
Fachada limpia, posible tezontle rojizo o cantera rojiza cuidada, marco de cantera clara o pintura neutra uniforme, cortina metalica limpia y pareja, rojo T1 sobrio, sin oxido, sin abolladuras, sin manchas, sin graffiti, sin polvo pesado, sin humedad, sin pintura descarapelada.
Interior impecable pero sencillo: piso limpio, anaqueles actuales, anchos, de vidrio con madera clara/media, bien mantenidos, ordenados y no saturados, mercancia de cabello/barba bien acomodada en pocos grupos, madera cuidada pero no lujosa, vidrio limpio, cero cables visibles, cero acumulacion, cero cajas viejas, cero deterioro.
La tienda es humilde, tradicional y pequena; debe sentirse funcional, luminosa, digna, bien atendida y en operacion.

ROJO T1:
Usar rojo T1 #DA3B2B solo en cortina metalica, pano rojo y carcasa/acento de la terminal punto de venta. No generar logo. El unico texto permitido es el rotulo tradicional de fachada con texto exacto "LA NACIONAL".

NEGATIVO:
no people, no character, no storyboard action, no moodboard, no irregular collage, no product catalog, no text except "LA NACIONAL" on facade sign, no titles, no captions, no labels, no watermarks, no logos, no brands, no UI, no QR, no luxury boutique, no showroom, no gourmet store, no antique store, no dirty shop, no grime, no trash, no rust, no peeling paint, no graffiti, no clutter, no overloaded shelves, no fully packed shelves, no right wall shelf, no terminal point of sale facing customer aisle, no laptop, no computer, no tablet, no monitor, no keyboard, no straight counter, no linear bar counter, no simple rectangular counter, no missing short arm of the L counter, no stepped counter, no two-level counter, no double-height counter, no split-level cashier counter, no lower short arm, no bench-like counter arm, no platform counter, no pedestal block, no counter opening toward entrance, no access to counter from entrance, no reversed layout, no night scene, no harsh HDR, no stock photo look.
```

## 03 — Formula Para El Story Y Sequence Board Posterior

Usar en una ventana nueva y limpia cuando ya esten aprobados:

1. Character sheet de Don Rafael.
2. Blocking map aprobado: `07_assets/locations/blocking-maps/L_Tienda-pequena-centro-historico-blocking-map.png`
3. Location sheet visual L01 aprobado vigente.

```text
Usa las 3 imagenes adjuntas como referencias estrictas:

1. Character sheet aprobado de Don Rafael:
Identidad, rostro, edad, pelo entrecano, complexion, manos, vestuario, actitud y props personales.

2. Blocking map aprobado de L01:
Planta fija, entrada y cortina al sur, interior al norte, anaquel izquierdo, anaquel de fondo, pared derecha limpia, pasillo central, caja lateral derecha en L, pasillo vendedor, props fijos y continuidad espacial.

3. Location sheet visual aprobado de L01:
Arquitectura, fachada de tezontle/cantera rojiza, cortina roja T1, mostrador en L, anaqueles con articulos de cabello/barba, materiales, paleta, luz de amanecer, limpieza y tono cinematografico.

JERARQUIA DE REFERENCIAS:
La identidad del personaje viene solo de la referencia 1.
La geometria y continuidad espacial vienen solo de la referencia 2.
El look, arquitectura y materiales vienen solo de la referencia 3.

No uses ninguna otra imagen como referencia.
No inventes otra tienda.
No cambies el layout.
No cruces eje.
No cambies al personaje.
No cambies ropa, edad, rostro, luz, paleta ni epoca.
```

## 04 — Prompt Para Toma 01 Con Don Rafael En L01

Usar en chat nuevo. Adjuntar exactamente estas referencias:

1. Character sheet aprobado de Don Rafael.
2. Blocking map aprobado: `07_assets/locations/blocking-maps/L_Tienda-pequena-centro-historico-blocking-map.png`
3. Location sheet visual aprobado de L01 vigente.

```text
Haz una imagen horizontal 16:9 tipo sequence sheet cinematografico para la Toma 01 de una tienda pequena tradicional del Centro Historico de Ciudad de Mexico.

Usa las 3 imagenes adjuntas como referencias estrictas y unicas:

1. Character sheet de Don Rafael:
Usalo solo para identidad del personaje: rostro, edad, pelo entrecano, complexion, manos, vestuario, actitud y presencia.

2. Blocking map de la tienda:
Usalo solo para geometria y continuidad espacial: entrada/cortina al frente, local angosto y profundo, anaquel izquierdo, anaquel de fondo, pared derecha limpia, pasillo central, caja lateral derecha en L, pasillo vendedor, fondo, direccion de entrada desde la calle hacia el interior, props fijos de caja y orientacion de terminal punto de venta hacia la pared derecha.

3. Location sheet visual de la tienda:
Usalo solo para look de locacion: fachada de tezontle/cantera rojiza, cortina metalica roja T1, interior limpio, anaqueles con articulos de cabello/barba, mostrador en L de madera, props sobre barra larga en orden pluma, libreta, pano rojo y terminal punto de venta tipo handheld blanca con carcasa/acento rojo T1, luz de amanecer, paleta y tono cinematografico.
La fachada, la luz y el caracter visual deben conservar el look del location sheet aprobado. La secuencia puede cambiar la accion, pero no debe cambiar la fachada, el rotulo, la paleta, el local ni la geometria.

CONTINUIDAD DE CALLE / EXTERIOR:
La calle exterior debe ser siempre la misma calle del Centro Historico. Mantener la misma banqueta, mismo empedrado o pavimento, mismos bolardos si aparecen, misma linea de fachadas, misma direccion del sol bajo de amanecer y mismo eje de calle.
La tienda siempre esta en la misma acera y misma fachada. No mover la tienda a otra esquina, no cambiar el lado de la calle, no invertir la direccion de la calle, no cambiar el fondo urbano.
Los planos exteriores pueden alternar entre frontal, tres cuartos y detalle, pero deben sentirse filmados desde posiciones coherentes alrededor del mismo acceso, sin saltar a una calle distinta.

No uses ninguna otra imagen como referencia.
No inventes otra tienda.
No cambies el layout.
No cambies a Don Rafael.
No cambies ropa, edad, rostro, luz, paleta ni epoca.

OBJETIVO:
Crear un sequence sheet de la primera toma: Don Rafael llega muy temprano, cuando apenas esta saliendo el sol, abre la cortina metalica roja de su tienda, respira mirando la calle y la primera luz del dia, entra al local y llega a la barra para revisar datos en su libreta.
La imagen debe servir para fijar continuidad de personaje, locacion, accion, direccion de luz y progresion de la toma.
La tienda vende articulos de cabello, barba y cuidado personal; si se revela el interior, deben verse peines, cepillos, brochas, navajas, tijeras, pomadas, geles, ceras, tintes, ligas, pasadores y accesorios pequenos sin marcas legibles.

FORMATO:
- Una sola imagen horizontal 16:9.
- Grilla limpia de 4 columnas por 4 filas, 16 paneles totales.
- Los 16 paneles deben tener exactamente el mismo tamano, misma proporcion horizontal, mismo margen y misma separacion interna.
- Todos los paneles deben parecer stills cinematograficos de la misma toma.
- Sin texto, sin numeros, sin titulos, sin captions, sin labels, sin logos, sin marcas de agua.
- No dejar paneles vacios.
- No hacer collage irregular. No paneles grandes mezclados con paneles pequenos. No mosaico libre.

ACCION DE LA TOMA 01:
Panel 01: fachada cerrada muy temprano, amanecer apenas naciendo, calle tranquila casi vacia, cortina metalica roja abajo, rotulo tradicional sobrio "LA NACIONAL".
Panel 02: Don Rafael entra a cuadro desde la misma banqueta de la misma calle, caminando hacia su cortina con calma de rutina diaria. Mantener el mismo eje exterior del panel 01.
Panel 03: Don Rafael se detiene frente a la cortina, de espalda o tres cuartos, mirando su tienda cerrada. La fachada y calle siguen siendo la misma ubicacion.
Panel 04: baja las manos hacia la barra inferior de la cortina.
Panel 05: toma la cortina desde abajo con ambas manos.
Panel 06: empieza a levantarla; aparece una primera franja baja de luz dorada entrando desde la calle.
Panel 07: la cortina sube con peso real, verticalmente; se insinua el interior limpio.
Panel 08: Don Rafael sigue levantando la cortina con movimiento lento, natural y pesado.
Panel 09: la cortina queda abierta o a media altura suficiente; se revela el pasillo central, anaquel izquierdo, anaquel de fondo, pared derecha limpia y caja lateral derecha en L segun el mapa. Debe verse o insinuarse el brazo corto de la L cerrando hacia la entrada.
Panel 10: Don Rafael baja las manos y queda en el umbral, todavia cerca de la entrada.
Panel 11: Don Rafael gira ligeramente hacia la calle y la luz del amanecer.
Panel 12: momento de respiracion: Don Rafael mira la calle/sol naciente con gesto tranquilo, como diciendo sin texto "empieza un nuevo dia".
Panel 13: Don Rafael se da la media vuelta hacia el interior de la tienda.
Panel 14: cruza el umbral y avanza de sur/frente a norte/fondo por el pasillo central libre, pasando junto al anaquel izquierdo. No se mete a la caja por el frente.
Panel 15: llega al extremo posterior/norte abierto de la caja en L y entra al pasillo vendedor desde ahi, sin abrir puerta, sin pasar por el frente de la caja. La caja debe verse como L, con brazo corto al sur/frente y barra larga norte-sur separada de la pared derecha.
Panel 16: Don Rafael queda junto a la barra larga y revisa datos en la libreta pequena. Mantener visibles, si el encuadre lo permite, pluma, libreta, pano rojo y terminal punto de venta en el orden correcto del mapa. La terminal debe ser blanca con carcasa/acento rojo T1, no negra, no dataphone generico oscuro.

CONTINUIDAD OBLIGATORIA:
Mismo Don Rafael en todos los paneles.
Misma ropa y misma edad en todos los paneles.
Misma tienda en todos los paneles.
Misma fachada y misma cortina.
Misma calle exterior en todos los paneles exteriores: misma acera, mismo eje de calle, mismo fondo urbano, misma direccion del sol, misma posicion relativa de Don Rafael respecto a la cortina.
Misma direccion de luz de amanecer desde la calle.
Misma iluminacion en todos los paneles: amanecer muy temprano, luz dorada baja desde calle/sur hacia interior/norte, misma temperatura de color, misma exposicion, mismo contraste y misma calidad de sombra.
Misma geometria del mapa: entrada al frente, local angosto y profundo, anaquel izquierdo y anaquel de fondo con articulos de cabello/barba, pared derecha limpia, pasillo central libre, caja lateral derecha en L, pasillo vendedor detras de caja.
La caja lateral derecha debe leerse como L en los paneles interiores donde aparezca: brazo corto al sur/frente cerrando hacia la entrada, barra larga norte-sur separada de pared derecha, pasillo vendedor estrecho detras. No convertirla en barra recta.
Toda la caja en L es un solo mueble continuo con misma altura en barra larga y brazo corto. No escalon, no modulo bajo, no banca, no pedestal.
La mercancia en anaqueles debe verse ordenada y poco saturada: pocos grupos reconocibles, espacios vacios visibles, sin cientos de objetos miniatura.
Mismo color rojo T1 de la cortina abierta o cerrada.
La accion siempre va desde calle hacia entrada, luego hacia el interior y finalmente hacia la barra. No sugerir que Don Rafael viene desde la caja hacia afuera.
Ruta fisica obligatoria: calle / sur -> cortina -> umbral -> pasillo central -> extremo posterior/norte abierto de la L -> pasillo vendedor -> libreta sobre barra larga.
Eje de calle obligatorio: Don Rafael siempre se aproxima por la banqueta frente a la misma fachada; al voltear a ver la calle, mira hacia el mismo eje exterior de amanecer establecido en los primeros paneles. No cambiar a una calle transversal nueva.
No crear acceso frontal a la caja desde la entrada. Don Rafael no debe entrar al pasillo vendedor por el brazo corto/sur de la L; debe acceder por el extremo posterior/norte abierto, como indica el mapa.
Si aparecen props de caja, deben respetar el mapa: sobre la barra larga, de sur/frente a norte/fondo van pluma, libreta, pano rojo, terminal punto de venta.
La terminal punto de venta es tipo handheld, blanca con carcasa/acento rojo T1, pantalla negra vacia y teclado fisico integrado. En planta se lee como rectangulo horizontal OESTE-ESTE: pantalla a la izquierda/OESTE, botones a la derecha/ESTE, frente de uso hacia pared derecha vacia / este. No mira hacia pasillo central, entrada ni cliente. No copiar logos, UI ni texto de referencia. No sustituir por dataphone negro, lector bancario oscuro, telefono, tablet ni pantalla en pedestal.
No agregar computadora, laptop, tablet, monitor ni teclado sobre el mostrador.

LOOK:
Cine independiente mexicano contemporaneo. Sobrio, humano, cercano, honesto y digno. Mood de amanecer muy temprano, apenas saliendo el sol, calle quieta, luz dorada baja y suave entrando desde la calle. Fotografia suave, contraste medio, negros ligeramente levantados, altas luces con roll-off analogico, grano fino cinematografico. Textura real de metal limpio, cantera/tezontle cuidado, concreto cuidado, madera sencilla, vidrio limpio y productos de cabello/barba ordenados.

ESTADO DEL MUNDO:
Todo debe verse limpio, cuidado, recientemente mantenido y en excelente estado.
La tienda es humilde y tradicional, no lujosa. Debe sentirse funcional, luminosa, digna, bien atendida y en operacion.

ROJO T1:
Usar rojo T1 #DA3B2B solo en cortina metalica, pano rojo y carcasa/acento de la terminal punto de venta. No generar logo ni texto.

NEGATIVO:
no text, no numbers, no titles, no captions, no labels, no logos, no brands, no watermark, no UI, no storyboard captions, no random location, no different street, no changing street direction, no moving shop to another corner, no reversed exterior axis, no inconsistent sidewalk, no changed store layout, no different counter position, no central island counter, no straight counter, no linear bar counter, no missing short arm of the L counter, no stepped counter, no two-level counter, no lower short arm, no luxury boutique, no showroom, no gourmet store, no dirty shop, no grime, no trash, no rust, no graffiti, no peeling paint, no poverty look, no abandoned look, no clutter, no overloaded shelves, no fully packed shelves, no hundreds of tiny products, no cables, no night scene, no midday sun, no harsh HDR, no stock photo look, no soccer, no football, no ball, no stadium, no flags, no laptop, no computer, no tablet, no monitor, no keyboard, no black payment terminal, no dark bank card reader, no dataphone negro, no terminal point of sale facing customer aisle, no props changing order, no counter opening toward entrance, no access to counter from entrance, no front counter gate, no formal doorway behind counter, no Don Rafael reaching the bar before opening the shutter, no reversed action, no shutter moving sideways.
```
