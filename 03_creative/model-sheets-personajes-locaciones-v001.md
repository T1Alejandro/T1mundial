---
title: "Model Sheets - Personajes y Locaciones T1 Mundial"
doc_type: "creative-system"
status: "draft"
owner: "Arturo / Parco"
reviewers: ["Creative", "Production", "Legal PI"]
version: "0.1"
last_updated: "2026-05-08"
language: "es"
audience: ["creative", "production", "ai-agent", "figma"]
tags: ["model-sheets", "personajes", "locaciones", "paleta", "figma", "ai-image"]
source_of_truth: "../03_creative/prompts/chatgpt-master-rack-36-v004.md"
confidence: "medium"
related_docs:
  - "../HANDS-UP.md"
  - "../00_admin/prd-claude-code-handoff-v001.md"
  - "../03_creative/prompts/chatgpt-master-rack-36-v004.md"
  - "prompts/model-sheets-master-generation-pack-v001.md"
  - "../04_production/camera-animation-bible-36-v001.md"
  - "../04_production/global-motion-rules-v001.md"
---

# Model Sheets - Personajes y Locaciones T1 Mundial

## 1. Intencion

Crear fichas visuales en español para personajes, locaciones, vestuario, props y paletas del universo T1 Mundial.

Las imagenes de referencia compartidas sirven como estructura: vistas frontal, 3/4, perfil, posterior, close-ups, expresiones, paleta, vestuario, accesorios, entorno y pose cinematografica. La ejecucion final debe verse mas limpia, premium y cinematografica: menos saturada, menos caricatura, menos plantilla generica.

La tipografia sugerida es SF Pro o equivalente minimalista:

- Titulos: SF Pro Display Semibold / Bold.
- Secciones: SF Pro Text Semibold.
- Cuerpo: SF Pro Text Regular.
- Numeros y tokens: SF Mono Regular.

No usar tipografia condensada tipo poster, salvo si se define una version secundaria mas tecnica. La ficha debe sentirse como documento de direccion de arte para cine y AI production, no como ficha escolar ni hoja de personaje fantastico.

## 2. Formato De Ficha

Formato recomendado:

- Lienzo: 16:9 horizontal o A3 horizontal.
- Fondo: blanco calido `#F7F5F0` o gris tecnico `#F5F6F7`.
- Reticula: 12 columnas, margen exterior amplio, divisores finos.
- Lineas divisorias: `#D8D6D0`, 1 px.
- Texto principal: `#1B1B1B`.
- Texto secundario: `#545454`.
- Chips / tokens: swatch cuadrado + nombre + hex.
- Fotografia: realista cinematografica, no ilustracion cartoon.
- Idioma visible: español.

Bloques minimos por ficha de personaje:

1. Ficha de identidad.
2. Identidad y escala: frontal, 3/4, perfil, posterior.
3. Detalle de cabeza: frontal, perfil, 3/4, angulo bajo, angulo dinamico, vista superior.
4. Paleta de colores con hex.
5. Vestuario y accesorios.
6. Props / herramientas.
7. Notas de personaje y continuidad.
8. Pose cinematografica / close-up.
9. Entorno principal.
10. Negativos legales y visuales.

Bloques minimos por ficha de locacion:

1. Identidad de locacion.
2. Planta emocional: que representa en la historia.
3. Vistas: wide, medium, close detail, textura, entrada/salida.
4. Paleta de colores con hex.
5. Materiales y props.
6. Luz y atmosfera.
7. Reglas de continuidad.
8. Riesgos legales / negativos.
9. Plano cinematografico hero.

## 3. Paleta Global Guardada

### 3.1 Brand Red / T1

| Token | Uso | Hex |
|---|---|---|
| `color/brand/red/50` | fondo tenue, UI secundaria | `#FEF4F4` |
| `color/brand/red/100` | tint suave | `#F9D2D2` |
| `color/brand/red/200` | tint medio | `#F1B0A9` |
| `color/brand/red/400` | acento suave | `#E9897E` |
| `color/brand/red/500` | acento vivo | `#E26153` |
| `color/brand/red/600` | rojo T1 final / base de marca | `#DB3B2B` |
| `color/brand/red/600-legacy` | rojo usado en prompts previos | `#DA3B2B` |
| `color/brand/red/900` | rojo oscuro / alerta | `#CC0000` |

