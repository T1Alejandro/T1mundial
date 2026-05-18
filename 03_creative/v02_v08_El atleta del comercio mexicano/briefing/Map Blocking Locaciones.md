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

No usar otras imagenes para resolver arquitectura, layout, fachada, interior, ropa o identidad.

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
        │               │ pano/libreta │     │        │
        │               │ POS          │     │        │
        │               │ computadora  │     │        │
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
- La secuencia operativa de props sobre la barra larga sigue el recorrido fisico de Don Rafael, de sur a norte: pano + libreta + pluma -> terminal POS -> computadora.

## Objetos Fijos

- Cortina metalica: al sur, plano frontal del local, se abre verticalmente.
- Entrada / umbral: mismo eje que cortina, conecta calle con pasillo central.
- Mostrador: caja lateral derecha en forma de L. La barra larga corre norte-sur y queda separada de la pared derecha; el brazo corto/base toca o llega a la pared derecha hacia el sur/frente.
- Anaqueles: pared izquierda y fondo, ordenados, sin marcas legibles. No hay anaquel derecho corrido.
- Piso: limpio, continuo, con lineas de perspectiva hacia el fondo.
- Luz principal: amanecer desde la calle, entra desde el sur hacia el norte.
- Props de mostrador: sobre la barra larga de la L, de sur a norte por recorrido fisico: pano rojo + libreta + pluma, luego terminal POS, luego computadora/laptop.
- Orientacion de dispositivos: POS y computadora miran hacia la pared derecha vacia, no hacia el pasillo central ni hacia cliente. Para la computadora, de oeste a este / izquierda a derecha sobre el counter: pantalla -> teclado -> espacio del mueble / pasillo vendedor -> pared derecha.

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
- Los props principales van sobre la barra larga, siguiendo el recorrido fisico sur -> norte: pano + libreta + pluma -> terminal POS -> computadora/laptop.
- POS, computadora o tablet miran hacia la pared derecha vacia; no hacia pasillo central, entrada ni cliente.
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
Hay un mostrador de madera cuidado en el lado derecho, cerca de la entrada o a media profundidad, como caja funcional de tienda tradicional. El mostrador debe tener forma de L, no de C. La barra larga corre paralela al eje largo del local, de sur a norte, y queda separada de la pared derecha para formar un pasillo vendedor estrecho. El brazo corto/base de la L queda hacia el sur/frente, cierra el frente de la caja y toca o llega hasta la pared derecha. No debe haber acceso directo a la caja desde la entrada. No debe ser una isla central. El extremo posterior/norte de la L queda abierto hacia el fondo para que el vendedor pueda pasar detras de la barra; no dibujar puerta, vano, arco ni entrada formal. El pasillo central del cliente debe quedar libre.
Sobre el mostrador deben indicarse props como formas geometricas simples, sin texto: pano rojo + libreta + pluma, terminal POS y computadora/laptop.

DISPOSICION DE PROPS SOBRE LA BARRA LARGA:
Colocar los props principales sobre la barra larga norte-sur de la L, no sobre el brazo corto/base, salvo papeles secundarios pequenos si hicieran falta.
Ordenar los props por recorrido fisico de Don Rafael, no por lectura normal de pagina. Desde SUR/frente hacia NORTE/fondo sobre la barra larga:
1. Posicion sur/frente, cerca del brazo corto/base: pano rojo doblado junto a libreta pequena y pluma con clip rojo.
2. Posicion media: terminal punto de venta / POS generica, compacta, blanca, con pantalla negra vacia y pequeno acento rojo.
3. Posicion norte/fondo: computadora/laptop pequena y limpia, pantalla negra o mate, sin UI, texto ni iconos.

ORIENTACION DE OBJETOS SOBRE EL MOSTRADOR:
Separar posicion de orientacion: aunque los props se ordenan de sur a norte, la orientacion fisica de pluma, POS y computadora se define de oeste a este / izquierda a derecha sobre la profundidad del counter.

Pluma: horizontal sobre la barra. Boton/capuchon/clip rojo hacia el lado visual derecho / oeste; punta de escritura hacia el lado visual izquierdo / este, apuntando hacia laptop y POS. No generar texto en la libreta.

