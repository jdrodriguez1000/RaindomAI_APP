# progress.md

> **Archivo principal del proyecto.** Da la vision general: como va el proyecto, cual es el
> avance, que es lo ultimo realizado y cual es el siguiente paso.
> **No detalla tareas** — el detalle de tareas vive en `tasks.md`.

---

## Indice

| Seccion | Contenido |
|---|---|
| [1. Estado general](#1-estado-general) | Etapa actual, salud del proyecto, avance |
| [2. Ultimo realizado](#2-ultimo-realizado) | Lo mas reciente que quedo terminado |
| [3. Siguiente paso](#3-siguiente-paso) | Que sigue ahora |
| [4. Hitos](#4-hitos) | Hitos del proyecto y su estado |
| [5. Bitacora](#5-bitacora) | Sesiones `S-XXX` (una jornada cada una, no un dia) |
| [6. Mapa de persistencia](#6-mapa-de-persistencia) | Que se registra en cada archivo |

### Sesiones

> Una sesion es una **jornada** de trabajo (manana, tarde, noche o dia completo). Puede haber
> varias en la misma fecha; cada una lleva su propio `S-XXX`.

| Codigo | Sesion | Fecha | Etapa |
|---|---|---|---|
| [S-001](#s-001---primer-cierre-se-monta-la-forma-de-trabajar) | Primer cierre: se monta la forma de trabajar | 2026-08-31 | `000_preproject` |
| [S-002](#s-002---rename-del-agente-de-auditoria-y-nuevas-reglas-de-claudemd) | Rename del agente de auditoria y nuevas reglas de `CLAUDE.md` | 2026-08-31 | `000_preproject` |
| [S-003](#s-003---se-evaluan-y-registran-los-cuatro-hallazgos-de-r-002) | Se evaluan y registran los cuatro hallazgos de `R-002` | 2026-09-01 | `000_preproject` |

---

## Convenciones

| Campo | Valores posibles |
|---|---|
| Codigo de sesion | `S-XXX`, correlativo, no se reutiliza |
| Codigo de hito | `H-nn`, correlativo, no se reutiliza |
| Salud | `En marcha` / `Bloqueado` / `En riesgo` / `Detenido` |
| Estado de hito | `Pendiente` / `En curso` / `Alcanzado` / `Cancelado` |

🚨 **Este archivo no se escribe a mano durante la jornada.** Lo produce el cierre de sesion, junto
con `tasks.md`. Escribirlo sobre la marcha hace que diga lo que se penso hacer y no lo que se hizo.

🚨 **El indice de sesiones se escribe a mano, sin generador.** Cada fila enlaza por ancla a su
entrada en la [Bitacora](#5-bitacora).

---

## 1. Estado general

| Campo | Valor |
|---|---|
| Etapa actual | `000_preproject` |
| Ultima actualizacion | 2026-09-01 (S-003) |
| Salud | En marcha |
| Avance de la etapa | El commit `c575bc0` (auditoria `R-002` sobre `S-002`) dejo cuatro hallazgos abiertos (`F-001`..`F-004`). En esta sesion `manager` los evaluo, verifico cada uno contra `HEAD` y los acepto los cuatro: registro `T-004`..`T-007` con `Origen: report_auditor`, corrigio la fuga de dos identificadores `auditor` vivos, acoto por nota fechada el enunciado del bloque de verificacion de `D-016`, devolvio `DT-001` a `Propuesta (pendiente del usuario)` y corrigio la tabla de actores de `session-closer.md`. Quedaron dos decisiones nuevas (`D-019`, `D-020`) y una leccion nueva (`L-006`). Sigue pendiente el trabajo de producto: `T-001`, `T-002`, `T-003`. |
| Bloqueos activos | El alcance y el objetivo del proyecto no estan definidos (`T-001`); las etapas posteriores a `000_preproject` no estan declaradas (`T-002`); `A-003` — si el historico de la fuente oficial es obtenible — sigue sin verificar y de el depende el ciclo entero del producto (`T-003`); `DT-001` sigue esperando la confirmacion del usuario |

---

## 2. Ultimo realizado

`manager` evaluo los cuatro hallazgos que dejo `R-002` sobre `S-002` (`F-001`..`F-004`), verificando
cada uno contra `HEAD` antes de aceptarlo (los cuatro se aceptaron, ninguno se rechazo). Se
registraron `T-004`..`T-007` con `Origen: report_auditor`, y sobre cada uno:

- `F-001` — el bloque de verificacion de `D-016` afirmaba «cero identificadores `auditor` vivos» sin
  acotar ambito; se le anadio debajo una nota fechada que acota el ambito real y aporta el barrido
  completo (`D-019`: un bloque de verificacion antiguo se corrige por nota, nunca reescribiendolo).
- `F-002` — las dos referencias vivas al handle `auditor` que ese ambito estrecho no cubria
  (`_audit/findings.md:3` y un ejemplo en `_persistence/tasks.md`) se corrigieron a `report_auditor`.
- `F-003` — `DT-001` volvio de `Confirmada` a `Propuesta (pendiente del usuario)`: ese valor lo
  habia escrito el cierre de `S-002`, y el Paso 5 de `protocol-close` se lo prohibe.
- `F-004` — la tabla de actores de `session-closer.md` describia a `report_auditor` en «su propio
  repositorio», resto del esquema que `D-012` revoco; ahora nombra lo que escribe de verdad.

Ademas: `L-006` (un bloque de verificacion declara su ambito dentro del enunciado), `D-020` (`manager`
escribe en `tasks.md` al registrar un hallazgo de auditoria, por mandato de `CLAUDE.md`), y una
observacion nueva en `A-001` (primera senal a favor del supuesto, con material real de `R-002`).

---

## 3. Siguiente paso

Definir el alcance y el objetivo del proyecto a partir de `_brief/client_brief.md` (`T-001`), que es
lo que abre la etapa siguiente a `000_preproject`. En paralelo, `manager` debe lanzar `report_auditor`
sobre el commit de este cierre, y pedir al usuario que confirme o rechace `DT-001` (`F-003`).

---

## 4. Hitos

| Codigo | Hito | Estado | Fecha |
|---|---|---|---|
| — | — | — | — |

---

## 5. Bitacora

<!--
Plantilla:

### S-XXX - Titulo de la sesion
| Campo | Valor |
|---|---|
| Fecha | AAAA-MM-DD |
| Etapa | |
| Tareas | T-XXX, T-XXX |

- **Que se hizo:** resumen de la jornada.
- **Que quedo abierto:** lo que sigue pendiente al cerrar.
-->

### S-001 - Primer cierre: se monta la forma de trabajar
| Campo | Valor |
|---|---|
| Fecha | 2026-08-31 |
| Etapa | `000_preproject` |
| Tareas | T-001, T-002, T-003 |

- **Que se hizo:** se construyo desde cero el andamiaje de trabajo del proyecto: los siete archivos
  de `_persistence/`, `project.md`, `CLAUDE.md`, `.gitignore`, y el ciclo de sesion completo con tres
  agentes y tres skills (`session-starter`/`protocol-start`, `session-closer`/`protocol-close`,
  `auditor`/`protocol-audit`), mas `_audit/` con su tablero (`index.md`) y su registro de hallazgos
  (`findings.md`). El material de partida vino de un proyecto anterior aportado como guia en
  `temporal/`: se adopto la forma (`D-001`, `D-002`) y se descarto el contenido. A mitad de jornada
  se revoco el esquema de dos terminales ya construido y se sustituyo por auditoria mediante un
  agente en este mismo repositorio (`D-012`, que revoca `D-008`), lo que obligo a reescribir
  material y a renombrar el rol `executor` a `manager` (`D-010`). Los cuatro archivos del porque
  quedaron escritos: 15 decisiones, 4 restricciones, 3 supuestos y 4 lecciones. Es el primer commit
  de este repositorio.
- **Que quedo abierto:** el alcance y el objetivo del proyecto no estan definidos — existe
  `_brief/client_brief.md` con el encargo del cliente, pero un encargo no es una decision (`T-001`).
  Las etapas posteriores a `000_preproject` no estan declaradas (`T-002`). `A-003` — si el historico
  de la fuente oficial es obtenible — sigue sin verificar, y de el depende el ciclo entero del
  producto (`T-003`).

---

### S-002 - Rename del agente de auditoria y nuevas reglas de `CLAUDE.md`
| Campo | Valor |
|---|---|
| Fecha | 2026-08-31 |
| Etapa | `000_preproject` |
| Tareas | — (sin tareas de `tasks.md` cerradas esta sesion) |

- **Que se hizo:** dos encargos del usuario. (1) Rename completo del agente `auditor` a
  `report_auditor`: archivo, `name:` del frontmatter, y todas las referencias vivas —`CLAUDE.md`,
  `project.md`, los tres skills, los otros dos agentes, y el valor de campo `Origen: auditor` en los
  seis archivos de `_persistence/`— (`D-016`). Verificado con el comando de la seccion de
  verificacion de `D-016` (`git grep` sobre `.claude`, `CLAUDE.md` y `project.md` buscando
  identificadores de `auditor` entre backticks, en negrita, o como `Origen:`/`agente auditor`):
  cero coincidencias. Lo historico —`A-001`, `D-012`, `_audit/S-001.md`, `_audit/R-001.md`, la
  narrativa de `progress.md`— se dejo sin tocar. (2) Se añadio a `CLAUDE.md` una seccion «Idioma»
  (`D-017`, `C-005`) y las secciones «Principios de ingenieria» (`PI-1`..`PI-5`) y «Reglas de
  operacion» (`D-018`, `C-006`), a partir de texto aportado por el usuario. `PI-5` se adapto con dos
  casillas —test en verde para codigo, bloque de verificacion para documentacion— en vez de dejarlo
  literal, decision del usuario. `debtec.md` quedo registrado como la unica excepcion conocida a la
  regla de idioma (`DT-001`, `Confirmacion: Confirmada`).
- **Que quedo abierto:** `T-001`, `T-002` y `T-003` siguen `No implementada`, sin tocar esta sesion.
  `DT-001` (renombrar `debtec.md` a `techdebt.md`) sigue sin pagarse.

---

### S-003 - Se evaluan y registran los cuatro hallazgos de `R-002`
| Campo | Valor |
|---|---|
| Fecha | 2026-09-01 |
| Etapa | `000_preproject` |
| Tareas | T-004, T-005, T-006, T-007 |

- **Que se hizo:** `manager` evaluo los cuatro hallazgos abiertos por `R-002` sobre `S-002`
  (`F-001`..`F-004`), verificando cada uno contra `HEAD` (`c575bc0`) antes de aceptarlo. Los cuatro
  se aceptaron: `T-004` acoto por nota fechada el enunciado del bloque de verificacion de `D-016`
  sin reescribir el comando ya ejecutado (`D-019`); `T-005` corrigio los dos identificadores
  `auditor` vivos que ese ambito estrecho dejo fuera (`_audit/findings.md:3` y un ejemplo de
  `_persistence/tasks.md`); `T-006` devolvio `DT-001` de `Confirmada` a
  `Propuesta (pendiente del usuario)`, valor que el Paso 5 de `protocol-close` prohibe escribir al
  `session-closer`; `T-007` corrigio la tabla de actores de `.claude/agents/session-closer.md`, que
  describia a `report_auditor` en «su propio repositorio» (resto del esquema que `D-012` revoco).
  Se registro ademas `L-006` (un bloque de verificacion declara su ambito dentro del enunciado),
  `D-020` (`manager` escribe en `tasks.md` al registrar un hallazgo de auditoria) y una observacion
  nueva en `A-001`, primera senal a favor del supuesto con material real. Las cuatro filas de
  `_audit/findings.md` pasaron de `Abierto` a `Aceptado — pendiente`, citando su `T-XXX`.
- **Que quedo abierto:** `T-001`, `T-002` y `T-003` siguen `No implementada`. `DT-001` sigue sin la
  confirmacion del usuario (ahora correctamente marcada como pendiente). Los cuatro hallazgos
  quedan `Aceptado — pendiente` hasta que una auditoria posterior verifique la correccion sobre este
  commit y los cierre.

---

## 6. Mapa de persistencia

| Archivo | Registra | Codigo |
|---|---|---|
| `progress.md` | Vision general, avance, ultimo hecho, siguiente paso | `S-XXX` sesiones, `H-nn` hitos |
| `tasks.md` | Tareas realizadas y por realizar | `T-XXX` |
| `decisions.md` | Decisiones tomadas en el proyecto | `D-XXX` |
| `constraints.md` | Limitaciones y restricciones del proyecto | `C-XXX` |
| `assumptions.md` | Supuestos vigentes por validar | `A-XXX` |
| `lessons.md` | Lecciones aprendidas durante la ejecucion | `L-XXX` |
| `debtec.md` | Deuda tecnica del proyecto | `DT-XXX` |
