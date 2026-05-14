---
title: "LoRA Realism Prompt System v001"
doc_type: "prompt-system"
status: "active-draft"
owner: "Arturo / Parco"
reviewers: ["Creative", "Production", "AI Image"]
version: "0.1"
last_updated: "2026-05-13"
language: "es"
audience: ["creative", "production", "ai-agent", "higgsfield", "chatgpt-images"]
tags: ["lora", "realism", "skin-texture", "micro-detail", "v08", "commerce-athlete"]
source_of_truth:
  - "03_creative/prompts/higgsfield-character-location-sheet-v008.md"
  - "03_creative/prompts/chatgpt-master-rack-14-v008-commerce-athlete.md"
confidence: "medium"
---

# LoRA Realism Prompt System v001

## Objetivo

Este documento no entrena un LoRA real. Funciona como un **módulo de prompt de realismo extremo** para empujar los renders de T1 v08 hacia piel, manos, ojos, telas, superficies y objetos con textura físicamente creíble.

Usar este módulo sobre:

- `higgsfield-character-location-sheet-v008.md`
- `chatgpt-master-rack-14-v008-commerce-athlete.md`
- prompts individuales de Don Rafael, Doña Carmen, Miguel, Sofía, Lupita y manos diversas.

La prioridad es lograr realismo cabrón sin caer en:

- piel plástica,
- belleza retocada,
- poros simétricos falsos,
- nitidez digital,
- suciedad o deterioro,
- look médico desagradable,
- pérdida de identidad del personaje.

## Regla Principal

Agregar realismo microscópico solo donde aporta producción:

- rostro,
- manos,
- ojos,
- cuello,
- piel visible,
- cabello fino,
- tela,
- cartón,
- fruta,
- madera,
- metal limpio,
- pantallas lisas,
- terminales y empaques.

No convertir todo en macro dermatológico. Para sheets 6x2 y racks, el realismo debe sentirse aunque el plano sea medio o wide.

## Módulo Global De Realismo

Pegar después del look global del prompt:

```text
REALISMO EXTREMO:
Intensificar la microestructura auténtica de piel, manos, telas y materiales con realismo sin concesiones, manteniendo la identidad, proporciones faciales, edad, gesto y dirección de arte original. Revelar textura orgánica real: poros visibles no simétricos, microrelieve natural, líneas finas de expresión, asimetrías sutiles, pequeñas marcas, variación tonal, vello facial o vello fino donde corresponda, resequedad leve natural y comportamiento físico real de la piel. Distinguir zonas mate, zonas con sebo natural, piel más seca, piel más cálida, sombra bajo ojos, textura de labios, cejas, pestañas, manos trabajadas, uñas reales y pliegues finos.

Mantener el color grading cinematográfico original: dorados cálidos, negros levantados, sombras suaves, roll-off analógico en highlights y grano fino orgánico. No reinterpretar la paleta. No suavizar piel. No embellecer. No plastificar. No aplicar beauty lighting. No usar nitidez digital agresiva. Todo detalle debe parecer óptico y fotografiado, no sharpen artificial.

La imagen debe sentirse incómodamente real en el buen sentido: una producción cinematográfica premium capturada con lente 35mm/50mm, sensor de alta calidad, luz natural o práctica, profundidad de campo media a shallow, microcontraste físico y textura tangible.
```

## Módulo Rostro

Usar en personajes:

```text
ROSTRO REALISTA:
Preservar identidad exacta del personaje, edad aparente, proporciones, gesto y expresión. Añadir textura facial auténtica: poros no uniformes, líneas finas de expresión, microarrugas naturales, leves asimetrías, variación de tono en mejillas, nariz, frente y bajo ojos, vello fino visible con luz lateral, cejas con irregularidad natural, pestañas reales, labios con textura suave, pequeñas marcas o pecas sutiles si encajan con el personaje. La piel debe tener profundidad y respuesta física real, con brillos controlados y zonas mate naturales.
```

## Módulo Ojos

Usar en retratos medios o close-ups:

