---
title: "Model Sheets Master Generation Pack"
doc_type: "prompt-pack"
status: "draft"
owner: "Arturo / Parco"
reviewers: []
version: "0.1"
last_updated: "2026-05-08"
language: "es"
audience: ["creative", "production", "ai-image"]
tags: ["model-sheets", "personajes", "locaciones", "prompts", "chatgpt-images", "continuity"]
source_of_truth: "../model-sheets-personajes-locaciones-v001.md"
confidence: "medium"
related_docs:
  - "../model-sheets-personajes-locaciones-v001.md"
  - "chatgpt-master-rack-36-v004.md"
  - "../../04_production/camera-animation-bible-36-v001.md"
---

# Model Sheets Master Generation Pack

## Uso Recomendado En ChatGPT Images

Para reducir que el modelo invente, trabajar asi:

1. Abrir un chat nuevo por bloque: personajes comercio, personajes futbol, locaciones.
2. No adjuntar imagenes de referencia por default. El prompt debe sostener color, luz, textura y continuidad por si solo.
3. Pegar siempre el `HEADER MAESTRO`.
4. Si es locacion, pegar tambien el `CANDADO CLEAN PARA LOCACIONES`.
5. Pegar debajo solo el bloque del personaje o locacion que quieres generar.
6. No pedir mas de 1 ficha por generacion.
7. Si sale bien, guardar PNG en `07_assets/.../model-sheets/`.
8. Si sale mal, iterar con patch corto, no reescribir todo desde cero.

## Indice Por Color / Bloque

| Codigo | Color narrativo | Tipo | Assets |
|---|---|---|---|
| `[ROJO]` | T1 / comercio / cobro / activacion | Personajes comercio | P02, P08, P09, P10 |
| `[VERDE]` | Futbol / cancha / uniforme ficticio | Personajes futbol | P04, P06, P07, P11 |
| `[NEGRO]` | Puente emocional / ciudad | Personaje puente | P01 |
| `[GRIS]` | Locaciones fisicas | Locaciones | L01-L08 |
| `[AZUL]` | Cierre pais / espacio | Locaciones cosmicas | L09 |

## Mapa Rapido Por Toma

| Tomas | Asset principal | Codigo |
|---|---|---|
| 01 | L01 Tienda con cortina metalica | `[GRIS]` |
| 02, 04, 06, 09, 11-13, 15-16, 21, 23, 25-30, 33-34 | L03 Estadio moderno modular Soumaya-inspirado / concreto sobrio | `[GRIS/VERDE]` |
| 03, 05, 06 | P01 Joven mochila roja + L02 Metro/calle | `[NEGRO]` |
| 08 | P02 Señora que cobra / mercado + L04 Mercado | `[ROJO]` |
| 09 | P12 Vaso rojo cafe / gesto comercial | `[ROJO]` |
| 10 | P13 Equipo huddle | `[VERDE]` |
| 20 | P04 Arbitro extranjero | `[VERDE]` |
| 14 | P05 Hombre ecommerce + L05 Bodega | `[ROJO]` |
| 12, 13, 15, 23, 26, 28, 30 | P06 Capitan / delantero | `[VERDE]` |
| 16 | P07 Entrenador | `[VERDE]` |
| 17 | P08 Emprendedora skincare / joyeria + L06 Mesa emprendedora | `[ROJO]` |
| 18, 19 | P09 Vendedor sneakers + L07 Tienda sneakers | `[ROJO]` |
| 20, 22, 24, 31, 32 | P10 Protagonista restaurante + L08 Restaurante | `[ROJO]` |
| 25, 27, 29 | P11 Portero estadounidense | `[VERDE]` |
| 35, 36 | L09 Mexico nocturno / espacio | `[AZUL]` |

## HEADER MAESTRO - Pegar Siempre