Computadora/laptop: abierta sobre el counter, pero debe mirar hacia la pared derecha vacia, no hacia la entrada ni hacia el pasillo del cliente. Usar este corte estricto de izquierda a derecha / oeste a este sobre el counter:
pantalla/display -> teclado -> espacio libre del counter / pasillo vendedor -> pared derecha.
La pantalla/display queda del lado visual izquierdo / oeste de la laptop, el teclado inmediatamente a su lado visual derecho / este, y la pantalla mira hacia el este / hacia la pared derecha. Desde la entrada o pasillo central debe verse principalmente la parte trasera o canto de la pantalla, no la pantalla viendo al cliente.

Terminal punto de venta / POS: horizontal sobre el counter, en la misma logica de orientacion que la computadora: debe mirar hacia la pared derecha vacia, no hacia pasillo central, entrada ni cliente. Usar este corte estricto de oeste a este / izquierda a derecha sobre el counter:
pantalla/frente/botones -> base mas gruesa / impresora de recibos -> espacio libre del counter / pasillo vendedor -> pared derecha.
La pantalla/frente/botones quedan del lado oeste / visual izquierdo de la terminal, la base mas gruesa o impresora queda inmediatamente hacia el este / visual derecho, y el conjunto mira hacia la pared derecha. Si aparecen botones, deben ser formas vacias sin numeros legibles, sin marcas, sin simbolos de pago, sin UI y sin recibo con texto.

Tamano y lectura: los dispositivos deben ser proporcionales y creibles. La terminal POS debe ser compacta, de escala handheld, no tablet grande ni pantalla en pedestal. La computadora/laptop debe ser pequena, limpia y sin interfaz visible.
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
El brazo corto de la L queda hacia la entrada, cierra el frente de la caja y puede pegar o llegar hasta la pared derecha.
No debe existir acceso a la caja desde la entrada.
La L queda abierta en su extremo posterior hacia el fondo del local, como espacio libre de paso para el vendedor. No dibujar puerta ni convertir el mostrador en forma de C.
El fondo no tiene puerta visible. El fondo debe resolverse como anaquel/vitrina continuo, limpio y casi vacio.
Los props de caja quedan sobre la barra larga, en orden sur a norte: pano + libreta + pluma, terminal POS, computadora/laptop. No poner los props principales sobre el brazo corto salvo papeles secundarios pequenos.
La pantalla de la computadora/laptop mira hacia pared derecha; no mira hacia entrada, cliente ni pasillo central.
La terminal POS sigue la misma orientacion general: pantalla/frente/botones hacia la pared derecha, no hacia entrada, cliente ni pasillo central.

PERSONAJE:
No mostrar personaje. No mostrar monito de Don Rafael. No mostrar siluetas humanas. No mostrar puntos de recorrido.

CAMARAS:
No mostrar camaras. No mostrar conos de vision. No mostrar flechas de camara. Las camaras se definiran despues en el location sheet y en el storyboard.

LUZ:
No mostrar flechas de luz. La luz se definira despues en el location sheet. La planta solo debe fijar arquitectura.

LOOK DEL MAPA:
Tecnico, minimalista, preciso, clean architectural floor plan, top-view-only store floor plan, thin furniture lines, thicker wall lines, grayscale only. Mobiliario claro y simplificado, casi sin mercancia dibujada.

