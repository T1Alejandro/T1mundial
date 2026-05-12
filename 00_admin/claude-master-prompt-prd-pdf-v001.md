---
title: "Claude Master Prompt - PRD PDF Ejecutivo T1 Mundial"
doc_type: "prompt"
status: "draft"
owner: "Arturo / Parco"
version: "0.1"
last_updated: "2026-05-12"
language: "es"
audience: ["claude-code", "creative", "production", "exec"]
tags: ["prd", "pdf", "executive-deck", "pipeline", "ai-video"]
---

# Prompt maestro para Claude

Copia y pega este prompt en Claude Code desde la raíz del repo:

```text
Actúa como director estratégico de producción AI-first, productor ejecutivo de cine, director editorial tipo Apple/Figma keynote y document designer senior.

Necesito que me ayudes a crear un PRD / documento ejecutivo en PDF para el proyecto cinematográfico AI-first “T1 Mundial”.

Este documento NO debe sentirse como documento corporativo pesado ni como reporte técnico. Debe sentirse como una pieza ejecutiva premium: Apple keynote, Figma presentation, editorial minimal, New York Times Magazine. Mucho aire, pocas palabras, jerarquía clara, criterio cinematográfico, diseño contemporáneo y narrativa estratégica.

Importante: tú no conoces este proyecto todavía. Antes de escribir el PRD final, lee el contexto del repo local y construye una comprensión real.

## Ubicación del proyecto

Repo local:

`/Users/parco/T1mundial`

Trabaja desde esa carpeta.

## Documentos que debes leer primero

Lee en este orden:

1. `README.md`
2. `00_admin/project-brief.md`
3. `03_creative/treatment-summary.md`
4. `03_creative/shot-list/current-rack-36-v005.md`
5. `04_production/production-pipeline.md`
6. `04_production/next-production-roadmap-v001.md`
7. `04_production/full-production-template-system.md`
8. `00_admin/decision-log.md`
9. `00_admin/open-questions.md`
10. `05_legal/legal-checklist.md`
11. `08_deliverables/delivery-specs.md`
12. `03_creative/model-sheets-personajes-locaciones-v001.md`
13. `03_creative/prompts/model-sheets-prompt-pack-v001.md`
14. Si necesitas más granularidad visual, revisa `02_references/visual/Stills T1mundial/` y la lista de stills en `03_creative/shot-list/current-rack-36-v005.md`.

No intentes leer todo el repo al mismo tiempo. Primero entiende estructura, narrativa, pipeline, assets y riesgos.

## Contexto ejecutivo del proyecto

“T1 Mundial” es un hero film cinematográfico AI-first para T1 alrededor del momento futbolístico 2026.

El proyecto consiste en aproximadamente 34 a 36 tomas cinematográficas de 3 a 5 segundos cada una, para construir un video final cercano a 1 minuto.

El proyecto ya no está en fase de exploración conceptual.

Ya existen:

- stills base,
- rack visual vigente,
- estructura narrativa,
- folders organizados,
- pipeline operativo,
- prompts,
- assets,
- model sheets,
- referencias,
- estructura técnica trabajada desde Claude Code + VSCode.

El objetivo ahora es terminar la producción cinematográfica completa de forma estable, consistente y escalable.

La preocupación principal NO es solo el costo económico.

También importa:

- estabilidad operativa,
- claridad del pipeline,
- continuidad visual,
- velocidad de iteración,
- desgaste mental,
- control legal,
- y evitar quedarnos sin créditos a mitad de producción.

## Tesis central del documento

La decisión ya NO es:

“qué herramienta está más cool”.

La decisión real es:

qué pipeline permite terminar el video completo:

- con menos fricción,
- menos desgaste mental,
- suficiente libertad creativa,
- continuidad visual,
- estabilidad operativa,
- control de versiones,
- y una ventana de producción cubierta correctamente.

El documento debe comunicar:

- madurez del pipeline,
- claridad de pensamiento,
- control operativo,
- criterio creativo,
- visión estratégica,
- y una transición seria hacia producción cinematográfica AI.

No debe sonar a:

- “necesito más créditos”,
- improvisación,
- exploración ansiosa,
- documento técnico demasiado denso,
- comparativa superficial de herramientas.

Debe sonar a:

“Estamos entrando a producción cinematográfica AI seria y necesitamos cubrir correctamente la ventana operativa.”

## Herramientas evaluadas

### Claude Code + VSCode

Rol recomendado:
estructura operativa, documentación, prompts, PRD, shot tracking, naming, templates, control de producción, QA textual y coordinación del sistema.

### Krea AI

Pros:
- muy buena experiencia operativa,
- node editor,
- exploración visual rápida,
- sistema amigable,
- flujo creativo claro,
- styles y organización cómodos,
- se siente más como un creative operating system.

Contras:
- cinematográficamente no siempre alcanza el nivel de Higgsfield.

Uso ideal:
hub creativo, exploration layer, node workflows, organización visual, look development.

### Higgsfield

Pros:
- excelente lenguaje cinematográfico,
- fuerte en movimientos de cámara,
- shots complejos,
- sensación premium para video AI,
- bueno para tomas hero y cinematic motion.

Contras:
- flujo algo disperso,
- puede sentirse fragmentado,
- exige mucha atención mental para operar varias partes del pipeline.

Uso ideal:
motor cinematográfico principal, motion, tomas hero, image-to-video premium.

### Seedance

Uso esperado:
- generación final,
- stitching,
- render,
- producción de clips,
- capa final de producción/render.

No debe plantearse necesariamente como lugar principal para pensar o explorar.

### Figma Weave

Necesito que lo trates con cuidado.

Mi percepción actual:
- viene del ecosistema Figma,
- parece tener filosofía UX tipo Figma,
- apunta a workflows creativos visuales,
- interfaces cuidadas,
- lógica más enfocada a sistemas creativos que a simple generación AI,
- puede tener muchísimo potencial,
- puede crecer fuerte entre diseñadores,
- se siente más humano y pensado.

Pero:
- parece temprano para usarlo como columna vertebral absoluta de producción final cinematográfica.

Uso ideal por ahora:
exploración visual avanzada, workflows personales, R&D creativo, crecimiento estratégico futuro.

Importante: si tienes acceso a internet o documentación actual, valida qué es exactamente Figma Weave antes de afirmarlo. Si no puedes verificarlo, marca esa sección como “hipótesis operativa” y no la presentes como hecho definitivo.

## Reflexión de costo real

El error sería calcular el costo solamente por duración final.

No es:

34 tomas x 4 segundos.

En AI video, cada toma requiere múltiples iteraciones.

Modelo real:

34 tomas x 4 a 8 iteraciones promedio = 136 a 272 generaciones reales.

El verdadero costo viene de:

- refinamiento,
- continuidad,
- motion,
- fixing,
- consistencia,
- stitching cinematográfico,
- descartes,
- pruebas,
- regeneración por errores legales o visuales.

No inventes precios actuales de herramientas si no puedes verificarlos. Si vas a proponer costos o tiers, estructura escenarios por volumen de generaciones y supuestos, no como cotización definitiva.

## Recomendación final actual

Pipeline recomendado:

Claude Code + VSCode
→ estructura operativa

Krea
→ exploración / node workflows / organización creativa

Higgsfield
→ generación cinematográfica principal

Seedance
→ render y generación final

Weave
→ exploración futura / workflows AI creativos / crecimiento estratégico

## Entregable principal

Quiero que produzcas un PRD / PDF ejecutivo en español.

Debe poder mostrarse directamente a dirección o liderazgo creativo.

Debe incluir:

1. narrativa ejecutiva,
2. arquitectura de pipeline,
3. diagnóstico de fase actual,
4. comparación sobria de herramientas,
5. recomendación de stack,
6. modelo de iteraciones reales,
7. tiers o escenarios de producción,
8. riesgos y mitigaciones,
9. plan de producción,
10. criterios de aprobación,
11. próximos pasos,
12. guía visual para convertirlo a PDF/deck premium.

## Formato deseado

Quiero dos outputs:

### Output A: PRD ejecutivo

Un documento en Markdown listo para convertirse a PDF, guardado idealmente como:

`00_admin/t1-mundial-production-prd-executive-v001.md`

Debe tener tono ejecutivo, limpio, sobrio, visualmente escaneable.

### Output B: Guía de deck / PDF visual

Una estructura slide-by-slide o page-by-page para diseñar el PDF con estética Apple/Figma/editorial minimal.

Guardarlo idealmente como:

`00_admin/t1-mundial-production-prd-deck-outline-v001.md`

## Estilo editorial

Usa español natural, ejecutivo y contemporáneo.

Reglas de copy:

- pocas palabras,
- frases contundentes,
- cero relleno,
- evitar jerga innecesaria,
- evitar sonar a pitch desesperado,
- evitar “necesitamos más créditos”,
- hablar de “ventana operativa”, “continuidad”, “control”, “producción”, “iteración”, “calidad final”.

Tono:

- estratégico,
- cinematográfico,
- sobrio,
- seguro,
- minimal,
- premium,
- humano.

No uses lenguaje de startup genérico.
No uses claims grandilocuentes.
No conviertas esto en tabla corporativa pesada.

## Dirección de diseño

El PDF/deck debe sentirse como:

- Apple keynote,
- Figma presentation,
- editorial minimal,
- sistema creativo premium,
- producción cinematográfica seria.

Características:

- mucho espacio en blanco,
- tipografía tipo SF Pro,
- jerarquía extrema,
- pocas palabras por página,
- diagramas simples,
- retícula limpia,
- contraste sobrio,
- uso estratégico de stills del proyecto,
- nada saturado,
- nada de fondos barrocos,
- nada de dashboards corporativos genéricos.

Sugerir layouts por página:

- título grande + subtítulo mínimo,
- una frase por slide cuando sea importante,
- diagramas de pipeline muy simples,
- matriz de herramientas sobria,
- escenarios de producción con pocas cifras,
- cierre con decisión recomendada.

## Posible narrativa del deck

Puedes mejorarla, pero parte de esta lógica:

1. Portada: T1 Mundial / Production Readiness
2. Ya no estamos explorando. Estamos entrando a producción.
3. El reto no es generar 1 minuto. Es sostener 34+ tomas.
4. La unidad real de costo es la iteración.
5. La continuidad es el riesgo central.
6. El pipeline ya existe.
7. Cada herramienta tiene un rol, no una religión.
8. Stack recomendado.
9. Krea como hub creativo.
10. Higgsfield como motor cinematográfico.
11. Seedance como capa final.
12. Weave como R&D estratégico.
13. Escenarios de producción: lean / controlled / full coverage.
14. Riesgos y mitigaciones.
15. Decisión recomendada.
16. Próximos pasos.

## Escenarios de producción

Propón tiers sin inventar precios si no puedes verificarlos:

### Lean
- menos iteraciones por toma,
- prioriza tomas críticas,
- mayor riesgo de continuidad,
- sirve si el presupuesto/créditos son limitados.

### Controlled
- rango medio de iteraciones,
- cobertura suficiente para sostener calidad,
- recomendado para producción seria.

### Full Coverage
- más iteraciones,
- buffer para regeneración,
- mayor estabilidad creativa,
- ideal si se quiere proteger calidad final y reducir desgaste.

Incluye una tabla simple con:

- número de tomas,
- iteraciones promedio,
- generaciones estimadas,
- uso recomendado,
- riesgo operativo.

Usa rangos:

- 34 tomas x 4 iteraciones = 136 generaciones
- 34 tomas x 6 iteraciones = 204 generaciones
- 34 tomas x 8 iteraciones = 272 generaciones

Puedes adaptar a 36 tomas si el rack vigente lo requiere, explicando la diferencia entre “34 aproximadas” y “36 en source of truth visual”.

## Riesgos que debe cubrir

Incluye riesgos y mitigaciones:

- quedarse sin créditos a mitad de producción,
- continuidad de personajes,
- continuidad de locaciones,
- motion inconsistente,
- legal/IP/logos/texto visible,
- fatiga operativa,
- sobreexploración,
- pipeline fragmentado,
- stitching débil,
- falta de criterios de aprobación,
- cambios de herramienta a mitad del proceso.

## Criterios de aprobación

Incluir criterios claros:

- still aprobado antes de motion,
- cada toma con estado,
- naming consistente,
- asset source traceable,
- checklist legal,
- continuidad visual,
- motion usable,
- integración en rough cut,
- decisión de entrada/salida del master.

## Proceso de trabajo esperado

Antes de escribir:

1. Revisa los documentos clave.
2. Resume en 10 bullets qué entendiste del proyecto.
3. Identifica huecos o inconsistencias.
4. Propón la estructura final del PRD.
5. Luego redacta los archivos.

Si falta información crítica, haz preguntas puntuales. No hagas más de 5 preguntas al inicio. Si puedes avanzar con supuestos razonables, avanza y marca los supuestos.

## Restricciones importantes

- No cambies la visión creativa del proyecto.
- No conviertas el proyecto en una simple comparativa de software.
- No inventes datos de precio actuales.
- No afirmes cosas no verificadas sobre Weave.
- No escribas demasiado texto por slide.
- No pierdas la sensibilidad cinematográfica.
- No hagas un documento defensivo.
- No uses un tono de “pedir permiso”.
- El documento debe proyectar control.

## Definición de éxito

El resultado debe hacer que dirección/liderazgo creativo entienda rápidamente:

1. que el proyecto ya tiene madurez real,
2. que la producción final requiere una ventana operativa cubierta,
3. que el costo real vive en iteraciones, no en segundos finales,
4. que cada herramienta tiene un rol preciso,
5. que el pipeline recomendado reduce fricción y protege continuidad,
6. y que la decisión correcta es financiar/autorizar una producción controlada, no improvisar toma por toma.

Empieza revisando el repo y luego entrega los dos archivos Markdown.
```

