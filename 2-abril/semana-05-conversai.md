# 💬 Semana 05 — ConversAI

> **Chatbot conversacional con memoria y contexto usando LangChain y FastAPI**

| Campo              | Detalle           |
| ------------------ | ----------------- |
| 📅 Fechas          | 4-5 de abril 2026 |
| 🏷️ Categoría       | IA/ML & GenAI     |
| ⏱️ Tiempo estimado | 10-12 horas       |
| 📊 Dificultad      | ⭐⭐⭐ Intermedio |

---

## 🎯 Descripción

ConversAI es un chatbot conversacional que mantiene contexto a lo largo de una conversación. Usa LangChain para orquestar las llamadas a LLMs, implementa diferentes estrategias de memoria (buffer, summary, window), y expone todo a través de una API REST con FastAPI.

El proyecto demuestra que integrar IA va más allá de llamar a una API — requiere gestión de estado, diseño de prompts, y arquitectura pensada.

---

## 🏗️ Arquitectura

```
┌──────────────────────────┐
│    Cliente (HTTP/WebUI)   │
└────────────┬─────────────┘
             │
    ┌────────▼────────┐
    │   FastAPI App    │
    │  (Chat Router)   │
    └────────┬────────┘
             │
    ┌────────▼────────┐
    │   LangChain      │
    │   Chain/Agent    │
    ├──────────────────┤
    │ • Prompt Template│
    │ • Memory (Buffer)│
    │ • Output Parser  │
    └────────┬────────┘
             │
    ┌────────▼────────┐
    │   LLM Provider   │
    │ (OpenAI / Local) │
    └──────────────────┘
```

---

## ✨ Features

### Conversación

- [ ] Chat con contexto persistente por sesión
- [ ] Múltiples sesiones de conversación
- [ ] Historial de mensajes consultable
- [ ] Streaming de respuestas (SSE)
- [ ] Soporte para system prompts personalizados

### Memoria

- [ ] Buffer Memory (últimos N mensajes)
- [ ] Summary Memory (resumen de conversación)
- [ ] Window Memory (ventana deslizante)
- [ ] Selección de estrategia por sesión

### API

- [ ] Crear nueva sesión de chat
- [ ] Enviar mensaje y recibir respuesta
- [ ] Obtener historial de sesión
- [ ] Listar sesiones activas
- [ ] Eliminar sesión

### Prompts

- [ ] Templates de prompt configurables
- [ ] System prompts por "personalidad"
- [ ] Prompt engineering documentado

---

## 🛠️ Stack técnico

| Tecnología        | Propósito                |
| ----------------- | ------------------------ |
| **LangChain**     | Orquestación de LLMs     |
| **FastAPI**       | API REST                 |
| **OpenAI API**    | Proveedor de LLM         |
| **SQLite**        | Persistencia de sesiones |
| **Pydantic**      | Validación               |
| **SSE-Starlette** | Streaming                |
| **Docker**        | Containerización         |
| **pytest**        | Testing                  |

---

## 📡 Endpoints de la API

```
POST   /api/v1/sessions              # Crear sesión de chat
GET    /api/v1/sessions               # Listar sesiones
GET    /api/v1/sessions/{id}          # Obtener sesión con historial
DELETE /api/v1/sessions/{id}          # Eliminar sesión

POST   /api/v1/sessions/{id}/chat     # Enviar mensaje
GET    /api/v1/sessions/{id}/stream   # Chat con streaming (SSE)
GET    /api/v1/sessions/{id}/history  # Historial de mensajes

GET    /api/v1/prompts                # Listar prompts disponibles
```

---

## 🗓️ Plan del fin de semana

### Sábado

| Hora           | Actividad                                 |
| -------------- | ----------------------------------------- |
| 🌅 9:00-10:00  | Setup: FastAPI, LangChain, OpenAI, Docker |
| 🌅 10:00-12:00 | Chain básico: prompt → LLM → response     |
| 🌞 12:00-13:00 | Integración de memoria (Buffer Memory)    |
| 🌞 14:00-16:00 | API de sesiones + persistencia SQLite     |
| 🌆 16:00-18:00 | Endpoint de chat + historial              |

### Domingo

| Hora           | Actividad                          |
| -------------- | ---------------------------------- |
| 🌅 9:00-10:30  | Streaming con SSE                  |
| 🌅 10:30-12:00 | Estrategias de memoria adicionales |
| 🌞 13:00-14:30 | System prompts y personalidades    |
| 🌞 14:30-16:00 | Tests (mocking de API de OpenAI)   |
| 🌆 16:00-17:00 | README y documentación de prompts  |

---

## ✅ Definición de "hecho"

- [ ] Chat funcional con contexto persistente
- [ ] Al menos 2 estrategias de memoria
- [ ] Streaming de respuestas
- [ ] Sesiones independientes
- [ ] Tests con mock de LLM
- [ ] Docker Compose funcional
- [ ] README con ejemplos de uso

---

## 💼 Lo que demuestra al reclutador

| Habilidad    | Evidencia                          |
| ------------ | ---------------------------------- |
| IA/GenAI     | LangChain, prompts, memoria        |
| Arquitectura | Separación LLM / API / storage     |
| Streaming    | SSE para respuestas en tiempo real |
| API Design   | Endpoints bien diseñados           |
| Testing      | Mocking de servicios externos      |