NEGATIVO:
no cinematic final frame, no realistic photo scene, no colorful render, no isometric game map, no character portrait, no detailed person, no full body person, no realistic Don Rafael, no person icon, no human silhouette, no people crowd, no route dots, no character path, no red route, no arrows, no camera icons, no camera cones, no light cones, no yellow cones, no moodboard, no collage, no storyboard panels, no facade view, no elevation drawing, no side view, no section drawing, no isometric view, no perspective view, no 3D cutaway, no thumbnails, no secondary panels, no multi-view architecture board, no central island counter, no C-shaped counter, no counter door, no counter gate, no formal doorway behind counter, no boutique showroom island, no gourmet store island, no luxury retail layout, no open concept showroom, no counter blocking central aisle, no long bar fully attached to right wall with no seller space, no access to counter from entrance, no front opening in counter, no blocked access behind counter, no right wall fully occupied by shelves in the counter area, no POS facing customer aisle, no computer facing central aisle, no tablet facing central aisle, no arbitrary cameras, no camera axis crossing, no messy diagram, no clutter, no overloaded shelves, no tiny-object overload, no every shelf fully packed, no detailed inventory, no product catalog, no excessive text, no captions, no labels, no numbers if avoidable, no UI, no metadata, no logo, no brand, no soccer, no football, no ball, no stadium, no flags, no famous landmarks, no dirty shop, no grime, no trash, no rust, no peeling paint, no abandoned look, no confusing camera positions, no crossed camera axis, no reversed shop layout.
```

## 02 — Prompt Para Crear Location Sheet Visual L01 Desde Mapa

Usar con el blocking map aprobado como unica imagen de referencia.

Blocking map aprobado:
usar el nuevo mapa L01 aprobado generado desde el prompt 01 activo.

```text
Haz una imagen horizontal 16:9 de location sheet visual cinematografico para una tienda pequena tradicional del Centro Historico de Ciudad de Mexico, zona Donceles/Zocalo.

Usa la imagen adjunta del plano de planta como referencia estricta y unica.
La imagen final debe traducir ese mapa a una ficha visual cinematografica de la misma tienda.
No inventes otra planta.
No cambies la posicion de entrada, cortina, anaqueles, pasillo central, caja lateral en L, pasillo vendedor ni fondo.
El mapa manda sobre cualquier descripcion escrita si hubiera duda.
La pared derecha debe permanecer limpia, sin anaquel corrido, porque esa zona pertenece a caja en L y pasillo vendedor.

La tienda debe sentirse como comercio real de toda la vida: humilde, honesto, funcional, bien barrido, cuidado y recientemente mantenido.
No debe sentirse lujosa, boutique, showroom, gourmet ni retail caro.
Tradicional no significa antiguo ni deteriorado: el mobiliario debe verse actual, limpio, sencillo y bien mantenido. Los anaqueles deben ser anchos y legibles, tipo vitrina sencilla con vidrio limpio y estructura de madera clara o media. No deben parecer muebles viejos de madera oscura ni anticuario.

Fachada:
Puede incluir piedra volcanica rojiza tipo tezontle o cantera rojiza del Centro Historico, limpia y bien mantenida, combinada con marco claro de cantera o pintura neutra.
La cortina metalica debe ser de color rojo T1 #DA3B2B, muy sobrio e integrado naturalmente al local.
Sin logo, sin texto, sin marca.

Mercancia:
La tienda vende articulos para cabello, barba y cuidado personal: peines, cepillos, brochas, navajas, tijeras, maquinas de corte, pomadas, geles, ceras, tintes, ligas, pasadores y accesorios pequenos. Los productos deben verse reales, humildes, ordenados y sin marcas legibles.
Importante: la mercancia debe ser minimal y aireada. No llenar todos los anaqueles. Usar pocos grupos de producto bien acomodados, con espacios vacios visibles entre objetos. Priorizar claridad visual sobre cantidad de objetos.
Evitar que los productos pequenos se vuelvan ruido visual. Mostrar familias de producto reconocibles, no cientos de objetos miniatura.
Puede haber algunos peines vintage o herramientas clasicas como acento de producto, pero solo los productos; los anaqueles, mostrador, piso y fachada deben verse limpios, recientes y cuidados.

OBJETIVO:
Crear una ficha visual de locacion, no un storyboard.
La imagen debe fijar look, arquitectura, materiales, luz, limpieza, paleta y continuidad visual de la tienda basada en el mapa.

FORMATO:
- Una sola imagen horizontal 16:9.
- Location sheet visual de produccion, limpio y cinematografico.
- Grilla limpia, ordenada y visual.
- Sin texto, sin numeros, sin titulos, sin captions, sin labels, sin logos, sin marcas de agua.
- No collage irregular.
- Paneles cinematograficos limpios, no catalogo de productos.

ESTRUCTURA SUGERIDA:
Crear una grilla limpia de 4 columnas por 3 filas, 12 paneles totales.
Todos los paneles deben parecer stills cinematograficos horizontales de la misma tienda.
No dejar paneles vacios.