Decision activa: usar `#DB3B2B` como rojo final de T1 en fichas, prompts nuevos, UI y direccion de arte. El valor `#DA3B2B` queda registrado solo como legado de prompts previos.

### 3.2 Paleta Cinematografica T1 Mundial

| Token | Uso | Hex |
|---|---|---|
| `color/film/cream-bg` | fondo de ficha, highlights calidos | `#F7F5F0` |
| `color/film/paper` | tarjetas, areas tecnicas | `#FFFFFF` |
| `color/film/ink` | texto principal | `#1B1B1B` |
| `color/film/ink-soft` | texto secundario | `#545454` |
| `color/film/rule` | divisores finos | `#D8D6D0` |
| `color/film/concrete` | estadio, tunel, ciudad | `#8C8980` |
| `color/film/concrete-dark` | sombras de concreto | `#4F514D` |
| `color/film/grass-muted` | cesped natural poco saturado | `#53694C` |
| `color/film/jersey-green` | uniforme principal ficticio | `#194D36` |
| `color/film/rival-blue` | equipo rival ficticio | `#24476B` |
| `color/film/referee-green` | arbitro fosforescente controlado | `#B7E84A` |
| `color/film/golden-hour` | luz amanecer/ocaso | `#C99245` |
| `color/film/warm-skin-mid` | piel media calida | `#C98963` |
| `color/film/deep-shadow` | sombras frias | `#2D3A4A` |
| `color/film/cardboard` | carton ecommerce | `#A87545` |
| `color/film/screen-white` | pantallas blancas limpias | `#FAFAF7` |
| `color/film/keeper-yellow` | uniforme portero ficticio | `#E6B73D` |

Estos hex son tokens de direccion de arte, no deben usarse como colores planos literales en cada frame. Sirven para consistencia visual, fichas, Figma y prompts.

## 4. Reglas Visuales Globales

- Realismo cinematografico curado.
- Piel con textura natural, no plastica.
- Vestuario limpio, usado con dignidad, sin decadencia.
- Nada de logos, marcas, escudos, textos, QR, UI generada ni iconos.
- Personas mexicanas/latinoamericanas reales para comercio, ciudad, restaurante y jugadores principales.
- Arbitros: fisionomia extranjera, no mexicana/latinoamericana.
- Portero: fisionomia estadounidense, rasgos anglosajones.
- Estadio: exterior moderno modular tipo Soumaya-inspirado por piel/textura/facetas, no por curva literal; interior moderno de concreto sobrio, monumental y ficticio, sin parecer Azteca. Evitar la palabra y el lenguaje brutalista en prompts activos porque el modelo lo interpreta como lugubre/apocaliptico.
- Pantallas: blancas limpias, sin contenido, excepto composicion posterior con UI real T1.
- Rojo T1: usar `#DB3B2B` como acento narrativo, nunca como baño general de color.
- Direccion socioeconomica: mezcla de sectores mexicanos, desde popular cuidado hasta aspiracional real, siempre curado, digno y con ligera prioridad aspiracional.

## 5. Fichas De Personaje Iniciales

### P01 - Joven Con Mochila Roja

**Tomas:** 03, 05, 06.  
**Funcion narrativa:** puente emocional entre Mexico cotidiano y estadio imaginado.  
**Arquetipo:** testigo / joven en ascenso / esperanza contenida.

