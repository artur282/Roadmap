# 🦀 Semana 04 — RustCLI

> **Herramienta CLI de alto rendimiento para desarrolladores con Rust, Clap y Ratatui**

| Campo              | Detalle              |
| ------------------ | -------------------- |
| 📅 Fechas          | 28-29 de marzo 2026  |
| 🏷️ Categoría       | Backend Foundations  |
| ⏱️ Tiempo estimado | 10-12 horas          |
| 📊 Dificultad      | ⭐⭐⭐ Intermedio   |

---

## 🎯 Descripción

RustCLI es una herramienta de línea de comandos de alto rendimiento diseñada para aumentar la productividad de desarrolladores. Incluye utilidades como: scaffold de proyectos, gestión de snippets de código, análisis de repositorios Git y un dashboard interactivo en terminal. Todo construido en **Rust** para máxima velocidad y eficiencia de memoria.

Este proyecto demuestra dominio de Rust como lenguaje de sistemas, su modelo de ownership/borrowing, y la capacidad de crear herramientas profesionales con su ecosistema de crates.

---

## ✨ Features

### Scaffold de proyectos

- [ ] `rustcli init <template>` — Crear proyecto desde template
- [ ] Templates: rust-cli, rust-api, python-fastapi, node-express
- [ ] Generación de Dockerfile, docker-compose, Makefile
- [ ] Configuración automática del proyecto (Cargo.toml / pyproject.toml)
- [ ] Inicialización de Git + .gitignore

### Gestión de snippets

- [ ] `rustcli snippet add <name>` — Guardar snippet de código
- [ ] `rustcli snippet list` — Listar snippets con búsqueda fuzzy
- [ ] `rustcli snippet get <name>` — Copiar snippet al clipboard
- [ ] `rustcli snippet export` — Exportar todos los snippets a JSON
- [ ] Almacenamiento local con SQLite (rusqlite)

### Utilidades Git

- [ ] `rustcli git stats` — Estadísticas del repo (commits, contribuidores)
- [ ] `rustcli git changelog` — Generar changelog desde commits convencionales
- [ ] `rustcli git clean-branches` — Limpiar ramas ya mergeadas

### Dashboard interactivo (TUI)

- [ ] `rustcli dash` — Dashboard interactivo en terminal con Ratatui
- [ ] Visualización de estadísticas del proyecto actual
- [ ] Lista de tareas pendientes con navegación por teclado
- [ ] Timer pomodoro integrado con barra de progreso

---

## 🛠️ Stack técnico

| Tecnología     | Propósito                                 |
| -------------- | ----------------------------------------- |
| **Rust**       | Lenguaje principal — rendimiento y safety |
| **Clap**       | Framework CLI (parsing de argumentos)     |
| **Ratatui**    | UI interactiva en terminal (TUI)          |
| **Crossterm**  | Manejo cross-platform de terminal         |
| **rusqlite**   | SQLite embebido para almacenamiento local |
| **serde**      | Serialización/deserialización (JSON/TOML) |
| **tera**       | Motor de templates (scaffold)             |
| **git2**       | Operaciones Git programáticas (libgit2)   |
| **arboard**    | Clipboard cross-platform                  |
| **cargo-test** | Testing integrado                         |

---

## 📁 Estructura del proyecto

```
rustcli/
├── src/
│   ├── main.rs                # Entry point + setup de Clap
│   ├── cli.rs                 # Definición de comandos CLI
│   ├── commands/
│   │   ├── mod.rs
│   │   ├── init.rs            # Scaffold de proyectos
│   │   ├── snippet.rs         # Gestión de snippets
│   │   ├── git_utils.rs       # Utilidades Git
│   │   └── dashboard.rs       # TUI con Ratatui
│   ├── db/
│   │   ├── mod.rs
│   │   └── storage.rs         # Operaciones SQLite
│   ├── templates/             # Templates Tera para scaffold
│   │   ├── rust-cli/
│   │   ├── rust-api/
│   │   └── python-fastapi/
│   ├── tui/
│   │   ├── mod.rs
│   │   ├── app.rs             # Estado de la app TUI
│   │   ├── ui.rs              # Renderizado de widgets
│   │   └── event.rs           # Manejo de eventos de teclado
│   └── error.rs               # Tipos de error personalizados
├── tests/
│   ├── test_init.rs
│   ├── test_snippets.rs
│   └── test_git_utils.rs
├── Cargo.toml
├── Makefile
├── Dockerfile
└── README.md
```

---

## 🗓️ Plan del fin de semana

### Sábado

| Hora           | Actividad                                         |
| -------------- | ------------------------------------------------- |
| 🌅 9:00-10:00  | Setup: `cargo init`, Cargo.toml, estructura base  |
| 🌅 10:00-12:00 | Definición CLI con Clap + comando `init` con Tera |
| 🌞 12:00-13:00 | Base de datos SQLite con rusqlite                  |
| 🌞 14:00-16:00 | Comandos de snippets (add, list, get, export)      |
| 🌆 16:00-18:00 | Utilidades Git con git2 (stats, changelog)         |

### Domingo

| Hora           | Actividad                                           |
| -------------- | --------------------------------------------------- |
| 🌅 9:00-10:30  | Dashboard TUI con Ratatui (layout, widgets)         |
| 🌅 10:30-12:00 | Interactividad TUI (navegación, timer pomodoro)     |
| 🌞 13:00-14:30 | Tests unitarios e integración                       |
| 🌞 14:30-16:00 | Error handling robusto + manejo de tipos de error    |
| 🌆 16:00-17:00 | README con GIFs de demo, `cargo install` y Dockerfile|

---

## ✅ Definición de "hecho"

- [ ] Al menos 4 comandos funcionales compilados en un solo binario
- [ ] Dashboard TUI interactivo con Ratatui
- [ ] Instalable con `cargo install --path .`
- [ ] Snippets persistentes con SQLite (rusqlite)
- [ ] Tests unitarios para cada módulo
- [ ] Manejo de errores con tipos personalizados (sin `unwrap()` en producción)
- [ ] README con ejemplos, instrucciones y al menos un GIF de demostración
- [ ] Binario cross-platform (Linux, macOS, Windows)

---

## 🧠 Conceptos de Rust demostrados

| Concepto                  | Aplicación en el proyecto                    |
| ------------------------- | -------------------------------------------- |
| Ownership & Borrowing     | Manejo eficiente de strings y buffers        |
| Pattern Matching          | Parsing de comandos y manejo de errores      |
| Enums + Result/Option     | Error handling idiomático                    |
| Traits                    | Abstracciones para storage y templates       |
| Lifetime annotations      | Referencias en estructuras de datos          |
| Módulos y crates          | Organización profesional del código          |
| Async (opcional)          | Operaciones de red no bloqueantes            |
| Derive macros             | Serialización con serde, CLI con clap        |

---

## 💼 Lo que demuestra al reclutador

| Habilidad                | Evidencia                                         |
| ------------------------ | ------------------------------------------------- |
| Rust idiomático          | Ownership, borrowing, pattern matching, traits     |
| Systems programming      | Binario único, cero runtime, alto rendimiento      |
| UX en terminal           | TUI interactiva con Ratatui, experiencia pulida    |
| Diseño de software       | Módulos desacoplados, error types, clean code      |
| Ecosistema Rust          | Clap, Serde, Ratatui, rusqlite, git2               |
| Distribución profesional | `cargo install`, Dockerfile, binarios multi-plat.  |
