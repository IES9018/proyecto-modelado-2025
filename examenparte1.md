## Actor principal
ERROR #1

Ubicación: Actor Principal

Descripción:
El actor “Sistema” está definido como actor principal, lo cual es incorrecto porque los actores deben ser entidades externas al sistema y no el sistema en sí mismo. 

Corrección:
Eliminar al “Sistema” como actor. El único actor principal debería ser Administrador

## DESCRIPCION
ERROR #2

Ubicación: Descripción

Descripción: El actor definido es el Administrador, la descripcion es incorrecta ya que se menciona que el usuario lo solicita. La descripcion no es precisa 

Corrección: “El sistema permite al Administrador eliminar artículos del blog.”

## Precondiciones
ERROR #3

Ubicación: Precondiciones

Descripción:
La precondición “El artículo debe tener más de 100 comentarios” es irrelevante no es una condicion que se ponga en la descripcion
No es condicion para eliminar el articulo del sistema

Corrección:
Se elimina esa precondicion y se deja solo:
El Administrador está autenticado
El artículo existe

## Flujo Principal

ERROR #4

Ubicación: Flujo Principal – Paso 5

Descripción:
El sistema elimina el artículo inmediatamente sin solicitar confirmación previa, lo cual no es correcto para una acción destructiva, lo cual es necesario corregir para evitar problemas en el flujo.

Corrección:
Agregar un paso de confirmación en el flujo principal antes de eliminar el artículo. Mensaje de confirmacion "Esta seguro de eliminar el Articulo"

## Flujo alternativo
ERROR #5

Ubicación: Flujos Alternativos

Descripción:
Podría existir un flujo alternativo si el Administrador decide cancelar la eliminación. 

Corrección:
Agregar un flujo alternativo:
·El sistema valida los permisos del usuario.
·El Administrador cancela la eliminación → el sistema no elimina el artículo y finaliza el caso de uso.

## Precondiciones
ERROR #6

Ubicación: Postcondiciones

Descripción:
Las postcondiciones incluyen acciones como “el sistema envía un email” y “el Administrador recibe una notificación”, las cuales no representan estados finales del sistema sino comportamientos.
El sistema envía un email al autor: se puede mover esta acción al flujo principal o a un flujo alternativo. Describe una accion 

Corrección:
Dejar en las postcondiciones solo estados verificables, como:

El artículo fue eliminado
Los comentarios asociados fueron eliminados

## Excepciones
ERROR #7

Ubicación: Excepciones

Descripción:
La excepción “Si el artículo no existe” contradice la precondición que indica que el artículo debe existir y además debería tratarse como un flujo alternativo.

Corrección:

Una excepcion podria ser que ocurre un error inesperado del sistema durante la eliminación del artículo.
