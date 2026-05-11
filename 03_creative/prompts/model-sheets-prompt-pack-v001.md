---
title: "Model Sheets Prompt Pack"
doc_type: "prompt-pack"
status: "active"
owner: "Arturo / Parco"
reviewers: []
version: "0.2"
last_updated: "2026-05-11"
language: "es"
audience: ["creative", "production", "ai-image"]
tags: ["model-sheets", "personajes", "locaciones", "prompts"]
source_of_truth: "../model-sheets-personajes-locaciones-v001.md"
confidence: "medium"
related_docs:
  - "../model-sheets-personajes-locaciones-v001.md"
  - "../prompts/chatgpt-master-rack-36-v004.md"
---

# Model Sheets Prompt Pack

> **v0.2 — 11 mayo 2026:** Prompts completos añadidos para P04, P05, P06, P07, P08 (actualizado), P09, P11, L01, L02, L04, L05, L06, L07, L08, L09. Estos son los prompts operativos activos — usar estos, no los bloques cortos de `model-sheets-master-generation-pack-v001.md`.
>
> Nota histórica: Los bloques L03 v002/v003 abajo quedan como historial. No usar para estadio — contienen lenguaje que empuja al modelo hacia arquitectura oscura/pesada. La ficha aprobada de L03 ya está en `07_assets/locations/model-sheets/approved/`.
>
> **Importante para locaciones:** antes de cualquier L01-L08, pegar el bloque `CANDADO CLEAN PARA LOCACIONES`. Si una ficha sale oscura, sucia, abandonada o con fondo raro, regenerar desde cero con el candado en vez de seguir iterando sobre esa salida.

## Uso

Usar este archivo para copiar y pegar prompts completos de fichas visuales.  
La biblia de especificaciones vive en:

```text
03_creative/model-sheets-personajes-locaciones-v001.md
```

Guardar outputs en:

```text
07_assets/characters/model-sheets/
07_assets/locations/model-sheets/
```

## P01 - Joven Con Mochila Roja - v002

```text
Crea una ficha visual de personaje para T1 Mundial, en español, formato horizontal 16:9, estilo model sheet cinematográfico premium.

Diseño editorial minimalista con tipografía tipo SF Pro, fondo blanco cálido, divisores finos, retícula limpia, swatches de color con códigos hexadecimales visibles. La ficha debe sentirse como un documento de dirección de arte para cine y producción AI, no como ficha escolar, no como concept art fantástico, no como plantilla genérica.

La imagen debe estar completamente en español.

ESTILO VISUAL:
Realismo cinematográfico mexicano contemporáneo, piel natural con textura real, luz suave, color controlado, composición limpia, materiales dignificados, look premium pero humano. Nada cartoon, nada 3D infantil, nada publicitario stock. Más cine autoral independiente que comercial deportivo.

TIPOGRAFÍA Y DISEÑO:
Usar una tipografía limpia tipo SF Pro o equivalente minimalista.
Titulares sobrios, texto pequeño legible, espaciado amplio, líneas divisorias finas color #D8D6D0.
Fondo blanco cálido #F7F5F0.
Texto principal #1B1B1B.
Texto secundario #545454.
Incluir swatches de color con nombre y HEX.

LA FICHA DEBE INCLUIR ESTAS SECCIONES:
1. Ficha de identidad.
2. Identidad y escala: vista frontal, vista 3/4, perfil y posterior.
3. Detalle de cabeza: frontal, perfil, 3/4, ángulo bajo, ángulo dinámico y vista superior.
4. Paleta de colores con nombres y códigos HEX.
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
Fisionomía: joven mexicano/latinoamericano real, rostro memorable pero común, sin parecer celebridad, influencer, atleta profesional ni modelo publicitario.
Complexión: media-delgada, natural, cuerpo urbano real.
Pelo: oscuro, natural, corte sencillo urbano.
Piel: tono medio cálido latinoamericano, textura natural, sin piel plástica.
Personalidad visual: reservado, determinado, observador, con emoción interna. Debe transmitir esperanza contenida, no euforia.
Arquetipo: testigo / joven en ascenso / puente emocional entre México cotidiano y estadio imaginado.

VESTUARIO:
Ropa completamente negra.
Hoodie o chamarra ligera negra sin logo.
Playera negra sin marca.
Pantalón oscuro.
Tenis negros o gris oscuro sin logo, sin swoosh, sin marca.
Mochila roja T1 como acento principal, color #DB3B2B.
La mochila debe conservar el protagonismo visual, pero verse sobria, urbana y funcional: moderna, simple, sin logos, sin texto, sin parches, sin marcas. Debe sentirse como objeto de uso real, no como anuncio de mochila.

PROPS:
No inventar props extra.
No libreta.
No termo.
No audífonos.
No botella.
No accesorios de moda.
Solo mostrar ropa, mochila, tenis y bolsillos funcionales si hace falta.

PALETA DE COLOR:
Negro ropa: #151515.
Rojo mochila T1: #DB3B2B.
Piel media cálida: #C98963.
Concreto urbano: #8C8980.
Golden hour / ocaso: #C99245.
Sombra fría: #2D3A4A.
Fondo ficha: #F7F5F0.
Texto principal: #1B1B1B.
Divisores: #D8D6D0.

ENTORNO:
El personaje pertenece a tres momentos:
1. Escaleras de salida tipo metro o paso subterráneo.
2. Calle céntrica de CDMX anónima, amplia, tranquila y viva, sin multitud ni tráfico dominante. Debe sentirse abierta y real, no vacía ni postapocalíptica. Puede tener señales de ciudad desenfocadas, arquitectura urbana anónima, luz de ocaso y profundidad.
3. Interior de estadio ficticio monumental, moderno y de concreto limpio/sobrio, con arquitectura mexicana contemporánea, escala amplia y sensación cinematográfica. Debe ser una locación ficticia, no réplica de un edificio real.

El sheet puede mostrar pequeños thumbnails de entorno, pero sin texto urbano legible, sin logos, sin señalética real, sin monumentos, sin marcas.

EXPRESIONES:
Neutra.
Concentrado.
Respiración contenida.
Mirada hacia arriba.
Asombro silencioso.
Determinación tranquila.

POSE CINEMATOGRÁFICA / CLOSE-UP:
Close-up cinematográfico del joven mirando ligeramente hacia arriba, con luz suave de ocaso en el rostro y sombra fría en el fondo. La mochila roja puede verse parcialmente en hombro o correa. La emoción debe ser íntima, humana y contenida.

NOTAS DE CONTINUIDAD:
Debe mantener el mismo rostro exacto entre tomas 03, 05 y 06.
Debe mantener la misma ropa negra y la misma mochila roja #DB3B2B.
Debe verse como una persona real de México contemporáneo, no como personaje de moda ni actor famoso.
La emoción debe subir de avance silencioso a asombro, sin volverse triunfo exagerado.
El rojo solo debe vivir en la mochila como acento narrativo.

NEGATIVOS LEGALES Y VISUALES:
No logos.
No marcas.
No texto visible.
No marcas deportivas.
No swoosh.
No Adidas stripes.
No escudos.
No banderas.
No símbolos nacionales.
No celebridades.
No atletas reales.
No influencer look.
No uniforme escolar.
No props extra.
No libreta.
No termo.
No audífonos.
No botella.
No landmarks de CDMX.
No Ángel de la Independencia.
No Torre Latinoamericana.
No Bellas Artes.
No Monumento a la Revolución.
No Estadio Azteca.
No copia literal del Museo Soumaya.
No edificio real reconocible.
No FIFA.
No World Cup.
No México 2026.
No QR.
No UI.
No piel plástica.
No manos deformes.
No anatomía rara.
No look stock.
No HDR agresivo.
No caricatura.
No 3D cartoon.
No texto inventado.
```

## HISTÓRICO NO USAR - L03 - Estadio Soumaya-Inspirado / Interior Brutalista - v002

