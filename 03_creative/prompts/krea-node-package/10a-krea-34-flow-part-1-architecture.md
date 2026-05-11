# Krea 34 Shots - Parte 1/4 - Arquitectura y Biblia

Copia y pega esta parte primero en el mismo chat del agente de Krea. No pidas construir todavia; esta parte solo establece arquitectura, reglas y biblia global.

```text
PARTE 1/4 - ARQUITECTURA Y BIBLIA GLOBAL

Voy a enviarte 4 partes en total para construir un workflow de 34 keyframes cinematograficos 16:9 en Krea Nodes.

IMPORTANTE:
No construyas todavia.
No ejecutes ningun generador.
No ejecutes el LLM todavia.
No uses video, enhance, upscale ni variantes masivas.
Espera a recibir PARTE 4/4 antes de proponer el canvas final.

ID DE FLUJO:
KREA_34_ES_STYLE_COMPILER_V1

OBJETIVO:
Armar un workflow espacialmente limpio, editable y barato de calibrar para 34 tomas. Todo debe quedar en espanol. Quiero revisar estructura y prompts antes de generar imagenes.

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

ESTRUCTURA VISUAL DEL CANVAS:

COLUMNA 1 - RAIZ / BIBLIA:
- BIBLIA_GLOBAL_ES
- REGLAS_LLM_ESTILO_ES
- NEGATIVO_GLOBAL_ES
- REF_TEXTURA_GLOBAL opcional, sin obligar

COLUMNA 2 - COMPILADOR DE ESTILO:
- LLM_ESTILO_COMPACTO

COLUMNA 3 - ESCENAS MANUALES:
- ESCENA_01 a ESCENA_34

COLUMNA 4 - PROMPTS FINALES:
- PROMPT_FINAL_01 a PROMPT_FINAL_34

COLUMNA 5 - GENERADORES:
- IMAGE_GEN_01 a IMAGE_GEN_34

COLUMNA 6 - KEYFRAMES:
- KEYFRAME_01 a KEYFRAME_34

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

Espera PARTE 2/4 con escenas 01-12.
```