```text
Crea UNA ficha visual para T1 Mundial, en español, formato horizontal 16:9, estilo model sheet / production design sheet cinematográfico premium.

La ficha debe funcionar como documento de dirección de arte para mantener continuidad visual en una película publicitaria cinematográfica. Debe ser clara, limpia, elegante y útil para producción AI.

DISEÑO:
Diseño editorial minimalista con tipografía tipo SF Pro o equivalente.
Fondo blanco cálido #F7F5F0.
Texto principal #1B1B1B.
Texto secundario #545454.
Divisores finos #D8D6D0.
Retícula limpia, aire visual, márgenes generosos.
Incluir swatches de color con nombres y códigos HEX.
Todo el texto visible debe estar en español.

LOOK GLOBAL:
Realismo cinematográfico mexicano contemporáneo.
Más cine autoral independiente que comercial deportivo.
Luz suave, natural o práctica.
Altas luces con roll-off analógico.
Sombras ligeramente frías pero abiertas.
Color controlado, sin saturación excesiva.
Textura real: piel, tela, metal, concreto, césped y cartón limpio.
Materiales limpios, mantenidos, dignificados.
México contemporáneo sin cliché.
Mezcla de sectores: popular cuidado + aspiracional real, siempre curado.

COLOR:
Rojo T1 final: #DB3B2B.
Usar el rojo T1 solo como acento narrativo, nunca como baño general.
Verdes naturales poco saturados.
Golden hour controlado.
Sombras frías suaves.
Pantallas blancas limpias #FAFAF7.

LEGAL / NEGATIVOS GLOBALES:
No logos.
No marcas.
No texto comercial.
No QR.
No UI inventada.
No marcas deportivas.
No swoosh.
No Adidas stripes.
No escudos.
No banderas.
No símbolos nacionales.
No FIFA.
No World Cup.
No México 2026.
No equipos reales.
No uniformes oficiales.
No celebridades.
No atletas reales.
No landmarks reconocibles.
No Estadio Azteca.
No piel plástica.
No manos deformes.
No anatomía rara.
No look stock.
No HDR agresivo.
No caricatura.
No 3D cartoon.
No texto inventado.
```

## CANDADO CLEAN PARA LOCACIONES - Pegar Siempre Que Sea L01-L08

```text
CANDADO DE LOCACION LIMPIA:
La ficha debe verse igual de premium, clara y editorial que las fichas de personajes aprobadas. Mantener fondo blanco cálido #F7F5F0, retícula limpia, aire visual y color controlado.

Las locaciones deben sentirse vivas, mantenidas, filmables y dignificadas. No deben sentirse abandonadas, deterioradas, sucias, lúgubres, decadentes, postapocalípticas, turísticas ni de stock.

SUPERFICIES Y AMBIENTE:
Todo debe estar limpio y cuidado: pisos, paredes, mesas, cortinas metálicas, concreto, vidrios, repisas, cajas, productos, textiles y mobiliario.
Permitir textura real de uso cotidiano, pero sin mugre, basura, manchas, humedad, óxido dominante, paredes descascaradas, cables sueltos, graffiti, polvo visible, grasa, moho, deterioro o ruina.

LUZ:
Luz suave, cálida-controlada o natural, con sombras abiertas.
No fondo oscuro. No iluminación de terror. No Dune. No apocalíptico. No bodega abandonada. No calle peligrosa. No suciedad dramática.

REGLA DE CONTINUIDAD:
Cada locación debe verse como un espacio mexicano contemporáneo curado para cine: real, humano, aspiracional sin lujo excesivo, popular cuidado cuando aplique.
```

## P01 - Joven Con Mochila Roja `[NEGRO]`

