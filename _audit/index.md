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
| `S-019.md` | S-019 | 2026-09-03 | `1b30e16` | `R-019.md` | Con hallazgos (3) | F-048, F-049, F-050 |
| `S-020.md` | S-020 | 2026-09-04 | `3ff670e` | `R-020.md` | Con hallazgos (4) | F-051, F-052, F-053, F-054 |
| `S-021.md` | S-021 | 2026-09-05 | `76a2cb6` | `R-021.md` | Con hallazgos (4) | F-055, F-056, F-057, F-058 |
| `S-022.md` | S-022 | 2026-09-06 | `97bb948` | `R-022.md` | Con hallazgos (3) | F-059, F-060, F-061 |
| `S-023.md` | S-023 | 2026-09-06 | `b83ce5e` | `R-023.md` | Con hallazgos (4) | F-062, F-063, F-064, F-065 |
| `S-024.md` | S-024 | 2026-09-07 | `a1f5fa8` | `R-024.md` | Con hallazgos (4) | F-066, F-067, F-068, F-069 |
| `S-025.md` | S-025 | 2026-09-07 | `f1f2291` | `R-025.md` | Con hallazgos (4) | F-070, F-071, F-072, F-073 |
| `S-026.md` | S-026 | 2026-09-07 | `d1a8c02` | `R-026.md` | Con hallazgos (2) | F-074, F-075 |
| `S-027.md` | S-027 | 2026-09-07 | `79e88a2` | `R-027.md` | Con hallazgos (4) | F-076, F-077, F-078, F-079 |
| `S-028.md` | S-028 | 2026-09-08 | `5ba9c4e` | `R-028.md` | Con hallazgos (3) | F-080, F-081, F-082 |
| `S-029.md` | S-029 | 2026-09-08 | `c1fb41e` | `R-029.md` | Con hallazgos (4) | F-083, F-084, F-085, F-086 |

> 📌 **Nota del 2026-09-06 (`F-060`, sesion S-023).** La columna `Fecha` de este tablero **no
> coincide con la fecha del commit** en ocho de las veintidos filas. `F-060` lo abrio sobre `S-021` y
> `S-022`; el barrido completo, corrido al evaluarlo, ensena que el desfase venia de antes. Ninguna
> fila se reescribe — estan todas auditadas, y cambiarles la fecha convertiria «falta exactitud» en
> «hay exactitud falsa». Lo que se corrige es la regla, hacia adelante: `D-093` y el Paso 7d de
> `protocol-close`.
>
> ```
> $ awk -F'|' '/^\| `S-[0-9]+\.md`/{gsub(/[ `]/,"",$4); gsub(/[ `]/,"",$5); if($5!="") printf "%s %s\n",$5,$4}' _audit/index.md \
>     | while read h f; do
>         c=$(git log -1 --format=%ad --date=short "$h" 2>/dev/null)
>         [ "$c" = "$f" ] || echo "$h tablero=$f commit=$c"
>     done
> d906a5d tablero=2026-09-02 commit=2026-09-01
> 122b770 tablero=2026-09-02 commit=2026-09-01
> f096fff tablero=2026-09-02 commit=2026-09-01
> fc91957 tablero=2026-09-02 commit=2026-09-01
> ca56b93 tablero=2026-09-03 commit=2026-09-02
> bd8a9ff tablero=2026-09-03 commit=2026-09-02
> 76a2cb6 tablero=2026-09-05 commit=2026-09-04
> 97bb948 tablero=2026-09-06 commit=2026-09-04
> ```
>
> ⚠️ **La orden se corre sobre el arbol de trabajo a proposito**, porque interroga a este
> mismo archivo tal como esta hoy; anclarla a un commit anterior mediria un tablero mas corto.

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
del commit que la contiene. Lo rellena la auditoria, que ya lo tiene delante — y lo que escribe es
**el hash literal de la cabecera del informe**, el mismo que acaba de auditar.

🚨 **No se deriva con `git log -1 --format=%h -- _audit/S-XXX.md`.** Cuando el cierre ancla el
informe con un segundo commit, esa orden devuelve **el commit de anclaje** —que lleva un solo
archivo— y no el commit de la sesion, que es el que la auditoria juzgo. Una fila que publique el de
anclaje manda a quien la lea a un estado que no es el que se juzgo. Lo fija `D-090`, y el
procedimiento vive en `protocol-audit`.

📌 **Esa orden sigue sirviendo para una cosa, y conviene saber cual:** dice **si hubo commit de
anclaje** y cual es. Como dato de historial vale; como fuente de la columna, no.

🚨 **Una fila con `Auditoria: Pendiente` y mas de una sesion de antiguedad es una auditoria que no
se corrio.** El arranque la reporta arriba del todo. Un paso obligatorio cuyo olvido no deja huella
se olvida.
