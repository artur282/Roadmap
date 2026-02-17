# 🌐 Semana 23 — APIMarket

> **Marketplace y Agregador de APIs con Gateway, Billing y Documentación Automática**

| Campo              | Detalle             |
| ------------------ | ------------------- |
| 📅 Fechas          | 8-9 de agosto 2026  |
| 🏷️ Categoría       | Capstone Project    |
| ⏱️ Tiempo estimado | 10-12 horas         |
| 📊 Dificultad      | ⭐⭐⭐⭐⭐ Avanzado |

---

## 🎯 Descripción

APIMarket es una plataforma que permite a desarrolladores publicar sus microservicios (APIs) y a otros consumirlos a través de un gateway unificado. El sistema maneja la generación de API Keys, el control de cuotas (Rate Limiting), la facturación simulada (uso por request) y la documentación unificada.

Este proyecto consolida los conocimientos de GateKeeper (Junio) y AuthGuard (Marzo) en un producto SaaS completo.

---

## ✨ Features

### Para Proveedores de API

- [ ] Registro de nuevos endpoints (target URL, method).
- [ ] Definición de planes de uso (Free, Pro, Enterprise).
- [ ] Dashboard de métricas (requests recibidos, latencia, errores).

### Para Consumidores

- [ ] Explorador de APIs (Marketplace UI).
- [ ] Generación y rotación de API Keys.
- [ ] Dashboard de consumo y costos estimados.
- [ ] Sandbox para probar endpoints en el navegador.

### Core System

- [ ] **Gateway Unificado**: Un solo punto de entrada (`api.market.com/v1/{service_id}/...`).
- [ ] **Billing Engine**: Conteo atómico de requests y cálculo de deuda.
- [ ] **Auto-Docs**: Ingesta de OpenAPI specs para generar docs visuales.

---

## 🛠️ Stack técnico

| Tecnología            | Propósito                                     |
| --------------------- | --------------------------------------------- |
| **FastAPI**           | Core API y Proxy logic                        |
| **Redis**             | Rate Limiting de alto rendimiento y caching   |
| **TimescaleDB / PG**  | Almacenamiento de series de tiempo (métricas) |
| **Stripe (Simulado)** | Lógica de suscripciones y pagos               |
| **React + Tailwind**  | Frontend del Marketplace                      |
| **Docker**            | Despliegue de servicios simulados             |

---

## 🗓️ Plan del fin de semana

### Sábado

| Hora           | Actividad                                                              |
| -------------- | ---------------------------------------------------------------------- |
| 🌅 9:00-10:00  | Diseño de DB Schema (Services, Plans, Subscriptions, Usage).           |
| 🌅 10:00-12:00 | **Gateway Core**: Proxy reverso dinámico con autenticación de API Key. |
| 🌞 12:00-13:00 | **Rate Limiting**: Implementación estricta con Redis por plan.         |
| 🌞 14:00-16:00 | **Usage Tracking**: Middleware que loguea cada request asíncronamente. |
| 🌆 16:00-18:00 | API de gestión (CRUD de servicios y planes).                           |

### Domingo

| Hora           | Actividad                                                             |
| -------------- | --------------------------------------------------------------------- |
| 🌅 9:00-11:00  | **Frontend**: Catálogo de APIs y Dashboard de usuario.                |
| 🌅 11:00-12:30 | **Sandbox**: Componente React para probar llamadas (tipo Swagger UI). |
| 🌞 13:00-14:30 | Simulación de facturación y reportes de uso.                          |
| 🌞 14:30-16:00 | Deploy de 2 servicios "dummy" para poblar el mercado.                 |
| 🌆 16:00-17:00 | Documentación final y capturas.                                       |

---

## ✅ Definición de "hecho"

- [ ] Funciona el proxy: Request a Gateway -> Auth/RateLimit -> Target Service -> Response.
- [ ] El conteo de uso es preciso.
- [ ] UI permite registrar una API y generar una Key para consumirla.
- [ ] Bloqueo efectivo al superar límites del plan.

---

## 💼 Lo que demuestra al reclutador

| Habilidad         | Evidencia                                                            |
| ----------------- | -------------------------------------------------------------------- |
| Arquitectura SaaS | Multi-tenancy, gestión de cuotas, facturación                        |
| High Performance  | Uso eficiente de Redis para validar cada request con latencia mínima |
| API Product       | Entendimiento de la experiencia de desarrollador (DX)                |
| Integración       | Proxy reverso y manejo de tráfico HTTP                               |
