# 👁️ Semana 10 — PriceWatch

> **Sistema de monitoreo de precios con web scraping, alertas y análisis de tendencias**

| Campo              | Detalle                       |
| ------------------ | ----------------------------- |
| 📅 Fechas          | 9-10 de mayo 2026             |
| 🏷️ Categoría       | Data Engineering & Automation |
| ⏱️ Tiempo estimado | 10-12 horas                   |
| 📊 Dificultad      | ⭐⭐⭐ Intermedio             |

---

## 🎯 Descripción

PriceWatch es un sistema que monitorea precios de productos en sitios web de e-commerce, almacena el historial de precios, detecta cambios significativos y envía alertas. Combina lo aprendido en DataHarvest (scraping) con ingeniería de datos para crear un producto útil y funcional.

---

## ✨ Features

### Monitoreo

- [ ] Configuración de productos a monitorear (URL + selector CSS)
- [ ] Scraping periódico con Selenium
- [ ] Detección de cambios de precio
- [ ] Historial de precios por producto
- [ ] Soporte para múltiples sitios web

### Análisis

- [ ] Tendencias de precio (subida/bajada/estable)
- [ ] Precio mínimo, máximo y promedio histórico
- [ ] Gráficos de evolución de precio (Plotly)
- [ ] Detección de ofertas (caída significativa)

### Alertas

- [ ] Alerta cuando el precio baja de un umbral
- [ ] Alerta por cambio porcentual
- [ ] Notificación por email (SMTP)
- [ ] Log de alertas enviadas

### API y CLI

- [ ] CLI para agregar/remover productos
- [ ] API para consultar precios e historial
- [ ] Dashboard de precios (HTML estático con gráficos)

---

## 🛠️ Stack técnico

| Tecnología   | Propósito                   |
| ------------ | --------------------------- |
| **Selenium** | Web scraping                |
| **Pandas**   | Análisis de datos           |
| **SQLite**   | Almacenamiento de historial |
| **Plotly**   | Gráficos de precios         |
| **FastAPI**  | API REST                    |
| **smtplib**  | Alertas por email           |
| **Typer**    | CLI                         |
| **Docker**   | Containerización            |

---

## 🗓️ Plan del fin de semana

### Sábado

| Hora           | Actividad                                        |
| -------------- | ------------------------------------------------ |
| 🌅 9:00-10:30  | Setup + modelo de datos para productos y precios |
| 🌅 10:30-12:00 | Motor de scraping configurable por producto      |
| 🌞 12:00-13:00 | Almacenamiento de historial en SQLite            |
| 🌞 14:00-16:00 | Detección de cambios + sistema de alertas        |
| 🌆 16:00-18:00 | CLI para gestión de productos                    |

### Domingo

| Hora           | Actividad                         |
| -------------- | --------------------------------- |
| 🌅 9:00-10:30  | Análisis: tendencias, min/max/avg |
| 🌅 10:30-12:00 | Gráficos con Plotly               |
| 🌞 13:00-14:30 | API REST para consultas           |
| 🌞 14:30-16:00 | Tests                             |
| 🌆 16:00-17:00 | README y documentación            |

---

## ✅ Definición de "hecho"

- [ ] Monitoreo funcional de al menos 3 productos
- [ ] Historial de precios persistente
- [ ] Al menos 1 tipo de alerta funcional
- [ ] Gráficos de tendencia
- [ ] CLI y/o API funcional
- [ ] Tests
- [ ] README con setup y ejemplos

---

## 💼 Lo que demuestra al reclutador

| Habilidad          | Evidencia                             |
| ------------------ | ------------------------------------- |
| Scraping avanzado  | Monitoreo periódico, múltiples sitios |
| Análisis de datos  | Tendencias, estadísticas, Plotly      |
| Producto funcional | Sistema útil de verdad                |
| Automatización     | Alertas, ejecución periódica          |
