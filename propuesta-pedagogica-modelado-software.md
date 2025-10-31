### 🏫 **Institución:** IES 9-018 "Gobernador Celso Jaque"
### 📚 **Carrera:** Tecnicatura Superior en Desarrollo de Software
### 📖 **Materia:** Modelado de Software
### 👨‍🏫 **Profesor:** Paulo Alvarez
---
# Propuesta Pedagógica: Modelado de Software

## 1. Fundamentación

La materia "Modelado de Software" es fundamental en la Tecnicatura Superior en Desarrollo de Software, ya que actúa como puente entre la fase de levantamiento de requerimientos y la fase de codificación. Un buen modelado permite crear software robusto, escalable y mantenible, facilitando la comunicación dentro del equipo de desarrollo y con el cliente.

Esta propuesta se enfoca en un aprendizaje progresivo y práctico, utilizando el Lenguaje Unificado de Modelado (UML) como herramienta principal. Se busca que el estudiante no solo aprenda a "dibujar" diagramas, sino que comprenda el "porqué" de cada elemento del modelo y cómo este se traduce en una solución de software de calidad.

## 2. Objetivos Generales

Al finalizar el cursado, el estudiante será capaz de:

*   Comprender la importancia del modelado en el ciclo de vida del desarrollo de software.
*   Interpretar y crear diagramas UML para representar los aspectos estáticos y dinámicos de un sistema.
*   Aplicar principios de diseño básicos para lograr software de mayor calidad.
*   Reconocer y utilizar patrones de diseño y arquitecturas de software comunes.
*   Comunicar ideas de diseño de forma clara y no ambigua a través de modelos.

## 3. Metodología

Se propone una metodología de "aprender haciendo" (learning by doing). Cada clase combinará una parte teórica con una parte práctica intensiva. Se utilizará un caso de estudio simple que evolucionará a lo largo de las tres clases, permitiendo a los estudiantes aplicar los conceptos aprendidos de forma incremental.

**Caso de Estudio Sugerido:** Un sistema simple de gestión para una biblioteca (préstamo y devolución de libros, gestión de socios y libros).

**Herramientas:** Se recomienda el uso de una herramienta de diagramado online y gratuita como `diagrams.net` (anteriormente draw.io), que es accesible y no requiere instalación.

## 4. Estructura del Curso (3 Clases de 3 horas)

---

### **Clase 1: Introducción al Modelado y Casos de Uso**

*   **Objetivos:**
    *   Entender qué es el modelado de software y su propósito.
    *   Identificar los elementos básicos de UML.
    *   Aprender a capturar los requisitos funcionales de un sistema mediante Diagramas de Casos de Uso.
*   **Contenido Teórico (1 hora):**
    *   ¿Qué es un modelo? ¿Por qué modelar?
    *   Introducción a UML: Historia, objetivos y tipos de diagramas.
    *   Diagramas de Casos de Uso: Actores, casos de uso, relaciones (include, extend, generalización).
*   **Contenido Práctico (2 horas):**
    *   Presentación del caso de estudio: "Sistema de Biblioteca".
    *   Brainstorming en grupo para identificar actores y casos de uso.
    *   Creación del Diagrama de Casos de Uso para el sistema utilizando `diagrams.net`.
    *   Redacción de la descripción de 1 o 2 casos de uso principales.

---

### **Clase 2: Modelado de la Estructura y el Comportamiento**

*   **Objetivos:**
    *   Modelar la estructura estática de un sistema con Diagramas de Clases.
    *   Modelar la interacción entre objetos con Diagramas de Secuencia.
    *   Modelar flujos de trabajo complejos con Diagramas de Actividad.
*   **Contenido Teórico (1 hora):**
    *   **Diagramas de Clases:** Clases, atributos, métodos, visibilidad, relaciones (asociación, agregación, composición, herencia).
    *   **Diagramas de Secuencia:** Líneas de vida, mensajes (síncronos, asíncronos), creación y destrucción de objetos.
    *   **Diagramas de Actividad:** Acciones, nodos de decisión, forks, joins.
*   **Contenido Práctico (2 horas):**
    *   A partir del caso de estudio, identificar las clases principales del sistema (Libro, Socio, Préstamo, etc.).
    *   Crear el Diagrama de Clases, definiendo atributos, métodos y relaciones.
    *   Modelar el flujo del caso de uso "Prestar Libro" utilizando un Diagrama de Secuencia.
    *   Modelar el proceso completo de "Devolución de Libro" (incluyendo posibles multas) con un Diagrama de Actividad.

---

### **Clase 3: Principios de Diseño, Patrones y Arquitecturas**

*   **Objetivos:**
    *   Comprender principios de diseño clave como la cohesión y el acoplamiento.
    *   Introducir el concepto de Patrones de Diseño y ver ejemplos simples.
    *   Introducir el concepto de Arquitecturas de Software (MVC).
    *   Entender cómo el modelado se integra en metodologías ágiles.
*   **Contenido Teórico (1.5 horas):**
    *   **Principios de Diseño:** Descomposición, cohesión (alta), acoplamiento (bajo).
    *   **Patrones de Diseño:** ¿Qué son y por qué son útiles? Ejemplos de patrones creacionales (Singleton, Factory Method) y estructurales (Facade).
    *   **Arquitecturas de Software:** Concepto de vistas. Arquitectura Modelo-Vista-Controlador (MVC).
    *   **Modelado en Metodologías Ágiles:** El rol del "just enough" design y la refactorización.
*   **Contenido Práctico (1.5 horas):**
    *   Revisar el Diagrama de Clases de la Clase 2 y discutir cómo mejorar su cohesión y acoplamiento.
    *   Aplicar el patrón Singleton a una clase `Biblioteca` para asegurar una única instancia.
    *   Bosquejar cómo se aplicaría la arquitectura MVC al caso de estudio.
    *   Discusión final: ¿Cómo estos modelos nos ayudarían a planificar un "sprint" en una metodología ágil?

## 5. Evaluación

La evaluación será continua y formativa, basada en la participación activa en clase and la entrega de los diagramas generados.

*   **Clase 1:** Entrega del Diagrama de Casos de Uso.
*   **Clase 2:** Entrega de los Diagramas de Clases, Secuencia y Actividad.
*   **Clase 3:** Entrega del Diagrama de Clases refactorizado y discusión sobre la aplicación de patrones y arquitecturas.

Este enfoque práctico asegura que los estudiantes no solo memoricen conceptos, sino que desarrollen la habilidad de aplicar el modelado de software a problemas concretos.
