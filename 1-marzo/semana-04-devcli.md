# ⌨️ Semana 04 — DevCLI

> **Herramienta CLI de productividad para desarrolladores con Python, Typer y Rich**

| Campo              | Detalle              |
| ------------------ | -------------------- |
| 📅 Fechas          | 28-29 de marzo 2026  |
| 🏷️ Categoría       | Backend Foundations  |
| ⏱️ Tiempo estimado | 10-12 horas          |
| 📊 Dificultad      | ⭐⭐ Intermedio-bajo |

---

## 🎯 Descripción

DevCLI es una herramienta de línea de comandos diseñada para aumentar la productividad de desarrolladores. Incluye utilidades como: scaffold de proyectos, gestión de snippets de código, generación de boilerplate, análisis de repositorios Git, y más. Todo con una interfaz hermosa usando Rich y una experiencia de usuario tipo "feel good".

Este proyecto demuestra que Python no es solo para APIs — es una herramienta poderosa para automatización local.

---

## ✨ Features

### Scaffold de proyectos

- [ ] `devcli init <template>` — Crear proyecto desde template
- [ ] Templates: fastapi, django, python-lib, scraper
- [ ] Generación de Dockerfile, docker-compose, Makefile
- [ ] Configuración automática de pyproject.toml
- [ ] Inicialización de Git + .gitignore

### Gestión de snippets

- [ ] `devcli snippet add <name>` — Guardar snippet de código
- [ ] `devcli snippet list` — Listar snippets con búsqueda
- [ ] `devcli snippet get <name>` — Copiar snippet al clipboard
- [ ] `devcli snippet export` — Exportar todos los snippets
- [ ] Almacenamiento local con SQLite

### Utilidades Git

- [ ] `devcli git stats` — Estadísticas del repo (commits, contributors)
- [ ] `devcli git changelog` — Generar changelog desde commits
- [ ] `devcli git clean-branches` — Limpiar ramas mergeadas

### Productividad

- [ ] `devcli todo` — Lista de tareas rápida (SQLite)
- [ ] `devcli timer` — Pomodoro timer en terminal
- [ ] `devcli env check` — Verificar herramientas instaladas

---

## 🛠️ Stack técnico

| Tecnología         | Propósito                  |
| ------------------ | -------------------------- |
| **Typer**          | Framework CLI              |
| **Rich**           | UI hermosa en terminal     |
| **SQLite**         | Almacenamiento local       |
| **Click**          | Complemento a Typer        |
| **Jinja2**         | Templates para scaffold    |
| **pyperclip**      | Clipboard                  |
| **pytest**         | Testing                    |
| **setuptools/pip** | Empaquetado y distribución |

---

## 📁 Estructura del proyecto

```
devcli/
├── devcli/
│   ├── __init__.py
│   ├── __main__.py            # Entry point
│   ├── app.py                 # App Typer principal
│   ├── commands/
│   │   ├── init_cmd.py        # Scaffold
│   │   ├── snippet.py         # Gestión de snippets
│   │   ├── git_utils.py       # Utilidades Git
│   │   └── productivity.py    # Todo, timer, etc.
│   ├── templates/             # Templates Jinja2
│   │   ├── fastapi/
│   │   ├── django/
│   │   └── python-lib/
│   ├── db/
│   │   └── storage.py         # SQLite operations
│   └── ui/
│       └── console.py         # Formateo con Rich
├── tests/
│   ├── test_init.py
│   ├── test_snippets.py
│   └── test_git_utils.py
├── pyproject.toml
├── Makefile
└── README.md
```

---

## 🗓️ Plan del fin de semana

### Sábado

| Hora           | Actividad                               |
| -------------- | --------------------------------------- |
| 🌅 9:00-10:00  | Setup: proyecto, Typer, estructura base |
| 🌅 10:00-12:00 | Comando `init` con templates Jinja2     |
| 🌞 12:00-13:00 | Base de datos SQLite para snippets      |
| 🌞 14:00-16:00 | Comandos de snippets (add, list, get)   |
| 🌆 16:00-18:00 | Utilidades Git (stats, changelog)       |

### Domingo

| Hora           | Actividad                                    |
| -------------- | -------------------------------------------- |
| 🌅 9:00-10:30  | Comandos de productividad (todo, timer)      |
| 🌅 10:30-12:00 | UI con Rich (tablas, paneles, colores)       |
| 🌞 13:00-14:30 | Tests                                        |
| 🌞 14:30-16:00 | Empaquetado con pyproject.toml + pip install |
| 🌆 16:00-17:00 | README con GIFs de demo y docs               |

---

## ✅ Definición de "hecho"

- [ ] Al menos 4 comandos funcionales
- [ ] UI hermosa con Rich (colores, tablas, paneles)
- [ ] Instalable con `pip install .`
- [ ] Snippets persistentes con SQLite
- [ ] Tests de cada comando
- [ ] README con ejemplos e instrucciones
- [ ] Al menos un GIF de demostración

---

## 💼 Lo que demuestra al reclutador

| Habilidad          | Evidencia                            |
| ------------------ | ------------------------------------ |
| Python avanzado    | CLI, templates, empaquetado          |
| UX en terminal     | Rich, experiencia de usuario cuidada |
| Diseño de software | Comando-patrón, modular, extensible  |
| Automatización     | Herramientas que ahorran tiempo      |
| Distribución       | Paquete instalable con pip           |
