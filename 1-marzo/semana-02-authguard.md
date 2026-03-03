# 🔐 Semana 02 — AuthGuard

> **Sistema de autenticación y autorización completo con Django, DRF y JWT**

| Campo              | Detalle             |
| ------------------ | ------------------- |
| 📅 Fechas          | 14-15 de marzo 2026 |
| 🏷️ Categoría       | Backend Foundations |
| ⏱️ Tiempo estimado | 10-12 horas         |
| 📦 Repositorio     | [artur282/AuthGuard](https://github.com/artur282/AuthGuard) |
| 📊 Dificultad      | ⭐⭐⭐ Intermedio   |

---

## 🎯 Descripción

AuthGuard es un sistema de autenticación y autorización listo para producción construido con Django y Django REST Framework. Va más allá del login básico: implementa JWT con refresh tokens, roles y permisos granulares, registro con verificación de email, y endpoints seguros.

Este proyecto se puede reutilizar como módulo de autenticación en cualquier proyecto futuro del portafolio.

---

## 🏗️ Arquitectura

```
┌─────────────────────────────────────────┐
│              Cliente (HTTP)              │
└──────────────────┬──────────────────────┘
                   │
          ┌────────▼────────┐
          │   Django + DRF  │
          │   (Views +      │
          │   Permissions)   │
          └────────┬────────┘
                   │
     ┌─────────────┼─────────────┐
     │             │             │
┌────▼────┐  ┌────▼────┐  ┌────▼────┐
│  Auth   │  │  Users  │  │  Roles  │
│ Module  │  │ Module  │  │ Module  │
│ (JWT)   │  │ (CRUD)  │  │ (RBAC)  │
└────┬────┘  └────┬────┘  └────┬────┘
     │             │             │
     └─────────────┼─────────────┘
                   │
          ┌────────▼────────┐
          │   PostgreSQL     │
          │   (Docker)       │
          └─────────────────┘
```

---

## ✨ Features

### Autenticación

- [x] Registro de usuarios con validación
- [x] Login con JWT (access + refresh tokens)
- [x] Refresh token rotation
- [x] Logout (blacklist de tokens)
- [x] Cambio de contraseña
- [x] Reset de contraseña (flujo completo)

### Autorización (RBAC)

- [x] Roles predefinidos (admin, editor, viewer)
- [x] Permisos granulares por recurso
- [x] Decoradores de permisos personalizados
- [x] Middleware de autenticación

### Gestión de usuarios

- [x] CRUD de usuarios (solo admin)
- [x] Perfil de usuario (lectura/edición propia)
- [x] Listado con filtros y paginación
- [x] Soft delete de usuarios
- [x] Auditoría de último login

### Seguridad

- [x] Rate limiting en endpoints de auth
- [x] Password hashing (bcrypt/argon2)
- [x] Validación de fortaleza de contraseña
- [x] Protección contra brute force
- [x] Headers de seguridad (CORS, CSRF)

---

## 🛠️ Stack técnico

| Tecnología                | Propósito             |
| ------------------------- | --------------------- |
| **Django 5.x**            | Framework web         |
| **Django REST Framework** | API REST              |
| **SimpleJWT**             | Tokens JWT            |
| **PostgreSQL 16**         | Base de datos         |
| **Docker Compose**        | Infraestructura local |
| **pytest-django**         | Testing               |
| **Ruff**                  | Linting               |
| **drf-spectacular**       | Documentación OpenAPI |

---

## 📡 Endpoints de la API

```
POST   /api/v1/auth/register         # Registro
POST   /api/v1/auth/login             # Login → access + refresh
POST   /api/v1/auth/refresh           # Refresh token
POST   /api/v1/auth/logout            # Logout (blacklist token)
POST   /api/v1/auth/change-password   # Cambiar contraseña
POST   /api/v1/auth/reset-password    # Solicitar reset
POST   /api/v1/auth/reset-confirm     # Confirmar reset con token

GET    /api/v1/users/me               # Mi perfil
PUT    /api/v1/users/me               # Editar mi perfil
GET    /api/v1/users                  # Listar usuarios (admin)
GET    /api/v1/users/{id}             # Ver usuario (admin)
DELETE /api/v1/users/{id}             # Eliminar usuario (admin)

GET    /api/v1/roles                  # Listar roles
POST   /api/v1/users/{id}/roles       # Asignar rol (admin)
```

---

## 🗓️ Plan del fin de semana

### Sábado

| Hora           | Actividad                                     |
| -------------- | --------------------------------------------- |
| 🌅 9:00-10:00  | Setup: Django project, Docker Compose, config |
| 🌅 10:00-11:30 | Modelo de usuario custom + migraciones        |
| 🌞 11:30-13:00 | Registro y login con JWT (SimpleJWT)          |
| 🌞 14:00-16:00 | Refresh tokens, logout, cambio de password    |
| 🌆 16:00-18:00 | Sistema de roles y permisos (RBAC)            |

### Domingo

| Hora           | Actividad                           |
| -------------- | ----------------------------------- |
| 🌅 9:00-11:00  | CRUD de usuarios + perfil           |
| 🌅 11:00-12:30 | Tests de autenticación y permisos   |
| 🌞 13:30-15:00 | Rate limiting + seguridad           |
| 🌞 15:00-16:30 | Documentación API (drf-spectacular) |
| 🌆 16:30-17:30 | README y push a GitHub              |

---

## ✅ Definición de "hecho"

- [x] Flujo completo de autenticación funcional
- [x] RBAC con al menos 3 roles
- [x] Tests de cada endpoint de auth
- [x] Rate limiting configurado
- [x] Documentación OpenAPI completa
- [x] Docker Compose funcional
- [x] README con instrucciones y ejemplos de uso

---

## 💼 Lo que demuestra al reclutador

| Habilidad  | Evidencia                                     |
| ---------- | --------------------------------------------- |
| Seguridad  | JWT, RBAC, rate limiting, password hashing    |
| Django     | Modelo custom de usuario, middleware, signals |
| API Design | Endpoints RESTful, errores consistentes       |
| Patrones   | Separación de responsabilidades, SOLID        |
| Testing    | Flujos de auth complejos testeados            |
