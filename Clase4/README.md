# Clase 4

## Objetivo
Modelar y documentar comportamientos y arquitectura del blog (flujo de publicación y diagrama MVC) y mantener las fuentes de los diagramas en el repositorio.

## Qué se hizo en esta clase
- Documentación y refinamiento del flujo de publicación (incluye autenticación, validación, sanitización, persistencia y manejo de errores).
- Modelado de la arquitectura MVC que soporta el proceso (Modelo, Controlador, Vista).
- Exportación de imágenes de los diagramas y almacenamiento de las fuentes editables (draw.io / mermaid).
- Redacción de descripciones detalladas de las imágenes para la documentación del proyecto.

## Qué diagramas se crearon
- Diagrama de flujo / actividad: Proceso de publicación de artículo (inicio, autenticación, validación, sanitización, guardado, mensajes y redirecciones).
- Diagrama MVC: Arquitectura del blog con entidades Modelo, Controladores y Vistas y sus interacciones.
- Fuentes: draw.io (.drawio) y/o mermaid (.mmd / .md) para cada diagrama.

## Referencias a las imágenes
- imagenes/publicar-articulo-flujo.png — Diagrama de flujo del proceso de publicación
- imagenes/blog-mvc-diagrama.png — Diagrama MVC del blog
- diagramas/publicar-articulo.drawio — Fuente editable (draw.io)
- diagramas/blog-mvc.drawio — Fuente editable (draw.io)
- diagrama-secuencia.md — Código mermaid con ejemplos de secuencia y actividad

## Decisiones de diseño tomadas
- Comprobar autenticación antes de permitir la publicación.
- Validar campos obligatorios (título, contenido) y devolver errores locales al formulario.
- Mantener los datos del formulario cuando hay errores para facilitar corrección del autor.
- Sanitizar entradas antes de persistir para prevenir inyección y XSS.
- Mostrar mensajes claros de estado (iniciar sesión, error en datos, error al guardar, publicado con éxito).
- Usar formatos editables (draw.io, mermaid) para versionado y exportación a PNG para documentación.
- Separación de responsabilidades siguiendo MVC: lógica en SistemaBlog/Controladores, persistencia en Modelo, presentación en Vistas.

## Descripción completa y detallada de las imágenes

### Imagen 1 – Diagrama de Flujo del Proceso de Publicación
La imagen representa verticalmente el flujo para publicar un artículo, usando nodos rectangulares (acciones) y rombos (decisiones). Pasos principales:
1. Inicio.
2. Decisión: "¿Usuario autenticado?"
   - Si NO: mostrar “Inicia sesión para publicar” → Fin.
   - Si SÍ: ir a rellenar formulario.
3. Acción: Autor rellena formulario y presiona "Publicar".
   - Aparecen bloques que muestran interacción MVC: SistemaBlog: publicarArticulo() y ArticuloController (el controlador recibe datos y llama al sistema).
4. Decisión: "¿Datos válidos y completos?"
   - Si NO: mostrar mensaje de error, recargar formulario con datos previos, permitir reintento.
   - Si SÍ: sanitizar entrada y proceder a guardar en BD.
5. Decisión: "¿Guardado exitoso?"
   - Si NO: mostrar "Error al guardar" → Fin.
   - Si SÍ: mostrar "Artículo publicado con éxito", redirigir a la vista del artículo → Fin.

La imagen ilustra además pasos de sanitización y manejo de errores en cada punto crítico, con flechas que regresan al formulario cuando corresponde.

### Imagen 2 – Diagrama MVC del Blog
Diagrama dividido en tres columnas: Modelo, Controlador, Vista. Elementos y relaciones:
- Modelo:
  - Usuario: notifica cambios, se relaciona con autenticación, Artículo y Comentario.
  - ServicioAutenticacionUsuario: valida credenciales y comunica login/logout.
  - Artículo y Comentario: entidades persistentes.
- Controlador:
  - ArticuloController: recibe acciones desde FormularioArtículo y llama a SistemaBlog.publicarArticulo(datos); interactúa con el modelo Artículo.
  - ComentarioController: procesa comentarios y llama a SistemaBlog.dejarComentario(datos); interactúa con modelo Comentario.
  - SistemaBlog: núcleo lógico que centraliza operaciones de publicación y comentarios y devuelve resultados a controladores.
- Vista:
  - FormularioArtículo: envía acciones al controlador (publicar).
  - PáginaArtículo: muestra artículo publicado y recibe notificaciones del modelo.
  - ListaComentarios: muestra comentarios y se actualiza según notificaciones del modelo.

Las flechas entre columnas están etiquetadas con relaciones (envía acciones, interactúa con, notifica cambios), dejando claro el flujo de datos entre usuario, vista, controlador y modelo.

## Plantilla sugerida (ejemplo de Clase1/README.md)
## Objetivo
Modelar los requisitos funcionales de vane_legui-blog usando diagramas de casos de uso.

## Actores identificados
- Autor
- Visitante
- Administrador

## Casos de Uso principales
1. Publicar Artículo
2. Leer Artículo
3. Comentar Artículo
4. Gestionar Categorías

## Diagrama
![Casos de Uso](casos-uso-vane-legui.png)

## Archivos
- casos-uso-vane-legui.drawio — Fuente editable
- casos-uso-vane-legui.png — Exportación para documentación

## Archivos de esta clase
- diagramas/publicar-articulo.drawio
- diagramas/blog-mvc.drawio
- imagenes/publicar-articulo-flujo.png
- imagenes/blog-mvc-diagrama.png
- diagrama-secuencia.md