```text
OJOS REALISTAS:
Ojos con fidelidad anatómica: iris definido con fibras radiales naturales, variación cromática sutil, humedad real en superficie ocular, catchlight suave y rectangular, esclerótica blanca natural con leve tinte cálido, borde del párpado y lagrimal creíbles, pestañas individuales no perfectas, cejas con pelos irregulares. Evitar ojos de muñeco, exceso de brillo, simetría perfecta o mirada artificial.
```

## Módulo Manos

Clave para tomas 03, 05, 07, 09 y 12:

```text
MANOS REALISTAS:
Manos con anatomía correcta y textura real: nudillos, venas sutiles, pliegues, resequedad leve, uñas naturales, cutículas, pequeñas marcas de trabajo, variación tonal, poros y vello fino según edad. Los dedos deben tener proporciones correctas y contacto físico creíble con objetos: terminal, caja, cinta, fruta, teclado, tablet, prenda, dinero abstracto o etiqueta. No manos perfectas de stock, no dedos extra, no muñecas rotas, no uñas falsas, no piel plástica.
```

## Módulo Materiales Limpios

Usar en locaciones y props:

```text
MATERIALES LIMPIOS Y TÁCTILES:
Todo material debe tener respuesta física real: metal limpio con microarañazos sutiles pero sin óxido, cartón kraft nuevo con fibra visible, cinta lisa con reflejo suave, fruta fresca con poros y cera natural, madera noble limpia con veta real, cerámica con brillo controlado, tela con trama visible, delantales y camisas con fibras reales, pantallas lisas con reflejo suave, terminales limpias y sin marcas. Textura sí, deterioro no. Realismo sí, suciedad no.
```

## Módulo Pantallas Lisas Para Post

Usar en laptops, tablets, teléfonos y terminales:

```text
PANTALLAS PARA POST:
Las pantallas deben ser superficies lisas y creíbles, listas para composición posterior. Pueden ser blanco suave, gris claro, negro mate o reflejo tenue del ambiente. Sin logos, sin texto, sin números, sin iconos, sin dashboard, sin UI, sin puntos de tracking, sin cruces y sin gráficos. La pantalla debe tener reflejo óptico real, borde limpio, vidrio creíble y ligera variación de luz, pero ningún contenido legible.
```

## Módulo Limpieza Premium

Usar en todos los prompts v08:

```text
LIMPIEZA PREMIUM:
Todos los espacios deben verse nuevos, limpios, mantenidos y dignos. Evitar cualquier lectura de abandono, precariedad o suciedad. No polvo pesado, no paredes manchadas, no óxido, no humedad, no pintura descarapelada, no basura, no pisos rotos, no cables desordenados, no puestos deteriorados, no cartón dañado. La textura debe venir de materiales reales y cuidados, no de mugre.
```

## Negative Prompt De Realismo

Agregar al negative prompt general:

```text
airbrushed skin, smooth skin, uniform skin tone, beauty retouching, beauty lighting, ring light, porcelain skin, waxy skin, plastic skin, silicone skin, CGI skin, doll eyes, fake eyelashes, symmetrical pore patterns, digital sharpening halos, oversharpening, flat lighting, fake texture, AI skin texture, melted pores, blurry pores, fake freckles, malformed eyes, crossed eyes, dead eyes, glassy doll eyes, extra fingers, fused fingers, broken wrists, malformed hands, fake nails, overprocessed HDR, synthetic gloss, muddy skin, dirty skin, grime, decay, damaged materials, rust, stains, peeling paint, cracked walls, clutter, text, logos, watermarks
```

## Uso Recomendado En El Sheet 6x2

Para el character + location sheet:

1. Mantener el prompt maestro v08.
2. Insertar `REALISMO EXTREMO` después de `LOOK GLOBAL`.
3. Insertar `MATERIALES LIMPIOS Y TÁCTILES` después de `TEXTURA Y LUZ`.
4. Insertar `PANTALLAS PARA POST` dentro de la sección de pantallas/superficies.
5. Añadir `ROSTRO REALISTA` a los 5 personajes.
6. Añadir `MANOS REALISTAS` a la toma 06 de manos diversas.
7. Añadir `LIMPIEZA PREMIUM` antes de la fila de locaciones.
8. Añadir el negative de realismo al negative prompt general.

## Bloque Compacto Para Pegar

Versión corta cuando el prompt ya está muy largo:

