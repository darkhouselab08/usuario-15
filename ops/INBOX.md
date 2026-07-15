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

---

## Historial (resuelto / descartado)

_(vacío por ahora)_
