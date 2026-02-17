# 🔬 Semana 08 — SentiScope

> **API de análisis de sentimiento y extracción de entidades con NLP y FastAPI**

| Campo              | Detalle             |
| ------------------ | ------------------- |
| 📅 Fechas          | 25-26 de abril 2026 |
| 🏷️ Categoría       | IA/ML & GenAI       |
| ⏱️ Tiempo estimado | 10-12 horas         |
| 📊 Dificultad      | ⭐⭐⭐ Intermedio   |

---

## 🎯 Descripción

SentiScope es una API de procesamiento de lenguaje natural (NLP) que ofrece análisis de sentimiento, extracción de entidades nombradas (NER), detección de idioma y resumen de textos. A diferencia de los proyectos anteriores que usan LLMs, este proyecto usa modelos de NLP especializados — demostrando que no toda la IA requiere modelos gigantes.

---

## 🏗️ Arquitectura

```
┌──────────────────────────┐
│    Cliente (HTTP)         │
└────────────┬─────────────┘
             │
    ┌────────▼────────┐
    │   FastAPI App    │
    │   (Router)       │
    └────────┬────────┘
             │
   ┌─────────┼─────────┐
   │         │         │
┌──▼──┐  ┌──▼──┐  ┌──▼──┐
│Sent.│  │ NER │  │Summ.│
│Anal.│  │     │  │     │
└──┬──┘  └──┬──┘  └──┬──┘
   │         │         │
   ▼         ▼         ▼
  spaCy   Transformers  Sumy
```

---

## ✨ Features

### Análisis de sentimiento

- [ ] Clasificación: positivo, negativo, neutro
- [ ] Score de confianza (0-1)
- [ ] Análisis por oración
- [ ] Soporte multi-idioma (español, inglés)

### Extracción de entidades (NER)

- [ ] Personas, organizaciones, lugares
- [ ] Fechas, cantidades, porcentajes
- [ ] Entidades personalizables
- [ ] Posición en el texto (offset)

### Utilidades adicionales

- [ ] Detección automática de idioma
- [ ] Resumen extractivo de textos
- [ ] Tokenización y estadísticas de texto
- [ ] Análisis batch (múltiples textos)

### API

- [ ] Endpoint de análisis de sentimiento
- [ ] Endpoint de extracción de entidades
- [ ] Endpoint de resumen
- [ ] Endpoint combinado (análisis completo)
- [ ] Análisis batch

---

## 🛠️ Stack técnico

| Tecnología           | Propósito               |
| -------------------- | ----------------------- |
| **FastAPI**          | API REST                |
| **spaCy**            | NLP: NER, tokenización  |
| **TextBlob / VADER** | Análisis de sentimiento |
| **langdetect**       | Detección de idioma     |
| **sumy**             | Resumen extractivo      |
| **Pandas**           | Procesamiento batch     |
| **Docker**           | Containerización        |
| **pytest**           | Testing                 |

---

## 📡 Endpoints de la API

```
POST   /api/v1/sentiment          # Análisis de sentimiento
POST   /api/v1/entities           # Extracción de entidades
POST   /api/v1/summarize          # Resumen de texto
POST   /api/v1/detect-language    # Detección de idioma
POST   /api/v1/analyze            # Análisis completo combinado
POST   /api/v1/batch/sentiment    # Análisis batch
POST   /api/v1/batch/entities     # Entidades batch

GET    /api/v1/models             # Modelos disponibles
GET    /api/v1/health             # Health check
```

---

## 🗓️ Plan del fin de semana

### Sábado

| Hora           | Actividad                                  |
| -------------- | ------------------------------------------ |
| 🌅 9:00-10:00  | Setup: FastAPI, spaCy, modelos NLP         |
| 🌅 10:00-12:00 | Análisis de sentimiento (VADER + TextBlob) |
| 🌞 12:00-13:00 | Extracción de entidades con spaCy          |
| 🌞 14:00-16:00 | Detección de idioma + resumen              |
| 🌆 16:00-18:00 | Endpoint combinado + análisis batch        |

### Domingo

| Hora           | Actividad                               |
| -------------- | --------------------------------------- |
| 🌅 9:00-10:30  | Soporte multi-idioma (español + inglés) |
| 🌅 10:30-12:00 | Optimización y caching de modelos       |
| 🌞 13:00-14:30 | Tests con textos de ejemplo             |
| 🌞 14:30-16:00 | Docker (incluyendo descarga de modelos) |
| 🌆 16:00-17:00 | README con ejemplos y curl commands     |

---

## ✅ Definición de "hecho"

- [ ] Análisis de sentimiento funcional
- [ ] NER con al menos 5 tipos de entidades
- [ ] Resumen extractivo funcional
- [ ] Análisis batch
- [ ] Tests con fixtures de texto
- [ ] Docker funcional (modelos incluidos)
- [ ] README con ejemplos de cada endpoint

---

## 💼 Lo que demuestra al reclutador

| Habilidad    | Evidencia                                 |
| ------------ | ----------------------------------------- |
| NLP          | spaCy, NER, sentimiento sin APIs externas |
| ML práctico  | Modelos especializados vs LLMs            |
| API Design   | Endpoints claros, batch processing        |
| Optimización | Caching de modelos, eficiencia            |
| Versatilidad | IA no solo con LLMs                       |
