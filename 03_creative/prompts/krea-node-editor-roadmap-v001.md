# Krea Node Editor Roadmap v001

Documento puente basado en `storyboard-grid-prompt-v001.md`.

Este archivo no reemplaza el prompt maestro. Su funcion es traducir el storyboard completo a una estructura pensada para trabajar en Krea Node Editor, manteniendo continuidad visual, control de estilo y pantallas genericas T1 para composicion posterior.

## Objetivo

Construir un patch de trabajo que permita generar keyframes consistentes para las 34 tomas del storyboard, sin pedir que el modelo resuelva UX final, texto, logos, marcas o interfaces definitivas.

Las pantallas de smartphone, smartwatch, tablet y laptop deben salir como pantallas genericas T1, creibles dentro de la toma, pero listas para foto-video montaje o ajuste posterior.

## Principio De Trabajo

* El storyboard maestro define narrativa, look, restricciones y continuidad.
* Krea Node Editor debe separar estilo global, continuidad de personajes/vestuario, prompts por toma, negativos globales y referencias visuales.
* Cada toma debe poder generarse como keyframe individual 16:9.
* La hoja de contactos completa, es decir la cuadricula con todos los keyframes juntos, debe funcionar solo como referencia de lectura general, no como output final de produccion.
* Este documento no debe pegarse completo como un solo prompt en Krea. Debe usarse como mapa para construir nodos o prompts cortos por bloque.

## Patch General Propuesto

1. Global Style Node
    * Cine autoral suave.
    * Negros levantados.
    * Highlights con roll-off analogico.
    * Grano fino.
    * Menos contraste, mas atmosfera.
    * Luz natural primero, luz practica despues.
    * Sensacion nostalgica contemporanea.

2. Color Continuity Node
    * Verde natural no saturado.
    * Amarillo calido / golden hour.
    * Sombras ligeramente frias.
    * Rojo acento `#DA3B2B`.
    * Verde oscuro y dorado calido solo para superficies digitales abstractas.

3. Wardrobe Continuity Node
    * Equipo principal: playera verde con dos lineas blancas, short blanco, calcetas rojas `#DA3B2B`.
    * Equipo contrario: playera blanca, short azul, calcetas blancas.
    * Arbitros: playera verde fosforescente, short negro.
    * Portero: uniforme amarillo solido.
    * Sin logos, escudos, marcas ni uniformes oficiales.

4. Texture Node
    * Metal.
    * Piel.
    * Tela.
    * Carton.
    * Fruta.
    * Concreto.
    * Cesped.
    * Polvo y haze.
    * Jersey con textura geometrica abstracta inspirada libremente en patrones prehispanicos, sin simbolos reconocibles.

5. Generic T1 Screen Node
    * Pantallas genericas T1 como superficies digitales creibles para montaje posterior.
    * Bloques abstractos, campos vacios, tarjetas genericas, lineas tacticas o formas suaves.
    * Sin UX final especifica.
    * Sin texto.
    * Sin numeros.
    * Sin iconos reconocibles.
    * Sin labels.
    * Sin apps clonadas.

6. Negative Prompt Node
    * Usar el negative prompt global del storyboard maestro.
    * Reforzar en tomas con pantallas: no readable phone screen, no readable laptop screen, no generated UX, no UI labels, no UI numbers, no app icons.

7. Shot Prompt Node
    * Un nodo por toma.
    * Cada nodo debe contener solo la descripcion de esa toma, mas referencias a los nodos globales.
    * Output: keyframe 16:9 limpio.

8. Reference / Consistency Node
    * Usar keyframes aprobados como referencias visuales para tomas hermanas.
    * Mantener continuidad por bloques narrativos, no necesariamente por identidad facial exacta en todas las tomas.

## Bloques Narrativos

### Bloque 01: Apertura / Salida

Tomas 1-5.

Funcion:
Abrir en calma y establecer la rima entre comercio, ciudad, tunel y ascenso hacia el escenario.

Nodos clave:
* Global Style.
* Color Continuity.
* Texture.
* Wardrobe para tomas deportivas.

Riesgo:
Que el modelo vuelva estas tomas demasiado publicitarias o dramaticas.

Control:
Pedir silencio visual, luz natural, composicion sobria y menos contraste.

