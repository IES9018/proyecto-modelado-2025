```mermaid
sequenceDiagram
    participant Visitante
    Visitante ->> ArticuloView: Escribe comentario y "Enviar"
    ArticuloView ->> ComentarioController: crearComentario(datos)
    ComentarioController ->> Comentario: crear()
    ComentarioController ->> Comentario: guardar()
    ComentarioController -->> ArticuloView: Informe de éxito
```
