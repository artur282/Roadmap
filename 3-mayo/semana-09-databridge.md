# 🌉 Semana 09 — DataBridge

> **Pipeline ETL completo con validación, transformación y carga entre sistemas**

| Campo              | Detalle                       |
| ------------------ | ----------------------------- |
| 📅 Fechas          | 2-3 de mayo 2026              |
| 🏷️ Categoría       | Data Engineering & Automation |
| ⏱️ Tiempo estimado | 10-12 horas                   |
| 📊 Dificultad      | ⭐⭐⭐ Intermedio             |

---

## 🎯 Descripción

DataBridge es un pipeline ETL (Extract, Transform, Load) profesional que migra datos entre diferentes fuentes: archivos CSV/JSON, bases SQLite y PostgreSQL. Incluye validación de datos, transformaciones configurables, manejo de errores con rollback, logging detallado y reportes de ejecución.

Simula un escenario real de migración de datos empresariales — una de las tareas más comunes y críticas en ingeniería de datos.

---

## 🏗️ Arquitectura

```
┌──────────────────────────────────────────────────────┐
│                    Pipeline ETL                       │
│                                                      │
│  ┌──────────┐    ┌──────────┐    ┌──────────┐       │
│  │ EXTRACT  │───▶│TRANSFORM │───▶│   LOAD   │       │
│  │          │    │          │    │          │       │
│  │ • CSV    │    │ • Clean  │    │ • PostgreSQL│     │
│  │ • JSON   │    │ • Validate│   │ • Batch   │     │
│  │ • SQLite │    │ • Convert │   │ • Upsert  │     │
│  │ • API    │    │ • Enrich  │   │ • Rollback│     │
│  └──────────┘    └──────────┘    └──────────┘       │
│       │               │               │              │
│       └───────────────┼───────────────┘              │
│                       │                              │
│              ┌────────▼────────┐                     │
│              │   Orchestrator   │                     │
│              │   (Pipeline      │                     │
│              │    Manager)      │                     │
│              └────────┬────────┘                     │
│                       │                              │
│       ┌───────────────┼───────────────┐              │
│       │               │               │              │
│  ┌────▼────┐    ┌────▼────┐    ┌────▼────┐         │
│  │ Logger  │    │ Reporter│    │ Monitor │         │
│  └─────────┘    └─────────┘    └─────────┘         │
└──────────────────────────────────────────────────────┘
```

---

## ✨ Features

### Extract (Extracción)

- [ ] Lectura de archivos CSV con diferentes encodings
- [ ] Lectura de archivos JSON y JSON Lines
- [ ] Extracción desde SQLite
- [ ] Extracción desde APIs REST
- [ ] Lectores configurables y extensibles

### Transform (Transformación)

- [ ] Limpieza de datos (nulls, duplicados, whitespace)
- [ ] Validación con schemas (Pydantic/Pandera)
- [ ] Conversión de tipos de datos
- [ ] Normalización de campos (fechas, monedas, emails)
- [ ] Enriquecimiento (campos calculados)
- [ ] Transformaciones configurables por YAML

### Load (Carga)

- [ ] Carga a PostgreSQL
- [ ] Inserción batch (bulk insert)
- [ ] Upsert (insert or update)
- [ ] Transacciones con rollback en caso de error
- [ ] Exportación a CSV/JSON (alternativa)

### Orquestación

- [ ] Pipeline configurable por YAML
- [ ] Ejecución por CLI
- [ ] Logging detallado (por paso y por fila)
- [ ] Reporte de ejecución (filas procesadas, errores, duración)
- [ ] Modo dry-run (validar sin cargar)

---

## 🛠️ Stack técnico

| Tecnología         | Propósito                 |
| ------------------ | ------------------------- |
| **Python 3.11+**   | Lenguaje base             |
| **Pandas**         | Procesamiento de datos    |
| **Pandera**        | Validación de schemas     |
| **SQLAlchemy**     | Conexión a bases de datos |
| **PostgreSQL**     | Destino principal         |
| **SQLite**         | Fuente de ejemplo         |
| **Typer**          | CLI                       |
| **Rich**           | Visualización de progreso |
| **Docker Compose** | Infraestructura           |
| **pytest**         | Testing                   |

---

## 🗓️ Plan del fin de semana

### Sábado

| Hora           | Actividad                                       |
| -------------- | ----------------------------------------------- |
| 🌅 9:00-10:00  | Setup, Docker Compose, estructura               |
| 🌅 10:00-12:00 | Extractores: CSV, JSON, SQLite                  |
| 🌞 12:00-13:00 | Transformadores: limpieza, validación           |
| 🌞 14:00-16:00 | Transformadores: normalización, enriquecimiento |
| 🌆 16:00-18:00 | Loaders: PostgreSQL (batch + upsert)            |

### Domingo

| Hora           | Actividad                                  |
| -------------- | ------------------------------------------ |
| 🌅 9:00-10:30  | Pipeline orchestrator + configuración YAML |
| 🌅 10:30-12:00 | CLI + modo dry-run                         |
| 🌞 13:00-14:30 | Logging, reportes de ejecución             |
| 🌞 14:30-16:00 | Tests con datasets de ejemplo              |
| 🌆 16:00-17:00 | README con ejemplos y diagramas            |

---

## ✅ Definición de "hecho"

- [ ] Pipeline funcional CSV → Transform → PostgreSQL
- [ ] Al menos 3 extractores y 5 transformadores
- [ ] Validación de datos con reporte de errores
- [ ] CLI con modo normal y dry-run
- [ ] Tests con datasets fixture
- [ ] Docker Compose funcional
- [ ] README con ejemplos y configuración

---

## 💼 Lo que demuestra al reclutador

| Habilidad    | Evidencia                                    |
| ------------ | -------------------------------------------- |
| ETL          | Pipeline completo extract → transform → load |
| Datos        | Pandas, validación, limpieza a escala        |
| SQL          | PostgreSQL, batch insert, upsert             |
| Arquitectura | Pipeline pattern, plugins, configuración     |
| Producción   | Logging, rollback, reportes                  |