```text
Crea una ficha visual de locación para T1 Mundial, en español, formato horizontal 16:9, estilo cinematic production design sheet premium.

Diseño editorial minimalista con tipografía tipo SF Pro, fondo blanco cálido, divisores finos, retícula limpia, swatches de color con códigos hexadecimales visibles. La ficha debe sentirse como un documento de dirección de arte para cine y producción AI, no como lámina escolar, no como moodboard casual, no como arquitectura genérica.

La imagen debe estar completamente en español.

ESTILO VISUAL:
Realismo cinematográfico mexicano contemporáneo, arquitectura monumental ficticia, luz suave, color controlado, materiales dignificados, textura real, exterior escultórico tipo Soumaya, interior brutalista de concreto, metal mate, césped, polvo, haze, gradas y escala humana. Más cine autoral independiente que comercial deportivo. No HDR agresivo, no estadio de videojuego, no render inmobiliario.

TIPOGRAFÍA Y DISEÑO:
Usar una tipografía limpia tipo SF Pro o equivalente minimalista.
Titulares sobrios, texto pequeño legible, espaciado amplio, líneas divisorias finas color #D8D6D0.
Fondo blanco cálido #F7F5F0.
Texto principal #1B1B1B.
Texto secundario #545454.
Incluir swatches de color con nombre y HEX.

LA FICHA DEBE INCLUIR ESTAS SECCIONES:
1. Identidad de locación.
2. Rol narrativo.
3. Vistas principales: exterior monumental, interior de cancha, túnel, gradas, vista cenital y detalle de textura.
4. Paleta de colores con nombres y códigos HEX.
5. Materiales.
6. Props / elementos arquitectónicos.
7. Luz y atmósfera.
8. Reglas de continuidad.
9. Plano cinematográfico hero.
10. Negativos legales y visuales.

LOCACIÓN:
Nombre interno: Estadio Soumaya-inspirado T1.
Tipo: estadio monumental ficticio.
Función narrativa: escenario donde el mundo del fútbol y el mundo del comercio mexicano se sienten como una sola fuerza colectiva.
Rol emocional: escala, tensión, orgullo tranquilo, épica cotidiana.
Presencia en tomas: túnel, cancha, gradas, portería, celebración, cenital, fondo del joven con mochila roja.

DIRECCIÓN FORMAL:
El exterior debe sentirse tipo Museo Soumaya: escultórico, curvo, envolvente, facetado, metálico mate o plateado sobrio, con volumen fluido y presencia icónica.
El exterior NO debe verse brutalista ni como una masa pesada de concreto.
El brutalismo vive principalmente en el interior: túneles, gradas, escaleras, accesos y estructura de concreto.
El guiño al Museo Soumaya debe ser inspiración de lenguaje formal, no réplica literal del edificio.
El estadio debe verse original, ficticio y legalmente seguro.
Debe sentirse como una arquitectura nueva e inventada, no como un edificio existente.

ARQUITECTURA:
Exterior curvo, escultórico y facetado, con piel metálica mate o paneles geométricos plateados, evocando el lenguaje del Museo Soumaya sin copiarlo.
Silueta exterior icónica, suave y envolvente, no brutalista.
Interior con gradas de concreto, geometría clara, túneles profundos y escala enorme.
Túneles y accesos con concreto expuesto, líneas fuertes, luz al fondo, polvo y haze.
Cancha con césped natural poco saturado.
Portería blanca genérica sin marcas.
Gradas llenas de público desenfocado, sin banderas, sin escudos, sin textos.

MATERIALES:
Exterior: metal claro brillante-controlado, piel facetada, paneles plateados sobrios, textura arquitectónica contemporánea. Debe sentirse luminoso y aspiracional, no oscuro ni apagado.
Interior: concreto expuesto.
Interior: concreto texturizado.
Escaleras de concreto.
Barandales oscuros sin logos.
Césped natural.
Haze atmosférico.
Luz de estadio suave y realista.

PALETA DE COLOR:
Concreto principal: #8C8980.
Concreto oscuro: #4F514D.
Césped natural poco saturado: #53694C.
Blanco luz / portería: #F7F5F0.
Sombra fría: #2D3A4A.
Metal mate claro: #B9B8B0.
Golden hour sutil: #C99245.
Rojo T1 acento mínimo: #DB3B2B.
Fondo ficha: #F7F5F0.
Texto principal: #1B1B1B.
Divisores: #D8D6D0.

LUZ Y ATMÓSFERA:
Luz cinematográfica suave.
Altas luces con roll-off analógico.
Sombras ligeramente frías.
Haze sutil en túneles y gradas.
Nada de brillo plástico.
Nada de HDR extremo.
Debe sentirse monumental pero real, no futurista, no sci-fi.

VISTAS REQUERIDAS:
Exterior monumental tipo Soumaya-inspirado del estadio ficticio.
Interior desde cancha a gradas.
Túnel de jugadores con contraluz.
Vista de portería centrada.
Vista cenital parcial donde se entienda la piel curva/facetada exterior y el bowl interior.
Detalle de piel exterior facetada.
Detalle de concreto interior.
Detalle de gradas con público desenfocado.
Plano hero cinematográfico con escala humana.

REGLAS DE CONTINUIDAD:
El estadio debe ser el mismo en todas las tomas.
Debe mantener exterior curvo, escultórico y facetado tipo Soumaya-inspirado.
Debe mantener interior brutalista de concreto en túneles, gradas y accesos.
No debe parecer Estadio Azteca.
No debe parecer un estadio real de México ni del mundo.
No debe parecer copia literal del Museo Soumaya.
No debe incluir logos, marcas, nombres, banderas ni señalética real.
Debe poder funcionar tanto en túnel oscuro como en interior lleno y vista cenital.

PLANO CINEMATOGRÁFICO HERO:
Un plano amplio que combine escala interior y lenguaje exterior: desde la cancha se sienten gradas de concreto brutalista, mientras en la parte alta aparece una envolvente curva/facetada tipo Soumaya-inspirada, con haze suave, luces de estadio y público desenfocado. Debe sentirse épico pero sobrio, como cine, no como broadcast deportivo.

NEGATIVOS LEGALES Y VISUALES:
No Estadio Azteca.
No copia literal del Museo Soumaya.
No edificio real reconocible.
No estadio real reconocible.
No nombres de estadio.
No logos.
No marcas.
No patrocinadores.
No FIFA.
No World Cup.
No México 2026.
No banderas.
No escudos.
No símbolos nacionales.
No texto visible.
No señalética legible.
No pantallas con contenido.
No anuncios en gradas.
No marcas deportivas.
No look de render arquitectónico inmobiliario.
No estadio futurista sci-fi.
No arena genérica internacional.
No arquitectura tipo estadio europeo reconocible.
No exterior brutalista de concreto pesado.
No HDR agresivo.
No plástico.
No superficies demasiado brillantes.
No caos visual.
No multitudes deformes en primer plano.
No texto inventado.
```

## HISTÓRICO NO USAR - L03 - Estadio Modular Soumaya-Inspirado / Interior Brutalista - v003

