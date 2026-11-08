# 01 · El prompt (lo que le pedí al asistente)

> **Copia literal de la instrucción.** La idea le pide al asistente tres cosas de RAG:
> 1) responder **solo** con el manual, 2) **citar** la sección o página, y 3) decir
> **"no aparece"** cuando no lo encuentre (para no alucinar).

---

Vas a responder preguntas de operación de una bodega **usando únicamente el manual de
procesos que te acabo de compartir (Manual de Procesos de Operaciones de Distribuidora
Valle Verde, versión 3.2)**. Nada más: ni tu conocimiento general, ni suposiciones, ni
"lo que suele hacerse en bodegas".

Reglas:

1. **Fuente única:** si un dato no está literalmente en el manual, responde exactamente:
   *"No aparece en el manual"* — sin ofertas de alternativas, sin sugerencias, sin
   completar "con respecto a lo que uslmente se hace".
2. **Cita:** cada afirmación lleva su referencia como `[sección 2.5 · página 4]`. Si el
   dato está en dos lugares, cita ambos.
3. **Textual:** cuando lo puedas, copia la frase del manual, entre comillas, y solo
   después la explicación propia.
4. **Si el manual tiene dos partes con números diferentes** (por ejemplo texto de
   sección vs. tabla del Anexo D o del control de cambios), **cita ambas** y señala que
   "el mismo manual las dice distinto", sin elegir tú cuál es la correcta a menos que el
   propio manual defina una jerarquía (como la sección 1.4 con el control de cambios).
5. Si la pregunta es de idea, consejo u operación fuera del manual, recuérdame bajo tu
   propia regla 1 antes de contestar y detén: "No aparece en el manual".

Importante: le importa que esta respuesta solo responda qué dice el documento, no qué
debería hacer la bodega.

---

*(A la asistente se le pegó el PDF del manual en la conversación antes de enviar este
prompt: `manual-de-procesos-valle-verde-v3.2.pdf`, y después se hicieron las preguntas de
los archivos [02](./02-preguntas-y-verificacion.md) y [03](./03-pregunta-de-control.md)).*
