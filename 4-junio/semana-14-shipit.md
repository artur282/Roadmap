# 🚢 Semana 14 — ShipIt

> **Pipeline CI/CD completo con GitHub Actions, Docker y deploy automático**

| Campo              | Detalle           |
| ------------------ | ----------------- |
| 📅 Fechas          | 6-7 de junio 2026 |
| 🏷️ Categoría       | DevOps & Cloud    |
| ⏱️ Tiempo estimado | 10-12 horas       |
| 📊 Dificultad      | ⭐⭐⭐ Intermedio |

---

## 🎯 Descripción

ShipIt es un proyecto enfocado en construir un pipeline CI/CD profesional desde cero. Toma una aplicación FastAPI existente (o nueva), la containeriza con Docker multi-stage, configura GitHub Actions para linting, testing, build y deploy automático. El resultado: cada push a `main` despliega automáticamente.

---

## ✨ Features

### Docker

- [ ] Dockerfile multi-stage (build + production)
- [ ] Imagen optimizada (slim, layers cacheadas)
- [ ] Docker Compose para desarrollo local
- [ ] Health checks en container
- [ ] .dockerignore optimizado

### GitHub Actions

- [ ] Pipeline de CI: lint (Ruff) → test (pytest) → build (Docker)
- [ ] Pipeline de CD: deploy automático en push a main
- [ ] Caché de dependencias (pip, Docker layers)
- [ ] Matrix testing (Python 3.11, 3.12)
- [ ] Badges de estado en README

### Deploy

- [ ] Deploy a un servicio cloud (Railway, Render o Fly.io)
- [ ] Variables de entorno seguras (GitHub Secrets)
- [ ] Health check post-deploy
- [ ] Rollback manual documentado

### Calidad

- [ ] Pre-commit hooks (Ruff + mypy)
- [ ] Coverage report en CI
- [ ] Semantic versioning con tags
- [ ] Changelog automático

---

## 🛠️ Stack técnico

| Tecnología         | Propósito        |
| ------------------ | ---------------- |
| **GitHub Actions** | CI/CD            |
| **Docker**         | Containerización |
| **FastAPI**        | App de ejemplo   |
| **pytest**         | Testing          |
| **Ruff**           | Linting          |
| **mypy**           | Type checking    |
| **Railway/Render** | Deploy cloud     |

---

## 🗓️ Plan del fin de semana

### Sábado

| Hora           | Actividad                                |
| -------------- | ---------------------------------------- |
| 🌅 9:00-10:30  | App FastAPI base (o reutilizar TaskFlow) |
| 🌅 10:30-12:00 | Dockerfile multi-stage optimizado        |
| 🌞 12:00-13:00 | Docker Compose para dev + DB             |
| 🌞 14:00-16:00 | GitHub Actions: pipeline CI              |
| 🌆 16:00-18:00 | GitHub Actions: pipeline CD + deploy     |

### Domingo

| Hora           | Actividad                            |
| -------------- | ------------------------------------ |
| 🌅 9:00-10:30  | Deploy a Railway/Render              |
| 🌅 10:30-12:00 | Pre-commit hooks + quality gates     |
| 🌞 13:00-14:30 | Coverage report + badges             |
| 🌞 14:30-16:00 | Tests del pipeline completo          |
| 🌆 16:00-17:00 | README con badges y docs de pipeline |

---

## ✅ Definición de "hecho"

- [ ] Pipeline CI funcional (lint → test → build)
- [ ] Pipeline CD con deploy automático
- [ ] Docker multi-stage optimizado
- [ ] App desplegada y accesible públicamente
- [ ] Badges de CI/CD en README
- [ ] Pre-commit hooks configurados
- [ ] README con documentación del pipeline

---

## 💼 Lo que demuestra al reclutador

| Habilidad        | Evidencia                           |
| ---------------- | ----------------------------------- |
| CI/CD            | GitHub Actions, pipelines completos |
| Docker           | Multi-stage, optimización           |
| DevOps           | Deploy automático, quality gates    |
| Buenas prácticas | Pre-commit, coverage, badges        |
