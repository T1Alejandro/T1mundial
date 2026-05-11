---
title: "PRD - Claude Code Handoff T1 Mundial"
doc_type: "prd"
status: "draft"
owner: "Arturo / Parco"
reviewers: ["Claude Code", "Codex", "Arturo / Parco"]
version: "0.1"
last_updated: "2026-05-08"
language: "es"
audience: ["ai-agent", "production", "creative", "ops"]
tags: ["prd", "claude-code", "handoff", "skills", "hands-up", "production-os"]
source_of_truth: "local-project"
confidence: "medium"
related_docs:
  - "../HANDS-UP.md"
  - "project-brief.md"
  - "../INDEX.md"
  - "../01_strategy/campaign-north-star.md"
  - "../04_production/next-production-roadmap-v001.md"
  - "../03_creative/prompts/chatgpt-master-rack-36-v004.md"
---

# PRD - Claude Code Handoff T1 Mundial

## 1. Resumen

T1 Mundial es el sistema operativo de produccion para un hero film cinematografico de T1, pensado para el momento futbolistico 2026 en Mexico.

El proyecto busca producir un video principal de 60-90 segundos para YouTube, con cortes derivados para redes, usando una mezcla controlada de estrategia creativa, stills generados con AI, pruebas de motion, VO, edicion, postproduccion, QA legal y entregables finales.

La tesis creativa es:

> Cuando Mexico juega, Mexico entero juega. Once en el campo, millones en sus negocios. Un solo pais, un solo equipo. Todo conectado en uno.

La frase final aprobada como norte creativo es:

> Todo Mexico es uno. Todo en uno. T1.

Claude Code debe entrar como agente de produccion y organizacion: mantener el repo ordenado, instalar o preparar skills utiles, actualizar `HANDS-UP.md`, crear tableros/documentos cuando haga falta y ayudar a convertir prompts, stills, motion tests y entregables en un flujo repetible.

## 2. Objetivo Del Producto

Crear un Project OS robusto para llevar el hero film de T1 desde stills aprobados hasta motion tests, rough cut, QA y masters finales.

El resultado no es solo un video. Es un sistema que permite:

- Saber que esta aprobado, bloqueado o pendiente.
- Regenerar tomas sin perder consistencia visual.
- Mantener el riesgo legal bajo control.
- Coordinar herramientas como Figma, Krea, Higgsfield, Seedance, Kling, Veo, ElevenLabs, Premiere, After Effects y Notion.
- Dar handoffs claros entre agentes humanos y AI.

## 3. Contexto Creativo

El film alterna dos mundos que se revelan como uno:

- Futbol: cancha, tunel, jugadores, arbitros, portero, gol, estadio ficticio.
- Comercio mexicano: tienda, mercado, ecommerce, restaurante, pagos, dispositivos, negocio diario.

La emocion buscada es orgullo tranquilo, epica cotidiana y dignidad comercial. Debe sentirse como cine autoral mexicano contemporaneo, no como comercial deportivo tradicional ni AI demo.

La barra de calidad esta definida por estos principios:

- Cine, no comercial generico.
- Mexico sin cliches.
- Comerciantes retratados con dignidad.
- Cero marcas, logos, uniformes oficiales, celebridades, estadios reconocibles o terminos protegidos.
- Ninguna toma con errores evidentes de AI entra al corte final.

## 4. Estado Actual

Segun `HANDS-UP.md` y `04_production/next-production-roadmap-v001.md`, el proyecto ya tiene:

- Project OS local armado en `/Users/parco/T1mundial`.
- Brief, estrategia, north star, QA, legal checklist y pipeline.
- Storyboard de 36 tomas oficiales.
- Prompt maestro activo: `03_creative/prompts/chatgpt-master-rack-36-v004.md`.
- 36 stills oficiales en `02_references/visual/Stills T1mundial`.
- Prompt pack inicial para Figma Weave/Wave: `04_production/wave-figma-first-6-prompt-pack-v001.md`.
- Roadmap de siguiente fase: motion tests, VO scratch, matriz de continuidad, decision de herramienta por toma.

El cambio de fase importante:

> Ya no estamos en look-dev inicial. Estamos entrando a produccion de motion tests, continuidad, VO y rough cut.

## 5. Usuarios Y Actores

Usuario principal:

- Arturo / Parco: owner creativo-operativo, decide direccion y aprueba avances.

Usuarios secundarios:

- Claude Code: agente de codigo, documentacion, setup, automatizacion, QA y handoff.
- Codex: agente colaborador para implementar, revisar y producir documentos.
- Equipo creativo T1: revisa tono, calidad, narrativa y entregables.
- Marketing T1: valida fit de marca, awareness y formatos.
- Producto T1: valida representacion del producto/pantallas.
- Legal / PI: valida derechos, marcas, likeness, terminos protegidos y uso comercial de herramientas AI.

