---
title: "Higgsfield Agent v08 Context Pack"
doc_type: "agent-context"
status: "active-draft"
owner: "Arturo / Parco"
reviewers: ["Creative", "Production", "Branding", "Legal"]
version: "0.1"
last_updated: "2026-05-13"
language: "es"
audience: ["higgsfield", "ai-agent", "creative", "production"]
tags: ["v08", "higgsfield", "agent", "context-pack", "commerce-athlete", "character-sheet", "14-shots"]
source_of_truth:
  - "../../../00_admin/source-materials/T1_mundial_v08_Briefing_Alejandro.docx"
  - "../../../00_admin/source-materials/T1_mundial_v08_Anexo_Branding.docx"
  - "higgsfield-character-location-sheet-v008.md"
  - "chatgpt-master-rack-14-v008-commerce-athlete.md"
  - "lora-realism-prompt-system-v001.md"
confidence: "high"
---

# Higgsfield Agent v08 Context Pack

Este documento es para pegarlo en el agente de Higgsfield cuando ya esta generando character sheets, locaciones o keyframes del spot v08.

## Bloque 00 — Mensaje Corto Para El Agente

```text
Contexto de proyecto:
Estoy produciendo T1 v08, hero film 60-90s para YouTube. El concepto oficial es "El atleta del comercio mexicano". El protagonista ya NO es futbolista, NO es estudiante y NO hay estadio, balon, cancha, arbitro ni uniforme deportivo. La energia atletica vive en el comercio mexicano: abrir tienda, cobrar, empacar, analizar, entregar, vender y conectar negocios.

Necesito que trabajes desde esta direccion oficial v08. Ignora versiones anteriores de futbol, estadio, rack escolar, anti-ambush escolar o 36 tomas. La version actual son 5 personajes principales, 6 locaciones base, 14 tomas finales y un cierre T1 en postproduccion.

Regla clave:
No generes logos T1, textos T1, UI final, dashboards legibles, stickers con palabras ni puntos/cruces de tracking. Las pantallas y superficies deben quedar lisas para post: blanco suave, gris claro, negro mate o reflejo optico real. El rojo T1 #DA3B2B solo aparece como acento limpio: pulsera roja, vivo, costura, cinta lisa, etiqueta sin texto, franja roja lisa, cuaderno, taza, cutter, clip, arete o prop rojo.
```

## Bloque 01 — Tesis Creativa

```text
TESIS CREATIVA:
El comerciante mexicano es el atleta de su propio negocio.

Cada mexicano que vende entrena cada manana cuando abre. Estudia su mercado como otros estudian al rival. Sabe que cada movimiento cuenta. La pieza debe sentirse epica, precisa y emocional, pero sin deporte explicito.

La camara, la luz y el montaje deben tratar a los comerciantes como atletas de elite: camara lenta heroica, angulos bajos de dignidad, macro precision de manos, respiracion, concentracion, timing, disciplina, ritual y control.

No hay futbol. No hay Mundial. No hay estadio. No hay balon. No hay cancha. No hay arbitro. No hay porteria. No hay estudiantes jugando. No hay lectura de evento masivo.
```

## Bloque 02 — Voice Over Final

No modificar el VO. Usarlo solo para entender ritmo emocional y timing.

```text
00:00 - 00:05
(silencio. Solo ambiente y musica suave.)

00:05 - 00:10
Hay dias que no son como los demas.

00:10 - 00:15
Dias donde uno se prepara para algo grande.

00:15 - 00:22
Donde cada movimiento cuenta. Donde no se falla en los detalles.

00:22 - 00:28
Donde el equipo es todo.

00:28 - 00:35
Hay quien lo entrena toda la vida. Hay quien lo entrena cada manana, cuando abre.

00:35 - 00:42
Hay quien estudia al rival. Hay quien estudia el mercado.

00:42 - 00:50
Hay quien sabe que el tiempo se mueve rapido. Y hay quien sabe que el dinero tambien.

00:50 - 00:58
Hoy todo Mexico se prepara. Millones de manos. Millones de suenos.

00:58 - 01:05
Mismo pais. Mismo equipo.

01:05 - 01:10
(silencio total. 5 segundos.)

01:10 - 01:13
Todo Mexico es uno.

01:13 - 01:16
Todo en uno.

01:16 - 01:18
T1.

01:18 - 01:25
(silencio. Logo en pantalla. Fade.)
```

## Bloque 03 — Look Global

