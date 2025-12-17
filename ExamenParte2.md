## Caso de Uso – Nueva Funcionalidad
## ID: CU-09: Dar “Me Gusta” a Foto de Artículo
## Actor Principal

Usuario Registrado

## Actores Secundarios

Sistema de Almacenamiento

## Descripción

El usuario registrado puede dar “Me gusta” a una foto asociada a un artículo, permitiendo expresar su valoración. El sistema registra la acción y actualiza el contador de “Me gusta” visible en la foto.

## Precondiciones

El usuario debe estar autenticado en el sistema

El artículo debe estar publicado

La foto debe existir y estar asociada a un artículo

El usuario no debe haber dado “Me gusta” previamente a esa foto

## Flujo Principal

El Usuario Registrado accede a un artículo publicado

El sistema muestra las fotos del artículo con su contador de “Me gusta”

El Usuario Registrado hace clic en el botón “Me gusta” de una foto

El sistema verifica que el usuario no haya dado “Me gusta” previamente a esa foto

El sistema registra el “Me gusta” asociado al usuario y a la foto

El sistema incrementa el contador de “Me gusta” de la foto

El sistema actualiza el contador en la interfaz

El sistema cambia el botón a estado “Te gusta”

Fin del caso de uso

## Flujos Alternativos

FA1: Usuario ya dio “Me gusta”

En el paso 4, si el usuario ya dio “Me gusta” a la foto:

4a. El sistema muestra el mensaje “Ya diste Me gusta a esta foto”

4b. El sistema no modifica el contador

4c. Fin del caso de uso

FA2: Quitar “Me gusta”

En el paso 3, si el botón se encuentra en estado “Te gusta”:

3a. El Usuario Registrado hace clic para quitar el “Me gusta”

3b. El sistema elimina el registro de “Me gusta”

3c. El sistema decrementa el contador de la foto

3d. El sistema actualiza la interfaz

3e. Fin del caso de uso

FA3: Usuario no autenticado

En el paso 3, si el usuario no está autenticado:

3a. El sistema muestra el mensaje “Debes iniciar sesión para dar Me gusta”

3b. El sistema redirige a la pantalla de inicio de sesión

3c. Fin del caso de uso

## Postcondiciones

El “Me gusta” queda registrado en la base de datos

El contador de “Me gusta” de la foto se actualiza correctamente

El usuario no puede volver a dar “Me gusta” a la misma foto

El estado del botón refleja la acción realizada

## Excepciones

EX1: Si la foto no existe o fue eliminada durante la operación, el sistema muestra un mensaje de error y no registra el “Me gusta”

EX2: Si ocurre un error de conexión con la base de datos, el sistema muestra un mensaje de error y no actualiza el contador

EX3: Si el artículo asociado a la foto deja de estar publicado, el sistema bloquea la acción y muestra un mensaje informativo
## DIAGRAMA DE CLASES
classDiagram
class Usuario {
  -id: int
  -nombre: String
  +darMeGusta(foto: Foto)
  +quitarMeGusta(foto: Foto)
}

class Articulo {
  -id: int
  -titulo: String
  -publicado: boolean
}

class Foto {
  -id: int
  -url: String
  -contadorMeGusta: int
  +incrementarMeGusta()
  +decrementarMeGusta()
}

class MeGustaFoto {
  -id: int
  -fecha: Date
}

class FotoController {
  +darMeGusta()
  +quitarMeGusta()
}

Usuario "1" --> "0..*" MeGustaFoto
Foto "1" --> "0..*" MeGustaFoto
Articulo "1" --> "1..*" Foto
FotoController --> Foto
FotoController --> MeGustaFoto

## DIAGRAMA DE SECUENCIA
sequenceDiagram
  actor Usuario
  participant Vista
  participant Controller as FotoController
  participant Modelo as Foto
  participant BD

  Usuario->>Vista: click "Me gusta"
  Vista->>Controller: darMeGusta(fotoId)
  Controller->>BD: verificarMeGusta(usuario, foto)
  BD-->>Controller: no existe
  Controller->>Modelo: incrementarMeGusta()
  Controller->>BD: guardarMeGusta(usuario, foto)
  Controller-->>Vista: actualizarContador()
  Vista-->>Usuario: muestra "Te gusta"
## Diagrama de ACTIVIDAD
flowchart TD
A[Inicio] --> B[Usuario visualiza foto]
B --> C[Hace clic en Me gusta]
C --> D{¿Usuario autenticado?}
D -- No --> E[Mostrar mensaje de login]
E --> Z[Fin]

D -- Sí --> F{¿Ya dio Me Gusta?}
F -- Sí --> G[Mostrar mensaje informativo]
G --> Z[Fin]

F -- No --> H[Registrar Me Gusta]
H --> I[Incrementar contador]
I --> J[Actualizar interfaz]
J --> Z[Fin]