```text
Crea una ficha visual de locación para T1 Mundial, en español, formato horizontal 16:9, estilo cinematic production design sheet premium.

Diseño editorial minimalista con tipografía tipo SF Pro, fondo blanco cálido, divisores finos, retícula limpia, swatches de color con códigos hexadecimales visibles. La ficha debe sentirse como un documento de dirección de arte para cine y producción AI, no como lámina escolar, no como moodboard casual, no como arquitectura genérica.

La imagen debe estar completamente en español.

ESTILO VISUAL:
Realismo cinematográfico mexicano contemporáneo, arquitectura monumental ficticia, luz suave, color controlado, materiales dignificados, textura real, exterior modular/facetado inspirado en el lenguaje material del Museo Soumaya, interior brutalista de concreto, metal mate, césped, polvo suave, haze ligero, gradas vivas y escala humana. Más cine autoral independiente que comercial deportivo.

La iluminación debe seguir la biblia visual de T1 Mundial: suave, cálida-controlada, con roll-off analógico, sombras ligeramente frías pero no lúgubres. Debe sentirse vivo, esperanzador y monumental, no apocalíptico, no Dune, no distópico, no postindustrial.

TIPOGRAFÍA Y DISEÑO:
Usar una tipografía limpia tipo SF Pro o equivalente minimalista.
Titulares sobrios, texto pequeño legible, espaciado amplio, líneas divisorias finas color #D8D6D0.
Fondo blanco cálido #F7F5F0.
Texto principal #1B1B1B.
Texto secundario #545454.
Incluir swatches de color con nombre y HEX.

LA FICHA DEBE INCLUIR ESTAS SECCIONES:
1. Identidad de locación.
2. Rol narrativo.
3. Vistas principales: exterior monumental, interior de cancha, túnel, gradas, vista cenital y detalle de textura.
4. Paleta de colores con nombres y códigos HEX.
5. Materiales.
6. Props / elementos arquitectónicos.
7. Luz y atmósfera.
8. Reglas de continuidad.
9. Plano cinematográfico hero.
10. Negativos legales y visuales.

LOCACIÓN:
Nombre interno: Estadio modular Soumaya-inspirado T1.
Tipo: estadio monumental ficticio.
Función narrativa: escenario donde el mundo del fútbol y el mundo del comercio mexicano se sienten como una sola fuerza colectiva.
Rol emocional: escala, tensión, orgullo tranquilo, épica cotidiana, país vivo.
Presencia en tomas: túnel, cancha, gradas, portería, celebración, cenital, fondo del joven con mochila roja.

DIRECCIÓN FORMAL:
El exterior debe tomar inspiración del Museo Soumaya solo en su sistema modular/facetado y en la textura de piel arquitectónica.
NO hacer la curva literal del Museo Soumaya.
NO copiar la silueta del Museo Soumaya.
NO hacer un edificio reconocible.
El exterior debe ser un estadio original, amplio y bajo/extendido, con piel modular plateada o concreto claro facetado.
Debe sentirse mexicano contemporáneo, escultórico y sobrio, pero no futurista.
El exterior NO debe verse brutalista ni como una masa pesada de concreto.
El brutalismo vive principalmente en el interior: túneles, gradas, escaleras, accesos y estructura de concreto.

ARQUITECTURA:
Exterior de estadio con módulos/facetas inspirados en Soumaya, paneles hexagonales o triangulares sobrios, metal claro brillante-controlado o concreto claro texturizado.
Silueta exterior original, menos curva, más estadio, más horizontal y monumental.
Interior con gradas de concreto, geometría clara, túneles profundos y escala enorme.
Túneles y accesos con concreto expuesto, líneas fuertes, luz cálida al fondo, polvo suave y haze ligero.
Cancha con césped natural poco saturado.
Portería blanca genérica sin marcas.
Gradas llenas de público vivo, humano y mezclado: afición mexicana diversa y personas estadounidenses genéricas, familias, adultos, jóvenes, ropa casual y jerseys verdes genéricos sin logos. El público debe verse vivo y celebratorio, no tétrico.

MATERIALES:
Exterior: módulos/facetas tipo piel arquitectónica, paneles plateados brillante-controlados, concreto claro texturizado, textura sobria.
Interior: concreto expuesto.
Interior: concreto texturizado.
Escaleras de concreto.
Barandales oscuros sin logos.
Césped natural.
Haze atmosférico ligero.
Luz de estadio suave y realista.

PALETA DE COLOR:
Concreto principal: #8C8980.
Concreto oscuro: #4F514D.
Césped natural poco saturado: #53694C.
Blanco luz / portería: #F7F5F0.
Sombra fría: #2D3A4A.
Metal mate claro: #B9B8B0.
Concreto claro exterior: #C8C4B8.
Golden hour sutil: #C99245.
Rojo T1 acento mínimo: #DB3B2B.
Fondo ficha: #F7F5F0.
Texto principal: #1B1B1B.
Divisores: #D8D6D0.

LUZ Y ATMÓSFERA:
Luz cinematográfica suave, viva y esperanzadora.
Golden hour sutil o luz de estadio cálida-controlada.
Altas luces con roll-off analógico.
Sombras ligeramente frías pero abiertas.
Haze sutil en túneles y gradas.
Ambiente lleno de vida, no lúgubre.
Nada de tormenta dramática.
Nada de cielo gris apocalíptico.
Nada de brillo plástico.
Nada de HDR extremo.
Debe sentirse monumental pero real, no futurista, no sci-fi.

VISTAS REQUERIDAS:
Exterior monumental del estadio ficticio con módulos/facetas tipo Soumaya-inspirado, brillante-controlado, sin curva literal.
Interior desde cancha a gradas.
Túnel de jugadores con contraluz cálido, no lúgubre.
Vista de portería centrada.
Vista cenital parcial donde se entienda la piel modular/facetada exterior y el bowl interior.
Detalle de piel exterior modular/facetada.
Detalle de concreto interior.
Detalle de gradas con público vivo y desenfocado.
Plano hero cinematográfico con escala humana.

REGLAS DE CONTINUIDAD:
El estadio debe ser el mismo en todas las tomas.
Debe mantener exterior modular/facetado tipo Soumaya-inspirado, sin curva literal.
Debe mantener interior brutalista de concreto en túneles, gradas y accesos.
No debe parecer Estadio Azteca.
No debe parecer un estadio real de México ni del mundo.
No debe parecer copia literal del Museo Soumaya.
No debe incluir logos, marcas, nombres, banderas ni señalética real.
Debe poder funcionar tanto en túnel oscuro como en interior lleno y vista cenital.

PLANO CINEMATOGRÁFICO HERO:
Un plano amplio que combine escala interior y lenguaje exterior: desde la cancha se sienten gradas de concreto brutalista, mientras en la parte alta aparece una piel modular/facetada Soumaya-inspirada sin curva literal, con haze suave, luces cálidas de estadio y público vivo desenfocado. Debe sentirse épico pero sobrio, como cine, no como broadcast deportivo.

NEGATIVOS LEGALES Y VISUALES:
No Estadio Azteca.
No copia literal del Museo Soumaya.
No curva literal del Museo Soumaya.
No silueta reconocible del Museo Soumaya.
No edificio real reconocible.
No estadio real reconocible.
No nombres de estadio.
No logos.
No marcas.
No patrocinadores.
No FIFA.
No World Cup.
No México 2026.
No banderas.
No escudos.
No símbolos nacionales.
No texto visible.
No señalética legible.
No pantallas con contenido.
No anuncios en gradas.
No marcas deportivas.
No look de render arquitectónico inmobiliario.
No estadio futurista sci-fi.
No arena genérica internacional.
No arquitectura tipo estadio europeo reconocible.
No exterior brutalista de concreto pesado.
No exterior demasiado curvo.
No Dune.
No apocalíptico.
No distópico.
No tétrico.
No cielo de tormenta.
No iluminación lúgubre.
No público tétrico.
No multitudes deformes en primer plano.
No HDR agresivo.
No plástico.
No superficies demasiado brillantes.
No caos visual.
No texto inventado.
```

---

## HEADER MAESTRO — Pegar siempre antes de cada bloque