```text
LOOK GLOBAL:
Cine independiente mexicano contemporaneo. Sobrio, elegante, humano, aspiracional-real. Mas cine autoral que publicidad comercial. No look corporativo. No stock photo. Todo debe sentirse premium-real, cinematografico, silencioso y preciso.

Fotografia suave sin HDR agresivo, contraste medio, negros ligeramente levantados, altas luces con roll-off analogico, grano fino cinematografico, textura real, lente 35mm/50mm, profundidad de campo media a shallow, luz natural primero y luz practica despues.

El mundo debe estar limpio, nuevo, cuidado, digno y en excelente estado. Realismo si, suciedad no. Textura si, deterioro no.
```

## Bloque 04 — Paleta Y Branding

```text
PALETA:
Mundo del comerciante: dorado amanecer, ambar suave, terracota suave, ocres nobles, marrones calidos, blancos cremosos, negro suave.

Tecnologia / marca para post: rojo T1 #DA3B2B, blanco limpio, grises limpios, negro mate y dorado tactico muy discreto.

Evitar verde dominante, verde escolar, verde bosque dominante, combinacion verde+blanco+rojo, azul+blanco+rojo, naranja excesivo, sepia, beige sucio, cafe decadente, tierra, polvo pesado o look lugubre.

BRANDING PARA POST:
No generar logos T1 con AI.
No generar UI final con AI.
No generar textos T1.
No generar dashboards legibles.
No generar stickers con palabras.
No generar puntos/cruces de tracking.

Pantallas y superficies: blanco suave, gris claro, negro mate o reflejo optico real; lisas, limpias y listas para composicion posterior.

Rojo T1 #DA3B2B: usar solo como acento natural y controlado en pulsera, vivo, costura, ribete, cinta lisa, etiqueta sin texto, franja roja lisa, cuaderno rojo, taza con detalle rojo liso, cutter rojo, clip rojo, arete rojo o prop rojo.
```

## Bloque 05 — Cast Principal Oficial

```text
PERSONAJES SOUL CAST:

Don Rafael:
Hombre mexicano 55-60, comerciante del Centro Historico, manos trabajadas, pelo entrecano, mirada digna. Aparece en tomas 01, 02, 03 y puede sentirse en cierre.

Dona Carmen:
Mujer mexicana 45, comerciante de tianguis, pelo recogido, delantal, sonrisa serena, presencia confiable. Aparece en tomas 04 y 05.

Miguel:
Hombre mexicano 32, fisico delgado y atletico, empacador DTC, concentrado, manos precisas. Aparece en tomas 06 y 07.

Sofia:
Mujer mexicana 32, founder DTC, pelo negro lacio, mirada analitica, estetica moderna. Aparece en tomas 08 y 09.

Lupita:
Mujer mexicana 50, duena de tienda de provincia, calidez maternal, elegancia digna, mirada segura. Aparece en tomas 10 y 11.

Manos diversas:
Comerciantes mexicanos reales y dignos de distintas edades y tonos de piel. Aparecen en toma 12.

Nadie debe parecer celebridad, figura publica ni atleta real.
```

## Bloque 06 — Locaciones Base

```text
LOCACIONES BASE:

01. Tienda pequena Centro Historico / Don Rafael:
Tienda mexicana limpia al amanecer. Cortina metalica en excelente estado, mostrador cuidado, productos ordenados, piso impecable, luz dorada controlada entrando desde la calle. Arquitectura mexicana generica, sin monumentos ni marcas reales.

02. Tianguis / Dona Carmen:
Mercado mexicano limpio, digno, vibrante pero sobrio. Puesto de frutas frescas, toldo cuidado, cajas ordenadas, gente cotidiana desenfocada. Paleta calida con mangos, papayas, jitomates, platanos, mandarinas. Evitar verde dominante. Sin QR, sin letreros legibles, sin marcas.

03. Bodega / taller DTC / Miguel:
Espacio de empaque limpio, organizado, eficiente, premium-real. Mesas de trabajo, cajas kraft nuevas, rollos de cinta roja lisa, etiquetas limpias sin texto, pantalla pequena blanca/gris lisa, estanterias ordenadas. Cero desorden, cero deterioro.

04. Workspace moderno / Sofia:
Espacio contemporaneo tipo Condesa, limpio y aspiracional. Laptop con pantalla lisa blanca/gris clara, productos de emprendimiento, plantas, taza blanca con detalle rojo liso, cuaderno rojo liso, pluma con clip rojo, luz natural fria elegante. Mexicano urbano moderno, no corporativo, no Silicon Valley generico.

05. Tienda de provincia / Lupita:
Interior cuidado con productos artesanales mexicanos contemporaneos, madera limpia, ceramica, textiles sobrios, mostrador ordenado, tablet lisa visible, acento rojo liso cerca de caja o etiqueta sin texto. Calle colonial generica desenfocada por ventana, sin monumentos reconocibles.

06. Mexico nocturno T1:
Vista aerea poetica de Mexico sugerido por luces, no mapa literal. Miles de puntos dorados calidos como negocios activos, con algunos puntos rojo T1 #DA3B2B y lineas finas rojas muy sutiles conectando nodos para sugerir ecosistema comercial. Sin logos, sin texto, sin fronteras politicas, sin labels, sin bandera, sin interfaz satelital.
```

