# Krea Operating Notes

Notas para mantener este paquete honesto y no inventar funciones.

Basado en documentacion publica de Krea revisada el 2026-05-01:

* Krea Nodes usa un canvas visual con nodos que tienen inputs, parameters y outputs.
* El canvas permite organizar workflows con secciones, grupos y sticky notes.
* Krea documenta nodos de generacion de imagen y video, entre otros, pero los modelos disponibles pueden rotar.
* El Node Agent puede leer el canvas, proponer un plan, construir el workflow y mostrar costo antes de ejecutar.
* Por eso este paquete no especifica nombres de modelos obligatorios ni funciones no verificadas.

Uso practico:

* Pedir al agente que proponga plan antes de construir.
* Pedir que no ejecute nada hasta aprobar costo.
* Pedir 5 keyframes primero.
* Evitar video, enhancement/upscale y variantes masivas hasta aprobar el look.
* Si Krea ofrece un modelo barato y uno caro, pedir al agente que explique diferencia de costo antes de usarlo.