```text
Crea UNA ficha visual para T1 Mundial, en español, formato horizontal 16:9,
estilo model sheet / production design sheet cinematográfico premium.

La ficha debe funcionar como documento de dirección de arte para mantener
continuidad visual en una película publicitaria cinematográfica. Debe ser
clara, limpia, elegante y útil para producción AI.

DISEÑO:
Diseño editorial minimalista con tipografía tipo SF Pro o equivalente.
Fondo blanco cálido #F7F5F0. Texto principal #1B1B1B. Texto secundario #545454.
Divisores finos #D8D6D0. Retícula limpia, aire visual, márgenes generosos.
Incluir swatches de color con nombres y códigos HEX.
Todo el texto visible debe estar en español.

LOOK GLOBAL:
Realismo cinematográfico mexicano contemporáneo.
Más cine autoral independiente que comercial deportivo.
Luz suave, natural o práctica. Altas luces con roll-off analógico.
Sombras ligeramente frías pero abiertas. Color controlado, sin saturación excesiva.
Textura real: piel, tela, metal, concreto, césped y cartón limpio.
Materiales limpios, mantenidos, dignificados.
México contemporáneo sin cliché.

COLOR:
Rojo T1: #DB3B2B — solo como acento narrativo, nunca como baño general.
Verdes naturales poco saturados. Golden hour controlado. Sombras frías suaves.
Pantallas blancas limpias #FAFAF7.

LEGAL / NEGATIVOS GLOBALES:
No logos. No marcas. No texto comercial. No QR. No UI inventada.
No marcas deportivas. No swoosh. No Adidas stripes. No escudos.
No banderas. No símbolos nacionales. No FIFA. No World Cup. No México 2026.
No equipos reales. No uniformes oficiales. No celebridades. No atletas reales.
No landmarks reconocibles. No Estadio Azteca.
No piel plástica. No manos deformes. No anatomía rara.
No look stock. No HDR agresivo. No caricatura. No 3D cartoon. No texto inventado.
```

---

## CANDADO CLEAN PARA LOCACIONES — Pegar siempre antes de L01-L08

```text
CANDADO DE LOCACION LIMPIA:
La ficha debe verse igual de premium, clara y editorial que las fichas de personajes aprobadas: mismo fondo blanco cálido #F7F5F0, misma retícula limpia, misma tipografía tipo SF Pro, mismas líneas finas #D8D6D0, mismo uso de swatches con HEX.

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

---

## P04 - Árbitro Extranjero - v001

```text
TIPO DE FICHA: Ficha visual de personaje.

SECCIONES:
1. Ficha de identidad.
2. Identidad y escala: frontal, 3/4, perfil, posterior.
3. Detalle de cabeza: frontal, perfil, 3/4, ángulo bajo, ángulo dinámico, vista superior.
4. Paleta de colores con HEX.
5. Vestuario y accesorios.
6. Props.
7. Notas de personaje.
8. Pose cinematográfica / close-up.
9. Entorno principal.
10. Negativos legales y visuales.

PERSONAJE:
Nombre interno: Árbitro extranjero.
Edad aparente: 35 a 50 años.
Fisionomía: extranjera — europea, africana o asiática, nunca mexicana/latinoamericana.
Complexión: atlética funcional, no culturista.
Personalidad visual: preciso, firme, serio, neutral, autoridad externa.
Arquetipo: decisión / autoridad / tensión.

VESTUARIO:
Playera verde fosforescente controlado #B7E84A, corte deportivo funcional.
Short negro #151515. Medias negras. Tachones sin logo.
Sin insignias. Sin escudos. Sin números. Sin marcas deportivas.

PROPS:
Smartwatch con pulsera roja T1 #DB3B2B en muñeca izquierda.
Silbato genérico sin marca si aplica.
No tarjetas, no banderas, no VAR inventado.

ENTORNO:
Cancha de césped natural. Estadio lleno desenfocado al fondo.
Luz de partido: cálida-controlada o golden hour suave.

PALETA:
Verde árbitro #B7E84A. Negro short #151515.
Pulsera roja #DB3B2B. Piel extranjera media-clara #D4A882.
Césped #53694C. Concreto estadio #8C8980. Sombra fría #2D3A4A.

POSE CINEMATOGRÁFICA:
Plano medio, árbitro con brazo extendido señalando, expresión firme.
Estadio y cancha desenfocados. Luz de partido sobre rostro y brazo.
Smartwatch con pulsera roja visible.

NOTAS DE CONTINUIDAD:
Siempre fisionomía extranjera (no latinoamericana). Playera #B7E84A.
Smartwatch con pulsera roja visible cuando mano aparece.
Tomas donde aparece: 09, 11, 21.
```

---

## P05 - Hombre Ecommerce / Bodega - v001

```text
TIPO DE FICHA: Ficha visual de personaje.

SECCIONES:
1. Ficha de identidad.
2. Identidad y escala: frontal, 3/4, perfil, posterior.
3. Detalle de cabeza: frontal, perfil, 3/4, ángulo bajo, ángulo dinámico, vista superior.
4. Paleta de colores con HEX.
5. Vestuario y accesorios.
6. Props.
7. Notas de personaje.
8. Pose cinematográfica / close-up — manos empacando.
9. Entorno principal.
10. Negativos legales y visuales.

PERSONAJE:
Nombre interno: Operador ecommerce.
Género: masculino.
Edad aparente: 30 a 45 años.
Fisionomía: mexicano/latinoamericano real, rasgos comunes, sin parecer modelo.
Personalidad visual: práctico, silencioso, metódico, cuidadoso.
Arquetipo: disciplina invisible del negocio / operación detrás del partido.

VESTUARIO:
Playera o camisa de trabajo en tono oscuro o medio: carbón, gris pizarra o azul marino.
Pantalón funcional oscuro. Calzado cómodo sin logo.
Nada de lino, beige ni arena.
Pulsera delgada roja T1 #DB3B2B en muñeca derecha, discreta, sin logo.

PROPS:
Caja de cartón sin marca. Cinta beige sin texto.
Etiqueta genérica blanca sin texto legible.
Mesa de empaque. Impresora térmica genérica sin marca.
No carriers. No marketplaces. No texto legible en ninguna superficie.

ENTORNO:
Pequeña bodega o taller ecommerce limpio y funcional.
Luz fría funcional, pared neutra, repisas ordenadas.
Real y aspiracional: negocio pequeño bien llevado, no precario.
No almacén industrial. No Amazon. No bodega oscura.

PALETA:
Cartón #A87545. Cinta #D8D6D0. Luz fría #D8E0E4.
Pulsera roja #DB3B2B. Pared neutra #C8C4B8.
Piel media #C98963. Sombra #2D3A4A. Negro ropa #3A3A3A.

POSE CINEMATOGRÁFICA:
Close-up de manos empacando caja sobre mesa. Pulsera roja visible.
Luz fría funcional sobre manos y cartón. Fondo de bodega desenfocado.

NOTAS DE CONTINUIDAD:
Pulsera roja en muñeca derecha siempre visible cuando aparecen las manos.
Ropa oscura sin marcas. Toma donde aparece: 14.
```

---

## P06 - Capitán / Delantero Equipo Principal - v001

```text
TIPO DE FICHA: Ficha visual de personaje deportivo.

SECCIONES:
1. Ficha de identidad.
2. Identidad y escala: frontal, 3/4, perfil, posterior.
3. Detalle de cabeza: frontal, perfil, 3/4, ángulo bajo, ángulo dinámico, vista superior.
4. Paleta de colores con HEX.
5. Uniforme completo y accesorios.
6. Props deportivos.
7. Notas de personaje.
8. Pose cinematográfica / close-up — gesto decisivo.
9. Entorno principal.
10. Negativos legales y visuales.

PERSONAJE:
Nombre interno: Capitán equipo principal.
Edad aparente: 22 a 32 años.
Fisionomía: mexicana/latinoamericana, no atleta real conocido, rostro memorable pero común.
Complexión: atlética natural, no culturista.
Arquetipo: precisión / ataque / liderazgo / gesto decisivo.
Personalidad visual: concentrado, determinado, líder silencioso.

UNIFORME:
Jersey verde ficticio #194D36.
UNA sola línea blanca en cada hombro, simétrica. Sin doble línea. Sin triple línea.
Short blanco #F7F5F0. Calcetas rojas T1 #DB3B2B hasta la rodilla.
Tachones sin logo. Sin escudo. Sin número. Sin marca deportiva.
Cinta de capitán blanca con letra C roja en brazo izquierdo.

PROPS:
Balón clásico: pentágonos negros #111111 y hexágonos blancos #F7F5F0. Sin marca. Sin texto.

ENTORNO:
Cancha de césped natural poco saturado.
Estadio ficticio lleno y desenfocado al fondo.
Luz cinematográfica: golden hour suave o luz de partido cálida-controlada.