| Campo | Descripcion |
|---|---|
| Edad aparente | 18-24 |
| Genero | Masculino |
| Fisionomia | Mexicana/latinoamericana real, rostro memorable pero no celebridad |
| Complexion | Media-delgada, natural, no atleta profesional |
| Pelo | Oscuro, natural, corte sencillo urbano |
| Vestuario | Ropa negra completa: hoodie o chamarra ligera, pantalon oscuro, tenis sin logo |
| Acento visual | Mochila roja T1 `#DB3B2B` |
| Entorno | Escaleras de salida, calle centrica CDMX anonima, estadio ficticio interior |
| Personalidad visual | Reservado, determinado, observador, emocion interna |
| Expresiones | neutra, respiracion contenida, asombro, mirada hacia arriba, decision |
| Props | mochila roja, correas visibles, ningun logo |

**Paleta:** negro ropa `#151515`, rojo mochila `#DB3B2B`, piel media `#C98963`, concreto `#8C8980`, golden hour `#C99245`, sombra fria `#2D3A4A`.

**Notas de continuidad:**

- Mismo rostro exacto entre tomas 03, 05 y 06.
- Misma mochila roja, misma ropa negra, misma edad aparente.
- La emocion sube de avance silencioso a asombro, sin volverse triunfo exagerado.
- En toma 06 el estadio crece detras, pero el personaje sigue siendo humano e intimo.

**Negativos:** no uniforme escolar, no celebridad, no atleta, no bandera, no landmarks, no logos, no texto urbano legible.

### P02 - Señora Que Cobra / Vendedora De Mercado

**Toma:** 08.  
**Funcion narrativa:** comercio cotidiano como cancha; primer gesto claro de cobro fluido dentro del mundo T1.  
**Arquetipo:** dueña del ritmo / precision diaria.

| Campo | Descripcion |
|---|---|
| Edad aparente | 40-55 |
| Genero | Femenino |
| Fisionomia | Mexicana real, rasgos regionales naturales, sin caricatura |
| Complexion | Media, cuerpo de trabajo cotidiano |
| Pelo | Oscuro o castano, recogido practico |
| Vestuario | Blusa o delantal limpio, colores neutros con pequenos acentos calidos |
| Acento visual | Fruta/verdura y posible detalle rojo discreto |
| Entorno | Puesto de frutas y verduras, mercado vivo pero ordenado |
| Personalidad visual | Concentrada, rapida, amable, dueña del espacio |
| Expresiones | atenta, resolutiva, ligera sonrisa, foco en transaccion |
| Props | terminal generica de cobro, smartphone cliente, fruta, cajas limpias |

**Paleta:** verdes naturales `#53694C`, jitomate/acento `#DB3B2B`, carton `#A87545`, blanco pantalla `#FAFAF7`, piel media `#C98963`, sombras frias `#2D3A4A`.

**Notas de continuidad:**

- La terminal no debe mostrar marca ni logo.
- Smartphone en blanco o sin contenido.
- Mercado vivo, no caotico, no sucio, no documental crudo.
- Fondo puede tener jerseys verdes genericos desenfocados.

**Negativos:** no QR, no marcas de frutas/cajas, no logos de pago, no texto legible, no cerveza/alcohol.

### P03 - Conductora En Trafico

**Estado:** deprecada. Ya no aparece en el rack visual vigente `02_references/visual/Stills T1mundial`.  
**Toma anterior:** 10.  
**Funcion narrativa:** pausa urbana / espera productiva.  
**Arquetipo:** operadora moderna / ciudad en tension.

| Campo | Descripcion |
|---|---|
| Edad aparente | 28-42 |
| Genero | Femenino |
| Fisionomia | Mexicana/latinoamericana real |
| Vestuario | Casual profesional, manga neutra, sin marca |
| Acento visual | Pulsera smartwatch roja `#DB3B2B` |
| Entorno | Interior de auto, avenida amplia CDMX anonima, trafico denso |
| Personalidad visual | Calma bajo presion, concentrada, practica |
| Props | volante, smartwatch pantalla blanca, tablero sin marcas visibles |

**Paleta:** negro interior auto `#1B1B1B`, rojo pulsera `#DB3B2B`, luces trafico `#8B1F1B`, sombra fria `#2D3A4A`, screen white `#FAFAF7`.

**Notas de continuidad:**

