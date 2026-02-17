# ⚡ Semana 11 — FlowEngine

> **Automatización de flujos empresariales con n8n, webhooks y APIs**

| Campo              | Detalle                       |
| ------------------ | ----------------------------- |
| 📅 Fechas          | 16-17 de mayo 2026            |
| 🏷️ Categoría       | Data Engineering & Automation |
| ⏱️ Tiempo estimado | 10-12 horas                   |
| 📊 Dificultad      | ⭐⭐⭐ Intermedio             |

---

## 🎯 Descripción

FlowEngine es un proyecto que demuestra dominio de n8n para automatización de flujos empresariales. Incluye la creación de workflows complejos que integran múltiples servicios: webhooks, APIs REST, bases de datos, notificaciones por email y procesamiento de datos. Además, incluye un backend custom con FastAPI que actúa como fuente de datos y receptor de webhooks.

---

## ✨ Features

### Workflows n8n

- [ ] **Workflow 1: Lead Processing** — Webhook recibe lead → valida datos → guarda en DB → notifica por email
- [ ] **Workflow 2: Data Sync** — Cron trigger → extrae datos de API → transforma → carga en DB
- [ ] **Workflow 3: Report Generator** — Trigger diario → consulta DB → genera reporte → envía por email
- [ ] **Workflow 4: Alert Monitor** — Polling de API → detecta condiciones → envía alerta

### Backend (FastAPI)

- [ ] API REST como fuente de datos para los workflows
- [ ] Webhook receiver para triggers de n8n
- [ ] Base de datos PostgreSQL para persistencia
- [ ] Endpoints de consulta para reportes

### Infraestructura

- [ ] Docker Compose: n8n + FastAPI + PostgreSQL
- [ ] Configuración de credenciales segura
- [ ] Documentación de cada workflow
- [ ] Export de workflows como JSON

---

## 🛠️ Stack técnico

| Tecnología         | Propósito                 |
| ------------------ | ------------------------- |
| **n8n**            | Orquestación de workflows |
| **FastAPI**        | Backend API               |
| **PostgreSQL**     | Base de datos             |
| **Docker Compose** | Infraestructura           |
| **SMTP**           | Notificaciones            |
| **Webhooks**       | Triggers y callbacks      |

---

## 🗓️ Plan del fin de semana

### Sábado

| Hora           | Actividad                                  |
| -------------- | ------------------------------------------ |
| 🌅 9:00-10:30  | Docker Compose: n8n + FastAPI + PostgreSQL |
| 🌅 10:30-12:00 | Backend FastAPI: endpoints para datos      |
| 🌞 12:00-13:00 | Workflow 1: Lead Processing                |
| 🌞 14:00-16:00 | Workflow 2: Data Sync                      |
| 🌆 16:00-18:00 | Workflow 3: Report Generator               |

### Domingo

| Hora           | Actividad                           |
| -------------- | ----------------------------------- |
| 🌅 9:00-10:30  | Workflow 4: Alert Monitor           |
| 🌅 10:30-12:00 | Webhook receiver en FastAPI         |
| 🌞 13:00-14:30 | Testing de flujos end-to-end        |
| 🌞 14:30-16:00 | Export de workflows + documentación |
| 🌆 16:00-17:00 | README con screenshots de n8n       |

---

## ✅ Definición de "hecho"

- [ ] Al menos 3 workflows funcionales en n8n
- [ ] Backend FastAPI con endpoints operativos
- [ ] Docker Compose levanta todo con un comando
- [ ] Workflows exportados como JSON
- [ ] Documentación de cada workflow con diagrama
- [ ] README con setup y screenshots

---

## 💼 Lo que demuestra al reclutador

| Habilidad       | Evidencia                     |
| --------------- | ----------------------------- |
| Automatización  | n8n, workflows complejos      |
| Integración     | APIs, webhooks, DB, email     |
| Low-code + code | Combinación n8n + FastAPI     |
| DevOps          | Docker Compose multi-servicio |
