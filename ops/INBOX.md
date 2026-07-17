# INBOX — Ideas y decisiones pendientes

Bandeja de entrada del orquestador. Todo lo que aún no es tarea ejecutable vive aquí hasta que Franco decide.
Estados: **IDEA** (sin analizar) · **ANALIZADA** (con propuesta, espera decisión) · **APROBADA** (pasa a TASKS.md) · **DESCARTADA**.

Formato de item:
```
### [ID] Título
- Estado: IDEA | ANALIZADA | APROBADA | DESCARTADA
- Fecha: YYMMDD
- Contexto: …
- Propuesta / decisión: …
```

---

## Pendientes de decisión

### INB-001 Nivel de crítica del orquestador
- Estado: ANALIZADA
- Fecha: 260715
- Contexto: El perfil de Usuario 15 incluye "retar" en modo estratégico, pero necesita permiso explícito.
- Propuesta: Elegir entre (a) abiertamente crítico —frena y discute rutas— o (b) crítico solo cuando se le pide. Decisión de Franco.

### INB-002 Externalizar CSS y JS de index.html
- Estado: IDEA
- Fecha: 260715
- Contexto: Todo el CSS/JS está embebido en frontend/index.html (~1085 líneas). Extraerlos a frontend/assets/css/ y frontend/assets/js/ mejora mantenimiento.
- Propuesta: Skill `engineering:architecture` para decidir el corte; luego ejecutar.

### INB-003 Imágenes de historias faltantes
- Estado: IDEA
- Fecha: 260715
- Contexto: frontend/index.html referencia historia1-3.jpeg (no existen; hay fallback por onerror).
- Propuesta: Franco provee las 3 fotos → van a frontend/assets/img/.

### INB-004 Deploy del sitio
- Estado: APROBADA (hecho)
- Fecha: 260715
- Contexto: GitHub Pages gratis no soporta repos privados. Se evaluó Netlify (evita el problema) pero Franco prefirió simplicidad: el proyecto aún es un demo sin información delicada, así que el repo volvió a público y se usa GitHub Pages directo. Revisitar (repo privado + Netlify o GitHub Pro) cuando haya datos sensibles reales en `ops/`.
- Propuesta: — (resuelto). Sitio en vivo: `https://darkhouselab08.github.io/usuario-15/`. Workflow: `.github/workflows/deploy.yml`, se dispara en cada push a `main` que toque `frontend/`.

### INB-005 Crear cuenta de GitHub
- Estado: APROBADA (hecho)
- Fecha: 260715
- Contexto: Protocolo escrito en `ops/GITHUB-SETUP.md`. Cuenta creada, repo `darkhouselab08/usuario-15` conectado y en privado.
- Propuesta: — (resuelto, ver historial).

### INB-006 Reestructuración frontend/ + ops/
- Estado: APROBADA (hecho)
- Fecha: 260715
- Contexto: El repo mezclaba código de producto con operación de la empresa (INBOX, TASKS, memory, specs, perfil del orquestador) en la raíz. Franco pidió una estructura que se vea profesional para un ingeniero externo pero mantenga la capa agent-led operable, escalable a backend/marketing/socios/control futuros.
- Propuesta: — (resuelto). Ver `ARQUITECTURA.md` en la raíz para el diseño completo y el roadmap de dominios futuros.

### INB-007 Presentación para inversionista + creación de ops/socios/
- Estado: APROBADA (hecho)
- Fecha: 260715
- Contexto: Franco pidió una presentación HTML para mostrarle al dueño del terreno (inversionista clave) la visión de un complejo de cabañas operado con software de Vertex Pather. Se creó `ops/socios/pitch-inversionista-2026-07.html`, publicada también como Artifact. Esto activó el dominio `ops/socios/` del roadmap (antes solo documentado).
- Propuesta: — (resuelto). Copia editable (sin diseño, solo contenido) también en Google Drive de Franco, con link al Artifact.