- Esta ficha queda en historial. No generar nuevas fichas salvo reactivacion explicita.
- La rima 10 -> 11 de smartwatch conductora/arbitro queda deprecada.
- No mostrar logos de auto, apps, relojes ni calles reconocibles.

### P12 - Vaso Rojo Cafe / Gesto Comercial

**Toma:** 09.  
**Funcion narrativa:** gesto comercial cotidiano, pausa calida y precisa entre mercado/futbol/equipo.  
**Arquetipo:** detalle de comercio / micro-momento.

| Campo | Descripcion |
|---|---|
| Objeto principal | Vaso/taza roja T1 `#DB3B2B` con cafe o bebida caliente |
| Entorno | Cafeteria o mostrador contemporaneo, clean, sin marcas |
| Props | Vaso rojo sin logo, cafe/espuma natural, manos reales, superficie sobria |
| Paleta | Rojo `#DB3B2B`, cafe `#8A5C3A`, crema `#F7F5F0`, sombra fria `#2D3A4A` |

**Negativos:** no logos, no marcas de cafe, no texto en vaso, no cadena reconocible, no QR.

### P13 - Equipo Huddle

**Toma:** 10.  
**Funcion narrativa:** union del equipo antes del juego.  
**Arquetipo:** equipo / tension previa / energia contenida.

| Campo | Descripcion |
|---|---|
| Personas | Jugadores mexicanos/latinoamericanos reales, diversidad natural |
| Uniforme | Playera verde ficticia `#194D36`, una sola linea blanca en cada hombro, short blanco, calcetas rojas si se ven |
| Pose | Abrazo/huddle cerrado de equipo, tension previa, no celebracion final |
| Entorno | Cancha con estadio desenfocado |

**Negativos:** no uniformes oficiales, no seleccion mexicana, no escudos, no numeros, no marcas deportivas, no atletas reales.

### P04 - Arbitro Extranjero

**Tomas:** 09, 11, 21.  
**Funcion narrativa:** decision, reglas, silbatazo.  
**Arquetipo:** autoridad externa / tension objetiva.

| Campo | Descripcion |
|---|---|
| Edad aparente | 35-50 |
| Genero | Masculino o femenino, definir por toma |
| Fisionomia | Extranjera: europea, africana o cualquier region excepto Mexico/LatAm |
| Complexion | Atletica funcional, no celebridad |
| Vestuario | Playera verde fosforescente, short negro, sin insignias |
| Acento visual | Smartwatch con pulsera roja `#DB3B2B` |
| Entorno | Cancha, estadio lleno desenfocado |
| Personalidad visual | Preciso, firme, serio, neutral |
| Props | smartwatch, silbato sin marca si aplica |

**Paleta:** referee green `#B7E84A`, negro short `#151515`, rojo pulsera `#DB3B2B`, cesped `#53694C`, concreto estadio `#8C8980`.

**Negativos:** no escudos federativos, no FIFA, no World Cup, no marca deportiva, no bandera.

### P05 - Hombre De Ecommerce / Bodega

**Toma:** 14.  
**Funcion narrativa:** disciplina invisible del negocio.  
**Arquetipo:** operador metodico.

| Campo | Descripcion |
|---|---|
| Edad aparente | 30-45 |
| Genero | Masculino |
| Fisionomia | Mexicana/latinoamericana real |
| Vestuario | Camisa o playera neutra de trabajo, delantal opcional sin logo |
| Entorno | Pequena bodega/taller limpio, funcional, no precario |
| Personalidad visual | Practico, silencioso, cuidadoso |
| Props | caja de carton, cinta blanca, etiqueta generica sin texto, mesa de empaque |

**Paleta:** carton `#A87545`, cinta blanca `#F7F5F0`, luz fria funcional `#D8E0E4`, sombra `#2D3A4A`, piel `#C98963`.

**Negativos:** no paqueterias, no codigos de barra legibles, no marcas de marketplace, no texto.

### P06 - Capitan / Delantero Equipo Principal

**Tomas:** 12, 13, 15, 23, 26, 28, 30.  
**Funcion narrativa:** energia deportiva del equipo ficticio.  
**Arquetipo:** precision / ataque / gesto decisivo.

