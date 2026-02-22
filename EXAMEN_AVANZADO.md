# 🧠 Evaluación Avanzada: Arquitectura y Lógica de Agentes (044)

¡Impresionante! Has clavado el primer examen. Ahora vamos a subir el nivel para ver si dominas lo que pasa "bajo el capó" de LangChain 1.0.

---

### **Pregunta 1: Acceso al Contexto en Herramientas**
En el código del notebook `003`, definimos una herramienta que recibe `runtime: ToolRuntime[Context]`. ¿Cuál es el propósito real de este objeto `runtime`?
- a) Sirve para medir el tiempo de ejecución de la herramienta.
- b) Permite que la herramienta acceda a datos externos del usuario (como `user_id`) sin que el LLM tenga que pasarlos explícitamente como argumentos.
- c) Es una función que reinicia el Agente si hay un error.
- d) Es el objeto que contiene las claves API de OpenAI.

### **Pregunta 2: Persistencia de Memoria**
Usamos `InMemorySaver()` para el `checkpointer` del agente. Si reinicias el Kernel de Jupyter o detienes tu script de Python, ¿qué ocurre con el historial de conversaciones guardado?
- a) Se mantiene guardado en un archivo oculto `.langchain_history`.
- b) Se sube automáticamente a LangSmith si la clave API está activa.
- c) Se pierde completamente porque está almacenado en la memoria RAM del proceso.
- d) Se recupera la próxima vez que uses el mismo `thread_id`.

### **Pregunta 3: Configuración de Hilos (Threads)**
Al invocar al agente, pasamos `config = {"configurable": {"thread_id": "1"}}`. ¿Por qué es obligatorio usar la clave `"configurable"`?
- a) Porque es un requisito de seguridad de OpenAI.
- b) Porque LangChain/LangGraph utiliza este estándar para separar los parámetros de ejecución (mensajes) de los parámetros de persistencia y metadatos.
- c) Porque permite al usuario configurar la temperatura dinámicamente.
- d) No es obligatoria, podríamos pasar el `thread_id` directamente en la raíz del diccionario.

### **Pregunta 4: Estrategia de Salida Estructurada**
En `agent = create_agent(..., response_format=ToolStrategy(ResponseFormat))`, ¿qué hace realmente esa `ToolStrategy`?
- a) Obliga al LLM a usar siempre una herramienta de dibujo.
- b) Convierte el esquema de tu `dataclass` en una "herramienta virtual" de salida, forzando al modelo a generar un JSON que encaje exactamente con esa estructura al final de su razonamiento.
- c) Filtra las palabras malsonantes de la respuesta del modelo.
- d) Traduce automáticamente la respuesta al idioma definido en el contexto.

### **Pregunta 5: Invocación vs Bucle de Pensamiento**
En los notebooks `001` y `002` vimos que un Agente Real es "agéntico" porque puede iterar. Si el Agente llama a una herramienta y el resultado no es suficiente para responder, ¿qué hace LangChain por defecto?
- a) Devuelve un error de "Timeout".
- b) Pide ayuda al usuario mediante un prompt.
- c) Envía el resultado de la herramienta de vuelta al LLM para que este decida si necesita llamar a otra herramienta o si ya puede generar la respuesta final.
- d) Se detiene y devuelve el nombre de la herramienta que falló.

### **Pregunta 6: El decorador @tool y la documentación**
En LangChain, el "Docstring" (el texto entre `"""` justo debajo de la función) de una herramienta es:
- a) Opcional y solo sirve para que el programador humano entienda el código.
- b) Crítico, porque es lo que el LLM lee para entender cuándo y cómo debe usar esa herramienta específica.
- c) Un lugar para poner ejemplos de uso para el usuario final.
- d) El lugar donde se definen los tipos de datos de entrada.

---
*¡Este examen separa a los usuarios de los desarrolladores! Pon tus respuestas en el chat.* 💡🔥
