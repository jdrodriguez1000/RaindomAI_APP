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
| [S-011](#s-011---se-aceptan-f-027-y-f-028-nace-el-puntero-a-las-lecciones-globales-y-la-cosecha) | Se aceptan `F-027` y `F-028`; nace el puntero a las lecciones globales y la cosecha | 2026-09-02 | `000_preproject` |
| [S-012](#s-012---se-aceptan-f-029-a-f-031-nace-_phases010_prototypemd-y-el-paso-2d-del-cierre) | Se aceptan `F-029` a `F-031`; nace `_phases/010_prototype.md` y el Paso 2d del cierre | 2026-09-02 | `000_preproject` |
| [S-013](#s-013---se-aceptan-f-032-y-f-033-nacen-las-plantillas-de-_templates010_prototype) | Se aceptan `F-032` y `F-033`; nacen las plantillas de `_templates/010_prototype/` | 2026-09-02 | `000_preproject` |
| [S-014](#s-014---se-acepta-f-034-nace-d-065l-020-la-seccion-7-del-informe-y-_workflow010_prototypemd) | Se acepta `F-034`; nace `D-065`/`L-020`, la seccion 7 del informe y `_workflow/010_prototype.md` | 2026-09-03 | `000_preproject` |
| [S-015](#s-015---nace-el-gate-1-agente-y-skill-no-etapa-d-067-a-d-070) | Nace el Gate 1 (agente y skill, no etapa; `D-067` a `D-070`) | 2026-09-02 | `000_preproject` |
| [S-016](#s-016---se-aceptan-f-035-a-f-038-la-comprobacion-0-pasa-a-orden-del-grafo-d-071-y-nace-_phases020_baselinemd-d-072) | Se aceptan `F-035` a `F-038`; la Comprobacion 0 pasa a orden del grafo (`D-071`) y nace `_phases/020_baseline.md` (`D-072`) | 2026-09-03 | `000_preproject` |
| [S-017](#s-017---se-acepta-f-039-t-059-nacen-las-plantillas-de-_templates020_baseline-d-073-d-074-y-l-024) | Se acepta `F-039` (`T-059`); nacen las plantillas de `_templates/020_baseline/` (`D-073`, `D-074`) y `L-024` | 2026-09-03 | `000_preproject` |
| [S-018](#s-018---se-aceptan-f-040-a-f-044-nace-_workflow020_baselinemd-t-057-d-075-d-076) | Se aceptan `F-040` a `F-044`; nace `_workflow/020_baseline.md` (`T-057`, `D-075`, `D-076`) | 2026-09-03 | `000_preproject` |
| [S-019](#s-019---se-aceptan-f-045-a-f-047-t-066-a-t-068-d-077-nace-_phases025_wsltmd-y-su-reparto-d-078-a-d-080) | Se aceptan `F-045` a `F-047` (`T-066` a `T-068`, `D-077`); nace `_phases/025_wslt.md` y su reparto (`D-078` a `D-080`) | 2026-09-03 | `000_preproject` |
| [S-020](#s-020---se-aceptan-f-048-a-f-050-t-072-a-t-075-d-081-nace-el-paso-2e-de-protocol-close-y-_phases030_growthmd-d-082) | Se aceptan `F-048` a `F-050` (`T-072` a `T-075`, `D-081`); nace el Paso 2e de `protocol-close` y `_phases/030_growth.md` (`D-082`) | 2026-09-04 | `000_preproject` |
| [S-021](#s-021---se-aceptan-f-051-a-f-054-t-077-a-t-082-nace-el-paso-7c-de-protocol-close-d-083-a-d-085-y-las-plantillas-de-_templates030_growth) | Se aceptan `F-051` a `F-054` (`T-077` a `T-082`); nace el Paso 7c de `protocol-close` (`D-084`) y las plantillas de `_templates/030_growth/` (`D-085`, `T-083`) | 2026-09-05 | `000_preproject` |
| [S-022](#s-022---se-aceptan-f-055-a-f-058-t-084-a-t-090-nace-el-paso-1c-de-protocol-close-y-_workflow030_growthmd-d-091) | Se aceptan `F-055` a `F-058` (`T-084` a `T-090`); nace el Paso 1c de `protocol-close` y `_workflow/030_growth.md` (`D-091`) | 2026-09-06 | `000_preproject` |
| [S-023](#s-023---se-aceptan-f-059-a-f-061-t-093-a-t-096-nacen-los-pasos-7c-bis-y-7d-de-protocol-close-y-el-gate-2-d-094) | Se aceptan `F-059` a `F-061` (`T-093` a `T-096`); nacen los Pasos 7c-bis y 7d de `protocol-close`, y el Gate 2 (`D-094`) | 2026-09-06 | `000_preproject` |
| [S-024](#s-024---se-aceptan-f-062-a-f-065-t-097-a-t-100-a-010-se-refuta-y-se-acota-d-099-nace-_phases040_evolmd-d-100) | Se aceptan `F-062` a `F-065` (`T-097` a `T-100`); `A-010` se refuta y se acota (`D-099`); nace `_phases/040_evol.md` (`D-100`) | 2026-09-07 | `000_preproject` |
| [S-025](#s-025---se-aceptan-f-066-a-f-069-t-101-a-t-104-nacen-las-plantillas-de-_templates040_evol-d-105) | Se aceptan `F-066` a `F-069` (`T-101` a `T-104`); nacen las plantillas de `_templates/040_evol/` (`D-105`) | 2026-09-07 | `000_preproject` |
| [S-026](#s-026---se-aceptan-f-070-a-f-073-t-106-a-t-109-nace-_workflow040_evolmd-sin-adoptar-d-110) | Se aceptan `F-070` a `F-073` (`T-106` a `T-109`); nace `_workflow/040_evol.md`, sin adoptar (`D-110`) | 2026-09-07 | `000_preproject` |
| [S-027](#s-027---se-aceptan-f-074-y-f-075-t-110-t-111-un-codigo-instanciado-pasa-a-ser-dato-propio-d-113-a-d-115-claudemd-y-claude-quedan-agnosticos) | Se aceptan `F-074` y `F-075` (`T-110`, `T-111`); un codigo instanciado pasa a ser dato propio (`D-113` a `D-115`); `CLAUDE.md` y `.claude/` quedan agnosticos | 2026-09-07 | `000_preproject` |
| [S-028](#s-028---nace-_templates000_preproject-d-116-y-se-realinea-_phases000_preprojectmd-con-el-andamiaje-real-d-117) | Nace `_templates/000_preproject/` (`D-116`) y se realinea `_phases/000_preproject.md` con el andamiaje real (`D-117`) | 2026-09-08 | `000_preproject` |
| [S-029](#s-029---se-aceptan-f-076-a-f-082-t-116-a-t-122-nace-el-acta-de-cierre-de-etapa-d-121-a-d-123) | Se aceptan `F-076` a `F-082` (`T-116` a `T-122`); nace el acta de cierre de etapa, con `phase_exit_auditor` y la cosecha antes de la firma (`D-121` a `D-123`) | 2026-09-08 | `000_preproject` |
| [S-030](#s-030---se-aceptan-f-083-a-f-086-t-130-a-t-135-nace-el-acta-de-cierre-de-etapa-y-el-sexto-agente-phase_exit_auditor-t-123-a-t-125) | Se aceptan `F-083` a `F-086` (`T-130` a `T-135`); se construye el acta de cierre de etapa y el sexto agente `phase_exit_auditor` (`T-123` a `T-125`) | 2026-09-08 | `000_preproject` |
| [S-031](#s-031---se-aceptan-f-087-a-f-090-t-136-a-t-141-nace-la-skill-protocol-harvest-t-142-y-se-cierra-el-enganche-del-acta-t-126-t-127-t-129) | Se aceptan `F-087` a `F-090` (`T-136` a `T-141`); nace la skill `protocol-harvest` (`T-142`) y se cierra el enganche del acta (`T-126`, `T-127`, `T-129`) | 2026-09-10 | `000_preproject` |
| [S-032](#s-032---se-aceptan-f-091-y-f-092-t-145-a-t-147-el-arranque-lee-los-supuestos-abiertos-t-143-d-136) | Se aceptan `F-091` y `F-092` (`T-145` a `T-147`); el arranque lee los supuestos abiertos (`T-143`, `D-136`) | 2026-09-10 | `000_preproject` |
| [S-033](#s-033---se-aceptan-f-093-y-f-094-t-148-a-t-151-se-adopta-la-secuencia-de-etapas-d-142-y-se-aplazan-t-001-t-003-y-t-144-d-143) | Se aceptan `F-093` y `F-094` (`T-148` a `T-151`); se adopta la secuencia de etapas (`D-142`) y se aplazan `T-001`, `T-003` y `T-144` (`D-143`) | 2026-09-10 | `000_preproject` |
| [S-034](#s-034---se-aceptan-f-095-a-f-097-t-152-a-t-155-y-nace-el-paso-7c-ter-d-144-el-esqueleto-de-arranque-pasa-a-ser-repositorio-propio-d-145-a-d-148-t-156-a-t-163) | Se aceptan `F-095` a `F-097` (`T-152` a `T-155`), nace el Paso 7c-ter (`D-144`); el esqueleto de arranque pasa a ser repositorio propio (`D-145` a `D-148`, `T-156` a `T-163`) | 2026-09-11 | `000_preproject` |
| [S-035](#s-035---se-aceptan-f-098-y-f-099-t-164-a-t-166-nace-el-paso-7c-quater-d-149-y-l-055-el-esqueleto-se-publica-como-repositorio-t-157-y-nace-la-forma-de-arranque-por-clone-d-150) | Se aceptan `F-098` y `F-099` (`T-164` a `T-166`); nace el Paso 7c-quater (`D-149`) y `L-055`; el esqueleto se publica como repositorio (`T-157`) y nace la forma de arranque por clone (`D-150`) | 2026-09-11 | `000_preproject` |
| [S-036](#s-036---se-aceptan-f-100-y-f-101-t-169-t-170-se-corrige-la-cuarta-cita-cruzada-t-171-el-esqueleto-queda-sincronizado-y-con-su-barrido-de-cierre-t-158-a-t-161-nace-dt-007-d-151-c-010-l-057) | Se aceptan `F-100` y `F-101` (`T-169`, `T-170`); se corrige la cuarta cita cruzada (`T-171`); el esqueleto queda sincronizado y con su barrido de cierre (`T-158` a `T-161`); nace `DT-007` (`D-151`, `C-010`, `L-057`) | 2026-09-11 | `000_preproject` |

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
| Ultima actualizacion | 2026-09-11 (S-036) |
| Salud | En marcha |
| Avance de la etapa | Se evaluaron, contra `HEAD` (`ce0ac4e`, la auditoria `R-035` sobre `S-035` en `cce48e0`), los dos hallazgos abiertos de `R-035` (`F-100`, `F-101`): los dos se aceptan y quedan `Aceptado — pendiente` en `_audit/findings.md`, con su `T-XXX` (`T-169`, `T-170`). `F-100` (la bitacora de `S-035` afirmaba que `project.md` ganaba dos filas nuevas, y el commit `cce48e0` no toca ese archivo) y `F-101` (el bloque de verificacion de `T-157` describia un «segundo barrido» sin publicar ni su patron ni su salida) se corrigen por nota fechada, sin reescribir la prosa original; el segundo se rehizo hoy sobre el mismo arbol del esqueleto porque la orden original nunca se habia escrito y no se podia reconstruir. Al leer los criterios de cierre de `D-145` a `D-151` de corrido aparecio una cuarta cita cruzada que la pasada de `T-168` no habia visto —el cuerpo de `D-147` remitia a `T-162` en vez de `T-159`—, y se corrige por nota fechada (`T-171`). Fuera de los hallazgos: se completan `T-158` (sincronizar las seis areas agnosticas del esqueleto, commit `1748f0a` en `SDAI_TripleS`), `T-159` (registrar la ubicacion del esqueleto en `project.md`), `T-160` (el Paso 2f de `protocol-close`, con sus tres resultados probados) y `T-161` (la skill `protocol-promote`, con su puerta antes de escribir). Al medir el alcance de una barra invertida que se pierde al escribir por shell aparecen `C-010` y `L-057`, con **26 ocurrencias heredadas** del mismo defecto que documentan `DT-003` a `DT-006`, ya commiteadas en `tasks.md`, `assumptions.md` y `findings.md`; `D-151` decide no corregirlas en masa —reescribirlas convertiria «evidencia que no reproduce» en «evidencia falsa»— y la deuda se propone como `DT-007`. Nace tambien `L-056` (una orden que busca su propio rotulo en el archivo donde queda escrita se cuenta a si misma) y `A-019` (la skill de promocion existe y esta bien ordenada, pero no se ha ejecutado ni una vez). `CLAUDE.md` se corrige para decir que la cosecha es «uno de los dos» protocolos que escriben fuera del repositorio, nombrando a `protocol-promote`. Los controles de fuga (Pasos 1b y 1c) y de indices (Paso 2b) de este cierre salen limpios; el Paso 2c muestra las mismas dos diferencias ya conocidas y documentadas en `project.md` (`010_prototype/` y `temporal/`). |
| Bloqueos activos | El alcance y el objetivo del proyecto siguen sin definir (`T-001`, aplazada por `D-143`; se retoma cuando `A-004` quede confirmado **y** `005_discovery` este activa); `A-003` sigue sin verificar y `T-003` sigue `Suspendida` (`D-143`); del esqueleto de arranque solo quedan `T-156` (construir el esqueleto reutilizable en si — `Bloqueante`), `T-162` (guia de arranque) y `T-163` (dos huecos menores: brief y `temporal/`), y `T-167` (llevar a la plantilla de `project.md` las dos filas de `D-150`), todas `No implementada` |

---

## 2. Ultimo realizado

Se evaluaron, verificados contra `HEAD` (`ce0ac4e`, la auditoria `R-035` sobre el commit de `S-035`
`cce48e0`) antes de tratarlos, los dos hallazgos abiertos de `R-035`. Los dos se sostuvieron contra
la evidencia y se aceptan:

- `F-100` (la entrada `S-035` de la bitacora afirmaba que `project.md` ganaba dos filas nuevas —
  esqueleto de origen y version de partida—, y el commit `cce48e0` no toca `project.md`): nota
  fechada en la propia entrada, con las dos ordenes que muestran que ni el commit ni el archivo en
  `HEAD` tienen esas filas, sin reescribir la prosa original (`T-169`).
- `F-101` (el bloque de verificacion de `T-157` describia un «segundo patron, por codigos
  instanciados», pero ninguna orden publicada correspondia a ese patron): la orden de entonces no se
  pudo reconstruir —nunca se escribio—, asi que no se finge. Se rehizo hoy sobre el mismo arbol del
  esqueleto (sigue en `fa7da56`, sin sincronizar) y se publica entera, con su patron, su ambito y su
  salida cruda, por nota fechada sin reescribir el bullet original (`T-170`).

Los dos hallazgos quedan `Aceptado — pendiente` en `_audit/findings.md`, citando su `T-XXX`.

Al leer de corrido los criterios de cierre de `D-145` a `D-151` aparecio una **cuarta** cita cruzada
que la pasada anterior (`T-168`) no vio, porque buscaba solo la forma «Lo implementa `T-XXX`»: el
cuerpo de `D-147` remite a `T-162` (la guia de arranque) donde debia decir `T-159` (la escritura de
las dos filas). Se corrige por nota fechada, con la orden anclada al commit donde el defecto existe
para que la nota no se incluya en su propio barrido (`T-171`).

Fuera de los hallazgos, se completan las cuatro tareas que `T-157` desbloqueaba:

- `T-158` — las seis areas agnosticas del esqueleto quedan sincronizadas (commit `1748f0a` en
  `SDAI_TripleS`): los ocho archivos por detras que `T-157` habia dejado sin tocar, mas la
  correccion de un final de linea (un archivo en CRLF aqui se copia convertido a LF, el que el
  destino ya tenia). Los cuatro barridos de agnosticismo sobre el esqueleto ya sincronizado salen
  limpios.
- `T-159` — `project.md` registra la ubicacion del esqueleto (repositorio y remoto), con la nota del
  caso invertido («este proyecto no salio del esqueleto: el esqueleto salio de este proyecto»).
- `T-160` — nace el **Paso 2f** en `protocol-close`: el barrido de desfase con el esqueleto, que
  informa y no frena, con guarda para el caso de ruta ausente (`SIN COMPROBAR`) y su seccion propia
  en el informe de auditoria.
- `T-161` — nace la skill `protocol-promote`: lleva al esqueleto lo que este proyecto escriba en las
  seis areas, con la misma puerta que `protocol-harvest` y en el mismo orden (los barridos y la
  medicion de final de linea van antes de la puerta, nunca despues).

Al escribir estos bloques de verificacion con patrones `\b` se descubrio que las barras invertidas se
pierden al escribir por shell y quedan como caracter de retroceso real (`0x08`), invisible en
pantalla (`C-010`, `L-057`). El barrido de alcance encuentra **26 ocurrencias heredadas** del mismo
defecto que ya documentan `DT-003` a `DT-006`, en `tasks.md`, `assumptions.md` y `findings.md`.
`D-151` decide no corregirlas en masa —reescribir un bloque antiguo para que exhiba el patron que
debio ejecutarse convertiria «evidencia que no reproduce» en «evidencia falsa»—, y la deuda se
propone como `DT-007`. Nace tambien `L-056` (una orden que busca su propio rotulo en el archivo
donde queda escrita se cuenta a si misma) y `A-019` (la skill `protocol-promote` esta bien escrita y
bien ordenada, pero no se ha ejecutado ni una vez). `CLAUDE.md` se corrige en dos sitios para decir
que la cosecha es «uno de los dos» protocolos que escriben fuera del repositorio, nombrando al otro.

Los controles de fuga (Pasos 1b y 1c) y de indices (Paso 2b) de este cierre salen limpios. El Paso 2c
muestra las mismas dos diferencias ya conocidas y documentadas en `project.md` (`010_prototype/` y
`temporal/`).

- **Que quedo abierto:** de la familia del esqueleto solo quedan `T-156` (la tarea paraguas, sigue
  `Bloqueante`), `T-162` (guia de arranque) y `T-163` (dos huecos menores: brief y `temporal/`), y
  `T-167` (llevar a la plantilla de `project.md` las dos filas de `D-150`), todas `No implementada`.
  `T-001` y `T-144` siguen `No implementada` (aplazadas, etapa no iniciada). `T-003` sigue
  `Suspendida`. `T-128` (la primera cosecha real) sigue `No implementada`, sin bloqueo. `DT-002` a
  `DT-007` siguen `Propuesta (pendiente del usuario)`. `A-006` a `A-009`, `A-011` a `A-015`, `A-018` y
  `A-019` siguen abiertos; `A-016`/`A-017` siguen `Confirmado`, `A-010` `Refutado`. La
  autorreferencia del criterio de cierre de `D-088` sigue sin resolver.

---

## 3. Siguiente paso

Lanzar `report_auditor` sobre el commit de este cierre: tiene que comprobar que `F-100` y `F-101`
quedaron `Aceptado — pendiente` con su `T-XXX`, que las notas fechadas de `T-169` y `T-170`
reproducen sus ordenes sin tocar la prosa anterior, que la nota de `T-171` corrige de verdad la
cuarta cita cruzada de `D-147` con su orden anclada, que `T-158` a `T-161` estan de verdad
`Implementada` (el esqueleto sincronizado en `1748f0a`, `project.md` con sus dos filas, el Paso 2f en
`protocol-close`, la skill `protocol-promote` escrita), y que `DT-007` no duplica sin decirlo el
alcance ya cubierto por `DT-003` a `DT-006`.

El siguiente trabajo de fondo sigue siendo **el esqueleto de arranque**: quedan `T-162` (la guia de
arranque, que tiene que cubrir lo que un `clone` no trae — `temporal/`, el `.git` propio) y `T-163`
(los dos huecos menores). Con eso `T-156` quedaria lista para cerrarse. La primera **promocion**
real con `protocol-promote` (sobre las cuatro diferencias que esta misma sesion dejo pendientes:
`protocol-close`, `protocol-harvest`, `protocol-promote` nueva y `CLAUDE.md`) es la primera prueba
del supuesto `A-019` — y solo puede pedirla el usuario, con el repositorio limpio y subido.

Sigue pendiente la primera cosecha real de `000_preproject` con `protocol-harvest` (`T-128`), pero
solo cuando la etapa se vaya a cerrar de verdad (`_phases/000_preproject.md` exige que corra **antes**
de la firma del patrocinador) — y con ella, el primer uso real de `protocol-phase-exit` sobre su
condicion de salida.

`T-001` se retoma cuando `A-004` quede confirmado —hay acceso al patrocinador— **y** `005_discovery`
este activa. `T-003` se retoma cuando se aborde el diseño tecnico de obtencion de datos. `T-144` se
retoma cuando `005_discovery` este activa.

Es decision del usuario si `DT-002` a `DT-007` se confirman, si `A-006` (los codigos `FT-`/`SC-`
declarados) se valida o se retira, si `A-007` se confirma cuando la etapa se adopte, si `A-012` se
confirma o se corrige antes de que `040_evol` se adopte, y si `A-015` se mantiene o se acota. `A-013`
sigue sin comprobar de fondo, por muestreo. `A-018` se confirma o se refuta la primera vez que el
barrido del Paso 2f devuelva algo y se promueva de verdad (ahora que `T-160` esta hecha, ese momento
ya puede llegar). `A-019` se refuta con la primera ejecucion real de `protocol-promote` que no haga
lo que la skill dice. Sigue tambien sin resolver la autorreferencia del criterio de cierre de
`D-088`.

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

### S-011 - Se aceptan `F-027` y `F-028`; nace el puntero a las lecciones globales y la cosecha
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Etapa | `000_preproject` |
| Tareas | T-035, T-036 |

- **Que se hizo:** `manager` evaluo los dos hallazgos abiertos por `R-010` sobre `S-010` (`F-027`,
  `F-028`), verifico cada uno contra `HEAD` (`cbb92a9`) y los acepto los dos. `T-035` ancla con nota
  fechada el bloque de verificacion de `T-032`, que no se reproducia sobre `51354ef` y cuya lectura
  en prosa quedaba desmentida por una linea viva; el fondo de `T-032` se sostiene, fallo la
  evidencia. `T-036` completa en `_audit/S-010.md` la viñeta de `decisions.md`, que omitia las dos
  notas fechadas que `T-033` inserta dentro de `D-043` y `D-044`.

  El usuario aporto en `temporal/` un archivo de 98 lecciones transversales de proyectos anteriores.
  `D-053` lo lleva a un repositorio propio y externo (`TripleS_Lessons/global_lessons.md`, privado en
  GitHub), fuera de este repositorio y de `_methodology/` para no crear copias divergentes. `D-054`
  hace la primera consulta de arranque —bloques D y E, 17 lecciones, ancladas a `fa03813`— y produce
  `T-037` (inventario de acciones irreversibles) mas cinco señales de producto/alcance registradas
  para `005_discovery`, sin adoptarlas hoy. `D-055` construye el puntero de uso en tres piezas: la
  regla sin datos propios en `CLAUDE.md`, la ruta en `project.md`, el control en la condicion de
  salida de `_phases/000_preproject.md`. `D-056` cierra el camino de vuelta: una casilla de cosecha
  por etapa declarada mas la columna `Portabilidad` en el indice de `lessons.md` que la hace
  comprobable; nacen `L-016` (una consulta que cambia lo que se hace no deja rastro visible por si
  sola) y `L-017` (una condicion de salida no es una tarea pendiente).

  Por iniciativa propia se empezo a verificar `A-003` con `curl` contra la fuente oficial: el sitio
  responde sin cabeceras de navegador y trae datos en el HTML crudo, pero la verificacion quedo a
  medias —falta historico completo, los siete campos del brief, la plataforma de despliegue y las
  condiciones de uso—. `A-003` sigue `Abierto`. Se registra `T-038`: el barrido de fuga de
  `protocol-audit` cubre menos carpetas que el de `protocol-close`, y su correccion es decision del
  usuario.
- **Que quedo abierto:** `T-001`, `T-002` y `T-003` siguen `No implementada`. `A-003`, `A-004` y
  `A-005` siguen `Abierto`. `F-027` y `F-028` quedan `Aceptado — pendiente` hasta que la auditoria
  siguiente verifique la correccion sobre este commit y los cierre. `T-037` y `T-038` nacen
  `Pendiente` — valor que no esta en la lista de estados que declara la convencion de `tasks.md`
  (`Implementada` / `No implementada` / `Cancelada` / `Suspendida`); se deja tal como lo escribio
  `manager` y se señala aqui, no se reescribe. Las cinco señales de `D-054` sobre `005_discovery`
  quedan registradas sin adoptar. `000_preproject` gana la condicion de salida de la cosecha con sus
  quince lecciones `Sin evaluar`.

📌 **Nota del 2026-09-02 (`T-041`, hallazgo `F-031`).** La bitacora se deja tal cual (`D-019`).
«Quince lecciones `Sin evaluar`» son **diecisiete** sobre el commit de esa sesion: el recuento es el
mismo defecto que la nota de la seccion 2 acota, con el mismo bloque anclado a `2a2d3b6`.

---

### S-012 - Se aceptan `F-029` a `F-031`; nace `_phases/010_prototype.md` y el Paso 2d del cierre
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Etapa | `000_preproject` |
| Tareas | T-039, T-040, T-041, T-042, T-043, T-044 |

- **Que se hizo:** `manager` evaluo los tres hallazgos abiertos por `R-011` sobre `S-011` (`F-029`,
  `F-030`, `F-031`), verifico cada uno contra `HEAD` (`f1f3fea`) y los acepto todos. `T-039`
  normaliza a `No implementada` el estado `Pendiente` (fuera de convencion) de `T-037` y `T-038`,
  sin crear un quinto estado (`D-057`). `T-040` da a `T-038` el respaldo que le faltaba: `D-058`
  declara que nacio de una observacion propia de `manager` al leer `R-010`, fuera de las dos
  excepciones de la convencion, y `T-038` lo cita. `T-041` anota con nota fechada, en los cuatro
  sitios que el hallazgo enumera, que el recuento «quince lecciones `Sin evaluar`» de `S-011` son
  diecisiete. `T-042` cierra la segunda mitad de `F-031`: `protocol-close` gana el **Paso 2d**, que
  localiza los bloques de verificacion publicados sin ancla a un commit y obliga a reejecutarlos
  antes de cerrar — septima repeticion del mismo defecto (`F-005`, `F-008`, `F-011`, `F-022`,
  `F-025`, `F-027`, `F-031`), con `L-013`/`L-015` ya escritas y sin mecanismo hasta ahora.

  Por separado, el usuario aporto un archivo de etapa de prototipo de otro proyecto en `temporal/`.
  `T-043` lo adapta a esta metodologia y nace `_phases/010_prototype.md`: agnostico, sin datos
  propios ni codigos instanciados, con la casilla de cosecha que `D-056` exige. Adaptarlo destapo un
  choque que no existia en el proyecto de origen —la etapa produce codigo y prohibe tests, contra
  `PI-5`—, resuelto con `D-059` (excepcion explicita y acotada al artefacto descartable) y `D-060`
  (el archivo se adelanta sin declarar la etapa en `project.md`, que es trabajo del descubrimiento).
  Nace `L-018`: adaptar un archivo ajeno no es traducirlo, porque sus reglas venian equilibradas con
  otro conjunto de reglas. `T-044` cierra los enganches sueltos a peticion del usuario: dos fugas de
  estado del proyecto en el archivo nuevo, la carpeta de entregables `010_prototype/` (`D-061`), y
  un incumplimiento de `L-007` en `D-059` —la excepcion a `PI-5` habia quedado sin puntero en
  `CLAUDE.md`—, corregido en la misma sesion. `D-062` deja escrito que el numero minimo de usuarios
  del prototipo lo fija el proyecto, porque la guia de metodo no lo fija.
- **Que quedo abierto:** `T-001`, `T-002` y `T-003` siguen `No implementada`. `T-037` y `T-038`
  siguen `No implementada` (ya con estado valido). `F-029`, `F-030` y `F-031` quedan
  `Aceptado — pendiente` hasta que la auditoria siguiente verifique la correccion sobre este commit
  y los cierre. `_phases/010_prototype.md` existe pero **no adopta la etapa**: `project.md` sigue
  declarando solo `000_preproject` y `005_discovery`, y el archivo referencia plantillas en
  `_templates/010_prototype/` y un archivo de reparto en `_workflow/010_prototype.md` que hoy no
  existen — condicion para abrir la etapa, no trabajo pendiente de dentro de ella.

---

### S-013 - Se aceptan `F-032` y `F-033`; nacen las plantillas de `_templates/010_prototype/`
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Etapa | `000_preproject` |
| Tareas | T-045, T-046, T-047, T-048 |

- **Que se hizo:** `manager` evaluo los dos hallazgos abiertos por `R-012` sobre `S-012` (`F-032`,
  `F-033`), verifico cada uno contra `HEAD` (`265bfeb`) y los acepto ambos. `T-045` anota con nota
  fechada, sin reescribir (`D-019`), que el bloque de `T-041` publicaba `_persistence/progress.md:2`
  como prueba de cuatro notas fechadas, cuando la orden sobre el commit que lo contiene (`7f55389`)
  y sobre `HEAD` devuelve `1`, y el total real es `3` notas, no `4` — la cuarta se perdio cuando el
  cierre sobrescribio la seccion viva de `progress.md` (`L-015`). `T-046` cierra la segunda mitad de
  `F-032`, la que evita un noveno caso del mismo defecto: el Paso 2d de `protocol-close` gana el
  parrafo que exige publicar la **lista completa** de su primera orden, con su recuento, en vez de
  una seleccion (`D-063`) — es la octava repeticion (`F-005`, `F-008`, `F-011`, `F-022`, `F-025`,
  `F-027`, `F-031`, `F-032`), ocurrida en la misma sesion que creo el Paso 2d. Nace `L-019`: correr
  un control y documentar una parte de su salida no es haberlo corrido. Al verificarlo aparecio que
  la orden del Paso 2d no devuelve el mismo numero en todos los entornos (`26` en `R-012`, `28`
  aqui, sobre el mismo commit). `T-047` atiende `F-033`: la nota de cierre de `D-060` afirmaba que
  `project.md` «no nombra la etapa nueva en ningun sitio», y la nombra en tres —todas de la carpeta
  de entregables de `D-061`—; se acota con nota fechada, sin reescribir, a lo que la orden prueba de
  verdad: que la tabla «Etapas» sigue teniendo dos.

  Por separado, el usuario aporto en `temporal/` cinco archivos de otro proyecto como material para
  las plantillas de la etapa del prototipo. `T-048` los adapta y nacen las cinco plantillas de
  `_templates/010_prototype/`, una por artefacto de `_phases/010_prototype.md` §5. `D-064` fija que
  se adaptan, no se copian, y documenta siete cambios de fondo: rutas de este metodo, los actores
  reales, codigos genericos del registro, sin tildes, sin la cifra de participantes que en su origen
  ya estaba sin respaldo (la fija el proyecto, `D-062`), sin referencias a un archivo de etapa de
  Gate que este proyecto no tiene, y con hueco para el codigo de producto que `project.md` aun no
  declara.
- **Que quedo abierto:** `T-001`, `T-002` y `T-003` siguen `No implementada`. `T-037` y `T-038`
  siguen `No implementada`. `F-032` y `F-033` quedan `Aceptado — pendiente` hasta que la auditoria
  siguiente verifique la correccion sobre este commit y los cierre. Las cinco plantillas de
  `_templates/010_prototype/` no adoptan la etapa (`D-060` vigente) ni completan su condicion de
  entrada: falta `_workflow/010_prototype.md`, que no se escribio hoy.

---

### S-014 - Se acepta `F-034`; nace `D-065`/`L-020`, la seccion 7 del informe y `_workflow/010_prototype.md`
| Campo | Valor |
|---|---|
| Fecha | 2026-09-03 |
| Etapa | `000_preproject` |
| Tareas | T-049, T-050, T-051 |

- **Que se hizo:** `manager` evaluo el hallazgo abierto por `R-013` sobre `S-013` (`F-034`), lo
  verifico contra `HEAD` (`4e9d639`) y lo acepto: la seccion 6 de `_audit/S-013.md` afirmaba haber
  publicado la lista completa del Paso 2d remitiendo a la verificacion de `T-046`, que contiene dos
  ordenes y ninguna es la primera del Paso 2d — la salida solo vivio en pantalla. `T-049` deja nota
  fechada al lado de la seccion 6 de `_audit/S-013.md`, sin reescribir el original (`D-019`),
  publicando la lista entera anclada al rango `265bfeb..8eb8666` (`13` apariciones, `10` ordenes
  distintas, no `nueve`). `T-050` ataca la causa de fondo: `D-065` decide que la evidencia del Paso
  2d tiene sitio fijo — la seccion 7 nueva del informe `_audit/S-XXX.md` —, porque `D-063` decia
  **que** publicar y no **donde**, y una evidencia sin destino no genera ningun momento en que se
  eche en falta. Dos inserciones en `protocol-close`, ambas de solo-insercion. Nace `L-020`: una
  regla que dice que registrar pero no donde no se incumple, se evapora.

  Por pedido del usuario nace `_workflow/010_prototype.md` (`T-051`, `D-066`), condicion de entrada
  de la etapa junto con las plantillas de `_templates/010_prototype/` (`_phases/010_prototype.md`
  §5). Reparte los nueve pasos del procedimiento derivando `_workflow/team.md` y
  `_workflow/ai_levels.md`: la IA construye el prototipo (Paso 4, primera vez que escribe codigo en
  el metodo, autonomia reversible/impacto relevante, revision humana entera); queda fuera de las
  sesiones de usuario y de negocio (Pasos 5 y 9); la inmovilidad del prototipo la vigila el
  historial (Paso 6); y la IA clasifica sin pesar las observaciones (Paso 8). No adopta la etapa
  (`D-060` vigente) ni reparte nada por si solo (`_workflow/team.md` §8).
- **Que quedo abierto:** `T-001`, `T-002` y `T-003` siguen `No implementada`. `T-037` y `T-038`
  siguen `No implementada`. `F-034` queda `Aceptado — pendiente` hasta que la auditoria siguiente
  verifique la correccion sobre este commit y lo cierre. `010_prototype` ya tiene plantillas y
  reparto, pero sigue sin adoptarse en `project.md`.

---

### S-015 - Nace el Gate 1 (agente y skill, no etapa; `D-067` a `D-070`)
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Etapa | `000_preproject` |
| Tareas | T-052 |

- **Que se hizo:** el usuario trajo `temporal/015_gate1.md`, un borrador del Gate 1, y pidio
  construir su archivo de etapa. Contrastandolo con `_methodology/000_method.md` §28-§32 se decidio
  que un Gate no es una etapa —es un acto de juicio, no un tramo de trabajo— y se monto como agente
  y skill: nace `.claude/agents/gate1_auditor.md`, `.claude/skills/protocol-gate1/SKILL.md` y
  `_templates/015_gate1/005_verdict.md` (`T-052`, `D-067`).

  `D-068` separa el dictamen tecnico de `gate1_auditor` —sobre seis de los siete criterios de §29—
  de la decision de inversion del usuario como patrocinador; el criterio 6 se marca `— corresponde
  al patrocinador` y `APROBADO`/`NO APROBADO` no aparecen como valor en ningun artefacto del Gate.

  `D-069` adopta `NO AUDITABLE` como tercer resultado, ausente en la guia de metodo: se determina en
  una Comprobacion 0 previa a cualquier criterio, resuelta con fechas del historial de `git` — la
  unica comprobacion del metodo imposible de aprobar a posteriori. Cada criterio se resuelve con tres
  valores, `CUMPLE`/`NO CUMPLE`/`NO COMPROBABLE`, tambien ausente en la guia.

  > 📌 **Nota del 2026-09-03 (`T-060`, hallazgo `F-037`).** El parrafo de arriba **no se reescribe**
  > —es la bitacora de lo que se decidio aquel dia—, y esta nota dice en que se paso de largo.
  > «Resuelta con fechas del historial de `git` — la unica comprobacion del metodo imposible de
  > aprobar a posteriori» era **falso tal como estaba implementado**: la Comprobacion 0 resolvia el
  > «antes» con `%ad`, la fecha de autor, que se sobrescribe con una variable de entorno.
  >
  > ```
  > $ git show 6b42d0f:.claude/skills/protocol-gate1/SKILL.md | grep -c "merge-base --is-ancestor"
  > 3
  > ```
  >
  > `D-071` (sesion `S-016`) ya adopto el **orden del grafo** —`git merge-base --is-ancestor`— para
  > las tres lecturas de «antes», y dejo `%ad` como dato informativo. La decision de tener un tercer
  > resultado `NO AUDITABLE` **sigue vigente**; lo que cambio es con que se determina. Este era el
  > tercero de los tres sitios que `F-037` nombraba, y el unico que `R-016` encontro sin corregir.

  `D-070` fija que los dictamenes son correlativos (`005_verdict_NNN.md`) y que ninguno se
  sobrescribe: `gate1_auditor` lee los anteriores antes de escribir el suyo, y un mismo fallo de
  Comprobacion 0 repetido es hallazgo de importancia alta por si mismo.

  `project.md` declara el Gate y su reparto de autoridad; `_phases/010_prototype.md` ancla lanzar el
  Gate como ultimo paso obligatorio de la etapa, sobre evidencia subida y sin contarle el contexto.

  Nace `L-021`: un barrido de fuga con `git grep` corrido antes de versionar los archivos nuevos
  devuelve cero por no verlos, no por estar limpios; se repitio con `grep -r` para el cero real.

- **Que quedo abierto:** `T-001`, `T-002` y `T-003` siguen `No implementada`. `010_prototype` sigue
  sin adoptarse en `project.md` (`D-060`). `R-014` sobre `S-014` abrio `F-035` (Media) y `F-036`
  (Baja); ninguno de los dos fue evaluado en esta sesion — siguen `Abierto` en `_audit/findings.md`,
  y esa evaluacion es tarea de `manager` en la sesion siguiente.

---

### S-016 - Se aceptan `F-035` a `F-038`; la Comprobacion 0 pasa a orden del grafo (`D-071`) y nace `_phases/020_baseline.md` (`D-072`)
| Campo | Valor |
|---|---|
| Fecha | 2026-09-03 |
| Etapa | `000_preproject` |
| Tareas | T-053, T-054, T-055, T-056, T-058 (T-057 queda abierta) |

- **Que se hizo:** `manager` evaluo, contra `HEAD` (`54f55d9`), los cuatro hallazgos abiertos de
  `R-014` (`F-035`, `F-036`) y `R-015` (`F-037`, `F-038`), y los acepto los cuatro. `F-035`
  (`T-053`): la seccion 7 de `_audit/S-014.md` atribuia mal el archivo de origen de tres de sus once
  ordenes; se añade nota fechada (`D-019`) con la procedencia derivada del diff, sin reescribir el
  bloque, y la seccion 7 de `protocol-close` pasa a exigir esa derivacion. `F-036` (`T-054`): se
  reescribe en forma generica la cita instanciada de una leccion en `_workflow/005_discovery.md`.
  `F-037` (`T-055`): se demuestra en un repositorio desechable que la Comprobacion 0 del Gate 1
  comparaba `%ad` (fecha de autor, falsificable con `GIT_AUTHOR_DATE`) y habria dado `PASA` sobre una
  hipotesis fechada antes pero escrita despues; `D-071` adopta resolver el «antes» por orden del
  grafo (`git merge-base --is-ancestor`), y la afirmacion absoluta se corrige en el skill, en la
  plantilla del dictamen y como nota fechada en `D-069`. `F-038` (`T-056`): la Comprobacion 0 pasa a
  localizar la subcarpeta del prototipo con `git ls-tree -d` y a emitir `NO AUDITABLE` si no la
  encuentra, en vez de depender de un valor no declarado en `project.md`. Nacen `L-022` y `L-023`.
  Ademas, sobre un borrador que trajo el usuario, nace `_phases/020_baseline.md` (`T-058`, `D-072`),
  sin adoptar la etapa en `project.md`. Queda abierta `T-057`: el reparto (`_workflow/020_baseline.md`)
  y las plantillas (`_templates/020_baseline/`) que ese archivo declara como su propia condicion de
  entrada.
- **Que quedo abierto:** `T-001`, `T-002` y `T-003` siguen `No implementada`. `010_prototype` sigue
  sin adoptarse en `project.md` (`D-060`). `T-057` queda `No implementada`. Los cuatro hallazgos de
  esta sesion quedan `Aceptado — pendiente` hasta que una auditoria posterior verifique la correccion
  sobre este commit.

---

### S-017 - Se acepta `F-039` (`T-059`); nacen las plantillas de `_templates/020_baseline/` (`D-073`, `D-074`) y `L-024`
| Campo | Valor |
|---|---|
| Fecha | 2026-09-03 |
| Etapa | `000_preproject` |
| Tareas | T-059 |

- **Que se hizo:** `manager` evaluo, contra `HEAD` (`b990e05`), el unico hallazgo de `R-016`
  (`F-039`, sobre `S-016`) y lo acepto (`T-059`). El primer bloque de la seccion 7 de
  `_audit/S-016.md` publicaba «Quince lineas» que en realidad eran su salida **deduplicada a mano**
  (la orden devuelve veintiuna), y esa orden ademas no reproducia contra el commit por correr sobre
  el area de staging. El bloque original no se reescribe: recibe una nota fechada con las dos
  cifras y la forma anclada de la orden. El Paso 2d de `protocol-close` y la plantilla de la
  seccion 7 pasan a exigir el recuento de lineas devueltas (el de ordenes distintas, aparte y con
  ese nombre), la lista sin deduplicar, y la orden anclada al commit con el propio informe excluido.
  Nace `L-024`: un barrido de caracteres de control encontro que `\b` se habia corrompido a `0x08`
  en seis lineas del registro; la de esta sesion se repara, las cinco anteriores quedan declaradas
  sin tocar, a la espera de que lo decida una auditoria. Aparte, el usuario pidio construir las
  nueve plantillas de `_templates/020_baseline/`; nacen numeradas por orden de procedimiento
  (`D-073`), y al escribirlas se destapo que `_phases/020_baseline.md` §5 decia «Ocho artefactos»
  sobre nueve filas — el usuario zanja que son nueve (`D-074`).
- **Que quedo abierto:** `T-001`, `T-002` y `T-003` siguen `No implementada`. `010_prototype` sigue
  sin adoptarse en `project.md` (`D-060`). `T-057` sigue `No implementada`: las plantillas ya
  existen, pero falta `_workflow/020_baseline.md`. Las cinco apariciones antiguas de `\x08` que
  `L-024` deja declaradas siguen sin resolver. `F-039` queda `Aceptado — pendiente` hasta que una
  auditoria posterior verifique la correccion sobre este commit.

---

### S-018 - Se aceptan `F-040` a `F-044`; nace `_workflow/020_baseline.md` (`T-057`, `D-075`, `D-076`)
| Campo | Valor |
|---|---|
| Fecha | 2026-09-03 |
| Etapa | `000_preproject` |
| Tareas | T-057, T-060, T-061, T-062, T-063, T-064, T-065 |

- **Que se hizo:** `manager` evaluo, contra `HEAD` (`6b42d0f`), los cinco hallazgos de `R-017`
  (sobre `S-017`) y los acepto todos. `F-040`: se declaran `FT-XXX` y `SC-XXX` en la tabla «Codigos»
  de `project.md` (`D-075`, `T-061`), siguiendo el precedente de `D-034`/`D-038`. `F-041`: la
  afirmacion de `D-073`/`T-057` sobre «sin codigos instanciados mas alla del primero» descansaba en
  un patron ciego a los prefijos de dos letras; se anota con nota fechada sin reescribir los
  bloques originales, con el patron ampliado y su salida real (`T-062`, nace `L-025`). `F-042`: el
  pendiente de las cinco lineas con `0x08` estaba delegado en `report_auditor`, que no decide; se
  abre `DT-003` y se corrige la frase de `L-024` (`T-063`). `F-043`: se corrige en `L-024` el
  recuento de lineas presentado como apariciones, y una segunda frase con el mismo defecto que el
  hallazgo no señalaba (`T-064`). `F-044`: se endurece la plantilla de la seccion `## 1. Que se
  hizo` de `protocol-close` para exigir tambien las entradas ya existentes que el commit edita, no
  solo las que nacen (`T-065`, nace `L-026`). Aparte, nace `_workflow/020_baseline.md` (`T-057`,
  pasa a `Implementada`): puntua «variabilidad de la entrada» en 2 y no declara discrepancia,
  a diferencia de los dos repartos anteriores (`D-076`); al escribirlo se corrige que
  `_phases/020_baseline.md` citaba el reparto en generico en vez de nombrarlo (nace `L-026`). Se
  anota tambien con nota fechada la bitacora de `S-015`, tercer sitio de `F-037` que `R-016` habia
  encontrado sin corregir (`T-060`).
- **Que quedo abierto:** `T-001`, `T-002` y `T-003` siguen `No implementada`. `010_prototype` sigue
  sin adoptarse en `project.md` (`D-060`). El reparto de `_workflow/020_baseline.md` existe pero no
  queda adoptado por existir. `DT-003` sigue `No implementada` y `Propuesta (pendiente del
  usuario)`. `A-006` queda abierto: si los codigos `FT-`/`SC-` declarados hoy son los que el
  proyecto acabara usando. Los cinco hallazgos de `R-017` quedan `Aceptado — pendiente` hasta que
  una auditoria posterior verifique la correccion sobre este commit.

---

### S-019 - Se aceptan `F-045` a `F-047` (`T-066` a `T-068`, `D-077`); nace `_phases/025_wslt.md` y su reparto (`D-078` a `D-080`)
| Campo | Valor |
|---|---|
| Fecha | 2026-09-03 |
| Etapa | `000_preproject` |
| Tareas | T-066, T-067, T-068, T-069, T-070, T-071 |

- **Que se hizo:** `manager` evaluo, contra `HEAD` (`ac31884`), los tres hallazgos de `R-018` (sobre
  `S-018`) y los acepto todos. `F-045`: la seccion 7 de `_audit/S-018.md` publicaba 28 lineas donde
  son 26, decia que no habia repetidas cuando hay tres, y dejaba una orden sin salida; nota fechada
  con las cifras correctas, sin reescribir el informe (`T-066`). `F-046`: la seccion 1 de ese
  informe atribuia a `L-020` una nota que el commit pone en `L-019`; nota fechada con la atribucion
  derivada del diff (`T-067`). `F-047`: el patron ampliado de `D-073` seguia ciego a `H-`, el hito;
  se sustituye por un patron **derivado** de la tabla «Codigos» de `project.md` y de §46 de
  `_methodology/000_method.md` en vez de escrito a mano (`D-077`, `T-068`). Nace `L-027`: los tres
  hallazgos comparten la misma forma —una lista derivable escrita a mano— y el Paso 2d y el Paso 6b
  de `protocol-close` se endurecen para numerar, atribuir y derivar patrones con una orden en vez de
  a ojo. Aparte, a peticion del usuario, nace la etapa `025_wslt` —el esqueleto que camina—: el
  archivo de etapa `_phases/025_wslt.md`, portado de un borrador propio del usuario de otro
  proyecto y adaptado al agnosticismo y a los codigos de este repositorio (`D-078`, `T-069`); su
  quinto artefacto, el acta del esqueleto, con plantilla en `_templates/025_wslt/005_skeleton_record.md`
  porque un test en verde no demuestra ni el rojo previo, ni la comprobacion desde fuera, ni lo que
  rompio el despliegue (`D-079`, `T-070`); y `_workflow/025_wslt.md`, el reparto Humano/Software/IA
  de los seis pasos, que deja el despliegue y el empuje de historial fuera de lo que la IA puede
  ejecutar por ser accion irreversible, y por eso puntua el eje «Impacto de un error» en 2 de forma
  condicional a ese reparto (`D-080`, `T-071`; nace `A-007`). Ninguna de las tres etapas queda
  adoptada. El cierre de esta sesion encontro ademas siete lineas nuevas con el caracter de control
  `0x08` —el mismo defecto que `DT-003`— dentro y alrededor de `D-077` en `decisions.md` y de `T-068`
  en `tasks.md`; se propone `DT-004`, sin tocar ninguna de las dos.
- **Que quedo abierto:** `T-001`, `T-002` y `T-003` siguen `No implementada`. `010_prototype` sigue
  sin adoptarse en `project.md` (`D-060`). Las tres etapas nuevas de `025_wslt` no quedan adoptadas
  ni su reparto. `DT-003` y `DT-004` siguen `No implementada` y `Propuesta (pendiente del usuario)`.
  `A-006` y `A-007` quedan abiertos. Los tres hallazgos de `R-018` quedan `Aceptado — pendiente`
  hasta que una auditoria posterior verifique la correccion sobre este commit.

  📌 **Nota del 2026-09-04 (`T-075`, hallazgo `F-050`).** La frase de arriba cuenta mal:
  **`025_wslt` es una etapa, no tres.** Lo que no queda adoptado es esa unica etapa, cuyos **tres
  archivos** —`_phases/025_wslt.md`, `_templates/025_wslt/005_skeleton_record.md` y
  `_workflow/025_wslt.md`— si nacen en este commit:

```
$ git diff --name-only --diff-filter=A 1b30e16^ 1b30e16 | grep 025_wslt
_phases/025_wslt.md
_templates/025_wslt/005_skeleton_record.md
_workflow/025_wslt.md
```

  La entrada se deja tal cual se escribio (`D-019`); se lee con esta nota. El recuento de etapas
  declaradas sigue siendo el de la tabla «Etapas» de `project.md`, y `T-002` es quien lo cambia.

### S-020 - Se aceptan `F-048` a `F-050` (`T-072` a `T-075`, `D-081`); nace el Paso 2e de `protocol-close` y `_phases/030_growth.md` (`D-082`)
| Campo | Valor |
|---|---|
| Fecha | 2026-09-04 |
| Etapa | `000_preproject` |
| Tareas | T-072, T-073, T-074, T-075, T-076 |

- **Que se hizo:** `manager` evaluo, contra `HEAD` (`c2a98b5`), los tres hallazgos de `R-019` (sobre
  `S-019`) y los acepto todos. `F-048`: la seccion 7 de `_audit/S-019.md` publicaba 42 de las 48
  lineas que devuelve su propia orden, con recuentos derivados de esa lista truncada; nota fechada
  con las cifras reales —48 lineas, 37 ordenes distintas, 11 repetidas— y la salida de las seis
  posiciones que faltaban, sin reescribir el informe (`T-072`). `F-049`: `DT-004` declaraba siete
  lineas nuevas con `0x08` en dos archivos, contadas a mano sobre los dos que el Paso 6 del cierre
  anterior tenia delante, cuando el barrido del commit entero da diez en cuatro; nota fechada con los
  dos barridos, escrita por `manager` bajo la excepcion puntual que abre `D-081` —acotada a corregir
  un dato factual sin tocar `Estado`, `Confirmacion` ni el titulo de la entrada— (`T-073`). `F-050`:
  dos frases llamaban «las tres etapas nuevas de `025_wslt`» a los tres archivos de una sola etapa;
  nota fechada en los dos sitios (`T-075`). Nace `L-028`: el conjunto sobre el que corre un recuento
  tiene que derivarse del diff, igual que la lista misma (`L-027`); por eso nace el **Paso 2e** de
  `protocol-close` (`T-074`), que barre caracteres de control sobre los archivos que el commit toca
  —derivados de `git diff --cached --name-only`— y publica el resultado en la nueva seccion 8 del
  informe, tambien cuando sale vacio. Aparte, a peticion del usuario, nace `_phases/030_growth.md`
  (`D-082`, `T-076`): la etapa que hace crecer el producto colgando slices de un esqueleto que ya
  camina, portada de un borrador del usuario y adaptada al agnosticismo del repositorio; no instancia
  ningun codigo de producto porque la guia de metodo colisiona el prefijo de la tarea de producto con
  el que `project.md` ya usa para la tarea de jornada, y esa colision queda para la etapa de la
  baseline.
- **Que quedo abierto:** `T-001`, `T-002` y `T-003` siguen `No implementada`. `010_prototype`,
  `025_wslt` y `030_growth` siguen sin adoptarse en `project.md`. `DT-003` y `DT-004` (con ambito
  ampliado a diez lineas en cuatro archivos) siguen `No implementada` y
  `Propuesta (pendiente del usuario)`. `A-006` y `A-007` quedan abiertos. Los tres hallazgos de
  `R-019` quedan `Aceptado — pendiente` hasta que una auditoria posterior verifique la correccion
  sobre este commit.

> 📌 **Nota del 2026-09-05 (`T-080`, hallazgo `F-054`).** La enumeracion de etapas sin adoptar
> de esta viñeta **esta corta: nombra tres y son cuatro.** Falta `020_baseline`, que tiene archivo de
> etapa, plantillas en `_templates/020_baseline/` y reparto en `_workflow/020_baseline.md`. La lista se
> deriva —no se escribe a mano— restando las declaradas a los archivos de `_phases/`, anclada al
> commit que esta viñeta describe:
>
> ```
> $ comm -23 <(git ls-tree --name-only f09d1f7 _phases/ | sed 's|_phases/||; s|\.md$||' | sort) <(git show f09d1f7:project.md | grep 'Etapas declaradas' | grep -oE '`[a-z0-9_]+`' | tr -d '`' | sort)
> 010_prototype
> 020_baseline
> 025_wslt
> 030_growth
> ```
>
> ⚠️ **Y es exactamente la forma de `L-027`/`L-028`:** una lista derivable con una orden,
> escrita de memoria. `T-002` saca de aqui cuales son las etapas que faltan por declarar, asi que una
> etapa que se cae de la enumeracion es una etapa que nadie recuerda declarar. `T-082` hace que el
> cierre la derive en vez de escribirla.

---

### S-021 - Se aceptan `F-051` a `F-054` (`T-077` a `T-082`); nace el Paso 7c de `protocol-close` (`D-084`) y las plantillas de `_templates/030_growth/` (`D-085`, `T-083`)
| Campo | Valor |
|---|---|
| Fecha | 2026-09-05 |
| Etapa | `000_preproject` |
| Tareas | T-077, T-078, T-079, T-080, T-081, T-082, T-083 |

- **Que se hizo:** `manager` evaluo, contra `HEAD` (`628fd47`), los cuatro hallazgos de `R-020`
  (sobre `S-020`) y los acepto todos. `F-051`: la seccion 8 de `_audit/S-020.md` igualaba catorce
  lineas de control con «los diez casos que `DT-004` documenta», sin serlo; nota fechada que separa
  las dos cuentas, y la linea de `_audit/findings.md` que no cabe en ninguna de las dos deudas nace
  como `DT-005` (`T-077`, `D-083`). `F-052`: la seccion 1 del informe prometia una nota de cierre con
  la lista de archivos anclada al commit que nunca se pego; se pega ahora, con `f09d1f7` y sus once
  archivos (`T-078`). `F-053`: la cabecera pedia una orden en vez de un hash, y esa orden devolvia el
  commit de anclaje (`3ff670e`) en vez del commit de la sesion (`f09d1f7`); nota que fija el hash
  literal (`T-079`). `F-054`: las dos viñetas de este archivo que enumeran etapas sin adoptar
  nombraban tres y son cuatro —faltaba `020_baseline`—; nota fechada en las dos (`T-080`). De fondo,
  `F-052` y `F-053` son el mismo defecto —tres datos del informe no pueden estar completos mientras
  se escribe, porque su commit aun no existe—, y `D-084`/`T-081` lo corrigen en el protocolo: nace el
  **Paso 7c** de `protocol-close` (un commit de anclaje posterior al push que rellena cabecera, nota
  de la seccion 1 y nota de la seccion 7 en una sola pasada, y nombra cual de los dos commits es «el
  commit de la sesion»), y `protocol-audit` deja de fiarse de la orden derivada y reconoce un commit
  de anclaje por su `--stat` de un solo archivo. `T-082`/`F-054` dan al Paso 3 del cierre el recuadro
  que exige derivar con `comm -23` cualquier lista que una orden pueda producir. Aparte, a peticion
  del usuario, nacen las tres plantillas de `_templates/030_growth/` —iteracion, slice y ventana de
  observacion— sin instanciar ningun codigo de producto, porque `slice`, `tarea de producto` y `caso
  de prueba` no estan en la tabla «Codigos» de `project.md` (`D-085`, `T-083`). `_workflow/030_growth.md`
  sigue sin existir, asi que la etapa sigue sin poder abrirse. Nace `A-008` y `L-029`.
- **Que quedo abierto:** `T-001`, `T-002` y `T-003` siguen `No implementada`. `010_prototype`,
  `020_baseline`, `025_wslt` y `030_growth` siguen sin adoptar en `project.md`.
  `_workflow/030_growth.md` sigue sin existir. `DT-002`, `DT-003`, `DT-004` y `DT-005` siguen `No
  implementada` y `Propuesta (pendiente del usuario)`. `A-006`, `A-007` y `A-008` quedan abiertos. Los
  cuatro hallazgos de `R-020` quedan `Aceptado — pendiente` hasta que una auditoria posterior
  verifique la correccion sobre este commit.

---

### S-022 - Se aceptan `F-055` a `F-058` (`T-084` a `T-090`); nace el Paso 1c de `protocol-close` y `_workflow/030_growth.md` (`D-091`)
| Campo | Valor |
|---|---|
| Fecha | 2026-09-06 |
| Etapa | `000_preproject` |
| Tareas | T-084, T-085, T-086, T-087, T-088, T-089, T-090, T-091, T-092 |

- **Que se hizo:** `manager` evaluo, contra `HEAD` (`e1d1b54`), los cuatro hallazgos de `R-021`
  (sobre `S-021`): `F-055` a `F-058`. Los cuatro se aceptan. `F-055` (`T-084`, `D-086`): se quitan de
  la cabecera de una nota de `_phases/030_growth.md` los dos codigos instanciados (`T-083`, `D-085`)
  que eran la unica ocurrencia de esa clase de fuga en toda la carpeta; el bloque de verificacion de
  la nota no se toca. `T-085`/`D-087` dan al cierre el **Paso 1c**: cero codigos instanciados en
  `_phases/` y `_workflow/`. `F-056` (`T-086`): la salida pegada en esa misma nota no era la que
  devolvia su orden (comillas de mas); nota fechada con la orden real y su salida. `F-057` (`T-087`,
  `T-089`, `D-088`): los criterios de cierre de `D-083` y `D-084` publicaban seis ordenes sin salida;
  reciben su nota con las ordenes ancladas a `76a2cb6` y su salida, y `decisions.md` fija la forma del
  bloque en tres partes siempre. `F-058` (`T-088`, `D-089`): `_audit/S-021.md` conservaba dos lineas
  de instruccion de plantilla; no se borran, reciben nota fechada, y el Paso 6b del cierre gana el
  control que exige cero lineas `^<` antes del `git add`. Ademas, dos recomendaciones sin hallazgo de
  `R-021`: `D-090` hace que `_audit/index.md` publique el hash literal de la cabecera del informe, no
  el derivado; y, a peticion del usuario, nace `_workflow/030_growth.md` (`D-091`, `T-091`), con lo
  que las dos condiciones de entrada del §5 de `_phases/030_growth.md` quedan cumplidas. Hallazgo
  propio (`T-092`): la fila de `L-029` en el indice de `lessons.md` tenia cinco campos en vez de
  siete. Nacen `A-009` y `L-030`. Esta misma sesion escribe dos pasos nuevos en su propia skill de
  cierre, `protocol-close`: el Paso 1c (arriba) y un control de huecos de plantilla en el Paso 6b.
- **Que quedo abierto:** `T-001`, `T-002` y `T-003` siguen `No implementada`. `010_prototype`,
  `020_baseline`, `025_wslt` y `030_growth` siguen sin adoptar en `project.md`, aunque las cinco
  entradas de `030_growth` ya estan completas. `DT-002` a `DT-005` siguen `No implementada` y
  `Propuesta (pendiente del usuario)`. `A-006` a `A-009` quedan abiertos. Los cuatro hallazgos de
  `R-021` quedan `Aceptado — pendiente` hasta que una auditoria posterior verifique la correccion
  sobre este commit. El Paso 2d de este mismo cierre encontro que el bloque «Criterio de cierre» de
  `D-088` es autorreferencial: su segunda orden, re-ejecutada, encuentra tres coincidencias en vez de
  la una publicada, porque el propio bloque cita el texto que busca. Queda senalado para que
  `manager` decida si se ancla al commit o se reformula.

---

### S-023 - Se aceptan `F-059` a `F-061` (`T-093` a `T-096`); nacen los Pasos 7c-bis y 7d de `protocol-close`, y el Gate 2 (`D-094`)
| Campo | Valor |
|---|---|
| Fecha | 2026-09-06 |
| Etapa | `000_preproject` |
| Tareas | T-093, T-094, T-095, T-096 |

- **Que se hizo:** `manager` evaluo, contra `HEAD` (`97bb948`), los tres hallazgos de `R-022` (sobre
  `S-022`): `F-059` a `F-061`. Los tres se aceptan. `F-059` (`T-093`, `T-094`, `D-092`): las seis
  decisiones nacidas en `97bb948` publicaban 18 ordenes de «Criterio de cierre» y solo 2 ancladas;
  reciben nota fechada republicando las 16 restantes ancladas a `97bb948` con su salida — la
  reejecucion encontro que el bloque de `D-088` es autorreferencial y no reproduce, documentado sin
  corregirse (`D-019`). Nace el **Paso 7c-bis** de `protocol-close`: despues del commit, el cierre
  ancla las ordenes de «Criterio de cierre» de las decisiones nacidas en esa misma sesion y pega su
  salida — unica excepcion mecanica a que el cierre no escribe en los cuatro archivos del porque.
  `F-060` (`T-095`, `D-093`): `S-022` iba dos dias por delante de su commit; el barrido completo
  (publicado en `_audit/index.md`) encontro ocho filas desfasadas de veintidos, desde `S-006`; no se
  reescriben. Nace el **Paso 7d**: la fecha se deriva con `date +%F` y se contrasta contra el commit.
  `F-061` (`T-096`): dos convenciones seguian prescribiendo la orden que `D-090` ya rechazaba;
  corregidas. Ademas, a peticion del usuario, nace el **Gate 2** (`D-094`): `gate2_auditor`,
  `protocol-gate2` y `_templates/035_gate2/005_verdict.md`, con tres comprobaciones propias (mide la
  MEDICION, exige generadores reales de uso, separa adopcion de recurrencia). Nacen `C-008` (finales
  de linea mixtos, no se normalizan), `L-031` (un guion que trunca antes de escribir destruyo
  `_audit/index.md`, recuperado con `git show HEAD:`) y `L-032` (sustitucion literal fallida por
  CRLF/LF mixto). Nace `A-010`: el anclaje del Paso 7c-bis se declara mecanico sin haberse ejecutado
  todavia. Ninguna etapa nueva queda adoptada.
- **Que quedo abierto:** `T-001`, `T-002`, `T-003`, `T-037` y `T-038` siguen `No implementada`.
  `010_prototype`, `020_baseline`, `025_wslt` y `030_growth` siguen sin adoptar en `project.md`.
  `DT-002` a `DT-005` siguen `No implementada` y `Propuesta (pendiente del usuario)`. `A-006` a
  `A-010` quedan abiertos. Los tres hallazgos de `R-022` quedan `Aceptado — pendiente` hasta que una
  auditoria posterior verifique la correccion sobre este commit. La autorreferencia del criterio de
  cierre de `D-088`, senalada desde `S-022`, queda documentada por nota fechada sin corregir el
  bloque original — decidir si se ancla o se reformula sigue siendo del usuario. El Paso 7c-bis que
  esta sesion crea se ejecuta por primera vez en este mismo cierre, sobre `D-092`, `D-093` y `D-094`.

---

### S-024 - Se aceptan `F-062` a `F-065` (`T-097` a `T-100`); `A-010` se refuta y se acota (`D-099`); nace `_phases/040_evol.md` (`D-100`)
| Campo | Valor |
|---|---|
| Fecha | 2026-09-07 |
| Etapa | `000_preproject` |
| Tareas | T-097, T-098, T-099, T-100 |

- **Que se hizo:** `manager` evaluo, contra `HEAD` (`a661edd`), los cuatro hallazgos de `R-023`
  (sobre `S-023`): `F-062` a `F-065`. Los cuatro se aceptan. `F-062` (`T-097`, `D-095`): la primera
  ejecucion real del Paso 7c-bis borro tres lineas de prosa de `D-092`, incumpliendo la prohibicion
  que el propio paso estrenaba en el mismo commit (mientras que, en `D-093`, en la misma pasada, el
  paso cumplio); gana una frontera visible —solo se reescribe dentro del bloque de codigo de la orden
  y su salida—, la regla de que la linea del anclaje se anade y no sustituye, y la prohibicion de
  actualizar a pasado un texto en futuro; la prosa borrada se repone por nota fechada. `F-063`
  (`T-098`, `D-096`): el bloque «Contexto» de `D-092` publicaba dos ordenes sobre `HEAD` que dejaron
  de reproducir (`18`/`2` publicadas, `33`/`12` hoy); el ancla se exige ahora para toda orden de
  `decisions.md`, no solo el «Criterio de cierre», con la prohibicion de escribir `HEAD` dentro de
  una orden publicada; se republican ancladas a `20ef118`, con lo que devuelven `18` y `2`. `F-064`
  (`T-099`, `D-097`): el paso nombraba «un `ls`» como no anclable y su propia ejecucion lo anclo
  igual, y una orden partida en dos dejo la nota diciendo «Las cuatro» sobre cinco; se autoriza la
  reescritura de forma con la prueba «¿la forma anclada contesta lo mismo?» y una tabla de casos, el
  `ls` sale de la lista de no anclables, y la nota pasa a declarar el recuento contandolo. `F-065`
  (`T-100`, `D-098`): la seccion 0 de `_audit/S-023.md` llamo `HEAD` a `97bb948`, que era el commit
  auditado; `protocol-close` gana un bloque que distingue los dos commits de esa seccion, de donde
  sale cada uno, y la forma de la frase que los nombra. Ademas, `A-010` se refuta en su primera
  aplicacion real (el propio `F-062` es el control que la refuta) y, por decision del usuario, se
  **acota** en vez de retirarse (`D-099`) — contra la consecuencia que el propio supuesto habia
  pre-comprometido por escrito; nacen `L-033` y `L-034` sobre el borde visible que necesita una
  autorizacion de sustitucion y sobre como se renegocia un pre-compromiso sin ocultarlo. A peticion
  del usuario, tomando como guia un borrador que vivia en `temporal/`, nace `_phases/040_evol.md`
  (`D-100`): el archivo de la etapa de evolucion, con las mismas ocho secciones que sus hermanos, sin
  codigos de producto ni datos propios del proyecto, con su condicion de salida propia de cada
  iteracion (no del cierre de la etapa) y su cosecha por iteracion. No adopta la etapa.
- **Que quedo abierto:** `T-001`, `T-002`, `T-003`, `T-037` y `T-038` siguen `No implementada`.
  `010_prototype`, `020_baseline`, `025_wslt`, `030_growth` y `040_evol` siguen sin adoptar en
  `project.md`. `DT-002` a `DT-005` siguen `No implementada` y `Propuesta (pendiente del usuario)`.
  `A-006` a `A-009` quedan abiertos; `A-010` queda `Refutado`. Los cuatro hallazgos de `R-023` quedan
  `Aceptado — pendiente` hasta que una auditoria posterior verifique la correccion sobre este commit.
  La autorreferencia del criterio de cierre de `D-088` (senalada desde `S-022`) sigue sin resolver:
  esta sesion no la toco. `_phases/040_evol.md` declara faltantes, como condicion de entrada de su
  etapa, las plantillas de `_templates/040_evol/` y el reparto de `_workflow/040_evol.md`. `D-099`
  deja escrito que si el Paso 7c-bis vuelve a tocar prosa fuera de su bloque de codigo, la excepcion
  se retira sin discusion.

---

### S-025 - Se aceptan F-066 a F-069 (T-101 a T-104); nacen las plantillas de _templates/040_evol/ (D-105)
| Campo | Valor |
|---|---|
| Fecha | 2026-09-07 |
| Etapa | `000_preproject` |
| Tareas | T-101, T-102, T-103, T-104, T-105 |

- **Que se hizo:** `manager` evaluo, contra `HEAD` (`8959da8`), los cuatro hallazgos de `R-024`
  (sobre `S-024`): `F-066` a `F-069`. Los cuatro se aceptan. `F-066` (`T-101`, `D-101`): el Paso 7c
  exigia anclar cuatro sitios y `S-024` anclo tres, dejando la seccion 7 del informe sin su nota de
  cierre; `protocol-close` gana el recuadro que fija que esa nota es un **puntero** —hash, recuento
  por archivo y frase de cierre—, nunca una republicacion de las 41 ordenes, con un barrido universal
  que se detiene ante un archivo que el Paso 7c-bis no tiene autorizado tocar. `F-067` (`T-102`,
  `D-102`): `tasks.md` quedo con doce ordenes sin anclar tras el commit de anclaje de `S-024` — el
  mismo hecho de `F-059`, desplazado de archivo; el Paso 7c-bis pasa a anclar tambien `tasks.md`, que
  ya era del `session-closer`, y las doce se republican ancladas a `a1f5fa8`. `F-068` (`T-103`,
  `D-103`): la seccion 7 de `S-024` afirmo «41, sin repeticion» citando un `sort -u` que en realidad
  da 31; el Paso 2d exige ahora que la cifra accesoria vaya siempre con su propia orden y salida, y
  la afirmacion se corrige por nota fechada (`D-019`). `F-069` (`T-104`, `D-104`): dos notas del Paso
  7c-bis quedaron pegadas al `---` de `decisions.md`, que Markdown lee como encabezado; se anaden las
  dos lineas en blanco que faltaban y el paso exige esa linea de ahi en adelante. Nace `L-035`: una
  regla ampliada por el nombre del archivo donde dolio deja abierto el archivo de al lado; queda
  registrada en `A-011` la costumbre que hoy sostiene la asimetria «deteccion universal, escritura
  acotada». Por peticion del usuario nacen las dos plantillas que `_phases/040_evol.md` §5 exigia como
  condicion de entrada —`_templates/040_evol/005_iteration_NNN.md` y `010_slice_NNN.md`— (`D-105`); el
  archivo de etapa actualiza su tabla de estado y nace `T-105` para el reparto que aun falta
  (`_workflow/040_evol.md`). La etapa sigue sin adoptarse.
- **Que quedo abierto:** `T-001`, `T-002`, `T-003`, `T-037`, `T-038` y `T-105` siguen `No
  implementada`. Las cinco etapas con archivo de etapa siguen sin adoptar en `project.md`. `DT-002` a
  `DT-005` siguen `Propuesta (pendiente del usuario)`. `A-006` a `A-009` y `A-011` quedan abiertos;
  `A-010` sigue `Refutado`. Los cuatro hallazgos de `R-024` quedan `Aceptado — pendiente` hasta que
  una auditoria posterior verifique la correccion sobre este commit. La autorreferencia del criterio
  de cierre de `D-088` sigue sin resolver.

---

### S-026 - Se aceptan F-070 a F-073 (T-106 a T-109); nace _workflow/040_evol.md, sin adoptar (D-110)
| Campo | Valor |
|---|---|
| Fecha | 2026-09-07 |
| Etapa | `000_preproject` |
| Tareas | T-106, T-107, T-108, T-109, T-105 |

- **Que se hizo:** `manager` evaluo, contra `HEAD` (`3bf61d4`), los cuatro hallazgos de `R-025`
  (sobre `S-025`): `F-070` a `F-073`. Los cuatro se aceptan. `F-070` (`T-106`, `D-106`): la nota de
  cierre de `S-025` §7 se etiquetaba «sobre `HEAD` (`f1f2291`)» con una orden hibrida —lista del
  commit, contenido del arbol de trabajo—, y su salida `2/2/14` correspondia al estado posterior al
  anclaje, no a `f1f2291` (`2/22/28`); el Paso 7c exige ahora forma anclada siempre (`cat` y `HEAD`
  prohibidos) y que la nota nombre el commit de su salida, con la nota fechada que republica la
  comprobacion contra los dos commits. `F-071` (`T-107`, `D-107`): el barrido debia salir VACIO y en
  su primera ejecucion devolvio tres lineas sin `D-XXX` que respaldara la excepcion escrita en prosa;
  se parte en un CENSO universal que informa y un CONTROL —tambien universal y anclado— cuya
  condicion de parada es que todo archivo de su salida este autorizado por el Paso 7c-bis. `F-072`
  (`T-108`, `D-108`): el recuento accesorio de `S-025` publico 27 ordenes distintas siendo 22, y
  «las mismas ocho» siendo trece; se corrige por nota fechada. `F-073` (`T-109`, `D-109`): la frase
  de cierre de `S-025` contradecia a su propia nota y publicaba cifras sin orden (32 anclas de 35,
  no 34; 34 anclas totales con dos fuera de la lista por el filtro del Paso 2d; 18 lineas del
  barrido, no 16); se corrige por nota fechada y el recuadro exige ahora construir la frase con las
  salidas de los barridos, nunca recontando a mano. Nace `L-036`: una condicion de parada
  inalcanzable se convierte en excepcion redactada en prosa cada vez, y esa prosa es donde entraron
  `F-070`, `F-072` y `F-073`. El criterio de refutacion de `A-011` se sustituye por uno que se valida
  contra los bloques «Criterio de cierre» (`D-107`); nace `A-012` sobre la doble lectura de «usuarios
  reales» en `ai_levels.md` §6. Por peticion del usuario nace `_workflow/040_evol.md` (`D-110`): el
  reparto de la etapa de la evolucion, con una fila por cada uno de sus ocho pasos y lectura de nivel
  de sistema de IA en 6 —la unica del metodo—; se escribe y **no se adopta**, `_phases/040_evol.md`
  §5 pasa a decir «escrito, sin adoptar», y `T-105` se marca `Implementada` con su criterio acotado a
  lo que esta decision cubre. La etapa sigue sin adoptarse.
- **Que quedo abierto:** `T-001`, `T-002`, `T-003`, `T-037` y `T-038` siguen `No implementada`. Las
  cinco etapas con archivo de etapa siguen sin adoptar en `project.md`, y `040_evol` ademas necesita
  el `D-XXX` de adopcion de su reparto ya escrito. `DT-002` a `DT-005` siguen `Propuesta (pendiente
  del usuario)`. `A-006` a `A-009` y `A-012` quedan abiertos; `A-010` sigue `Refutado`; `A-011` sigue
  abierto con su criterio corregido. Los cuatro hallazgos de `R-025` quedan `Aceptado — pendiente`
  hasta que una auditoria posterior verifique la correccion sobre este commit. La autorreferencia del
  criterio de cierre de `D-088` sigue sin resolver.

---

### S-027 - Se aceptan F-074 y F-075 (T-110, T-111); un codigo instanciado pasa a ser dato propio (D-113 a D-115); CLAUDE.md y .claude/ quedan agnosticos
| Campo | Valor |
|---|---|
| Fecha | 2026-09-07 |
| Etapa | `000_preproject` |
| Tareas | T-110, T-111, T-112, T-113, T-114, T-115 |

- **Que se hizo:** `manager` evaluo, contra `HEAD` (`3aadf62`), los dos hallazgos de `R-026` (sobre
  `S-026`): `F-074` y `F-075`. Los dos se aceptan. `F-074` (`T-110`, `D-112`): la NOTA DE CIERRE de
  `_audit/S-026.md` §7 afirmaba 29 ordenes ancladas («14 + 14 + 1») y fueron 28 — la `ls-tree` de
  `T-105` era la primera de las 14 de `tasks.md`, no una decimoquinta, y se conto dos veces; quedan
  ademas 2 lineas con `<hash>` deliberadas. Se corrige por nota fechada (28/27/2) y el recuadro de la
  NOTA DE CIERRE pasa a prohibir la aritmetica de prosa. `F-075` (`T-111`, `D-111`): `S-026` habia
  borrado y sustituido la linea del «Criterio de cierre» de `T-105`, nacida en `S-025` y ya auditada;
  se restaura literal, con nota fechada encima. Nace `L-037`: un criterio que cita el mismo texto que
  su correccion transcribe se acierta a si mismo sin anclas `^`/`$`.

  Por peticion separada del usuario se declara que un codigo instanciado del registro es un dato
  propio que el Paso 1b no detecta (`D-113`): 55 citas en `.claude/` (52) y `CLAUDE.md` (3), con
  `_phases/` y `_workflow/` ya en cero. Se elige limpiar conservando el hecho (`D-114`): `T-114`
  aplica a `CLAUDE.md` (tres citas fuera, entra la convencion); `T-115` aplica a los tres archivos de
  `.claude/` (54 lineas), genericizando tambien tres ejemplos que el control no marcaba. El caso que
  **cuenta** hallazgos se resuelve cambiando el sujeto de «este repositorio» a «este metodo»
  (`D-115`). `.claude/` queda en cero codigos instanciados. `T-112` (segundo barrido del Paso 1b)
  queda sin implementar.
- **Que quedo abierto:** `T-001`, `T-002`, `T-003`, `T-037`, `T-038` y `T-112` siguen
  `No implementada`. `DT-002` a `DT-006` siguen `Propuesta (pendiente del usuario)` —`DT-006` nace
  esta sesion, cuatro lineas con `0x08` en `assumptions.md` (`A-013`), que `session-closer` no puede
  corregir por no ser suyo el archivo. `A-006` a `A-009`, `A-012` y `A-013` quedan abiertos. Los dos
  hallazgos de `R-026` quedan `Aceptado — pendiente` hasta que una auditoria posterior verifique la
  correccion sobre este commit. La autorreferencia del criterio de cierre de `D-088` sigue sin
  resolver.

---

### S-028 - Nace `_templates/000_preproject/` (D-116) y se realinea `_phases/000_preproject.md` con el andamiaje real (D-117)
| Campo | Valor |
|---|---|
| Fecha | 2026-09-08 |
| Etapa | `000_preproject` |
| Tareas | — |

- **Que se hizo:** el usuario pregunto si podia llevarse el andamiaje a un proyecto nuevo con solo
  los seis archivos agnosticos, `_audit/`/`_brief/` vacias, `_persistence/` con encabezados y
  `project.md` vacio; la respuesta fue que no, porque `project.md` vacio deja sin poder ejecutarse a
  varios controles del cierre y el registro no viaja al no llevar plantilla. Nace
  `_templates/000_preproject/` con diez plantillas en blanco —una por cada archivo del andamiaje sin
  plantilla propia hasta hoy—, con cabecera, indice vacio y convenciones integras genericizadas, y
  en cero en los dos barridos de agnosticismo (`D-116`). Al escribir su criterio de cierre con un
  script de Python, un patron `\b` llego al archivo como `0x08`; se detecto al reejecutar la orden y
  se corrigio sin commitear (`L-038`). Nace `A-014`: que las diez plantillas basten para arrancar un
  proyecto desde cero sigue sin comprobarse.

  Por peticion del usuario se releyo entero `_phases/000_preproject.md`: describia seis carpetas
  donde ya hay ocho y tres agentes donde ya hay cinco, con su condicion de salida diciendose «espejo
  de los cinco entregables» sin serlo (`L-039`). Se realinea (`D-117`): la condicion de salida pasa
  de ocho a diez casillas agrupadas por procedencia (5 espejo, 2 que la etapa se exige a si misma
  —incluida la copiabilidad del metodo, nueva—, 1 a la auditoria, 2 de lecciones globales); entra la
  casilla de `project.md` completo; `_templates/`, `_workflow/` y `.gitignore` entran en el arbol de
  artefactos; y «los tres agentes» pasa a «los cinco», con los dos de Gate exigidos como montados, no
  ejecutados. Nace `A-015`: que todo proyecto quiera los dos Gates montados desde esta etapa es un
  supuesto del usuario, tomado contra la recomendacion de `manager`.
- **Que quedo abierto:** `T-001`, `T-002`, `T-003`, `T-037`, `T-038` y `T-112` siguen
  `No implementada`. `010_prototype`, `020_baseline`, `025_wslt`, `030_growth` y `040_evol` siguen sin
  adoptar en `project.md`. `DT-002` a `DT-006` siguen `Propuesta (pendiente del usuario)`. `A-006` a
  `A-009`, `A-012` a `A-015` quedan abiertos; `A-010` sigue `Refutado`; `A-011` sigue abierto. Los
  cuatro hallazgos de `R-027` (`F-076` a `F-079`) siguen `Abierto`: esta sesion no los evaluo. El
  Paso 2d de este cierre encontro que el recuento publicado en la verificacion de `D-117`
  (`grep -rn '_workflow' _phases/ | grep -c .`) da 19 en la entrada y 20 al reejecutarlo contra el
  mismo `acb3359` que la entrada declara; queda senalado para `manager`, sin corregir por no ser
  `decisions.md` un archivo de este cierre. La autorreferencia del criterio de cierre de `D-088`
  sigue sin resolver.

---

### S-029 - Se aceptan F-076 a F-082 (T-116 a T-122); nace el acta de cierre de etapa (D-121 a D-123)
| Campo | Valor |
|---|---|
| Fecha | 2026-09-08 |
| Etapa | `000_preproject` |
| Tareas | T-116, T-117, T-118, T-119, T-120, T-121, T-122 |

- **Que se hizo:** se evaluaron, verificados contra `HEAD`, los siete hallazgos abiertos de `R-027`
  y `R-028` (`F-076` a `F-082`); los siete se aceptan y quedan `Aceptado — pendiente` con su `T-XXX`.
  Cinco se corrigen por nota fechada sin reescribir lo commiteado (`D-019`): cifras de volumen de
  `T-115` (`F-076`), el recuento `113`/`121` de `A-013`/`D-114` (`F-077`), el total sumado en prosa de
  la NOTA DE CIERRE de `S-027` (`F-078`), el `19`/`20` del bloque de `D-117` (`F-080`), y la prosa que
  el Paso 7c-bis borro en `D-117` (`F-081`, reincidencia exacta de `F-062`). Dos amplian reglas hacia
  adelante: `CLAUDE.md` distingue ahora «serie consecutiva de un ejemplo trabajado» de una cita del
  registro (`F-079` → `D-118`), y `protocol-close` exige que todo recuento por archivo de la seccion 1
  vaya con su orden (`F-082` → `D-120`). Por la reincidencia de `F-081`, el Paso 7c-bis gana el
  CONTROL DE PROSA BORRADA: compara la prosa fuera de bloques de codigo antes y despues del anclaje y
  se detiene si algo desaparecio (`D-119`; `L-040`, que generaliza: una prohibicion que ya reincidio
  se corrige con un control, no con mas texto). Aparte de los hallazgos, a peticion del usuario nace
  el **acta de cierre de etapa**: generica, con dos firmas que no se sustituyen —tecnica de un agente
  nuevo que arranca en frio, y aprobacion del usuario como patrocinador— y enganchada como entrada de
  la etapa siguiente (`D-121`); el agente es **uno solo**, `phase_exit_auditor`, con su skill
  `protocol-phase-exit`, generico para las siete etapas (`D-122`, nace `A-016`); y la cosecha de
  lecciones va **antes** de la firma, con un hueco declarado y sin resolver —quien escribe en el
  repositorio de lecciones globales— (`D-123`, `T-127` bloqueante; nace `A-017`). Nace `L-041`: un
  criterio sin artefacto donde firmarse no falla hasta que alguien intenta cerrar. Los controles de
  fuga (1b, 1c) y de indices (2b) del cierre salen limpios; el Paso 2c repite las dos diferencias ya
  documentadas.
- **Que quedo abierto:** `T-001`, `T-002`, `T-003`, `T-037`, `T-038` y `T-112` siguen
  `No implementada`. `T-123` a `T-129` —todo lo que construye el acta— quedan `No implementada`;
  `T-127` es bloqueante de la cosecha, no de la sesion. `010_prototype`, `020_baseline`, `025_wslt`,
  `030_growth` y `040_evol` siguen sin adoptar en `project.md`. `DT-002` a `DT-006` siguen
  `Propuesta (pendiente del usuario)`. `A-006` a `A-009`, `A-011` a `A-017` quedan abiertos; `A-010`
  sigue `Refutado`. La autorreferencia del criterio de cierre de `D-088` sigue sin resolver.

---

### S-030 - Se aceptan F-083 a F-086 (T-130 a T-135); se construye el acta de cierre de etapa y el sexto agente `phase_exit_auditor` (T-123 a T-125)
| Campo | Valor |
|---|---|
| Fecha | 2026-09-08 |
| Etapa | `000_preproject` |
| Tareas | T-123, T-124, T-125, T-130, T-131, T-132, T-133, T-134, T-135 |

- **Que se hizo:** se evaluaron, verificados contra `HEAD`, los cuatro hallazgos abiertos de `R-029`
  (`F-083` a `F-086`); los cuatro se aceptan y quedan `Aceptado — pendiente` con su `T-XXX`. `F-083`
  y `F-084` se corrigen por nota fechada en `_audit/S-029.md` sin reescribir su prosa (`D-019`), y de
  fondo suprimen la cifra de ordenes distintas del Paso 2d — tercera vez que sale falsa, ninguna otra
  parte del protocolo la consume (`D-124`; `L-042`) — y anaden dos contrastes obligatorios a la tabla
  del Paso 2e (`D-125`). `F-085` completa la serie `SC-` del ejemplo de trazabilidad y fija que el
  ambito de la regla de series es la union de los seis archivos/carpetas agnosticos (`D-126`). `F-086`
  hace que el Paso 7c-bis publique la salida del CONTROL DE PROSA BORRADA en la NOTA DE CIERRE,
  tambien cuando sale limpia (`D-127`). Aparte de los hallazgos, se construye el acta de cierre de
  etapa completa que `S-029` habia dejado decidida: nace `_templates/phase_exit_record.md`, en la
  raiz de `_templates/` por el `git ls-tree` no recursivo del criterio de `D-121` (`D-128`, `T-123`);
  nace el agente `phase_exit_auditor` con su skill `protocol-phase-exit`, corriendo con `sonnet`
  (`D-129`, `T-124`); y `_phases/000_preproject.md` sube su casilla 2 de cinco a seis agentes
  (`T-125`). Al recorrer con el mismo procedimiento dos etapas distintas, `A-016` queda **Confirmado**
  con acotacion: la mitad mecanica es uniforme en las siete, la de juicio se resuelve con
  `NO COMPROBABLE` (`L-043`). Nace `L-044`: una premisa cuantificada sobre el propio repositorio se
  comprueba con una orden, no se asume — cazada al escribir el criterio de cierre de `D-129`. Los
  controles de fuga (1b, 1c) y de indices (2b) del cierre salen limpios; el Paso 2c repite las dos
  diferencias ya documentadas.
- **Que quedo abierto:** `T-001`, `T-002`, `T-003`, `T-037`, `T-038` y `T-112` siguen
  `No implementada`. `T-126` a `T-129` quedan `No implementada`, `T-127` bloqueante de la cosecha.
  `010_prototype`, `020_baseline`, `025_wslt`, `030_growth` y `040_evol` siguen sin adoptar en
  `project.md`. `DT-002` a `DT-006` siguen `Propuesta (pendiente del usuario)`. `A-006` a `A-009`,
  `A-011` a `A-015` y `A-017` quedan abiertos; `A-010` `Refutado`; `A-016` pasa a `Confirmado`. La
  autorreferencia del criterio de cierre de `D-088` sigue sin resolver.

---

### S-031 - Se aceptan `F-087` a `F-090` (`T-136` a `T-141`); nace la skill `protocol-harvest` (`T-142`) y se cierra el enganche del acta (`T-126`, `T-127`, `T-129`)
| Campo | Valor |
|---|---|
| Fecha | 2026-09-10 |
| Etapa | `000_preproject` |
| Tareas | T-126, T-127, T-129, T-136, T-137, T-138, T-139, T-140, T-141, T-142, T-143, T-144 |

- **Que se hizo:** `manager` evaluo los cuatro hallazgos abiertos por `R-030` sobre `S-030`
  (`F-087` a `F-090`), verifico cada uno contra `HEAD` (`b32193d`) y los acepto los cuatro. `F-087`
  (la seccion 4 del informe afirmaba «trece» supuestos abiertos donde la orden devuelve quince, y su
  propia enumeracion sumaba quince) y `F-088` (la NOTA DE CIERRE afirmaba «las 6 restantes» con un
  desglose que sumaba cinco) se corrigen por nota fechada en `_audit/S-030.md`, sin reescribir su
  prosa (`T-136`, `T-138`). De fondo, `protocol-close` gana dos reglas nuevas: la seccion 4 exige la
  salida cruda de su orden en vez de un recuento tecleado (`D-130`, `T-137`), y todo desglose de la
  NOTA DE CIERRE se deriva con una orden sobre el commit de anclaje o no se publica (`D-131`,
  `T-139`). `F-089` (la plantilla `_templates/000_preproject/005_project.md` no recibio la
  actualizacion de la fila `_audit/` que si recibio `project.md`) se corrige en la plantilla
  (`T-140`); nace `L-046`. `F-090` (el Paso 2e declara como ambito «los archivos que el commit toca»
  y mide el area de staging previa: `progress.md`, el informe y el tablero quedaban fuera, y la tabla
  publicada tenia catorce filas donde el commit lleva diecisiete) se resuelve con una segunda pasada
  obligatoria del Paso 2e, anclada al commit, publicada en la NOTA DE CIERRE aunque salga limpia
  (`D-132`, `T-141`); nace `L-045`.

  Aparte de los hallazgos, se cerro el enganche del acta de cierre de etapa que `S-029` y `S-030`
  habian dejado construido pero no enganchado. `D-133`/`T-142` decide quien cosecha y como: `manager`,
  nunca un agente nuevo (arranca en frio y no puede aplicar el filtro 2 de portabilidad sobre la etapa
  que cosecha) y nunca a mano; con una skill propia, `protocol-harvest`, que nace en esta sesion con
  nueve pasos y uso exclusivo de `manager`; y con una **puerta** antes de escribir en el repositorio
  de lecciones globales — clasificar y redactar es automatico, escribir/commitear/subir espera la
  aprobacion del usuario, entrada por entrada. `T-126` anade la tercera entrada obligatoria de
  `_phases/005_discovery.md`: el acta de cierre de la etapa anterior, levantada y firmada, sin la cual
  la etapa no puede empezar salvo excepcion deliberada con su `D-XXX`. `T-129`/`D-134` hace y registra
  la consulta de arranque a las lecciones globales por su indice: dos bloques (D — decisiones y
  arquitectura, E — corte del trabajo), 17 lecciones, y los ocho bloques restantes declarados
  `NO MIRADOS`, no limpios. Produce `T-143` (`LG-52`: el arranque reporta bloqueos leyendo solo
  `tasks.md`, dejando fuera quince supuestos `Abierto`) y `T-144` (`LG-54`: evaluacion y
  observabilidad no tienen dueño ni sitio, a diferencia de seguridad); confirma `T-037` sin abrirla de
  nuevo (`LG-38`); deja `LG-51`/`LG-53` como practica ya adoptada y grieta conocida sin tarea; y
  aplaza once lecciones que exigen producto, con su razon escrita. De paso, `A-017` queda
  `Confirmado`.

  Los controles de fuga (Pasos 1b y 1c) y de indices (Paso 2b) de este cierre salen limpios. El
  Paso 2c muestra las mismas dos diferencias ya conocidas y documentadas en `project.md`
  (`010_prototype/` y `temporal/`).
- **Que quedo abierto:** `T-001`, `T-002`, `T-003`, `T-037`, `T-038` y `T-112` siguen
  `No implementada`. `T-128` (la primera cosecha real) sigue `No implementada`, ya sin bloqueo —la
  skill que la ejecuta existe—, y corre solo cuando `000_preproject` se vaya a cerrar de verdad.
  `T-143` y `T-144`, nacidas esta sesion, siguen `No implementada`. `010_prototype`, `020_baseline`,
  `025_wslt`, `030_growth` y `040_evol` siguen sin adoptar en `project.md`. `DT-002` a `DT-006`
  siguen `Propuesta (pendiente del usuario)`. `A-006` a `A-009` y `A-011` a `A-015` quedan abiertos;
  `A-010` sigue `Refutado`; `A-016` y `A-017` quedan `Confirmado`. La autorreferencia del criterio de
  cierre de `D-088` sigue sin resolver.

---

### S-032 - Se aceptan `F-091` y `F-092` (`T-145` a `T-147`); el arranque lee los supuestos abiertos (`T-143`, `D-136`)
| Campo | Valor |
|---|---|
| Fecha | 2026-09-10 |
| Etapa | `000_preproject` |
| Tareas | T-143, T-145, T-146, T-147 |

- **Que se hizo:** `manager` evaluo los dos hallazgos abiertos por `R-031` sobre `S-031`
  (`F-091`, `F-092`), los verifico contra `HEAD` (`9bcc92f`) y los acepto los dos. `F-091` (la
  seccion 7 de `_audit/S-031.md` afirmaba «las 20 lineas 1 a 20 llevan `<hash>`» y la NOTA DE CIERRE
  «las 14 restantes de las 21»; de las 20, 19 llevan `<hash>` —la 15 lleva el hash historico
  `9b3f9ee`— y las restantes son 2, no 14) y `F-092` (la seccion 4 enumeraba once codigos de supuesto
  afirmando que «completan los catorce»; faltaban `A-001`, `A-002` y `A-003`) se corrigen por nota
  fechada en `_audit/S-031.md`, sin reescribir su prosa (`T-145`, `T-146`). De fondo, `T-147`
  generaliza la regla contra los recuentos tecleados a **todo** el informe, en cualquier seccion, no
  solo la del ultimo caso (`D-135`): las dos reglas nacidas en `S-031` se habian escrito cada una
  para su sitio, y el mismo commit que las estreno las incumplio un sitio mas alla —una cifra en la
  prosa de otra seccion, y una lista que la primera regla autorizaba expresamente a escribir a mano—.
  Nace `L-047`: una regla que nombra el sitio solo protege ese sitio.

  Aparte de los hallazgos, se implemento `T-143` (`D-134`, `LG-52`): el Paso 1b de `protocol-start`
  gana a `_persistence/assumptions.md` como quinto archivo obligatorio —indice y **cuerpo de los
  `Abierto`**, que es donde vive el disparador, no una columna nueva del indice (`D-136`)—, y el
  reporte gana un bloque fijo «Supuestos que tocan mirar», obligatorio aunque diga «ninguno». Al
  escribir su criterio de cierre broto `L-048`: el primer `grep` buscaba la frase que la fila movida
  llevaba antes, y la encontraba **citada** en la nota que explicaba por que se habia movido — un
  criterio de texto no distingue el defecto corregido de su propia explicacion.

  El disparador de `A-013` se activo por primera vez, al buscar el origen de `D-135` y `D-136` por su
  enunciado en `decisions.md`: las dos se encontraron. El supuesto no se cierra —habla de **cada**
  codigo quitado— pero el primer caso real salio a su favor.

  Los controles de fuga (Pasos 1b y 1c) y de indices (Paso 2b) de este cierre salen limpios. El
  Paso 2c muestra las mismas dos diferencias ya conocidas y documentadas en `project.md`
  (`010_prototype/` y `temporal/`).
- **Que quedo abierto:** `T-001`, `T-002`, `T-003`, `T-037`, `T-038` y `T-112` siguen
  `No implementada`. `T-128` (la primera cosecha real) sigue `No implementada`, sin bloqueo, y corre
  solo cuando `000_preproject` se vaya a cerrar de verdad. `T-144` sigue `No implementada`.
  `010_prototype`, `020_baseline`, `025_wslt`, `030_growth` y `040_evol` siguen sin adoptar en
  `project.md`. `DT-002` a `DT-006` siguen `Propuesta (pendiente del usuario)`. `A-006` a `A-009` y
  `A-011`, `A-012`, `A-014`, `A-015` quedan abiertos; `A-013` sigue `Abierto`, con su disparador
  activado una vez sin confirmar el supuesto; `A-010` sigue `Refutado`; `A-016` y `A-017` quedan
  `Confirmado`. La autorreferencia del criterio de cierre de `D-088` sigue sin resolver.

---

### S-033 - Se aceptan `F-093` y `F-094` (`T-148` a `T-151`); se adopta la secuencia de etapas (`D-142`) y se aplazan `T-001`, `T-003` y `T-144` (`D-143`)
| Campo | Valor |
|---|---|
| Fecha | 2026-09-10 |
| Etapa | `000_preproject` |
| Tareas | T-002, T-003, T-037, T-038, T-112, T-148, T-149, T-150, T-151 |

- **Que se hizo:** `manager` evaluo los dos hallazgos abiertos por `R-032` sobre `S-032` (`F-093`,
  `F-094`), los verifico contra `HEAD` (`0647d82`) y los acepto los dos. `F-093` (la seccion 8 de
  `_audit/S-032.md` publicaba «16 ocurrencias» donde sus propios operandos suman 17, el Contraste 2
  de la misma seccion lo confirma y su propio parrafo de cierre ya decia «17») y `F-094` (la seccion
  0 publicaba `Implementado` para `F-091`/`F-092`, que `findings.md` dejaba en `Aceptado —
  pendiente` en el mismo commit) se corrigen por nota fechada en `_audit/S-032.md`, sin reescribir su
  prosa (`T-148`, `T-150`).

  De fondo nacen dos controles mecanicos en `protocol-close`, porque las reglas de redaccion que
  perseguian este mismo defecto ya se habian reescrito dos veces y volvian a fallar en el commit que
  las estrenaba: el CONTROL DE CIFRA ADYACENTE del Paso 6b, acotado a la prosa pegada a un bloque de
  salida cruda —su respuesta correcta no es cero, devuelve del orden de diez lineas por informe y
  atrapa los dos defectos reales, frente a las ~130 lineas de ruido del barrido generico ya
  descartado (`D-137`, `T-149`)—; y el veredicto `Aceptado — corregido en este commit` sustituye a
  `Implementado` en la seccion 0, que deja de ofrecerse como opcion, con `protocol-audit` señalando
  su uso como hallazgo (`D-138`, `T-151`).

  Fuera de los hallazgos se cerraron cuatro tareas viejas. `T-112` se cierra **reformulada**: su
  premisa —que habia que anadir el control— era falsa, ya existia desde `S-022`; lo que si hacia
  falta era corregir que enumeraba ocho prefijos de dieciocho en uso y devolvia cero con la fuga
  inyectada de prueba. Pasa a reconocer codigos por **forma**, con `PI-` como unica exclusion
  (`D-139`; nacen `L-050` y `L-051`). `T-038` se cierra con mas alcance del pedido: los barridos de
  fuga de los dos protocolos quedan identicos en sus seis carpetas, y `protocol-audit` gana su propio
  control de codigos instanciados que no tenia en ninguna forma (`D-140`, con puerta del usuario por
  tratarse de la skill del agente que audita a `manager`). `T-037` se cierra escribiendo el
  inventario de acciones irreversibles como `C-009` de `constraints.md`, con sus dos tablas, en vez
  de un octavo archivo de persistencia (`D-141`). `T-002` se cierra adoptando la secuencia completa
  del metodo VERTICAL —siete etapas y sus dos Gates— en la tabla «Etapas» de `project.md`, y se
  descarta la secuencia del brief del cliente porque los siete archivos de etapa ya estaban escritos
  (`D-142`); declarar la secuencia no autoriza el trabajo de ninguna etapa.

  Por decision del usuario, que prioriza extraer del andamiaje un esqueleto reutilizable, se aplazan
  `T-001` y `T-144` —siguen `No implementada`, no `Suspendida`, porque pertenecen a una etapa no
  iniciada y nadie las ha pausado— y se suspende `T-003` —pertenece a la etapa activa, y su pausa si
  es una decision deliberada (`D-143`)—. `protocol-start` gana el bloque «Tareas de etapas no
  iniciadas» para que el arranque no las mezcle con las de hoy. Nace `L-049`: medir un control y
  descartarlo prueba que ese ambito no sirve, no que no exista uno que si.

  Los controles de fuga (Pasos 1b y 1c) y de indices (Paso 2b) de este cierre salen limpios. El
  Paso 2c muestra las mismas dos diferencias ya conocidas y documentadas en `project.md`
  (`010_prototype/` y `temporal/`).
- **Que quedo abierto:** `T-001` y `T-144` siguen `No implementada` (aplazadas). `T-003` queda
  `Suspendida`. `T-128` (la primera cosecha real) sigue `No implementada`, sin bloqueo.
  `010_prototype`, `020_baseline`, `025_wslt`, `030_growth` y `040_evol` estan declaradas pero **no
  iniciadas**. `DT-002` a `DT-006` siguen `Propuesta (pendiente del usuario)`. `A-006` a `A-009` y
  `A-011` a `A-015` quedan abiertos, `A-010` sigue `Refutado`, `A-016`/`A-017` siguen `Confirmado`.
  La autorreferencia del criterio de cierre de `D-088` sigue sin resolver. No existe todavia una
  `T-XXX` para el trabajo que `D-143` declara como prioridad inmediata —extraer un esqueleto
  reutilizable—; queda señalado en el informe de esta sesion.

---

### S-034 - Se aceptan `F-095` a `F-097` (`T-152` a `T-155`) y nace el Paso 7c-ter (`D-144`); el esqueleto de arranque pasa a ser repositorio propio (`D-145` a `D-148`, `T-156` a `T-163`)
| Campo | Valor |
|---|---|
| Fecha | 2026-09-11 |
| Etapa | `000_preproject` |
| Tareas | T-152, T-153, T-154, T-155, T-156, T-157, T-158, T-159, T-160, T-161, T-162, T-163 |

- **Que se hizo:** `manager` evaluo los tres hallazgos abiertos por `R-033` sobre `S-033` (`F-095`,
  `F-096`, `F-097`), los verifico contra `HEAD` (`ffb4130`) y los acepto los tres.

  `F-095` (`project.md` seguia diciendo que la razon del hueco en `FT-XXX`/`SC-XXX` era «la etapa no
  esta adoptada», cuando `D-142` habia declarado `020_baseline` en la tabla «Etapas» en el mismo
  commit que esa frase describia): se corrige la razon de fondo a «la etapa esta declarada, no
  iniciada», con nota fechada explicando que caduco y que el hueco de la ruta sigue en pie por otro
  motivo (`T-152`).

  `F-096` (las dos salidas crudas de la seccion 2 de `_audit/S-033.md` no reproducian: la orden
  publicada filtraba texto libre en la fila y recogia `T-039` por su titulo aunque su estado real
  era `Implementada`; la segunda publicaba `151` donde la orden devuelve `152`): nota fechada en
  `_audit/S-033.md` con las dos salidas derivadas, mas la orden correcta —filtrando por la columna de
  estado, sin podar nada a mano—, sin reescribir la prosa original (`T-153`). Nace `L-052`: un filtro
  por estado que busca texto libre recoge filas por su titulo.

  `F-097` (la NOTA DE CIERRE de `S-033` no publico la salida del CONTROL DE CIFRA ADYACENTE que el
  Paso 6b declara obligatoria): nota fechada en `_audit/S-033.md` con la salida completa —trece
  lineas, corridas sobre el informe tal como entro en su commit sustantivo— y la lectura de su
  condicion de parada linea por linea; el control pasa (`T-154`). De fondo nace un mecanismo, porque
  una regla de redaccion sola ya habia fallado tres veces: los cuatro bloques obligatorios de la NOTA
  DE CIERRE pasan a llevar un rotulo literal fijo, y nace el **Paso 7c-ter** en `protocol-close`, que
  busca los cuatro rotulos y no deja commitear el anclaje si falta alguno (`D-144`, `T-155`). El
  rotulo lleva el sufijo ` — salida:` porque la primera version, sin el, pasaba sobre el propio
  informe que motivo el hallazgo —su seccion 0 menciona el nombre del control en prosa al contar que
  nacio—; de ahi nace `L-053`: un control de presencia se prueba contra el artefacto que lo motivo, o
  no esta probado. `T-155` queda probada en sus dos casos.

  Los tres hallazgos quedan `Aceptado — pendiente` en `_audit/findings.md`, citando su `T-XXX`.
  Ninguna correccion reescribe un informe ya commiteado: las tres van por nota fechada.

  Fuera de los hallazgos, el usuario tomo cuatro decisiones sobre la prioridad que `D-143` habia
  dejado señalada sin tarea la sesion anterior: extraer del andamiaje un esqueleto reutilizable. Se
  encontro un intento ya existente en disco, con la estructura correcta pero ocho archivos por detras
  de este proyecto y sin ningun repositorio git.

  - **`D-145`** — el esqueleto pasa a ser un **repositorio propio con remoto privado**, la misma
    figura que ya tiene el repositorio de lecciones globales. Sin remoto no hay forma de clonarlo, y
    sin clonarlo cada proyecto nuevo lo copiaria a mano sin dejar constancia de la version de origen.
  - **`D-146`** — el andamiaje viaja **en un solo sentido**: el proyecto escribe y audita, el
    esqueleto recibe. Una mejora nace de una auditoria sobre un cierre real, y en el esqueleto no
    corre ningun cierre. La promocion sera una skill propia con la misma forma que la cosecha de
    lecciones —la ejecuta `manager`, nunca un agente, con puerta del usuario antes de escribir—, y
    detectar el desfase queda desacoplado de promoverlo: detectar es automatico en cada cierre,
    promover es manual y por lotes.
  - **`D-147`** — su ubicacion se registra como dos filas en `project.md`, no como restriccion, con
    una nota que deja escrito el caso invertido: este proyecto no salio del esqueleto, el esqueleto
    salio de este proyecto.
  - **`D-148`** — el cierre gana un barrido (`diff -rq --strip-trailing-cr`, probada la opcion contra
    un caso sintetico de CRLF) sobre las seis areas agnosticas contra el esqueleto, que **informa y
    no frena**: su salida normal es una lista de archivos por promover, y forzarlo a detener el
    cierre lo haria saltar casi cada sesion hasta que se ignore.

  El trabajo queda repartido en ocho tareas nuevas con orden de dependencia declarado: `T-156`
  (paraguas) y, en orden, `T-157` (crear el repositorio con el estado actual, desfasado, antes de
  sincronizar nada), `T-158` (sincronizar las seis areas), `T-159` (registrar la ubicacion en
  `project.md`), `T-160` (el barrido de `D-148` en el cierre), `T-161` (la skill de promocion),
  `T-162` (la guia de arranque) y `T-163` (dos huecos menores: `_brief/` sin plantilla y `temporal/`
  sin versionar). Ninguna se empezo esta sesion.

  Nace `A-018`: que toda diferencia que el barrido de `D-148` encuentre sea siempre una promocion
  pendiente y nunca una version legitimamente distinta que haya que conciliar —se apoya en que las
  seis areas tienen prohibido llevar datos de proyecto, pero es una deduccion sobre una regla, no una
  observacion: el caso todavia no ha ocurrido ni una vez, porque el esqueleto todavia no existe como
  repositorio. Y nace `L-054`: un original sin mecanismo de deteccion deja de ser original en
  silencio — la leccion de fondo detras de encontrar el esqueleto ocho archivos por detras sin que
  nadie lo notara.

  Los controles de fuga (Pasos 1b y 1c) y de indices (Paso 2b) de este cierre salen limpios. El Paso
  2c muestra las mismas dos diferencias ya conocidas y documentadas en `project.md` (`010_prototype/`
  y `temporal/`).
- **Que quedo abierto:** `T-156` a `T-163` siguen `No implementada` (`T-156` y `T-157` son
  `Bloqueante`; el resto, `No bloqueante`). `T-001` y `T-144` siguen `No implementada` (aplazadas).
  `T-003` sigue `Suspendida`. `T-128` (la primera cosecha real) sigue `No implementada`, sin bloqueo.
  `010_prototype`, `020_baseline`, `025_wslt`, `030_growth` y `040_evol` siguen declaradas y no
  iniciadas. `DT-002` a `DT-006` siguen `Propuesta (pendiente del usuario)`. `A-006` a `A-009`,
  `A-011` a `A-015` y ahora `A-018` quedan abiertos; `A-010` sigue `Refutado`, `A-016`/`A-017` siguen
  `Confirmado`. La autorreferencia del criterio de cierre de `D-088` sigue sin resolver.

---

### S-035 - Se aceptan `F-098` y `F-099` (`T-164` a `T-166`); nace el Paso 7c-quater (`D-149`) y `L-055`; el esqueleto se publica como repositorio (`T-157`) y nace la forma de arranque por clone (`D-150`)
| Campo | Valor |
|---|---|
| Fecha | 2026-09-11 |
| Etapa | `000_preproject` |
| Tareas | T-157, T-164, T-165, T-166, T-167, T-168 |

- **Que se hizo:** `manager` evaluo los dos hallazgos abiertos por `R-034` sobre `S-034` (`F-098`,
  `F-099`), verificados contra `HEAD` (`4f0cc42`, la auditoria `R-034`) sobre el estado que dejo el
  commit auditado (`2cef150`), y los acepto los dos.

  `F-098` (la seccion 1 de `_audit/S-034.md` abria con `git show --stat --name-only 2cef150` —sin
  `--format=`— y debajo pegaba la salida de la orden **con** `--format=`; los doce archivos listados
  eran correctos, pero el bloque no reproducia): nota fechada en `_audit/S-034.md` con la orden
  prescrita, su salida, y lo que devuelve de mas la orden publicada, sin reescribir la prosa original
  (`T-164`). De fondo nace un mecanismo: el **Paso 7c-quater** en `protocol-close`, que corre antes
  del commit de anclaje y comprueba con `grep -qF` que la seccion 1 publique la orden prescrita por
  el Paso 7c; una linea `FALTA…` detiene el cierre (`D-149`, `T-166`).

  `F-099` (esa misma seccion describia el cambio de `_audit/findings.md` con un residuo de edicion —
  «`F-095` (nace) no;»— y con la etiqueta «notas anadidas», cuando en `findings.md` no se anadio
  ninguna): nota fechada con la descripcion correcta y las cuatro ordenes que la sostienen (`T-165`).
  `D-149` decide **no** escribir mecanismo para este segundo defecto, y esa es la mitad deliberada de
  la decision: es prosa, y ningun patron la distingue de la prosa buena. De ahi nace `L-055` — mover
  un aviso a la plantilla reduce el fallo pero no lo elimina, porque el acto que falla sigue siendo
  copiar a mano; solo se vuelve comprobable cuando lo prescrito es una cadena literal.

  Los dos hallazgos quedan `Aceptado — pendiente` en `_audit/findings.md`, citando su `T-XXX`.
  Ninguna correccion reescribe un informe ya commiteado: las dos van por nota fechada.

  Fuera de los hallazgos se completa `T-157`, la primera tarea del esqueleto de arranque: deja de ser
  una carpeta suelta en disco y pasa a ser el repositorio `SDAI_TripleS` (`git init -b main`, commit
  del estado tal como estaba, `gh repo create --private --source=. --push`), publicado en
  `https://github.com/jdrodriguez1000/SDAI_TripleS`. El commit inicial recoge el desfase **sin
  sincronizar nada** —siete archivos por detras y `protocol-harvest` ausente—, que es la prueba de que
  el mecanismo hacia falta. El barrido de fuga de datos sobre el arbol entero del esqueleto salio
  limpio; el de codigos instanciados devolvio lineas que son series de ejemplo trabajado de
  `_methodology/`, permitidas por `CLAUDE.md`, comprobadas leyendo su contexto. `D-145` gana su nota
  de criterio de cierre cumplido.

  El usuario decide ademas como arrancara un proyecto nuevo desde el esqueleto (`D-150`): `git clone`,
  anotar el hash de partida, borrar `.git` y `git init` con remoto propio — nunca copiar la carpeta
  con el explorador, porque eso arrastraria el remoto del esqueleto dentro de `.git/` y el primer
  `git push` del proyecto nuevo subiria alli, rompiendo el sentido unico de `D-146` con una accion
  irreversible. `project.md` gana dos filas nuevas (esqueleto de origen y version de partida), y nace
  `T-167` para llevarlas a la plantilla. De paso se **midio**, en vez de razonarse, que un clone del
  esqueleto no trae `temporal/`.

  📌 **Nota del 2026-09-11 (`T-169`, hallazgo `F-100`).** El parrafo de arriba **no se reescribe**, y
  una de sus frases es falsa: **`project.md` no gana ninguna fila en este commit.** Lo que `D-150`
  prescribe es que el `project.md` de un **proyecto nuevo** lleve esas dos filas —esqueleto de origen
  y version de partida—, y llevarlas a la plantilla es justo lo que quedo pendiente en `T-167`
  (`No implementada`). El commit no toca el archivo, y el archivo tampoco las tiene en `HEAD`:

```
$ git show --name-only --format= cce48e0 | grep -xc "project.md"
0

$ git show ce0ac4e:project.md | grep -ciE "esqueleto|version de partida"
0
```

  Se corrigen tambien, por nota fechada, **tres citas cruzadas** encontradas al leer de corrido los
  criterios de cierre de `D-146`, `D-147` y `D-148`: cada una citaba la tarea de otra, por un
  desplazamiento que sobrevivio a una renumeracion (`T-168`). No lo encontro ningun control: las dos
  mitades de cada cita son codigos validos y existentes.

  Los controles de fuga (Pasos 1b y 1c) y de indices (Paso 2b) de este cierre salen limpios —el 2b
  tras escribir esta entrada, que era lo unico que faltaba—. El Paso 2c muestra las mismas dos
  diferencias ya conocidas y documentadas en `project.md` (`010_prototype/` y `temporal/`). El Paso 2d
  encontro **una** orden que no reproducia: la de «despues» del bloque de verificacion de `T-168`, que
  se corrio sobre el arbol mientras `decisions.md` seguia creciendo; se corrigio antes del `git add`,
  anclandola y actualizando sus numeros de linea, con su nota. El Paso 2e no anade ninguna linea nueva
  de caracter de control.
- **Que quedo abierto:** `T-156`, `T-158` a `T-163` y `T-167` siguen `No implementada` (`T-156` es
  `Bloqueante`; el resto, `No bloqueante`). `T-001` y `T-144` siguen `No implementada` (aplazadas).
  `T-003` sigue `Suspendida`. `T-128` (la primera cosecha real) sigue `No implementada`, sin bloqueo.
  `010_prototype`, `020_baseline`, `025_wslt`, `030_growth` y `040_evol` siguen declaradas y no
  iniciadas. `DT-002` a `DT-006` siguen `Propuesta (pendiente del usuario)`. `A-006` a `A-009`,
  `A-011` a `A-015` y `A-018` siguen abiertos; `A-010` sigue `Refutado`, `A-016`/`A-017` siguen
  `Confirmado`. La autorreferencia del criterio de cierre de `D-088` sigue sin resolver.

---

### S-036 - Se aceptan `F-100` y `F-101` (`T-169`, `T-170`); se corrige la cuarta cita cruzada (`T-171`); el esqueleto queda sincronizado y con su barrido de cierre (`T-158` a `T-161`); nace `DT-007` (`D-151`, `C-010`, `L-057`)
| Campo | Valor |
|---|---|
| Fecha | 2026-09-11 |
| Etapa | `000_preproject` |
| Tareas | T-158, T-159, T-160, T-161, T-169, T-170, T-171 |

- **Que se hizo:** `manager` evaluo los dos hallazgos abiertos por `R-035` sobre `S-035` (`F-100`,
  `F-101`), verificados contra `HEAD` (`ce0ac4e`, la auditoria `R-035`) sobre el estado que dejo el
  commit auditado (`cce48e0`), y los acepto los dos.

  `F-100` (la entrada `S-035` afirmaba que `project.md` ganaba dos filas nuevas, y el commit
  `cce48e0` no toca ese archivo): nota fechada en la propia entrada de arriba, con las dos ordenes
  que muestran que ni el commit ni `project.md` en `HEAD` tienen esas filas, sin reescribir la prosa
  original (`T-169`).

  `F-101` (el bloque de verificacion de `T-157` describia un «segundo barrido, por codigos
  instanciados», pero solo quedaban publicados el barrido de fuga y un `sed` de contexto — la orden
  del segundo nunca se escribio): como no se podia reconstruir la orden de entonces, se rehizo hoy
  sobre el mismo arbol del esqueleto (sigue en `fa7da56`, sin sincronizar todavia en ese momento) y
  se publico entera, con su patron, su ambito y su salida cruda, por nota fechada sin tocar el bullet
  original (`T-170`).

  Los dos hallazgos quedan `Aceptado — pendiente` en `_audit/findings.md`, citando su `T-XXX`.

  Al leer de corrido los criterios de cierre de `D-145` a `D-151` aparecio una **cuarta** cita
  cruzada que la pasada de `T-168` no vio: buscaba solo la forma «Lo implementa `T-XXX`», y el cuerpo
  de `D-147` remite a `T-162` (la guia de arranque) donde debia decir `T-159` (la escritura de las
  dos filas). Se corrigio por nota fechada, con la orden anclada al commit `ce0ac4e` para que la
  propia nota —que tambien cita tareas— no se incluyera en su barrido (`T-171`).

  Fuera de los hallazgos se completan las cuatro tareas que `T-157` desbloqueaba:

  - `T-158` — las seis areas agnosticas del esqueleto quedan sincronizadas (commit `1748f0a` en
    `SDAI_TripleS`): los ocho archivos por detras de `T-157`, mas la correccion de un final de linea
    (un archivo en CRLF aqui se copio convertido a LF, el que el destino ya tenia — medido con
    `tr -dc | wc -c`, no con `grep -c $'\r'`, que en este entorno da un falso positivo). Los cuatro
    barridos de agnosticismo sobre el esqueleto ya sincronizado salen limpios.
  - `T-159` — `project.md` registra la ubicacion del esqueleto (repositorio y remoto), con la nota
    del caso invertido.
  - `T-160` — nace el **Paso 2f** en `protocol-close`: el barrido de desfase con el esqueleto,
    probado en sus tres resultados (al dia, desfasado, ruta ausente). La primera version sin guarda
    no producia `SIN COMPROBAR` ante una ruta ausente, sino seis lineas de `No such file or
    directory` indistinguibles de un desfase — lo encontro la prueba del tercer caso, no la
    relectura.
  - `T-161` — nace la skill `protocol-promote`: lleva al esqueleto lo que este proyecto escriba en
    las seis areas, con la misma puerta y el mismo orden que `protocol-harvest` (los barridos y la
    medicion de final de linea van antes de la puerta). No se ha ejecutado todavia.

  Al escribir estos bloques con patrones `\b` se descubrio que las barras invertidas se pierden al
  escribir por shell y quedan como caracter de retroceso real (`0x08`), invisible en pantalla —
  incluso dentro de un heredoc citado (`C-010`, `L-057`). El barrido de alcance encuentra **26
  ocurrencias heredadas** del mismo defecto que ya documentan `DT-003` a `DT-006`, en `tasks.md`,
  `assumptions.md` y `findings.md`. `D-151` decide no corregirlas en masa —convertiria «evidencia que
  no reproduce» en «evidencia falsa»—, y la deuda se propone como `DT-007`. Nace tambien `L-056`
  (una orden que busca su propio rotulo en el archivo donde queda escrita se cuenta a si misma, visto
  al comprobar la nota de `T-170`) y `A-019` (la skill `protocol-promote` esta bien escrita y bien
  ordenada, pero no se ha ejecutado ni una vez). `CLAUDE.md` se corrige en dos sitios —el suyo propio
  y el de `protocol-harvest`— para decir que la cosecha es «uno de los dos» protocolos que escriben
  fuera del repositorio, nombrando al otro.

  Los controles de fuga (Pasos 1b y 1c) y de indices (Paso 2b) de este cierre salen limpios. El Paso
  2c muestra las mismas dos diferencias ya conocidas y documentadas en `project.md` (`010_prototype/`
  y `temporal/`).
- **Que quedo abierto:** de la familia del esqueleto quedan `T-156` (tarea paraguas, `Bloqueante`),
  `T-162` (guia de arranque), `T-163` (dos huecos menores) y `T-167` (llevar a la plantilla de
  `project.md` las dos filas de `D-150`), todas `No implementada`. `T-001` y `T-144` siguen `No
  implementada` (aplazadas). `T-003` sigue `Suspendida`. `T-128` (la primera cosecha real) sigue `No
  implementada`, sin bloqueo. `DT-002` a `DT-007` siguen `Propuesta (pendiente del usuario)`. `A-006`
  a `A-009`, `A-011` a `A-015`, `A-018` y `A-019` siguen abiertos; `A-010` sigue `Refutado`,
  `A-016`/`A-017` siguen `Confirmado`. La autorreferencia del criterio de cierre de `D-088` sigue sin
  resolver. La primera ejecucion real de `protocol-promote` sigue pendiente de que el usuario la
  pida.

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