## 6. Requerimientos Funcionales

### 6.1 Onboarding De Claude Code

Al iniciar, Claude Code debe leer en este orden:

1. `HANDS-UP.md`
2. `README.md`
3. `INDEX.md`
4. `00_admin/project-brief.md`
5. `01_strategy/campaign-north-star.md`
6. `04_production/next-production-roadmap-v001.md`
7. `03_creative/prompts/chatgpt-master-rack-36-v004.md`
8. `04_production/wave-figma-first-6-prompt-pack-v001.md`

Despues de leer, debe responder con:

- Resumen de 5-8 bullets del estado real.
- Bloqueadores activos.
- Proximo paso recomendado.
- Archivos que va a tocar.
- Riesgos que requieren decision humana.

### 6.2 Protocolo HANDS-UP

`HANDS-UP.md` es el estado ejecutivo vivo. Claude Code debe actualizarlo cuando:

- Cambie el estado de una fase.
- Se aprueben o rechacen stills.
- Se detecte riesgo legal, visual, tecnico, presupuesto o fecha.
- Se complete un motion test.
- Se cree o cambie un flujo de herramienta.
- Haya una decision importante de Arturo / Parco.

Cada actualizacion debe incluir:

- Fecha real.
- Que cambio.
- Que queda pendiente.
- Bloqueadores.
- Proximo paso concreto.

Regla: si una tarea afecta calidad, legal, fecha o presupuesto, debe aparecer en HANDS-UP.

### 6.3 Instalacion Y Preparacion De Skills

Claude Code debe revisar que el entorno tenga skills o capacidades equivalentes para:

- Figma: leer/disenar pantallas, boards, UI T1 y referencias visuales.
- Notion: crear o actualizar tablero vivo, tareas, minutas y decisiones.
- Browser/local preview: abrir interfaces locales o documentacion generada.
- Image generation: preparar prompts, variantes, referencias y assets bitmap.
- Documents/decks: convertir el estado en PRDs, handoffs, decks o reportes.
- Spreadsheets/data: crear matrices de continuidad, QA, costos, herramienta por toma.

Si el entorno soporta instalacion de skills, Claude Code debe instalar o activar las equivalentes. Si no soporta instalacion automatica, debe documentar el gap en `HANDS-UP.md` y continuar con archivos Markdown locales.

Skills recomendadas por prioridad:

1. Notion / knowledge capture / project tracking.
2. Figma / design implementation / figma-use.
3. Browser automation para revisar outputs locales.
4. Image generation para prompts y assets.
5. Documents o presentations para handoffs ejecutivos.
6. Spreadsheets para matrices de produccion.

### 6.4 Produccion De Motion Tests

Claude Code debe apoyar la siguiente fase de produccion:

- Crear o mantener carpetas por toma en `04_production/ai-generations/motion-tests/shot-##/`.
- Mantener `notes.md` por toma.
- Registrar herramienta usada, prompt, version, archivo exportado y decision.
- Comparar outputs contra el still oficial.
- Marcar riesgos de identidad, manos, texto, logos, fisica, pantallas o movimiento.

Naming requerido:

```text
t1mundial_shot-##_motion-test_tool-v###_yyyymmdd.mp4
t1mundial_shot-##_motion-prompt_tool-v###_yyyymmdd.md
```

### 6.5 Matriz De Continuidad

Claude Code debe crear una matriz para las 36 tomas con:

- Numero de toma.
- Bloque narrativo.
- Personaje / objeto principal.
- Locacion.
- Vestuario.
- Color/acento.
- Dispositivo o pantalla.
- Riesgo legal.
- Riesgo AI.
- Riesgo de movimiento.
- Herramienta recomendada.
- Estado: pendiente, test, aprobado, remake, descartado.

Salida sugerida:

- `04_production/continuity-matrix-36-v001.md`

### 6.6 QA Legal Y Visual

Claude Code debe cruzar cada toma contra:

- `05_legal/legal-checklist.md`
- `04_production/qa/qa-checklist.md`
- negativos globales del prompt maestro

Debe levantar hands-up si detecta:

- Logo o marca visible.
- Uniforme real o demasiado parecido a seleccion/equipo oficial.
- Estadio reconocible.
- Terminos FIFA, World Cup, Mexico 2026 o equivalentes.
- Celebridad, atleta real o likeness sospechoso.
- Pantalla con UI inventada, texto, iconos o numeros.
- Manos, rostros o anatomia rotos.
- Movimiento que destruya continuidad.

### 6.7 Notion Board

El tablero Notion sigue pendiente como operacion viva. Claude Code debe proponer o crear un board con columnas:

- Backlog
- Ready
- In Progress
- Review
- Approved
- Blocked
- Done

Propiedades sugeridas:

- Shot
- Area
- Status
- Owner
- Priority
- Tool
- Risk Level
- Due Date
- Link local
- Notes

