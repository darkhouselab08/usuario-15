# ops/ — Operación de la empresa

Esta carpeta es el "backstage" de **Refugio del Cielo**: cómo se toman las decisiones, qué está pendiente, y qué sabe el sistema. Vive separada de `frontend/` a propósito — ver [`ARQUITECTURA.md`](../ARQUITECTURA.md) en la raíz.

Refugio del Cielo es parte de **Vertex Pather**, una apuesta por empresas dirigidas y asistidas por agentes: casi todo lo que hay en esta carpeta lo mantiene un orquestador de IA (**Usuario 15**), no un equipo humano tradicional.

## Contenido

| Archivo/carpeta | Qué es |
|---|---|
| [`CONTEXTO.md`](./CONTEXTO.md) | **Empieza aquí si eres nuevo** (Cowork u otro agente): estado actual, qué se puede/no se puede hacer, decisiones clave. |
| [`ORCHESTRATOR.md`](./ORCHESTRATOR.md) | Perfil, personalidad y roster de skills del orquestador Usuario 15. |
| [`GITHUB-SETUP.md`](./GITHUB-SETUP.md) | Protocolo de cuenta y repo de GitHub. |
| [`INBOX.md`](./INBOX.md) | Ideas y decisiones pendientes de aprobación. |
| [`TASKS.md`](./TASKS.md) | Pendientes operativos ya aprobados. |
| [`memory/`](./memory/) | Knowledge base: decisiones (`DEC-`), aprendizajes (`APR-`), glosario. |
| [`specs/`](./specs/) | Especificaciones técnicas aprobadas antes de codear. |
| [`socios/`](./socios/) | Presentaciones, propuestas y notas para socios/inversionistas. |

## Flujo de trabajo

```
INBOX.md (idea) → aprobación de Franco → TASKS.md (ejecutable) → specs/ si es técnico → ejecución → memory/ (si deja aprendizaje)
```

## Futuro

`ops/marketing/` se crea cuando haya contenido real que gestionar (ver roadmap en `ARQUITECTURA.md`). Son datos de negocio — nunca deben salir de un repo privado.
