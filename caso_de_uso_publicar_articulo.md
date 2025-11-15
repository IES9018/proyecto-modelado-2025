# Caso de Uso: Publicar Artículo

**Actor Principal:** Autor

**Resumen:**  
El Autor crea, edita y publica un nuevo artículo en el blog de la institución.

## Flujo Principal (Camino Feliz)
1. El Autor inicia sesión en el sistema.
2. El sistema presenta al Autor un formulario para crear un nuevo artículo (con campos para título, contenido, etc.).
3. El Autor completa el formulario y presiona "Publicar".
4. El sistema valida los datos y guarda el artículo en la base de datos con estado "Publicado".
5. El sistema muestra un mensaje de confirmación y redirige al Autor a la lista de sus artículos.

## Flujos Alternativos
### 4a - Datos inválidos
Si el título está vacío o falta contenido, el sistema muestra un mensaje de error y no guarda el artículo.
