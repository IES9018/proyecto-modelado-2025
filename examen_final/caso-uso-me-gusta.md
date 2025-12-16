ID y Nombre:

CU-XX: Dar/Quitar Me Gusta en Artículo

Actores:

Principal: Lector (Usuario autenticado)

Secundario: Sistema de Estadísticas (actualizar contador)

Precondiciones:

Usuario debe estar autenticado

Artículo debe existir en el sistema

Usuario puede ver el artículo

Flujo Principal:

Usuario navega a un artículo

Usuario visualiza botón 'Me gusta' (con ícono de corazón)

Usuario hace clic en 'Me gusta'

Sistema verifica si el usuario ya dio 'me gusta'

Sistema registra el 'me gusta' (si no existía) O lo elimina (si existía)

Sistema incrementa/decrementa el contador

Sistema actualiza la UI (botón resaltado + contador actualizado)

Sistema muestra confirmación visual

Flujos Alternativos:

FA1 — Usuario ya dio 'Me gusta':

En el paso 4, si ya existe registro

Sistema elimina el 'me gusta' (toggle)

Sistema decrementa contador

FA2 — Error de base de datos:

Si la operación de persistencia falla

Sistema muestra mensaje: 'No se pudo procesar tu acción'

UI revierte al estado anterior

FA3 — Usuario no autenticado (opcional si tenés validación de auth):

Si usuario intenta dar 'me gusta' sin autenticación

Sistema redirige a login

Postcondiciones:

El registro de 'me gusta' se guardó en la BD (o se eliminó, según corresponda)

El contador de 'me gusta' del artículo está actualizado

La UI refleja el estado actual (botón liked/unliked + contador correcto)

El historial de 'me gusta' por usuario está registrado