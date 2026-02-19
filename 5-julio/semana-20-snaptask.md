# 📱 Semana 20 — SnapTask

> **App móvil de gestión de tareas con React Native, Expo y sincronización en la nube**

| Campo              | Detalle                |
| ------------------ | ---------------------- |
| 📅 Fechas          | 18-19 de julio 2026    |
| 🏷️ Categoría       | Full-Stack Integration |
| ⏱️ Tiempo estimado | 10-12 horas            |
| 📊 Dificultad      | ⭐⭐⭐ Intermedio      |

---

## 🎯 Descripción

SnapTask es una aplicación móvil de gestión de tareas construida con **React Native** y **Expo**, diseñada para funcionar en Android e iOS desde una sola base de código. Incluye un backend con FastAPI para sincronización en la nube, notificaciones push y categorización inteligente de tareas.

Este proyecto demuestra la capacidad de extender habilidades full-stack al desarrollo móvil, manteniendo código limpio y reutilizable con TypeScript y el ecosistema de React Native.

---

## ✨ Features

### Gestión de tareas

- [ ] Crear, editar y eliminar tareas con título, descripción y prioridad
- [ ] Categorías personalizables con colores e íconos
- [ ] Fechas límite con recordatorios locales
- [ ] Estados: pendiente, en progreso, completada
- [ ] Gestos de deslizamiento para acciones rápidas (completar, eliminar)

### Interfaz móvil nativa

- [ ] Navegación fluida con React Navigation (tabs + stack)
- [ ] Pantalla principal con lista de tareas agrupadas por fecha
- [ ] Pantalla de detalle de tarea con edición inline
- [ ] Dark mode / Light mode con toggle automático
- [ ] Animaciones suaves con Reanimated
- [ ] Pull-to-refresh para sincronización

### Sincronización en la nube

- [ ] Backend FastAPI con endpoints REST
- [ ] Autenticación con JWT (login/registro)
- [ ] Sincronización bidireccional de tareas
- [ ] Almacenamiento local con AsyncStorage (funciona offline)
- [ ] Resolución de conflictos (última escritura gana)

### Notificaciones

- [ ] Notificaciones push con Expo Notifications
- [ ] Recordatorios programados para tareas con fecha límite
- [ ] Badge de la app con conteo de tareas pendientes

---

## 🛠️ Stack técnico

| Tecnología               | Propósito                                  |
| ------------------------ | ------------------------------------------ |
| **React Native**         | Framework de desarrollo móvil              |
| **Expo**                 | Plataforma de desarrollo y distribución    |
| **TypeScript**           | Tipado estático y código más seguro        |
| **React Navigation**     | Navegación entre pantallas (tabs + stack)  |
| **Reanimated**           | Animaciones de alto rendimiento            |
| **AsyncStorage**         | Almacenamiento local persistente           |
| **Expo Notifications**   | Notificaciones push y locales              |
| **FastAPI**              | Backend API REST                           |
| **PostgreSQL**           | Base de datos del backend                  |
| **JWT (python-jose)**    | Autenticación basada en tokens             |

---

## 📁 Estructura del proyecto

```
snaptask/
├── mobile/                        # App React Native + Expo
│   ├── app/                       # Pantallas (Expo Router)
│   │   ├── (tabs)/
│   │   │   ├── index.tsx          # Pantalla principal (lista tareas)
│   │   │   ├── categories.tsx     # Gestión de categorías
│   │   │   └── settings.tsx       # Configuración y perfil
│   │   ├── task/
│   │   │   └── [id].tsx           # Detalle de tarea
│   │   ├── auth/
│   │   │   ├── login.tsx          # Inicio de sesión
│   │   │   └── register.tsx       # Registro
│   │   └── _layout.tsx            # Layout raíz
│   ├── components/
│   │   ├── TaskCard.tsx           # Tarjeta de tarea con gestos
│   │   ├── TaskForm.tsx           # Formulario de tarea
│   │   ├── CategoryBadge.tsx      # Badge de categoría
│   │   └── EmptyState.tsx         # Estado vacío ilustrado
│   ├── hooks/
│   │   ├── useTasks.ts            # Hook de gestión de tareas
│   │   ├── useAuth.ts             # Hook de autenticación
│   │   └── useSync.ts             # Hook de sincronización
│   ├── services/
│   │   ├── api.ts                 # Cliente HTTP (axios)
│   │   ├── storage.ts             # AsyncStorage helpers
│   │   └── notifications.ts      # Expo Notifications setup
│   ├── theme/
│   │   └── colors.ts              # Paleta de colores (dark/light)
│   ├── types/
│   │   └── index.ts               # Tipos TypeScript
│   ├── app.json                   # Configuración Expo
│   ├── package.json
│   └── tsconfig.json
├── backend/                       # API FastAPI
│   ├── app/
│   │   ├── main.py                # Entry point FastAPI
│   │   ├── models.py              # Modelos SQLAlchemy
│   │   ├── schemas.py             # Pydantic schemas
│   │   ├── routes/
│   │   │   ├── auth.py            # Endpoints de autenticación
│   │   │   └── tasks.py           # Endpoints CRUD de tareas
│   │   └── database.py            # Configuración de BD
│   ├── requirements.txt
│   └── Dockerfile
├── docker-compose.yml             # Backend + PostgreSQL
├── Makefile
└── README.md
```

