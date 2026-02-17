# 📋 Semana 18 — ProjectHub

> **App full-stack de gestión de proyectos con React + FastAPI + PostgreSQL**

| Campo              | Detalle                  |
| ------------------ | ------------------------ |
| 📅 Fechas          | 4-5 de julio 2026        |
| 🏷️ Categoría       | Full-Stack Integration   |
| ⏱️ Tiempo estimado | 10-12 horas              |
| 📊 Dificultad      | ⭐⭐⭐⭐ Intermedio-alto |

---

## 🎯 Descripción

ProjectHub es una aplicación full-stack de gestión de proyectos que combina un frontend moderno con React y TailwindCSS con un backend robusto en FastAPI. Incluye tablero Kanban, gestión de tareas, y autenticación de usuarios. Es el primer proyecto del portafolio que entrega una experiencia de usuario completa.

---

## ✨ Features

### Frontend (React)

- [ ] Dashboard con resumen de proyectos
- [ ] Tablero Kanban drag & drop
- [ ] Lista de tareas con filtros
- [ ] Formularios de crear/editar proyecto y tarea
- [ ] Autenticación (login/registro)
- [ ] Diseño responsive con TailwindCSS
- [ ] Dark mode

### Backend (FastAPI)

- [ ] API REST completa (proyectos, tareas, usuarios)
- [ ] Autenticación JWT
- [ ] Relaciones: usuarios → proyectos → tareas
- [ ] Filtros, paginación, búsqueda
- [ ] PostgreSQL con SQLAlchemy

### Integración

- [ ] React Query para data fetching
- [ ] Estado global con Zustand (o Context)
- [ ] Manejo de errores unificado
- [ ] Loading states y skeletons

---

## 🛠️ Stack técnico

| Tecnología         | Propósito               |
| ------------------ | ----------------------- |
| **React 18**       | Frontend                |
| **TailwindCSS**    | Estilos                 |
| **React Query**    | Data fetching           |
| **Zustand**        | Estado global           |
| **FastAPI**        | Backend                 |
| **PostgreSQL**     | Base de datos           |
| **SQLAlchemy**     | ORM                     |
| **Docker Compose** | Frontend + Backend + DB |

---

## 🗓️ Plan del fin de semana

### Sábado

| Hora           | Actividad                                   |
| -------------- | ------------------------------------------- |
| 🌅 9:00-10:00  | Setup: Vite + React + FastAPI + Docker      |
| 🌅 10:00-12:00 | Backend: modelos, auth, CRUD                |
| 🌞 12:00-13:00 | Frontend: layout principal, routing         |
| 🌞 14:00-16:00 | Frontend: login/registro + integración auth |
| 🌆 16:00-18:00 | Frontend: dashboard + lista de proyectos    |

### Domingo

| Hora           | Actividad                     |
| -------------- | ----------------------------- |
| 🌅 9:00-11:00  | Tablero Kanban (drag & drop)  |
| 🌅 11:00-12:00 | CRUD de tareas desde frontend |
| 🌞 13:00-14:30 | Polish: dark mode, responsive |
| 🌞 14:30-16:00 | Tests básicos                 |
| 🌆 16:00-17:00 | README con screenshots        |

---

## ✅ Definición de "hecho"

- [ ] App funcional: login → ver proyectos → gestionar tareas
- [ ] Kanban drag & drop
- [ ] Responsive y dark mode
- [ ] Docker Compose (frontend + backend + DB)
- [ ] Tests básicos de API
- [ ] README con screenshots

---

## 💼 Lo que demuestra al reclutador

| Habilidad   | Evidencia                          |
| ----------- | ---------------------------------- |
| Full-stack  | React + FastAPI + PostgreSQL       |
| UI/UX       | TailwindCSS, dark mode, responsive |
| Integración | Frontend ↔ Backend completo        |
| Producto    | App funcional de punta a punta     |
