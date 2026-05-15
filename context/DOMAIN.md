# DOMAIN.md — Bounded Context: Kanban Task Management

## 1. Lenguaje Ubicuo
- **Tarea (Task)**: Unidad de trabajo con un ID único, un Título y un Estado.
- **Estado (Status)**: La fase actual de la tarea. Valores permitidos: `TODO`, `DOING`, `DONE`.
- **Límite WIP (Work In Progress)**: Constante de dominio fijada en **3**.

## 2. Invariantes de Dominio (Reglas Inviolables)
- **INV-01 (Límite WIP)**: La columna `DOING` no puede contener más de 3 tareas simultáneamente. Cualquier intento de mover una tarea a `DOING` cuando ya hay 3 debe ser rechazado por el modelo de dominio.
- **INV-02 (Estado Inicial)**: Toda tarea nueva debe crearse obligatoriamente en estado `TODO`.
- **INV-03 (Integridad de Estado)**: Solo se permiten los estados `TODO`, `DOING` y `DONE`.
- **INV-04 (Título Requerido)**: Una tarea no puede existir sin un título (mínimo 3 caracteres).
- **INV-05 (Identidad Inmutable)**: El ID de la tarea (UUID) no puede cambiar una vez creada.
