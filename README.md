### 🏫 **Institución:** IES 9-018 "Gobernador Celso Jaque"
### 📚 **Carrera:** Tecnicatura Superior en Desarrollo de Software
### 📖 **Materia:** Modelado de Software
### 👨‍🏫 **Profesor:** Paulo Alvarez
---
# Proyecto de Aprendizaje: Modelado de Software - Institución Digital

## ¡Bienvenido/a!

Este repositorio contiene todo el material de clase para la materia "Modelado de Software". Nuestro objetivo es aprender los fundamentos del diseño y la arquitectura de software de una manera práctica y aplicada. Para ello, no solo estudiaremos teoría, sino que construiremos, paso a paso, el modelo de un proyecto real: un Sistema de Gestión de Contenidos (CMS) llamado **"Institución Digital"**.

---

## ¿Cómo Usar este Repositorio?

Sigue estos pasos para sacar el máximo provecho del material.

### Paso 1: Clona el Repositorio

Para tener una copia completa del proyecto en tu computadora, necesitarás clonar este repositorio. Abre una terminal o línea de comandos y ejecuta el siguiente comando (reemplaza la URL con la URL real de tu repositorio de GitHub):

```bash
# Clona el proyecto a tu máquina local
git clone https://github.com/IES9018/proyecto-modelado-2025.git

# Entra en la carpeta del proyecto
cd tu-repositorio
```

### Paso 2: Sigue las Clases en Orden

El aprendizaje está diseñado para ser progresivo. Los archivos más importantes son los tutoriales de cada clase. Debes seguirlos en orden:

1.  **[`clase-1-introduccion-uml.md`](./clase-1-introduccion-uml.md)**: Aprenderás los conceptos básicos, a definir los requisitos de un sistema con Casos de Uso y tus primeros comandos de Git.
2.  **[`clase-2-diagramas-uml.md`](./clase-2-diagramas-uml.md)**: Diseñarás la estructura interna del sistema con Diagramas de Clases y modelarás sus flujos con Diagramas de Secuencia y Actividad.
3.  **[`clase-3-principios-patrones-arquitecturas.md`](./clase-3-principios-patrones-arquitecturas.md)**: Aprenderás a refinar tu diseño con principios profesionales, patrones y la arquitectura MVC para que tu software sea de alta calidad.

### Paso 3: Consulta el Glosario

¿Encuentras un término que no entiendes? ¡No hay problema! El archivo [`glosario-desarrollo-software.md`](./glosario-desarrollo-software.md) es tu diccionario personal. Contiene explicaciones sencillas, analogías y ejemplos de todos los conceptos técnicos que veremos.

### Paso 4: Explora el Historial (Para los Curiosos)

Una de las herramientas más poderosas para aprender es ver cómo se construyó el proyecto. Puedes usar el comando `git log` en tu terminal para ver el historial de todos los "puntos de guardado" (commits). Prueba este comando para una vista gráfica y resumida:

```bash
git log --oneline --graph --all
```

Esto te mostrará las ramas y cómo se fueron fusionando, permitiéndote entender el flujo de trabajo real de un desarrollador.

---

## Estructura de Archivos

