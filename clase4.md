# Clase 4 - Implementación de lo aprendido aplicando features nuevas a la configuración base

## 📌 1. Diagrama de Caso de Uso – Camila-blog
flowchart TD

    subgraph Usuarios
        A[Usuario Visitante]
        B[Autor]
        C[Administrador]
    end

    subgraph Casos_de_Uso
        CU1((Leer artículos))
        CU2((Comentar artículos))
        CU3((Dar "Me gusta"))
        CU4((Ver artículos por categoría))
        CU5((Ver artículos por etiquetas))

        CU6((Crear borrador))
        CU7((Publicar borrador))
        CU8((Editar artículo))
        CU9((Eliminar artículo))

        CU10((Gestionar categorías))
        CU11((Gestionar etiquetas))
        CU12((Ver estadísticas del panel))

        CU13((Gestionar usuarios))
    end

    %% Relaciones

    %% Usuario Visitante
    A --> CU1
    A --> CU2
    A --> CU3
    A --> CU4
    A --> CU5

    %% Autor
    B --> CU6
    B --> CU7
    B --> CU8
    B --> CU9
    B --> CU10
    B --> CU11
    B --> CU12

    %% Administrador
    C --> CU13
    C --> CU10
    C --> CU11
    C --> CU12

## 📌 2. Diagrama de Clases – Camila-blog

Incluye:
✔ Artículos
✔ Categorías
✔ Etiquetas
✔ Likes
✔ Borradores (estado del artículo)
✔ Estadísticas

classDiagram

    class Usuario {
        +id: int
        +nombre: string
        +email: string
        +rol: string
        +login()
        +logout()
    }

    class Articulo {
        +id: int
        +titulo: string
        +contenido: string
        +fecha_creacion: date
        +fecha_publicacion: date
        +estado: string  <<draft/published>>
        +publicar()
        +editar()
        +eliminar()
    }

    class Categoria {
        +id: int
        +nombre: string
        +slug: string
        +descripcion: string
    }

    class Etiqueta {
        +id: int
        +nombre: string
        +slug: string
    }

    class Comentario {
        +id: int
        +contenido: string
        +fecha: date
        +eliminar()
    }

    class Like {
        +id: int
        +fecha: date
    }

    class Estadistica {
        +id: int
        +visitas_totales: int
        +likes_totales: int
        +articulos_publicados: int
        +generarReporte()
    }


    %% Relaciones
    Usuario "1" --> "*" Articulo : crea
    Usuario "1" --> "*" Comentario : escribe
    Usuario "1" --> "*" Like : da

    Articulo "1" --> "*" Comentario : tiene
    Articulo "*" --> "*" Categoria : pertenece
    Articulo "*" --> "*" Etiqueta : etiquetado
    Articulo "1" --> "*" Like : recibe
    Articulo "1" --> "1" Estadistica : genera

## 📌 3. Diagrama de Secuencia – Crear Categoría (Feature Nueva)
sequenceDiagram
    actor Autor
    participant UI as Interfaz Web
    participant C as ControladorCategoria
    participant M as ModeloCategoria
    participant DB as Base de Datos

    Autor ->> UI: Ingresa nombre/slug/descripción
    UI ->> C: Solicita crear nueva categoría
    C ->> M: Validar datos
    M ->> DB: INSERT categoría
    DB -->> M: OK
    M -->> C: Categoría creada
    C -->> UI: Mostrar mensaje de éxito
    UI -->> Autor: Categoría creada correctamente

## 📌 4. Diagrama de Secuencia – Publicar Borrador (Feature Nueva)
sequenceDiagram
    actor Autor
    participant UI as Interfaz Web
    participant C as ControladorArticulo
    participant M as ModeloArticulo
    participant DB as Base de Datos
    participant EST as ServicioEstadisticas

    Autor ->> UI: Seleccionar "Publicar artículo"
    UI ->> C: Solicitud para publicar
    C ->> M: Cambiar estado a "publicado"
    M ->> DB: UPDATE articulo SET estado="publicado"
    DB -->> M: OK

    M ->> EST: Notificar publicación
    EST ->> DB: UPDATE estadísticas
    DB -->> EST: OK

    EST -->> M: Actualización terminada
    M -->> C: Publicación exitosa
    C -->> UI: Confirmación
    UI -->> Autor: Artículo publicado

## 📌 5. Features Modeladas 

Tus 6 funcionalidades nuevas modeladas son:

✔ Likes (Me gusta)

✔ Categorías mejoradas (con slug + descripción)

✔ Etiquetas (tags)

✔ Borradores / publicación diferida

✔ Panel de estadísticas

✔ Gestión de usuarios (solo admins)