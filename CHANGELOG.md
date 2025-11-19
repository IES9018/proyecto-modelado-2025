# Changelog - EzeBlog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.1.0] - 2025-11-18

### Added (Agregado)
- **Sistema de Categorías Mejorado (Feature Único):**
    - Se incluye el modelado completo (Diagrama de Clases, Secuencia y Actividad) para la entidad `Categoria`.
    - Implementación de la relación Muchos a Muchos entre `Articulo` y `Categoria`.
    - Agregado el panel de administración para la gestión completa de categorías.
    - Filtro de artículos por categoría en la vista pública.
- Se añaden diagramas que refuerzan la estructura MVC y la aplicación del patrón Facade.
- **Diagrama de clases para el sistema de categorías (Clase4/diagrama-clase-categoria.png)**.

### Changed (Cambiado)
- Actualización de los Diagramas de Clases existentes para reflejar la relación con la nueva entidad `Categoria`.
- El `README.md` se actualiza para documentar el lanzamiento v1.1.0.
- Mejorada la interfaz de creación de artículos (UX).

## [1.0.0] - 2025-11-18

### Added (Agregado)
- **Lanzamiento Inicial de EzeBlog:** Creación del proyecto independiente a partir del *fork* de "Institución Digital".
- **Versionado Semántico (SemVer):** Establecimiento del sistema de versiones MAJOR.MINOR.PATCH.
- **Base de Modelado Completa:** Incluye los diagramas de UML (Clases, Secuencia, Actividad) y documentación de arquitectura (MVC, Cohesión/Acoplamiento) de las Clases 1 a 3.