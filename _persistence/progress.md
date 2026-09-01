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
| [S-004](#s-004---se-acepta-f-007-y-se-paga-dt-001-renombrado-de-techdebtmd) | Se acepta `F-007` y se paga `DT-001` (renombrado de `techdebt.md`) | 2026-09-01 | `000_preproject` |
| [S-005](#s-005---se-evaluan-f-005-a-f-010-nace-_phases-y-se-declara-005_discovery) | Se evaluan `F-005` a `F-010`, nace `_phases/` y se declara `005_discovery` | 2026-09-01 | `000_preproject` |
| [S-006](#s-006---se-aceptan-f-011-a-f-014-y-f-010-se-desatasca-con-d-027-nace-_methodology) | Se aceptan `F-011` a `F-014` y `F-010` se desatasca con `D-027`; nace `_methodology/` | 2026-09-02 | `000_preproject` |

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
| Ultima actualizacion | 2026-09-02 (S-006) |
| Salud | En marcha |
| Avance de la etapa | `R-005` (sobre `510d580`) abrio `F-011`, `F-012`, `F-013` y `F-014`. `manager` los evaluo contra `HEAD` (`a800d6b`) y los acepto todos: `T-014` ancla los dos recuentos sobre `HEAD` sin fecha de `A-001` y `T-012`; `T-015` propaga a los tres sitios que enuncian la regla la segunda excepcion de escritura de `manager` sobre `tasks.md`, reconociendola por su cita (`D-XXX`/`F-NNN`) y no por su numero; `T-016` anota en `D-023` que `D-026` ya amplio el ambito del Paso 1b, y corrige ademas la descripcion del ambito anterior; `T-017` corrige el recuento de hallazgos de `progress.md` en sus tres apariciones. De paso se desatasco `F-010` (`R-004`, seguia `Aceptado — pendiente` sin que nadie pudiera tocar el texto senalado): nace `D-027` —el texto que senala un hallazgo aceptado lo corrige `manager`, aunque el archivo sea de otro agente, con limites explicitos— y con ella `T-018` corrige la convencion viva de `_audit/findings.md`. Se dio ademas mecanismo a `D-022`, que llevaba desde `S-005` sin nada que la aplicara: `T-019` anade al Paso 6 de `protocol-close` la comprobacion del ambito temporal de los bloques de verificacion. Se registro `L-009` (un hallazgo acota su ejemplo, no el defecto). Por separado, el usuario aporto `_methodology/` —el metodo de desarrollo consolidado (`000_method.md`) y sus tres fuentes intactas (`sources/`)—: entra al repositorio como carpeta agnostica dentro del control de fuga del Paso 1b (`D-028`), se declara como guia de metodo vigente que no declara etapas del proyecto (`D-029`), sus codigos de producto en colision se renombran a `FT-`/`SC-` (`D-030`), y el Gate del metodo pasa a exigir dos firmas —veredicto tecnico de `report_auditor`, declaracion del usuario— en vez de una terminal auditora (`D-031`). Se registro `C-007` (las fuentes de la guia no se editan). |
| Bloqueos activos | El alcance y el objetivo del proyecto no estan definidos (`T-001`, etapa `005_discovery`); las etapas posteriores a `005_discovery` no estan declaradas (`T-002`, idem); `A-003` — si el historico de la fuente oficial es obtenible — sigue sin verificar y de el depende el ciclo entero del producto (`T-003`) |

---

## 2. Ultimo realizado

`manager` evaluo los cuatro hallazgos abiertos por `R-005` (`F-011`, `F-012`, `F-013`, `F-014`),
verificando cada uno contra `HEAD` (`a800d6b`) antes de aceptarlo, y los acepto todos: `T-014`
ancla a su hash los dos recuentos sobre `HEAD` sin fecha de la nota de `A-001` y de `T-012`;
`T-015` propaga a los tres sitios que enuncian la regla la segunda excepcion de escritura de
`manager` sobre `tasks.md` (`D-025`), y la hace reconocible por su cita en vez de por su numero de
filas; `T-016` anota bajo `D-023` que `D-026` ya amplio el ambito del Paso 1b, y corrige ademas que
la advertencia original describia mal el ambito anterior; `T-017` corrige el recuento de hallazgos
del «Avance de la etapa» de `progress.md` en sus tres apariciones, con un tercer error de conteo
que el propio `F-014` no nombraba. Los cuatro barridos de correccion se registran en `L-009` (un
hallazgo acota su ejemplo, no el defecto).

De paso se desatasco `F-010` (abierto por `R-004`, seguia `Aceptado — pendiente` sin que nadie
pudiera corregir el texto que senalaba: el auditor tiene prohibido corregir y `manager` tenia
prohibido escribir en `_audit/findings.md` mas alla de la fila de estado). Nace `D-027` —el texto
que senala un hallazgo aceptado lo corrige `manager`, aunque el archivo pertenezca a otro agente,
con limites explicitos sobre que se puede tocar—, y con ella `T-018` corrige la unica linea de la
convencion viva de `_audit/findings.md` que citaba el nombre antiguo de `techdebt.md`. Se dio
tambien mecanismo a `D-022` (`T-019`): el Paso 6 de `protocol-close` gana la comprobacion del
ambito temporal de los bloques de verificacion, que hasta ahora vivia solo como regla sin nada que
la aplicara.

Por separado, el usuario aporto `_methodology/`: el metodo de desarrollo consolidado
(`000_method.md`) y las tres fuentes de las que se consolido (`sources/`, intactas por `C-007`).
Entra al repositorio como carpeta agnostica y dentro del ambito del Paso 1b (`D-028`); se declara
guia de metodo vigente que **no** declara ninguna etapa del proyecto —las declaradas siguen siendo
las dos de `project.md`— (`D-029`); sus codigos de producto propuestos colisionaban con `F-NNN` y
`S-XXX` del registro, asi que se renombran a `FT-` y `SC-` dentro del documento, sin tocar el
registro ya auditado (`D-030`); y la seccion del Gate, que asignaba el veredicto a una terminal
auditora de un esquema ya revocado (`D-012`), pasa a exigir dos firmas —veredicto tecnico de
`report_auditor`, Gate declarado por el usuario— (`D-031`).

---

## 3. Siguiente paso

`manager` debe lanzar `report_auditor` sobre el commit de este cierre. En paralelo, definir el
alcance y el objetivo del proyecto a partir de `_brief/client_brief.md` (`T-001`, etapa
`005_discovery`), que es lo que de verdad abre esa etapa — nombrarla no la empieza.

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

### S-004 - Se acepta `F-007` y se paga `DT-001` (renombrado de `techdebt.md`)
| Campo | Valor |
|---|---|
| Fecha | 2026-09-01 |
| Etapa | `000_preproject` |
| Tareas | T-008 |

- **Que se hizo:** `manager` evaluo `F-007` (`R-003` sobre `S-003`), lo verifico contra `HEAD`
  (`ea0b850`) y lo acepto: registro `T-008` con `Origen: report_auditor` y escribio la excepcion de
  `D-020` **dentro de la convencion de `tasks.md`**, reflejandola tambien en `protocol-close` y en
  `session-closer.md`. El usuario confirmo que `manager` debe escribir esa `T-XXX` al aceptar un
  hallazgo, y esa confirmacion cierra la tension que `D-020` habia dejado declarada. En la misma
  peticion, el usuario pidio pagar `DT-001`: `_persistence/debtec.md` se renombro a
  `_persistence/techdebt.md` con `git mv`, y se reescribieron sus referencias vivas en los tres
  skills, `session-closer.md`, `CLAUDE.md`, `project.md` y la tabla de estructura de `progress.md`
  (`D-021`). `DT-001` pasa a `Confirmada`/`Implementada`. Se registro `L-007` (una excepcion se
  escribe donde esta la regla, no donde se decidio).
- **Que quedo abierto:** `T-001`, `T-002` y `T-003` siguen `No implementada`. `F-005` y `F-006` de
  `R-003` siguen `Abierto`, sin evaluar esta sesion.

---

### S-005 - Se evaluan `F-005` a `F-010`, nace `_phases/` y se declara `005_discovery`
| Campo | Valor |
|---|---|
| Fecha | 2026-09-01 |
| Etapa | `000_preproject` |
| Tareas | T-009, T-010, T-011, T-012, T-013 |

- **Que se hizo:** `manager` evaluo los seis hallazgos abiertos por `R-003` y `R-004` (`F-005`,
  `F-006`, `F-008`, `F-009`, `F-010`), verifico cada uno contra `HEAD` (`e61454b`) y los acepto
  todos. Los seis son el mismo defecto: un recuento tomado durante la jornada, presentado como si
  valiera sobre el commit que lo contendria. Se corrigieron por nota fechada sin reescribir el
  bloque original (`D-019`): `T-009` (observacion de `A-001`, que ademas rehace la señal 2 —«sesion
  sin auditar»— para que sea disparable), `T-010` (nota de `D-016`), `T-011` (bloque de `D-021`),
  `T-012` (criterio de cierre de `DT-001`) y `T-013` (alcance historico de `D-021`, que dejaba fuera
  del barrido las convenciones vivas de `_audit/findings.md`; la correccion del texto de esa linea
  queda pendiente del propio `report_auditor`). Se registro `D-022` (regla general: un recuento de
  ambito global se fecha, nunca se declara reproducible sobre su propio commit) y `L-008` (una
  leccion sin mecanismo que la aplique no evita la reincidencia — tres hallazgos del mismo patron en
  tres sesiones, con `L-006` ya escrita en las tres).

  Por separado, el usuario aporto una guia externa de otro metodo y pidio escribir con ella como
  forma —no como contenido— el archivo de la etapa en curso: nace `_phases/000_preproject.md`
  (`D-023`), agnostico, sin datos del proyecto ni codigos instanciados. Ese archivo deja escrito que
  `000_preproject` **no define alcance ni objetivo**, lo que dejo sin etapa a `T-001` y `T-002`
  (nacidas ahi por no haber otra declarada). El usuario decidio: declarar `005_discovery` como etapa
  siguiente (`D-024`); anadir el campo `Etapa`, obligatorio, a `tasks.md` —ficha e indice— y mover
  ahi las dos tareas (`D-025`); y ampliar el ambito del control de fuga del Paso 1b a `_phases/`
  (`D-026`), en `protocol-close` y en `protocol-audit`.
🕒 **Nota anadida el 2026-09-02 (`S-006`), tras el hallazgo `F-014` de `R-005`.** El texto de
arriba **se deja tal cual se escribio** —la bitacora es historico—, pero **el recuento es erroneo:
fueron cinco hallazgos, no seis**. `R-003` abrio tres (`F-005`, `F-006`, `F-007`) y `R-004` abrio
tres (`F-008`, `F-009`, `F-010`); `F-007` ya se habia aceptado y corregido en `S-004` (`T-008`), asi
que al abrirse `S-005` quedaban cinco sin evaluar — los cinco que la propia frase enumera, y las
cinco tareas que produjo (`T-009`..`T-013`).

```
$ sed -n '14,15p' _audit/index.md
| `S-003.md` | S-003 | 2026-09-01 | `ea0b850` | `R-003.md` | Con hallazgos (3) | F-005, F-006, F-007 |
| `S-004.md` | S-004 | 2026-09-01 | `c70b757` | `R-004.md` | Con hallazgos (3) | F-008, F-009, F-010 |

$ grep -cE "^[|] Sesion [|] S-005 [|]" _persistence/tasks.md
5
```

⚠️ **`F-014` señalo la frase de la seccion 1; el mismo error estaba en tres sitios.** Los dos
reescribibles —secciones 1 y 2, que el cierre sobrescribe— quedaron corregidos; este, que es
historico, lleva esta nota. **Que un hallazgo acote su ejemplo no acota el defecto:** la correccion se
barre entera antes de darla por hecha.

- **Que quedo abierto:** `T-001`, `T-002` y `T-003` siguen `No implementada`. `D-022` deja sin
  resolver, y anotado en su propio texto, si la regla que enuncia debe llevarse a `CLAUDE.md` o a
  `protocol-close` — no tiene todavia un codigo propio que lo agende.

---

### S-006 - Se aceptan `F-011` a `F-014`, `F-010` se desatasca con `D-027`; nace `_methodology/`
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Etapa | `000_preproject` |
| Tareas | T-014, T-015, T-016, T-017, T-018, T-019 |

- **Que se hizo:** `manager` evaluo los cuatro hallazgos abiertos por `R-005` sobre `S-005`
  (`F-011`, `F-012`, `F-013`, `F-014`), verifico cada uno contra `HEAD` (`a800d6b`) y los acepto
  todos. `T-014` ancla a `e61454b` los dos recuentos sobre `HEAD` sin fecha de la nota de `A-001` y
  de la ficha de `T-012` (las cifras eran correctas; faltaba el ancla). `T-015` propaga a los tres
  sitios que enuncian la regla la segunda excepcion de escritura de `manager` sobre `tasks.md`
  (`D-025`), y la redefine por su cita —un `D-XXX` o un `F-NNN` en la propia tarea— en vez de por
  numero de filas, criterio propuesto por la propia auditoria. `T-016` anota bajo `D-023` que
  `D-026` ya amplio el ambito del Paso 1b, y corrige ademas que la advertencia original describia
  mal el ambito anterior (decia tres rutas donde habia dos). `T-017` corrige el recuento de
  hallazgos del «Avance de la etapa» y de «Ultimo realizado» de `progress.md`, y anota por nota
  fechada el mismo error en la bitacora de `S-005` (historico, `D-019`); ademas de lo que `F-014`
  citaba, aparecio un tercer error de conteo («evaluo los seis» cuando fueron cinco) y el mismo
  fallo repetido en tres secciones, no una. Los cuatro barridos completos —no solo la cita literal
  de cada hallazgo— quedan registrados en `L-009`.

  De paso se desatasco `F-010` (`R-004`, seguia `Aceptado — pendiente` desde `S-005` sin que nadie
  pudiera corregir el texto senalado: prohibido para el auditor, fuera del mandato de `manager`).
  `D-027` decide que el texto que senala un hallazgo aceptado lo corrige `manager`, aunque el
  archivo sea de otro agente, con limites explicitos —registro vivo si, documentos entregados no—;
  `T-018` aplica esa autorizacion y corrige la unica linea de la seccion «Convenciones» de
  `_audit/findings.md` que citaba el nombre ya renombrado de `techdebt.md`. Y se le dio mecanismo a
  `D-022`, que desde `S-005` no tenia nada que la aplicara: `T-019` anade al Paso 6 de
  `protocol-close` la comprobacion del ambito temporal de los bloques de verificacion.

  Por separado, el usuario aporto `_methodology/`: `000_method.md` (documento canonico del metodo
  de desarrollo) y `sources/` (las tres fuentes de las que se consolido, intactas por `C-007`).
  Entra al repositorio como carpeta agnostica y dentro del ambito del Paso 1b (`D-028`); se declara
  guia de metodo vigente que no declara ninguna etapa del proyecto (`D-029`); sus codigos de
  producto propuestos —que colisionaban con `F-NNN` y `S-XXX` del registro— se renombran a `FT-` y
  `SC-` dentro del documento (`D-030`); y la seccion del Gate, que asignaba el veredicto a una
  terminal auditora de un esquema ya revocado (`D-012`), pasa a exigir dos firmas: veredicto
  tecnico de `report_auditor` y Gate declarado por el usuario (`D-031`).
- **Que quedo abierto:** `T-001`, `T-002` y `T-003` siguen `No implementada`. `F-010`, `F-011`,
  `F-012`, `F-013` y `F-014` quedan `Aceptado — pendiente` hasta que la auditoria siguiente
  verifique la correccion sobre este commit y los cierre.

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
| `techdebt.md` | Deuda tecnica del proyecto | `DT-XXX` |
