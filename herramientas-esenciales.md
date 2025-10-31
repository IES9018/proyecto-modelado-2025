### 🏫 **Institución:** IES 9-018 "Gobernador Celso Jaque"
### 📚 **Carrera:** Tecnicatura Superior en Desarrollo de Software
### 📖 **Materia:** Modelado de Software
### 👨‍🏫 **Profesor:** Paulo Alvarez
---
# Guía de Herramientas Esenciales para el Desarrollo

Este documento es tu guía de inicio rápido para instalar y usar las herramientas básicas que necesitaremos en este curso. El objetivo es que puedas configurar tu entorno de trabajo de forma sencilla y gratuita.

---

## 1. Git y GitHub: Tu Control de Versiones

Git es el programa que guarda el historial de tu proyecto. GitHub es la plataforma online donde alojas tus proyectos de Git para colaborar y tener una copia de seguridad.

### 1.1. Instalar Git en Windows

1.  **Ve a la página oficial de descargas de Git:** [https://git-scm.com/downloads](https://git-scm.com/downloads)
2.  El sitio debería detectar automáticamente que usas Windows. Haz clic en el enlace de descarga.
3.  Ejecuta el instalador que has descargado.
4.  El instalador te presentará muchas opciones. **No te asustes.** Para empezar, puedes dejar todas las opciones por defecto y hacer clic en "Next" en todos los pasos. La configuración estándar es perfecta para nosotros.
5.  Al finalizar la instalación, abre una nueva terminal (puedes buscar "CMD" o "PowerShell" en el menú de inicio) y escribe `git --version`. Si te responde con un número de versión (ej: `git version 2.39.1.windows.1`), ¡felicidades, Git está instalado!

### 1.2. Crear una Cuenta en GitHub

1.  **Ve a la página de GitHub:** [https://github.com/](https://github.com/)
2.  Haz clic en "Sign up" (Registrarse).
3.  Sigue las instrucciones: elige un nombre de usuario, introduce tu email y crea una contraseña. GitHub es gratuito para repositorios públicos y privados.

### 1.3. Crear tu Primer Repositorio en GitHub

Un repositorio (o "repo") es un proyecto en GitHub.

1.  Una vez que hayas iniciado sesión, haz clic en el icono `+` en la esquina superior derecha y selecciona **"New repository"**.
2.  **Dale un nombre:** Por ejemplo, `proyecto-modelado-software`.
3.  **Añade una descripción (opcional):** "Repositorio para el curso de Modelado de Software".
4.  **Elige "Public"** para que otros puedan verlo (ideal para un portafolio) o "Private" si prefieres que solo tú lo veas.
5.  **¡Muy importante!** No marques ninguna de las casillas que dicen "Add a README file", "Add .gitignore" o "Choose a license". Como ya tenemos nuestro proyecto en local, queremos empezar con un repositorio vacío.
6.  Haz clic en **"Create repository"**.

### 1.4. Subir tu Proyecto Local a GitHub

Después de crear el repositorio, GitHub te mostrará una página con instrucciones. Busca la sección que dice **"…or push an existing repository from the command line"**. Esos son los comandos que necesitas.

1.  Abre una terminal en la carpeta de tu proyecto local (donde ya hiciste `git init`).
2.  Copia y pega los tres comandos que te da GitHub, uno por uno:

    ```bash
    # 1. Conecta tu repositorio local con el repositorio remoto (en GitHub)
    git remote add origin https://github.com/tu-usuario/proyecto-modelado-software.git

    # 2. (Opcional, buena práctica) Renombra tu rama principal a "main" si no lo está ya
    git branch -M main

    # 3. Sube tus commits de la rama "main" a tu repositorio en GitHub
    git push -u origin main
    ```

### 1.5. Conceptos Clave para la Colaboración: Fork y Pull Request

Cuando trabajas en equipo o contribuyes a un proyecto que no te pertenece, el flujo de trabajo cambia un poco. En lugar de clonar directamente, se usan los "Forks" y "Pull Requests".

*   **`Fork` (Bifurcación):**
    *   **¿Qué es?** Es una **copia personal** de un repositorio completo que creas en tu propia cuenta de GitHub. Sigue siendo un repositorio de Git, pero vive bajo tu usuario.
    *   **Analogía:** Imagina que la biblioteca tiene un libro de referencia muy importante (el repositorio original). No te dejan llevártelo, pero te permiten hacer una fotocopia completa (el `Fork`). Ahora puedes trabajar sobre tu fotocopia: subrayar, tomar notas, etc., sin afectar al libro original.
    *   **¿Para qué se usa?** Para poder experimentar y hacer cambios en un proyecto sin tener permisos de escritura sobre el repositorio original.

*   **`Pull Request` (PR) (Solicitud de Fusión):**
    *   **¿Qué es?** Es una **propuesta formal** que le haces al dueño del repositorio original para que incorpore los cambios que tú has hecho en tu `Fork`.
    *   **Analogía:** Después de tomar notas y hacer mejoras en tu fotocopia del libro, vas a la biblioteca y le dices al bibliotecario: "He añadido estas aclaraciones y correcciones que creo que son muy valiosas. ¿Le gustaría incorporarlas al libro original para que todos se beneficien?". Tu propuesta, junto con tus cambios, es el `Pull Request`.
    *   **¿Para qué se usa?** Es el mecanismo principal para la colaboración en GitHub. Permite revisar los cambios, discutirlos y finalmente fusionarlos en el proyecto principal.

---

## 2. diagrams.net (draw.io): Tu Herramienta de Diagramado

Es una herramienta online y gratuita para crear nuestros diagramas UML. Es muy intuitiva.

**Acceder:** [https://app.diagrams.net/](https://app.diagrams.net/)

### Guía Rápida de la Interfaz

1.  **Panel de Formas (Izquierda):** Aquí está todo lo que necesitas. Busca las secciones llamadas **"General"** y, más abajo, **"UML"**. En la sección de UML encontrarás todas las figuras que usamos: `Actor`, `Use Case`, `Class`, etc.
2.  **Arrastrar y Soltar:** Simplemente haz clic en una forma (ej: `Actor`) y arrástrala al lienzo central.
3.  **Editar Texto:** Haz doble clic sobre cualquier forma para escribir o editar su nombre.
4.  **Crear Conectores:** Pasa el ratón sobre una forma. Verás unas flechas grises. Haz clic en una de ellas y arrastra la línea hasta otra forma para conectarlas. La herramienta creará un conector inteligente.
5.  **Panel de Estilo (Derecha):** Cuando seleccionas una forma o un conector, este panel te permite cambiar colores, estilos de línea (punteada, continua), añadir o quitar flechas, etc.
6.  **Exportar tu Trabajo:**
    *   Ve a **File > Export as > PNG...** o **JPG...**
    *   Elige las opciones (recomendado: "Include a copy of my diagram").
    *   Haz clic en "Export" y guarda la imagen en la carpeta de tu proyecto.

---

## 3. Visual Studio Code (VS Code): Tu Lector de Markdown y Editor de Código

Aunque hay muchos lectores de Markdown, te recomendamos instalar VS Code. Es un editor de código profesional, gratuito y el más popular del mundo. Aprender a usarlo te servirá para toda tu carrera.

### 3.1. ¿Qué es Markdown (.md)?

Es un lenguaje de formato de texto muy simple. Permite crear documentos bien estructurados (con títulos, negritas, listas, enlaces) usando caracteres normales. Todos los archivos de nuestro curso (`clase-1.md`, `README.md`, etc.) están escritos en Markdown.

### 3.2. Instalar VS Code

1.  **Ve a la página oficial:** [https://code.visualstudio.com/](https://code.visualstudio.com/)
2.  Haz clic en el botón de descarga para Windows.
3.  Ejecuta el instalador. Al igual que con Git, puedes aceptar todas las opciones por defecto.

### 3.3. Leer Archivos Markdown en VS Code

1.  Abre VS Code.
2.  Ve a **File > Open Folder...** y selecciona la carpeta de nuestro proyecto (`institucion-digital`).
3.  En el panel izquierdo (Explorador), verás la lista de todos los archivos del proyecto.
4.  Haz clic en un archivo `.md` (por ejemplo, `clase-1-introduccion-uml.md`). Verás el texto plano.
5.  Para verlo formateado y bonito, haz clic derecho sobre el nombre del archivo en la pestaña y selecciona **"Open Preview"** (o presiona `Ctrl+Shift+V`). Se abrirá una nueva pestaña al lado con el documento renderizado, mostrando los títulos, imágenes y enlaces correctamente.
