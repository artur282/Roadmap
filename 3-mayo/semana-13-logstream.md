# 📝 Semana 13 — LogStream

> **Sistema de ingestión, almacenamiento y análisis de logs en tiempo pseudo-real**

| Campo              | Detalle                       |
| ------------------ | ----------------------------- |
| 📅 Fechas          | 30-31 de mayo 2026            |
| 🏷️ Categoría       | Data Engineering & Automation |
| ⏱️ Tiempo estimado | 10-12 horas                   |
| 📊 Dificultad      | ⭐⭐⭐ Intermedio             |

---

## 🎯 Descripción

LogStream es un sistema que ingesta logs de aplicaciones (formato JSON structured logging), los almacena en PostgreSQL, y provee una API para consultarlos con filtros avanzados. Incluye un generador de logs simulados, dashboards de métricas básicas y alertas configurables por patrones de error.

Simula un sistema de observabilidad simplificado — una habilidad esencial en equipos de producción.

---

## ✨ Features

### Ingestión

- [ ] API para recibir logs (POST batch)
- [ ] Soporte de logs estructurados (JSON)
- [ ] Niveles: DEBUG, INFO, WARNING, ERROR, CRITICAL
- [ ] Metadatos: service, timestamp, trace_id, tags
- [ ] Generador de logs simulados para demo

### Almacenamiento

- [ ] PostgreSQL con esquema optimizado para logs
- [ ] Índices para búsqueda rápida (timestamp, level, service)
- [ ] Retención configurable (auto-limpieza de logs antiguos)
- [ ] Particionamiento por fecha (si alcanza el tiempo)

### Consulta y análisis

- [ ] Búsqueda por rango de tiempo, nivel, servicio
- [ ] Búsqueda por texto en mensaje
- [ ] Filtrado por tags y metadatos
- [ ] Agrupación por servicio/nivel (conteos)
- [ ] Detección de picos de errores

### Alertas

- [ ] Reglas configurables (ej: >10 errores en 1 minuto)
- [ ] Notificación por log/webhook
- [ ] Historial de alertas disparadas

---

## 🛠️ Stack técnico

| Tecnología      | Propósito                             |
| --------------- | ------------------------------------- |
| **FastAPI**     | API REST                              |
| **PostgreSQL**  | Almacenamiento de logs                |
| **SQLAlchemy**  | ORM                                   |
| **Pandas**      | Análisis y agregación                 |
| **APScheduler** | Tareas periódicas (limpieza, alertas) |
| **Docker**      | Containerización                      |
| **pytest**      | Testing                               |

---

## 🗓️ Plan del fin de semana

### Sábado

| Hora           | Actividad                         |
| -------------- | --------------------------------- |
| 🌅 9:00-10:30  | Setup + modelo de datos para logs |
| 🌅 10:30-12:00 | API de ingestión (batch POST)     |
| 🌞 12:00-13:00 | Generador de logs simulados       |
| 🌞 14:00-16:00 | API de consulta con filtros       |
| 🌆 16:00-18:00 | Búsqueda por texto + agrupaciones |

### Domingo

| Hora           | Actividad                      |
| -------------- | ------------------------------ |
| 🌅 9:00-10:30  | Sistema de alertas por reglas  |
| 🌅 10:30-12:00 | Auto-limpieza de logs antiguos |
| 🌞 13:00-14:30 | Métricas y estadísticas        |
| 🌞 14:30-16:00 | Tests                          |
| 🌆 16:00-17:00 | README y documentación         |

---

## ✅ Definición de "hecho"

- [ ] Ingestión de logs batch funcional
- [ ] Consulta con filtros avanzados
- [ ] Generador de logs para demo
- [ ] Al menos 1 regla de alerta funcional
- [ ] Tests
- [ ] Docker Compose funcional
- [ ] README con setup y ejemplos

---

## 💼 Lo que demuestra al reclutador

| Habilidad        | Evidencia                                    |
| ---------------- | -------------------------------------------- |
| Observabilidad   | Sistema de logs centralizado                 |
| SQL avanzado     | Índices, particionamiento, queries complejas |
| Data engineering | Ingestión, procesamiento, retención          |
| Producción       | Alertas, limpieza, monitoreo                 |
