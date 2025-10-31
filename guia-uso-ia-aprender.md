### 🏫 **Institución:** IES 9-018 "Gobernador Celso Jaque"
### 📚 **Carrera:** Tecnicatura Superior en Desarrollo de Software
### 📖 **Materia:** Modelado de Software
### 👨‍🏫 **Profesor:** Paulo Alvarez
---
# Guía para Usar la IA como un Tutor de Aprendizaje

## 1. La Filosofía: Usa la IA para Aprender, no para Copiar

Las herramientas de Inteligencia Artificial (IA) como Gemini, ChatGPT o Copilot son extremadamente poderosas. En tu vida profesional, serán tan comunes como lo es un buscador de Google hoy en día. Aprender a usarlas de manera efectiva es una habilidad crucial.

Sin embargo, hay una gran diferencia entre usar la IA para que **haga tu trabajo** y usarla para que te **ayude a entender tu trabajo**.

*   **❌ Mal Enfoque (La Calculadora Mágica):** Pedirle a la IA "Dame el diagrama de clases para un blog". Obtendrás una respuesta, pero no habrás aprendido nada. Es como copiar la tarea de un compañero: apruebas el examen, pero no sabes resolver el problema.

*   **✅ Buen Enfoque (El Tutor Personal):** Usar la IA como un compañero de estudio socrático. Le presentas tu trabajo, tus dudas y tu razonamiento, y le pides que te guíe, te cuestione y te dé feedback. El objetivo es que **tú** llegues a la respuesta correcta, con la IA actuando como un andamio para tu pensamiento.

Este documento te enseñará a usar este segundo enfoque.

---

## 2. Configurando tu Tutor de IA: El Prompt Inicial

Al comenzar una nueva sesión de chat con una IA para este proyecto, tu primer mensaje debe ser un "prompt de rol". Esto establece las reglas del juego y le dice a la IA cómo quieres que se comporte. 

Copia y pega el siguiente prompt al inicio de tu conversación:

```
Asume el rol de un tutor experto en Modelado de Software y diseño orientado a objetos. Mi nombre es [Tu Nombre] y soy un estudiante que está aprendiendo estos conceptos desde cero. Estoy trabajando en un proyecto de curso llamado "Institución Digital", que es un sistema de gestión de contenidos (CMS) y blog.

Tu misión es guiarme en mi aprendizaje, no darme las soluciones directamente. Para lograr esto, debes seguir estas reglas estrictamente:

1.  **Nunca me des la solución directa a un problema de modelado.** Si te pido un diagrama completo, niégate y en su lugar, ayúdame a construirlo paso a paso.
2.  **Responde a mis preguntas con otras preguntas.** Si te pregunto "¿Está bien esta relación?", responde con "Es una buena pregunta. ¿Qué te hace pensar que podría estar bien? ¿Qué escenario del mundo real estás intentando modelar con esa línea? ¿Qué pasaría si la quitaras?".
3.  **Usa analogías y ejemplos simples.** Para conceptos complejos como "acoplamiento", "cohesión" o "patrones de diseño", explícamelos con analogías de la vida real.
4.  **Pídeme siempre que justifique mis decisiones.** Si te muestro un diagrama, pregúntame "¿Por qué decidiste que la multiplicidad fuera de 1 a muchos aquí?", "¿Cuál es la responsabilidad principal de esa nueva clase que has creado?".
5.  **Actúa como un revisor de código (o de diagramas).** Cuando te presente mi trabajo, revísalo y dame feedback constructivo en forma de preguntas y sugerencias, no de correcciones directas.

Mi primer objetivo es crear el Diagrama de Casos de Uso para el proyecto. ¿Qué debería preguntarme a mí mismo para empezar a identificar a los actores del sistema?
```

---

## 3. El Flujo de Trabajo: Cómo "Conversar" con tu Tutor

Una vez que la IA ha asumido su rol, la calidad de la ayuda que recibas dependerá de la calidad de tus preguntas. Recuerda siempre darle **contexto** y mostrarle **tu trabajo**.

**❌ Ejemplo de un MAL Prompt:**

> "¿Cómo se conectan los comentarios a los artículos?"

*¿Por qué es malo? Es vago y pide una solución directa.*

**✅ Ejemplo de un BUEN Prompt:**

> "Estoy trabajando en el Diagrama de Clases de mi proyecto. Ya tengo una clase `Articulo` y una clase `Comentario`. Estoy pensando en cómo relacionarlas. Mi primera idea es añadir un atributo `id_articulo` en la clase `Comentario`. ¿Crees que esto representa correctamente la relación? ¿O sería mejor usar una línea de asociación en el diagrama? ¿Qué ventajas tendría cada enfoque?"

*¿Por qué es bueno? Muestra tu razonamiento, presenta tu borrador de idea, hace preguntas específicas sobre conceptos (atributos vs. asociación) y le da a la IA material sobre el que puede hacerte preguntas de vuelta.*

---

## 4. Manteniendo la Memoria del Proyecto

Las IAs conversacionales mantienen el contexto dentro de una misma sesión de chat. Para evitar tener que repetir el prompt de rol y el estado de tu proyecto cada vez, sigue esta simple regla:

**Usa la misma conversación o sesión de chat para todo tu proyecto.**

No inicies un nuevo chat cada vez que tengas una pregunta. Vuelve siempre a la misma conversación. De esta manera, tu tutor de IA "recordará" tus diagramas anteriores, las dudas que has tenido y el progreso general de tu trabajo, pudiendo darte una guía mucho más coherente y efectiva.
