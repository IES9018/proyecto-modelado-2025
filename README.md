# Examen Final – Modelado de Software

Este repositorio contiene la resolución del **Examen Final de la materia Modelado de Software** correspondiente a la carrera **Tecnicatura en Desarrollo de Software**.

## Estructura del Examen

El examen se resolvió siguiendo las consignas oficiales y se divide en dos partes principales, más la preparación para la defensa oral:

### Parte 1 – Análisis Crítico de Caso de Uso

* Identificación de errores conceptuales en un caso de uso provisto.
* Justificación de por qué cada punto es incorrecto.
* Propuesta de correcciones siguiendo buenas prácticas de modelado.
* Archivo de entrega: `examen-p1.md`.

### Parte 2 – Diseño de Nueva Funcionalidad

* Implementación del requisito **“Guardar artículo como borrador antes de publicar”**.
* Desarrollo de:

  * Caso de uso completo.
  * Diagrama de clases (enfoque MVC).
  * Diagrama de secuencia del flujo principal.
* Archivo de entrega: `examen-p2.md`.

### Parte 3 – Defensa Oral

Preparación teórica y conceptual para la defensa individual, incluyendo:

* Explicación de la arquitectura MVC aplicada.
* Justificación de decisiones de diseño.
* Identificación de principios SOLID y patrones utilizados.
* Defensa del caso de uso y diagramas realizados.

## Arquitectura

El proyecto está organizado bajo el patrón **MVC (Model–View–Controller)**, separando:

* **Model**: entidades del dominio y lógica de negocio.
* **Controller**: coordinación de acciones del usuario.
* **Service**: validaciones y reglas de negocio.
* **View**: interacción con el usuario.

## Entrega

La resolución se entrega mediante:

* Rama: `feature/examen`
* Pull Request contra `main`, con commits trazables para cada parte del examen.