```text
TIPO DE FICHA:
Ficha visual de personaje.

SECCIONES:
1. Ficha de identidad.
2. Identidad y escala: frontal, 3/4, perfil, posterior.
3. Detalle de cabeza: frontal, perfil, 3/4, ángulo bajo, ángulo dinámico, vista superior.
4. Paleta de colores con HEX.
5. Vestuario y accesorios.
6. Props estrictamente necesarios.
7. Notas de personaje.
8. Pose cinematográfica / close-up.
9. Entorno principal.
10. Negativos legales y visuales.

PERSONAJE:
Nombre interno: Joven con mochila roja.
Género: masculino.
Edad aparente: 18 a 24 años.
Fisionomía: joven mexicano/latinoamericano real, rostro memorable pero común.
Complexión: media-delgada, natural, cuerpo urbano real.
Pelo: oscuro, natural, corte sencillo urbano.
Piel: tono medio cálido latinoamericano, textura natural.
Personalidad visual: reservado, determinado, observador, esperanza contenida.
Arquetipo: testigo / joven en ascenso / puente emocional.

VESTUARIO:
Ropa completamente negra.
Hoodie o chamarra ligera negra sin logo.
Playera negra sin marca.
Pantalón oscuro.
Tenis negros o gris oscuro sin logo.
Mochila roja T1 #DB3B2B, sobria, urbana y funcional.

PROPS:
No inventar props extra.
Solo ropa, mochila, tenis y bolsillos funcionales.

ENTORNO:
Escaleras de salida tipo metro/paso subterráneo.
Calle céntrica CDMX anónima, amplia, tranquila y viva.
Interior de estadio ficticio.

PALETA:
Negro ropa #151515.
Rojo mochila T1 #DB3B2B.
Piel media cálida #C98963.
Concreto urbano #8C8980.
Golden hour #C99245.
Sombra fría #2D3A4A.
```

## P02 - Señora Que Cobra / Vendedora De Mercado `[ROJO]`

```text
TIPO DE FICHA:
Ficha visual de personaje.

SECCIONES:
Ficha de identidad, vistas de cuerpo, detalle de cabeza, manos cobrando, paleta, vestuario, props, notas, entorno mercado, negativos.

PERSONAJE:
Nombre interno: Señora que cobra.
Género: femenino.
Edad aparente: 40 a 55 años.
Fisionomía: mujer mexicana real, rasgos regionales naturales, sin caricatura.
Complexión: media, cuerpo de trabajo cotidiano.
Pelo: oscuro o castaño, recogido práctico.
Personalidad visual: concentrada, rápida, amable, dueña del espacio.
Arquetipo: precisión diaria / comercio cotidiano como cancha.

VESTUARIO:
Blusa neutra o delantal limpio.
Ropa práctica, digna, cuidada.
Nada de uniforme de marca.

PROPS:
Terminal genérica de cobro.
Smartphone de cliente.
Fruta y verdura.
Cajas limpias.
Pantallas blancas o sin contenido.

ENTORNO:
Mercado de frutas y verduras, vivo pero ordenado.
Popular cuidado, no precarizado.
Fondo con gente en mood futbolero, desenfocado, sin logos.

PALETA:
Verdes naturales #53694C.
Rojo T1/acento #DB3B2B.
Cartón #A87545.
Pantalla blanca #FAFAF7.
Piel media #C98963.
Sombra fría #2D3A4A.
```

## P03 - Conductora En Trafico `[DEPRECADO]`

```text
ESTADO:
Deprecado. La conductora del coche ya no aparece en el rack visual vigente `02_references/visual/Stills T1mundial`.
No generar ficha nueva salvo que Arturo / Parco reactive la toma.
```

## P12 - Vaso Rojo Cafe / Gesto Comercial `[ROJO]`

```text
TIPO DE FICHA:
Ficha visual de prop / gesto comercial.

PROP:
Nombre interno: Vaso rojo cafe.
Toma vigente: 09.
Funcion narrativa: gesto comercial cotidiano, pausa calida y precisa entre mercado/futbol/equipo.
Objeto principal: vaso o taza roja T1 #DB3B2B con cafe/bebida caliente, sin logo, sin texto, sin marca.
Estilo: detalle cinematografico, luz calida-controlada, manos reales, textura de espuma/cafe natural.

ENTORNO:
Cafeteria o mostrador contemporaneo, clean, sin marcas.
Debe sentirse como comercio mexicano aspiracional real, no cadena reconocible.

PALETA:
Rojo T1 #DB3B2B.
Cafe #8A5C3A.
Crema espuma #F7F5F0.
Sombra fria #2D3A4A.
Madera #8A5C3A.

NEGATIVOS:
No logos.
No marcas de cafe.
No texto en vaso.
No cadena reconocible.
No QR.
No UI.
```

## P13 - Equipo Huddle `[VERDE]`

