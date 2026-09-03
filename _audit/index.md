# _audit/index.md

> **Tablero de auditorias.** Una fila por sesion cerrada: su informe, la auditoria que lo juzgo y
> en que quedo. Es la vista rapida — el detalle de cada hallazgo vive en `findings.md`.

---

## Tablero

| Informe | Sesion | Fecha | Commit auditado | Auditoria | Veredicto | Hallazgos |
|---|---|---|---|---|---|---|
| `S-001.md` | S-001 | 2026-08-31 | `6a16e5f` | `R-001.md` | Sin hallazgos | - |
| `S-002.md` | S-002 | 2026-08-31 | `badc878` | `R-002.md` | Con hallazgos (4) | F-001, F-002, F-003, F-004 |
| `S-003.md` | S-003 | 2026-09-01 | `ea0b850` | `R-003.md` | Con hallazgos (3) | F-005, F-006, F-007 |
| `S-004.md` | S-004 | 2026-09-01 | `c70b757` | `R-004.md` | Con hallazgos (3) | F-008, F-009, F-010 |
| `S-005.md` | S-005 | 2026-09-01 | `510d580` | `R-005.md` | Con hallazgos (4) | F-011, F-012, F-013, F-014 |
| `S-006.md` | S-006 | 2026-09-02 | `d906a5d` | `R-006.md` | Con hallazgos (2) | F-015, F-016 |
| `S-007.md` | S-007 | 2026-09-02 | `122b770` | `R-007.md` | Con hallazgos (3) | F-017, F-018, F-019 |
| `S-008.md` | S-008 | 2026-09-02 | `f096fff` | `R-008.md` | Con hallazgos (4) | F-020, F-021, F-022, F-023 |
| `S-009.md` | S-009 | 2026-09-02 | `fc91957` | `R-009.md` | Con hallazgos (3) | F-024, F-025, F-026 |
| `S-010.md` | S-010 | 2026-09-02 | `51354ef` | `R-010.md` | Con hallazgos (2) | F-027, F-028 |
| `S-011.md` | S-011 | 2026-09-02 | `2a2d3b6` | `R-011.md` | Con hallazgos (3) | F-029, F-030, F-031 |
| `S-012.md` | S-012 | 2026-09-02 | `7f55389` | `R-012.md` | Con hallazgos (2) | F-032, F-033 |
| `S-013.md` | S-013 | 2026-09-02 | `8eb8666` | `R-013.md` | Con hallazgos (1) | F-034 |
| `S-014.md` | S-014 | 2026-09-03 | `ca56b93` | `R-014.md` | Con hallazgos (2) | F-035, F-036 |
| `S-015.md` | S-015 | 2026-09-02 | `ea48ae8` | `R-015.md` | Con hallazgos (2) | F-037, F-038 |
| `S-016.md` | S-016 | 2026-09-03 | `bd8a9ff` | `R-016.md` | Con hallazgos (1) | F-039 |
| `S-017.md` | S-017 | 2026-09-03 | `1988d2f` | `R-017.md` | Con hallazgos (5) | F-040, F-041, F-042, F-043, F-044 |
| `S-018.md` | S-018 | 2026-09-03 | `9a52cfa` | `R-018.md` | Con hallazgos (3) | F-045, F-046, F-047 |

---

## Convenciones

| Campo | Valores posibles |
|---|---|
| Informe | `S-XXX.md`, lo escribe el cierre de sesion |
| Commit auditado | el hash corto del commit que contiene ese informe |
| Auditoria | `R-XXX.md`, o `Pendiente` si todavia no se ha auditado |
| Veredicto | `Pendiente` / `Sin hallazgos` / `Con hallazgos (N)` |
| Hallazgos | los codigos `F-NNN` que abrio esa auditoria, o `-` |

🔑 **El emparejamiento es 1:1.** Cada `R-XXX.md` audita exactamente un `S-XXX.md`, sobre el commit
que lo contiene. Sin ese anclaje la auditoria juzga un relato: con el, cada afirmacion del informe
se puede contrastar contra el `git show` de ese commit.

🚨 **`Pendiente` es lo que escribe el cierre; el veredicto lo escribe la auditoria.** El cierre no
puede saber que va a encontrar alguien que todavia no ha mirado.

⚠️ **El commit auditado no lo escribe el cierre**, y no es un olvido: la fila se escribe **antes**
del commit que la contiene. Lo rellena la auditoria, que ya lo tiene delante:

```bash
git log -1 --format=%h -- _audit/S-XXX.md
```

🚨 **Una fila con `Auditoria: Pendiente` y mas de una sesion de antiguedad es una auditoria que no
se corrio.** El arranque la reporta arriba del todo. Un paso obligatorio cuyo olvido no deja huella
se olvida.
