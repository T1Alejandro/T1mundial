---
title: "v08 Shot Production Pack"
doc_type: "production-pack"
status: "active-draft"
owner: "Arturo / Parco"
reviewers: ["Creative", "Post", "Legal"]
version: "0.1"
last_updated: "2026-05-14"
language: "es"
audience: ["creative", "production", "post", "ai-video"]
tags: ["v08", "shot-production", "motion-tests", "figma", "ui-post"]
source_of_truth: "local-project"
confidence: "high"
related_docs:
  - "../HANDS-UP.md"
  - "../03_creative/v02_v08_commerce_athlete/prompts/storyboard-rack-16-v008-self-contained.md"
  - "../03_creative/v02_v08_commerce_athlete/briefing/Master Production Biblia.md"
  - "../03_creative/v02_v08_commerce_athlete/script/vo-script-v08-final.md"
  - "../07_assets/figma/"
---

# v08 Shot Production Pack

## Objetivo

Convertir el rack/storyboard 4x4 aprobado en unidades animables por toma.

La meta de esta fase no es regenerar el spot completo. La meta es producir cada toma como un experimento controlado:

`frame base aprobado -> UI/post si aplica -> motion test corto -> QA -> version aprobada`

La consistencia se dirige desde los frames individuales en `07_assets/figma/`, no desde un prompt largo ni desde una generacion completa de secuencia.

## Regla Maestra

- Un shot = un paquete.
- Un paquete = frame base, movimiento permitido, bloqueos, UI/post, negativos y criterio de aprobacion.
- No animar toda la secuencia de golpe.
- No pedir UI final a modelos generativos.
- No permitir que motion cambie rostro, manos, locacion, encuadre, pantalla o limpieza visual.
- Si una toma conecta con otra, usar el ultimo frame aprobado como referencia secundaria de la siguiente.

## Assets Base

| Shot | Frame base |
|---:|---|
| 01 | `07_assets/figma/ChatGPT-Image-May-14,-2026,-02_51_43-PM_01.png` |
| 02 | `07_assets/figma/ChatGPT-Image-May-14,-2026,-02_51_43-PM_02.png` |
| 03 | `07_assets/figma/ChatGPT-Image-May-14,-2026,-02_51_43-PM_03.png` |
| 04 | `07_assets/figma/ChatGPT-Image-May-14,-2026,-02_51_43-PM_04.png` |
| 05 | `07_assets/figma/ChatGPT-Image-May-14,-2026,-02_51_43-PM_05.png` |
| 06 | `07_assets/figma/ChatGPT-Image-May-14,-2026,-02_51_43-PM_06.png` |
| 07 | `07_assets/figma/ChatGPT-Image-May-14,-2026,-02_51_43-PM_07.png` |
| 08 | `07_assets/figma/ChatGPT-Image-May-14,-2026,-02_51_43-PM_08.png` |
| 09 | `07_assets/figma/ChatGPT-Image-May-14,-2026,-02_51_43-PM_09.png` |
| 10 | `07_assets/figma/ChatGPT-Image-May-14,-2026,-02_51_43-PM_10.png` |
| 11 | `07_assets/figma/ChatGPT-Image-May-14,-2026,-02_51_43-PM_11.png` |
| 12 | `07_assets/figma/ChatGPT-Image-May-14,-2026,-02_51_43-PM_12.png` |
| 13 | `07_assets/figma/ChatGPT-Image-May-14,-2026,-02_51_43-PM_13.png` |
| 14 | `07_assets/figma/ChatGPT-Image-May-14,-2026,-02_51_43-PM_14.png` |
| 15 | `07_assets/figma/ChatGPT-Image-May-14,-2026,-02_51_43-PM_15.png` |
| 16 | `07_assets/figma/ChatGPT-Image-May-14,-2026,-02_51_43-PM_16.png` |

## Orden Recomendado De Produccion

1. **Bloque A / Don Rafael / Shots 01-03**
   Define tono, apertura, ritual, terminal y lenguaje de camara.

2. **Bloque B / UI Critica / Shots 08-09 y 11**
   Primero montar UI real T1 en stills. Luego animar con pantallas ya resueltas o mantener motion de camara sin tocar pantalla.

3. **Bloque C / Cierre / Shots 15-16**
   Validar red nacional, espacio negativo, logo/slogan en post y tono final.

4. **Bloque D / Comercio y Manos / Shots 04-07, 10, 12-14**
   Probar manos, terminales, empaque, dinero abstracto, fruta, caja y continuidad de gestos.

## Shot Map Operativo