```text
TIPO DE FICHA:
Ficha visual de grupo / uniforme deportivo.

GRUPO:
Nombre interno: Equipo huddle.
Toma vigente: 10.
Funcion narrativa: union del equipo antes del juego.
Personas: jugadores mexicanos/latinoamericanos reales, diversidad natural de rostros, tonos de piel y complexiones atleticas.

UNIFORME:
Playera verde ficticia #194D36.
Una sola linea blanca en cada hombro, simetrica.
Short blanco.
Calcetas rojas T1 #DB3B2B si se ven.
Sin logos, sin escudos, sin numeros, sin marcas.

POSE:
Abrazo/huddle cerrado de equipo, energia contenida, tension previa, no celebracion final.

PALETA:
Verde playera #194D36.
Linea blanca #F7F5F0.
Rojo calcetas/acento #DB3B2B.
Cesped #53694C.
Sombra fria #2D3A4A.

NEGATIVOS:
No uniformes oficiales.
No seleccion mexicana.
No escudos.
No numeros.
No marcas deportivas.
No atletas reales.
```

## P04 - Arbitro Extranjero `[VERDE]`

```text
TIPO DE FICHA:
Ficha visual de personaje.

PERSONAJE:
Nombre interno: Árbitro extranjero.
Edad aparente: 35 a 50 años.
Fisionomía: extranjera, europea, africana o cualquier región excepto México/LatAm.
Complexión: atlética funcional.
Personalidad visual: preciso, firme, serio, neutral.
Arquetipo: autoridad externa / decisión.

VESTUARIO:
Playera verde fosforescente controlada #B7E84A.
Short negro.
Sin insignias.
Sin logos.

PROPS:
Smartwatch con pulsera roja #DB3B2B.
Silbato genérico sin marca si aplica.

ENTORNO:
Cancha y estadio lleno desenfocado.

PALETA:
Verde árbitro #B7E84A.
Negro short #151515.
Rojo pulsera #DB3B2B.
Césped #53694C.
Concreto estadio #8C8980.
```

## P05 - Hombre Ecommerce / Bodega `[ROJO]`

```text
TIPO DE FICHA:
Ficha visual de personaje.

PERSONAJE:
Nombre interno: Operador ecommerce.
Género: masculino.
Edad aparente: 30 a 45 años.
Fisionomía: mexicano/latinoamericano real.
Personalidad visual: práctico, silencioso, cuidadoso.
Arquetipo: disciplina invisible del negocio.

VESTUARIO:
Playera o camisa neutra de trabajo.
Delantal opcional sin logo.

PROPS:
Caja de cartón.
Cinta blanca.
Etiqueta genérica sin texto.
Mesa de empaque.
Impresora térmica genérica sin marca.

ENTORNO:
Pequeña bodega/taller limpio, funcional, aspiracional real.

PALETA:
Cartón #A87545.
Cinta blanca #F7F5F0.
Luz fría funcional #D8E0E4.
Sombra #2D3A4A.
Piel #C98963.
```

## P06 - Capitán / Delantero Equipo Principal `[VERDE]`

```text
TIPO DE FICHA:
Ficha visual de personaje deportivo.

PERSONAJE:
Nombre interno: Capitán equipo principal.
Edad aparente: 22 a 32 años.
Fisionomía: mexicana/latinoamericana, no atleta real.
Complexión: atlética natural.
Arquetipo: precisión / ataque / gesto decisivo.

UNIFORME:
Jersey verde ficticio #194D36 con UNA sola línea blanca en hombro.
Short blanco.
Calcetas rojas T1 #DB3B2B.
Botas sin logo.
Cinta de capitán blanca con C roja.

PROPS:
Balón clásico con pentágonos negros y hexágonos blancos, sin marca.

ENTORNO:
Cancha, césped natural, estadio ficticio desenfocado.

PALETA:
Jersey green #194D36.
Blanco uniforme #F7F5F0.
Rojo calcetas #DB3B2B.
Negro balón #111111.
Césped #53694C.
```

## P07 - Entrenador Con Tablet `[VERDE]`