PALETA:
Jersey verde #194D36. Blanco short #F7F5F0.
Calcetas rojas #DB3B2B. Balón negro #111111.
Piel latinoamericana media #C98963. Césped #53694C.
Sombra fría #2D3A4A. Golden hour #C99245.

POSE CINEMATOGRÁFICA:
Plano medio del capitán en cancha, brazo levantado o gesto de liderazgo.
Estadio y césped desenfocados. Calcetas rojas visibles. Luz de partido sobre rostro.

NOTAS DE CONTINUIDAD:
Siempre fisionomía latinoamericana. Calcetas rojas #DB3B2B siempre.
Jersey verde #194D36. Cinta de capitán en brazo izquierdo. Balón sin marca si aparece.
Tomas donde aparece: 12, 13, 15, 23, 26, 28, 30.
```

---

## P07 - Entrenador Con Tablet - v001

```text
TIPO DE FICHA: Ficha visual de personaje.

SECCIONES:
1. Ficha de identidad.
2. Identidad y escala: frontal, 3/4, perfil, posterior.
3. Detalle de cabeza: frontal, perfil, 3/4, ángulo bajo, ángulo dinámico, vista superior.
4. Paleta de colores con HEX.
5. Vestuario y accesorios.
6. Props.
7. Notas de personaje.
8. Pose cinematográfica / close-up — tablet en mano.
9. Entorno principal.
10. Negativos legales y visuales.

PERSONAJE:
Nombre interno: Entrenador.
Edad aparente: 40 a 60 años.
Fisionomía: mexicana/latinoamericana o internacional neutra, no atleta real.
Complexión: media, cuerpo de profesional veterano.
Personalidad visual: analítico, lector del juego, serio, contenido.
Arquetipo: estrategia / control / visión táctica.

VESTUARIO:
Polo negro liso sin logo #1B1B1B.
Pantalón oscuro funcional. Sin escudo. Sin marca.
Smartwatch con pulsera roja T1 #DB3B2B en muñeca izquierda.

PROPS:
Tablet con pantalla blanca limpia #FAFAF7. Sin UI. Sin texto. Sin iconos. Sin logo.
La tablet debe estar en mano derecha, inclinada hacia el entrenador.

ENTORNO:
Borde de campo de fútbol. Cancha y partido desenfocados al fondo.
Luz de partido: cálida-controlada. No interior de oficina.

PALETA:
Polo negro #1B1B1B. Pulsera roja #DB3B2B.
Pantalla blanca #FAFAF7. Césped #53694C.
Piel latinoamericana/neutra #C98963. Sombra fría #2D3A4A.

POSE CINEMATOGRÁFICA:
Plano medio, entrenador sosteniendo tablet en borde de campo.
Pulsera roja visible. Pantalla blanca. Partido desenfocado detrás.
Expresión analítica, concentrada, seria.
Rima visual OTS hombro derecho con tomas 17, 18 y 19.

NOTAS DE CONTINUIDAD:
Polo negro siempre. Pulsera roja en muñeca izquierda siempre visible.
Tablet con pantalla blanca. Sin logos en ninguna superficie.
Toma donde aparece: 16.
```

---

## P08 - Emprendedora Skincare / Joyería - v002 (activo)

```text
TIPO DE FICHA: Ficha visual de personaje.

SECCIONES:
1. Ficha de identidad.
2. Identidad y escala: frontal, 3/4, perfil, posterior.
3. Detalle de cabeza: frontal, perfil, 3/4, ángulo bajo, ángulo dinámico, vista superior.
4. Paleta de colores con HEX.
5. Vestuario y accesorios.
6. Props / herramientas de trabajo.
7. Notas de personaje.
8. Pose cinematográfica / close-up.
9. Entorno principal.
10. Negativos legales y visuales.

PERSONAJE:
Nombre interno: Emprendedora skincare / joyería.
Arquetipo: fundadora tranquila / ojo fino / negocio aspiracional real.
Género: femenino.
Edad aparente: 25 a 40 años.
Fisionomía: mujer mexicana/latinoamericana real, rostro común pero memorable, sin parecer celebridad, influencer ni modelo publicitaria.
Tono de piel: medio cálido latinoamericano.
Complexión: natural, cuerpo real.
Cabello: oscuro o castaño, limpio, natural, peinado sobrio y práctico.
Personalidad visual: concentrada, meticulosa, serena, ambiciosa sin ostentación.
Rol narrativo: emprendedora que revisa su tienda o inventario desde laptop mientras prepara productos.
Rango emocional: concentración, calma, control, expectativa, confianza.

VESTUARIO:
Suéter ligero o camiseta estructurada en tono oscuro o medio: carbón #3A3A3A, verde oscuro #194D36, pizarra #4A5568 o negro.
Pantalón de corte recto funcional, tela estructurada, no lino, no beige, no arena, no crema.
NADA de lino. NADA de ropa color arena o crema. NADA de prendas naturales de playa.
Joyería mínima y elegante sin logos.
Maquillaje natural.
Pulsera delgada roja T1 #DB3B2B en muñeca derecha, discreta, sin logo.
La pulsera debe ser visible en vistas de cuerpo y en close-up de manos.

PROPS:
Laptop con pantalla blanca limpia #FAFAF7, sin UI, sin texto, sin iconos, sin logo de marca.
Productos de skincare sin etiqueta: frascos, goteros, cremas genéricas.
Joyería fina o accesorios pequeños sin marca.
Charola o libreta simple sin texto legible.
No logos. No textos. No marcas cosméticas. No marcas de laptop. No ring light.

ENTORNO:
Escritorio de trabajo urbano contemporáneo CDMX.
Mesa de madera oscura o superficie neutra media con elementos de trabajo.
Espacio en departamento urbano o local pequeño bien curado: pared lisa neutra, luz de ventana de ciudad.
NO spa. NO tulum. NO lino ni rattan. NO adobe ni tabique expuesto. NO plantas tropicales.
NO textiles artesanales prominentes. NO canastas de palma. NO estética wellness o yoga.
NO boutique de lujo. NO beauty salon. NO estudio de influencer.
Puede haber una planta discreta no tropical, estante ordenado, muro liso o ventana urbana.

PALETA:
Piel: #C98963. Cabello: #2A1D17.
Vestuario oscuro principal: #3A3A3A o #194D36.
Neutro cálido entorno: #D7C4AE. Crema fondo: #F7F5F0.
Pantalla blanca: #FAFAF7. Sombra fría: #2D3A4A.
Pulsera roja T1: #DB3B2B. Madera oscura: #4A2E1A.

POSE CINEMATOGRÁFICA:
Close-up cinematográfico en 3/4, emprendedora revisando laptop desde mesa de trabajo urbana.
Luz suave sobre rostro y manos, fondo desenfocado con productos y materiales de trabajo.
Pulsera roja visible.

NOTAS DE CONTINUIDAD:
Misma mujer si aparece en derivados. Vestuario oscuro estructurado.
Pulsera roja T1 en muñeca derecha siempre visible. Laptop con pantalla blanca.
Toma donde aparece: 17.

NEGATIVOS ADICIONALES:
No lino. No beige. No crema. No arena. No telas orgánicas de playa.
No tulum. No spa. No wellness. No ring light. No influencer. No beauty salon.
```

---

## P09 - Vendedor De Sneakers - v001

```text
TIPO DE FICHA: Ficha visual de personaje.

SECCIONES:
1. Ficha de identidad.
2. Identidad y escala: frontal, 3/4, perfil, posterior.
3. Detalle de cabeza: frontal, perfil, 3/4, ángulo bajo, ángulo dinámico, vista superior.
4. Paleta de colores con HEX.
5. Vestuario y accesorios.
6. Props.
7. Notas de personaje.
8. Pose cinematográfica / close-up.
9. Entorno principal.
10. Negativos legales y visuales.

