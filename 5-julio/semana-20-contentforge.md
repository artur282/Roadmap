# ✏️ Semana 20 — ContentForge

> **Mini CMS headless con API REST, panel de administración y renderizado Markdown**

| Campo              | Detalle                |
| ------------------ | ---------------------- |
| 📅 Fechas          | 18-19 de julio 2026    |
| 🏷️ Categoría       | Full-Stack Integration |
| ⏱️ Tiempo estimado | 10-12 horas            |
| 📊 Dificultad      | ⭐⭐⭐ Intermedio      |

---

## 🎯 Descripción

ContentForge es un CMS headless minimalista que permite crear, editar y publicar artículos con soporte de Markdown. Tiene un panel de administración en React y una API para consumir el contenido desde cualquier frontend. Demuestra la capacidad de construir herramientas de gestión de contenido completas.

---

## ✨ Features

### Backend (API)

- [ ] CRUD de artículos (título, contenido MD, tags, estado)
- [ ] Estados: borrador, publicado, archivado
- [ ] Categorías y tags
- [ ] Búsqueda por texto y filtrado
- [ ] Autenticación para escritura (API pública para lectura)
- [ ] Renderizado de Markdown a HTML en API

### Panel Admin (React)

- [ ] Editor de Markdown con preview en vivo
- [ ] Lista de artículos con estados
- [ ] Publicar/despublicar con un click
- [ ] Gestión de categorías
- [ ] Dashboard con estadísticas (total artículos, borradores)

### API Pública

- [ ] Listar artículos publicados
- [ ] Obtener artículo por slug
- [ ] Filtrar por categoría/tag
- [ ] Paginación

---

## 🛠️ Stack técnico

| Tecnología      | Propósito               |
| --------------- | ----------------------- |
| **FastAPI**     | Backend API             |
| **React**       | Panel admin             |
| **PostgreSQL**  | Base de datos           |
| **Markdown-it** | Renderizado de Markdown |
| **TailwindCSS** | Estilos                 |
| **Docker**      | Containerización        |

---

## 🗓️ Plan del fin de semana

### Sábado

| Hora           | Actividad                       |
| -------------- | ------------------------------- |
| 🌅 9:00-10:30  | Setup + modelos de datos        |
| 🌅 10:30-12:00 | API CRUD de artículos           |
| 🌞 12:00-13:00 | Renderizado Markdown + slugs    |
| 🌞 14:00-16:00 | Panel admin: lista de artículos |
| 🌆 16:00-18:00 | Editor de Markdown con preview  |

### Domingo

| Hora           | Actividad                 |
| -------------- | ------------------------- |
| 🌅 9:00-10:30  | Categorías, tags, filtros |
| 🌅 10:30-12:00 | API pública + paginación  |
| 🌞 13:00-14:30 | Dashboard de estadísticas |
| 🌞 14:30-16:00 | Tests                     |
| 🌆 16:00-17:00 | README y documentación    |

---

## ✅ Definición de "hecho"

- [ ] CRUD de artículos funcional
- [ ] Editor Markdown con preview
- [ ] API pública para lectura
- [ ] Panel admin funcional
- [ ] Docker Compose
- [ ] README

---

## 💼 Lo que demuestra al reclutador

| Habilidad  | Evidencia                               |
| ---------- | --------------------------------------- |
| CMS        | Gestión de contenido completa           |
| Full-stack | API + Panel admin                       |
| API Design | Pública (lectura) + privada (escritura) |
| Producto   | Herramienta funcional y útil            |
