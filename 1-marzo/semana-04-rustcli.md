# 🦀 Semana 04 — RustCLI

> **Herramienta CLI de alto rendimiento para desarrolladores con Rust, Clap y Ratatui**

| Campo              | Detalle                                                 |
| ------------------ | ------------------------------------------------------- |
| 📅 Fechas          | 28-29 de marzo 2026                                     |
| 🏷️ Categoría       | Backend Foundations                                     |
| ⏱️ Tiempo estimado | 10-12 horas                                             |
| 📊 Dificultad      | ⭐⭐⭐ Intermedio                                       |
| 📊 Estado          | ✅ Completado                                           |
| 🔗 Repositorio     | [GitHub (DashTUI)](https://github.com/artur282/DashTUI) |

---

## 🎯 Descripción

RustCLI (ahora conocido como **DashTUI**) es una herramienta de línea de comandos todo-en-uno con un dashboard interactivo (TUI) de primer nivel diseñada para aumentar la productividad de desarrolladores. Incluye utilidades como: scaffold de proyectos (con plantillas nativas de Docker Compose), gestión de snippets de código leyendo automáticamente del portapapeles, análisis de repositorios Git en tiempo real, gestor de tareas, cronómetro pomodoro y una innovadora integración con **skills.sh** para descubrir AI Skills.

Todo está construido en **Rust** para máxima velocidad y eficiencia de memoria, operable 100% mediante el teclado. Este proyecto demuestra el dominio en crear herramientas profesionales y robustas para el ecosistema de desarrolladores.

---

## ✨ Features (Implementadas en DashTUI)

### 📊 1. General y Tareas

- [x] Dashboard interactivo navegable con flechas (Ratatui)
- [x] Vista general del entorno y métricas.
- [x] Gestor de "to-do" list integrado con atajos (`a` agregar, `x` completar, `d` eliminar).

### ⏱️ 2. Pomodoro

- [x] Cronómetro de concentración nativo en terminal.
- [x] Sigue periodos de enfoque con descansos automáticos.

### 🐳 3. Scaffold (Docker Ready)

- [x] Potente generador de proyectos (`bootstrap`) con mejores prácticas.
- [x] Templates nativos con **Docker Compose**: `rust-cli`, `rust-api`, `python-fastapi`, `python-django` (con PostgreSQL embebido), `node-express`.
- [x] Generación de `Dockerfile` multi-stage, `Makefile` unificado y `.gitignore`.

### 📝 4. Gestión de snippets

- [x] Manager de fragmentos de código conectado a base de datos embebida local.
- [x] Lectura automática del código desde el **portapapeles actual**.
- [x] Copiado fluido de vuelta al portapapeles.

### 🌿 5. Utilidades Git

- [x] Monitor en tiempo real del estado del repositorio (top contributors, total de commits).
- [x] Detección de ramas limpias y fuera de uso.
- [x] Limpieza de ramas locales ya mergeadas con un solo botón.

### 🔌 6. Skills (NUEVO)

- [x] Integración nativa con **skills.sh**
- [x] Búsqueda en el leaderboard global del ecosistema Agent.
- [x] Instalación inmediata mediante `npx skills add`.

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
| 🌞 12:00-13:00 | Base de datos SQLite con rusqlite                 |
| 🌞 14:00-16:00 | Comandos de snippets (add, list, get, export)     |
| 🌆 16:00-18:00 | Utilidades Git con git2 (stats, changelog)        |

### Domingo

| Hora           | Actividad                                             |
| -------------- | ----------------------------------------------------- |
| 🌅 9:00-10:30  | Dashboard TUI con Ratatui (layout, widgets)           |
| 🌅 10:30-12:00 | Interactividad TUI (navegación, timer pomodoro)       |
| 🌞 13:00-14:30 | Tests unitarios e integración                         |
| 🌞 14:30-16:00 | Error handling robusto + manejo de tipos de error     |
| 🌆 16:00-17:00 | README con GIFs de demo, `cargo install` y Dockerfile |

---

## ✅ Definición de "hecho"

- [x] Dashboard TUI interactivo con Ratatui funcional y navegable por pestañas
- [x] Scaffold generando múltiples lenguajes listos para Docker
- [x] Instalable con `make install` o `cargo install`
- [x] Snippets interoperables con el portapapeles del SO
- [x] Lógica de estado validada y robusta (sin crashes incontrolados en UI)
- [x] README completo con ejemplos, shields y documentación listos para Open Source
- [x] Binario cross-platform testeado

---

## 🧠 Conceptos de Rust demostrados

| Concepto              | Aplicación en el proyecto               |
| --------------------- | --------------------------------------- |
| Ownership & Borrowing | Manejo eficiente de strings y buffers   |
| Pattern Matching      | Parsing de comandos y manejo de errores |
| Enums + Result/Option | Error handling idiomático               |
| Traits                | Abstracciones para storage y templates  |
| Lifetime annotations  | Referencias en estructuras de datos     |
| Módulos y crates      | Organización profesional del código     |
| Async (opcional)      | Operaciones de red no bloqueantes       |
| Derive macros         | Serialización con serde, CLI con clap   |

---

## 💼 Lo que demuestra al reclutador

| Habilidad                | Evidencia                                         |
| ------------------------ | ------------------------------------------------- |
| Rust idiomático          | Ownership, borrowing, pattern matching, traits    |
| Systems programming      | Binario único, cero runtime, alto rendimiento     |
| UX en terminal           | TUI interactiva con Ratatui, experiencia pulida   |
| Diseño de software       | Módulos desacoplados, error types, clean code     |
| Ecosistema Rust          | Clap, Serde, Ratatui, rusqlite, git2              |
| Distribución profesional | `cargo install`, Dockerfile, binarios multi-plat. |
