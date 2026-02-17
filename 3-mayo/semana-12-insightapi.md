# 📈 Semana 12 — InsightAPI

> **API de reportes dinámicos con Pandas, visualizaciones y exportación multi-formato**

| Campo              | Detalle                       |
| ------------------ | ----------------------------- |
| 📅 Fechas          | 23-24 de mayo 2026            |
| 🏷️ Categoría       | Data Engineering & Automation |
| ⏱️ Tiempo estimado | 10-12 horas                   |
| 📊 Dificultad      | ⭐⭐⭐ Intermedio             |

---

## 🎯 Descripción

InsightAPI es una API que genera reportes dinámicos a partir de datos almacenados en PostgreSQL. Los usuarios pueden solicitar reportes configurables (filtros, agrupaciones, métricas), obtener visualizaciones como gráficos interactivos (Plotly), y exportar los resultados en múltiples formatos (JSON, CSV, PDF).

---

## ✨ Features

### Reportes

- [ ] Reportes configurables por parámetros (filtros, rango de fechas, agrupación)
- [ ] Métricas calculadas (suma, promedio, conteo, percentiles)
- [ ] Agrupación por dimensiones (categoría, fecha, región)
- [ ] Comparación de períodos (mes actual vs anterior)
- [ ] Templates de reportes predefinidos

### Visualizaciones

- [ ] Gráficos de barras, líneas, pie (Plotly)
- [ ] Gráficos interactivos embebidos en HTML
- [ ] Exportación de gráficos como imagen (PNG)

### Exportación

- [ ] JSON (datos crudos)
- [ ] CSV (descarga directa)
- [ ] Excel (.xlsx)
- [ ] PDF con formato (ReportLab/WeasyPrint)

### Datos de ejemplo

- [ ] Dataset de ventas ficticio (seed)
- [ ] Generador de datos de prueba

---

## 🛠️ Stack técnico

| Tecnología     | Propósito                  |
| -------------- | -------------------------- |
| **FastAPI**    | API REST                   |
| **Pandas**     | Procesamiento y agregación |
| **Plotly**     | Visualizaciones            |
| **PostgreSQL** | Base de datos              |
| **SQLAlchemy** | ORM                        |
| **ReportLab**  | Generación de PDF          |
| **openpyxl**   | Exportación Excel          |
| **Docker**     | Containerización           |

---

## 🗓️ Plan del fin de semana

### Sábado

| Hora           | Actividad                                           |
| -------------- | --------------------------------------------------- |
| 🌅 9:00-10:30  | Setup + modelo de datos + seed de ventas            |
| 🌅 10:30-12:00 | Engine de reportes con Pandas (filtros, agrupación) |
| 🌞 12:00-13:00 | Métricas calculadas y comparaciones                 |
| 🌞 14:00-16:00 | Visualizaciones con Plotly                          |
| 🌆 16:00-18:00 | API endpoints (solicitar reporte, consultar)        |

### Domingo

| Hora           | Actividad                          |
| -------------- | ---------------------------------- |
| 🌅 9:00-10:30  | Exportación: CSV, JSON, Excel      |
| 🌅 10:30-12:00 | Exportación: PDF con formato       |
| 🌞 13:00-14:30 | Templates de reportes predefinidos |
| 🌞 14:30-16:00 | Tests                              |
| 🌆 16:00-17:00 | README con ejemplos y screenshots  |

---

## ✅ Definición de "hecho"

- [ ] Al menos 3 tipos de reportes configurables
- [ ] Visualizaciones interactivas con Plotly
- [ ] Exportación a JSON, CSV y al menos un formato más
- [ ] Datos de ejemplo con seed
- [ ] Tests
- [ ] Docker Compose funcional
- [ ] README con ejemplos de reportes

---

## 💼 Lo que demuestra al reclutador

| Habilidad         | Evidencia                       |
| ----------------- | ------------------------------- |
| Análisis de datos | Pandas, agregaciones, métricas  |
| Visualización     | Plotly, gráficos interactivos   |
| API Design        | Reportes configurables por API  |
| Exportación       | Multi-formato (CSV, PDF, Excel) |
