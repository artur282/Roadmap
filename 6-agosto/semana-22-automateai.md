# 🤖 Semana 22 — AutomateAI

> **Plataforma de automatización de flujos de trabajo impulsada por IA (Capstone Project 1)**

| Campo              | Detalle             |
| ------------------ | ------------------- |
| 📅 Fechas          | 1-2 de agosto 2026  |
| 🏷️ Categoría       | Capstone Project    |
| ⏱️ Tiempo estimado | 12-14 horas         |
| 📊 Dificultad      | ⭐⭐⭐⭐⭐ Avanzado |

---

## 🎯 Descripción

AutomateAI es el primer proyecto Capstone del portafolio. Es una plataforma ambiciosa que integra automatización de flujos de trabajo (similar a n8n/Zapier) pero potenciada nativamente por Inteligencia Artificial. Permite a los usuarios describir una tarea en lenguaje natural y la plataforma genera y ejecuta el flujo de automatización correspondiente conectando APIs, bases de datos y procesamiento de lógica.

Combina: Backend robusto (FastAPI), IA (LangChain/OpenAI), Automatización (Celery/Workers) y una interfaz moderna (React).

---

## 🏗️ Arquitectura

```
┌─────────────────────────────────────────────────────────────┐
│                       Frontend (React)                       │
│  (Chat Interface + Visual Workflow Builder + Dashboard)     │
└─────────────────────────────┬───────────────────────────────┘
                              │ REST / WebSocket
                              ▼
┌─────────────────────────────────────────────────────────────┐
│                      Backend (FastAPI)                       │
│  ┌────────────┐   ┌────────────┐   ┌─────────────────────┐  │
│  │  API Gateway │   │ Auth Module│   │ Workflow Orkestrator│  │
│  └────────────┘   └────────────┘   └─────────────────────┘  │
└─────────────┬───────────────────────────────┬───────────────┘
              │                               │
    ┌─────────▼─────────┐           ┌─────────▼─────────┐
    │  AI Engine (RAG)  │           │   Execution Engine │
    │ (LangChain + LLM) │           │  (Celery Workers)  │
    └───────────────────┘           └─────────┬─────────┘
                                              │
                                    ┌─────────▼─────────┐
                                    │ Integrations Hub  │
                                    │ (Gmail, Slack, DB)│
                                    └───────────────────┘
```

---

## ✨ Features

### IA Core

- [ ] **Generador de Workflows**: Input de texto ("Guarda los emails de facturas en Dropbox") -> JSON Workflow.
- [ ] **Agente Inteligente**: Capacidad de decisión condicional dentro del flujo basada en contenido.
- [ ] **Data Mapping AI**: Mapeo automático de campos entre servicios distintos.

### Motor de Ejecución

- [ ] Ejecución asíncrona de tareas en cadena.
- [ ] Manejo de estado y paso de datos entre nodos.
- [ ] Logs de ejecución en tiempo real.
- [ ] Retry policies inteligentes.

### Integraciones (Nodos)

- [ ] **Trigger**: Webhook, Cron, Email recibido.
- [ ] **Action**: HTTP Request, Email Send, Slack Message.
- [ ] **Logic**: If/Else (AI based), Loop.
- [ ] **Data**: Database Insert/Query.

### UI/UX

- [ ] Editor visual de nodos (React Flow).
- [ ] Chat para generación asistida.
- [ ] Historial de ejecuciones.

---

## 🛠️ Stack técnico

| Tecnología             | Propósito                             |
| ---------------------- | ------------------------------------- |
| **FastAPI**            | Backend API                           |
| **LangChain**          | Lógica de IA y generación de flujos   |
| **Vector DBs**         | Pinecone, Chroma, Weaviate o pgvector |
| **Celery**             | Orquestación de tareas distribuidas   |
| **Redis**              | Broker de mensajería y caché          |
| **PostgreSQL**         | Persistencia de datos y definiciones  |
| **React + React Flow** | Frontend interactivo                  |
| **Docker Compose**     | Infraestructura completa              |

---

## 🗓️ Plan del fin de semana

### Sábado

| Hora           | Actividad                                                                        |
| -------------- | -------------------------------------------------------------------------------- |
| 🌅 9:00-10:00  | **Arquitectura**: Definir esquema JSON del workflow y modelos de datos.          |
| 🌅 10:00-12:00 | **AI Engine**: Prompt engineering para traducir texto a JSON de workflow válido. |
| 🌞 12:00-13:00 | **Backend Core**: API para guardar y recuperar workflows.                        |
| 🌞 14:00-16:00 | **Execution Engine**: Celery workers que interpretan y ejecutan el JSON.         |
| 🌆 16:00-18:00 | **Integraciones**: Crear nodos básicos (Webhook, HTTP, Log).                     |

### Domingo

| Hora           | Actividad                                                                    |
| -------------- | ---------------------------------------------------------------------------- |
| 🌅 9:00-11:00  | **Frontend**: Integrar React Flow para visualización (solo lectura inicial). |
| 🌅 11:00-12:30 | **Frontend**: Chat interface para interactuar con el AI Engine.              |
| 🌞 13:00-14:30 | **Conexión Total**: Frontend -> AI -> Backend save -> Execution.             |
| 🌞 14:30-16:00 | **Polish**: Logs en tiempo real y manejo de errores.                         |
| 🌆 16:00-17:00 | **Demo**: Grabar un video corto de uso (GIF para README).                    |

---

## ✅ Definición de "hecho"

- [ ] Un usuario puede escribir un prompt y se genera un flujo gráfico.
- [ ] El flujo se puede ejecutar manualmente.
- [ ] Al menos 3 tipos de integraciones funcionan realmente (ej: Webhook -> IA Analyze -> Email).
- [ ] Interfaz visual limpia.
- [ ] Código modular y extensible.

---

## 💼 Lo que demuestra al reclutador

| Habilidad     | Evidencia                                                    |
| ------------- | ------------------------------------------------------------ |
| System Design | Arquitectura compleja de microservicios e IA                 |
| GenAI Applied | Uso de LLMs para control lógico, no solo generación de texto |
| Full-Stack    | React complejo (grafos) + Backend asíncrono robusto          |
| Innovación    | Creación de una herramienta "No-Code" impulsada por IA       |