PERSONAJE:
Nombre interno: Vendedor de sneakers.
Género: masculino.
Edad aparente: 22 a 32 años.
Fisionomía: mexicano/latinoamericano real, urbano, sin parecer modelo.
Personalidad visual: curador urbano, atento, rápido, cool sin esfuerzo.
Arquetipo: comercio joven / movimiento / cultura urbana.

VESTUARIO:
Streetwear sobrio y oscuro sin logos: sudadera o chamarra en carbón, negro o gris.
Pantalón cargo o jogger oscuro. Tenis sin logo.
NADA de marcas deportivas. NADA de swoosh. NADA de stripes.
Pulsera delgada roja T1 #DB3B2B en muñeca derecha, discreta.

PROPS:
Smartphone con pantalla blanca #FAFAF7, sin UI.
Un par de sneakers rojos T1 #DB3B2B en repisa acrílica o en mano.
Los sneakers son genéricos, sin logo, sin marca, sin texto.
Gorras y playeras en fondo, desenfocadas, sin logos.

ENTORNO:
Tienda de sneakers y accesorios deportivos urbana.
Repisas acrílicas con sneakers, luz cálida de tarde, calle al fondo.
Aspiracional urbano real, no hype boutique de lujo.
No Jordan store. No Nike. No marcas visibles en ninguna superficie.

PALETA:
Sneaker rojo #DB3B2B. Pulsera roja #DB3B2B.
Charcoal ropa #1B1B1B. Acrílico #D8E0E4.
Pantalla blanca #FAFAF7. Luz tarde #C99245.
Piel media #C98963. Sombra fría #2D3A4A.

POSE CINEMATOGRÁFICA:
Plano medio del vendedor mostrando sneakers rojos en tienda.
Pulsera y smartphone visibles. Fondo de tienda desenfocado.
Actitud natural, no pose publicitaria.

NOTAS DE CONTINUIDAD:
Sneakers rojos #DB3B2B siempre sin logo. Pulsera roja en muñeca derecha.
Smartphone pantalla blanca. Ropa oscura sin marcas.
Tomas donde aparece: 18, 19.
```

---

## P11 - Portero Estadounidense - v001

```text
TIPO DE FICHA: Ficha visual de personaje deportivo.

SECCIONES:
1. Ficha de identidad.
2. Identidad y escala: frontal, 3/4, perfil, posterior.
3. Detalle de cabeza: frontal, perfil, 3/4, ángulo bajo, ángulo dinámico, vista superior.
4. Paleta de colores con HEX.
5. Uniforme completo y accesorios.
6. Props deportivos.
7. Notas de personaje.
8. Pose cinematográfica / close-up — postura de alerta.
9. Entorno principal.
10. Negativos legales y visuales.

PERSONAJE:
Nombre interno: Portero estadounidense.
Edad aparente: 25 a 35 años.
Fisionomía: estadounidense, rasgos anglosajones o del norte, no atleta real conocido.
Complexión: atlética, alto, potente, envergadura amplia.
Personalidad visual: concentración extrema, tensión contenida, reflejos.
Arquetipo: obstáculo / guardián / suspenso máximo.

UNIFORME:
Uniforme amarillo sólido #E6B73D — jersey de manga larga y short.
Sin logo. Sin escudo. Sin número. Sin marca.
Guantes de portero sin marca, negros o grises oscuros.
Tachones sin logo.

ENTORNO:
Portería centrada, postes blancos genéricos.
Estadio ficticio lleno y desenfocado al fondo.
Césped natural poco saturado.
Luz de partido: cálida o dramática-controlada.

PALETA:
Keeper yellow #E6B73D. Negro guantes #111111.
Blanco portería #F7F5F0. Césped #53694C.
Piel anglosajona clara #D4A882. Sombra fría #2D3A4A.

POSE CINEMATOGRÁFICA:
Portero en postura de alerta frente a portería, rodillas ligeramente flexionadas,
brazos abiertos, mirada al frente. Estadio y césped desenfocados detrás.
Luz dramática-controlada sobre uniforme amarillo.

NOTAS DE CONTINUIDAD:
Siempre fisionomía anglosajona/estadounidense. Uniforme amarillo #E6B73D siempre.
Sin ninguna marca. Guantes oscuros siempre presentes.
Tomas donde aparece: 25, 27, 29.
```

---

## L01 - Tienda Con Cortina Metálica - v001

```text
TIPO DE FICHA: Ficha visual de locación.

SECCIONES:
1. Ficha de identidad de locación.
2. Vistas principales: exterior frontal, detalle de cortina, plano lateral, plano cinematográfico hero.
3. Paleta de colores con HEX.
4. Materiales y texturas.
5. Luz y atmósfera.
6. Reglas de continuidad.
7. Negativos legales y visuales.

LOCACIÓN:
Nombre interno: Tienda con cortina metálica.
Tipo: fachada de tienda pequeña mexicana.
Rol narrativo: apertura del mundo, primer latido del comercio cotidiano.
Emoción: inicio, silencio antes del movimiento, potencial contenido.

ARQUITECTURA Y MATERIALES:
Cortina metálica corrugada, limpia, mantenida y con textura real de uso.
Banqueta de concreto limpio. Jamba o marco de metal o madera oscura.
Fachada sencilla, anónima, digna. No precaria. No en ruinas.
Puede haber una pequeña planta discreta o maceta al costado.

LUZ Y ATMÓSFERA:
Amanecer o madrugada tardía: luz dorada muy baja rasante sobre el metal.
Sombras largas y frías en contraste, pero abiertas.
La cortina metálica capta y refleja la luz dorada.

PALETA:
Metal corrugado #8C8980. Golden hour #C99245.
Sombra fría #2D3A4A. Negro tinta #1B1B1B.
Concreto banqueta #A8A49E. Metal cálido #7A6A58.

REGLAS DE CONTINUIDAD:
La misma cortina y fachada si aparece de noche o de día.
Sin letreros ni texto visible en ninguna variación.
Toma donde aparece: 01.

NEGATIVOS:
No letreros. No marcas. No texto. No graffiti.
No abandono. No precariedad. No decadencia.
No suciedad. No mugre. No óxido dominante. No humedad.
No número de local visible. No logo de tienda.
```

---

## L02 - Metro / Escaleras / Calle CDMX Anónima - v001

```text
TIPO DE FICHA: Ficha visual de locación.

SECCIONES:
1. Ficha de identidad de locación.
2. Vistas principales: escaleras de salida, pasillo subterráneo, calle exterior, plano hero cinematográfico.
3. Paleta de colores con HEX.
4. Materiales y texturas.
5. Luz y atmósfera.
6. Reglas de continuidad.
7. Negativos legales y visuales.

LOCACIÓN:
Nombre interno: Metro / escaleras / calle CDMX anónima.
Tipo: infraestructura urbana de tránsito.
Rol narrativo: ascenso urbano — el joven va hacia algo grande.
Emoción: movimiento, determinación, ciudad viva.

ARQUITECTURA Y MATERIALES:
Escaleras de salida tipo metro o paso subterráneo: concreto, loseta, barandal metálico.
La calle debe ser amplia, céntrica, viva y anónima — sin landmarks reconocibles.
Acera limpia. Árboles urbanos discretos. Edificios neutros al fondo.
No debe sentirse vacía ni postapocalíptica. Hay gente pero no multitud.

LUZ Y ATMÓSFERA:
Interior subterráneo: luz fría artificial con destello de luz natural al fondo de las escaleras.
Exterior: luz dorada de tarde sobre calle amplia. Ocaso/crepúsculo.

PALETA:
Concreto #8C8980. Loseta #A8A49E.
Barandal metálico #6E6E68. Golden hour calle #C99245.
Luz fría subterráneo #D8E0E4. Sombra azul #2D3A4A.
Rojo mochila P01 #DB3B2B (si aparece el personaje).

REGLAS DE CONTINUIDAD:
Misma arquitectura de escaleras en tomas 03 y 05.
Sin texto ni señalética legible en ninguna variación.
Tomas donde aparece: 03, 05.

