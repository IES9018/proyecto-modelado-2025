### 🏫 **Institución:** IES 9-018 "Gobernador Celso Jaque"
### 📚 **Carrera:** Tecnicatura Superior en Desarrollo de Software
### 📖 **Materia:** Modelado de Software
### 👨‍🏫 **Profesor:** Paulo Alvarez
---
# Glosario de Desarrollo de Software para Principiantes

Este glosario centraliza todos los términos técnicos que usamos en las clases. Está diseñado para ser una referencia rápida y clara, explicando los conceptos desde cero.

---

## Conceptos Generales de Software

### CMS (Content Management System)
*   **¿Qué es?** Un Sistema de Gestión de Contenidos. Es un software que permite crear, administrar y publicar contenido en un sitio web sin necesidad de tener conocimientos técnicos de programación.
*   **Analogía:** Es como usar un procesador de texto (como Microsoft Word o Google Docs) para tu sitio web. Te da una interfaz amigable con botones para poner texto en negrita, añadir imágenes y un gran botón de "Publicar", en lugar de tener que escribir código HTML y CSS a mano.
*   **¿Para qué sirve en nuestro proyecto?** "Institución Digital" es un CMS. Lo estamos diseñando para que los autores puedan escribir y publicar artículos fácilmente.

### Framework
*   **¿Qué es?** Un marco de trabajo. Es un conjunto de herramientas, librerías y reglas que te da una estructura base para construir una aplicación. No empiezas desde una hoja en blanco.
*   **Analogía:** Es como construir una casa con un kit prefabricado. El kit ya te da las paredes, el techo y las divisiones principales (la estructura). Tú te encargas de decorar el interior, poner los muebles y darle tu toque personal (la lógica específica de tu aplicación).
*   **¿Para qué sirve en nuestro proyecto?** No construiremos con un framework, pero diseñamos pensando en ellos. La arquitectura MVC, por ejemplo, es la base de frameworks web muy populares como Laravel, Django o Ruby on Rails.

### Base de Datos (Database)
*   **¿Qué es?** Un sistema organizado para almacenar, gestionar y recuperar grandes cantidades de información de forma eficiente y segura.
*   **Analogía:** Es como un archivador gigante y muy bien organizado. En lugar de tener papeles sueltos por todas partes, tienes cajones (tablas), carpetas (registros) y etiquetas (índices) que te permiten encontrar exactamente la información que necesitas al instante.
*   **¿Para qué sirve en nuestro proyecto?** Es el lugar donde se guardarán permanentemente todos los `Articulo`s, `Usuario`s y `Comentario`s de nuestro sistema.

---

## Conceptos de Modelado y UML

### UML (Unified Modeling Language)
*   **¿Qué es?** Lenguaje de Modelado Unificado. Es el lenguaje estándar, visual y gráfico, para crear los "planos" de un sistema de software.
*   **Analogía:** Es el "AutoCAD" de los arquitectos de software. Proporciona un conjunto de símbolos y diagramas estandarizados que todos en la industria entienden, al igual que los símbolos de puertas, ventanas y muros en un plano de construcción.
*   **¿Para qué sirve en nuestro proyecto?** Lo usamos para crear todos nuestros diagramas (Casos de Uso, Clases, etc.) y así diseñar nuestro sistema antes de programarlo.

### Actor
*   **¿Qué es?** Un rol que interactúa con el sistema. Puede ser una persona o incluso otro sistema informático.
*   **Analogía:** Son los "personajes" en la obra de teatro de nuestro sistema. No son personas específicas (no es "Juan Pérez"), sino el papel que juegan (un `Autor`, un `Visitante`).
*   **¿Para qué sirve en nuestro proyecto?** Nos ayuda a definir quién usará el sistema y desde qué perspectiva debemos pensar la funcionalidad.

### Caso de Uso (Use Case)
*   **¿Qué es?** Una funcionalidad específica y completa que el sistema realiza para un actor. Describe el "qué" hace el sistema, no el "cómo".
*   **Analogía:** Es una "escena" en la obra de teatro. Es una interacción completa con un resultado de valor para el personaje, como "Comprar un ticket" o "Pedir una bebida".
*   **¿Para qué sirve en nuestro proyecto?** Para definir el alcance y los requisitos funcionales. Casos de uso como `Publicar Artículo` o `Comentar Artículo` son las funcionalidades principales que debemos construir.

### Clase (Class)
*   **¿Qué es?** Una plantilla o molde para crear objetos.
*   **Analogía:** Es el "molde para hacer galletas". El molde (`Clase`) define la forma y las características (ej: forma de estrella, tamaño de 5cm). Las galletas que creas con el molde son los `Objetos`.
*   **¿Para qué sirve en nuestro proyecto?** Es el bloque de construcción fundamental de nuestro diseño. La clase `Articulo` define que todos los objetos artículo tendrán un `titulo` y un `contenido`.

### Objeto (Object)
*   **¿Qué es?** Una instancia de una clase. Es una entidad concreta que existe en la memoria del programa.
*   **Analogía:** Es la "galleta" que hemos creado usando el molde (la Clase). Mientras que la Clase es la idea, el Objeto es la cosa real.
*   **¿Para qué sirve en nuestro proyecto?** El sistema trabajará con objetos: un objeto `Articulo` específico, un objeto `Usuario` llamado "Paulo", etc.

