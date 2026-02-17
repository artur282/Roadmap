# 🛡️ Semana 16 — GateKeeper

> **API Gateway con rate limiting, caché, autenticación y proxy reverso**

| Campo              | Detalle                  |
| ------------------ | ------------------------ |
| 📅 Fechas          | 20-21 de junio 2026      |
| 🏷️ Categoría       | DevOps & Cloud           |
| ⏱️ Tiempo estimado | 10-12 horas              |
| 📊 Dificultad      | ⭐⭐⭐⭐ Intermedio-alto |

---

## 🎯 Descripción

GateKeeper es un API Gateway construido desde cero que actúa como punto de entrada único para múltiples microservicios. Implementa rate limiting, caché de respuestas, autenticación JWT, logging centralizado y proxy reverso. Protege las APIs backend y centraliza concerns transversales.

---

## ✨ Features

### Rate Limiting

- [ ] Limitar requests por IP (ej: 100/minuto)
- [ ] Limitar por API key o usuario
- [ ] Sliding window algorithm
- [ ] Headers de rate limit (X-RateLimit-Limit, X-RateLimit-Remaining)
- [ ] Storage en Redis

### Caché

- [ ] Caché de respuestas GET configurable
- [ ] TTL configurable por ruta
- [ ] Invalidación de caché
- [ ] Cache-Control headers

### Autenticación

- [ ] Validación de JWT en gateway
- [ ] API Key authentication
- [ ] Forwarding de user info a backend
- [ ] Rutas públicas vs protegidas

### Proxy Reverso

- [ ] Routing a múltiples backends
- [ ] Configuración por YAML
- [ ] Health check de backends
- [ ] Request/Response logging

---

## 🛠️ Stack técnico

| Tecnología         | Propósito                       |
| ------------------ | ------------------------------- |
| **FastAPI**        | Framework del gateway           |
| **Redis**          | Rate limiting + caché           |
| **PyJWT**          | Validación de tokens            |
| **httpx**          | Proxy HTTP async                |
| **Docker Compose** | Gateway + Redis + backends demo |
| **pytest**         | Testing                         |

---

## 🗓️ Plan del fin de semana

### Sábado

| Hora           | Actividad                                     |
| -------------- | --------------------------------------------- |
| 🌅 9:00-10:30  | Setup: FastAPI gateway + Redis + backend demo |
| 🌅 10:30-12:00 | Proxy reverso básico (routing a backends)     |
| 🌞 12:00-13:00 | Rate limiting con Redis (sliding window)      |
| 🌞 14:00-16:00 | Caché de respuestas                           |
| 🌆 16:00-18:00 | Autenticación JWT + API keys                  |

### Domingo

| Hora           | Actividad                         |
| -------------- | --------------------------------- |
| 🌅 9:00-10:30  | Configuración por YAML + rutas    |
| 🌅 10:30-12:00 | Health checks de backends         |
| 🌞 13:00-14:30 | Logging centralizado              |
| 🌞 14:30-16:00 | Tests                             |
| 🌆 16:00-17:00 | README y diagrama de arquitectura |

---

## ✅ Definición de "hecho"

- [ ] Rate limiting funcional con Redis
- [ ] Caché de respuestas configurable
- [ ] Autenticación JWT
- [ ] Proxy a al menos 2 backends demo
- [ ] Docker Compose con todos los servicios
- [ ] Tests
- [ ] README con diagrama de arquitectura

---

## 💼 Lo que demuestra al reclutador

| Habilidad       | Evidencia                    |
| --------------- | ---------------------------- |
| Arquitectura    | API Gateway pattern          |
| Seguridad       | Rate limiting, JWT, API keys |
| Performance     | Caché, Redis                 |
| Infraestructura | Multi-servicio, proxy        |