NEGATIVOS:
No landmarks reconocibles. No Monumento a la Revolución.
No Ángel de la Independencia. No letras de metro del STC visibles.
No texto urbano legible. No tráfico dominante. No multitud densa.
No metro oficial con colores reales. No señalética del STC Metro.
```

---

## L04 - Mercado De Frutas Y Verduras - v001

```text
TIPO DE FICHA: Ficha visual de locación.

SECCIONES:
1. Ficha de identidad de locación.
2. Vistas principales: vista general del mercado, puesto de frutas/verduras, detalle de productos, plano hero cinematográfico.
3. Paleta de colores con HEX.
4. Materiales y texturas.
5. Luz y atmósfera.
6. Reglas de continuidad.
7. Negativos legales y visuales.

LOCACIÓN:
Nombre interno: Mercado de frutas y verduras.
Tipo: mercado interior o de calle, popular cuidado.
Rol narrativo: comercio vivo y táctil, cancha de la vida cotidiana.
Emoción: movimiento, precisión, transacción, vida plena.

ARQUITECTURA Y MATERIALES:
Puestos con cajas limpias de madera o plástico neutro.
Productos: plátano, aguacate, jitomate, cebolla, limón, chiles, cilantro, papa, zanahoria, calabacita, naranja, manzana, mango, nopales, tomatillo.
Manteles o superficies neutras. Terminal genérica de cobro sin logo.
Popular cuidado: no precarizado, no mercado de lujo, no tianguis desordenado.
Puede haber toldos o techo de lámina con luz filtrada.

LUZ Y ATMÓSFERA:
Luz natural filtrada, suave y cálida. Sombras abiertas.
Ambiente vivo pero no caótico. Gente al fondo desenfocada, en mood futbolero.

PALETA:
Verdes naturales #53694C. Rojo T1/acento #DB3B2B.
Cartón #A87545. Naranja fruta #C97C45.
Cream #F7F5F0. Piel media #C98963. Sombra fría #2D3A4A.

REGLAS DE CONTINUIDAD:
Misma distribución de puesto en toma 08. Sin texto ni marcas en ninguna superficie.
Toma donde aparece: 08.

NEGATIVOS:
No QR. No logos de terminal de pago. No marcas de cajas.
No cerveza ni alcohol visible. No texto legible en ninguna superficie.
No Walmart. No supermercado corporativo.
No suciedad. No fruta podrida. No basura. No charcos. No piso mugroso.
```

---

## L05 - Bodega / Taller Ecommerce - v001

```text
TIPO DE FICHA: Ficha visual de locación.

SECCIONES:
1. Ficha de identidad de locación.
2. Vistas principales: vista general de la bodega, mesa de empaque, detalle de materiales, plano hero cinematográfico.
3. Paleta de colores con HEX.
4. Materiales y texturas.
5. Luz y atmósfera.
6. Reglas de continuidad.
7. Negativos legales y visuales.

LOCACIÓN:
Nombre interno: Bodega / taller ecommerce.
Tipo: espacio operativo pequeño.
Rol narrativo: disciplina invisible del negocio, operación detrás del partido.
Emoción: precisión, silencio productivo, control.

ARQUITECTURA Y MATERIALES:
Mesa de empaque limpia con cajas de cartón, cinta y etiquetas genéricas sin texto.
Repisas ordenadas con cajas. Impresora térmica genérica sin marca.
Pared neutra o blanca. Piso limpio.
Espacio pequeño pero funcional y bien organizado.

LUZ Y ATMÓSFERA:
Luz fría funcional de techo o ventana lateral, clara y limpia.
Ambiente de trabajo concentrado, no fábrica industrial, no almacén oscuro.

PALETA:
Cartón #A87545. Cinta #D8D6D0.
Pared neutra #C8C4B8. Luz fría #D8E0E4.
Negro ropa #1B1B1B. Piel #C98963. Sombra #2D3A4A.

REGLAS DE CONTINUIDAD:
Misma bodega en toma 14. Sin texto ni marcas en ninguna superficie.
Toma donde aparece: 14.

NEGATIVOS:
No carriers reconocibles (DHL, FedEx, etc.). No marketplaces.
No etiquetas con texto legible. No marcas en ninguna caja.
No precariedad. No oscuridad. No desorden. No polvo. No mugre.
```

---

## L06 - Mesa Emprendedora Skincare / Joyería - v001

```text
TIPO DE FICHA: Ficha visual de locación.

SECCIONES:
1. Ficha de identidad de locación.
2. Vistas principales: mesa completa, detalle de productos, ángulo sobre hombro, plano hero cinematográfico.
3. Paleta de colores con HEX.
4. Materiales y texturas.
5. Luz y atmósfera.
6. Reglas de continuidad.
7. Negativos legales y visuales.

LOCACIÓN:
Nombre interno: Mesa emprendedora skincare / joyería.
Tipo: espacio de trabajo urbano contemporáneo.
Rol narrativo: control comercial, detalle, inventario activo.
Emoción: concentración, orden, crecimiento silencioso.

ARQUITECTURA Y MATERIALES:
Mesa de madera oscura o superficie neutra media.
Laptop con pantalla blanca, sin logo. Productos de skincare sin etiqueta.
Joyería pequeña y accesorios sin marca. Charola o libreta sin texto.
Pared lisa neutra o ventana urbana al fondo. Planta discreta no tropical opcional.
NO spa. NO tulum. NO lino. NO rattan. NO adobe.

LUZ Y ATMÓSFERA:
Luz natural de ventana urbana, tarde cálida-controlada.
Sombras suaves. No ring light. No luz de influencer.

PALETA:
Madera oscura #4A2E1A. Neutro cálido #D7C4AE.
Cream fondo #F7F5F0. Pantalla blanca #FAFAF7.
Rojo pulsera #DB3B2B. Sombra fría #2D3A4A. Negro texto #1B1B1B.

REGLAS DE CONTINUIDAD:
Misma mesa y entorno en toma 17. Laptop con pantalla siempre blanca.
Sin logos ni marcas en ninguna superficie.

NEGATIVOS:
No marcas cosméticas. No texto en envases. No logo de laptop.
No UI visible. No ring light. No tulum. No spa.
No beauty salon. No boutique de lujo. No set de influencer.
```

---

## L07 - Tienda De Sneakers - v001

```text
TIPO DE FICHA: Ficha visual de locación.

SECCIONES:
1. Ficha de identidad de locación.
2. Vistas principales: interior de tienda, repisa con sneakers, mostrador, plano hero cinematográfico.
3. Paleta de colores con HEX.
4. Materiales y texturas.
5. Luz y atmósfera.
6. Reglas de continuidad.
7. Negativos legales y visuales.

LOCACIÓN:
Nombre interno: Tienda de sneakers y accesorios deportivos.
Tipo: local urbano comercial pequeño-mediano.
Rol narrativo: comercio urbano joven, activación cotidiana.
Emoción: aspiracional urbano real, movimiento, cultura.

ARQUITECTURA Y MATERIALES:
Repisas acrílicas o de metal con sneakers genéricos organizados.
Gorras, playeras ficticias y accesorios deportivos sin logos.
Piso limpio. Mostrador simple sin marca.
Calle o vitrina al fondo, desenfocada.

LUZ Y ATMÓSFERA:
Luz cálida de tarde. Luz práctica interior combinada con luz natural de vitrina.
Ambiente vivo, no oscuro ni de bodega.

PALETA:
Rojo acento #DB3B2B. Charcoal #1B1B1B.
Acrílico #D8E0E4. Luz cálida #C99245.
Piso #A8A49E. Sombra #2D3A4A.

REGLAS DE CONTINUIDAD:
Misma tienda en tomas 18 y 19. Sin logos ni marcas en ninguna superficie.
Sneakers rojos #DB3B2B siempre sin logo.

NEGATIVOS:
No swoosh. No Adidas stripes. No Jordan logo. No Nike.
No marcas en ningún producto. No cajas reconocibles.
No logos deportivos. No texto en ninguna superficie.
```

---

## L08 - Restaurante Mexicano Contemporáneo - v001

```text
TIPO DE FICHA: Ficha visual de locación.

