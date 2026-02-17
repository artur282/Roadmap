# 🔧 Semana 06 — MCPForge

> **Servidor MCP personalizado que expone herramientas como servicio para IA**

| Campo              | Detalle                  |
| ------------------ | ------------------------ |
| 📅 Fechas          | 11-12 de abril 2026      |
| 🏷️ Categoría       | IA/ML & GenAI            |
| ⏱️ Tiempo estimado | 10-12 horas              |
| 📊 Dificultad      | ⭐⭐⭐⭐ Intermedio-alto |

---

## 🎯 Descripción

MCPForge es un servidor Model Context Protocol (MCP) que expone un conjunto de herramientas útiles para asistentes de IA. El proyecto implementa el protocolo MCP desde cero (usando el SDK oficial), creando tools, resources y prompts que cualquier cliente MCP compatible puede consumir.

Este proyecto demuestra comprensión profunda de cómo funciona la infraestructura de IA moderna — no solo usarla, sino construirla.

---

## 🏗️ Arquitectura

```
┌──────────────────────────────────┐
│     Cliente MCP (Claude, etc.)    │
└───────────────┬──────────────────┘
                │ (stdio / SSE)
       ┌────────▼────────┐
       │   MCP Server     │
       │   (Python SDK)   │
       ├──────────────────┤
       │   Tools:         │
       │   ├─ db_query     │
       │   ├─ file_search  │
       │   ├─ api_call     │
       │   └─ text_process │
       ├──────────────────┤
       │   Resources:     │
       │   ├─ config      │
       │   └─ docs         │
       ├──────────────────┤
       │   Prompts:       │
       │   ├─ analyze     │
       │   └─ summarize   │
       └──────────────────┘
```

---

## ✨ Features

### Tools (Herramientas)

- [ ] `query_database` — Ejecutar consultas SQL de solo lectura
- [ ] `search_files` — Buscar archivos por nombre o contenido
- [ ] `call_api` — Hacer llamadas HTTP a APIs externas
- [ ] `process_text` — Transformaciones de texto (resumen, traducción, formato)
- [ ] `generate_report` — Generar reportes en Markdown

### Resources (Recursos)

- [ ] Exposición de archivos de configuración
- [ ] Documentación accesible como recurso
- [ ] Schema de base de datos como recurso

### Prompts

- [ ] Template de análisis de código
- [ ] Template de resumen de documentos
- [ ] Templates personalizables

### Infraestructura

- [ ] Transporte stdio y SSE
- [ ] Logging estructurado
- [ ] Manejo de errores del protocolo
- [ ] Configuración por archivo
- [ ] Docker para distribución

---

## 🛠️ Stack técnico

| Tecnología         | Propósito                    |
| ------------------ | ---------------------------- |
| **MCP Python SDK** | Implementación del protocolo |
| **Python 3.11+**   | Lenguaje base                |
| **SQLite**         | Base de datos demo           |
| **httpx**          | Llamadas HTTP async          |
| **Docker**         | Containerización             |
| **pytest**         | Testing                      |
| **Pydantic**       | Validación de inputs         |

---

## 📁 Estructura del proyecto

```
mcpforge/
├── server/
│   ├── __init__.py
│   ├── main.py               # Entry point del servidor MCP
│   ├── tools/
│   │   ├── database.py       # query_database tool
│   │   ├── files.py          # search_files tool
│   │   ├── api.py            # call_api tool
│   │   ├── text.py           # process_text tool
│   │   └── reports.py        # generate_report tool
│   ├── resources/
│   │   ├── config.py         # Recursos de configuración
│   │   └── docs.py           # Recursos de documentación
│   ├── prompts/
│   │   └── templates.py      # Templates de prompts
│   └── utils/
│       ├── logger.py
│       └── validators.py
├── tests/
│   ├── test_tools.py
│   ├── test_resources.py
│   └── test_server.py
├── config/
│   └── server.toml            # Configuración
├── docker-compose.yml
├── Dockerfile
├── pyproject.toml
└── README.md
```

---

## 🗓️ Plan del fin de semana

### Sábado

| Hora           | Actividad                                  |
| -------------- | ------------------------------------------ |
| 🌅 9:00-10:30  | Estudiar MCP SDK, setup del proyecto       |
| 🌅 10:30-12:00 | Servidor MCP básico con una tool funcional |
| 🌞 12:00-13:00 | Tool: query_database con SQLite            |
| 🌞 14:00-16:00 | Tools: search_files, call_api              |
| 🌆 16:00-18:00 | Tools: process_text, generate_report       |

### Domingo

| Hora           | Actividad                           |
| -------------- | ----------------------------------- |
| 🌅 9:00-10:30  | Resources: config y docs            |
| 🌅 10:30-12:00 | Prompts: templates                  |
| 🌞 13:00-14:30 | Transporte SSE + testing            |
| 🌞 14:30-16:00 | Docker + configuración              |
| 🌆 16:00-17:00 | README y documentación de cada tool |

---

## ✅ Definición de "hecho"

- [ ] Servidor MCP funcional con al menos 4 tools
- [ ] Al menos 2 resources expuestos
- [ ] Al menos 2 prompt templates
- [ ] Funciona con cliente MCP real
- [ ] Tests de cada herramienta
- [ ] Docker funcional
- [ ] README con instrucciones de integración

---

## 💼 Lo que demuestra al reclutador

| Habilidad       | Evidencia                              |
| --------------- | -------------------------------------- |
| MCP / IA infra  | Implementación del protocolo desde SDK |
| Arquitectura    | Diseño modular de herramientas         |
| Python avanzado | Async, protocolos, SDK                 |
| Innovación      | Tecnología de vanguardia               |
| Documentación   | Cada tool documentada                  |
