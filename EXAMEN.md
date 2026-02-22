# 📝 Evaluación de Aprendizaje: Proyectos LangChain 1.0 (044)

¡Felicidades por completar los primeros 3 notebooks de proyectos! Aquí tienes una pequeña evaluación para consolidar lo aprendido. Responde indicando la letra de la opción correcta.

---

### **Instrucciones**
1. Lee cada pregunta cuidadosamente.
2. Responde en este mismo archivo o en el chat con el formato: `1: a, 2: b, ...`
3. Cuando termines, dímelo y corregiremos juntos.

---

### **Pregunta 1: Inicialización de Modelos**
¿Qué parámetro de `init_chat_model` deberías establecer en `0.0` para asegurar que las respuestas del agente sean lo más factuales y consistentes posible (menos aleatorias)?
- a) `creativity`
- b) `random_seed`
- c) `temperature`
- d) `model_stability`

### **Pregunta 2: Invocación vs. Streaming**
Si quieres que tu aplicación muestre el texto "en vivo" a medida que la IA lo genera (tipo ChatGPT), ¿qué método de LangChain deberías utilizar?
- a) `.invoke()`
- b) `.stream()`
- c) `.playback()`
- d) `.live_call()`

### **Pregunta 3: Comportamiento Agéntico**
¿Cuál es la diferencia principal entre un "Chatbot simple" y un "Agente Real" según lo visto en el curso?
- a) El Agente Real siempre usa GPT-5, el Chatbot usa GPT-4.
- b) El Chatbot puede recordar, el Agente Real no puede.
- c) El Agente Real puede tomar decisiones de forma autónoma y usar herramientas para resolver problemas.
- d) No hay ninguna diferencia, son términos intercambiables.

### **Pregunta 4: Herramientas (Tools)**
Para que una función de Python sea reconocida por LangChain como una herramienta que el Agente puede usar, ¿qué decorador debemos aplicar?
- a) `@langchain_function`
- b) `@agent_task`
- c) `@tool`
- d) `@action`

### **Pregunta 5: Memoria a Corto Plazo**
Para que el agente pueda recordar lo que se dijo en mensajes anteriores dentro de una misma sesión, necesitamos un `checkpointer` (como `InMemorySaver`) y enviar un identificador específico en la configuración. ¿Cómo se llama ese identificador?
- a) `session_key`
- b) `thread_id`
- c) `chat_index`
- d) `memory_token`

### **Pregunta 6: Salida Estructurada**
Si queremos que el Agente responda siempre siguiendo un formato de datos estricto (por ejemplo, un objeto con campos específicos), ¿qué componente de Python y estrategia de LangChain solemos usar combinados?
- a) `List` + `DefaultStrategy`
- b) `Dictionary` + `JsonStrategy`
- c) `dataclass` + `ToolStrategy`
- d) `Markdown` + `PromptStrategy`

---
*Ánimo, ¡vas por muy buen camino!* 🚀