Paneles 1 a 3: fachada exterior y cortina al amanecer, tienda cerrada, sin personas.
Paneles 4 a 6: cortina a media altura o abierta, vista desde calle hacia interior, revelando pasillo central, anaquel izquierdo, anaquel de fondo, pared derecha limpia y caja lateral en L segun el mapa.
Paneles 7 a 9: interior desde entrada hacia fondo, anaquel alto izquierdo, anaquel de fondo, pared derecha limpia, pasillo central libre, caja lateral derecha en L: brazo largo separado del muro, brazo corto cerrando hacia la entrada.
Paneles 10 a 12: detalles limpios y cercanos de materiales y props fijos: metal limpio, madera clara o media del mostrador, piso impecable, anaqueles anchos tipo vitrina sencilla de vidrio limpio con estructura de madera clara o media, pocos peines/cepillos/pomadas/geles/navajas/tijeras/brochas, luz dorada, terminal POS generica orientada hacia la pared derecha vacia, libreta y pano rojo sin texto si aparecen naturalmente. Los detalles deben ser claros, con aire, y no saturados.

GEOMETRIA OBLIGATORIA:
Entrada y cortina metalica al frente, en la calle.
Interior rectangular, angosto y profundo.
Anaqueles altos, anchos y profundos en pared izquierda y fondo, tipo vitrina sencilla con vidrio limpio y estructura de madera clara o media. No debe haber anaquel en pared derecha.
Anaquel o producto ordenado al fondo con articulos de cabello, barba y cuidado personal, colocado en grupos simples con espacios vacios visibles.
Pasillo central libre desde entrada hacia fondo.
Mostrador lateral derecho tipo caja, con forma de L, no isla central.
La barra larga corre paralela al eje largo del local y queda separada de la pared derecha para formar un pasillo vendedor estrecho.
El brazo corto de la L queda hacia la entrada, cierra el frente de la caja y puede pegar o llegar hasta la pared derecha.
No debe haber acceso directo a la caja desde la entrada.
El mostrador no es una isla: solo la barra larga queda separada del muro; el brazo corto puede cerrar contra la pared derecha.
El paso al pasillo vendedor ocurre por el extremo posterior abierto de la L, hacia el fondo del local, no por el frente. No dibujar puerta ni vano.
El POS, computadora o tablet sobre el mostrador debe mirar hacia la pared derecha vacia. No debe mirar hacia el pasillo central, la entrada ni el cliente.
Los props fijos de caja deben respetar el mapa: sobre la barra larga, de sur/frente a norte/fondo van pano rojo + libreta + pluma, luego terminal POS, luego computadora/laptop.
La computadora/laptop debe quedar abierta mirando hacia la pared derecha: pantalla hacia la pared derecha vacia, teclado hacia el interior/pasillo central. Desde la entrada debe verse principalmente la parte trasera o canto de la pantalla, no la pantalla viendo al cliente.
Luz de amanecer entra desde la calle hacia el interior.

CONTINUIDAD OBLIGATORIA:
Misma tienda en todos los paneles.
Misma fachada.
Misma cortina metalica.
Mismo mostrador en L.
Mismo anaquel izquierdo y mismo anaquel de fondo con la misma mercancia de cabello/barba, siempre ordenada y poco saturada.
Misma direccion de luz.
Misma paleta.
Mismo estado limpio, cuidado, humilde, digno y funcional.
Mismo estado nuevo, ordenado y recientemente mantenido.
Misma planta del mapa en todos los paneles.
Mismas posiciones relativas: entrada al frente, anaquel izquierdo, anaquel de fondo, pared derecha limpia, pasillo central libre, mostrador en L dentro del local, brazo corto de la L cerrando hacia entrada, pasillo vendedor detras de caja.
Misma orientacion del POS/computadora/tablet: pantalla hacia la pared derecha vacia, no hacia el pasillo central, entrada ni cliente.
Misma disposicion de props sobre la barra larga: desde sur/frente hacia norte/fondo, pano rojo + libreta + pluma, luego terminal POS, luego computadora/laptop.
Las vistas deben respetar la geometria del mapa.

