ERROR #1

Ubicación: Actor Principal

Descripción:
Se incluye al Sistema como actor principal. Un actor debe ser una entidad externa al sistema; el sistema no puede interactuar consigo mismo.

Corrección:
Eliminar “Sistema” de los actores.
Actor Principal correcto: Administrador.

ERROR #2

Ubicación: Actores

Descripción:
No se especifican actores secundarios, a pesar de que el sistema envía correos/notificaciones al autor del artículo.

Corrección:
Agregar actor secundario:

Sistema de Notificaciones o Servicio de Email.

ERROR #3

Ubicación: Precondiciones

Descripción:
La precondición “El artículo debe tener más de 100 comentarios” no es una condición necesaria para ejecutar el caso de uso. Es una regla arbitraria sin justificación funcional.

Corrección:
Reemplazar por:

El usuario está autenticado como Administrador

El artículo existe en el sistema

ERROR #4

Ubicación: Flujo Principal – Paso 5

Descripción:
El artículo se elimina de forma inmediata, sin solicitar confirmación al usuario. En operaciones destructivas debe existir confirmación.

Corrección:
Agregar:
5. El sistema solicita confirmación de eliminación
6. El Administrador confirma
7. El sistema elimina el artículo

ERROR #5

Ubicación: Flujos Alternativos

Descripción:
Se indica “Ninguno”, pero existen flujos alternativos evidentes, como cuando el Administrador cancela la operación.

Corrección:
Agregar:

FA1: Cancelar eliminación

Si el Administrador cancela, el sistema no elimina el artículo

El sistema muestra mensaje “Operación cancelada”

Retorna a la lista de artículos

ERROR #6

Ubicación: Postcondiciones

Descripción:
Algunas postcondiciones no representan estados finales del sistema, sino acciones del proceso:

“El sistema envía un email al autor”

“El Administrador recibe una notificación”

Corrección:
Dejar solo postcondiciones que describan el estado final:

El artículo ya no existe en la base de datos

Los comentarios asociados fueron eliminados

ERROR #7

Ubicación: Excepciones

Descripción:
La excepción “Si el artículo no existe” es redundante, ya que en las precondiciones se establece que el artículo debe existir. Si la precondición no se cumple, el caso de uso no debería ejecutarse.

Corrección:
Eliminar la excepción o moverla a un flujo alternativo:

FA2: Artículo no encontrado

El sistema informa que el artículo no existe

Retorna a la lista de artículos

---

Nota: Las correcciones anteriores se han añadido tal como se solicitó para incluirlas en el examen.

