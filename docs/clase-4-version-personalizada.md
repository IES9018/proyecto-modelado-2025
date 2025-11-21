# Clase 4 – Versión Personalizada del Proyecto

---

## 🎯 Objetivo de esta etapa
Transformar el proyecto base “Institución Digital” en una **versión personalizada**, definiendo el contexto real de uso, las funcionalidades principales y la estructura para su evolución.

---

## 🏫 Contexto institucional elegido
La versión personalizada está pensada para un **Instituto Superior / Institución Terciaria**, donde los estudiantes y docentes necesitan un sistema centralizado para administrar información académica, recursos, calendarios y comunicaciones.

---

## 🔎 Alcance funcional (Roadmap evolutivo)

| Versión | Funcionalidades principales |
|---------|------------------------------|
| v1.0.0  | Documentación, estructura inicial, lectura de requerimientos, diagramas, organización del repositorio |
| v1.1.0  | Gestión de usuarios y sistema de foros (roles: estudiante, docente y administrador) |
| v1.2.0  | Biblioteca digital (descargas, materiales) y calendario académico interactivo |
| v1.3.0  | Chatbot institucional y sistema de notificaciones automáticas |

---

## 🏗️ Arquitectura propuesta
Se adopta la arquitectura **MVC (Modelo–Vista–Controlador)** porque:

✔ Permite separar responsabilidades  
✔ Favorece la escalabilidad del código  
✔ Es compatible con frameworks modernos  
✔ Facilita futuras integraciones (API, base de datos, frontend)

📂 Organización aplicada al proyecto:

```bash
src/
├── models/ # Datos, entidades, lógica de negocio
├── controllers/ # Procesos, reglas, validación
└── views/ # Interfaces y visualización
```

---

## 📘 Diagramas involucrados

| Tipo de diagrama | Propósito |
|------------------|-----------|
| Casos de uso | Representan los actores y requerimientos funcionales |
| Diagrama de clases | Define estructura y entidades principales |
| Diagrama arquitectónico MVC | Representa la organización general del sistema |

> Los archivos están ubicados en `/diagrams`.

---

## 🗂️ Organización del repositorio

```bash
proyecto-modelado-alex/
├── docs/ # Documentación general
│ ├── clase-1-introduccion.md
│ ├── clase-2-uml.md
│ ├── clase-3-arquitecturas.md
│ └── clase-4-version-personalizada.md
├── diagrams/ # Diagramas UML y arquitectónicos
│ ├── mvc.drawio
│ ├── arquitectura-general.pdf
│ └── casos-de-uso.png
├── src/ # Código fuente (futuro desarrollo)
│ ├── models/
│ ├── controllers/
│ └── views/
├── README.md
└── .gitignore
```

## 💡 Conclusión
Esta etapa marca el inicio de mi **versión evolutiva y personalizada**, donde se organiza el proyecto, se define el contexto institucional real y se prepara la base estructural para su desarrollo futuro.

---

📌 Próximo paso: completar archivos de Clase 1, 2 y 3 dentro de `/docs` y preparar el Pull Request final.
