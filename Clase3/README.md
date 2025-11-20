# Clase 3

## Objetivo
Modelar y documentar el proceso de publicación de artículos y los diagramas asociados (actividad, decisiones y flujo de errores).

## Qué se hizo en esta clase
- Modelado del flujo completo de "Publicar Artículo" incluyendo autenticación, validación, sanitización y persistencia.
- Creación de diagramas (actividad y flujo detallado) y descripción textual de la imagen del diagrama.
- Exportación de la imagen del diagrama y guardado del código fuente (mermaid/drawio).

## Qué diagramas se crearon
- Diagrama de actividad: Publicar Artículo (incluye decisiones: autenticación, validación de datos, resultado de guardado).
- Diagrama de flujo/estado: Manejo de errores y redirección tras publicación.
- (Opcional) Versión en mermaid para facilitar exportaciones y edición.

## Referencias a las imágenes
- ./imagenes/publicar-articulo-diagrama.png — Exportación del diagrama de publicación
- ./diagramas/publicar-articulo.drawio — Fuente editable (draw.io)
- El código mermaid fuente se encuentra en `diagrama-secuencia.md` o en `diagramas/publicar-articulo.mmd`

## Decisiones de diseño tomadas
- Verificar autenticación antes de permitir el envío del formulario.
- Validar campos obligatorios (título, contenido) y devolver errores si faltan datos.
- Mantener los datos del formulario cargados cuando hay errores para facilitar la corrección.
- Sanitizar la entrada antes de persistir para prevenir inyección.
- Mostrar mensajes claros al usuario: “Inicia sesión para publicar”, “Error al guardar”, “Artículo publicado con éxito”.
- Usar mermaid/draw.io para mantener diagramas versionables y exportables.

## Descripción de la imagen (basada en el diagrama)
La imagen muestra un diagrama de flujo que representa el proceso para publicar un artículo. El flujo va de arriba hacia abajo e incluye acciones, decisiones y mensajes al usuario. Estructura principal:
- Inicio.
- Decisión: "¿Usuario autenticado?" — Si NO: mostrar "Inicia sesión para publicar" y finalizar; si SÍ: continuar al formulario.
- Acción: Autor rellena el formulario y presiona "Publicar".
- Decisión: "¿Datos válidos y completos?" — Si NO: mostrar error, recargar formulario con datos previos y permitir reintento; si SÍ: sanitizar entrada y proceder a guardar.
- Decisión: "¿Guardado exitoso?" — Si NO: mostrar "Error al guardar" y finalizar; si SÍ: mostrar "Artículo publicado con éxito", redirigir a la vista del artículo y finalizar.

## Archivos
- diagramas/publicar-articulo.drawio — Fuente editable
- imagenes/publicar-articulo-diagrama.png — Exportación para documentación
- diagrama-secuencia.md — Código mermaid con los diagramas y ejemplos
