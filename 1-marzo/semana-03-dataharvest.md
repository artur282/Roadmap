# 🕷️ Semana 03 — DataHarvest

> **Web scraper inteligente con Selenium, Pandas y análisis automatizado de datos**

| Campo              | Detalle             |
| ------------------ | ------------------- |
| 📅 Fechas          | 21-22 de marzo 2026 |
| 🏷️ Categoría       | Backend Foundations |
| ⏱️ Tiempo estimado | 10-12 horas         |
| 📊 Dificultad      | ⭐⭐⭐ Intermedio   |

---

## 🎯 Descripción

DataHarvest es un web scraper robusto y ético que recolecta datos de fuentes públicas (por ejemplo, datos de mercado, empleos tech, o noticias), los procesa con Pandas y los almacena de forma estructurada. Incluye manejo de errores, retries, rotación de user-agents, y exportación a múltiples formatos.

Este proyecto sienta las bases para los proyectos de datos del mes de mayo.

---

## 🏗️ Arquitectura

```
┌──────────────────────────────────┐
│          Scheduler/CLI            │
└───────────────┬──────────────────┘
                │
       ┌────────▼────────┐
       │  Scraper Engine  │
       │  (Selenium +     │
       │   requests)      │
       └────────┬────────┘
                │
   ┌────────────┼────────────┐
   │            │            │
┌──▼───┐  ┌────▼────┐  ┌───▼────┐
│Parser│  │Validator│  │Cleaner │
│(BS4) │  │(Schema) │  │(Pandas)│
└──┬───┘  └────┬────┘  └───┬────┘
   │            │            │
   └────────────┼────────────┘
                │
   ┌────────────▼────────────┐
   │      Data Store          │
   │  (PostgreSQL + CSV/JSON) │
   └──────────────────────────┘
```

---

## ✨ Features

### Scraping

- [ ] Motor de scraping con Selenium (páginas dinámicas)
- [ ] Fallback a requests + BeautifulSoup (páginas estáticas)
- [ ] Rotación de user-agents
- [ ] Manejo de rate limiting y delays éticos
- [ ] Retry con backoff exponencial
- [ ] Respeto de robots.txt

### Procesamiento de datos

- [ ] Limpieza y normalización con Pandas
- [ ] Validación de schema de datos
- [ ] Deduplicación inteligente
- [ ] Transformaciones personalizables
- [ ] Detección de anomalías básicas

### Almacenamiento y exportación

- [ ] Persistencia en PostgreSQL
- [ ] Exportación a CSV, JSON, Excel
- [ ] Historial de ejecuciones
- [ ] Logs detallados de cada run

### CLI

- [ ] Interfaz CLI para ejecutar scrapers
- [ ] Configuración por YAML/TOML
- [ ] Modo dry-run para testing
- [ ] Reporte de resultados en consola

---

## 🛠️ Stack técnico

| Tecnología         | Propósito                         |
| ------------------ | --------------------------------- |
| **Selenium**       | Scraping de páginas dinámicas     |
| **BeautifulSoup4** | Parsing HTML                      |
| **Pandas**         | Procesamiento y limpieza de datos |
| **PostgreSQL**     | Almacenamiento persistente        |
| **SQLAlchemy**     | ORM                               |
| **Typer**          | Interfaz CLI                      |
| **Docker Compose** | Infraestructura                   |
| **pytest**         | Testing                           |

---

## 📁 Estructura del proyecto

```
dataharvest/
├── app/
│   ├── __init__.py
│   ├── cli.py                 # Entry point CLI
│   ├── config.py              # Configuración
│   ├── scrapers/
│   │   ├── base.py            # Clase base de scraper
│   │   ├── jobs_scraper.py    # Scraper de empleos tech
│   │   └── news_scraper.py    # Scraper de noticias
│   ├── processors/
│   │   ├── cleaner.py         # Limpieza de datos
│   │   ├── validator.py       # Validación de schema
│   │   └── transformer.py     # Transformaciones
│   ├── storage/
│   │   ├── database.py        # PostgreSQL
│   │   └── exporters.py       # CSV, JSON, Excel
│   └── utils/
│       ├── user_agents.py     # Rotación UA
│       └── retry.py           # Retry logic
├── tests/
│   ├── test_scrapers.py
│   ├── test_processors.py
│   └── fixtures/              # HTML de ejemplo para tests
├── config/
│   └── scrapers.yml           # Configuración de scrapers
├── docker-compose.yml
├── Makefile
├── pyproject.toml
└── README.md
```

---

## 🗓️ Plan del fin de semana

### Sábado

| Hora           | Actividad                                          |
| -------------- | -------------------------------------------------- |
| 🌅 9:00-10:00  | Setup del proyecto, Docker, dependencias           |
| 🌅 10:00-12:00 | Clase base de scraper + Selenium setup             |
| 🌞 12:00-13:00 | Primer scraper funcional (empleos tech)            |
| 🌞 14:00-16:00 | Procesadores: limpieza, validación, transformación |
| 🌆 16:00-18:00 | Almacenamiento en PostgreSQL + exportadores        |

### Domingo

| Hora           | Actividad                                   |
| -------------- | ------------------------------------------- |
| 🌅 9:00-10:30  | CLI con Typer + configuración YAML          |
| 🌅 10:30-12:00 | Segundo scraper (noticias tech)             |
| 🌞 13:00-14:30 | Tests con fixtures HTML                     |
| 🌞 14:30-16:00 | User-agent rotation, retries, rate limiting |
| 🌆 16:00-17:00 | README y documentación                      |

---

## ✅ Definición de "hecho"

- [ ] Al menos 2 scrapers funcionales
- [ ] Pipeline: scraping → limpieza → validación → almacenamiento
- [ ] Exportación a CSV y JSON
- [ ] CLI funcional con comandos claros
- [ ] Tests con HTML fixtures (sin depender de internet)
- [ ] Manejo de errores y retries
- [ ] README con instrucciones y ejemplos

---

## 💼 Lo que demuestra al reclutador

| Habilidad    | Evidencia                            |
| ------------ | ------------------------------------ |
| Web scraping | Selenium + BS4 + manejo robusto      |
| Datos        | Pandas, limpieza, validación         |
| Diseño       | Patrón base class, plugins, SOLID    |
| Ética        | Respeto de robots.txt, rate limiting |
| Testing      | Tests sin dependencias externas      |
