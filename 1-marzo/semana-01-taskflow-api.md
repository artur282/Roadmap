# 📋 Semana 01 — TaskFlow API

> **API REST completa para gestión de tareas con FastAPI, PostgreSQL y Docker**

| Campo              | Detalle              |
| ------------------ | -------------------- |
| 📅 Fechas          | 7-8 de marzo 2026    |
| 🏷️ Categoría       | Backend Foundations  |
| ⏱️ Tiempo estimado | 10-12 horas          |
| 📊 Dificultad      | ⭐⭐ Intermedio-bajo |

---

## 🎯 Descripción

TaskFlow API es una API REST profesional para gestión de tareas y proyectos. Es el primer proyecto del portafolio y establece las bases para todos los demás: estructura limpia, tests, Docker, documentación y buenas prácticas desde el día uno.

No es un simple CRUD tutorial — incluye filtros avanzados, paginación, validación robusta, manejo de errores consistente y documentación automática con OpenAPI.

---

## 🏗️ Arquitectura

```
┌─────────────────────────────────────────┐
│              Cliente (HTTP)              │
└──────────────────┬──────────────────────┘
                   │
          ┌────────▼────────┐
          │   FastAPI App   │
          │  (Routers +     │
          │   Middleware)    │
          └────────┬────────┘
                   │
          ┌────────▼────────┐
          │  Service Layer  │
          │ (Business Logic)│
          └────────┬────────┘
                   │
          ┌────────▼────────┐
          │   SQLAlchemy     │
          │   (ORM Layer)    │
          └────────┬────────┘
                   │
          ┌────────▼────────┐
          │   PostgreSQL     │
          │   (Docker)       │
          └─────────────────┘
```

---

## ✨ Features

### Core

- [ ] CRUD completo de tareas (crear, leer, actualizar, eliminar)
- [ ] CRUD de proyectos (agrupar tareas)
- [ ] Relación proyecto → tareas (1:N)
- [ ] Prioridades (baja, media, alta, urgente)
- [ ] Estados (pendiente, en progreso, completada, archivada)

### Avanzado

- [ ] Filtros por estado, prioridad, fecha, proyecto
- [ ] Paginación con cursor o offset
- [ ] Ordenamiento por múltiples campos
- [ ] Búsqueda por texto en título y descripción
- [ ] Validación robusta con Pydantic
- [ ] Manejo de errores consistente (RFC 7807)

### Infraestructura

- [ ] Docker Compose (app + PostgreSQL)
- [ ] Migraciones con Alembic
- [ ] Tests con pytest (cobertura ≥ 80%)
- [ ] Documentación OpenAPI automática
- [ ] Variables de entorno con Pydantic Settings
- [ ] Linting con Ruff

---

## 🛠️ Stack técnico

| Tecnología         | Propósito                  |
| ------------------ | -------------------------- |
| **FastAPI**        | Framework web async        |
| **PostgreSQL 16**  | Base de datos relacional   |
| **SQLAlchemy 2.x** | ORM async                  |
| **Alembic**        | Migraciones de DB          |
| **Pydantic v2**    | Validación y serialización |
| **Docker Compose** | Infraestructura local      |
| **pytest**         | Testing                    |
| **Ruff**           | Linting y formatting       |
| **httpx**          | Cliente HTTP para tests    |

---

## 📁 Estructura del proyecto

```
taskflow-api/
├── app/
│   ├── __init__.py
│   ├── main.py               # Entry point FastAPI
│   ├── config.py              # Settings con Pydantic
│   ├── database.py            # Conexión a DB
│   ├── models/
│   │   ├── task.py            # Modelo SQLAlchemy
│   │   └── project.py
│   ├── schemas/
│   │   ├── task.py            # Schemas Pydantic
│   │   └── project.py
│   ├── routers/
│   │   ├── tasks.py           # Endpoints de tareas
│   │   └── projects.py
│   ├── services/
│   │   ├── task_service.py    # Lógica de negocio
│   │   └── project_service.py
│   └── exceptions/
│       └── handlers.py        # Manejo de errores
├── tests/
│   ├── conftest.py
│   ├── test_tasks.py
│   └── test_projects.py
├── alembic/
│   └── versions/
├── docker-compose.yml
├── Dockerfile
├── Makefile
├── pyproject.toml
├── .env.example
└── README.md
```

---

## 📡 Endpoints de la API

```
GET    /api/v1/tasks              # Listar tareas (con filtros y paginación)
POST   /api/v1/tasks              # Crear tarea
GET    /api/v1/tasks/{id}         # Obtener tarea por ID
PUT    /api/v1/tasks/{id}         # Actualizar tarea
DELETE /api/v1/tasks/{id}         # Eliminar tarea

GET    /api/v1/projects           # Listar proyectos
POST   /api/v1/projects           # Crear proyecto
GET    /api/v1/projects/{id}      # Obtener proyecto con sus tareas
PUT    /api/v1/projects/{id}      # Actualizar proyecto
DELETE /api/v1/projects/{id}      # Eliminar proyecto

GET    /api/v1/health             # Health check
GET    /docs                      # Documentación Swagger
```

---

## 🗓️ Plan del fin de semana

### Sábado

| Hora           | Actividad                                       |
| -------------- | ----------------------------------------------- |
| 🌅 9:00-10:00  | Setup: Docker Compose, estructura, dependencias |
| 🌅 10:00-11:00 | Modelos SQLAlchemy + Alembic migrations         |
| 🌞 11:00-13:00 | Schemas Pydantic + Service layer                |
| 🌞 14:00-17:00 | Routers: CRUD completo de tareas y proyectos    |
| 🌆 17:00-18:00 | Filtros, paginación y búsqueda                  |

### Domingo

| Hora           | Actividad                       |
| -------------- | ------------------------------- |
| 🌅 9:00-11:00  | Tests con pytest + httpx        |
| 🌅 11:00-12:00 | Manejo de errores (RFC 7807)    |
| 🌞 13:00-14:00 | Polish: validaciones edge cases |
| 🌞 14:00-16:00 | README, Makefile, .env.example  |
| 🌆 16:00-17:00 | Review final y push a GitHub    |

---

## ✅ Definición de "hecho"

- [ ] API funcional con todos los endpoints
- [ ] Docker Compose levanta todo con un solo comando
- [ ] Tests pasan con cobertura ≥ 80%
- [ ] Documentación Swagger generada automáticamente
- [ ] README con instrucciones de setup y uso
- [ ] Código limpio (ruff check sin errores)
- [ ] Repositorio en GitHub con CI básico

---

## 💼 Lo que demuestra al reclutador

| Habilidad       | Evidencia                              |
| --------------- | -------------------------------------- |
| Diseño de APIs  | Endpoints RESTful con buenas prácticas |
| Python avanzado | Async/await, type hints, Pydantic      |
| Bases de datos  | PostgreSQL, migraciones, relaciones    |
| Testing         | pytest con fixtures y cobertura        |
| DevOps básico   | Docker, docker-compose, CI             |
| Documentación   | OpenAPI, README profesional            |
