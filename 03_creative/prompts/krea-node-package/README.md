# Krea Node Package

Paquete compacto derivado de `../storyboard-grid-prompt-v001.md` y `../krea-node-editor-roadmap-v001.md`.

Uso recomendado:

1. Para escalar a las 34 tomas en espanol, usar `10-krea-34-shot-spanish-style-compiler-flow.md`. Ese archivo arma el flujo recomendado actual: LLM solo como compresor de estilo global + 34 escenas manuales + 34 generadores.
2. Si el mensaje completo es demasiado largo para Krea, pegar en orden estas 4 partes en el mismo chat del agente: `10a-krea-34-flow-part-1-architecture.md`, `10b-krea-34-flow-part-2-scenes-01-12.md`, `10c-krea-34-flow-part-3-scenes-13-24.md`, `10d-krea-34-flow-part-4-scenes-25-34-review.md`.
3. Para el flujo de prueba de shots 01-04, usar `09-krea-option-c-llm-compiler-shot-01-04.md`. Ese archivo conserva la version inicial con LLM compilador por lineas y variante barata directa.
4. Si quieres evitar el LLM, el archivo `09-krea-option-c-llm-compiler-shot-01-04.md` incluye 4 prompts directos para pegar en generadores.
5. Para el flujo anterior de shots 01-04 sin LLM, usar `08-krea-flow-shot-01-04.md`.
6. Para Krea Agent con el batch anterior de 5 pruebas, usar `06-single-paste-krea-agent-request.md`.
7. Para nodos manuales o copy/paste, usar `07-copy-paste-node-texts-test.md`.
8. Leer `00-krea-operating-notes.md` para mantener el flujo aterrizado a lo que Krea documenta.
9. Revisar costo antes de ejecutar.
10. Probar pocas tomas antes de correr las 34.

Notas:

* Este paquete no asume funciones no verificadas de Krea.
* Usa lenguaje compatible con un flujo de Nodes: generar imagen, organizar secciones, reutilizar bloques de estilo, revisar plan y costo antes de ejecutar.
* Las pantallas deben verse como superficies digitales genericas y abstractas: creibles, sin texto legible, sin UX final, listas para montaje o ajuste posterior.
