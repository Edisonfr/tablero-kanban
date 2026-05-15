# TECH_CONSTRAINTS.md — Restricciones del Stack

- **Lenguaje**: Python 3.11+
- **Framework API**: FastAPI.
- **Persistencia**: PostgreSQL (usando SQLAlchemy 2.0).
- **Testing**: Pytest.
- **Validación de Datos**: Pydantic (solo en la capa de Infraestructura/API).
- **Regla Técnica**: La validación de la INV-01 debe hacerse en el Dominio, no mediante un `if` en el controlador de FastAPI.