SECCIONES:
1. Ficha de identidad de locación.
2. Vistas principales: salón general, mesa con comida, detalle de ambiente, plano hero cinematográfico.
3. Paleta de colores con HEX.
4. Materiales y texturas.
5. Luz y atmósfera.
6. Reglas de continuidad.
7. Negativos legales y visuales.

LOCACIÓN:
Nombre interno: Restaurante mexicano contemporáneo CDMX.
Tipo: restaurante de barrio cuidado en Ciudad de México, aspiracional real.
Rol narrativo: tensión colectiva durante el partido y celebración final.
Emoción: expectativa, comunidad, ansiedad compartida, alegría contenida que explota.

ARQUITECTURA Y MATERIALES:
Restaurante contemporáneo de CDMX: paredes de concreto pulido limpio, piso de concreto o piedra neutra, mesas sencillas de madera o material oscuro sobrio, sillas sencillas, ventanales urbanos amplios, luz natural de tarde entrando desde un lateral, barra o cocina desenfocada al fondo.
Comida mexicana real sobre las mesas: tacos, guisados, totopos, salsas, agua fresca, tortillas, platos compartidos. Sin marcas.
Personas vistiendo textil deportivo genérico ficticio, siguiendo exactamente las especificaciones del personaje "Cliente T1 restaurante": playera casual deportiva de manga corta, cuello redondo, corte sencillo, sin cuello polo, sin escudo, sin número y sin logo.
El protagonista o cliente principal debe llevar playera roja T1 #DB3B2B con UNA sola línea blanca vertical en cada hombro: una línea en hombro izquierdo y una línea en hombro derecho, colocada sobre la costura superior del hombro, desde cerca del cuello hacia el inicio de la manga. No debe haber doble línea, triple línea, franjas laterales ni stripes de marca.
Otros clientes pueden usar variaciones coherentes del mismo sistema: verde #194D36 con una línea blanca en cada hombro, blanco #F7F5F0 con una línea roja #DB3B2B o verde #194D36 en cada hombro. Todos sin logos, sin escudos, sin números.
Decoración mínima: algunas macetas color rojo T1 #DB3B2B con plantas discretas no tropicales; arte abstracto en pared con trazos negros sobrios, sin texto ni símbolos reconocibles.
No cantina. No bar. No antro. No palapa. No tulum. No boho playero. No restaurante rústico. No ladrillo expuesto dominante.

DISTRIBUCIÓN ESPACIAL:
El restaurante debe sentirse como un espacio real con varias mesas y varios grupos, no como una fila de extras posando.
Las mesas deben estar orientadas en diferentes ángulos: unas de frente, otras en diagonal, otras laterales.
Las personas NO deben mirar todas hacia la misma dirección.
Debe haber varios puntos de atención: televisiones fuera de cuadro en distintos muros, una pantalla al fondo desenfocada, una televisión lateral invisible para cámara, gente mirando a izquierda, derecha, arriba y hacia el fondo.
Algunos clientes ven el partido, otros miran su celular, otros se tapan la boca, otros están volteando hacia otra mesa, otros reaccionan al audio sin mirar directo.
La composición puede ser un plano cinematográfico de media distancia, con primer plano ligeramente desenfocado de comida y vasos, grupo principal en foco medio, y mesas/fans desenfocados al fondo.
No hacer una composición teatral con todos los rostros alineados hacia cámara o hacia el mismo televisor.

LUZ Y ATMÓSFERA:
Luz natural de tarde de partido, suave y lateral, entrando por ventanales. No debe sentirse como luz amarilla de lámpara ni restaurante nocturno.
Temperatura neutra-cálida controlada: tarde real en CDMX, con sombras abiertas y contraste cinematográfico moderado.
Ambiente vivo, familiar, aspiracional real, con tensión de partido. Puede ser un poco cinematográfico y contrastado, pero nunca lúgubre, sucio ni demasiado cálido.
Profundidad de campo natural: no todo necesita estar perfectamente nítido; permitir fondo suave y rostros secundarios desenfocados para que se sienta fotografía real.

PALETA:
Concreto pulido #B8B4AA.
Concreto sombra #8C8980.
Negro trazos arte #1B1B1B.
Rojo T1 macetas / jersey #DB3B2B.
Madera oscura sobria #5A4032.
Maíz / tortilla #DDBB75.
Verdes comida #53694C.
Sombra fría #2D3A4A.
Luz natural tarde #D8C7A3.

REGLAS DE CONTINUIDAD:
El mismo restaurante en tomas 20, 22, 24, 31, 32.
Textil deportivo genérico: playeras casuales deportivas de manga corta y cuello redondo, siguiendo exactamente el lenguaje del personaje "Cliente T1 restaurante". Protagonista en rojo T1 #DB3B2B con una sola línea blanca vertical en cada hombro, sobre la costura superior. Variaciones secundarias: verde #194D36 con línea blanca, blanco #F7F5F0 con línea roja o verde.
Sin logos, escudos ni marcas en ninguna variación.
Distribución de miradas siempre natural y variada, con varios puntos de televisión fuera de cuadro.

NEGATIVOS:
No alcohol. No cerveza. No cervezas de marca.
No pantallas con UI visible. No logos. No marcas en menús.
No Tulum. No palapa. No barro excesivo.
No decoración turística. No cantina oscura.
No ladrillo expuesto dominante.
No luz amarilla nocturna.
No lámparas cálidas como fuente principal.
No restaurante rústico.
No uniformes oficiales.
No jerseys profesionales.
No playeras con doble línea.
No playeras con triple línea.
No franjas tipo Adidas.
No suciedad. No grasa visible. No mesas pegajosas. No ambiente lúgubre.
No todos mirando hacia la misma dirección.
No extras alineados como coro.
No pose publicitaria.
No restaurante vacío.
No televisor enorme protagonista.
No pantallas con contenido legible.
```

---

## L09 - México Nocturno / Espacio - v001

```text
TIPO DE FICHA: Ficha visual de locación abstracta / cierre épico.

SECCIONES:
1. Ficha de identidad de locación.
2. Vistas principales: vista aérea de México nocturno, atmósfera terrestre, Tierra desde espacio, plano hero cinematográfico.
3. Paleta de colores con HEX.
4. Luz y atmósfera.
5. Reglas de continuidad.
6. Negativos legales y visuales.

LOCACIÓN:
Nombre interno: México nocturno / espacio.
Tipo: locación abstracta de cierre épico.
Rol narrativo: escala país, sistema completo, todos conectados.
Emoción: poético, épico tranquilo, grandeza sin grandilocuencia.

VISTAS REQUERIDAS:
Vista 1: México nocturno desde arriba — luces urbanas formando redes, sin mapa político.
Vista 2: Atmósfera terrestre con haze azul en el horizonte.
Vista 3: Tierra vista desde espacio exterior — planeta completo centrado, nocturno, con luces cálidas. NO media luna.
Vista 4: Plano hero cinematográfico — fusión poética de ciudad y cosmos.

LUZ Y ATMÓSFERA:
Espacio profundo oscuro. Luces urbanas cálidas #DDBB75 como red de vida.
Atmósfera azul suave en horizonte. Sin saturación excesiva. Poético, no de videojuego.

PALETA:
Espacio profundo #07111F. Luz urbana cálida #DDBB75.
Azul atmósfera #2D3A4A. Blanco suave estrellas #F7F5F0.
Verde oscuro nocturno #1A2E1A.

REGLAS DE CONTINUIDAD:
Toma 35: México nocturno desde arriba, luces sin mapa político.
Toma 36: Tierra como esfera completa centrada. NO media luna. NO mapa político literal.

NEGATIVOS:
No mapa político literal. No labels de países o ciudades.
No fronteras marcadas. No media luna en toma 36.
No banderas. No símbolos nacionales. No texto. No Google Earth look.
No videojuego. No CGI plástico. No ilustración.
No Estadio Azteca visible. No monumentos reconocibles.
```
