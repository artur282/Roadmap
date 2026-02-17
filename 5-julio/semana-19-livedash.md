# 📊 Semana 19 — LiveDash

> **Dashboard en tiempo real con WebSockets, gráficos interactivos y datos en vivo**

| Campo              | Detalle                  |
| ------------------ | ------------------------ |
| 📅 Fechas          | 11-12 de julio 2026      |
| 🏷️ Categoría       | Full-Stack Integration   |
| ⏱️ Tiempo estimado | 10-12 horas              |
| 📊 Dificultad      | ⭐⭐⭐⭐ Intermedio-alto |

---

## 🎯 Descripción

LiveDash es un dashboard que muestra datos en tiempo real usando WebSockets. Un backend FastAPI genera o recibe datos en vivo (simulando métricas de servidor, sensores IoT, o tráfico web), los transmite via WebSocket a un frontend React que los renderiza en gráficos interactivos que se actualizan automáticamente.

---

## ✨ Features

### Tiempo real

- [ ] WebSocket connection (FastAPI ↔ React)
- [ ] Datos actualizados cada 1-2 segundos
- [ ] Reconexión automática
- [ ] Indicador de estado de conexión

### Dashboard

- [ ] Gráfico de líneas en tiempo real (últimos N datos)
- [ ] Gráfico de barras actualizable
- [ ] Cards con métricas (KPIs)
- [ ] Historial de datos (últimas 24h)
- [ ] Selección de métricas/fuentes

### Backend

- [ ] WebSocket endpoint con broadcast
- [ ] Generador de datos simulados (configurable)
- [ ] API REST para datos históricos
- [ ] Almacenamiento de métricas en SQLite/PostgreSQL

### UI

- [ ] Layout tipo dashboard (grid)
- [ ] Animaciones suaves en actualizaciones
- [ ] Responsive
- [ ] Tema oscuro optimizado para dashboards

---

## 🛠️ Stack técnico

| Tecnología              | Propósito                   |
| ----------------------- | --------------------------- |
| **FastAPI**             | Backend + WebSockets        |
| **React**               | Frontend                    |
| **Recharts / Chart.js** | Gráficos                    |
| **TailwindCSS**         | Estilos                     |
| **WebSockets**          | Comunicación en tiempo real |
| **SQLite**              | Almacenamiento de métricas  |
| **Docker**              | Containerización            |

---

## 🗓️ Plan del fin de semana

### Sábado

| Hora           | Actividad                                         |
| -------------- | ------------------------------------------------- |
| 🌅 9:00-10:00  | Setup: FastAPI + React + WebSocket básico         |
| 🌅 10:00-12:00 | Backend: generador de datos + WebSocket broadcast |
| 🌞 12:00-13:00 | Backend: almacenamiento de métricas               |
| 🌞 14:00-16:00 | Frontend: layout dashboard + WebSocket client     |
| 🌆 16:00-18:00 | Frontend: gráfico de líneas en tiempo real        |

### Domingo

| Hora           | Actividad                                   |
| -------------- | ------------------------------------------- |
| 🌅 9:00-10:30  | KPI cards + gráfico de barras               |
| 🌅 10:30-12:00 | Datos históricos (API REST)                 |
| 🌞 13:00-14:30 | Reconexión automática + indicador de estado |
| 🌞 14:30-16:00 | Polish: animaciones, responsive, dark mode  |
| 🌆 16:00-17:00 | README con screenshots/GIFs                 |

---

## ✅ Definición de "hecho"

- [ ] Datos en tiempo real via WebSocket
- [ ] Al menos 2 tipos de gráficos
- [ ] KPI cards actualizables
- [ ] Reconexión automática
- [ ] Docker Compose funcional
- [ ] README con screenshots o GIFs

---

## 💼 Lo que demuestra al reclutador

| Habilidad     | Evidencia                                 |
| ------------- | ----------------------------------------- |
| WebSockets    | Comunicación bidireccional en tiempo real |
| Visualización | Gráficos dinámicos, dashboards            |
| Full-stack    | Integración frontend ↔ backend            |
| UX            | Animaciones, indicadores, responsive      |
