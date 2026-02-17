# 🔔 Semana 21 — NotifyHub

> **Sistema de notificaciones multi-canal con FastAPI, Celery y panel de gestión**

| Campo              | Detalle                  |
| ------------------ | ------------------------ |
| 📅 Fechas          | 25-26 de julio 2026      |
| 🏷️ Categoría       | Full-Stack Integration   |
| ⏱️ Tiempo estimado | 10-12 horas              |
| 📊 Dificultad      | ⭐⭐⭐⭐ Intermedio-alto |

---

## 🎯 Descripción

NotifyHub es un sistema de notificaciones que envía mensajes por múltiples canales: email, webhook y en-app. Usa Celery para procesamiento asíncrono, Redis como broker de mensajes, y un frontend React para configurar y monitorear las notificaciones. Demuestra manejo de tareas asíncronas y mensajería.

---

## ✨ Features

### Canales de notificación

- [ ] **Email** — Enviar notificaciones por SMTP
- [ ] **Webhook** — POST a URL configurable
- [ ] **In-App** — Notificaciones consultables por API

### Procesamiento asíncrono

- [ ] Celery workers para envío
- [ ] Redis como message broker
- [ ] Retry automático en caso de fallo
- [ ] Dead letter queue para fallos permanentes
- [ ] Rate limiting por canal

### API

- [ ] Enviar notificación (seleccionar canal)
- [ ] Enviar a múltiples canales simultáneamente
- [ ] Templates de notificación (Jinja2)
- [ ] Historial de notificaciones
- [ ] Estado de entrega (pending, sent, failed)

### Panel de gestión (React)

- [ ] Dashboard: notificaciones enviadas, fallidas, pendientes
- [ ] Configurar canales y destinatarios
- [ ] Ver historial con filtros
- [ ] Crear y editar templates

---

## 🛠️ Stack técnico

| Tecnología         | Propósito                 |
| ------------------ | ------------------------- |
| **FastAPI**        | API REST                  |
| **Celery**         | Procesamiento asíncrono   |
| **Redis**          | Message broker            |
| **PostgreSQL**     | Almacenamiento            |
| **React**          | Panel de gestión          |
| **Jinja2**         | Templates de notificación |
| **SMTP**           | Canal email               |
| **Docker Compose** | Infraestructura completa  |

---

## 🗓️ Plan del fin de semana

### Sábado

| Hora           | Actividad                                    |
| -------------- | -------------------------------------------- |
| 🌅 9:00-10:30  | Setup: FastAPI + Celery + Redis + Docker     |
| 🌅 10:30-12:00 | Modelos: notificaciones, templates, destinos |
| 🌞 12:00-13:00 | Canal email (SMTP + Celery task)             |
| 🌞 14:00-16:00 | Canal webhook + in-app                       |
| 🌆 16:00-18:00 | API: enviar, listar, historial               |

### Domingo

| Hora           | Actividad                            |
| -------------- | ------------------------------------ |
| 🌅 9:00-10:30  | Templates Jinja2 + envío multi-canal |
| 🌅 10:30-12:00 | Retry, dead letter, rate limiting    |
| 🌞 13:00-14:30 | Panel React: dashboard + historial   |
| 🌞 14:30-16:00 | Tests                                |
| 🌆 16:00-17:00 | README y documentación               |

---

## ✅ Definición de "hecho"

- [ ] Al menos 2 canales de notificación funcionales
- [ ] Celery con retry automático
- [ ] Templates de notificación
- [ ] Historial con estado de entrega
- [ ] Docker Compose (API + Celery + Redis + DB)
- [ ] README

---

## 💼 Lo que demuestra al reclutador

| Habilidad    | Evidencia                         |
| ------------ | --------------------------------- |
| Async        | Celery, Redis, tareas asíncronas  |
| Arquitectura | Mensajería, multi-canal           |
| Producción   | Retry, dead letter, rate limiting |
| Full-stack   | API + Panel de gestión            |
