# PROTOCOLO — Operación de sesión (Arnés Fase 1)

> Los tres arneses baratos y de alto rendimiento, formalizados. Cero código: es disciplina y formato.
> Implementa: **SDD Init (#3)**, **Face DAG + Artifact Dependency (#6, #7)**, **Verify (#12)** y **Result Contract (#8)** de `ops/HARNESS.md`.
> El orquestador (Usuario 15) sigue este protocolo en cada sesión.

---

## 1. Arranque de sesión — *SDD Init*

Antes de tocar nada, cargar y reportar el estado en este bloque fijo:

```
SESIÓN INICIADA — [fecha]
─────────────────────────────
Rama:             [nombre]
Último commit:    [mensaje]
INBOX pendiente:  [N — títulos de items sin decidir]
Objetivo:         [pregunta al fundador]
─────────────────────────────
```

Reglas de arranque:
- Leer `CLAUDE.md` (memoria de trabajo) e `ops/INBOX.md`.
- Verificar rama y último commit.
- No ejecutar tareas técnicas hasta confirmar objetivo con Franco.

---

## 2. Regla de fases — *Face DAG + Artifact Dependency*

El trabajo fluye en este orden. **No se salta ninguna fase.**

```
IDEA  →  SPEC  →  CÓDIGO  →  VERIFY  →  CIERRE
```

| Fase | Requiere de entrada | Produce | Dónde |
|------|--------------------|---------|-------|
| **IDEA** | — | item registrado | `ops/INBOX.md` |
| **SPEC** | idea aprobada por Franco | especificación | `ops/specs/NN_*.md` |
| **CÓDIGO** | spec aprobado | cambios en rama | `feature/NN-desc` |
| **VERIFY** | código terminado | evidencia (§3) | reporte |
| **CIERRE** | verify OK | sobre + commit (§4) | `ops/` + git |

Dependencias inviolables:
- **No hay código sin spec.** Si no hay spec, primero se redacta y Franco aprueba.
- **No hay spec sin idea aprobada** en INBOX.
- Cambios triviales (typo, doc menor) pueden ir *inline* sin spec — criterio del orquestador, declarado al hacerlo.

---

## 3. Verificación antes de cerrar — *Verify*

No basta decir "listo": hay que demostrarlo. Checklist mínimo:

- [ ] ¿Hace lo que el spec / la tarea pedía?
- [ ] ¿Se probó? (código: corre sin error; doc: releído y coherente)
- [ ] ¿Los archivos quedaron en la carpeta correcta y con el nombre de convención?
- [ ] ¿Memoria actualizada? (`INBOX`, `TASKS`, `memory/` según aplique)
- [ ] ¿Sin datos de negocio inventados ni secretos en texto plano?
- [ ] ¿Hay mensaje de commit propuesto?

Si algo falla → no se cierra; se resuelve o se reporta como riesgo.

---

## 4. Cierre de sesión — *Result Contract*

Cada cierre devuelve este "sobre" fijo, no prosa suelta:

```
CIERRE DE SESIÓN — [fecha]
─────────────────────────────
Status:            [en curso | cerrada]
Hecho:             [bullets de lo entregado]
Riesgos/pendientes:[bullets — o "ninguno"]
Siguiente paso:    [una línea]
Archivos tocados:  [lista]
Commit propuesto:  [mensaje en Conventional Commits]
─────────────────────────────
```

Recordatorio: el orquestador prepara staging y commit; **Franco hace el push** desde su terminal.

---

*Arnés Fase 1 · activo desde 260717 · ver `ops/HARNESS.md` para el mapa completo y las fases 2–3.*
