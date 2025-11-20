# Clase 2

## Objetivo
Modelar el proceso "Publicar Artículo" y documentar diagramas relacionados (actividad y secuencia).

## Qué se hizo en esta clase
- Modelado del flujo "Publicar Artículo" con diagrama de actividad que incluye decisión de validación.
- Ejemplo de diagrama de secuencia para el envío de comentarios.
- Guardado del código mermaid en `diagrama-secuencia.md` y exportación de la imagen del diagrama de actividad.

## Qué diagramas se crearon
- Diagrama de actividad: Publicar Artículo (validación de datos).
- Diagrama de secuencia: Envío de comentario (Visitante → ArticuloView → ComentarioController → Comentario).

## Referencias a las imágenes
- ![Diagrama de Actividad](../mermaid-diagram-2025-11-11-162438.png)
- El código mermaid fuente está en `diagrama-secuencia.md` (puede pegarse en mermaid.live o mermaidchart.com/raw para visualizar/exportar).

## Decisiones de diseño tomadas
- Validación previa al guardado: comprobar campos obligatorios (ej. título) antes de persistir.
- En caso de error, devolver el formulario con los datos ya cargados para facilitar corrección por parte del Autor.
- Mensajes claros de éxito y error tras la acción.
- Usar mermaid para mantener diagramas como texto versionable y reproducible.

## Archivos
- diagrama-secuencia.md — Código mermaid con diagrama de actividad y secuencia
- ../mermaid-diagram-2025-11-11-162438.png — Exportación del diagrama de actividad

## Prefijos de commit recomendados

Para mantener mensajes consistentes en el historial de git, usar prefijos estilo Conventional Commits. Ejemplos:

- feat: agregar sistema de categorías
- docs: actualizar README con roadmap
- refactor: reorganizar estructura de carpetas
- fix: corregir validación de comentarios

Usar estos prefijos al commitear cambios relacionados con la Clase 2 (diagramas, documentación, archivos fuente).
