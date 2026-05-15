# CONTEXT.md — Tablero Kanban Personal con Límite WIP

## 1. Propósito
Proveer una herramienta de gestión visual de tareas basada en la metodología Kanban. El sistema debe obligar al usuario a mantener un flujo de trabajo saludable mediante la restricción técnica de tareas en ejecución.

## 2. Problema a Resolver
El "multitasking" reduce la productividad. El sistema debe impedir que el usuario tenga más de 3 tareas en la columna "DOING", forzándolo a terminar tareas antes de empezar nuevas (Stop Starting, Start Finishing).

## 3. Stakeholders
- **Usuario**: Santiago Carvajal y equipo (Edison, Damian, Estefania).
- **Evaluador**: Ing. Germán González Rozo.

## 4. Alcance (Laboratorio)
- Gestión de un tablero único con tres estados fijos: `TODO`, `DOING`, `DONE`.
- Persistencia en PostgreSQL.
- API REST con FastAPI.
