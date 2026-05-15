# Tablero Kanban Personal con Límite WIP

Este repositorio contiene la implementación de un sistema de gestión de tareas basado en la metodología Kanban. El proyecto se desarrolla bajo el marco de **Ingeniería de Contexto** y **Spec-Driven Development (SDD)** para la materia de Ingeniería de Software II.

## 🎯 Propósito del Proyecto
El objetivo es construir una aplicación robusta donde la regla de negocio principal —el **Límite de Work In Progress (WIP)**— esté protegida por el modelo de dominio, asegurando que no se puedan gestionar más de 3 tareas simultáneas en la columna de ejecución.

## 🛠️ Stack Tecnológico
- **Lenguaje:** Python 3.11+
- **Framework API:** FastAPI
- **Base de Datos:** PostgreSQL
- **Arquitectura:** Hexagonal (Puertos y Adaptadores)
- **Metodología:** SDD (Spec-Driven Development)

## 📂 Estructura del Repositorio
Organización siguiendo los estándares de la guía del curso:

```text
├── context/               # Paquete de Contexto (Invariantes y Reglas)
│   ├── CONTEXT.md         # Propósito y actores
│   ├── DOMAIN.md          # Lenguaje ubicuo e Invariantes (INV)
│   ├── ARCHITECTURE.md    # Estructura de capas
│   └── TECH_CONSTRAINTS.md # Restricciones técnicas
├── specs/                 # Especificaciones (Casos de Uso)
│   └── SPECS.md           # Detalle de UC-01, UC-02, UC-03
├── src/                   # Código Fuente
│   ├── dominio/           # Entidades y lógica de negocio pura
│   ├── aplicacion/        # Servicios y Puertos
│   └── infraestructura/   # Adaptadores (FastAPI, PostgreSQL)
├── BITACORA.md            # Registro de decisiones y cambios
└── README.md              # Documentación principal
