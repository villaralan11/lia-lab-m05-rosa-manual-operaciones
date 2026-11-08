# Proyecto · Clase 5 · Rosa comprueba que su asistente responde con el manual y no con lo que supone

**LIA Lab · DEV.F · Módulo 5 (RAG, modelos y alucinaciones)**
**Rol: Rosa (Operaciones de la Distribuidora Valle Verde) · Tiempo estimado: ~30 min**

Caso: Rosa quiere ayudar a los ingresos nuevos de la bodega con su asistente, pero solo si
las respuestas **realmente salen del manual de procesos** y no de la mayor habilidad de los
modelos de inventar respuestas seguras. Esta entrega prueba el asistente con el manual como
única fuente y comprueba cada respuesta con la página del manual.

## Estructura del proyecto

| Archivo | Contenido |
|---|---|
| [01-prompt.md](./01-prompt.md) | La instrucción al asistente para responder SOLO con el manual |
| [02-preguntas-y-verificacion.md](./02-preguntas-y-verificacion.md) | 3 preguntas de los ingresos nuevos + respuesta + dónde se comprobó en el manual (+ todo lo demás) |
| [03-pregunta-de-control.md](./03-pregunta-de-control.md) | La pregunta que NO está en el manual y lo que hizo el asistente |
| [04-revision.md](./04-revision.md) | Lo que la revisión encontró: respuesta incompleta, contradicción DENTRO del manual y una suposición |
| [manual-de-procesos-valle-verde-v3.2.pdf](./manual-de-procesos-valle-verde-v3.2.pdf) | El manual usado como fuente (versión 3.2, entregada por el proyecto) |

## Cómo saber si quedó bien (checklist del brief)

- [x] Las 3 preguntas piden **datos concretos y revisables** (un plazo, una cifra, un paso), no "resume el manual".
- [x] El prompt pide responder **solo con el manual**, **citar sección/página** y decir "no aparece" cuando no encuentre.
- [x] Cada respuesta indica **dónde se comprobó** en el manual (sección y página) y qué se vio al abrirlo.
- [x] Se probó una pregunta **que el manual no contesta** y se registró el comportamiento del asistente.
- [x] La revisión nombra algo concreto: una suposición del asistente, una respuesta incompleta y una **contradicción interna del manual** — y qué se decidió hacer.

## Nota importante para reproducción

El manual tiene una regla de jerarquía en la sección **1.4 (página 3)**: *"Si una sección
contradice la tabla de control de cambios de la sección 11, manda el control de cambios"*.
La revisión (archivo 04) muestra una zona **donde el texto de la sección 6.2 (página 9) sigue
con el dato viejo de 24 horas** mientras la tabla de cambios (página 14, versión 3.2) ya lo
cambió a **48 horas**.
