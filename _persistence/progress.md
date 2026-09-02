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
| [S-007](#s-007---se-aceptan-f-015-y-f-016-nace-_phases005_discoverymd) | Se aceptan `F-015` y `F-016`; nace `_phases/005_discovery.md` | 2026-09-02 | `000_preproject` |
| [S-008](#s-008---se-aceptan-f-017-a-f-019-nacen-las-plantillas-de-_templates005_discovery) | Se aceptan `F-017` a `F-019`; nacen las plantillas de `_templates/005_discovery/` | 2026-09-02 | `000_preproject` |
| [S-009](#s-009---se-aceptan-f-020-a-f-023-los-artefactos-se-mudan-a-005_discovery-nace-_workflow) | Se aceptan `F-020` a `F-023`; los artefactos se mudan a `005_discovery/`; nace `_workflow/` | 2026-09-02 | `000_preproject` |
| [S-010](#s-010---se-aceptan-f-024-a-f-026-nace-_workflow005_discoverymd) | Se aceptan `F-024` a `F-026`; nace `_workflow/005_discovery.md` | 2026-09-02 | `000_preproject` |

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
| Ultima actualizacion | 2026-09-02 (S-010) |
| Salud | En marcha |
| Avance de la etapa | `R-009` (sobre `99c3aa3`) abrio `F-024`, `F-025` y `F-026`. `manager` verifico los tres contra `HEAD` (`99c3aa3`) antes de aceptarlos, y los acepto los tres. `D-050` resuelve `F-024`: la correccion que `T-028` hizo en la celda «Avance de la etapa» no sobrevivio al cierre que la sobrescribe entera, asi que se trata como resuelto por desaparicion — `T-028` pasa a `Cancelada` y `T-032` deja nota fechada en los tres registros que afirmaban la nota inexistente (`L-015`). `T-033` ancla con nota fechada los bloques de verificacion de `D-043` y `D-044`, que `F-025` señalo sin reproducirse sobre su propio commit. `T-034` corrige en `techdebt.md` la cita cruzada `L-013` → `L-014` que `F-026` señalo. Por pedido del usuario, `_workflow/` gana un archivo por etapa declarada (`D-051`): nace `_workflow/005_discovery.md`, que aplica `team.md` y `ai_levels.md` a los siete pasos del procedimiento de la etapa y queda citado desde `_phases/005_discovery.md` — el cuarto enganche que `DT-002` reclamaba, aunque la deuda sigue `Propuesta (pendiente del usuario)`. `D-052` deja escrito que el reparto de `005_discovery` no se adopta todavia: se adopta con su `D-XXX` al abrir la etapa, no antes. |
| Bloqueos activos | El alcance y el objetivo del proyecto no estan definidos (`T-001`, etapa `005_discovery`, con entrada obligatoria explicita en `_phases/005_discovery.md`: sin acceso al patrocinador la etapa no puede empezar, `A-004`); las etapas posteriores a `005_discovery` no estan declaradas (`T-002`, idem); `A-003` — si el historico de la fuente oficial es obtenible — sigue sin verificar y de el depende el ciclo entero del producto (`T-003`) |

---

## 2. Ultimo realizado

`manager` evaluo los tres hallazgos abiertos por `R-009` sobre `S-009` (`F-024`, `F-025`, `F-026`),
verificando cada uno contra `HEAD` (`99c3aa3`) antes de aceptarlo, y los acepto los tres.

`F-024` tenia razon: `T-028` habia editado la celda «Avance de la etapa» de `progress.md` para
corregir el commit atribuido a `R-007`, pero el cierre sobrescribe esa celda entera en cada pasada
y la correccion desaparecio con el texto que corregia. `D-050` fija el tratamiento: `F-021` queda
resuelto **por desaparicion del texto**, no por correccion; `T-028` pasa de `Implementada` a
`Cancelada`, sin objeto de reintentarla; y `T-032` deja nota fechada en los tres registros que
afirmaban la nota inexistente —la propia viñeta de `F-021`, la bitacora de `S-009` y la ficha de
`T-028`—, sin reescribir ningun texto historico (`D-019`). La leccion queda en `L-015`: una
correccion escrita en una seccion que el cierre sobrescribe no es una correccion, es un borrador.

`T-033` atiende `F-025`: los bloques de verificacion de `D-043` y `D-044` se escribieron con
`git show HEAD:` sin anclar y no se reproducen sobre el commit que los contiene (`D-043` registraba
`16` donde `fc91957` da `23`; `D-044` registraba `exit=1` donde da ocho coincidencias). Se les añade
a cada uno una nota fechada con la orden anclada a un commit concreto y su salida cruda, sin tocar
el texto original — el mismo patron que `T-029` aplico a `D-036`, `D-038` y `D-040`.

`T-034` atiende `F-026`: el cuerpo de `DT-002` citaba `L-013` donde corresponde `L-014`. Se corrige
la cita, remision cruzada dentro del mismo registro.

Por pedido del usuario, `_workflow/` gana **un archivo por etapa declarada** (`D-051`): nace
`_workflow/005_discovery.md`, que aplica `team.md` y `ai_levels.md` a los siete pasos del
procedimiento de la etapa —una fila por paso—, y `_phases/005_discovery.md` queda editado para
mandar leerlo antes del Paso 1 de su procedimiento. Es el cuarto enganche que `L-014` y `DT-002`
señalaban como faltante, aunque la deuda **no se marca `Implementada`**: quien confirma que quedo
pagada es el usuario, no `manager`. `project.md` y `CLAUDE.md` se actualizan para describir el
archivo nuevo. `D-052` deja escrito, ademas, que el reparto que ese archivo permite **no se adopta
todavia**: se adopta con su propio `D-XXX` al abrir la etapa `005_discovery`, no antes, porque
adoptarlo hoy repartiria trabajo sobre entradas —el acceso de `A-004`— que aun no estan confirmadas.

---

## 3. Siguiente paso

`manager` debe lanzar `report_auditor` sobre el commit de este cierre. En paralelo, definir el
alcance y el objetivo del proyecto a partir de `_brief/client_brief.md` (`T-001`, etapa
`005_discovery`) — y antes de arrancarla, resolver `A-004`: confirmar que existe un patrocinador
alcanzable y personas que puedan hablar del proceso real, porque el propio archivo de etapa dice
que sin ese acceso no puede empezar. Al abrir `005_discovery`, registrar el `D-XXX` de adopcion del
reparto de `_workflow/005_discovery.md` que `D-052` deja pendiente —incluida la discrepancia de su
§6 con la tabla de lectura de `ai_levels.md` §6, y los `A-XXX` que el reparto de por ciertos sin
confirmar—. Aparte, es decision del usuario si `DT-002` se confirma ya como pagada ahora que el
cuarto enganche existe.

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

### S-007 - Se aceptan `F-015` y `F-016`; nace `_phases/005_discovery.md`
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Etapa | `000_preproject` |
| Tareas | T-020, T-021, T-022 |

- **Que se hizo:** `manager` evaluo los dos hallazgos abiertos por `R-006` sobre `S-006` (`F-015`,
  `F-016`), verifico cada uno contra `HEAD` (`111fc40`) y los acepto ambos. `T-020` escribe
  `_phases/005_discovery.md` —el archivo que `D-023` exige desde `S-005` y que tres sesiones
  nombraron sin agendar—, adaptado (no copiado) de la guia que aporto el usuario (`D-033`); resuelve
  de paso los codigos del descubrimiento (`N-XXX` nuevo; `A-XXX`/`C-XXX` ya existentes para
  supuestos y restricciones, `D-034`) y la ubicacion futura de sus plantillas
  (`_templates/005_discovery/`, sin crear todavia, `D-035`; abre `T-022`). `T-021` reescribe la
  apertura de la convencion de `tasks.md`, que anunciaba «una unica excepcion» cuatro parrafos
  despues de escribir la segunda; su barrido de correccion se acota a los tres sitios donde la
  regla se enuncia, no al repositorio entero, porque un barrido global nunca puede dar cero
  (`_audit/` y `T-015` citan el texto viejo para explicarse, y no se reescriben — `D-019`). Ambos
  criterios de cierre se verificaron contra el arbol de trabajo antes de marcar las tareas
  `Implementada`: `_phases/` contiene ya un archivo por cada etapa declarada en `project.md` y el
  control de fuga de datos propios del Paso 1b sigue en cero; el barrido acotado de `T-021` no deja
  ninguna variante viva de la regla vieja. Se registro `A-004` (acceso al patrocinador y a quienes
  conocen el proceso real, entrada obligatoria segun el propio archivo de etapa), `L-010` (un
  criterio de cierre cuyo ambito incluye el registro no puede cumplirse nunca) y `D-032` (las
  entradas de esta sesion se fechan `2026-09-02`, por continuidad con `S-006`/`R-006`, aunque el
  reloj del entorno marque `2026-09-01`).
- **Que quedo abierto:** `T-001`, `T-002` y `T-003` siguen `No implementada`. `A-004` sigue
  `Abierto`: no hay confirmacion de que exista acceso al patrocinador, y es entrada obligatoria
  para empezar `005_discovery`. `F-015` y `F-016` quedan `Aceptado — pendiente` hasta que la
  auditoria siguiente verifique la correccion sobre este commit y los cierre.

---

### S-008 - Se aceptan `F-017` a `F-019`; nacen las plantillas de `_templates/005_discovery/`
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Etapa | `000_preproject` |
| Tareas | T-022, T-023, T-024, T-025, T-026 |

- **Que se hizo:** `manager` evaluo los tres hallazgos abiertos por `R-007` sobre `S-007` (`F-017`,
  `F-018`, `F-019`), verifico cada uno contra `HEAD` (`ae06147`) y los acepto los tres. `T-023`
  añade a la ficha de `T-020` los dos bloques de verificacion que faltaban, anclados a `122b770`
  con nota fechada (patron de `T-014`). `T-024` acota la frase de `T-021` que afirmaba un barrido
  «sobre todo el repositorio» y añade el tercer bloque con ese barrido real, insensible a
  mayusculas, que encontro una coincidencia en `session-closer.md:90` que el patron original no
  alcanzaba (`L-012`); el fondo del hallazgo original seguia siendo correcto. `T-025` no reescribe
  `_audit/S-007.md` (`D-040`): la correccion de `F-019` va al mecanismo de `protocol-close`, cuya
  seccion 1 ahora exige la salida generada en vez de una lista redactada de memoria (`L-011`).
  Ademas se escriben las cuatro plantillas de `_templates/005_discovery/` (`T-022`), adaptadas de
  las que aporto el usuario (`D-041`); se decide donde viven los artefactos rellenos del
  descubrimiento (`_discovery/`, `D-036`); se decide no escribir la quinta plantilla —restricciones
  y supuestos—, remitiendola a `_persistence/`, que gana los campos `Dueño` y `Riesgo abierto`
  (`D-037`); entra el codigo `I-XXX` para interesado (`D-038`); `T-022` se reetiqueta a
  `000_preproject` (`D-039`); y `T-026` extiende el Paso 1b de `protocol-close` a `_templates/`.
  Las entradas de esta sesion se fechan `2026-09-02` por continuidad con el registro (`D-042`).
- **Que quedo abierto:** `T-001`, `T-002` y `T-003` siguen `No implementada`. `A-004` sigue
  `Abierto`. `F-017`, `F-018` y `F-019` quedan `Aceptado — pendiente` hasta que la auditoria
  siguiente verifique la correccion sobre este commit y los cierre.

---

### S-009 - Se aceptan `F-020` a `F-023`; los artefactos se mudan a `005_discovery/`; nace `_workflow/`
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Etapa | `000_preproject` |
| Tareas | T-027, T-028, T-029, T-030, T-031 |

- **Que se hizo:** `manager` evaluo los cuatro hallazgos abiertos por `R-008` sobre `S-008`
  (`F-020` a `F-023`), verifico cada uno contra `HEAD` (`7025a05`) y los acepto los cuatro.
  `T-027` borra en `_audit/findings.md` la viñeta residual de `F-017` que contradecia a la
  fechada. `T-028` corrige en `progress.md` el commit atribuido a `R-007` —`122b770`, no
  `ae06147`— con nota fechada. `T-029` no reescribe los tres bloques de verificacion de
  `decisions.md` desmentidos por `F-022` (`D-036`, `D-038`, `D-040`): añade una nota fechada con la
  orden que si se reproduce en cada uno, sin tocar el texto original (`L-013`). `T-030` registra en
  `D-044` la desviacion de `T-026` que `F-023` señalo, como caso puntual, sin abrir una tercera
  excepcion en la convencion de `tasks.md`. Por orden del usuario nace `D-045`, que revoca `D-036`:
  los artefactos rellenos del descubrimiento pasan de `_discovery/` a `005_discovery/`; `T-031`
  mueve los diecisiete sitios donde estaba escrita la ruta vieja. Nace `_workflow/` (`D-046`), con
  `team.md` y `ai_levels.md`, agnostica y enganchada en `project.md`, `CLAUDE.md` y el Paso 1b de
  `protocol-close` (`D-047`); la secuencia de fases del documento fuente del usuario no entra en el
  repositorio (`D-048`); se fija la frontera entre los dos archivos nuevos (`D-049`). Se registra
  `A-005`: la parte de `ai_levels.md` sin experiencia propia detras (harness, observabilidad,
  evaluaciones, rubricas, metricas) es un supuesto abierto, no un hecho comprobado.
- **Que quedo abierto:** `T-001`, `T-002` y `T-003` siguen `No implementada`. `A-004` y `A-005`
  siguen `Abierto`. `F-020` a `F-023` quedan `Aceptado — pendiente` hasta que la auditoria
  siguiente verifique la correccion sobre este commit y los cierre. `L-014` señala un cuarto
  enganche sin resolver para `_workflow/` —que algo mande leerla en el momento en que sirve—, dejado
  a proposito porque toca una decision del usuario sobre `_phases/`.

📌 **Nota del 2026-09-02 (`T-032`, hallazgo `F-024`): la nota fechada que esta bitacora da por
hecha no existe.** `T-028` si edito la celda, pero el cierre la sobrescribio entera en el mismo
commit y la correccion desaparecio con el texto que corregia. **El texto original no se
reescribe** (`D-019`). `F-021` queda resuelto por desaparicion, no por correccion, y `T-028`
pasa a `Cancelada` (`D-050`):

```
$ git show fc91957:_persistence/progress.md | grep -o 'R-007` (sobre `[0-9a-f]*`)' ; echo "exit=$?"
exit=1

$ git show fc91957 -- _persistence/progress.md | grep -n "^[+-].*ae06147" | cut -c1-60
43:-| Avance de la etapa | `R-007` (sobre `ae06147`) abrio `F-01
44:+| Avance de la etapa | `R-008` (sobre `f096fff`) abrio `F-02
52:-verificando cada uno contra `HEAD` (`ae06147`) antes de acept
80:+commit que la propia bitacora de `S-008` atribuia a `R-007` —
82:+`ae06147` de la misma celda, el `HEAD` contra el que se verif
135:+  `ae06147`— con nota fechada. `T-029` no reescribe los tres
```

El par `-`/`+` de las lineas 43 y 44 es la prueba: la celda entera sale y entra otra, no hay
correccion de la cadena. ⚠️ **La segunda orden de `F-024` —`grep -c`, que el hallazgo registra
en `0`— no se reproduce: devuelve `6`.** El fondo del hallazgo se sostiene igual; lo que no se
sostiene es esa cifra, y se deja escrito aqui en vez de repetirla.

---

### S-010 - Se aceptan `F-024` a `F-026`; nace `_workflow/005_discovery.md`
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Etapa | `000_preproject` |
| Tareas | T-032, T-033, T-034 |

- **Que se hizo:** `manager` evaluo los tres hallazgos abiertos por `R-009` sobre `S-009` (`F-024`,
  `F-025`, `F-026`), verifico cada uno contra `HEAD` (`99c3aa3`) y los acepto los tres. `D-050`
  resuelve `F-024`: la correccion de `T-028` en la celda «Avance de la etapa» no sobrevivio a que el
  cierre la sobrescriba entera; se trata como resuelto **por desaparicion**, `T-028` pasa a
  `Cancelada`, y `T-032` deja nota fechada en los tres registros que afirmaban la nota inexistente,
  sin reescribir texto historico (`D-019`). Se registra `L-015`: una correccion escrita en una
  seccion que el cierre sobrescribe no es una correccion. `T-033` ancla con nota fechada los
  bloques de verificacion de `D-043` y `D-044`, que `F-025` señalo sin reproducirse sobre su propio
  commit. `T-034` corrige en `techdebt.md` la cita cruzada `L-013` → `L-014` que `F-026` señalo.

  Por pedido del usuario, `_workflow/` gana un archivo por etapa declarada (`D-051`): nace
  `_workflow/005_discovery.md`, que aplica `team.md` y `ai_levels.md` a los siete pasos del
  procedimiento de la etapa, y `_phases/005_discovery.md` queda editado para citarlo antes del
  Paso 1 — el cuarto enganche que `L-014` y `DT-002` señalaban sin resolver. `DT-002` no se marca
  `Implementada`: la confirmacion es del usuario. `D-052` deja escrito que el reparto de esa tabla
  no se adopta todavia: se adopta con su `D-XXX` al abrir `005_discovery`, no antes.
- **Que quedo abierto:** `T-001`, `T-002` y `T-003` siguen `No implementada`. `A-004` y `A-005`
  siguen `Abierto`. `F-024` a `F-026` quedan `Aceptado — pendiente` hasta que la auditoria siguiente
  verifique la correccion sobre este commit y los cierre. `DT-002` sigue `No implementada` /
  `Propuesta (pendiente del usuario)`, aunque el cuarto enganche que reclamaba ya existe. El `D-XXX`
  de adopcion del reparto de `_workflow/005_discovery.md` queda pendiente para cuando se abra
  `005_discovery` (`D-052`).

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
