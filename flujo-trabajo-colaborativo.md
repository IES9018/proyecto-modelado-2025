### 🏫 **Institución:** IES 9-018 "Gobernador Celso Jaque"
### 📚 **Carrera:** Tecnicatura Superior en Desarrollo de Software
### 📖 **Materia:** Modelado de Software
### 👨‍🏫 **Profesor:** Paulo Alvarez
---
# Flujo de Trabajo Colaborativo con Forks y Pull Requests

## 1. El "Porqué": Proteger el Proyecto y Trabajar como Profesionales

En el mundo del desarrollo de software, es fundamental tener una única fuente de verdad que sea estable y confiable. Este es el **repositorio principal** (en nuestro caso, el que vive en la organización `IES9018`). No podemos permitir que los cambios se hagan directamente sobre él sin un proceso de revisión, ya que un error podría romper el proyecto para todos.

Este flujo de trabajo resuelve ese problema usando dos herramientas clave:

*   **Fork (Bifurcación):** Le da a cada miembro del equipo (o a cada estudiante) una **copia personal y segura** del proyecto. Es tu "zona de pruebas" donde tienes control total para trabajar y experimentar sin afectar el original.

*   **Pull Request (PR) (Solicitud de Fusión):** Es el mecanismo **formal para proponer tus cambios** al proyecto principal. Un PR le dice al dueño del proyecto: "He completado un trabajo en mi copia personal, creo que es valioso y está listo. Por favor, revísalo y, si estás de acuerdo, incorpóralo al proyecto oficial".

Adoptar este modelo no solo organiza nuestro curso, sino que te enseña el estándar de colaboración que se utiliza en empresas como Google, Microsoft y en la inmensa mayoría de los proyectos de código abierto.

---

## 2. El Flujo de Trabajo Paso a Paso

### Fase 1: Preparación (Lo haces una sola vez)

1.  **Hacer "Fork" del Repositorio Base:**
    *   Navega a la página del repositorio principal de la materia en la organización `IES9018` (el profesor te dará el enlace).
    *   En la esquina superior derecha, haz clic en el botón **"Fork"**.
    *   GitHub te preguntará dónde quieres crear el fork. Selecciona tu propia cuenta de usuario.
    *   **Resultado:** ¡Felicidades! Ahora tienes una copia exacta del proyecto en tu propia cuenta de GitHub (ej: `tu-usuario/proyecto-modelado-2025`).

2.  **Clonar tu Fork a tu Computadora Local:**
    *   Ve a la página de **tu fork** (¡no el original de IES9018!).
    *   Haz clic en el botón verde **"<> Code"**.
    *   Copia la URL HTTPS que aparece.
    *   Abre una terminal en tu computadora y ejecuta:
        ```bash
        git clone URL_QUE_COPIASTE
        ```
    *   **Resultado:** Ahora tienes el proyecto en tu computadora y está conectado a tu fork personal, no al de la institución.

### Fase 2: Trabajo y Progreso (Lo haces cada vez que trabajas)

1.  **Trabaja en tu Proyecto:** Abre la carpeta en VS Code, edita los archivos `.md`, crea tus diagramas, etc.

2.  **Guarda tu Progreso con Commits:** Usa el ciclo normal de Git para guardar tus cambios.
    ```bash
    # Añade tus archivos al área de preparación
    git add .

    # Crea un "punto de guardado" con un mensaje descriptivo
    git commit -m "feat: Añade el Diagrama de Clases para la funcionalidad de Artículos"
    ```

3.  **Sube los Cambios a tu Fork:** Envía tus commits guardados a tu repositorio en GitHub.
    ```bash
    git push origin main
    ```
    *   **Resultado:** Tu copia personal en GitHub está actualizada con tu último trabajo. El repositorio de IES9018 sigue sin cambios.

### Fase 3: La Entrega (Cuando terminas una tarea o el proyecto)

1.  **Crear el Pull Request (PR):**
    *   Ve a la página de **tu fork** en GitHub.
    *   Verás un mensaje que dice "This branch is X commits ahead of IES9018:main". Haz clic en el botón **"Contribute"** y luego en **"Open pull request"**.
    *   GitHub te llevará a una página para crear el PR. La base (a donde apuntas) debe ser el repositorio de `IES9018`, y la cabeza (desde donde vienen los cambios) debe ser tu fork.
    *   **Escribe un Título y Descripción:** Dale un título claro a tu entrega (ej: "Entrega Fase 1 - Juan Pérez") y, si es necesario, añade una descripción de lo que has hecho.
    *   Haz clic en **"Create pull request"**.

2.  **Revisión y Feedback:**
    *   **Resultado:** Has creado la solicitud de entrega. Yo, como profesor, recibiré una notificación y podré ver todos tus cambios en un solo lugar.
    *   Podré dejarte comentarios directamente en tus archivos y aprobar tu entrega.
    *   Tú podrás ver mi feedback y, si es necesario, hacer más commits en tu rama para aplicar correcciones. El Pull Request se actualizará automáticamente.

Este ciclo de **Fork -> Clone -> Trabajar (commit/push) -> Pull Request** es el corazón del desarrollo de software colaborativo moderno.