### INB-008 Backend de reservas
- Estado: ANALIZADA
- Fecha: 260715
- Contexto: El sitio hoy es 100% estático, sin backend. Franco quiere iniciar reservas, conversación con huéspedes por WhatsApp y mucha interacción con clientes a mediano/largo plazo. Ya se conversó una propuesta de stack (no implementada): Node.js/TypeScript en serverless (Cloudflare Workers o Vercel), Supabase (Postgres) para reservas/huéspedes/conversaciones, WhatsApp Cloud API de Meta, Claude API/Agent SDK para la conversación — ver `ops/memory/decisiones.md` si se retoma la discusión completa.
- Propuesta: Queda como plan a futuro, no arrancar código todavía. Cuando Franco lo apruebe, el primer paso es un spec en `ops/specs/` antes de tocar código (flujo normal del proyecto).

### INB-009 Propuesta formal de sociedad para cabañas adicionales
- Estado: ANALIZADA (prioritaria)
- Fecha: 260717
- Contexto: Franco marca como siguiente paso prioritario estructurar una propuesta seria para construir cabañas adicionales bajo esquema de sociedad: el propietario aporta el terreno, nosotros (como constructora) aportamos la edificación. Requiere: (a) estrategia de persuasión al dueño de tierras, (b) perfil/estructura empresarial idónea de la constructora, (c) ruta de financiamiento.
- Propuesta: Redactar un documento marco en `ops/socios/` (estructura de la sociedad, propuesta de valor, opciones de reparto y de financiamiento) SIN cifras inventadas — solo marcadores hasta tener datos reales.
- Plan de trabajo (260717): `ops/socios/plan-propuesta-sociedad.md` — 6 fases (datos base → investigación → estrategia → borrador → números → cierre). Pendiente: Franco aprueba el plan y decide arrancar por F1 (datos base) o F2 (investigación legal/financiera).

### INB-010 Consolidar y mapear los "arneses de desarrollo"
- Estado: ANALIZADA (mapeo hecho)
- Fecha: 260717
- Contexto: Franco quiere los "arneses de desarrollo" mapeados antes de escalar. Se revisó la *Guía de Harness Engineering* (Drive, 260717) y se mapeó contra la capa `ops/`.
- Resultado: El núcleo del arnés ya existe (~60%). Ver `ops/HARNESS.md`. **Fase 1 HECHA (260717)** → `ops/PROTOCOLO.md` (SDD Init, Face DAG, Verify, Result Contract). Fase 2: con backend (TDD, sub-agentes). Fase 3: al escalar.
- Propuesta: Fase 1 cerrada. Fase 2 queda ligada a INB-008 (backend). Decisión de Franco sobre cuándo activarla.

### INB-011 Revisar doc de conceptos clave en Drive
- Estado: BLOQUEADA
- Fecha: 260717
- Contexto: Franco creó en Google Drive un documento con los conceptos clave para el flujo de trabajo en Cowork y la interacción con Claude; quiere abstraerlos para estructurar un flujo más organizado.
- Propuesta: Falta el link o conectar Google Drive para leerlo. En cuanto llegue, extraer conceptos → posible `ops/memory/` o guía de flujo.

### INB-012 Formalizar modelo de negocio "socio tecnológico estratégico"
- Estado: IDEA
- Fecha: 260717
- Contexto: Modelo para Usuario 15: administración remota de un complejo de cabañas exclusivo para profesionales/empresarios digitales; software con tecnologías emergentes para gestión física local + automatización + dashboard central. Posicionamiento: socio tecnológico estratégico. Alineado con Vertex-Partner ("cerebro digital" para clientes).
- Propuesta: Documentar la propuesta de valor y el encaje con Vertex Pather. Insumo directo para INB-009.

### INB-013 Visión inmobiliaria de largo plazo
- Estado: IDEA (visión)
- Fecha: 260717
- Contexto: El complejo de cabañas como catalizador de un desarrollo mayor: sector de alta plusvalía con infraestructura vial y residencias de lujo para la comunidad global de profesionales de internet de altos ingresos. Referencias: origen de los Hamptons; modelo Farrell de integración vertical en construcción.
- Propuesta: Guardar como norte estratégico. No accionar todavía; informa la ambición de INB-009.

### INB-014 Nombre oficial: Vertex Pather vs Vertex-Partner
- Estado: APROBADA (resuelto)
- Fecha: 260717
- Contexto: En el volcado aparecía "Vertex-Partner"; en el repo y en el deck de inversores es "Vertex Pather" ("Pather = socio/partner").
- Decisión de Franco: nombre canónico **Vertex Pather**; su sentido viene de "partner/socio". Glosario actualizado.

---

## Historial (resuelto / descartado)

_(vacío por ahora)_