> **Nota sobre Diagramas:** Este repositorio utiliza [Mermaid](https://mermaid-js.github.io/mermaid/#/) para la creación de diagramas directamente en Markdown. Puedes copiar el código de cualquier diagrama Mermaid y pegarlo en [mermaid.live](https://mermaid.live/) para visualizarlo y experimentar con él.

*   `README.md`: Esta guía que estás leyendo.

**Documentos de Apoyo y Flujo de Trabajo:**

*   [`herramientas-esenciales.md`](./herramientas-esenciales.md): **(Leer primero)** Guía de instalación y uso de Git, GitHub, diagrams.net y VS Code.
*   [`flujo-trabajo-colaborativo.md`](./flujo-trabajo-colaborativo.md): **(Muy importante)** Explica cómo usar Forks y Pull Requests, el método que usaremos para las entregas.
*   [`CHANGELOG.md`](./CHANGELOG.md): Documenta todos los cambios significativos en el material del curso, ideal para entender la evolución del proyecto.
*   [`guia-uso-ia-aprender.md`](./guia-uso-ia-aprender.md): **(Recomendado)** Enseña cómo usar una IA como Gemini de forma efectiva y ética para potenciar tu aprendizaje.
*   [`fundamentos-arquitectura-software.md`](./fundamentos-arquitectura-software.md): Lectura recomendada para entender los conceptos de alto nivel detrás de nuestras decisiones de diseño.
*   [`glosario-desarrollo-software.md`](./glosario-desarrollo-software.md): Tu diccionario de consulta para todos los términos técnicos.

**Documentos del Proyecto y Tarea:**

*   [`tarea-proyecto-final.md`](./tarea-proyecto-final.md): **(Importante)** Contiene las instrucciones detalladas de la tarea final del curso.
*   [`rubrica-evaluacion.md`](./rubrica-evaluacion.md): Describe cómo será evaluado tu trabajo.
*   [`LISTA_ESTUDIANTES.md`](./LISTA_ESTUDIANTES.md): Directorio con los enlaces a los repositorios de todos los compañeros para la revisión por pares.

**Tutoriales del Proyecto:**

*   [`clase-1-introduccion-uml.md`](./clase-1-introduccion-uml.md): **(Empezar aquí)** Tutorial de la Clase 1.
*   [`clase-2-diagramas-uml.md`](./clase-2-diagramas-uml.md): Tutorial de la Clase 2.
*   [`clase-3-principios-patrones-arquitecturas.md`](./clase-3-principios-patrones-arquitecturas.md): Tutorial de la Clase 3.

**Documentos del Curso:**

*   [`propuesta-pedagogica-modelado-software.md`](./propuesta-pedagogica-modelado-software.md): Documento con la estrategia pedagógica general del curso.

**Diagramas del Sistema (Mermaid):**

*   [`diagrama-sistema-completo.md`](./diagrama-sistema-completo.md): Visión general y evolutiva del sistema "Institución Digital" a través de diagramas Mermaid.

---

## Tarea del Proyecto Final

La evaluación principal de este curso se basa en la construcción de tu propio proyecto "Institución Digital". Todos los detalles, instrucciones de entrega y expectativas están en los siguientes documentos:

*   **[Instrucciones de la Tarea](./tarea-proyecto-final.md):** Lee este documento cuidadosamente para saber qué tienes que hacer.
*   **[Rúbrica de Evaluación](./rubrica-evaluacion.md):** Consulta este documento para entender cómo será evaluado tu trabajo.

---

# vane_legui-blog v1.0.0

> Mi propia versión de CMS/Blog, fork de "Institución Digital" con funcionalidades únicas.

## 🌟 Qué hace único a vane_legui-blog

- **Sistema de categorías mejorado** para organizar artículos de forma intuitiva.
- **Interfaz simplificada** para escritura rápida y productiva.
- **Soporte para filtros por categoría** en la vista pública (próximamente: editor Markdown integrado).
- **Autenticación segura** con gestión de sesiones.
- **Sistema de comentarios bidireccional** donde autores y visitantes interactúan.
- **Validación y sanitización** de datos para máxima seguridad.

## 📋 Descripción General

**vane_legui-blog** es una plataforma de blogging construida siguiendo principios de modelado de software, patrones de diseño y buenas prácticas de desarrollo web. Permite a autores publicar contenido, a visitantes comentar artículos y a administradores gestionar el sistema de forma segura y eficiente.

## 🏗️ Arquitectura

El proyecto está estructurado en capas:

```
vane_legui-blog/
├── docs/                    # Documentación y diagramas
│   ├── diagramadeflujo.md  # Diagramas de casos de uso y secuencias
│   └── ...
├── src/                     # Código fuente (backend/frontend)
│   ├── controllers/
│   ├── services/
│   ├── models/
│   └── views/
├── tests/                   # Pruebas unitarias e integración
├── scripts/                 # Scripts de utilidad
├── README.md                # Este archivo
└── .gitignore
```

## 🚀 Instalación

### Requisitos previos
- Node.js 16+ o Python 3.9+
- Git
- npm o pip (según el stack)

### Pasos

1. **Clonar el repositorio**
   ```bash
   git clone https://github.com/vanes-legui/proyecto-modelado-2025.git
   cd proyecto-modelado-2025
   ```

2. **Instalar dependencias**
   ```bash
   npm install
   # o si usas Python:
   pip install -r requirements.txt
   ```

3. **Configurar variables de entorno**
   ```bash
   cp .env.example .env
   # Editar .env con tus valores (URL DB, puerto, etc.)
   ```

4. **Iniciar el servidor**
   ```bash
   npm start
   # o: python app.py
   ```

5. **Acceder a la aplicación**
   ```
   http://localhost:3000
   ```

## 📖 Uso

### Para Autores
1. Registrarse o iniciar sesión.
2. Crear un nuevo artículo desde el panel "Mis Artículos".
3. Seleccionar categoría y publicar.
4. Ver comentarios en tiempo real.

### Para Visitantes
1. Navegar por artículos publicados sin autenticación.
2. Filtrar artículos por categoría.
3. Iniciar sesión para dejar comentarios.
4. Ver respuestas de autores en el mismo artículo.

### Para Administradores
1. Acceder al panel de administración.
2. Moderar comentarios y artículos.
3. Eliminar contenido inapropiado.
4. Ver estadísticas de usuarios y artículos.

## 🔄 Flujos Principales

### Publicar Artículo
```
Autor → Completa formulario → Selecciona categoría → Validación → Guardado en BD → Publicación
```

### Comentar Artículo
```
Visitante → Autentica → Escribe comentario → Validación → Guardado → Confirmación visual
```

### Leer Comentarios
```
Autor → Navega a artículo → Ve lista de comentarios → Filtra/Ordena por fecha
```

## 📊 Diagramas

Consulta los diagramas UML en [`docs/diagramadeflujo.md`](docs/diagramadeflujo.md):
- **Diagrama de Clases**: Entidades Usuario, Artículo, Comentario, Categoría.
- **Diagrama de Casos de Uso**: Actores y sus interacciones.
- **Diagrama de Secuencia**: Flujo detallado de publicación de comentarios.

## 🧪 Pruebas

Ejecutar suite de pruebas:
```bash
npm test
# o: pytest tests/
```

Cobertura de pruebas:
```bash
npm run test:coverage
```

## 🔐 Seguridad

- ✅ Contraseñas hasheadas (bcrypt/argon2).
- ✅ Validación y sanitización en servidor.
- ✅ Protección CSRF.
- ✅ Rate limiting en endpoints sensibles.
- ✅ Autenticación JWT o sesiones seguras.

## 📦 Dependencias Principales

- **Backend**: Express.js (Node) / Flask (Python)
- **Base de Datos**: PostgreSQL / MongoDB
- **Autenticación**: JWT / Session-based
- **Validación**: Joi / Yup / Pydantic
- **Frontend**: React / Vue (si aplica)

## 🤝 Contribuir

1. Fork el repositorio.
2. Crea una rama feature: `git checkout -b feature/tu-funcionalidad`.
3. Commit cambios: `git commit -m "feat: descripción"`.
4. Push a tu fork: `git push origin feature/tu-funcionalidad`.
5. Abre un Pull Request en `main`.

Consulta [`CONTRIBUTING.md`](CONTRIBUTING.md) para detalles.

## 📝 Ramas de Trabajo

- **main**: Versión estable y lista para producción.
- **develop**: Rama de desarrollo; nuevas features aquí.
- **feature/***: Ramas feature (ej: `feature/comentarios`, `feature/categorias`).
- **bugfix/***: Ramas para correcciones (ej: `bugfix/validacion`).
- **docs/***: Ramas para documentación (ej: `docs/diagrama-flujo`).

## 🚀 Basado en

Este proyecto es un fork independiente de [IES9018/proyecto-modelado-2025](https://github.com/IES9018/proyecto-modelado-2025), el repositorio oficial del curso "Modelado de Software" en la Institución IES 9-018.

## 📜 Roadmap

- [x] **v1.0.0** - Sistema base de blog
  - Autenticación de usuarios
  - CRUD de artículos
  - Sistema de comentarios
  - Diagramas UML (Clases, Casos de Uso, Secuencias)
  
- [ ] **v1.1.0** - Sistema de categorías
  - Crear/editar/eliminar categorías
  - Asignar categorías a artículos
  - Filtros por categoría en vista pública
  - Validación de categorías duplicadas
  
- [ ] **v1.2.0** - Sistema de etiquetas
  - Etiquetas (tags) para artículos
  - Nube de etiquetas
  - Búsqueda por etiqueta
  - Autocomplete en formulario
  
- [ ] **v2.0.0** - Editor Markdown integrado
  - Editor WYSIWYG para artículos
  - Preview en tiempo real
  - Soporte para imágenes embebidas
  - Exportación a PDF

## 📄 Licencia

MIT License - Ver [LICENSE](LICENSE).

## 👤 Autor

**Vanesa Legui** - [GitHub](https://github.com/vanes-legui)

## 📧 Contacto

Para preguntas o sugerencias, abrí un issue o contactame en tu correo.

---

**Última actualización**: 17 de noviembre de 2025