| Campo | Descripcion |
|---|---|
| Edad aparente | 22-32 |
| Fisionomia | Mexicana/latinoamericana, no atleta real |
| Complexion | Atletica natural |
| Uniforme | Jersey verde con una sola linea blanca en hombro, short blanco, calcetas rojas |
| Acento visual | Calcetas rojas `#DB3B2B`, cinta de capitan con C roja |
| Props | balon clasico pentagonos negros/hexagonos blancos, botas sin logo |

**Paleta:** jersey green `#194D36`, blanco uniforme `#F7F5F0`, rojo calcetas `#DB3B2B`, negro balon `#111111`, cesped `#53694C`.

**Negativos:** no seleccion mexicana, no escudos, no marcas deportivas, no patrones oficiales.

### P07 - Entrenador Con Tablet

**Toma:** 16.  
**Funcion narrativa:** estrategia deportiva paralela a estrategia comercial.  
**Arquetipo:** lector del juego.

| Campo | Descripcion |
|---|---|
| Edad aparente | 40-60 |
| Fisionomia | Mexicana/latinoamericana o internacional neutra |
| Vestuario | Polo negro liso, pantalon oscuro, sin logo |
| Props | tablet con pantalla blanca, smartwatch pulsera roja |
| Entorno | Borde de campo, partido desenfocado |

**Notas:** rima visual con P08 y P09: over-the-shoulder desde hombro derecho, dispositivo en mismo eje.

### P08 - Emprendedora De Skincare / Joyeria

**Toma:** 17.  
**Funcion narrativa:** negocio aspiracional real, venta y control de productos de skincare, joyeria y accesorios.  
**Arquetipo:** fundadora tranquila / ojo fino.

| Campo | Descripcion |
|---|---|
| Edad aparente | 25-40 |
| Genero | Femenino |
| Fisionomia | Mexicana/latinoamericana real |
| Vestuario | Blusa neutra, joyeria minima, maquillaje natural |
| Entorno | Mesa con skincare, joyeria, accesorios y prendas deportivas al fondo |
| Props | laptop pantalla blanca, productos sin etiqueta, cafe opcional |

**Paleta:** screen white `#FAFAF7`, piel `#C98963`, neutros calidos `#D7C4AE`, rojo acento `#DB3B2B`, sombra fria `#2D3A4A`.

**Negativos:** no marcas de cosmeticos, no texto en envases, no UI, no logo laptop.

### P09 - Vendedor De Sneakers

**Tomas:** 18, 19.  
**Funcion narrativa:** comercio joven, inventario, velocidad de venta.  
**Arquetipo:** curador urbano / vendedor atento.

| Campo | Descripcion |
|---|---|
| Edad aparente | 22-32 |
| Genero | Masculino |
| Fisionomia | Mexicana/latinoamericana real |
| Vestuario | Streetwear sobrio, sin logos, capas neutras |
| Entorno | Tienda de sneakers, playeras de futbol genericas, gorras, calle al fondo |
| Props | smartphone pantalla blanca, sneakers rojos en repisa acrilica |

**Paleta:** rojo sneaker `#DB3B2B`, negro/charcoal `#1B1B1B`, blanco pantalla `#FAFAF7`, acrilico `#D8E0E4`, luz tarde `#C99245`.

**Negativos:** no swoosh, no adidas stripes, no marcas, no cajas con texto, no logos deportivos.

### P10 - Protagonista Del Restaurante

**Tomas:** 20, 22, 31, 32.  
**Funcion narrativa:** tension y liberacion del comercio/futbol; cliente que esta creando o activando su tienda justo en el momento paralelo al cobro de la falta.  
**Arquetipo:** cliente-emprendedor / aficionado que convierte el momento en negocio.

