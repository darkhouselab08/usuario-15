# Arquitectura del repositorio

Cómo está organizado **Refugio del Cielo** y hacia dónde escala como empresa dirigida por agentes (**Vertex Pather**). Este documento es la fuente de verdad de "qué va dónde" — se actualiza cada vez que se crea un dominio nuevo.

## Principio

Separar dos capas que no se deben mezclar:

1. **Producto** (`frontend/`, `backend/`) — lo que un ingeniero necesita para correr y entender el sitio.
2. **Operación** (`ops/`) — cómo se dirige la empresa: decisiones, tareas, memoria, marketing, socios. Vive aparte para que el producto se lea limpio y para que datos de negocio no terminen mezclados con código.

## Estado actual

```
refugio-del-cielo/
├── frontend/            # el sitio: HTML/CSS/JS vanilla
│   ├── index.html
│   ├── assets/          # img, css, js, fonts
│   └── docs/            # brief de diseño y notas técnicas del frontend
├── ops/                 # operación de la empresa agent-led
│   ├── README.md
│   ├── ORCHESTRATOR.md  # perfil del orquestador Usuario 15
│   ├── GITHUB-SETUP.md  # protocolo de cuenta/repo GitHub
│   ├── INBOX.md         # ideas y decisiones pendientes
│   ├── TASKS.md         # pendientes operativos
│   ├── memory/          # decisiones, aprendizajes, glosario
│   └── specs/           # specs técnicos aprobados antes de codear
├── .github/workflows/   # CI / deploy
├── CLAUDE.md            # memoria de trabajo (raíz, requerido por Claude Code)
├── ARQUITECTURA.md       # este archivo
├── LICENSE
└── README.md
```

## Roadmap — dominios futuros (no creados aún)

Se crean solo cuando tengan contenido real, no como scaffolding vacío. Regla: **una carpeta nace cuando hay algo que guardar en ella, no antes.**

| Dominio | Dónde vivirá | Cuándo se crea |
|---|---|---|
| **backend/** | raíz, junto a `frontend/` | Cuando exista lógica de servidor real (reservas, pagos, formulario con envío a base de datos). Hoy el sitio es 100% estático. |
| **Marketing** | `ops/marketing/` | Cuando haya campañas, copy o calendario de contenido que gestionar más allá de la landing. |
| **Socios** | `ops/socios/` ✅ creado | Notas de reuniones, acuerdos, contactos y presentaciones a partners/inversionistas. Primer contenido: `pitch-inversionista-2026-07.html`. |
| **Panel de control** | `control/` (raíz) | Visión a futuro: un panel donde Franco (dueño) tenga visibilidad y mando sobre todo el proyecto — estado de tareas, métricas, decisiones pendientes — sin tener que leer archivos sueltos. Se define con un spec en `ops/specs/` cuando se decida construirlo. |

## Reglas de visibilidad y datos sensibles

- El repo es **privado**. `ops/socios/` y `ops/marketing/` pueden contener información de negocio — nunca deben vivir en un repo público.
- Si algún día el código (`frontend/`, `backend/`) se separa a un repo público para portfolio, `ops/` **no** se replica ahí.

## Cómo crecer esto

Cuando se necesite un dominio nuevo que no está en la tabla de arriba:
1. Se registra como IDEA en `ops/INBOX.md`.
2. Se decide dónde vive (¿producto o operación? ¿sensible o no?).
3. Se agrega una fila a este documento.
4. Se crea la carpeta solo entonces.
