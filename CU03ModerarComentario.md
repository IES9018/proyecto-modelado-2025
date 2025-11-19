# Caso de Uso: Moderar Comentarios

**Actor Principal:** Administrador

**Resumen:** El administrador puede visualizar una lista de comentarios pendientes, leer su contenido y decidir si aprobarlos para su publicación o rechazarlos definitivamente.

**Precondiciones:**
1. El Administrador debe haber iniciado sesión.
2. Deben existir comentarios con estado "PENDIENTE" en el sistema.

**Flujo Principal (el "camino feliz" - Aprobar)**
1. El Administrador accede al apartado "Panel de Moderación" desde el menú principal.
2. El sistema consulta la base de datos y muestra una lista de todos los comentarios con estado **PENDIENTE**, ordenados por fecha (del más antiguo al más reciente).
3. El Administrador selecciona un comentario de la lista para ver los detalles (autor, texto completo, fecha y artículo asociado).
4. El sistema despliega la vista de detalle del comentario con los botones "Aprobar" y "Rechazar".
5. El Administrador revisa el contenido y presiona el botón **"Aprobar"**.
6. El sistema cambia el estado del comentario a **APROBADO** en la base de datos.
7. El sistema dispara una notificación interna para que el comentario se haga visible inmediatamente en el artículo correspondiente.
8. El sistema elimina el comentario de la lista de pendientes del Panel de Moderación y muestra un mensaje de éxito: "Comentario aprobado y publicado".

**Flujos Alternativos (¿qué podría salir mal / otras decisiones?)**
* **2a. No hay pendientes:** Si el sistema no encuentra comentarios con estado PENDIENTE, muestra un mensaje: "No hay comentarios pendientes de revisión" y la lista aparece vacía.
* **5a. Rechazar comentario:**
    1. En el paso 5, el Administrador decide que el contenido es inapropiado y presiona el botón **"Rechazar"**.
    2. El sistema cambia el estado del comentario a **RECHAZADO** en la base de datos.
    3. El comentario no se publica en el artículo.
    4. El sistema elimina el comentario de la lista de pendientes y muestra un mensaje: "Comentario rechazado".
* **6a. Error de conexión:** Si al intentar guardar el nuevo estado (Aprobado/Rechazado) ocurre un error en la base de datos, el sistema muestra un mensaje de error: "No se pudo procesar la solicitud, intente nuevamente" y mantiene el comentario en la lista.