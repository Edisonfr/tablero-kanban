# PLAN_ATOMICO.md — Hoja de Ruta de Implementación

> **Estado:** 🟡 Pendiente de Ejecución  
> **Metodología:** SDD + Arquitectura Hexagonal  
> **Objetivo:** Implementar el límite WIP (INV-01) en el corazón del sistema.

---

## FASE 1: Dominio Puro (Core) 🧠
*En esta fase no se usan bases de datos ni frameworks. Solo Python puro.*

- [ ] **Paso 1.1:** Definir la Entidad `Tarea` en `src/dominio/entidades.py` con atributos: `id`, `titulo`, `estado`.
- [ ] **Paso 1.2:** Crear la lógica de validación de la **INV-01** (Límite WIP) en un servicio de dominio o método de entidad.
- [ ] **Paso 1.3:** Implementar excepciones personalizadas de negocio (ej. `WipLimitExceededError`) en `src/dominio/excepciones.py`.

## FASE 2: Pruebas Unitarias (Garantía) 🧪
*Validar que las reglas de negocio funcionan antes de seguir.*

- [ ] **Paso 2.1:** Crear tests en `pruebas/test_dominio.py` que intenten mover 4 tareas a `DOING`.
- [ ] **Paso 2.2:** Verificar que el test falle (Rojo) y luego pase al implementar la lógica (Verde).

## FASE 3: Aplicación (Casos de Uso) ⚙️
*Orquestación de las acciones.*

- [ ] **Paso 3.1:** Definir el Puerto (Interface) del repositorio en `src/aplicacion/puertos.py`.
- [ ] **Paso 3.2:** Crear el Caso de Uso `MoverTarea` en `src/aplicacion/casos_de_uso.py`.

## FASE 4: Infraestructura (Detalles Técnicos) 🔌
*Conexión con el mundo real.*

- [ ] **Paso 4.1:** Implementar el Adaptador de Persistencia (PostgreSQL/SQLAlchemy) en `src/infraestructura/persistencia/`.
- [ ] **Paso 4.2:** Crear los controladores de FastAPI en `src/infraestructura/http/api.py`.
- [ ] **Paso 4.3:** Configurar el archivo `.env` y la conexión a la base de datos.

## FASE 5: Integración y Cierre 🏁
- [ ] **Paso 5.1:** Pruebas de integración con la API corriendo.
- [ ] **Paso 5.2:** Documentación final en el README sobre cómo ejecutar el proyecto.

---
**Nota de trazabilidad:** Cada paso completado debe registrarse en la `BITACORA.md`.
