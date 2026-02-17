# 🟢 Semana 15 — MicroNode

> **Microservicio profesional con Node.js, Express y TypeScript**

| Campo              | Detalle             |
| ------------------ | ------------------- |
| 📅 Fechas          | 13-14 de junio 2026 |
| 🏷️ Categoría       | DevOps & Cloud      |
| ⏱️ Tiempo estimado | 10-12 horas         |
| 📊 Dificultad      | ⭐⭐⭐ Intermedio   |

---

## 🎯 Descripción

MicroNode es un microservicio construido con Node.js, Express y TypeScript siguiendo todas las buenas prácticas: estructura modular, validación con Zod, manejo de errores centralizado, logging estructurado, tests, y Docker. Demuestra que el dominio trasciende lenguajes y frameworks.

Puede ser un servicio de gestión de URLs cortas (URL shortener) o un servicio de bookmarks — algo concreto y funcional.

---

## ✨ Features

### Core (URL Shortener)

- [ ] Acortar URL → generar código único
- [ ] Redirigir URL acortada a la original
- [ ] Estadísticas de clicks por URL
- [ ] Custom slugs opcionales
- [ ] Expiración configurable

### Arquitectura

- [ ] Estructura modular (routes, controllers, services, repositories)
- [ ] Validación de inputs con Zod
- [ ] Manejo de errores centralizado (middleware)
- [ ] Logging estructurado (Winston/Pino)
- [ ] Variables de entorno tipadas

### Calidad

- [ ] Tests unitarios y de integración (Jest/Vitest)
- [ ] Docker multi-stage
- [ ] ESLint + Prettier configurados
- [ ] Health check endpoint
- [ ] Documentación con Swagger (express-openapi)

---

## 🛠️ Stack técnico

| Tecnología     | Propósito        |
| -------------- | ---------------- |
| **Node.js**    | Runtime          |
| **Express**    | Framework web    |
| **TypeScript** | Tipado estático  |
| **Zod**        | Validación       |
| **PostgreSQL** | Base de datos    |
| **Prisma**     | ORM              |
| **Pino**       | Logging          |
| **Vitest**     | Testing          |
| **Docker**     | Containerización |

---

## 📁 Estructura del proyecto

```
micronode/
├── src/
│   ├── index.ts               # Entry point
│   ├── app.ts                 # Express app setup
│   ├── config/
│   │   └── env.ts             # Variables de entorno tipadas
│   ├── routes/
│   │   └── url.routes.ts
│   ├── controllers/
│   │   └── url.controller.ts
│   ├── services/
│   │   └── url.service.ts
│   ├── repositories/
│   │   └── url.repository.ts
│   ├── middleware/
│   │   ├── errorHandler.ts
│   │   ├── validator.ts
│   │   └── logger.ts
│   ├── schemas/
│   │   └── url.schema.ts      # Zod schemas
│   └── utils/
│       └── shortCode.ts
├── prisma/
│   └── schema.prisma
├── tests/
│   ├── url.service.test.ts
│   └── url.routes.test.ts
├── Dockerfile
├── docker-compose.yml
├── tsconfig.json
├── package.json
└── README.md
```

---

## 🗓️ Plan del fin de semana

### Sábado

| Hora           | Actividad                                  |
| -------------- | ------------------------------------------ |
| 🌅 9:00-10:00  | Setup: TypeScript, Express, Prisma, Docker |
| 🌅 10:00-12:00 | Modelos Prisma + setup de DB               |
| 🌞 12:00-13:00 | Service layer: acortar URL, redirigir      |
| 🌞 14:00-16:00 | Controllers + Routes + Validación Zod      |
| 🌆 16:00-18:00 | Middleware: error handler, logger          |

### Domingo

| Hora           | Actividad                   |
| -------------- | --------------------------- |
| 🌅 9:00-10:30  | Estadísticas de clicks      |
| 🌅 10:30-12:00 | Tests (Vitest)              |
| 🌞 13:00-14:30 | Docker multi-stage          |
| 🌞 14:30-16:00 | Swagger docs + health check |
| 🌆 16:00-17:00 | README y documentación      |

---

## ✅ Definición de "hecho"

- [ ] URL shortener funcional (acortar + redirigir)
- [ ] TypeScript estricto sin `any`
- [ ] Validación con Zod
- [ ] Tests unitarios y de integración
- [ ] Docker funcional
- [ ] Documentación Swagger
- [ ] README profesional

---

## 💼 Lo que demuestra al reclutador

| Habilidad            | Evidencia                       |
| -------------------- | ------------------------------- |
| Node.js / TypeScript | Microservicio profesional       |
| Versatilidad         | Dominio más allá de Python      |
| Arquitectura         | Capas bien separadas            |
| Calidad              | Tests, linting, tipado estricto |
