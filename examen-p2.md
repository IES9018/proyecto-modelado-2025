## PARTE 2
## CASO DE USO COMPLETO, NUEVA FUNCIONALIDAD "GUARDAR ARTÍCULO COMO BORRADOR"

## CU-10 – Guardar Artículo como Borrador

## Actores

Actor Principal: Autor

## Descripción

El Autor guarda un artículo como borrador para poder continuar editándolo más adelante sin publicarlo.

## Precondiciones

El Autor está autenticado en el sistema.

El Autor tiene permisos para crear o editar artículos.

## Flujo Principal

1 El Autor accede al editor de artículos.

2 El Autor ingresa el título y contenido del artículo.

3 El Autor selecciona la opción “Guardar como borrador”.

4 El sistema valida los datos ingresados.

5 El sistema guarda el artículo con estado Borrador.

6 El sistema muestra un mensaje de confirmación.

7 Fin del caso de uso.

## Flujos Alternativos

3a. Cancelación:
Si el Autor cancela la operación, el sistema no guarda cambios y vuelve al editor.

## Postcondiciones

El artículo queda almacenado en el sistema con estado Borrador.

El artículo no es visible públicamente.

## Código Mermaid del Diagrama
classDiagram
    class Autor {
        id
        nombre
    }
    class Articulo {
        id
        titulo
        contenido
        estado
        guardarComoBorrador()
    }
    class ArticuloController {
        guardarBorrador(datosArticulo)
    }
    class ArticuloService {
        validarDatos()
        guardarBorrador(articulo)
    }
    Autor "1" --> "0..*" Articulo
    ArticuloController --> ArticuloService
    ArticuloService --> Articulo

## Diagrama de Secuencia Mermaid
sequenceDiagram
    actor Autor
    participant C as ArticuloController
    participant S as ArticuloService
    participant A as Articulo

    Autor->>C: guardarBorrador(datosArticulo)
    C->>S: guardarBorrador(datosArticulo)
    S->>S: validarDatos()
    S->>A: guardarComoBorrador()
    S-->>C: confirmación
    C-->>Autor: mensaje "Borrador guardado"