| Campo | Descripcion |
|---|---|
| Edad aparente | 24-32 |
| Fisionomia | Mexicana/latinoamericana real, sin barba ni bigote |
| Rol | Cliente de T1 en proceso de crear/activar su tienda durante el partido |
| Vestuario | Playera deportiva roja `#DB3B2B` tipo jersey generico de aficionado, con una sola linea blanca en cada hombro; sin escudo, sin logo, sin numero visible |
| Entorno | Restaurante mexicano contemporaneo, clean, tranquilo, aspiracional real; no Tulum/tuluminati |
| Props | smartphone vertical; en 20/22/32 vemos respaldo, en 31 pantalla blanca |
| Expresiones | tension contenida, espera, alivio, celebracion |

**Paleta:** jersey red `#DB3B2B`, mesa madera `#8A5C3A`, tortillas/maiz `#DDBB75`, verdes comida `#53694C`, sombras `#2D3A4A`.

**Notas de grupo:** las personas alrededor deben tener variedad clara de rostros, generos, tonos de piel, edades y rasgos; no deben parecer copias del protagonista. Vestuario natural/random de restaurante, priorizando playeras deportivas ficticias coherentes: verdes con linea blanca en cada hombro, blancas con linea roja `#DB3B2B`, blancas con linea verde `#194D36`, rojas con linea blanca. Sin logos, escudos, numeros ni marcas.

**Negativos:** no barba, no bigote, no alcohol, no cervezas, no marcas de restaurante, no UI inventada, no pantalla visible salvo toma 31 blanca, no Tulum/tuluminati, no boho playero, no decoracion turistica.

### P11 - Portero Estadounidense

**Tomas:** 25, 27, 29.  
**Funcion narrativa:** suspenso, defensa, proteccion.  
**Arquetipo:** obstaculo / guardian.

| Campo | Descripcion |
|---|---|
| Edad aparente | 25-35 |
| Fisionomia | Estadounidense, rasgos anglosajones |
| Complexion | Atletica, alto, potente |
| Uniforme | Amarillo solido, sin logo |
| Props | guantes sin marca, tachones sin logo |
| Entorno | Porteria centrada, estadio lleno desenfocado |
| Expresiones | concentracion extrema, mandibula tensa, mirada fija |

**Paleta:** keeper yellow `#E6B73D`, negro guantes `#111111`, blanco porteria `#F7F5F0`, cesped `#53694C`, sombra fria `#2D3A4A`.

**Negativos:** no club, no seleccion, no marca de guantes, no rostro de atleta real.

## 6. Fichas De Locacion Iniciales

### L01 - Tienda Con Cortina Metalica

**Toma:** 01.  
**Rol:** apertura del mundo comercio.  
**Materiales:** metal corrugado, banqueta, polvo fino, luz dorada baja.  
**Paleta:** metal `#8C8980`, golden hour `#C99245`, sombra `#2D3A4A`, tinta `#1B1B1B`.

**Reglas:** composicion frontal simetrica, cortina como textura hero, sin letreros ni marcas.

### L02 - Metro / Escaleras / Calle CDMX Anonima

**Tomas:** 03, 05.  
**Rol:** ascenso urbano hacia algo grande.  
**Materiales:** concreto, loseta, barandal, luz de ocaso.  
**Paleta:** concreto `#8C8980`, golden hour `#C99245`, azul sombra `#2D3A4A`, rojo mochila `#DB3B2B`.

**Reglas:** solo 5% de boca de metro en toma 05, avenida abierta, sin coches ni multitud, sin landmarks.

### L03 - Estadio Moderno Modular Soumaya-Inspirado / Concreto Sobrio

**Tomas:** 02, 04, 06, 09, 11-13, 15-16, 21, 23, 25-30, 33-34.  
**Rol:** escenario monumental, pero legalmente ficticio.  
**Direccion formal:** exterior ovalado, continuo y uniforme, tipo estadio moderno de anillo envolvente, con acabado modular/facetado tipo Soumaya-inspirado por piel arquitectonica y textura. La forma debe ser ordenada, no irregular ni deforme. Puede tomar la claridad formal de una renovacion contemporanea tipo nuevo Bernabeu, sin copiarlo ni hacerlo reconocible. El exterior debe ser brillante-controlado, luminoso y aspiracional. El interior debe ser moderno de concreto sobrio: tunel de jugadores, gradas, accesos de cancha y estructura limpia. Evitar lenguaje brutalista.  
**Materiales:** exterior con piel modular/facetada en metal claro brillante-controlado o concreto claro texturizado; interior con concreto claro expuesto, gradas geometricas limpias, cesped natural, haze ligero, luces calidas-controladas.  
**Paleta:** concrete `#8C8980`, concrete dark `#4F514D`, grass `#53694C`, screen light `#F7F5F0`, shadow `#2D3A4A`.

