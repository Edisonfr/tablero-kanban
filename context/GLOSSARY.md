# GLOSSARY.md — Glosario del Dominio Kanban

> **Archivo de paquete de contexto (5 de 5).** Este documento establece la definición oficial de los términos utilizados en el sistema. Su objetivo es eliminar la ambigüedad en el código y en la comunicación del equipo.

---

## 1. Términos de Negocio (Kanban)

| Término | Definición |
| :--- | :--- |
| **Tablero (Board)** | Representación visual del flujo de trabajo, compuesto por columnas que representan estados. |
| **Tarea (Task)** | La unidad atómica de trabajo. Representa una actividad que debe ser completada. |
| **Estado (Status)** | La etapa actual de una tarea en el flujo (TODO, DOING, DONE). |
| **Límite WIP (Work In Progress)** | Restricción técnica que limita la cantidad de tareas permitidas en una columna específica (en este proyecto, limitado a 3 en DOING). |
| **Flujo de Trabajo (Workflow)** | El movimiento secuencial de las tareas desde la creación hasta su finalización. |

## 2. Términos Técnicos (Arquitectura)

| Término | Definición |
| :--- | :--- |
| **Invariante (Invariant)** | Una regla de negocio que debe cumplirse siempre, sin importar qué acción se realice sobre el sistema. |
| **Dominio (Domain)** | El corazón del software donde reside la lógica de negocio pura, aislada de bases de datos o frameworks. |
| **Capa de Aplicación** | Capa que orquestra los casos de uso pero no contiene lógica de decisión de negocio. |
| **Puerto (Port)** | Definición de una interfaz que permite al dominio comunicarse con el mundo exterior (ej. un repositorio). |
| **Adaptador (Adapter)** | Implementación técnica de un puerto (ej. un repositorio de PostgreSQL o un controlador de FastAPI). |
| **Entidad (Entity)** | Un objeto de dominio que tiene una identidad única (ID) que persiste a través del tiempo. |

## 3. Siglas y Acrónimos

- **SDD**: Spec-Driven Development (Desarrollo Guiado por Especificaciones).
- **WIP**: Work In Progress (Trabajo en Progreso).
- **UUID**: Universally Unique Identifier (Identificador Único Universal).
- **DTO**: Data Transfer Object (Objeto de Transferencia de Datos entre capas).
- **API**: Application Programming Interface (Interfaz de Programación de Aplicaciones).

---
*Cualquier término nuevo que aparezca durante el desarrollo en las especificaciones debe ser agregado aquí antes de la fase de codificación.*
