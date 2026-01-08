Caso de Uso con Errores
CU-05: Eliminar Artículo
Actor Principal: Sistema, Administrador

Descripción:
El sistema permite eliminar artículos del blog cuando el usuario lo solicita.

Precondiciones:

El artículo debe existir en la base de datos
El artículo debe tener más de 100 comentarios
Flujo Principal:

El Administrador accede al panel de control
El Administrador selecciona la opción "Gestionar Artículos"
El sistema muestra la lista de artículos
El Administrador hace clic en "Eliminar" junto al artículo deseado
El sistema elimina el artículo inmediatamente
El sistema muestra mensaje "Artículo eliminado"
Fin del caso de uso
Flujos Alternativos:

Ninguno
Postcondiciones:

El artículo ya no existe en la base de datos
El sistema envía un email al autor
Todos los comentarios asociados se eliminan
El Administrador recibe una notificación
Excepciones:

Si el artículo no existe, el sistema muestra un error

## SOLUCIONES

## Actor Principal 1
sistema no puede ser actor principal porque los actores deben ser externos al sistema

## Descripción 2
La descripción debe enfocarse en la acción del actor, no del sistema


## Precondiciones 3
El artículo debe tener más de 100 comentarios

No es una condición lógica ni necesaria para eliminar un artículo.
Representa una regla arbitraria que no corresponde a una precondición válida.


## Flujo Principal 4
El sistema elimina el artículo inmediatamente

Eliminar un artículo es una acción destructiva y debe requerir confirmación del usuario.
Se deberían agregar pasos

# Flujos Alternativos 5
ninguno

pueden haber, como si el usuario quisiera cancelar la operación de eliminar, el sistema no elimina el archivo

## Postcondiciones 6

El sistema envía un email al autor
El Administrador recibe una notificación

Las postcondiciones deben describir estados finales del sistema, no acciones.

## También Falta de actor secundario 7

Ubicación: Actores / Postcondiciones

Se menciona el envío de emails/notificaciones sin definir un actor externo responsable.

Actor Secundario: Sistema de Notificaciones