```text
TIPO DE FICHA:
Ficha visual de personaje.

PERSONAJE:
Nombre interno: Entrenador.
Edad aparente: 40 a 60 años.
Fisionomía: mexicana/latinoamericana o internacional neutra.
Personalidad visual: lector del juego, serio, analítico.

VESTUARIO:
Polo negro liso.
Pantalón oscuro.
Sin logo.

PROPS:
Tablet con pantalla blanca #FAFAF7.
Smartwatch con pulsera roja #DB3B2B.

ENTORNO:
Borde de campo, partido desenfocado.

NOTA:
Debe rimar visualmente con P08 y P09: over-the-shoulder desde hombro derecho, dispositivo en mismo eje.
```

## P08 - Emprendedora De Skincare / Joyeria `[ROJO]`

```text
TIPO DE FICHA:
Ficha visual de personaje.

PERSONAJE:
Nombre interno: Emprendedora skincare / joyería.
Género: femenino.
Edad aparente: 25 a 40 años.
Fisionomía: mexicana/latinoamericana real.
Personalidad visual: fundadora tranquila, ojo fino, control de detalle.
Arquetipo: negocio aspiracional real.

VESTUARIO:
Blusa neutra.
Joyería mínima.
Maquillaje natural.
Sin marcas visibles.

PROPS:
Laptop pantalla blanca.
Productos de skincare sin etiqueta.
Joyería y accesorios sin logos.
Café opcional sin marca.

ENTORNO:
Mesa de trabajo con skincare, joyería, accesorios y prendas deportivas al fondo.
Aspiracional real, no influencer set.

PALETA:
Pantalla blanca #FAFAF7.
Piel #C98963.
Neutros cálidos #D7C4AE.
Rojo acento #DB3B2B.
Sombra fría #2D3A4A.
```

## P09 - Vendedor De Sneakers `[ROJO]`

```text
TIPO DE FICHA:
Ficha visual de personaje.

PERSONAJE:
Nombre interno: Vendedor de sneakers.
Género: masculino.
Edad aparente: 22 a 32 años.
Fisionomía: mexicana/latinoamericana real.
Personalidad visual: curador urbano, atento, rápido.

VESTUARIO:
Streetwear sobrio sin logos.
Capas neutras.
Nada de marcas deportivas.

PROPS:
Smartphone con pantalla blanca.
Sneakers rojos T1 #DB3B2B en repisa acrílica.
Gorras y playeras ficticias sin logos.

ENTORNO:
Tienda de sneakers y accesorios deportivos.
Luz cálida de tarde.
Calle al fondo.

PALETA:
Rojo sneaker #DB3B2B.
Charcoal #1B1B1B.
Pantalla blanca #FAFAF7.
Acrílico #D8E0E4.
Luz tarde #C99245.
```

## P10 - Protagonista Restaurante / Cliente T1 `[ROJO]`

```text
TIPO DE FICHA:
Ficha visual de personaje.

PERSONAJE:
Nombre interno: Cliente T1 restaurante.
Edad aparente: 24 a 32 años.
Fisionomía: mexicano/latinoamericano real, rostro común pero memorable, sin barba ni bigote.
Rol: cliente de T1 que está creando o activando su tienda durante el partido.
Personalidad visual: tenso, concentrado, esperanzado, celebratorio al final.
Arquetipo: aficionado que convierte el momento en negocio.

VESTUARIO:
Playera deportiva roja T1 #DB3B2B tipo jersey genérico de aficionado, similar a camiseta deportiva simple.
Debe tener UNA SOLA LÍNEA BLANCA EN CADA HOMBRO, simétrica: una línea blanca en hombro izquierdo y una línea blanca en hombro derecho. Esa es la única línea/acento gráfico.
Sin doble línea por hombro.
Sin triples líneas.
Sin escudo, sin logo, sin marca, sin número visible.
La playera debe verse como ropa casual de aficionado, no uniforme oficial.
Ropa casual limpia y contemporánea.

PROPS:
Smartphone vertical.
En tomas 20, 22, 32 vemos el respaldo del celular.
En toma 31 la pantalla puede verse blanca limpia, sin UI.
Mesa con comida mexicana y bebidas sin alcohol.

ENTORNO:
Restaurante mexicano contemporáneo, clean, tranquilo, cuidado y aspiracional real.
No Tulum, no tuluminati, no boho playero, no palapa, no barro excesivo, no decoración turística.
Materiales sobrios: madera limpia, vidrio, plantas discretas, muros neutros, luz natural cálida-controlada.
Personas alrededor vestidas de forma natural/random de restaurante, pero priorizando playeras deportivas ficticias coherentes con el sistema T1 Mundial.
Variaciones permitidas: playeras verdes con una línea blanca en cada hombro, playeras blancas con una línea roja #DB3B2B en cada hombro, playeras blancas con una línea verde #194D36 en cada hombro, playeras rojas con una línea blanca en cada hombro.
Todas las playeras deportivas deben ser genéricas, sin logos, sin escudos, sin números y sin marcas.
Debe haber variedad clara de rostros y rasgos: mujeres y hombres, tonos de piel distintos, edades 20-45, diversidad mexicana/latinoamericana natural, algunos rasgos estadounidenses genéricos si están en fondo.
Los rostros del grupo no deben parecer copias del protagonista ni entre sí.

PALETA:
Playera roja T1 #DB3B2B.
Madera #8A5C3A.
Maíz/tortilla #DDBB75.
Verdes comida #53694C.
Sombras #2D3A4A.
```