## Bloque 07 — Shot List Oficial 14 Tomas

```text
SHOT LIST OFICIAL V08:

01. Don Rafael abre cortina metalica al amanecer.
Duracion aproximada: 0:00-0:05.
Personaje: Don Rafael.
Funcion: ritual de apertura, dignidad, inicio del dia.

02. Don Rafael entra a su tienda.
Duracion aproximada: 0:05-0:08.
Personaje: Don Rafael.
Funcion: paso firme hacia su arena cotidiana.

03. Macro de manos preparando mostrador, caja y terminal lisa.
Duracion aproximada: 0:08-0:12.
Personaje: manos de Don Rafael.
Funcion: precision ritual, primer gesto operativo.

04. Dona Carmen cobra en tianguis con terminal lisa.
Duracion aproximada: 0:12-0:17.
Personaje: Dona Carmen.
Funcion: cobro como gesto de precision y control.

05. Dona Carmen entrega producto.
Duracion aproximada: 0:17-0:20.
Personaje: manos de Dona Carmen.
Funcion: servicio filmado como gesto perfecto.

06. Miguel empaca pedidos ecommerce con disciplina.
Duracion aproximada: 0:20-0:25.
Personaje: Miguel.
Funcion: fuerza fisica, ritmo, disciplina.

07. Macro manos cerrando caja con cinta lisa.
Duracion aproximada: 0:25-0:28.
Personaje: manos de Miguel.
Funcion: ultimo detalle antes de salir.

08. Sofia analiza laptop con pantalla lisa.
Duracion aproximada: 0:28-0:33.
Personaje: Sofia.
Funcion: estrategia, lectura del mercado, control mental.

09. Manos de Sofia tipeando / reflejo suave de pantalla lisa.
Duracion aproximada: 0:33-0:36.
Personaje: manos / ojos de Sofia.
Funcion: decision, velocidad, precision.

10. Lupita en tienda de provincia.
Duracion aproximada: 0:36-0:41.
Personaje: Lupita.
Funcion: comercio regional, calidez, escala humana.

11. Lupita revisa tablet con pantalla lisa.
Duracion aproximada: 0:41-0:44.
Personaje: Lupita.
Funcion: control multicanal sugerido, sin UI generada.

12. Montaje rapido de manos diversas.
Duracion aproximada: 0:44-0:55.
Personajes: multiples comerciantes.
Funcion: millones de manos, precision colectiva.

13. Zoom out Mexico iluminado.
Duracion aproximada: 0:55-1:05.
Personaje: N/A.
Funcion: red nacional de negocios, pais conectado.

14. Cierre con slogan y logo en post.
Duracion aproximada: 1:05-1:25.
Personaje: marca / humanidad sugerida.
Funcion: cierre emocional y de marca, sin texto generado por AI.
```

## Bloque 08 — Prompt Maestro Para Character + Location Sheet

Usar este si el agente necesita recordar el sheet 6x2.