### Bloque 02: Primer Paralelo Comercio / Futbol

Tomas 6-11.

Funcion:
Conectar accion cotidiana, pago, espera urbana y arranque deportivo.

Nodos clave:
* Generic T1 Screen para smartwatch y terminal.
* Wardrobe Continuity.
* Negative Prompt reforzado para marcas y texto.

Riesgo:
Logos de pago, marcas de smartwatch, senaletica legible o equipos reales.

Control:
Terminal generica, smartwatch sin marca, senalizacion desenfocada y sin texto legible.

### Bloque 03: Preparacion / Gestion

Tomas 12-17.

Funcion:
Rimar gestos manuales: cerrar caja, ajustar cinta, revisar tablet/laptop/smartphone.

Nodos clave:
* Texture.
* Generic T1 Screen.
* Color Continuity con acento `#DA3B2B`.

Riesgo:
Que el modelo intente inventar dashboards finales, tiendas online o interfaces copiadas.

Control:
Usar solo pantallas genericas T1 y reservar el montaje definitivo para postproduccion.

### Bloque 04: Decision / Ejecucion

Tomas 18-24.

Funcion:
Cruzar el momento de decision del protagonista en restaurante con la preparacion del tiro.

Nodos clave:
* Generic T1 Screen para tomas 20 y 22.
* Wardrobe Continuity.
* Food / Restaurant Texture.
* Football Action Texture.

Riesgo:
Demasiada reaccion caricaturesca o pantallas con texto.

Control:
Tension contenida, pulgares listos, pantalla abstracta, emociones realistas.

### Bloque 05: Climax

Tomas 25-30.

Funcion:
Resolver el tiro, el gol y la confirmacion de accion en paralelo.

Nodos clave:
* Action Detail.
* Generic T1 Screen para toma 29.
* Restaurant Celebration.

Riesgo:
Iconos de exito muy literales, UI final, celebracion stock.

Control:
Confirmacion abstracta sin icono reconocible; celebracion natural y comprimida.

### Bloque 06: Abstraccion / Cierre

Tomas 31-34.

Funcion:
Pasar de euforia colectiva a geografia emocional y cierre cosmico.

Nodos clave:
* Global Style.
* Color Continuity.
* Abstract Geography.
* Negative Prompt reforzado para mapas, banderas, labels y simbolos nacionales.

Riesgo:
Mapa politico literal, bandera, poster patriotico, satelite con UI.

Control:
Luces humanas como constelacion invertida, sin fronteras ni informacion cartografica.

## Orden De Produccion Sugerido

1. Generar 3-5 keyframes de prueba:
    * Toma 1: comercio / textura metal.
    * Toma 7: futbol / handshake / arbitros.
    * Toma 17: smartphone con pantalla generica T1.
    * Toma 29: confirmacion generica T1 abstracta.
    * Toma 34: cierre Tierra / Mexico tenue.

2. Aprobar look global:
    * Color.
    * Contraste.
    * Grano.
    * Tratamiento de piel.
    * Tratamiento de pantallas.

3. Generar las 34 tomas individualmente.

4. Seleccionar una version hero por toma.

5. Usar keyframes aprobados como referencias para continuidad por bloque.

6. Pasar tomas seleccionadas a video/motion.

7. Componer o ajustar pantallas definitivas en post.

8. Hacer una hoja de contactos final solo con keyframes aprobados.

## Instruccion Corta Para Agente Krea

Usa `storyboard-grid-prompt-v001.md` como biblia creativa y este documento como mapa de nodos, no como prompt unico gigante. Crea un patch modular con nodos separados para estilo global, color, vestuario, texturas, pantallas genericas T1, negativos globales y prompts por toma. Genera primero pruebas de las tomas 1, 7, 17, 29 y 34 antes de producir las 34 tomas completas. No generes texto, logos, marcas, UX final especifica ni interfaces legibles en ningun dispositivo.

## Decision Pendiente

Hay dos caminos posibles:

* Acceso directo con plugin/Codex a la computadora: armar o asistir el patch dentro de la interfaz, revisar outputs y ajustar iterativamente.
* Roadmap manual: usar este documento como briefing para construir el patch o pedirselo al agente de Krea.
