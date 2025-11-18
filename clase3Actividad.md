# 📄 Clase 3 – Refinando la Arquitectura

## ✔ 1. Diagrama de Clases Refactorizado

Aplicando Alta Cohesión y Bajo Acoplamiento, el diseño queda de la siguiente forma:

La clase Usuario ya no gestiona autenticación.

La lógica de login/logout se mueve a ServicioAutenticacion.

Se reduce el acoplamiento entre controladores y modelos.

classDiagram
    class Usuario {
        -id
        -nombre
        -email
    }

    class Articulo {
        -id
        -titulo
        -contenido
        +publicar()
    }

    class Comentario {
        -id
        -texto
        +agregar()
    }

    class ServicioAutenticacion {
        +login(email, password)
        +logout()
    }

    Usuario --> ServicioAutenticacion : usa
    Articulo "1" --> "0..*" Comentario : contiene

## ✔ 2. Arquitectura MVC – Diagrama Conceptual
graph TD
    subgraph Modelo
        M1[Usuario]
        M2[Articulo]
        M3[Comentario]
        M4[ServicioAutenticacion]
    end

    subgraph Vista
        V1[FormularioArticulo]
        V2[PaginaArticulo]
        V3[ListaComentarios]
    end

    subgraph Controlador
        C1[ArticuloController]
        C2[ComentarioController]
        C3[AuthController]
    end

    V1 --> C1
    V2 --> C1
    V3 --> C2

    C1 --> M2
    C1 --> M1
    C2 --> M3
    C3 --> M4

    M2 --> V2
    M3 --> V3
    M1 --> V1

## ✔ 3. Patrón de Diseño Aplicado: Facade

Patrón: Facade

Problema detectado:
Los controladores estaban creando objetos y gestionando lógica interna de varias clases del modelo, aumentando el acoplamiento.

Solución:
Se introduce una clase que actúa como “fachada” del sistema, por ejemplo SistemaBlog, que expone métodos simples como:

sistema.publicarArticulo(datos)
sistema.agregarComentario(datos)


Esto oculta la complejidad interna, reduce dependencias y hace que los controladores interactúen con una única interfaz estable.

Beneficio:

Menor acoplamiento

Código más mantenible

Se puede cambiar la implementación interna sin afectar al resto del sistema