LOOK:
Cine independiente mexicano contemporaneo. Sobrio, humano, cercano, honesto y digno. Fotografia suave, contraste medio, negros ligeramente levantados, altas luces con roll-off analogico, grano fino cinematografico. Luz dorada de amanecer. Textura real de metal limpio, concreto cuidado, madera sencilla clara o media, anaqueles/vitrinas de vidrio limpio, laminado limpio y productos de cabello/barba ordenados con aire visual. El local debe sentirse tradicional por escala, oficio y fachada, no por mobiliario viejo.

ESTADO DEL MUNDO:
Todo debe verse limpio, cuidado, recientemente mantenido y en excelente estado. Realismo si, suciedad no. Textura si, deterioro no.
Fachada limpia, posible tezontle rojizo o cantera rojiza cuidada, marco de cantera clara o pintura neutra uniforme, cortina metalica limpia y pareja, rojo T1 sobrio, sin oxido, sin abolladuras, sin manchas, sin graffiti, sin polvo pesado, sin humedad, sin pintura descarapelada.
Interior impecable pero sencillo: piso limpio, anaqueles actuales, anchos, de vidrio con madera clara/media, bien mantenidos, ordenados y no saturados, mercancia de cabello/barba bien acomodada en pocos grupos, madera cuidada pero no lujosa, vidrio limpio, cero cables visibles, cero acumulacion, cero cajas viejas, cero deterioro.
La tienda puede ser humilde, tradicional y pequena, pero debe sentirse funcional, luminosa, digna, bien atendida y en operacion.

ROJO T1:
Usar rojo T1 #DA3B2B solo como acento natural. Puede aparecer en pano liso, detalle pequeno, ribete, etiqueta sin texto o cortina metalica sobria si se ve propia del local. No generar logo ni texto.

NEGATIVO:
no people, no character, no storyboard action, no moodboard, no irregular collage, no product catalog, no text, no numbers, no titles, no captions, no labels, no watermarks, no logos, no brands, no UI, no dashboard, no QR, no pharmacy, no supermarket, no grocery store, no liquor store, no luxury boutique, no showroom, no gourmet store, no luxury retail, no expensive marble retail, no designer store, no antique store, no old wooden shelves, no dark antique wood shelving, no thin wire racks, no cheap plastic shelving, no dusty vintage shop, no dirty shop, no grime, no trash, no rust, no peeling paint, no broken wall, no poverty look, no abandoned look, no clutter, no overloaded shelves, no tiny-object overload, no fully packed shelves, no hundreds of tiny products, no cables, no old damaged shutter, no dusty shutter, no dented shutter, no graffiti, no stains, no humidity damage, no cracked floor, no messy shelves, no old boxes, no decayed facade, no inconsistent shop layout, no counter switching sides, no shelves changing position, no right wall shelf, no POS facing customer aisle, no computer facing central aisle, no tablet facing central aisle, no straight counter if the map shows L counter, no counter opening toward entrance, no access to counter from entrance, no reversed layout, no night scene, no harsh HDR, no stock photo look.
```

## 03 — Formula Para El Story Y Sequence Board Posterior

Usar en una ventana nueva y limpia cuando ya esten aprobados:

1. Character sheet de Don Rafael.
2. Blocking map L01: nuevo mapa L01 aprobado generado desde el prompt 01 activo.
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
2. Blocking map aprobado de L01: nuevo mapa L01 aprobado generado desde el prompt 01 activo.
3. Location sheet visual aprobado de L01 vigente.

```text
Haz una imagen horizontal 16:9 tipo sequence sheet cinematografico para la Toma 01 de una tienda pequena tradicional del Centro Historico de Ciudad de Mexico.

Usa las 3 imagenes adjuntas como referencias estrictas y unicas:

1. Character sheet de Don Rafael:
Usalo solo para identidad del personaje: rostro, edad, pelo entrecano, complexion, manos, vestuario, actitud y presencia.

2. Blocking map de la tienda:
Usalo solo para geometria y continuidad espacial: entrada/cortina al frente, local angosto y profundo, anaquel izquierdo, anaquel de fondo, pared derecha limpia, pasillo central, caja lateral derecha en L, pasillo vendedor, fondo, direccion de entrada desde la calle hacia el interior, props fijos de caja y orientacion de POS/computadora hacia la pared derecha.

