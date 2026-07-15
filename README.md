# Refugio del Cielo

Landing one-page para **Refugio del Cielo**, una cabaña-mirador off-grid en Tobía, Cundinamarca. Internet Starlink garantizado, energía solar y vista de 180° al valle. Enfocada a nómadas digitales y parejas.

**Demo en vivo:** https://darkhouselab08.github.io/usuario-15/

## Stack

Sitio estático: HTML + CSS + JavaScript vanilla. Sin dependencias de build. Fuentes vía Google Fonts (Fraunces + Inter).

## Estructura

```
refugio-del-cielo/
├── frontend/            # el sitio: HTML/CSS/JS, assets, docs de diseño
├── ops/                 # operación del proyecto (decisiones, tareas, memoria)
├── .github/workflows/   # deploy a GitHub Pages
├── ARQUITECTURA.md      # diseño del repo y roadmap de dominios futuros
├── CLAUDE.md
└── LICENSE
```

Detalle completo y roadmap (backend, marketing, panel de control) en [`ARQUITECTURA.md`](./ARQUITECTURA.md).

## Desarrollo local

No requiere build. Desde `frontend/`:

```bash
cd frontend
python3 -m http.server 8000
# abre http://localhost:8000
```

## Cómo se gestiona este proyecto

Refugio del Cielo es parte de **Vertex Pather**, una apuesta por empresas dirigidas y asistidas por agentes: este repositorio lo opera un orquestador de IA (**Usuario 15**), con pocos humanos en el loop. Cómo funciona eso está documentado en [`ops/README.md`](./ops/README.md).

## Pendientes

Ver [`ops/TASKS.md`](./ops/TASKS.md) (operativos) y [`ops/INBOX.md`](./ops/INBOX.md) (decisiones pendientes).