**Reglas:** no Azteca, no copia literal del Museo Soumaya, no curva literal Soumaya, no Santiago Bernabeu reconocible, no estadio real reconocible, no silueta irregular/deforme, no brutalismo, no exterior pesado, no iluminacion apocaliptica/lugubre, no publico tetrico, no tunel gigante, no tunel de acceso publico, no nombres, no arquitectura reconocible como edificio real, no logos, no banderas, no FIFA/World Cup.

### L04 - Mercado De Frutas Y Verduras

**Toma:** 08.  
**Rol:** comercio vivo y tactil.  
**Materiales:** fruta, verdura, cajas limpias, manteles neutros, terminal generica.  
**Paleta:** greens `#53694C`, tomato red `#DB3B2B`, cardboard `#A87545`, cream `#F7F5F0`.

**Reglas:** vivo pero ordenado, no precarizado, no saturacion excesiva.

### L05 - Bodega / Taller Ecommerce

**Toma:** 14.  
**Rol:** disciplina operativa.  
**Materiales:** carton, cinta, mesa, impresora generica, repisas.  
**Paleta:** cardboard `#A87545`, neutral wall `#D8D6D0`, cool light `#D8E0E4`, ink `#1B1B1B`.

**Reglas:** sin carriers, sin marketplaces, sin etiquetas legibles.

### L06 - Mesa Emprendedora Skincare / Joyeria

**Toma:** 17.  
**Rol:** control comercial, detalle, inventario.  
**Materiales:** laptop, productos sin etiqueta, joyeria minima, textiles deportivos al fondo.  
**Paleta:** cream `#F7F5F0`, warm neutral `#D7C4AE`, red accent `#DB3B2B`, ink `#1B1B1B`.

**Reglas:** aspiracional real, no influencer set, no marcas.

### L07 - Tienda De Sneakers

**Tomas:** 18, 19.  
**Rol:** comercio urbano joven.  
**Materiales:** acrilico, repisas, sneakers genericos, gorras, playeras ficticias.  
**Paleta:** red accent `#DB3B2B`, charcoal `#1B1B1B`, acrylic `#D8E0E4`, warm light `#C99245`.

**Reglas:** absolutamente sin swoosh, stripes, logos, cajas reconocibles ni marcas.

### L08 - Restaurante Mexicano

**Tomas:** 20, 22, 24, 31, 32.  
**Rol:** tension colectiva y celebracion cotidiana.  
**Materiales:** madera limpia, vidrio, muros neutros, plantas discretas, comida mexicana, celulares, luz calida-controlada, playeras deportivas genericas.  
**Paleta:** red jersey `#DB3B2B`, wood `#8A5C3A`, maize `#DDBB75`, green `#53694C`, shadow `#2D3A4A`.

**Reglas:** restaurante contemporaneo, clean, tranquilo, aspiracional real; no Tulum/tuluminati, no boho playero, no decoracion turistica. Comida real y cuidada, sin cerveza/alcohol, sin marcas, sin pantallas con UI.

### L09 - Mexico Nocturno / Espacio

**Tomas:** 35, 36.  
**Rol:** cierre de escala pais/sistema.  
**Materiales:** luces urbanas, atmosfera nocturna, planeta completo.  
**Paleta:** deep space `#07111F`, glow warm `#DDBB75`, shadow blue `#2D3A4A`, soft white `#F7F5F0`.

**Reglas:** no mapa politico literal, no labels, no fronteras marcadas, no media luna en toma 36.

## 7. Dónde Guardar Las Imagenes Generadas

