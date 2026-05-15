# UC-02: Mover Tarea a Estado "DOING"

## Descripción
Como usuario, quiero mover una tarea a la columna "Haciendo" para empezar a trabajar en ella.

## Criterios de Aceptación (AC)
- **AC-01**: Si el número de tareas en `DOING` es menor a 3, el sistema debe permitir el cambio.
- **AC-02**: Si el número de tareas en `DOING` es igual a 3, el sistema debe lanzar una excepción de negocio `WipLimitExceededError`.
- **AC-03**: El cambio debe persistirse en la base de datos solo si la regla INV-01 se cumple.
