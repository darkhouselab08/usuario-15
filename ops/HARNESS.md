# HARNESS — El arnés de Usuario 15

> Abstracción de la *Guía Integral de Harness Engineering* (Drive, 260717) aplicada a este repo.
> Idea central: el salto de calidad con IA no está en mejores prompts, sino en construir el **arnés** — la capa de control que rodea al modelo y le da **dirección, memoria, verificación y límites**. El repo es el arnés; el chat no es la fuente de verdad.

---

## 1. Los tres pilares (resumen ejecutivo)

1. **Repositorio como sistema** — las reglas viven en archivos (`.md`, scripts), no en la conversación.
2. **Orquestación multi-agente** — un líder que dirige y delega a sub-agentes con contexto aislado y mínimo.
3. **Verificación automatizada** — el agente no dice que terminó: lo *demuestra* con evidencia (pruebas, logs).

Y dos disciplinas de contexto: **externalizar** la información a archivos, y **limpiar** el contexto antes de que se degrade (al 20–40% de la ventana).

---

## 2. Mapa: qué ya tienes vs. qué falta

Los 20 harnesses de la guía, contra la capa `ops/` actual.

| # | Harness | Estado en este repo | Dónde vive |
|---|---------|---------------------|------------|
| **A — Orquestación y contexto** ||||
| 1 | SDD Orchestrator | ✅ Tiene | `ops/ORCHESTRATOR.md` + skill `vp-session` |
| 2 | Delegation | 🟡 Parcial | roster de skills (`ORCHESTRATOR.md §6`) |
| 3 | SDD Init | ✅ Tiene (Fase 1) | `ops/PROTOCOLO.md §1` |
| 4 | Execution Mode | ✅ Tiene | guardrails: Franco aprueba lo irreversible |
| 5 | Artifact Store | ✅ **Fuerte** | INBOX/TASKS/memory/docs = fuente de verdad |
| **B — Fases y dependencias** ||||
| 6 | Face DAG (no saltar etapas) | ✅ Tiene (Fase 1) | `ops/PROTOCOLO.md §2` |
| 7 | Artifact Dependency | ✅ Tiene | `ops/PROTOCOLO.md §2` + `ops/specs/` |
| 8 | Result Contract | ✅ Tiene (Fase 1) | `ops/PROTOCOLO.md §4` |
| 9 | Artifact Grammar | 🟡 Parcial | convención de nombres + formato INBOX/TASKS |
| **C — Memoria y continuidad** ||||
| 10 | Engram Memory | ✅ **Fuerte** | `ops/memory/` + `CLAUDE.md` |
| 11 | Strict TDD | ⬜ Falta | *no aplica aún* (sitio estático, sin backend) |
| 12 | Verify | ✅ Tiene (Fase 1) | `ops/PROTOCOLO.md §3` |
| 13 | Operational Continuity | ✅ Tiene | `ops/CONTEXTO.md` + cierre de `vp-session` |
| **D — Skills y sub-agentes** ||||
| 14 | Skill Registry | ✅ Tiene | roster (`ORCHESTRATOR §6`) |
| 15 | Skill Digestion | ⬜ Falta | *nice to have* |
| 16 | Skill Resolution Feedback | ⬜ Falta | *avanzado* |
| 17 | Sub-Agent Isolation | ⬜ Falta | *aplica al usar subagentes / Claude Code* |
| **E — Entrega y revisión** ||||
| 18 | Review Workload | 🟡 Parcial | Conventional Commits + Franco revisa |
| 19 | Delivery Strategy | 🟡 Parcial | ramas `feature/` |
| 20 | Chain Strategy | ⬜ Falta | *avanzado, cuando haya más código* |

**Lectura:** el núcleo que da el 80% del valor (Artifact Store, Engram Memory, Orchestrator, Skill Registry, Continuity) **ya está**. Lo que falta se divide en *barato y de alto rendimiento ahora* y *prematuro hasta que haya backend real*.

---

## 3. Plan por fases (estratégico — no sobre-construir)

### Fase 1 — ✅ HECHA (260717) → `ops/PROTOCOLO.md`
Alto rendimiento, costo bajo. Solo archivos y disciplina.

- **SDD Init (#3):** ✅ bloque de arranque de sesión explícito — `PROTOCOLO §1`.
- **Result Contract (#8):** ✅ "sobre" de cierre con formato fijo — `PROTOCOLO §4`.
- **Face DAG + Verify (#6, #12):** ✅ regla de fases y checklist de verificación — `PROTOCOLO §2 y §3`.

### Fase 2 — Cuando arranque el backend (ligado a INB-008)
Estos harnesses solo tienen sentido con código real que ejecutar y probar.

- **Strict TDD (#11)** y **Verify con evidencia (#12 pleno):** rojo-verde-refactor, logs y comandos corridos.
- **Sub-Agent Isolation (#17)** y **Skill Digestion (#15):** al delegar a subagentes / Claude Code.

### Fase 3 — Cuando escale (multi-proyecto / B2B)
- **Chain / Delivery Strategy (#19, #20)** y **Skill Resolution Feedback (#16).**

---

## 4. Principio rector

> No construir el arnés completo de golpe. Construir el pedazo que resuelve un dolor real *hoy*, dejar documentado el resto, y activarlo cuando el proyecto lo pida. Un arnés prematuro es burocracia; un arnés ausente es caos. El punto medio es la ingeniería.

*Fuente: Guía Integral de Harness Engineering (Drive, 260717). Este documento es la versión abstraída y aplicada; el original queda en Drive.*