## P11 - Portero Estadounidense `[VERDE]`

```text
TIPO DE FICHA:
Ficha visual de personaje deportivo.

PERSONAJE:
Nombre interno: Portero estadounidense.
Edad aparente: 25 a 35 años.
Fisionomía: estadounidense, rasgos anglosajones, no atleta real.
Complexión: atlética, alto, potente.
Personalidad visual: concentración extrema, tensión, reflejo.
Arquetipo: obstáculo / guardián / suspenso.

UNIFORME:
Uniforme amarillo sólido #E6B73D.
Sin logo.
Sin escudo.
Guantes sin marca.
Tachones sin logo.

ENTORNO:
Portería centrada, estadio lleno desenfocado, césped natural.

PALETA:
Keeper yellow #E6B73D.
Negro guantes #111111.
Blanco portería #F7F5F0.
Césped #53694C.
Sombra fría #2D3A4A.
```

## L01 - Tienda Con Cortina Metalica `[GRIS]`

```text
TIPO DE FICHA:
Ficha visual de locación.

LOCACIÓN:
Tienda pequeña mexicana con cortina metálica al amanecer.
Rol narrativo: apertura del mundo comercio.
Materiales: metal corrugado limpio, banqueta cuidada, luz dorada baja.
Composición: frontal, simétrica, cortina como textura hero.

PALETA:
Metal #8C8980.
Golden hour #C99245.
Sombra fría #2D3A4A.
Negro tinta #1B1B1B.

NEGATIVOS:
No letreros.
No marcas.
No texto.
No abandono.
No suciedad.
No mugre.
No decadencia.
```

## L02 - Metro / Escaleras / Calle CDMX Anonima `[GRIS]`

```text
TIPO DE FICHA:
Ficha visual de locación.

LOCACIÓN:
Salida tipo metro o paso subterráneo y calle céntrica de CDMX anónima.
Rol narrativo: ascenso urbano hacia algo grande.
Materiales: concreto, loseta, barandal, luz de ocaso.
La calle debe ser amplia, viva, tranquila, no vacía ni postapocalíptica.

PALETA:
Concreto #8C8980.
Golden hour #C99245.
Sombra azul #2D3A4A.
Rojo mochila #DB3B2B.

NEGATIVOS:
No landmarks.
No texto urbano legible.
No monumentos.
No tráfico dominante.
No multitud.
```

## L03 - Estadio Moderno Modular Soumaya-Inspirado / Concreto Sobrio `[GRIS/VERDE]`