```text
Crea UNA imagen tipo character + location sheet cinematografico para T1 v08: "El atleta del comercio mexicano".

Formato obligatorio: una sola imagen horizontal grande en cuadricula exacta de 6 columnas x 2 filas = 12 frames totales. No mas, no menos. Todos los frames deben tener el mismo tamano y proporcion 16:9. Lectura de izquierda a derecha y de arriba hacia abajo. Fila superior: 5 personajes principales + manos diversas. Fila inferior: 6 locaciones base. No usar collage irregular, layout libre ni mosaico variable. Separacion minima y uniforme entre frames. No pongas texto, nombres, numeros, labels, captions, marcas de agua, logos ni UI final.

Fila 1:
01 Don Rafael. Hombre mexicano 55-60, comerciante Centro Historico, pelo entrecano, manos trabajadas, mirada digna, tienda pequena limpia, luz de amanecer.
02 Dona Carmen. Mujer mexicana 45, comerciante de tianguis, pelo recogido, delantal limpio con vivo rojo, sonrisa serena, frutas frescas.
03 Miguel. Hombre mexicano 32, fisico delgado atletico, empacador DTC, bodega limpia, cajas kraft nuevas, cinta roja lisa.
04 Sofia. Mujer mexicana 32, founder DTC, pelo negro lacio, mirada analitica, workspace limpio tipo Condesa, laptop lisa.
05 Lupita. Mujer mexicana 50, duena de tienda de provincia, calidez maternal, elegancia digna, textiles/ceramica/madera limpia, tablet lisa.
06 Manos diversas. Manos mexicanas reales y dignas, distintas edades y tonos de piel, acciones de comercio: contar dinero abstracto, sellar caja, pegar etiqueta sin texto, tocar terminal lisa, doblar prenda, escribir nota sin texto legible, firmar entrega sin texto legible.

Fila 2:
07 Tienda pequena Centro Historico limpia al amanecer.
08 Tianguis limpio, digno, vibrante pero sobrio.
09 Bodega/taller DTC limpio, organizado, eficiente.
10 Workspace moderno tipo Condesa, limpio y aspiracional.
11 Tienda de provincia calida, artesanal contemporanea, sin folclor turistico.
12 Mexico nocturno T1 sugerido por luces de negocios, no mapa literal.
```

## Bloque 09 — Realismo Premium

```text
REALISMO PREMIUM:
Preservar identidad, edad, gesto, composicion y color grading original. Anadir microestructura autentica: poros no uniformes, lineas finas, vello fino, variacion tonal, textura de labios, cejas, pestanas, manos con pliegues, unas naturales, piel con zonas mate y brillo real. Materiales limpios y tactiles: metal limpio, carton nuevo, fruta fresca, madera noble, ceramica, tela con fibras, pantallas lisas con reflejo optico. Cero piel plastica, cero beauty retouch, cero nitidez digital, cero suciedad, cero deterioro. Realismo cinematografico premium, 35mm/50mm, grano fino organico, highlights con roll-off analogico.
```

## Bloque 10 — Global Negative Prompt

```text
no text, no captions, no subtitles, no shot numbers, no labels, no titles, no grid labels, no panel borders, no watermarks, no logos, no T1 logo generated by AI, no fake T1 logo, no random logos, no brands, no trademarks, no competitor logos, no final UI, no readable dashboard, no app interface, no generated typography, no sticker text, no tracking dots, no tracking crosses, no artificial markers, no Mercado Pago, no Mercado Libre, no Clip, no Stripe, no PayPal, no Shopify, no Amazon, no Visa, no Mastercard, no FedEx, no DHL, no UPS, no Estafeta, no Coca-Cola, no Telcel, no Bimbo, no soccer, no football, no futbol, no ball, no balon, no stadium, no estadio, no cancha, no goal, no net, no referee, no player, no jersey, no sports uniform, no cleats, no trophy, no fans, no crowd, no FIFA, no World Cup, no Mundial, no Copa del Mundo, no Mexico 2026, no national team, no flags, no patriotic styling, no green-white-red dominant palette, no blue-white-red dominant palette, no famous landmarks, no real software UI, no unreadable AI text, no readable QR code, no dollars, no euros, no foreign currency, no exact Mexican bills, no readable denominations, no official banknote portraits, no official seals, no poverty porn, no grime, no trash, no dirt, no dust heavy, no stains, no old broken objects, no peeling paint, no rust, no humidity damage, no cracked walls, no cracked floors, no worn-out market stall, no deteriorated shutters, no messy cables, no clutter, no abandoned look, no decay, no dirty floors, no damaged cardboard, no stained clothing, no airbrushed skin, no smooth plastic skin, no waxy skin, no distorted hands, no extra fingers, no malformed faces, no stock photo look
```

## Bloque 11 — Instruccion Operativa Para Higgsfield Agent

```text
Tarea para ti como agente de Higgsfield:

1. Usa el contexto v08 anterior como biblia creativa.
2. No uses versiones anteriores del proyecto.
3. Primero termina character + location sheet 6x2.
4. Mantén consistencia de los 5 personajes principales.
5. Mantén todas las locaciones ultra limpias y sin deterioro.
6. Mantén pantallas lisas para post, sin UI ni logos.
7. Aplica realismo premium en piel, manos y materiales.
8. Despues del sheet, prepara prompts separados por las 14 tomas, cada uno con:
   - personaje,
   - locacion,
   - accion,
   - camara,
   - luz,
   - continuidad,
   - negativos especificos.
9. No generes nada relacionado con futbol, Mundial, estadio, cancha, balon, escuela o evento masivo.
10. Antes de producir, dame una propuesta de estructura de prompts separada por toma para aprobarla.
```