Si no tiene acceso a Notion, debe crear el schema en Markdown y dejarlo listo en:

- `00_admin/notion-board-schema.md`

## 7. Requerimientos No Funcionales

- Mantener todo versionado y legible.
- No borrar trabajo existente sin permiso explicito.
- No reescribir el lenguaje visual sin decision humana.
- Usar Markdown claro con frontmatter cuando sea documento persistente.
- Preferir cambios pequenos y trazables.
- Mantener compatibilidad con trabajo humano en Figma, Notion, Premiere, After Effects y herramientas AI externas.
- Evitar automatizaciones fragiles si el flujo todavia cambia rapido.

## 8. No Objetivos

Claude Code no debe:

- Aprobar legalmente el proyecto.
- Elegir por si solo la herramienta final de video sin evidencia.
- Cambiar la tesis creativa.
- Convertir el proyecto en landing page, app o dashboard innecesario.
- Generar UI final de T1 dentro de las pantallas AI sin assets reales.
- Usar marcas, logos, uniformes oficiales o nombres protegidos como atajos creativos.

## 9. Primer Sprint Recomendado Para Claude Code

### Sprint 1: Setup Y Control De Produccion

Objetivo:

Convertir el estado actual en una operacion lista para motion tests y rough cut.

Tareas:

1. Leer los documentos de onboarding.
2. Actualizar `HANDS-UP.md` con fecha 2026-05-08 si hay cambios reales.
3. Confirmar existencia de los 36 stills oficiales.
4. Crear `04_production/continuity-matrix-36-v001.md`.
5. Crear o validar estructura de carpetas `motion-tests/shot-##/`.
6. Revisar `wave-figma-first-6-prompt-pack-v001.md` contra las primeras 6 tomas oficiales.
7. Preparar checklist para motion tests 01-06.
8. Documentar skills disponibles, faltantes y plan de instalacion.
9. Crear o actualizar schema de Notion board.
10. Entregar reporte corto con proximo paso: correr Wave/Figma 01-06 o VO scratch.

Criterios de aceptacion:

- Claude Code puede explicar el proyecto sin perder la tesis creativa.
- `HANDS-UP.md` refleja el estado actual.
- Existe una matriz accionable de 36 tomas.
- Las carpetas de motion tests estan listas.
- Los riesgos activos estan visibles.
- El siguiente operador sabe exactamente que hacer.

## 10. Riesgos Principales

| Riesgo | Severidad | Mitigacion |
|---|---:|---|
| Movimiento AI rompe identidad o manos | Alta | Still aprobado como ancla, motion prompt corto, QA por toma |
| Logos, marcas o terminos protegidos | Alta | Negative prompt, legal checklist, revision frame por frame |
| Estadio o uniforme demasiado reconocible | Alta | Arquitectura ficticia, uniformes sin escudo ni identidad oficial |
| Pantallas AI inventan UI/texto | Alta | Pantallas blancas en AI, UI real en post/Figma |
| Falta de VO para ritmo | Media | Sprint rapido en ElevenLabs con scratch VO |
| Herramienta elegida por hype | Media | Decision por pruebas comparables, no por promesa |
| HANDS-UP desactualizado | Media | Actualizar al cerrar cada bloque de trabajo |

## 11. Definicion De Done

El Project OS esta listo para produccion sostenida cuando:

- Los 36 stills oficiales tienen estado claro.
- Las primeras 6 tomas tienen motion test inicial.
- Hay scratch VO para marcar ritmo.
- Existe matriz de continuidad.
- Existe tablero Notion o equivalente local.
- Cada riesgo relevante esta en `HANDS-UP.md`.
- Hay decision documentada de herramienta por tipo de toma.
- El rough cut puede empezar aunque algunas tomas sigan como stills.

## 12. Prompt Inicial Para Claude Code

Usar este prompt para arrancar una sesion nueva:

```text
Estamos trabajando en /Users/parco/T1mundial.

Primero lee:
1. HANDS-UP.md
2. README.md
3. INDEX.md
4. 00_admin/project-brief.md
5. 01_strategy/campaign-north-star.md
6. 04_production/next-production-roadmap-v001.md
7. 00_admin/prd-claude-code-handoff-v001.md

Necesito que actues como agente de produccion para el hero film T1 Mundial 2026.

Tu prioridad es mantener HANDS-UP vivo, preparar skills/capacidades necesarias, crear la matriz de continuidad de 36 tomas, validar estructura de motion tests y dejar listo el siguiente sprint de produccion.

No cambies la tesis creativa ni borres archivos existentes. Si algo afecta calidad, legal, fecha o presupuesto, levantalo en HANDS-UP.

Al terminar tu primera lectura, dame:
- resumen del estado actual
- bloqueadores
- skills/capacidades disponibles o faltantes
- archivos que vas a crear o tocar
- siguiente paso concreto
```

