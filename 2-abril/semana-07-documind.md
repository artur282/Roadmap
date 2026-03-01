# 📚 Semana 07 — DocuMind

> **Pipeline RAG para Q&A sobre documentos con embeddings y búsqueda semántica**

| Campo              | Detalle                  |
| ------------------ | ------------------------ |
| 📅 Fechas          | 18-19 de abril 2026      |
| 🏷️ Categoría       | IA/ML & GenAI            |
| ⏱️ Tiempo estimado | 10-12 horas              |
| 📊 Dificultad      | ⭐⭐⭐⭐ Intermedio-alto |

---

## 🎯 Descripción

DocuMind es una aplicación de Retrieval Augmented Generation (RAG) que permite hacer preguntas en lenguaje natural sobre documentos (PDFs, Markdown, texto). Ingesta documentos, los divide en chunks, genera embeddings, los almacena en una vector store, y usa búsqueda semántica para encontrar el contexto relevante antes de generar respuestas con un LLM.

Este proyecto demuestra una de las aplicaciones más demandadas de GenAI en la industria.

---

## 🏗️ Arquitectura

```
                    ┌─────────────┐
                    │  Documentos  │
                    │ (PDF/MD/TXT) │
                    └──────┬──────┘
                           │
              ┌────────────▼────────────┐
              │     Document Loader     │
              │  (PyPDF, Markdown, etc.)│
              └────────────┬────────────┘
                           │
              ┌────────────▼────────────┐
              │     Text Splitter       │
              │  (Recursive, Semantic)  │
              └────────────┬────────────┘
                           │
              ┌────────────▼────────────┐
              │   Embedding Model       │
              │  (OpenAI / Sentence     │
              │   Transformers)         │
              └────────────┬────────────┘
                           │
              ┌────────────▼────────────┐
              │    Vector Store         │
              │  (Pinecone / Chroma /   │
              │   Weaviate / pgvector)  │
              └────────────┬────────────┘
                           │
        ┌──────────────────┼──────────────────┐
        │                  │                  │
   ┌────▼─────┐    ┌──────▼──────┐    ┌──────▼──────┐
   │ Retriever│    │  LLM Chain  │    │  FastAPI    │
   │ (Top-K)  │───▶│  (Prompt +  │◀───│  (API)     │
   └──────────┘    │   Context)  │    └─────────────┘
                   └─────────────┘
```

---

## ✨ Features

### Ingestión de documentos

- [ ] Carga de PDFs, Markdown y archivos de texto
- [ ] Chunking inteligente (recursive, por tamaño, semántico)
- [ ] Metadatos por chunk (página, fuente, posición)
- [ ] Procesamiento batch de múltiples documentos

### Búsqueda y retrieval

- [ ] Generación de embeddings
- [ ] Almacenamiento en vector store (Pinecone, Weaviate, Chroma o pgvector)
- [ ] Búsqueda semántica (Top-K)
- [ ] Filtrado por metadatos
- [ ] Score de relevancia

### Generación de respuestas

- [ ] RAG chain con LangChain
- [ ] Citación de fuentes en la respuesta
- [ ] Prompt template optimizado para Q&A
- [ ] Manejo de preguntas sin respuesta

### API

- [ ] Upload de documentos
- [ ] Q&A sobre documentos cargados
- [ ] Listar documentos y sus chunks
- [ ] Búsqueda semántica directa

---

## 🛠️ Stack técnico

| Tecnología          | Propósito        |
| ------------------- | ---------------- |
| **LangChain**       | Orquestación RAG |
| **Pinecone/Chroma** | Vector store     |
| **OpenAI**          | Embeddings + LLM |
| **FastAPI**         | API REST         |
| **PyPDF2**          | Lectura de PDFs  |
| **Docker**          | Containerización |
| **pytest**          | Testing          |

---

## 📡 Endpoints de la API

```
POST   /api/v1/documents/upload       # Subir documento
GET    /api/v1/documents               # Listar documentos
GET    /api/v1/documents/{id}/chunks   # Ver chunks de un documento
DELETE /api/v1/documents/{id}          # Eliminar documento

POST   /api/v1/query                   # Hacer pregunta sobre documentos
POST   /api/v1/search                  # Búsqueda semántica directa
```

---

## 🗓️ Plan del fin de semana

### Sábado

| Hora           | Actividad                                |
| -------------- | ---------------------------------------- |
| 🌅 9:00-10:00  | Setup: LangChain, Vector DB, FastAPI     |
| 🌅 10:00-12:00 | Document loaders + text splitters        |
| 🌞 12:00-13:00 | Embedding generation + Vector DB storage |
| 🌞 14:00-16:00 | Retriever + RAG chain                    |
| 🌆 16:00-18:00 | API de upload y Q&A                      |

### Domingo

| Hora           | Actividad                                 |
| -------------- | ----------------------------------------- |
| 🌅 9:00-10:30  | Citación de fuentes + score de relevancia |
| 🌅 10:30-12:00 | Metadatos y filtrado                      |
| 🌞 13:00-14:30 | Tests con documentos de ejemplo           |
| 🌞 14:30-16:00 | Docker + ajuste de prompts                |
| 🌆 16:00-17:00 | README con ejemplos y demo                |

---

## ✅ Definición de "hecho"

- [ ] Pipeline RAG funcional de extremo a extremo
- [ ] Soporte para PDF y Markdown
- [ ] Respuestas con citación de fuentes
- [ ] API de upload y Q&A
- [ ] Tests con documentos fixture
- [ ] Docker Compose funcional
- [ ] README con ejemplos de preguntas y respuestas

---

## 💼 Lo que demuestra al reclutador

| Habilidad          | Evidencia                                             |
| ------------------ | ----------------------------------------------------- |
| RAG                | Pipeline completo: ingestión → retrieval → generación |
| Embeddings         | Generación y búsqueda semántica                       |
| GenAI              | Integración de LLMs con contexto                      |
| Arquitectura       | Separación de concerns en pipeline                    |
| Demanda industrial | RAG es una de las skills más buscadas                 |