```text
TIPO DE FICHA:
Ficha visual de locación.

SECCIONES:
Identidad de locación.
Rol narrativo.
Vistas principales: exterior monumental, interior de cancha, túnel de jugadores, gradas, vista cenital y detalle de textura.
Paleta de colores con HEX.
Materiales.
Props / elementos arquitectónicos.
Luz y atmósfera.
Reglas de continuidad.
Plano cinematográfico hero.
Negativos legales y visuales.

LOCACIÓN:
Nombre interno: Estadio modular Soumaya-inspirado T1.
Tipo: estadio monumental ficticio.
Función narrativa: escenario donde fútbol y comercio se sienten como una sola fuerza colectiva.
Rol emocional: escala, tensión, orgullo tranquilo, épica cotidiana, país vivo.

DIRECCIÓN FORMAL:
Exterior ovalado, continuo y uniforme, tipo estadio moderno de anillo envolvente, con acabado Soumaya por MODULOS, PIEL y TEXTURA.
Exterior con módulos/facetas, paneles plateados, metal claro brillante-controlado o concreto claro texturizado, textura arquitectónica contemporánea.
La silueta exterior debe ser ovalada y ordenada, no irregular, no deforme, no caprichosa.
Debe sentirse cercano a una renovación contemporánea tipo nuevo Bernabéu en claridad de forma y continuidad de envolvente, pero con acabado modular/facetado Soumaya-inspirado.
El exterior debe ser luminoso, icónico, moderno y aspiracional.
No hacer la curva literal del Museo Soumaya.
No copiar la silueta del Museo Soumaya.
No copiar el Santiago Bernabéu ni otro estadio real.
No edificio reconocible.
Interior moderno de concreto sobrio: túnel de jugadores, gradas, escaleras técnicas, accesos de cancha y estructura. No usar lenguaje de arquitectura pesada, opresiva, cruda, sucia o lúgubre.

ARQUITECTURA:
Exterior amplio, horizontal y ovalado de estadio, modular/facetado, brillante pero no plástico.
Interior con gradas de concreto claro/sobrio, geometría limpia, túnel de jugadores y escala enorme solo en cancha/gradas.
Túnel de jugadores: corredor funcional de salida al campo, proporción humana, ancho medio, no gigantesco, no vestíbulo público, no entrada de aficionados. Debe sentirse backstage deportivo: concreto sobrio, piso limpio, luz cálida al final hacia la cancha, algunos jugadores en silueta o piernas entrando al campo, sin multitudes.
Césped natural poco saturado.
Portería blanca genérica.
Gradas llenas con público vivo y celebratorio: afición mexicana diversa mezclada con personas estadounidenses genéricas, familias, jóvenes, adultos, ropa casual y jerseys verdes genéricos sin logos.

LUZ:
Luz cinematográfica suave, viva y esperanzadora.
Golden hour sutil o luz de estadio cálida-controlada.
Sombras frías abiertas.
Atmósfera limpia, con profundidad suave.
Nada Dune, nada apocalíptico, nada lúgubre.

PALETA:
Metal claro exterior #B9B8B0.
Concreto claro exterior #C8C4B8.
Concreto interior #8C8980.
Concreto sombra #4F514D.
Césped #53694C.
Blanco luz / portería #F7F5F0.
Sombra fría #2D3A4A.
Golden hour #C99245.
Rojo T1 mínimo #DB3B2B.

NEGATIVOS:
No Estadio Azteca.
No copia literal del Museo Soumaya.
No curva literal del Museo Soumaya.
No silueta reconocible del Museo Soumaya.
No Santiago Bernabéu reconocible.
No copiar estadio real.
No silueta irregular.
No volumen deforme.
No arquitectura pesada.
No arquitectura opresiva.
No interior lúgubre de concreto.
No exterior oscuro.
No concreto sucio.
No mugre.
No humedad.
No deterioro.
No túnel gigante.
No túnel para público.
No vestíbulo de aficionados.
No personas caminando como acceso general dentro del túnel.
No túnel monumental tipo aeropuerto.
No Dune.
No apocalíptico.
No distópico.
No tétrico.
No público tétrico.
No público deformado en primer plano.
No logos.
No marcas.
No banderas.
No escudos.
No FIFA.
No World Cup.
No México 2026.
No anuncios.
No texto visible.
```

## L04 - Mercado De Frutas Y Verduras `[GRIS/ROJO]`

