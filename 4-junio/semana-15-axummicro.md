# 🟢 Semana 15 — AxumMicro

> **Microservicio de alto rendimiento con Rust, Axum, SQLx y Distroless**

| Campo              | Detalle             |
| ------------------ | ------------------- |
| 📅 Fechas          | 13-14 de junio 2026 |
| 🏷️ Categoría       | DevOps & Cloud      |
| ⏱️ Tiempo estimado | 10-12 horas         |
| 📊 Dificultad      | ⭐⭐⭐ Intermedio   |

---

## 🎯 Descripción

AxumMicro es un microservicio ultraligero construido con Rust y Axum, enfocado en el alto rendimiento, eficiencia de memoria y modularidad. Utiliza SQLx para consultas directas y seguras a la base de datos sin la sobrecarga de un ORM, y Serde para una serialización y deserialización de datos ultrarrápida.

El servicio se despliega utilizando imágenes Docker multi-stage basadas en Distroless, logrando binarios finales extremadamente ligeros (apenas 20-30MB), lo cual es ideal para entornos de producción de rápido despliegue y máxima seguridad. Puede implementarse como un servicio de gestión de URLs cortas o una API de gestión de tareas.

---

## ✨ Features

### Core (URL Shortener)

- [ ] Acortar URL → generar código único alfanumérico
- [ ] Redirigir URL acortada a la original
- [ ] Estadísticas de clicks y telemetría ligera
- [ ] Configuración de expiración de enlaces

### Arquitectura y Stack

- [ ] **Axum**: API Router asíncrono y robusto, aprovechando el ecosistema de Tokio
- [ ] **SQLx**: Control total sobre SQL con verificación de queries en tiempo de compilación
- [ ] **Serde**: Manejo eficiente y declarativo de estructuras de datos (JSON)
- [ ] Manejo de errores implementando `IntoResponse` para respuestas tipadas y consistentes

### Calidad y Despliegue

- [ ] Tests integrados con la base de datos de pruebas
- [ ] **Docker + Distroless**: Imagen base mínima sin shell ni utilidades del sistema
- [ ] Binario final estáticamente enlazado (peso de 20-30MB)
- [ ] Integración continua y formateo de código (Clippy / Rustfmt)

---

## 🛠️ Stack técnico

| Tecnología     | Propósito                                |
| -------------- | ---------------------------------------- |
| **Rust**       | Lenguaje base                            |
| **Axum**       | Web Framework asíncrono y modular        |
| **SQLx**       | Database Driver (PostgreSQL) puro SQL    |
| **Serde**      | Serialización / Deserialización de datos |
| **Tokio**      | Runtime asíncrono                        |
| **Distroless** | Base de imagen Docker ligera y segura    |
| **Docker**     | Containerización multi-stage             |

---

## 📁 Estructura del proyecto

```text
axum_micro/
├── src/
│   ├── main.rs                # Entry point y configuración del server
│   ├── routes.rs              # Definición de las rutas web
│   ├── handlers.rs            # Lógica de controladores de Axum
│   ├── models.rs              # Estructuras de datos (Serde)
│   ├── db.rs                  # Módulo de conexión y queries (SQLx)
│   └── error.rs               # Manejo de errores centralizado
├── migrations/                # Archivos de migración SQL
├── tests/
│   └── integration_test.rs    # Pruebas integradas
├── Dockerfile                 # Multi-stage build con Distroless
├── docker-compose.yml         # Entorno local (con PostgreSQL)
├── Cargo.toml                 # Dependencias
└── README.md
```

---

## 🗓️ Plan del fin de semana

### Sábado

| Hora           | Actividad                                  |
| -------------- | ------------------------------------------ |
| 🌅 9:00-10:00  | Setup de Cargo, SQLx-cli y Docker          |
| 🌅 10:00-12:00 | Diseño de base de datos y migraciones (SQLx) |
| 🌞 12:00-13:00 | Estructuras en Rust y Serialización con Serde |
| 🌞 14:00-16:00 | Controladores (handlers) y Core logic      |
| 🌆 16:00-18:00 | Configuración de rutas web con Axum        |

### Domingo

| Hora           | Actividad                   |
| -------------- | --------------------------- |
| 🌅 9:00-10:30  | Manejo de Errores y `IntoResponse` |
| 🌅 10:30-12:00 | Tests de los endpoints      |
| 🌞 13:00-14:30 | Dockerfile (Multi-stage + Distroless) |
| 🌞 14:30-16:00 | Ajustes finales (Clippy, Rustfmt) |
| 🌆 16:00-17:00 | README y documentación      |

---

## ✅ Definición de "hecho"

- [ ] API funcional con endpoints completos
- [ ] Queries verificadas estáticamente durante la compilación
- [ ] Deserialización sin fallos mediante Serde
- [ ] Manejo de errores custom implementando `IntoResponse`
- [ ] Imagen de Docker final basada en `gcr.io/distroless/cc-debian12`
- [ ] Peso del contenedor final <= 30MB
- [ ] README documentado y profesional

---

## 💼 Lo que demuestra al reclutador

| Habilidad            | Evidencia                       |
| -------------------- | ------------------------------- |
| Rendimiento & Memoria| Implementación segura con Rust  |
| Control de DB        | Manipulación directa de SQL     |
| Optimización         | Imágenes Docker minimalistas    |
| Calidad              | Robustez basada en el ecosistema Rust |