### Atributo (Attribute)
*   **¿Qué es?** Una característica o dato que pertenece a una clase.
*   **Analogía:** Son los "ingredientes" definidos en la receta (Clase). La receta de una galleta puede especificar que necesita `harina`, `azucar` y `huevos`.
*   **¿Para qué sirve en nuestro proyecto?** Define los datos que componen nuestras clases, como el `titulo` de un `Articulo` o el `email` de un `Usuario`.

### Método (Method)
*   **¿Qué es?** Una acción o comportamiento que una clase puede realizar.
*   **Analogía:** Son los "pasos de la preparación" en la receta (Clase). La receta puede tener pasos como `mezclarIngredientes()`, `hornear()`.
*   **¿Para qué sirve en nuestro proyecto?** Define lo que nuestras clases pueden hacer, como `publicar()` un `Articulo` o `validarPassword()` de un `Usuario`.

---

## Principios y Arquitectura

### Cohesión (Cohesion)
*   **¿Qué es?** Un principio de diseño que mide qué tan enfocadas están las responsabilidades de una clase.
*   **Analogía:** Es el principio de "hacer una sola cosa, pero hacerla bien". Una navaja suiza tiene baja cohesión (hace de todo un poco). Un bisturí de cirujano tiene altísima cohesión (hace una sola cosa a la perfección).
*   **¿Para qué sirve en nuestro proyecto?** Buscamos **ALTA cohesión**. Queremos que nuestra clase `Articulo` se ocupe solo de cosas de artículos, y no de gestionar usuarios, por ejemplo. Esto hace el código más fácil de entender y mantener.

### Acoplamiento (Coupling)
*   **¿Qué es?** Un principio de diseño que mide el grado de dependencia entre dos clases.
*   **Analogía:** Imagina dos vagones de tren. Si están unidos por una barra de acero rígida, tienen alto acoplamiento: si uno se mueve bruscamente, el otro también. Si están unidos por un enganche flexible, tienen bajo acoplamiento: pueden moverse con más independencia. En software, el alto acoplamiento es malo.
*   **¿Para qué sirve en nuestro proyecto?** Buscamos **BAJO acoplamiento**. Queremos que si modificamos la clase `Usuario`, no tengamos que modificar obligatoriamente la clase `Articulo`. Esto nos da flexibilidad para cambiar partes del sistema sin romperlo todo.

### MVC (Model-View-Controller)
*   **¿Qué es?** Un patrón de **arquitectura** que organiza el código en tres capas separadas: Modelo, Vista y Controlador.
*   **Analogía:** La del restaurante:
    *   **Modelo:** La cocina, con los ingredientes y los cocineros. Gestiona los datos y la lógica.
    *   **Vista:** El menú y la presentación del plato. Es lo que el usuario ve.
    *   **Controlador:** El chef de sala (Maître). Recibe los pedidos y coordina a la cocina.
*   **¿Para qué sirve en nuestro proyecto?** Nos ayuda a organizar nuestras clases. `Articulo` y `Usuario` son parte del **Modelo**. El HTML que muestra el artículo es la **Vista**. El código que responde al clic del botón "Publicar" es el **Controlador**.

### Patrón de Diseño (Design Pattern)
*   **¿Qué es?** Una solución general y probada para un problema común en el diseño de software.
*   **Analogía:** Es una "receta de cocina" de un chef famoso. No es el plato final, sino los pasos y la técnica para resolver un problema culinario específico (ej: "cómo hacer una salsa bechamel perfecta").
*   **¿Para qué sirve en nuestro proyecto?** Nos evita "reinventar la rueda". Usamos patrones para resolver problemas como asegurar que solo haya una instancia de una clase (Singleton) o simplificar el uso de un sistema complejo (Facade).

---

## Conceptos de Git y Control de Versiones

### Git
*   **¿Qué es?** Un sistema de control de versiones. Es el software que nos permite guardar un historial de los cambios en nuestro proyecto.
*   **Analogía:** Es como la función de "Historial de versiones" de Google Docs, pero superpotenciada. Te permite ver cada cambio, quién lo hizo, cuándo, y te permite "viajar en el tiempo" a cualquier versión anterior.

### Repositorio (Repository)
*   **¿Qué es?** La carpeta del proyecto que contiene todo el código, los archivos y el historial completo de Git (en una subcarpeta oculta llamada `.git`).

### Commit
*   **¿Qué es?** Un "punto de guardado" permanente en el historial de Git.
*   **Analogía:** Es como tomar una "foto" del estado de tu proyecto en un momento dado. Cada commit tiene un código único y un mensaje que describe qué cambió.

### Rama (Branch)
*   **¿Qué es?** Una línea de desarrollo independiente dentro del repositorio.
*   **Analogía:** Imagina que la historia de tu proyecto es el tronco de un árbol (`rama main`). Cuando creas una nueva rama, es como si creciera una nueva rama del tronco. Puedes trabajar en ella (añadirle hojas y flores) sin afectar al tronco principal. 
*   **¿Para qué sirve en nuestro proyecto?** Creamos la rama `feature/comentarios` para desarrollar la funcionalidad de comentarios de forma aislada y segura, sin arriesgarnos a romper la versión estable que está en `main`.

### Fusionar (Merge)
*   **¿Qué es?** El acto de integrar los cambios de una rama en otra.
*   **Analogía:** Es cuando la rama que creció en el árbol se vuelve tan fuerte y útil que decides injertarla de nuevo en el tronco principal, combinando su crecimiento con el resto del árbol.
*   **¿Para qué sirve en nuestro proyecto?** Lo usamos para pasar los cambios de la rama `feature/comentarios` a la rama `main` una vez que la funcionalidad estuvo lista.
