# Decisiones (DEC-)

Registro de decisiones de negocio y arquitectura. Cada una: qué se decidió, por qué, y consecuencia.

---

### DEC-260715-01 · Orquestador único llamado "Usuario 15"
- **Qué:** El cerebro digital del proyecto se llama Usuario 15 (nombre de trabajo, atado al workspace).
- **Por qué:** Evitar confusión entre el agente y otros nombres; simple y renombrable.
- **Consecuencia:** Todo el sistema (CLAUDE.md, docs) referencia a Usuario 15 como orquestador.

### DEC-260715-02 · Personalidad híbrida cofundador + jefe de operaciones
- **Qué:** El orquestador combina modo estratégico (retar, proponer) y modo operativo (ejecutar).
- **Por qué:** Franco quiere un par que piense con él y a la vez ejecute sin fricción.
- **Consecuencia:** Falta afinar el nivel de crítica (ver INB-001).

### DEC-260715-03 · Estructura de proyecto estático + knowledge base
- **Qué:** assets/{img,css,js,fonts}, docs/, memory/, specs/, INBOX.md, TASKS.md.
- **Por qué:** Reflejar en el IDE las directrices del orquestador y de Vertex Pather (empresa agent-led).
- **Consecuencia:** Base para escalar el sistema a otros proyectos. Superada por DEC-260715-04.

### DEC-260715-04 · Separación frontend/ vs ops/, repo privado
- **Qué:** Se reorganizó el repo en `frontend/` (producto: sitio, assets, docs técnicos) y `ops/` (operación de la empresa: INBOX, TASKS, memory, specs, perfil del orquestador). Se documentó el roadmap de dominios futuros (backend/, ops/marketing/, ops/socios/, control/) en `ARQUITECTURA.md`, sin crear carpetas vacías. El repo pasó de público a **privado**.
- **Por qué:** Franco quiere que el repo se vea profesional para un ingeniero externo (portfolio) sin perder la capa "agent-led" que documenta cómo opera la empresa. `ops/` iba a incluir datos de negocio (socios, marketing) que no pueden ser públicos.
- **Consecuencia:** Convención para todos los proyectos de Vertex Pather: código en su propio dominio (`frontend/`/`backend/`), operación en `ops/`, dominios nuevos se crean solo cuando hay contenido real (no scaffolding especulativo). Deploy a GitHub Pages ahora requiere workflow por Actions (`.github/workflows/deploy.yml`) en vez de "deploy from branch", porque el sitio ya no está en la raíz. Revertida (repo público) por DEC-260715-05.

### DEC-260715-05 · Repo vuelve a público, deploy con GitHub Pages
- **Qué:** Tras DEC-260715-04 (repo privado), al intentar activar GitHub Pages falló: el plan Free de GitHub no soporta Pages en repos privados. Se evaluó Netlify (sí soporta privados gratis) pero Franco eligió simplicidad: repo de vuelta a **público**, deploy con GitHub Pages. Sitio en vivo: `https://darkhouselab08.github.io/usuario-15/`.
- **Por qué:** El proyecto todavía es un demo, sin información delicada real en `ops/` (el pitch de `ops/socios/` no tiene cifras ni datos sensibles). Franco no quiere complicarse con Netlify por ahora ni pagar GitHub Pro.
- **Consecuencia:** Queda en el radar volver a privado (+ Netlify o GitHub Pro) el día que `ops/` empiece a tener datos reales sensibles (cifras, contratos, información de socios/huéspedes). Hasta entonces, todo lo que entre a `ops/` debe asumirse público — ver regla actualizada en `ARQUITECTURA.md`.
