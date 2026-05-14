# Krea 34-Shot Spanish Style Compiler Flow

Prompt autocontenido para pedirle al agente de Krea que escale el workflow a 34 tomas, manteniendo todo en espanol y usando el LLM solo como compresor de estilo global.

```text
Quiero escalar el canvas a 34 keyframes cinematograficos 16:9, todo en espanol.

IMPORTANTE:
No ejecutes generadores de imagen todavia.
No uses video, enhance, upscale ni variantes masivas.
Si necesitas volver a correr el LLM de estilo, dime primero el costo estimado y espera mi aprobacion.
No corras los 34 generadores hasta que yo revise la estructura y los prompts finales.

DIAGNOSTICO DEL FLUJO:
La arquitectura correcta NO es que el LLM escriba las 34 tomas.
La arquitectura correcta es:
- El LLM solo comprime la biblia global en un bloque de estilo compacto.
- Cada escena/toma vive en su propio nodo de texto editable, escrito manualmente en espanol.
- Cada PROMPT_FINAL concatena: ESTILO_COMPACTO + ESCENA_XX + NEGATIVO_GLOBAL.
- Cada generador recibe solo su PROMPT_FINAL correspondiente.

No conectes un output viejo del LLM con varias tomas juntas a los generadores.
No metas las 34 tomas dentro de cada generador.
No uses Line Splitter para las tomas en esta version.

OBJETIVO:
Crear un workflow espacialmente limpio, editable y barato de calibrar para 34 keyframes. Primero quiero revisar estructura y prompts; despues correremos solo una tanda pequena de prueba.

ESTRUCTURA VISUAL DEL CANVAS:

COLUMNA 1 - RAIZ / BIBLIA:
- BIBLIA_GLOBAL_ES
- REGLAS_LLM_ESTILO_ES
- NEGATIVO_GLOBAL_ES
- REF_TEXTURA_GLOBAL opcional, sin obligar

COLUMNA 2 - COMPILADOR DE ESTILO:
- LLM_ESTILO_COMPACTO

COLUMNA 3 - ESCENAS MANUALES:
- ESCENA_01
- ESCENA_02
- ESCENA_03
- ...
- ESCENA_34

COLUMNA 4 - PROMPTS FINALES:
- PROMPT_FINAL_01
- PROMPT_FINAL_02
- PROMPT_FINAL_03
- ...
- PROMPT_FINAL_34

COLUMNA 5 - GENERADORES:
- IMAGE_GEN_01
- IMAGE_GEN_02
- IMAGE_GEN_03
- ...
- IMAGE_GEN_34

COLUMNA 6 - KEYFRAMES:
- KEYFRAME_01
- KEYFRAME_02
- KEYFRAME_03
- ...
- KEYFRAME_34

CONEXIONES:
BIBLIA_GLOBAL_ES -> LLM_ESTILO_COMPACTO userPrompt
REGLAS_LLM_ESTILO_ES -> LLM_ESTILO_COMPACTO systemPrompt
LLM_ESTILO_COMPACTO outputText -> todos los PROMPT_FINAL_XX text_0
ESCENA_XX outputText -> PROMPT_FINAL_XX text_1
NEGATIVO_GLOBAL_ES outputText -> PROMPT_FINAL_XX text_2
PROMPT_FINAL_XX outputText -> IMAGE_GEN_XX prompt
IMAGE_GEN_XX outputImage -> KEYFRAME_XX image

Cada PROMPT_FINAL_XX debe contener solo:
1. estilo compacto,
2. la escena de esa toma,
3. negativo global compacto.

Cada PROMPT_FINAL_XX debe quedar debajo del limite de caracteres del nodo. Si alguno se pasa, compacta primero el negativo global y la escena, no elimines la accion principal de la toma.

BIBLIA_GLOBAL_ES:
Look cinematografico 16:9, tono fotografico suave, cine de autor independiente, no publicidad comercial. Roll-off analogico suave, negros levantados, sombras sin aplastar, highlights suaves, grano fino cinematografico. Luz natural primero, luz practica despues. Menos contraste, mas atmosfera, mas silencio visual, realismo tactil, nostalgia contemporanea. Sensacion de lente 35mm/50mm, profundidad de campo media a shallow, composicion limpia y legible, no HDR agresivo, no look stock. Colores: verdes naturales no saturados, amarillos calidos de golden hour, sombras ligeramente frias, acento rojo #DA3B2B donde se especifique. Texturas: metal, piel, tela, carton, fruta, concreto, cesped, polvo y haze. Realismo cinematografico curado: aunque aparezcan contextos populares, comercios pequenos o personas trabajadoras, todo debe sentirse cuidado por direccion de arte, con vestuario seleccionado, paleta controlada, maquillaje natural, escenografia ordenada y textura intencional. Textura real, limpia, mantenida y dignificada; material con uso normal, no decadencia. No pobreza extrema, no abandono, no descuido, no mugre, no grietas profundas, no cicatrices visuales fuertes, no humedad, no oxido pesado, no pintura descascarada, no superficies despintadas, no elementos rotos, cortados, arruinados o derrumbados, no precariedad brutalista, no crudeza documental extrema. Personas de comercio, ciudad, restaurante, espectadores y protagonistas con fisionomias mexicanas/latinoamericanas reales, diversidad natural de tonos de piel, edades, complexiones y rasgos regionales; sin caricatura, exotizacion ni estereotipo. Jugadores del equipo principal tambien mexicanos/latinoamericanos, sin parecer atletas reales. Excepcion: arbitros y equipo contrario blanco/azul no necesitan fisionomia mexicana. Equipo principal ficticio: playera verde con dos lineas blancas, short blanco, calcetas rojas #DA3B2B, sin logos, sin escudos, sin identidad oficial. Equipo contrario ficticio: playera blanca, short azul, calcetas blancas, sin logos. Arbitros: playera verde fosforescente y short negro, sin insignias. Pantallas digitales: smartphones, smartwatch, tablet y laptop muestran superficies digitales genericas y abstractas, bloques abstractos, campos vacios, tarjetas genericas o lineas tacticas, sin UX final, sin texto legible, sin numeros, sin iconos, sin labels, sin codigos QR.

REGLAS_LLM_ESTILO_ES:
Eres un compilador de estilo cinematografico. Extrae de la biblia solo la direccion global de estilo, color, textura, curaduria visual, casting, wardrobe, pantallas digitales genericas y restricciones negativas generales. Devuelve un solo parrafo compacto en espanol, debajo de 900 caracteres. No escribas shots, no bullets, no numeracion, no markdown, no explicaciones. Plain text only.

NEGATIVO_GLOBAL_ES:
sin texto, sin captions, sin subtitulos, sin numeros, sin labels, sin titulos, sin marcas de agua, sin logos, sin marcas comerciales, sin marcas deportivas, sin tres lineas tipo marca, sin uniformes oficiales, sin equipos reales, sin estadios reconocibles, sin nombres de estadios, sin anuncios de patrocinadores, sin balon o tachones de marca, sin atletas reales, sin celebridades, sin figuras publicas, sin landmarks famosos, sin banderas, sin emblemas nacionales, sin aguila, sin mapa politico, sin fronteras, sin pins, sin interfaz satelital, sin UI copiada, sin UX final, sin texto o numeros en pantallas, sin iconos reconocibles, sin QR, sin alcohol, sin simbolos prehispanicos literales, sin glifos arqueologicos, sin look stock, sin HDR, sin piel plastica, sin caras waxy, sin pobreza extrema, sin mugre excesiva, sin abandono, sin descuido, sin decadencia, sin grietas profundas, sin cicatrices visuales fuertes, sin humedad, sin manchas negras, sin oxido pesado, sin pintura descascarada, sin superficies despintadas, sin paredes destruidas, sin elementos rotos, cortados, arruinados o derrumbados, sin precariedad brutalista, sin crudeza documental extrema, sin anatomia deformada, sin manos malformadas, sin artefactos, sin blur cinematografico falso, sin lens flares excesivos

ESCENAS MANUALES:

ESCENA_01:
Cortina metalica de pequena tienda mexicana en centro historico abriendose al amanecer, vista frontal en angulo tres cuartos bajo. Persona mexicana/latinoamericana parcialmente visible en silueta levanta la cortina. Luz dorada entra desde abajo. Metal rayado y gastado como protagonista, atmosfera silenciosa y suspendida.

ESCENA_02:
Futbolista ficticio mexicano/latinoamericano caminando por tunel de estadio. Camara muy baja cerca del suelo, solo piernas, espinilleras y siluetas. Contraluz fuerte al final del tunel. Uniforme verde con dos lineas blancas, short blanco, calcetas rojas #DA3B2B, sin logos. Jersey con textura geometrica abstracta sutil.

ESCENA_03:
Joven mexicano/latinoamericano visto de espaldas ascendiendo escaleras hacia la superficie. Mochila #DA3B2B como protagonista contra entorno neutro. Encuadre medio trasero centrado, escaleras y barandales guian la mirada. Luz natural suave al final, cielo y vegetacion desenfocados, sensacion de progreso.

ESCENA_04:
Jugador ficticio mexicano/latinoamericano ascendiendo del tunel hacia el campo. Encuadre bajo desde atras, foco en piernas y tachones sobre escaleras de concreto. Fondo abre a estadio lleno con multitud desenfocada y contraluz suave. Uniforme verde, short blanco, calcetas rojas #DA3B2B, sin identidad oficial.

ESCENA_05:
Mismo joven mexicano/latinoamericano emergiendo de estacion de metro, subiendo escaleras. Encuadre abierto centrado, rostro nitido como punto emocional, mirada arriba/adelante con determinacion y esperanza. Avenida amplia con gente y autos, puesto de revistas al costado, senalizacion urbana roja generica desenfocada sin texto.

ESCENA_06:
Vendedora mexicana de mercado, unos 45 anos, en puesto de frutas y verduras. Cliente toca terminal generica con smartphone vertical. Manos y terminal como punto de accion. Fondo vivo con familias y personas en mood futbolero usando playeras verdes genericas de dos lineas blancas, todo desenfocado. Sin QR.

ESCENA_07:
Close-up de manos estrechandose entre jugadores antes del partido. Fondo con cuatro arbitros en linea esperando, uniforme verde fosforescente y short negro. Equipo principal verde/blanco/rojo; equipo contrario blanco/azul/blanco, sin logos. Tension previa al silbatazo, manos como punto de union.

ESCENA_08:
Conductora mexicana/latinoamericana vista desde interior del auto, una mano en volante y otra revisando smartwatch con pulsera #DA3B2B. POV desde asiento trasero/medio lado derecho. Trafico denso hacia el horizonte, luces rojas repetidas, avenida amplia tipo CDMX, pausa forzada y friccion urbana.

ESCENA_09:
Mismo encuadre POV pero en cancha. Mano derecha del arbitro revisando smartwatch con pulsera #DA3B2B antes del inicio. Arbitro con playera verde fosforescente y short negro, sin insignias. Fondo desenfocado con jugadores al centro listos para patada inicial.

ESCENA_10:
Pie de futbolista empujando balon hacia adelante. Camara a ras de pasto, balon y zapato en foco, movimiento diagonal, textura de cesped visible, multitud de estadio desenfocada al fondo.

ESCENA_11:
Toma abierta a ras de suelo de jugada entre pies de ambos equipos. Balon corre a ras de pasto con velocidad, piernas cruzan el encuadre. Equipo principal verde/blanco/rojo sin identidad oficial. Fondo de estadio desenfocado, energia de juego en progreso.

ESCENA_12:
Hombre mexicano/latinoamericano cerrando caja de ecommerce en pequena bodega o taller mexicano. Macro de manos, carton y etiqueta generica sin texto. Luz mixta fria funcional con ventana suave. Practico, disciplinado y silencioso.

ESCENA_13:
Delantero ficticio mexicano/latinoamericano ajustando cinta de capitan en medio del campo. Macro de manos y cinta blanca con marca grafica abstracta #DA3B2B sin letra legible. Partido desenfocado al fondo con jugadores corriendo, rima visual con cierre de caja.

ESCENA_14:
Entrenador estudiando tablet desde zona tecnica al borde del campo. Tablet con pantalla digital generica: lineas tacticas abstractas de jugada, sin texto, numeros ni iconos. Smartwatch con correa #DA3B2B. Partido en transcurso desenfocado al fondo.

ESCENA_15:
Mujer mexicana emprendedora revisando laptop en over-the-shoulder shot. Laptop con pantalla digital generica de nodos y bloques abstractos, sin UX final ni texto. Espacio aspiracional pero real, luz natural, plantas, cafe, productos de skincare y maceta #DA3B2B en tercer plano.

ESCENA_16:
Joven vendedor mexicano/latinoamericano de sneakers y accesorios deportivos, unos 24 anos, gestionando ventas en smartphone vertical over-the-shoulder. Pantalla digital generica sin texto. Familia saliendo al fondo, luz calida de tarde, capas de sneakers, playeras, gorras y calle; sneakers #DA3B2B en repisa acrilica.

ESCENA_17:
Manos sosteniendo smartphone vertical en primer plano dentro de tienda de sneakers. Pantalla digital generica con bloques abstractos blanco/rojo, estructura limpia y vacia, sin texto ni iconos. Encuadre over-the-right-shoulder, dedo interactuando con pantalla, fondo desenfocado de la tienda.

ESCENA_18:
Restaurante contemporaneo en CDMX durante partido en vivo. Hombre mexicano/latinoamericano con jersey #DA3B2B mira smartphone vertical, aislado del entorno. Grupo diverso alrededor con jerseys verdes genericos observa fuera de cuadro con tension. Mesa con tacos, totopos, salsas y bebidas sin alcohol.

ESCENA_19:
Arbitro marcando decision con silbato y brazo directo. Gesto firme, mirada concentrada, autoridad. Playera verde fosforescente y short negro sin logos. Fondo de estadio desenfocado con multitud calida, luz uniforme controlada, sensacion de decision irreversible.

ESCENA_20:
Restaurante contemporaneo en CDMX. Protagonista mexicano/latinoamericano con camiseta #DA3B2B sostiene smartphone vertical con ambas manos, pulgares listos. Mirada fija fuera de cuadro hacia partido, postura contenida de sorpresa. Amigos alrededor casi levantandose con tension y asombro.

ESCENA_21:
Jugador ficticio mexicano/latinoamericano colocando balon cuidadosamente sobre cesped. Encuadre a ras de piso con manos, balon y piernas en uniforme verde/blanco/rojo. Pasto protagonista en primer plano, estadio desenfocado, luz calida con leve haze, tension previa a ejecucion.

ESCENA_22:
Manos sosteniendo smartphone vertical sobre mesa con comida mexicana, over-the-right-shoulder. Pantalla digital generica con bloques rojizos abstractos, sin UX ni texto. Tacos, limones y bebidas sin alcohol desenfocados. Luz calida natural/practica, pulgar interactuando, sensacion de control inmediato.

ESCENA_23:
Balon de futbol generico reposando sobre cesped. Encuadre cerrado a ras de piso, balon en foco absoluto, pasto detallado en primer plano. Fondo completamente desenfocado, desgaste leve en balon, composicion centrada, silencio y tension suspendida.

ESCENA_24:
Pie de futbolista haciendo contacto directo con balon. Macro a ras de cesped, foco en zapato y balon, tachones detallados, tierra y particulas suspendidas. Uniforme verde/blanco/rojo visible, fondo desenfocado, instante exacto de impacto y energia liberandose.

ESCENA_25:
Portero en alerta frente a porteria. Encuadre frontal medio de cuerpo completo con ligera compresion. Piernas flexionadas, brazos abiertos listos para reaccion. Uniforme amarillo solido sin identidad, red al fondo, multitud desenfocada, tension sostenida justo al disparo.

ESCENA_26:
Balon suspendido en el aire en pleno vuelo. Encuadre cerrado con balon centrado y aislado, fondo de estadio completamente desenfocado. Profundidad shallow, luz de estadio suave, textura de balon visible, tiempo detenido en punto critico.

ESCENA_27:
Mano de portero extendida interceptando balon en pleno vuelo. Macro con foco en guante y balon en proximidad extrema. Guante con desgaste real, fondo de estadio desenfocado, momento exacto de contacto o milisegundos antes, reflejo y precision.

ESCENA_28:
Balon impactando la red desde angulo lateral extremo, casi dentro de porteria. Encuadre diagonal ligeramente inclinado. Red deformandose alrededor del balon, red y balon en foco, estadio difuso. Geometria dinamica de la red, climax absoluto del gol.

ESCENA_29:
Manos sosteniendo smartphone vertical sobre mesa con comida mexicana. Pantalla digital generica sugiere confirmacion abstracta con composicion centrada y formas simples, sin icono, texto ni numeros. Tacos, limones y bebidas sin alcohol desenfocados, pulgar listo para continuar, logro instantaneo.

ESCENA_30:
Grupo celebrando euforicamente en restaurante durante partido. Protagonista mexicano/latinoamericano con jersey #DA3B2B abrazandose con amigo. Personas alrededor con jerseys verdes genericos reaccionan al mismo tiempo. Mesa con tacos, totopos, salsas y bebidas sin alcohol, liberacion total.

ESCENA_31:
Espectador de espaldas abrazandose con distintas personas en multitud del estadio. Encuadre amplio con siluetas contra luz intensa, confeti en aire, amigos abrazandose, estadio curvo desenfocado, euforia masiva. Fuegos artificiales en cielo sin formas reconocibles.

ESCENA_32:
Vista cenital de estadio con multitud diversa festejando y cubierta de confeti. Gradas iluminadas por destellos de fuegos artificiales, dia volviendose mas oscuro y atmosferico. Realismo magico, surreal pero plausible, composicion amplia inmersiva y no caotica.

ESCENA_33:
Mexico sugerido desde arriba de noche, no como mapa literal. Territorio insinuado poeticamente por constelaciones de luces calidas de negocios, calles y pequenos comercios. Sin fronteras, labels, pines, interfaz satelital ni bandera. Geografia emocional vasta y abstracta.

ESCENA_34:
Frame final minimal casi negro, Tierra vista desde el espacio en composicion sobria con mucho espacio negativo. Mexico se percibe solo como resplandor tenue de luces calidas, sin contorno politico ni mapa literal. Atmosfera silenciosa, escala cosmica, cierre abstracto premium.

AJUSTE DE COSTO:
Antes de gastar mucho, deja todo armado y recomiendame una prueba barata:
- correr o refrescar solo el LLM_ESTILO_COMPACTO si hace falta,
- correr primero 4 generadores de control: 01, 05, 17, 34 o los que sugieras,
- no correr los 34 generadores hasta que apruebe.

REVISION OBLIGATORIA ANTES DE GENERAR:
1. Confirmar que LLM_ESTILO_COMPACTO ya no contiene ninguna escena.
2. Confirmar que cada PROMPT_FINAL_XX contiene solo una escena.
3. Confirmar que ningun prompt final excede el limite de caracteres.
4. Confirmar que todo esta en espanol.
5. Confirmar que no hay texto visible, marcas, equipos reales ni UI final en las imagenes.
```
