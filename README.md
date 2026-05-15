# Tablero Kanban Personal con Límite WIP

Este proyecto implementa un sistema de gestión de tareas basado en la metodología Kanban, desarrollado bajo los principios de **Ingeniería de Contexto** y **Spec-Driven Development (SDD)**. El enfoque principal es la protección de las reglas de negocio en el núcleo del sistema, utilizando una arquitectura desacoplada y robusta.

## 🎯 Propósito del Proyecto
El sistema permite gestionar el flujo de trabajo personal asegurando el cumplimiento de la metodología Kanban, específicamente mediante el control del **Work In Progress (WIP)** en la columna de ejecución, evitando la sobrecarga de tareas y garantizando un flujo constante.

## 🛠️ Stack Técnico
- **Lenguaje:** Python 3.11+
- **Framework API:** FastAPI
- **Base de Datos:** PostgreSQL
- **Arquitectura:** Hexagonal (Ports & Adapters) + DDD Táctico
- **Gestión de Dependencias:** pip / venv

## 🏗️ Estructura del Repositorio
Siguiendo la metodología SDD, el repositorio está organizado de la siguiente manera:

```text
├── context/               # Paquete de Contexto (Invariantes y Reglas)
│   ├── CONTEXT.md         # Propósito y stakeholders
│   ├── DOMAIN.md          # Lenguaje ubicuo e Invariantes (INV)
│   ├── ARCHITECTURE.md    # Definición de capas y puertos
│   └── TECH_CONSTRAINTS.md # Restricciones de stack y herramientas
├── specs/                 # Especificaciones (Casos de Uso)
│   └── SPECS.md           # Detalle de UC-01, UC-02 y UC-03
├── src/                   # Código Fuente (Hexagonal)
│   ├── dominio/           # Lógica pura de negocio (Entidades, Excepciones)
│   ├── aplicacion/        # Servicios de aplicación y Puertos
│   └── infraestructura/   # Adaptadores (API FastAPI, Persistencia SQL)
├── tests/                 # Pruebas unitarias y de integración
├── BITACORA.md            # Registro cronológico de decisiones
└── README.md              # Documentación principal


Reglas de Negocio Críticas (Invariantes)
INV-01 (Límite WIP): La columna DOING tiene un límite estricto de 3 tareas. El sistema rechazará cualquier intento de mover una cuarta tarea a este estado desde el modelo de dominio.

INV-02 (Flujo Inicial): Toda tarea nueva debe crearse obligatoriamente en el estado TODO.

INV-03 (Identidad): Cada tarea posee un identificador único e inmutable (UUID).



Metodología de Desarrollo (SDD)
Este proyecto no admite la generación de código sin un plan previo. El flujo de trabajo es:

Definir el Contexto.

Crear la Especificación del Caso de Uso.

Generar un Plan Atómico de implementación.

Ejecutar el código y registrar en la Bitácora.

Materia: Ingeniería de Software II
Profesor: Ing. Germán González Rozo