| Shot | Descripcion | Motion permitido | Bloqueos de continuidad | UI/Post | Estado |
|---:|---|---|---|---|---|
| 01 | Don Rafael abre cortina metalica al amanecer. | Push-in lento, cortina sube apenas, luz respira, polvo sutil. | No cambiar tienda, rostro/cuerpo, cortina, paleta ni limpieza. | No. | Pendiente motion |
| 02 | Don Rafael entra a tienda desde interior. | Dolly muy lento hacia adentro, paso contenido, contraluz estable. | Mismo Don Rafael, misma tienda, mismo amanecer. | No. | Pendiente motion |
| 03 | Manos de Don Rafael preparan mostrador y terminal. | Macro controlado, manos acomodan objetos, rack focus suave. | Manos anatomicas, terminal lisa, pano rojo, cero UI inventada. | Si: terminal puede requerir UI/post o pantalla lisa. | Pendiente UI/motion |
| 04 | Dona Carmen cobra en tianguis. | Dolly sutil, gestos de cobro, cliente desenfocado, ambiente vivo. | Misma Dona Carmen, tianguis limpio, frutas ordenadas, terminal lisa. | Si: terminal/pago. | Pendiente UI/motion |
| 05 | Dona Carmen entrega bolsa con fruta. | Movimiento de manos, entrega lenta, sonrisa contenida. | Mismo puesto, fruta fresca, cero etiquetas con texto. | No o minimo. | Pendiente motion |
| 06 | Miguel empaca pedidos en bodega/taller DTC. | Camara lateral suave, manos trabajan, cajas se acomodan. | Bodega limpia, Miguel consistente, cajas kraft nuevas. | No. | Pendiente motion |
| 07 | Manos de Miguel cierran caja. | Macro de cinta, presion, gesto preciso, rack focus. | Cinta lisa, etiqueta sin texto, manos correctas. | Posible etiqueta/post si se decide. | Pendiente motion |
| 08 | Sofia analiza laptop. | Push-in o parallax leve, luz en rostro, concentracion. | Misma Sofia, workspace mexicano, laptop estable. | Si: laptop/dashboard real T1 primero. | Pendiente UI/post |
| 09 | Manos de Sofia tipeando. | Teclas y manos con movimiento minimo, reflejo suave. | Manos correctas, teclado estable, pantalla no debe inventar UI. | Si: reflejo/pantalla T1 si aparece. | Pendiente UI/post |
| 10 | Lupita en tienda de provincia. | Camara lenta suave, gesto con cliente o mirada de control. | Misma Lupita, tienda limpia, no folclor turistico. | No o minimo. | Pendiente motion |
| 11 | Lupita revisa tablet. | Movimiento sutil de tablet/manos, push-in al rostro/tablet. | Tablet estable, piel madura real, productos limpios. | Si: tablet/dashboard real T1 primero. | Pendiente UI/post |
| 12 | Macro manos diversas con dinero abstracto. | Montaje o movimiento de manos, conteo sutil, luz tactil. | Billetes abstractos sin numeros/texto/retratos/escudos. | No. | Pendiente motion |
| 13 | Macro caja kraft, etiqueta y cinta roja. | Cinta/etiqueta/manos, macro preciso. | Etiqueta sin texto, caja nueva, cero logos inventados. | Posible etiqueta/post. | Pendiente motion |
| 14 | Macro fruta, libreta, terminal y manos. | Gestos multiples contenidos, rack focus entre objetos. | Terminal lisa, libreta sin texto legible, fruta fresca. | Si: terminal si toma protagonismo. | Pendiente UI/motion |
| 15 | Mexico nocturno como red de negocios. | Zoom out lento, puntos dorados/rojos pulsan sutilmente. | No mapa politico literal, no labels, no bandera, no interfaz. | Posible comp/post de red T1. | Pendiente motion/post |
| 16 | Tierra / Mexico luminoso con espacio negativo. | Drift lento, respiracion de luces, espacio para cierre. | No texto/logo generado; slogan y logo reales van en post. | Si: logo/slogan en post. | Pendiente post/motion |

## Template De Motion Prompt Por Toma

```text
Usa la imagen adjunta como referencia visual estricta y primer frame.
No redisenes encuadre, personaje, locacion, props, paleta ni luz.
Anima solo lo necesario para convertir este still en un clip cinematografico de 3-5 segundos.

MOVIMIENTO:
[describir movimiento fisico/camara especifico]

BLOQUEOS:
[rostro/personaje/locacion/props/pantalla que no deben cambiar]

CONTINUIDAD:
[si aplica, usar ultimo frame aprobado de toma anterior como referencia secundaria]

NEGATIVO:
no text, no captions, no labels, no logos, no brands, no UI invented, no dashboard invented, no app interface, no QR, no camera metadata, no sports, no soccer, no football, no futbol, no ball, no stadium, no jersey, no FIFA, no World Cup, no flags, no famous landmarks, no distorted hands, no malformed faces, no plastic skin, no dirty market, no clutter, no trash, no grime, no morphing, no fade, no dissolve, no hard cut, no hyperactive motion.
```

## UI/Post Workflow

Para shots 03, 04, 08, 09, 11, 14, 15 y 16:

1. Duplicar still base.
2. Montar interfaz real T1 en ChatGPT/post si la pantalla es protagonista.
3. Mantener pantalla lisa si la UI no sera legible en corte.
4. Animar despues del montaje si la UI debe moverse con la camara.
5. Si el modelo de video deforma la UI, volver a pantalla lisa y componer UI en After Effects/Premiere.

Regla: la IA de video nunca debe inventar dashboard, logo, textos, numeros, QR ni interfaz.

## Criterio De Aprobacion Por Shot

Un motion test se aprueba si:

1. Respeta el frame base.
2. Mantiene personaje, edad, rostro, manos y vestuario.
3. Mantiene locacion, paleta, limpieza y direccion de arte.
4. No inventa texto, marca, logo, UI, QR o dashboard.
5. No introduce futbol, Mundial, estadio, balon, jersey, bandera ni lectura de evento masivo.
6. El movimiento es fisico, lento, cinematografico y util para el corte.
7. No rompe anatomia, manos, pantallas, objetos ni perspectiva.

## Siguiente Accion

Empezar con el Bloque A:

1. Crear prompt final de motion para Shot 01.
2. Generar 1-2 tests baratos.
3. Seleccionar ganador.
4. Extraer ultimo frame si Shot 02 debe heredar continuidad.
5. Repetir con Shots 02 y 03.