3. Location sheet visual de la tienda:
Usalo solo para look de locacion: fachada de tezontle/cantera rojiza, cortina metalica roja T1, interior limpio, anaqueles con articulos de cabello/barba, mostrador en L de madera, POS, libreta, pano rojo, luz de amanecer, paleta y tono cinematografico.

No uses ninguna otra imagen como referencia.
No inventes otra tienda.
No cambies el layout.
No cambies a Don Rafael.
No cambies ropa, edad, rostro, luz, paleta ni epoca.

OBJETIVO:
Crear un sequence sheet de la primera toma: Don Rafael llega desde la calle, se aproxima a la cortina metalica de su tienda y empieza a abrirla al amanecer.
La imagen debe servir para fijar continuidad de personaje, locacion, accion, direccion de luz y progresion de la toma.
La tienda vende articulos de cabello, barba y cuidado personal; si se revela el interior, deben verse peines, cepillos, brochas, navajas, tijeras, pomadas, geles, ceras, tintes, ligas, pasadores y accesorios pequenos sin marcas legibles.

FORMATO:
- Una sola imagen horizontal 16:9.
- Grilla limpia de 4 columnas por 4 filas, 16 paneles totales.
- Todos los paneles deben parecer stills cinematograficos de la misma toma.
- Sin texto, sin numeros, sin titulos, sin captions, sin labels, sin logos, sin marcas de agua.
- No dejar paneles vacios.
- No hacer collage irregular.

ACCION DE LA TOMA 01:
Paneles 1 a 4: fachada cerrada al amanecer, cortina metalica abajo, calle tranquila, Don Rafael entra a cuadro desde banqueta.
Paneles 5 a 8: Don Rafael se acerca a la cortina, se detiene frente al acceso, mira el local con calma y prepara las manos.
Paneles 9 a 12: Don Rafael toma la cortina metalica desde abajo y empieza a levantarla. La luz dorada entra suavemente.
Paneles 13 a 16: la cortina queda a media altura, se revela el interior limpio, pasillo central, anaquel izquierdo, anaquel de fondo, pared derecha limpia y caja lateral derecha en L segun el mapa. Don Rafael permanece cerca del umbral; no debe llegar todavia hasta la caja.

CONTINUIDAD OBLIGATORIA:
Mismo Don Rafael en todos los paneles.
Misma ropa y misma edad en todos los paneles.
Misma tienda en todos los paneles.
Misma fachada y misma cortina.
Misma direccion de luz de amanecer desde la calle.
Misma geometria del mapa: entrada al frente, local angosto y profundo, anaquel izquierdo y anaquel de fondo con articulos de cabello/barba, pared derecha limpia, pasillo central libre, caja lateral derecha en L, pasillo vendedor detras de caja.
Mismo color rojo T1 de la cortina si aparece abierta o cerrada.
La accion siempre va desde calle hacia entrada. No sugerir que Don Rafael viene desde la caja hacia afuera.

LOOK:
Cine independiente mexicano contemporaneo. Sobrio, humano, cercano, honesto y digno. Fotografia suave, contraste medio, negros ligeramente levantados, altas luces con roll-off analogico, grano fino cinematografico. Luz dorada de amanecer. Textura real de metal limpio, cantera/tezontle cuidado, concreto cuidado, madera sencilla, vidrio limpio y productos de cabello/barba ordenados.

ESTADO DEL MUNDO:
Todo debe verse limpio, cuidado, recientemente mantenido y en excelente estado.
La tienda es humilde y tradicional, no lujosa. Debe sentirse funcional, luminosa, digna, bien atendida y en operacion.

ROJO T1:
Usar rojo T1 #DA3B2B solo como acento natural si ya aparece en las referencias: pano liso, detalle pequeno o cortina sobria. No generar logo ni texto.

NEGATIVO:
no text, no numbers, no titles, no captions, no labels, no logos, no brands, no watermark, no UI, no storyboard captions, no random location, no changed store layout, no different counter position, no central island counter, no luxury boutique, no showroom, no gourmet store, no dirty shop, no grime, no trash, no rust, no graffiti, no peeling paint, no poverty look, no abandoned look, no clutter, no cables, no night scene, no harsh HDR, no stock photo look, no soccer, no football, no ball, no stadium, no flags.
```
