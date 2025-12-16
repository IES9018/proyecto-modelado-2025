##📋 Consigna
##A continuación se presenta un caso de uso con 7 errores intencionales. Tu tarea es:

Identificar mínimo 5 errores
Explicar por qué es un error
Proponer la corrección apropiada

Formato de respuesta:

ERROR #1:
Ubicación: [Sección donde está el error]
Descripción: [Qué está mal]
Corrección: [Cómo debería ser]

📄 Caso de Uso con Errores
CU-05: Eliminar Artículo
Actor Principal: Sistema, Administrador

Descripción:
El sistema permite eliminar artículos del blog cuando el usuario lo solicita.

Precondiciones:

El artículo debe existir en la base de datos
El artículo debe tener más de 100 comentarios

Flujo Principal:

1. El Administrador accede al panel de control
2. El Administrador selecciona la opción "Gestionar Artículos"
3. El sistema muestra la lista de artículos
4. El Administrador hace clic en "Eliminar" junto al artículo deseado
5. El sistema elimina el artículo inmediatamente
6. El sistema muestra mensaje "Artículo eliminado"
7. Fin del caso de uso
   
Flujos Alternativos:

Ninguno

Postcondiciones:

El artículo ya no existe en la base de datos
El sistema envía un email al autor
Todos los comentarios asociados se eliminan
El Administrador recibe una notificación

Excepciones:

Si el artículo no existe, el sistema muestra un error

Error #1
Ubicación: [Actor principal]
Descripción: [El actor principal no puede ser el sistema tiene que ser una entidad externa]
Corrección: [Administrador]

Error #2
Ubicación: [Precondiciones 2]
Descripción: [La precondicion debe ser algo que sea verdad antes de empezar, tener 100 comentarios no es logico para todos los articulos]
Corrección: [Eliminar la precondicion 2]

Error #3
Ubicación: [Flujo principal punto 5]
Descripción: [como es una accion destructiva el sistema tiene que pedir confirmacion antes de eliminar]
Corrección: [El sistema pide confirmacion al administrador]

Error #4
Ubicación: [Flujo principal punto 5]
Descripción: [como es una accion destructiva el sistema tiene que pedir confirmacion antes de eliminar]
Corrección: [El sistema pide confirmacion al administrador]

Error #5
Ubicación: [Postcondicion 3 y 4]
Descripción: [La postcondicion debe mostrar el estado final del caso de uso por lo que las ultimas 2 postcondiciones estan de mas]
Corrección: [Se eliminan las ultimas 2 postcondiciones]


