**Caso de Uso:** Leer Artículo

**Actor Principal:** Visitante

**Resumen:** El visitante puede leer, calificar, colocar opinion y colocar como favorito el artículo leído.

**Flujo Principal (el "camino feliz")**
1. El visitante inicia sesión en el sistema.
2. El sistema le presenta al Visitante una lista de artículos ordenada por los más recientes. Además, un botón de filtros en el que seleccionar si los filtra por: Fecha, Tipo de artículo y ámbito.
3. El Visitante selecciona el artículo a leer.
4. El sistema revisa el artículo en la base de datos, si lo encuentra sigue el flujo.
5. El sistema muestra un mensaje de confirmación y redirige al Visitante al artículo.
6. El visitante hace click en favoritos.
7. El sistema muestra un mensaje de confirmación.
8. El Visitante presiona el botón "Opinar"
9. El sistema verifica si el Visitante inició sesión.
10. El sistema le muestra al visitante el menú para colocar su opinión y una cantidad de estrellas. 
11. El usuario una vez finalizada la opinión presiona el botón "Enviar".
12. El sistema analiza la opinión en busca de contenido prohibido. En caso de no tenerlo prosigue.
13. El sistema muestra un mensaje de confirmación y sube la opinión en la base de datos, la muestra en el apartado de opiniones del artículo.

**Flujos Alternativos (¿qué podría salir mal?)**
*   **4a. Artículo no encontrado:** Si el artículo no se encuentra en la base de datos el sistema muestra un mensaje de error.
*   **9a. Visitante no inició sesión:** Si el sistema detecta que el Visitante no inició sesión le muestra un mensaje solicitando que lo haga, en caso contrario no le permitirá opinar.
*   **12a. Contenido prohibido encontrado:** Si el sistema detecta contenido prohibido le da un mensaje de advertencia al Visitante, si este cambia el contenido el sistema permite subir la opinión.
*   **13a. Error en subir a base de datos:** Si el sistema no logra subir la opinión en la base de datos, el sistema mostrará un mensaje al visitante solicitando que intente nuevamente.