Usar esta regla:

- `02_references/`: imagenes externas o referencias de inspiracion que NO son assets propios finales.
- `07_assets/`: imagenes propias generadas o aprobadas para continuidad del proyecto.
- `04_production/`: outputs de trabajo por herramienta, pruebas, versiones y renders.

Guardar las fichas visuales generadas asi:

```text
07_assets/characters/model-sheets/
07_assets/locations/model-sheets/
```

Naming recomendado:

```text
t1mundial_model-sheet_P01_joven-mochila-roja_v001_20260508.png
t1mundial_model-sheet_P01_joven-mochila-roja_v002_20260508.png
t1mundial_model-sheet_L03_estadio-modular-soumaya-concreto-sobrio_v001_20260508.png
```

Cuando una ficha quede aprobada, duplicar o mover una copia a:

```text
07_assets/characters/model-sheets/approved/
07_assets/locations/model-sheets/approved/
```

Las versiones de exploracion o fallidas pueden vivir en:

```text
04_production/ai-generations/raw/model-sheets/
04_production/ai-generations/rejected/model-sheets/
04_production/ai-generations/selected/model-sheets/
```

## 8. Prompt Base Para Generar Una Ficha

```text
Crea una ficha visual de personaje para T1 Mundial, en español, formato horizontal 16:9, estilo model sheet cinematografico premium.

Diseño editorial minimalista con tipografia tipo SF Pro, fondo blanco calido, divisores finos, reticula limpia, swatches de color con codigos hexadecimales visibles. No usar estilo cartoon, no plantilla escolar, no exceso de decoracion.

La ficha debe incluir:
1. Ficha de identidad.
2. Identidad y escala: vista frontal, 3/4, perfil y posterior.
3. Detalle de cabeza: frontal, perfil, 3/4, angulo bajo, angulo dinamico y vista superior.
4. Paleta de colores con nombres y HEX.
5. Vestuario y accesorios.
6. Props / herramientas.
7. Notas de personaje.
8. Pose cinematografica / close-up.
9. Entorno principal.
10. Negativos legales y visuales.

Look: realismo cinematografico mexicano contemporaneo, luz suave, textura real, piel natural, vestuario limpio y digno, sin marcas, sin logos, sin texto comercial.

PERSONAJE:
[pegar ficha P##]
```

## 9. Prompt Base Para Ficha De Locacion

```text
Crea una ficha visual de locacion para T1 Mundial, en español, formato horizontal 16:9, estilo cinematic production design sheet.

Diseño editorial minimalista con tipografia tipo SF Pro, fondo blanco calido, divisores finos, reticula limpia, swatches de color con codigos hexadecimales visibles.

La ficha debe incluir:
1. Identidad de locacion.
2. Rol narrativo.
3. Vistas: plano abierto, plano medio, detalle de textura, entrada/salida, hero frame.
4. Paleta de colores con nombres y HEX.
5. Materiales.
6. Props.
7. Luz y atmosfera.
8. Reglas de continuidad.
9. Negativos legales y visuales.

Look: realismo cinematografico curado, Mexico contemporaneo sin cliche, materiales limpios y dignificados, atmosfera suave, no publicidad stock.

LOCACION:
[pegar ficha L##]
```

## 10. Contexto Que Falta Definir

Para cerrar fichas finales y no dejar que el modelo invente de mas, conviene decidir:

1. Nombre interno de cada personaje recurrente, aunque no aparezca en pantalla.
2. Edad exacta o rango final.
3. Nombres internos opcionales para personajes recurrentes, solo si ayudan a identificarlos en produccion.
4. Rasgos fisicos clave que no deben cambiar entre tomas.
5. Detalle exacto de la accion T1 en P10: crear tienda, activar tienda, confirmar cobro o completar setup.
6. Nivel socioeconomico visual por locacion: popular cuidado, aspiracional real, corporativo, familiar.
7. Assets reales T1 para pantallas, si ya existen.
8. Paleta oficial T1 completa mas alla del rojo final `#DB3B2B`.
