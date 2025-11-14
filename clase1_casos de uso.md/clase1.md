
# **Materia:** Modelado de Software  
**Profesor:** Paulo Álvarez  
**Proyecto:** Sistema de Gestión de Contenidos — *Institución Digital*  

---

## 🎯 Objetivo de la Clase

El objetivo de esta primera clase es conocer los fundamentos de **UML (Lenguaje Unificado de Modelado)** y aplicar sus elementos básicos para representar los **requisitos funcionales** del sistema *Institución Digital*.  
Aprenderás a identificar actores, definir casos de uso y registrar los primeros diagramas que describen el comportamiento general del sistema.

---

## 🧠 ¿Qué es UML?

UML (Unified Modeling Language) es un lenguaje visual que nos permite representar cómo funciona un sistema de software.  
Con él podemos **mostrar, analizar y diseñar** distintas partes de un proyecto sin necesidad de escribir código todavía.  

---

## 🏫 Contexto del Proyecto: *Institución Digital*

El proyecto tiene como propósito crear una **plataforma de gestión de contenidos educativos**, donde docentes y estudiantes puedan compartir materiales, tareas y comentarios.  
El sistema debe facilitar la comunicación y el acceso a la información dentro de una institución educativa.

---

## 📋 Requisitos del Sistema

- Los docentes pueden crear, editar y publicar materiales educativos.  
- Los estudiantes pueden visualizar los contenidos y dejar comentarios.  
- El administrador gestiona usuarios, permisos y publicaciones.  
- El sistema debe permitir el acceso desde navegadores web.  

---

## 👥 Actores del Sistema

| Actor | Descripción |
|-------|--------------|
| **Administrador** | Supervisa todo el sistema, crea usuarios y controla el contenido. |
| **Docente** | Carga materiales educativos, los edita y publica. |
| **Estudiante** | Visualiza los contenidos, comenta y realiza tareas. |

---

## ⚙️ Casos de Uso Principales

1. Administrador:  
   - Crear, editar y eliminar usuarios.  
   - Revisar publicaciones reportadas.  

2. Docente:  
   - Crear material educativo.  
   - Publicar contenido.  
   - Editar o eliminar publicaciones propias.  

3. Estudiante:  
   - Ver publicaciones.  
   - Comentar en los materiales.  

---

## 🧩 Diagrama de Casos de Uso (Mermaid)

> 📌 Copiá este bloque y pegalo en [https://mermaid.live](https://mermaid.live) para ver el diagrama visual.

```mermaid
graph LR
  Admin[Administrador] --> (Gestionar usuarios)
  Admin --> (Revisar publicaciones)
  Docente[Docente] --> (Crear material educativo)
  Docente --> (Publicar contenido)
  Docente --> (Editar o eliminar publicación)
  Estudiante[Estudiante] --> (Ver publicaciones)
  Estudiante --> (Comentar materiales)