---

## 🗓️ Plan del fin de semana

### Sábado

| Hora           | Actividad                                              |
| -------------- | ------------------------------------------------------ |
| 🌅 9:00-10:00  | Setup: Expo, React Navigation, estructura del proyecto |
| 🌅 10:00-12:00 | Pantalla principal: lista de tareas + TaskCard          |
| 🌞 12:00-13:00 | Backend FastAPI: modelos, auth JWT, CRUD tareas         |
| 🌞 14:00-16:00 | Pantalla de detalle + formulario de tarea               |
| 🌆 16:00-18:00 | Categorías, prioridades y gestos de deslizamiento       |

### Domingo

| Hora           | Actividad                                           |
| -------------- | --------------------------------------------------- |
| 🌅 9:00-10:30  | Sincronización: hooks useSync, AsyncStorage offline  |
| 🌅 10:30-12:00 | Dark mode + animaciones con Reanimated               |
| 🌞 13:00-14:30 | Notificaciones push + recordatorios programados      |
| 🌞 14:30-16:00 | Tests (Jest + React Native Testing Library)          |
| 🌆 16:00-17:00 | README con capturas de pantalla y video demo          |

---

## ✅ Definición de "hecho"

- [ ] CRUD completo de tareas funcionando en la app móvil
- [ ] Navegación fluida entre pantallas (tabs + stack)
- [ ] Sincronización con backend FastAPI
- [ ] Modo offline con AsyncStorage
- [ ] Dark mode y Light mode
- [ ] Al menos una animación con Reanimated
- [ ] Notificaciones locales para recordatorios
- [ ] Tests unitarios de componentes clave
- [ ] README con capturas de pantalla en ambos temas
- [ ] Docker Compose para el backend

---

## 🧠 Conceptos de React Native demostrados

| Concepto                     | Aplicación en el proyecto                     |
| ---------------------------- | --------------------------------------------- |
| Componentes funcionales      | Todas las pantallas y componentes con hooks    |
| Custom hooks                 | useTasks, useAuth, useSync                     |
| React Navigation             | Tab navigator + Stack navigator               |
| Gestos nativos               | Swipeable para acciones rápidas                |
| Animaciones (Reanimated)     | Transiciones y micro-interacciones             |
| Almacenamiento local         | AsyncStorage para persistencia offline         |
| Temas dinámicos              | Dark/Light mode con contexto de React          |
| TypeScript                   | Tipos estrictos en toda la app                 |
| Expo ecosystem               | Notifications, Router, config plugins          |

---

## 💼 Lo que demuestra al reclutador

| Habilidad                  | Evidencia                                           |
| -------------------------- | --------------------------------------------------- |
| Desarrollo móvil           | App nativa funcional en Android/iOS                  |
| React Native + Expo        | Ecosystem completo, navegación, notificaciones       |
| Full-stack mobile           | App móvil + Backend FastAPI + PostgreSQL              |
| TypeScript                 | Tipado estricto en frontend y backend                |
| UX/UI móvil                | Gestos, animaciones, dark mode, experiencia pulida   |
| Offline-first              | Funciona sin conexión con sincronización posterior    |
| Arquitectura limpia        | Separación de concerns con hooks y services          |
