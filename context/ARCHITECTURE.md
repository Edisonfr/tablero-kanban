# ARCHITECTURE.md — Diseño de Puertos y Adaptadores

## 1. Estilo Arquitectónico
Se utiliza **Arquitectura Hexagonal**. La lógica de negocio está aislada de los frameworks.

## 2. Capas
- **Capa de Dominio (`src/dominio`)**: Contiene las entidades y las Invariantes (INV). No depende de FastAPI ni de la base de datos.
- **Capa de Aplicación (`src/aplicacion`)**: Contiene los Casos de Uso y define los Puertos (Interfaces).
- **Capa de Infraestructura (`src/infraestructura`)**:
  - `http/`: Adaptadores para FastAPI.
  - `persistencia/`: Adaptadores para PostgreSQL (SQLAlchemy).

## 3. Regla de Oro
Las dependencias apuntan siempre hacia el centro (Dominio). Nada de la infraestructura debe filtrarse al dominio.
