# Proyecto — Landing Page Profesional / Institución Digital

Breve documento técnico y operativo del repositorio: descripción, instalación, estructura, licencias y normas de contribución.

---

## 🚀 Descripción
Landing page profesional, optimizada para rendimiento, accesibilidad y escalabilidad. Orientada a presentación de productos, servicios o portafolio con diseño responsive y código modular.

Incluye:
- Diseño responsive y accesible.
- Estructura modular (componentes, estilos, assets).
- Buenas prácticas y guía para contribuir.

---

## 🧩 Tecnologías
- HTML5, CSS3, JavaScript
- Opcional: React / Vue / Angular
- Control de versiones con Git

---

## 📁 Estructura recomendada

```bash
proyecto-landing-page/
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

---

## 📦 Instalación

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

---

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

---

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

---

## 📊 Diagramas

Consulta los diagramas UML en [`docs/diagramadeflujo.md`](docs/diagramadeflujo.md):
- **Diagrama de Clases**: Entidades Usuario, Artículo, Comentario, Categoría.
- **Diagrama de Casos de Uso**: Actores y sus interacciones.
- **Diagrama de Secuencia**: Flujo detallado de publicación de comentarios.

---

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

---

## 🔐 Seguridad

- ✅ Contraseñas hasheadas (bcrypt/argon2).
- ✅ Validación y sanitización en servidor.
- ✅ Protección CSRF.
- ✅ Rate limiting en endpoints sensibles.
- ✅ Autenticación JWT o sesiones seguras.

---

## 📦 Dependencias Principales

- **Backend**: Express.js (Node) / Flask (Python)
- **Base de Datos**: PostgreSQL / MongoDB
- **Autenticación**: JWT / Session-based
- **Validación**: Joi / Yup / Pydantic
- **Frontend**: React / Vue (si aplica)

---

## 🤝 Contribuir

1. Fork el repositorio.
2. Crea una rama feature: `git checkout -b feature/tu-funcionalidad`.
3. Commit cambios: `git commit -m "feat: descripción"`.
4. Push a tu fork: `git push origin feature/tu-funcionalidad`.
5. Abre un Pull Request en `main`.

Consulta [`CONTRIBUTING.md`](CONTRIBUTING.md) para detalles.

---

## 📝 Ramas de Trabajo

- **main**: Versión estable y lista para producción.
- **develop**: Rama de desarrollo; nuevas features aquí.
- **feature/***: Ramas feature (ej: `feature/comentarios`, `feature/categorias`).
- **bugfix/***: Ramas para correcciones (ej: `bugfix/validacion`).
- **docs/***: Ramas para documentación (ej: `docs/diagrama-flujo`).

---

## 🚀 Basado en

Este proyecto es un fork independiente de [IES9018/proyecto-modelado-2025](https://github.com/IES9018/proyecto-modelado-2025), el repositorio oficial del curso "Modelado de Software" en la Institución IES 9-018.

---

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

---

## 📄 Licencia

MIT License - Ver [LICENSE](LICENSE).

---

## 👤 Autor

**Vanesa Legui** - [GitHub](https://github.com/vanes-legui)

## 📧 Contacto

Para preguntas o sugerencias, abrí un issue o contactame en tu correo.

---

**Última actualización**: 17 de noviembre de 2025
