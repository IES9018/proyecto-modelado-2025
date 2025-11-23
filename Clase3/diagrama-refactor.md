## Refactorización y Facade (Resumen)

Se propone una fachada (`SistemaBlog`) para reducir acoplamientos entre controladores y facilitar cambios futuros.

```mermaid
classDiagram
    class SistemaBlog {
        +publicarArticulo(datos)
        +dejarComentario(datos)
    }

    class ArticuloController
    class ComentarioController

    SistemaBlog ..> ArticuloController : usa
    SistemaBlog ..> ComentarioController : usa
```
![diagrama](mermaid-diagram-2025-11-11-165629.png)