```text
REALISMO PREMIUM:
Preservar identidad, edad, gesto, composición y color grading original. Añadir microestructura auténtica: poros no uniformes, líneas finas, vello fino, variación tonal, textura de labios, cejas, pestañas, manos con pliegues, uñas naturales, piel con zonas mate y brillo real. Materiales limpios y táctiles: metal limpio, cartón nuevo, fruta fresca, madera noble, cerámica, tela con fibras, pantallas lisas con reflejo óptico. Cero piel plástica, cero beauty retouch, cero nitidez digital, cero suciedad, cero deterioro. Realismo cinematográfico premium, 35mm/50mm, grano fino orgánico, highlights con roll-off analógico.
```

## Bloque JSON Inspiracional Para Macros

Usar solo como referencia de estructura para prompts técnicos, no como formato obligatorio:

```json
{
  "model_style": "cinematic photorealism",
  "resolution": "4K",
  "subject": {
    "body_part": "face, hands, skin, material detail",
    "skin_tone": "Mexican/Latino natural warm skin tones",
    "imperfections": [
      "visible pore texture",
      "fine expression lines",
      "natural tonal variation",
      "subtle asymmetry",
      "vellus hair",
      "real hand texture",
      "natural nails and cuticles"
    ]
  },
  "lighting": "soft natural/practical cinematic light, raking side light when useful",
  "lens": "35mm or 50mm, medium to shallow depth of field",
  "texture_policy": "authentic microtexture without dirt or decay",
  "negative_prompt": [
    "airbrushed skin",
    "plastic skin",
    "waxy skin",
    "digital sharpening",
    "symmetrical pores",
    "beauty retouching",
    "malformed hands",
    "extra fingers",
    "dirty damaged materials",
    "logos",
    "text"
  ]
}
```

## Aplicación Por Personaje

### Don Rafael

Enfatizar:

- manos trabajadas,
- piel madura real,
- arrugas suaves,
- cejas y pelo entrecano naturales,
- mirada digna,
- textura de camisa oscura,
- metal limpio de cortina.

Evitar:

- piel demasiado lisa,
- viejo caricaturesco,
- suciedad,
- tienda deteriorada.

### Doña Carmen

Enfatizar:

- sonrisa serena real,
- textura de piel natural de 45 años,
- manos de trabajo cotidiano,
- delantal limpio,
- fruta fresca con microtextura.

Evitar:

- mercado sucio,
- folklor turístico,
- fruta podrida,
- delantal gastado.

### Miguel

Enfatizar:

- manos precisas,
- piel real en nudillos,
- fibras de camiseta,
- cartón kraft nuevo,
- cinta lisa,
- luz fría funcional.

Evitar:

- gimnasio/deporte,
- bodega mugrosa,
- cajas rotas,
- piel de modelo retocado.

### Sofía

Enfatizar:

- rostro analítico,
- piel real sin beauty retouch,
- cabello negro lacio con fibras reales,
- manos en teclado,
- workspace limpio y aspiracional.

Evitar:

- look corporativo Silicon Valley,
- software real,
- dashboard legible,
- piel de anuncio cosmético.

### Lupita

Enfatizar:

- calidez maternal,
- piel madura cuidada,
- textiles limpios,
- cerámica y madera noble,
- luz cálida suave.

Evitar:

- folclor exagerado,
- tienda vieja,
- calle turística reconocible,
- deterioro.

## Aplicación En Locaciones

Para todas las locaciones:

```text
La locación debe sentirse recién cuidada para filmación: limpia, luminosa, ordenada, con materiales reales y textura táctil. La textura viene de metal, madera, cartón, fruta, cerámica, tela y luz, no de suciedad ni deterioro.
```

## Checklist Antes De Generar

- ¿El prompt pide realismo sin pedir suciedad?
- ¿Las pantallas están lisas y sin UI?
- ¿No hay logos T1 generados por AI?
- ¿El rojo T1 aparece como acento natural?
- ¿Las locaciones se sienten limpias y dignas?
- ¿La piel conserva edad y textura?
- ¿Las manos tienen anatomía correcta?
- ¿No hay futbol, estadio, balón, jersey ni escuela?
