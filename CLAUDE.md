# CLAUDE.md — Memoria de trabajo del proyecto

## Proyecto
**Refugio del Cielo** — landing one-page para una cabaña-mirador off-grid en Tobía, Cundinamarca.
Parte del ecosistema **Vertex Pather** (empresas dirigidas y asistidas por agentes).

## Orquestador
El proyecto se gestiona con **Usuario 15**, el agente orquestador (cofundador estratégico + jefe de operaciones).
Perfil, personalidad y roster de skills: `ops/ORCHESTRATOR.md`.
Arranque de sesión y clasificación de inputs: skill `vp-session`.
Protocolo operativo (arranque, fases, verificación, cierre): `ops/PROTOCOLO.md` — **seguirlo en cada sesión**.
Modelo del arnés y roadmap de fases: `ops/HARNESS.md`.

## Arquitectura del repo
Separación producto (`frontend/`) / operación (`ops/`). Diseño completo y roadmap de dominios futuros (backend, marketing, socios, panel de control) en `ARQUITECTURA.md`. Repo **público** desde 260715 (ver DEC-260715-04/05) — nada con cifras reales, contratos o datos personales entra a `ops/` mientras siga así.

## Stack
Sitio estático: HTML + CSS + JS vanilla, sin build, en `frontend/`. Fuentes por Google Fonts (Fraunces + Inter).

## Convenciones
- Imágenes en `assets/img/`, estilos en `assets/css/`, scripts en `assets/js/`.
- Documentación y decisiones en `docs/`.
- Commits en formato Conventional Commits (`feat:`, `fix:`, `docs:`, `chore:`…).
- Rama principal: `main`. Trabajo por features en `feature/<descripcion>`.

## Estado actual
- Todo el CSS y JS está embebido en `frontend/index.html` (1085 líneas). Pendiente extraerlos.
- Faltan imágenes `historia1-3.jpeg` (hay fallback por `onerror`).
- Deploy pendiente: workflow de GitHub Pages listo (`.github/workflows/deploy.yml`) pero dormido hasta decidir plataforma y activar "Pages source: GitHub Actions".

## Sistema de trabajo
- `ops/PROTOCOLO.md` — protocolo de sesión (Init · Fases · Verify · Cierre). Arnés Fase 1.
- `ops/HARNESS.md` — mapa del arnés (20 harnesses) y roadmap por fases.
- `ops/INBOX.md` — ideas y decisiones pendientes.
- `ops/TASKS.md` — pendientes operativos.
- `ops/memory/` — knowledge base (decisiones, aprendizajes, glosario).
- `ops/specs/` — especificaciones técnicas aprobadas antes de codear.
- `frontend/docs/README.md` — índice de documentación de producto.

## Pendientes
Ver `ops/TASKS.md` (operativos) e `ops/INBOX.md` (decisiones). Prioritarios: definir nivel de crítica del orquestador, imágenes de historias, externalizar CSS/JS, deploy.