```text
TIPO DE FICHA:
Ficha visual de locación.

LOCACIÓN:
Mercado de frutas y verduras.
Rol narrativo: comercio vivo y táctil.
Materiales: fruta, verdura, cajas limpias, manteles neutros, terminal genérica.
Ambiente: vivo, ordenado, popular cuidado, no precarizado.

PALETA:
Verdes #53694C.
Rojo acento #DB3B2B.
Cartón #A87545.
Cream #F7F5F0.

NEGATIVOS:
No QR.
No logos de pago.
No marcas de cajas.
No cerveza.
No texto.
```

## L05 - Bodega / Taller Ecommerce `[GRIS/ROJO]`

```text
TIPO DE FICHA:
Ficha visual de locación.

LOCACIÓN:
Pequeña bodega/taller ecommerce.
Rol narrativo: disciplina operativa.
Materiales: cartón, cinta, mesa, impresora genérica, repisas.
Ambiente: limpio, funcional, real, aspiracional sin lujo excesivo.

PALETA:
Cartón #A87545.
Pared neutra #D8D6D0.
Luz fría funcional #D8E0E4.
Texto/negro #1B1B1B.

NEGATIVOS:
No carriers.
No marketplaces.
No etiquetas legibles.
No precariedad.
```

## L06 - Mesa Emprendedora Skincare / Joyeria `[GRIS/ROJO]`

```text
TIPO DE FICHA:
Ficha visual de locación.

LOCACIÓN:
Mesa de emprendedora de skincare, joyería y accesorios.
Rol narrativo: control comercial, detalle, inventario.
Materiales: laptop, productos sin etiqueta, joyería mínima, textiles deportivos al fondo.
Ambiente: aspiracional real, no influencer set.

PALETA:
Cream #F7F5F0.
Neutro cálido #D7C4AE.
Rojo acento #DB3B2B.
Negro texto #1B1B1B.

NEGATIVOS:
No marcas cosméticas.
No texto en envases.
No logo laptop.
No UI.
```

## L07 - Tienda De Sneakers `[GRIS/ROJO]`

```text
TIPO DE FICHA:
Ficha visual de locación.

LOCACIÓN:
Tienda de sneakers y accesorios deportivos.
Rol narrativo: comercio urbano joven.
Materiales: acrílico, repisas, sneakers genéricos, gorras, playeras ficticias.
Ambiente: cálido, aspiracional real, urbano, ordenado.

PALETA:
Rojo acento #DB3B2B.
Charcoal #1B1B1B.
Acrílico #D8E0E4.
Luz cálida #C99245.

NEGATIVOS:
No swoosh.
No Adidas stripes.
No marcas.
No cajas reconocibles.
No logos deportivos.
```

## L08 - Restaurante Mexicano `[GRIS/ROJO]`

```text
TIPO DE FICHA:
Ficha visual de locación.

LOCACIÓN:
Restaurante mexicano cuidado.
Rol narrativo: tensión colectiva y celebración cotidiana.
Materiales: madera, comida mexicana, celulares, luz cálida, jerseys genéricos.
Ambiente: vivo, familiar, aspiracional real, no cantina, no bar.

PALETA:
Rojo jersey #DB3B2B.
Madera #8A5C3A.
Maíz/tortilla #DDBB75.
Verde comida #53694C.
Sombra #2D3A4A.

NEGATIVOS:
No alcohol.
No cerveza.
No marcas.
No pantallas con UI.
No logos.
```

## L09 - Mexico Nocturno / Espacio `[AZUL]`

```text
TIPO DE FICHA:
Ficha visual de locación abstracta/cierre.

LOCACIÓN:
México nocturno desde arriba y Tierra desde espacio.
Rol narrativo: cierre de escala país/sistema.
Materiales visuales: luces urbanas, atmósfera nocturna, planeta completo.
Debe sentirse poético, no mapa literal.

PALETA:
Espacio profundo #07111F.
Brillo cálido #DDBB75.
Azul sombra #2D3A4A.
Blanco suave #F7F5F0.

NEGATIVOS:
No mapa político literal.
No labels.
No fronteras marcadas.
No media luna en toma 36.
No banderas.
No símbolos nacionales.
```
