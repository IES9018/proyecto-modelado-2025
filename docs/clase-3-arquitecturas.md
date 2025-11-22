# Clase 3 – Arquitecturas de Software

---

## 🏛️ ¿Qué es una arquitectura?
Es la **forma en que organizamos un sistema**, cómo se divide en partes y cómo se conectan entre sí.

Es como el plano estructural de una casa, pero de software.

---

## 🧱 Tipos de arquitecturas vistas

| Arquitectura | Características |
|--------------|------------------|
| Monolítica | Todo junto en una única estructura |
| Cliente-Servidor | Separación entre interfaz y servidor |
| Capas n-tier | División en capas (presentación, lógica, datos) |
| MVC | Modelo – Vista – Controlador (la usada en este proyecto) |

---

## 🎯 ¿Por qué usamos MVC?
✔ Separa responsabilidades  
✔ Fácil de mantener y escalar  
✔ Organiza bien la estructura del código  
✔ Compatible con frameworks modernos

---

## 🧩 Diagrama base MVC aplicado al proyecto

```bash
src/
├── models/       # Datos y entidades
├── controllers/  # Lógica, procesos, validaciones
└── views/        # Interfaz (plantillas, HTML, formularios)
