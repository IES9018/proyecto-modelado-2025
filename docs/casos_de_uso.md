# Documentación de Casos de Uso

## Caso de Uso 1: Gestionar Artículo

**Actores:** Autor, Administrador

**Objetivo:** Crear y editar artículos, y gestionar las etiquetas
asociadas.

**Precondiciones:** - El actor debe haber iniciado sesión. - Debe tener
permisos de Autor o Administrador.

**Postcondiciones:** - El artículo queda registrado o actualizado. - Se
actualizan las etiquetas asociadas.

**Flujo principal:** 1. El actor selecciona "Gestionar Artículo". 2. El
sistema muestra opciones: Crear, Editar, Agregar etiqueta, Quitar
etiqueta. 3. El actor elige una acción. 4. El sistema solicita los datos
necesarios. 5. El actor completa la información. 6. El sistema valida.
7. El sistema guarda los cambios. 8. Se muestra confirmación.

**Flujos alternativos:** - A1: Datos incompletos → error. - A2: El
artículo no existe → aviso.

------------------------------------------------------------------------

## Caso de Uso 2: Gestionar Etiquetas

**Actor:** Administrador

**Objetivo:** Crear, editar y eliminar etiquetas.

**Precondiciones:** - Sesión iniciada. - Permisos de Administrador.

**Postcondiciones:** - La etiqueta queda creada, modificada o eliminada.

**Flujo principal:** 1. El administrador selecciona "Gestionar
Etiquetas". 2. El sistema muestra opciones: Crear, Editar, Eliminar. 3.
Selecciona una acción. 4. El sistema pide datos. 5. El administrador
ingresa la información. 6. El sistema valida. 7. El sistema aplica los
cambios. 8. Confirmación.

**Flujos alternativos:** - A1: Etiqueta duplicada. - A2: Etiqueta
inexistente.

------------------------------------------------------------------------

## Caso de Uso 3: Leer Artículo

**Actor:** Visitante

**Objetivo:** Permitir la visualización de artículos publicados.

**Precondiciones:** - Debe existir al menos un artículo publicado.

**Postcondiciones:** - El visitante visualiza el contenido del artículo.

**Flujo principal:** 1. El visitante accede a la página principal. 2.
Selecciona un artículo. 3. El sistema carga el contenido. 4. El
visitante visualiza título, contenido y etiquetas.

**Flujos alternativos:** - A1: El artículo fue eliminado → aviso.
