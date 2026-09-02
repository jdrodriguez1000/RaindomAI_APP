# findings.md

> Registro de los **hallazgos de auditoria**: lo que el agente `report_auditor` encontro, y en que acabo
> cada cosa. Cada hallazgo tiene codigo `F-NNN`.
>
> 🔑 **Este archivo existe por una sola razon: que un hallazgo no desaparezca porque no nos gusto.**
> Aceptado, rechazado o aplazado, todos siguen aqui con su estado.

---

## Indice

| Codigo | Hallazgo | Auditoria | Gravedad | Estado |
|---|---|---|---|---|
| [F-001](#f-001---el-bloque-de-verificacion-de-d-016-afirma-mas-de-lo-que-su-comando-comprueba) | El bloque de verificacion de `D-016` afirma mas de lo que su comando comprueba | R-002 | Media | Implementado |
| [F-002](#f-002---quedan-identificadores-auditor-vivos-fuera-del-ambito-del-barrido) | Quedan identificadores `auditor` vivos fuera del ambito del barrido | R-002 | Baja | Implementado |
| [F-003](#f-003---dt-001-se-registro-como-confirmada-contra-el-paso-5-de-protocol-close) | `DT-001` se registro como `Confirmada` contra el Paso 5 de `protocol-close` | R-002 | Media | Implementado |
| [F-004](#f-004---session-closermd-describe-a-report_auditor-en-su-propio-repositorio) | `session-closer.md` describe a `report_auditor` en «su propio repositorio» | R-002 | Media | Implementado |
| [F-005](#f-005---el-bloque-de-verificacion-de-la-observacion-nueva-de-a-001-no-se-reproduce-sobre-su-propio-commit) | El bloque de verificacion de la observacion nueva de `A-001` no se reproduce sobre su propio commit | R-003 | Media | Implementado |
| [F-006](#f-006---la-nota-de-ambito-de-d-016-registra-recuentos-que-no-cuadran-con-el-commit-que-la-contiene) | La nota de ambito de `D-016` registra recuentos que no cuadran con el commit que la contiene | R-003 | Baja | Implementado |
| [F-007](#f-007---d-020-declara-una-excepcion-que-la-convencion-de-tasksmd-no-recoge-y-la-tension-queda-sin-registrar) | `D-020` declara una excepcion que la convencion de `tasks.md` no recoge, y la tension queda sin registrar | R-003 | Media | Implementado |
| [F-008](#f-008---el-bloque-de-verificacion-de-d-021-afirma-reproducirse-sobre-su-commit-y-no-se-reproduce) | El bloque de verificacion de `D-021` afirma reproducirse sobre su commit y no se reproduce | R-004 | Media | Implementado |
| [F-009](#f-009---dt-001-queda-implementada-con-un-criterio-de-cierre-que-no-se-cumple) | `DT-001` queda `Implementada` con un criterio de cierre que no se cumple | R-004 | Baja | Implementado |
| [F-010](#f-010---una-convencion-vigente-de-_auditfindingsmd-cita-un-archivo-que-ya-no-existe) | Una convencion vigente de `_audit/findings.md` cita un archivo que ya no existe | R-004 | Baja | Implementado |
| [F-011](#f-011---la-nota-nueva-de-a-001-vuelve-a-registrar-un-recuento-sobre-head-que-no-se-reproduce-sobre-su-commit) | La nota nueva de `A-001` vuelve a registrar un recuento sobre `HEAD` que no se reproduce sobre su commit | R-005 | Media | Implementado |
| [F-012](#f-012---la-segunda-excepcion-de-d-025-no-llego-a-los-tres-sitios-que-siguen-diciendo-es-la-unica-excepcion) | La segunda excepcion de `D-025` no llego a los tres sitios que siguen diciendo «es la unica excepcion» | R-005 | Media | Implementado |
| [F-013](#f-013---d-023-conserva-vigente-una-advertencia-que-d-026-desmiente-en-el-mismo-commit) | `D-023` conserva vigente una advertencia que `D-026` desmiente en el mismo commit | R-005 | Baja | Implementado |
| [F-014](#f-014---el-avance-de-la-etapa-de-progressmd-atribuye-mal-la-procedencia-de-los-hallazgos-y-cuenta-f-006-dos-veces) | El «Avance de la etapa» de `progress.md` atribuye mal la procedencia de los hallazgos y cuenta `F-006` dos veces | R-005 | Baja | Implementado |
| [F-015](#f-015---005_discovery-sigue-declarada-sin-su-archivo-en-_phases-y-ya-nadie-lo-agenda) | `005_discovery` sigue declarada sin su archivo en `_phases/`, y ya nadie lo agenda | R-006 | Media | Implementado |
| [F-016](#f-016---el-criterio-de-cierre-de-t-015-no-se-cumple-al-ejecutarlo-y-la-tarea-queda-implementada) | El criterio de cierre de `T-015` no se cumple al ejecutarlo, y la tarea queda `Implementada` | R-006 | Baja | Implementado |
| [F-017](#f-017---t-020-queda-implementada-sin-ningun-bloque-de-verificacion-y-el-informe-remite-a-una-seccion-que-tampoco-lo-tiene) | `T-020` queda `Implementada` sin ningun bloque de verificacion, y el informe remite a una seccion que tampoco lo tiene | R-007 | Media | Implementado |
| [F-018](#f-018---t-021-afirma-un-barrido-sobre-todo-el-repositorio-del-que-no-registra-ni-el-patron-ni-el-ambito-ni-la-salida) | `T-021` afirma un barrido «sobre todo el repositorio» del que no registra ni el patron ni el ambito ni la salida | R-007 | Baja | Implementado |
| [F-019](#f-019---la-lista-de-archivos-de-la-seccion-1-del-informe-no-cuadra-con-el-comando-que-dice-haberla-producido) | La lista de archivos de la seccion 1 del informe no cuadra con el comando que dice haberla producido | R-007 | Baja | Implementado |
| [F-020](#f-020---la-entrada-de-f-017-en-findingsmd-conserva-la-linea-que-dice-que-sigue-pendiente-de-evaluar) | La entrada de `F-017` en `findings.md` conserva la linea que dice que sigue pendiente de evaluar | R-008 | Baja | Implementado |
| [F-021](#f-021---progressmd-atribuye-a-r-007-un-commit-auditado-que-no-es-el-suyo) | `progress.md` atribuye a `R-007` un commit auditado que no es el suyo | R-008 | Baja | Implementado |
| [F-022](#f-022---tres-bloques-de-verificacion-de-decisionsmd-registran-una-salida-que-no-se-reproduce) | Tres bloques de verificacion de `decisions.md` registran una salida que no se reproduce | R-008 | Media | Implementado |
| [F-023](#f-023---t-026-se-escribio-a-mano-sin-el-d-xxx-ni-el-f-nnn-que-la-convencion-exige-y-la-desviacion-no-llego-a-decisionsmd) | `T-026` se escribio a mano sin el `D-XXX` ni el `F-NNN` que la convencion exige, y la desviacion no llego a `decisions.md` | R-008 | Baja | Implementado |
| [F-024](#f-024---f-021-se-declara-implementado-y-la-correccion-no-esta-en-el-diff) | `F-021` se declara `Implementado` y la correccion no esta en el diff | R-009 | Alta | Implementado |
| [F-025](#f-025---los-bloques-de-verificacion-de-d-043-y-d-044-usan-head-sin-anclar-y-no-se-reproducen) | Los bloques de verificacion de `D-043` y `D-044` usan `HEAD` sin anclar y no se reproducen | R-009 | Media | Implementado |
| [F-026](#f-026---dt-002-cita-l-013-donde-corresponde-l-014) | `DT-002` cita `L-013` donde corresponde `L-014` | R-009 | Baja | Implementado |
| [F-027](#f-027---el-bloque-de-verificacion-de-t-032-no-se-reproduce-sobre-su-propio-commit-y-su-lectura-en-prosa-queda-desmentida) | El bloque de verificacion de `T-032` no se reproduce sobre su propio commit, y su lectura en prosa queda desmentida | R-010 | Media | Implementado |
| [F-028](#f-028---la-lista-de-la-seccion-1-del-informe-omite-dos-ediciones-de-decisionsmd) | La lista de la seccion 1 del informe omite dos ediciones de `decisions.md` | R-010 | Baja | Implementado |
| [F-029](#f-029---t-037-y-t-038-llevan-el-estado-pendiente-que-la-convencion-de-tasksmd-no-declara) | `T-037` y `T-038` llevan el estado `Pendiente`, que la convencion de `tasks.md` no declara | R-011 | Media | Implementado |
| [F-030](#f-030---t-038-se-escribio-a-mano-sin-citar-el-d-xxx-o-f-nnn-que-la-habilita) | `T-038` se escribio a mano sin citar el `D-XXX` o `F-NNN` que la habilita | R-011 | Baja | Implementado |
| [F-031](#f-031---el-recuento-quince-lecciones-sin-evaluar-no-se-reproduce-sobre-su-propio-commit-y-esta-en-cuatro-sitios) | El recuento «quince lecciones `Sin evaluar`» no se reproduce sobre su propio commit, y esta en cuatro sitios | R-011 | Media | Implementado |
| [F-032](#f-032---el-bloque-de-t-041-publica-un-recuento-que-su-commit-no-sostiene-y-su-prosa-afirma-cuatro-notas-donde-hay-tres) | El bloque de `T-041` publica un recuento que su commit no sostiene, y su prosa afirma cuatro notas donde hay tres | R-012 | Media | Implementado |
| [F-033](#f-033---la-nota-de-cierre-de-d-060-afirma-que-projectmd-no-nombra-la-etapa-nueva-y-el-mismo-commit-lo-desmiente) | La nota de cierre de `D-060` afirma que `project.md` no nombra la etapa nueva, y el mismo commit lo desmiente | R-012 | Baja | Implementado |
| [F-034](#f-034---el-informe-remite-a-una-lista-completa-del-paso-2d-que-no-existe-en-el-commit) | El informe remite a una lista completa del Paso 2d que no existe en el commit | R-013 | Media | Abierto |

---

## Convenciones

| Campo | Valores posibles |
|---|---|
| Codigo | `F-NNN`, correlativo, no se reutiliza |
| Auditoria | el `R-XXX` que lo abrio |
| Gravedad | `Alta` / `Media` / `Baja` |
| Estado | `Abierto` / `Aceptado — pendiente` / `Implementado` / `No se implementa` |
| Cerrado en | el commit sobre el que la auditoria verifico la correccion |

### Que significa cada estado

| Estado | Cuando | Que exige |
|---|---|---|
| `Abierto` | la auditoria lo abrio y `manager` aun no lo ha evaluado | — |
| `Aceptado — pendiente` | de acuerdo, pero todavia no hecho | **su `T-XXX`**, abierta |
| `Implementado` | corregido, y **una auditoria posterior lo verifico** | el commit donde se verifico |
| `No se implementa` | rechazado | **su `D-XXX`**. Si el rechazo es por coste o prioridad y no por ser incorrecto, ademas **su `DT-XXX`** |

🚨 **`Implementado` no lo escribe `manager`, lo escribe la auditoria siguiente.** Un hallazgo se
cierra **verificando la correccion sobre un commit posterior**, no declarandola. Si el auditado
pudiera cerrar sus propios hallazgos, este archivo diria lo que quisieramos que dijera.

🚨 **`Aceptado — pendiente` no es un adorno.** Sin ese estado, un hallazgo con el que estamos de
acuerdo pero que aun no hicimos no esta implementado ni rechazado: no aparece en ningun sitio y
desaparece del radar. Asi es como se pierden los hallazgos buenos.

⚠️ **Un rechazo por coste o prioridad es deuda tecnica por definicion**, y exige su `DT-XXX`. Un
rechazo por coste sin entrada en `techdebt.md` es, por si solo, un hallazgo nuevo — y no requiere
criterio: se comprueba mirando si la entrada existe.

🚨 **El indice se escribe a mano, sin generador.** Cada fila enlaza por ancla a su hallazgo.

---

## Hallazgos

<!--
Plantilla:

### F-NNN - Titulo
| Campo | Valor |
|---|---|
| Auditoria | R-XXX |
| Fecha | AAAA-MM-DD |
| Gravedad | |
| Estado | Abierto |
| Registrado en | T-XXX / D-XXX / DT-XXX |
| Cerrado en | |

- **Que se observo:** el hecho, con su comando y salida cruda.
- **Por que importa:** que se rompe si se queda asi.
- **Que se hizo:** la evaluacion de `manager` y donde quedo registrada.
-->

### F-001 - El bloque de verificacion de `D-016` afirma mas de lo que su comando comprueba
| Campo | Valor |
|---|---|
| Auditoria | R-002 |
| Fecha | 2026-08-31 |
| Gravedad | Media |
| Estado | Implementado |
| Registrado en | T-004 |
| Cerrado en | `ea0b850` (R-003) |

- **Que se observo:** el bloque de `D-016` se titula «Verificacion — cero identificadores
  `auditor` vivos», sin acotar ambito, y su comando cubre solo tres rutas:

```
$ git grep -nE '`auditor`|\*\*auditor\*\*|Origen: auditor|agente auditor' badc878 -- .claude CLAUDE.md project.md
exit=1
```

  La misma decision declara que el rename alcanza tambien el valor `Origen: auditor` en los seis
  archivos de `_persistence/` (`decisions.md:387`), y `progress.md:144-147` cita ese exit code como
  respaldo del rename entero. Aplicado a `_persistence/`, el mismo patron devuelve 18 lineas.
- **Por que importa:** el ambito reducido tapo una fuga real (`F-002`). Un bloque de verificacion
  mas ancho en su enunciado que en su comando da por cerrado lo que nadie miro.
- **Que se hizo:** `manager` lo acepta (2026-09-01, sesion `S-003`). Se verifico contra `HEAD`
  (`c575bc0`) que el defecto seguia vivo. El bloque original **no se toca** —no se reescribe un
  comando ya ejecutado—: se le anade debajo una nota fechada que declara su ambito real y registra
  el barrido con ambito completo, con patron y salida cruda. Registrado en `T-004`.

---

### F-002 - Quedan identificadores `auditor` vivos fuera del ambito del barrido
| Campo | Valor |
|---|---|
| Auditoria | R-002 |
| Fecha | 2026-08-31 |
| Gravedad | Baja |
| Estado | Implementado |
| Registrado en | T-005 |
| Cerrado en | `ea0b850` (R-003) |

- **Que se observo:** dos lineas vivas siguen citando el handle viejo.

```
$ git show badc878:_persistence/tasks.md | sed -n '39p'
existente —«usuario, pero por escrito», «auditor, pero de otra pasada»— no es un valor nuevo: va

$ git show badc878:_audit/findings.md | sed -n '3p'
> Registro de los **hallazgos de auditoria**: lo que el agente `auditor` encontro, y en que acabo
```

  En `tasks.md:39` la palabra nombra el valor del campo `Origen`, cuya fila ya dice
  `report_auditor`: no es el sustantivo comun que `D-016` excluye. En `findings.md:3` es la cabecera
  viva de un registro activo; el motivo con que `D-016` excluye `_audit/` («describen lo que se
  decidio en su momento») no le aplica.
- **Por que importa:** poco por si solo; importa como prueba de que el ambito de `F-001` importaba.
- **Que se hizo:** `manager` lo acepta (2026-09-01, sesion `S-003`). Las dos lineas seguian vivas en
  `HEAD` (`c575bc0`) y ambas nombran el identificador del agente, no el sustantivo comun: se
  corrigen. Registrado en `T-005`. La auditoria **no** corrigio la cabecera de `findings.md`:
  corregir sobre el commit auditado invalidaria el propio informe.

---

### F-003 - `DT-001` se registro como `Confirmada` contra el Paso 5 de `protocol-close`
| Campo | Valor |
|---|---|
| Auditoria | R-002 |
| Fecha | 2026-08-31 |
| Gravedad | Media |
| Estado | Implementado |
| Registrado en | T-006 |
| Cerrado en | `ea0b850` (R-003) |

- **Que se observo:**

```
$ git show badc878:_persistence/debtec.md | sed -n '13p'
| [DT-001](#dt-001---debtecmd-incumple-la-regla-de-nombres-en-ingles) | `debtec.md` incumple la regla de nombres en ingles | No implementada | Confirmada | Baja | No bloqueante |

$ git show badc878:.claude/skills/protocol-close/SKILL.md | sed -n '365,366p'
2. **Marcada como propuesta**, tanto en el campo `Confirmacion` de la entrada como en el reporte,
   para que el usuario la confirme o la tumbe.
```

  El propio `S-002` §6 declara que el valor descansa en el traspaso, no en el diff. No hay `D-XXX`
  que ampare la excepcion.
- **Por que importa:** `Confirmacion` existe para distinguir lo confirmado de lo supuesto. Un
  `Confirmada` escrito por el actor a quien el protocolo se lo prohibe vacia el campo de funcion.
- **Que se hizo:** `manager` lo acepta (2026-09-01, sesion `S-003`). El valor seguia siendo
  `Confirmada` en `HEAD` (`c575bc0`). Vuelve a `Propuesta (pendiente del usuario)` en el indice y en
  el detalle, con nota fechada. `manager` **no la confirma**: el dueno de la confirmacion va dentro
  del valor y es el usuario, a quien se le pide en el reporte de esta sesion. Registrado en `T-006`.

---

### F-004 - `session-closer.md` describe a `report_auditor` en «su propio repositorio»
| Campo | Valor |
|---|---|
| Auditoria | R-002 |
| Fecha | 2026-08-31 |
| Gravedad | Media |
| Estado | Implementado |
| Registrado en | T-007 |
| Cerrado en | `ea0b850` (R-003) |

- **Que se observo:**

```
$ git grep -n "su propio repositorio" badc878 -- .claude
badc878:.claude/agents/session-closer.md:56:| **report_auditor** | su propio repositorio; audita, verifica y recomienda |

$ git show badc878:project.md | grep -n "dentro de este mismo repositorio"
19:| Auditoria | agente `report_auditor`, dentro de este mismo repositorio |
```

- **Por que importa:** resto del esquema de dos terminales que `D-012` revoco, vivo en la tabla de
  actores que `session-closer` lee en cada cierre. Contradice a `project.md`, a `CLAUDE.md` y a las
  dos lineas siguientes de su propio archivo.
- **Que se hizo:** `manager` lo acepta (2026-09-01, sesion `S-003`). La linea seguia viva en `HEAD`
  (`c575bc0`). La fila pasa a nombrar lo que el auditor escribe de verdad —`_audit/R-XXX.md`,
  `_audit/findings.md` y `_audit/index.md`, en este mismo repositorio—. Registrado en `T-007`.

---

### F-005 - El bloque de verificacion de la observacion nueva de `A-001` no se reproduce sobre su propio commit
| Campo | Valor |
|---|---|
| Auditoria | R-003 |
| Fecha | 2026-09-01 |
| Gravedad | Media |
| Estado | Implementado |
| Registrado en | T-009 |
| Cerrado en | `510d580` (R-005) |

- **Que se observo:** la observacion del 2026-09-01 bajo `A-001` registra este bloque y concluye
  «Cero sesiones cerradas sin auditar (señal 2)»:

```
$ git grep -n "| Pendiente |" -- _audit/index.md ; echo "exit=$?"
exit=1
```

  Sobre el commit que contiene esa afirmacion, el mismo comando devuelve una linea:

```
$ git grep -n "| Pendiente |" ea0b850 -- _audit/index.md ; echo "exit=$?"
ea0b850:_audit/index.md:14:| `S-003.md` | S-003 | 2026-09-01 | Pendiente | Pendiente | Pendiente | - |
exit=0
```

- **Por que importa:** la salida cruda registrada no es reproducible sobre el commit que la contiene,
  y ademas ese comando **no puede devolver `exit=1` en ningun cierre**: el propio cierre añade la
  fila de su sesion con `Pendiente` antes de commitear. Como señal de refutacion de `A-001` esta mal
  construida — mismo patron que `F-001` y `L-006`.
- **Que se hizo:** `manager` lo acepta (2026-09-01, sesion `S-005`). Verificado contra `HEAD`
  (`e61454b`) que el defecto sigue vivo: el bloque de `A-001` no se reproduce sobre `ea0b850`, y el
  comando **no puede devolver `exit=1` en ningun commit de cierre**, porque el `session-closer`
  escribe la fila de su propia sesion con `Pendiente` antes de commitear.

```
$ git grep -n "| Pendiente |" ea0b850 -- _audit/index.md ; echo "exit=$?"
ea0b850:_audit/index.md:14:| `S-003.md` | S-003 | 2026-09-01 | Pendiente | Pendiente | Pendiente | - |
exit=0

$ git grep -n "| Pendiente |" HEAD -- _audit/index.md ; echo "exit=$?"
exit=1
```

  El bloque original **no se toca** (`D-019`): se le anade debajo una nota fechada que declara su
  ambito real y **rehace la señal 2** para que pueda dispararse — una sesion cuenta como sin auditar
  cuando su fila sigue en `Pendiente` **al abrirse la sesion siguiente**, no en el instante del
  cierre. Registrado en `T-009`.

- **Cerrado por `R-005`** sobre `510d580`: la nota fechada esta bajo `A-001`, el bloque original
  quedo intacto (`D-019`), declara su ambito real y rehace la señal 2 con su momento de comprobacion
  —«al abrirse la sesion siguiente»—, que son los dos puntos del criterio de cierre de `T-009`.
  ⚠️ **La nota introduce un defecto nuevo, que va como `F-011` y no reabre este.**

---

### F-006 - La nota de ambito de `D-016` registra recuentos que no cuadran con el commit que la contiene
| Campo | Valor |
|---|---|
| Auditoria | R-003 |
| Fecha | 2026-09-01 |
| Gravedad | Baja |
| Estado | Implementado |
| Registrado en | T-010 |
| Cerrado en | `510d580` (R-005) |

- **Que se observo:** la nota del 2026-09-01 bajo el bloque de verificacion de `D-016` afirma que el
  barrido se hizo «ya escrito el registro de esta sesion», y registra `_persistence/progress.md:7`
  sin `_audit/S-003.md`. El mismo comando sobre el commit auditado devuelve:

```
$ git grep -cE '`auditor`|\*\*auditor\*\*|Origen: auditor|agente auditor' ea0b850 -- .
ea0b850:_audit/R-002.md:28
ea0b850:_audit/S-001.md:1
ea0b850:_audit/S-002.md:10
ea0b850:_audit/S-003.md:3
ea0b850:_audit/findings.md:6
ea0b850:_persistence/assumptions.md:1
ea0b850:_persistence/decisions.md:14
ea0b850:_persistence/lessons.md:3
ea0b850:_persistence/progress.md:8
ea0b850:_persistence/tasks.md:4
```

- **Por que importa:** las diferencias son lineas escritas despues del barrido y ninguna es una
  referencia viva, pero la nota declara mas ambito temporal del que tuvo. Repetir dentro de la
  correccion de `F-001` el defecto que `F-001` describe le resta valor a `L-006`.
- **Que se hizo:** `manager` lo acepta (2026-09-01, sesion `S-005`). Verificado contra `HEAD`
  (`e61454b`) que el defecto sigue vivo: la nota de `D-016` registra `progress.md:7` y ningun
  `_audit/S-003.md`, y sobre `ea0b850` son `progress.md:8` y `_audit/S-003.md:3`.

```
$ git grep -cE '`auditor`|\*\*auditor\*\*|Origen: auditor|agente auditor' ea0b850 -- . ; echo "exit=$?"
ea0b850:_audit/R-002.md:28
ea0b850:_audit/S-001.md:1
ea0b850:_audit/S-002.md:10
ea0b850:_audit/S-003.md:3
ea0b850:_audit/findings.md:6
ea0b850:_persistence/assumptions.md:1
ea0b850:_persistence/decisions.md:14
ea0b850:_persistence/lessons.md:3
ea0b850:_persistence/progress.md:8
ea0b850:_persistence/tasks.md:4
exit=0
```

  Las dos diferencias son lineas escritas despues del barrido y ninguna es una referencia viva: el
  fondo se sostiene, la declaracion de alcance temporal no. Se anade una segunda nota fechada bajo
  `D-016` con este recuento; los dos bloques anteriores quedan intactos. Registrado en `T-010`.

- **Cerrado por `R-005`** sobre `510d580`: existe la segunda nota fechada bajo `D-016` con su
  recuento sobre `ea0b850`, reproducido aqui y coincidente linea por linea. Los dos bloques
  anteriores quedan intactos.

```
$ git grep -cE '`auditor`|\*\*auditor\*\*|Origen: auditor|agente auditor' ea0b850 -- . | tail -3
ea0b850:_persistence/lessons.md:3
ea0b850:_persistence/progress.md:8
ea0b850:_persistence/tasks.md:4
```

---

### F-007 - `D-020` declara una excepcion que la convencion de `tasks.md` no recoge, y la tension queda sin registrar
| Campo | Valor |
|---|---|
| Auditoria | R-003 |
| Fecha | 2026-09-01 |
| Gravedad | Media |
| Estado | Implementado |
| Registrado en | T-008 |
| Cerrado en | R-004 (`c70b757`) |

- **Que se observo:** `D-020` esta `Vigente` y permite a `manager` escribir en `tasks.md`. La
  convencion del archivo sigue en absoluto, y la tension no esta en ningun tablero:

```
$ git show ea0b850:_persistence/tasks.md | sed -n '48,49p'
🚨 **Este archivo no se escribe a mano durante la jornada.** Lo produce el cierre de sesion, junto
con `progress.md`.

$ git grep -n "D-020" ea0b850 -- _persistence/debtec.md _persistence/tasks.md ; echo "exit=$?"
exit=1
```

- **Por que importa:** quien abra `tasks.md` sin conocer `D-020` lee una prohibicion absoluta que ya
  no rige, y `T-004`..`T-007` la incumplen a la vista. Una tension declarada solo en el cuerpo de la
  decision que la crea no vuelve a mirarla nadie.
- **Que se hizo:** `manager` lo acepta (2026-09-01, sesion `S-004`). Se verifico contra `HEAD`
  (`ea0b850`) que el defecto seguia vivo. El usuario, preguntado, confirmo que `manager` **si** debe
  escribir la `T-XXX` al registrar un hallazgo: la lectura de `D-020` era correcta y lo que faltaba
  era el registro. La excepcion se escribe dentro de la convencion de `tasks.md`, acotada a ese caso,
  y se refleja en `protocol-close` y en `session-closer.md`. La confirmacion queda anotada en
  `D-020`. Registrado en `T-008`.

- **Que cerro el hallazgo (`R-004`, commit `c70b757`):** la excepcion esta enunciada dentro de la
  convencion de `_persistence/tasks.md`, acotada al caso y citando `D-020`; se repite en
  `.claude/skills/protocol-close/SKILL.md` y en `.claude/agents/session-closer.md`; `D-020` lleva su
  nota fechada de cierre de tension; y no queda ningun tercer sitio con el enunciado absoluto:

```
$ git grep -n "a mano" c70b757 -- .claude _persistence CLAUDE.md project.md
c70b757:_persistence/tasks.md:50:🚨 **Este archivo no se escribe a mano durante la jornada.** Lo produce el cierre de sesion, junto
c70b757:_persistence/progress.md:43:🚨 **Este archivo no se escribe a mano durante la jornada.** Lo produce el cierre de sesion, junto
(el resto son «El indice se escribe a mano, sin generador», sin relacion)

$ git show c70b757:_persistence/tasks.md | sed -n '50,62p'
🚨 **Este archivo no se escribe a mano durante la jornada.** Lo produce el cierre de sesion, junto
con `progress.md`. **Tiene una unica excepcion, y esta escrita:** cuando `manager` evalua un hallazgo
`F-NNN` de una auditoria y lo acepta, escribe **en ese momento** la `T-XXX` con
`Origen: report_auditor`, sin esperar al cierre. Lo fija `D-020`, confirmada por el usuario el
2026-09-01.
```

---

### F-008 - El bloque de verificacion de `D-021` afirma reproducirse sobre su commit y no se reproduce
| Campo | Valor |
|---|---|
| Auditoria | R-004 |
| Fecha | 2026-09-01 |
| Gravedad | Media |
| Estado | Implementado |
| Registrado en | T-011 |
| Cerrado en | `510d580` (R-005) |

- **Que se observo:** `D-021` cierra su bloque de verificacion afirmando literalmente que «el
  recuento se tomo con el registro de esta sesion ya escrito, que es lo que hace que se reproduzca
  sobre el commit que lo contiene», y registra `_persistence/progress.md:2`. Sobre el commit que la
  contiene el recuento es otro:

```
$ git grep -nc "debtec" c70b757 -- . ; echo "exit=$?"
c70b757:_audit/R-001.md:2
c70b757:_audit/R-002.md:9
c70b757:_audit/R-003.md:5
c70b757:_audit/S-001.md:2
c70b757:_audit/S-002.md:4
c70b757:_audit/S-003.md:2
c70b757:_audit/S-004.md:17
c70b757:_audit/findings.md:4
c70b757:_persistence/decisions.md:13
c70b757:_persistence/progress.md:6
c70b757:_persistence/techdebt.md:4
exit=0
```

  `progress.md` da 6 y no 2; falta la linea `_audit/S-004.md:17`; y las 13 de `decisions.md` no son
  «las 13 de esta misma entrada» — solo 9 caen dentro de `D-021`, que empieza en la linea 573:

```
$ git grep -n "debtec" c70b757 -- _persistence/decisions.md | head -4
c70b757:_persistence/decisions.md:32:| [D-021](#d-021---debtecmd-pasa-a-llamarse-techdebtmd) | `debtec.md` pasa a llamarse `techdebt.md` | 2026-09-01 | Vigente |
c70b757:_persistence/decisions.md:130:  **`manager`, en el momento en que las cosas pasan**. `debtec.md` admite propuestas del cierre,
c70b757:_persistence/decisions.md:470:  historia ya auditada. El unico archivo trackeado que la incumple es `debtec.md`; se deja y queda
c70b757:_persistence/decisions.md:472:- **Alternativas descartadas:** aplicarla retroactivamente y renombrar `debtec.md` a `techdebt.md`

$ git show c70b757:_persistence/decisions.md | grep -n "^### D-021"
573:### D-021 - `debtec.md` pasa a llamarse `techdebt.md`
```

  `_audit/S-004.md` §4 y §6 declara la discrepancia por iniciativa propia, pero la corrige con **5**
  para `progress.md`; el valor real sobre el commit es **6**.
- **Por que importa:** el defecto no es el numero, es la frase. `F-001` y `F-006` ya se abrieron por
  bloques que afirmaban mas ambito del que su comando comprobaba, y de ahi salieron `D-019` y
  `L-006`. `D-021` es la primera entrada escrita despues de esa leccion y reincide, ademas
  **afirmando explicitamente una reproducibilidad que no tiene** — lo que desalienta la
  comprobacion en vez de solo omitirla.
- **Que se hizo:** `manager` lo acepta (2026-09-01, sesion `S-005`). Verificado contra `HEAD`
  (`e61454b`) que el defecto sigue vivo, incluido el subclaim de las 13 de `decisions.md`, que se
  comprobo aparte y no se dio por bueno:

```
$ git grep -n "debtec" c70b757 -- _persistence/decisions.md | awk -F: '$3>=573' | wc -l
9

$ git grep -c "debtec" HEAD -- _persistence/decisions.md
HEAD:_persistence/decisions.md:13
```

  Nueve de las trece caen dentro de `D-021`; el recuento de `progress.md` es 6 y no 2, y falta
  `_audit/S-004.md:17`. Se anade una nota fechada bajo el bloque de `D-021` con el recuento real
  sobre `c70b757` y la separacion de las 9 internas; el bloque original queda intacto (`D-019`).
  Registrado en `T-011`.

- **Cerrado por `R-005`** sobre `510d580`: la nota fechada bajo `D-021` corrige la frase, da el
  recuento sobre `c70b757` y separa las 9 coincidencias internas de las 4 externas. El subclaim se
  reprodujo:

```
$ git grep -n "debtec" c70b757 -- _persistence/decisions.md | awk -F: '$3>=573' | wc -l
9
```

---

### F-009 - `DT-001` queda `Implementada` con un criterio de cierre que no se cumple
| Campo | Valor |
|---|---|
| Auditoria | R-004 |
| Fecha | 2026-09-01 |
| Gravedad | Baja |
| Estado | Implementado |
| Registrado en | T-012 |
| Cerrado en | `510d580` (R-005) |

- **Que se observo:** el criterio de pago escrito en la entrada es absoluto, y la entrada pasa a
  `Implementada` en el mismo commit:

```
$ git show c70b757:_persistence/techdebt.md | sed -n '91,92p'
- **Como se paga:** renombrar a `techdebt.md` con `git mv`, actualizar todas sus referencias, y
  comprobar con `git grep -n "debtec" -- .` que no queda ninguna.

$ git show c70b757:_persistence/techdebt.md | sed -n '13p'
| [DT-001](#dt-001---debtecmd-incumple-la-regla-de-nombres-en-ingles) | `debtec.md` incumple la regla de nombres en ingles | Implementada | Confirmada | Baja | No bloqueante |
```

  Ese comando devuelve 11 archivos con coincidencias (salida en `F-008`). `D-021` acota el alcance
  al «ambito vivo» y la nota fechada de `DT-001` remite a `D-021`, pero el texto del criterio no se
  acota ni se declara superado.
- **Por que importa:** es el mismo defecto que `F-007`, cuya leccion `L-007` se escribe en este
  mismo commit —«una excepcion se escribe donde esta la regla, no donde se decidio»— y se repite
  tres archivos mas alla. Quien aplique el criterio literal concluye que la deuda no esta pagada.
  Gravedad `Baja` porque la informacion correcta si esta en la misma entrada, en la nota que remite
  a `D-021`: el dano es de lectura.
- **Que se hizo:** `manager` lo acepta (2026-09-01, sesion `S-005`). Verificado contra `HEAD`
  (`e61454b`) que el criterio literal sigue sin cumplirse y la entrada sigue `Implementada`:

```
$ git grep -c "debtec" HEAD -- . | wc -l
12

$ git grep -n "debtec" HEAD -- .claude CLAUDE.md project.md ; echo "exit=$?"
exit=1
```

  Se anade a la nota fechada de `DT-001` el criterio de cierre realmente aplicado —cero en el ambito
  vivo, historico intacto por `D-021`— con su comando y su salida cruda. El campo «Como se paga»
  original no se reescribe. Registrado en `T-012`.

- **Cerrado por `R-005`** sobre `510d580`: la nota de `DT-001` enuncia el criterio de cierre
  realmente aplicado, y sus dos comandos **si** se reproducen sobre el commit que los contiene. El
  campo «Como se paga» quedo intacto.

```
$ git grep -n "debtec" 510d580 -- .claude CLAUDE.md project.md ; echo "exit=$?"
exit=1

$ git ls-tree --name-only 510d580 _persistence/ | grep -i debt
_persistence/techdebt.md
```

---

### F-010 - Una convencion vigente de `_audit/findings.md` cita un archivo que ya no existe
| Campo | Valor |
|---|---|
| Auditoria | R-004 |
| Fecha | 2026-09-01 |
| Gravedad | Baja |
| Estado | Implementado |
| Registrado en | T-013, T-018 |
| Cerrado en | R-006 (`d906a5d`) |

- **Que se observo:**

```
$ git show c70b757:_audit/findings.md | sed -n '52,54p'
⚠️ **Un rechazo por coste o prioridad es deuda tecnica por definicion**, y exige su `DT-XXX`. Un
rechazo por coste sin entrada en `debtec.md` es, por si solo, un hallazgo nuevo — y no requiere
criterio: se comprueba mirando si la entrada existe.

$ git ls-tree --name-only c70b757 _persistence/ | grep -i debt
_persistence/techdebt.md
```

  No es una cita historica: es una regla vigente de este mismo archivo, que manda comprobar una
  entrada en una ruta que ya no existe.
- **Por que importa:** `D-021` clasifico `_audit/` entero como historico. Es correcto para los
  `S-XXX.md` y los `R-XXX.md`, que son documentos entregados, pero `findings.md` es un registro
  vivo cuyas convenciones se siguen aplicando. El criterio se aplico por carpeta y no por naturaleza
  del texto, y deja fuera del barrido el unico archivo de `_audit/` que sigue rigiendo.
- **Que se hizo:** `manager` lo acepta (2026-09-01, sesion `S-005`). Verificado contra `HEAD`
  (`e61454b`) que la convencion sigue citando el archivo inexistente:

```
$ git grep -n "debtec" HEAD -- _audit/findings.md | head -1
HEAD:_audit/findings.md:56:rechazo por coste sin entrada en `debtec.md` es, por si solo, un hallazgo nuevo — y no requiere

$ git ls-tree --name-only HEAD _persistence/ | grep -i debt
_persistence/techdebt.md
```

  Se acota por nota fechada el alcance de `D-021`: `_audit/` es historico **salvo las secciones de
  convenciones de `findings.md` e `index.md`**, que son ambito vivo. Registrado en `T-013`.
- ⚠️ **La correccion del texto de la linea 56 queda pendiente y no es de `manager`.** Este archivo
  lo escribe `report_auditor`; `manager` solo toca la fila de estado de cada hallazgo. Lo entregado
  aqui es el criterio que permite corregirla — el cambio de `debtec.md` a `techdebt.md` en esa
  convencion lo hace el auditor en una pasada posterior.

- 🚨 **`R-005` lo deja `Aceptado — pendiente` sobre `510d580`, no cerrado.** La parte de `manager`
  esta hecha (la nota fechada de `D-021` acota `_audit/` a historico salvo las convenciones vivas),
  pero el defecto sigue vivo:

```
$ git grep -n "debtec" 510d580 -- _audit/findings.md | head -1
510d580:_audit/findings.md:56:rechazo por coste sin entrada en `debtec.md` es, por si solo, un hallazgo nuevo — y no requiere
```

  Y **la auditoria tampoco corrige esa linea**: su protocolo le prohibe corregir nada sobre el commit
  auditado y solo la autoriza a escribir hallazgos, estados y filas. Quien corrige la seccion de
  convenciones de este archivo **no esta decidido**, y hasta que `manager` o el usuario lo zanjen con
  su `D-XXX`, este hallazgo no lo puede cerrar nadie. Ver `R-005`, seccion 5.


---

🕒 **Actualizacion del 2026-09-02 (`S-006`).** `R-005` mantuvo este hallazgo `Aceptado —
pendiente` porque `T-013` entrego el criterio pero no la correccion, y señalo en su seccion 5 que
**nadie podia hacerla**: el auditor tiene prohibido corregir y `manager` tenia prohibido escribir en
este archivo. El punto muerto se zanja con `D-027`, y la correccion va en `T-018`: la linea de la
seccion «Convenciones» ya cita el nombre vigente. Las demas apariciones del nombre antiguo en este
archivo son **citas de evidencia dentro de hallazgos entregados** y se dejan intactas.

```
$ sed -n '1,70p' _audit/findings.md | grep -n "debtec" ; echo "exit=$?"
exit=1
```

⚠️ **El estado no cambia y no puede cambiarlo `manager`:** sigue `Aceptado — pendiente`.
`Implementado` lo escribe la auditoria siguiente, verificando la correccion sobre un commit
posterior.

### F-011 - La nota nueva de `A-001` vuelve a registrar un recuento sobre `HEAD` que no se reproduce sobre su commit
| Campo | Valor |
|---|---|
| Auditoria | R-005 |
| Fecha | 2026-09-01 |
| Gravedad | Media |
| Estado | Implementado |
| Registrado en | T-014 |
| Cerrado en | R-006 (`d906a5d`) |

- **Que se observo:** la nota fechada que corrige `F-005` cierra el enunciado de la señal 2 rehecha
  con un bloque sobre `HEAD` que presenta como prueba de que «hoy la señal sigue sin cumplirse»:

```
$ git grep -n "| Pendiente |" HEAD -- _audit/index.md ; echo "exit=$?"
exit=1
```

  Sobre el commit que contiene la nota, el mismo comando devuelve lo contrario:

```
$ git grep -n "| Pendiente |" 510d580 -- _audit/index.md ; echo "exit=$?"
510d580:_audit/index.md:16:| `S-005.md` | S-005 | 2026-09-01 | Pendiente | Pendiente | Pendiente | - |
exit=0
```

  Segunda instancia, en `_persistence/tasks.md`, ficha de `T-012`: «el comando devuelve **12**
  archivos en `HEAD`», sin fecha ni ancla. Sobre el commit son 13:

```
$ git grep -c "debtec" 510d580 -- . | wc -l
13
```

- **Por que importa:** es el patron de `F-005`, `F-006` y `F-008` reapareciendo dentro de la
  correccion de `F-005`, y contra `D-022` regla 1, escrita en el mismo commit. Quien reproduzca el
  bloque de `A-001` sobre su commit obtiene `exit=0` y concluye que la señal 2 **si** se disparo, lo
  contrario de lo que la nota afirma — y esa es una de las dos señales que pueden refutar `A-001`.
  `Media` y no `Alta` porque el fondo de la correccion es correcto: la señal quedo bien redefinida y
  el bloque original quedo intacto.
- **Que se hizo:** `manager` lo **acepta** (2026-09-02, sesion `S-006`). Verificado contra `HEAD`
  (`a800d6b`) antes de tratarlo: el bloque de `A-001` sigue devolviendo `exit=1` sobre `HEAD` y
  `exit=0` sobre `510d580`, y el recuento global ya no da 12 ni 13 sino **14** — el hallazgo se
  sostiene entero, y la cifra que crece es la mejor prueba de por que `D-022` exige el ancla.

```
$ git grep -n "| Pendiente |" a800d6b -- _audit/index.md ; echo "exit=$?"
exit=1

$ git grep -c "debtec" a800d6b -- . | wc -l
14
```

  Corregido en `T-014`: dos notas fechadas anclan los bloques a `e61454b`, el `HEAD` real del
  momento, donde **si** se reproducen (`exit=1` y 12). Los originales quedan intactos (`D-019`).
  El asunto de fondo que el hallazgo señala —`D-022` sin mecanismo que la aplique— se atiende
  aparte, en `T-019`.

---

### F-012 - La segunda excepcion de `D-025` no llego a los tres sitios que siguen diciendo «es la unica excepcion»
| Campo | Valor |
|---|---|
| Auditoria | R-005 |
| Fecha | 2026-09-01 |
| Gravedad | Media |
| Estado | Implementado |
| Registrado en | T-015 |
| Cerrado en | R-006 (`d906a5d`) |

- **Que se observo:** `D-025` generaliza la excepcion de escritura de `manager` sobre `tasks.md` a un
  segundo caso y la escribe solo en la convencion de ese archivo. Los tres sitios que enuncian la
  regla para quien la ejecuta siguen diciendo que la excepcion es unica:

```
$ git grep -n "unica excepcion\|salvo la .T-XXX" 510d580 -- .claude CLAUDE.md _phases _persistence/tasks.md
510d580:.claude/agents/session-closer.md:68:auditable. **No la dupliques ni la reescribas:** comprueba que esta y sigue. Es la unica excepcion a
510d580:.claude/skills/protocol-close/SKILL.md:40:auditable. **No la dupliques ni la reescribas:** comprueba que esta y sigue. Es la unica excepcion a
510d580:.claude/skills/protocol-close/SKILL.md:447:**La unica excepcion, y es mecanica:** si un supuesto `A-XXX` quedo comprobado por la evidencia del
510d580:_persistence/tasks.md:57:con `progress.md`. **Tiene una unica excepcion, y esta escrita:** cuando `manager` evalua un hallazgo
510d580:_phases/000_preproject.md:182:| `tasks.md` | las tareas y su estado | **`session-closer`**, salvo la `T-XXX` que nace de un hallazgo aceptado |
```

  La linea 447 es de otro asunto (supuestos) y no cuenta. La 57 de `tasks.md` conserva el enunciado
  viejo pero el texto siguiente lo corrige explicitamente, asi que se lee entera y no engaña.
- **Por que importa:** es `F-007` otra vez, y `F-007` se cerro en `S-004` arreglando **esos mismos
  tres sitios**; `L-007` lleva escrita desde entonces. El `session-closer` arranca en frio y lee su
  skill, no `decisions.md`: con este texto tratara como infraccion una fila de `tasks.md` editada a
  mano que no nazca de un hallazgo. Y `_phases/000_preproject.md:182` nace hoy con la version vieja
  de la regla dentro.
- **Que se hizo:** `manager` lo **acepta** (2026-09-02, sesion `S-006`). Verificado contra `HEAD`
  (`a800d6b`): los tres sitios seguian afirmando que la excepcion es unica.

```
$ git grep -n "unica excepcion\|salvo la .T-XXX" a800d6b -- .claude CLAUDE.md _phases _persistence/tasks.md
a800d6b:.claude/agents/session-closer.md:68:auditable. **No la dupliques ni la reescribas:** comprueba que esta y sigue. Es la unica excepcion a
a800d6b:.claude/skills/protocol-close/SKILL.md:40:auditable. **No la dupliques ni la reescribas:** comprueba que esta y sigue. Es la unica excepcion a
a800d6b:.claude/skills/protocol-close/SKILL.md:447:**La unica excepcion, y es mecanica:** si un supuesto `A-XXX` quedo comprobado por la evidencia del
a800d6b:_persistence/tasks.md:57:con `progress.md`. **Tiene una unica excepcion, y esta escrita:** cuando `manager` evalua un hallazgo
a800d6b:_phases/000_preproject.md:182:| `tasks.md` | las tareas y su estado | **`session-closer`**, salvo la `T-XXX` que nace de un hallazgo aceptado |
exit=0
```

  Corregido en `T-015`, y se toma ademas el **criterio que la propia auditoria propuso**: la
  excepcion se reconoce por la cita —un `D-XXX` o un `F-NNN` en la propia tarea—, no por el numero
  de filas. Los tres textos lo enuncian asi, y al agente se le dice explicitamente que **una fila
  con su cita no es un desfase**, que era el dano concreto del hallazgo.

---

### F-013 - `D-023` conserva vigente una advertencia que `D-026` desmiente en el mismo commit
| Campo | Valor |
|---|---|
| Auditoria | R-005 |
| Fecha | 2026-09-01 |
| Gravedad | Baja |
| Estado | Implementado |
| Registrado en | T-016 |
| Cerrado en | R-006 (`d906a5d`) |

- **Que se observo:**

```
$ git show 510d580:_persistence/decisions.md | grep -n "todavia no entra en el ambito del Paso 1b" -A 3
877:⚠️ **`_phases/` todavia no entra en el ambito del Paso 1b**, que hoy cubre solo `.claude`,
878-`CLAUDE.md` y `project.md`. Mientras no entre, la agnosticidad de estos archivos **depende de que
879-alguien se acuerde**, que es justo lo que `L-008` describe. Ampliar el ambito del control es una
880-modificacion del protocolo y queda pendiente de acordarla con el usuario.

$ git show 510d580:.claude/skills/protocol-close/SKILL.md | grep -n "CLAUDE.md _phases"
96:git grep -nE "<nombre del proyecto>|<carpeta raiz de las rutas absolutas>|<host del remoto>" -- .claude CLAUDE.md _phases
```

- **Por que importa:** una entrada `Vigente` presenta como pendiente algo que `D-026` ya hizo en el
  mismo commit, y describe mal el ambito del control. Quien lea `D-023` sin llegar a `D-026`
  concluye que la agnosticidad de `_phases/` no tiene control que la compruebe. `Baja` porque la
  informacion correcta esta a tres entradas de distancia y nada operativo depende de esta linea.
- **Que se hizo:** `manager` lo **acepta** (2026-09-02, sesion `S-006`). Verificado contra `HEAD`
  (`a800d6b`): la advertencia sigue vigente en `D-023` y el control ya cubre `_phases/`.

```
$ git grep -n "todavia no entra en el ambito del Paso 1b" a800d6b -- _persistence/decisions.md ; echo "exit=$?"
a800d6b:_persistence/decisions.md:877:⚠️ **`_phases/` todavia no entra en el ambito del Paso 1b**, que hoy cubre solo `.claude`,
exit=0

$ git grep -n "CLAUDE.md _phases" a800d6b -- .claude ; echo "exit=$?"
a800d6b:.claude/skills/protocol-audit/SKILL.md:140:git grep -nE "<nombre del proyecto>|<carpeta raiz de las rutas absolutas>|<host del remoto>" <hash> -- .claude CLAUDE.md _phases
a800d6b:.claude/skills/protocol-close/SKILL.md:96:git grep -nE "<nombre del proyecto>|<carpeta raiz de las rutas absolutas>|<host del remoto>" -- .claude CLAUDE.md _phases
exit=0
```

  Corregido en `T-016` por nota fechada, sin reescribir el original (`D-019`). **El hallazgo se
  quedaba corto:** la advertencia tambien describia mal el ambito **anterior** —decia tres rutas
  donde habia dos, y la tercera nunca estuvo en el control—. La nota lo corrige tambien, con su
  comando sobre `c70b757`.

---

### F-014 - El «Avance de la etapa» de `progress.md` atribuye mal la procedencia de los hallazgos y cuenta `F-006` dos veces
| Campo | Valor |
|---|---|
| Auditoria | R-005 |
| Fecha | 2026-09-01 |
| Gravedad | Baja |
| Estado | Implementado |
| Registrado en | T-017 |
| Cerrado en | R-006 (`d906a5d`) |

- **Que se observo:**

```
$ git show 510d580:_persistence/progress.md | grep -n "dejo cinco hallazgos abiertos" | cut -c1-220
59:| Avance de la etapa | El commit `e61454b` (auditoria `R-004` sobre `S-004`) dejo cinco hallazgos abiertos (`F-005`, `F-006`, `F-008`, `F-009`, `F-010`), sumados al `F-006` ya abierto por `R-003`. `manager` evaluo los

$ git show 510d580:_audit/index.md | sed -n '14,15p'
| `S-003.md` | S-003 | 2026-09-01 | `ea0b850` | `R-003.md` | Con hallazgos (3) | F-005, F-006, F-007 |
| `S-004.md` | S-004 | 2026-09-01 | `c70b757` | `R-004.md` | Con hallazgos (3) | F-008, F-009, F-010 |
```

  `R-004` abrio tres; `F-005` y `F-006` los abrio `R-003`. La frase atribuye los cinco a `R-004` y
  despues suma `F-006` otra vez, que ya esta en su propia lista.
- **Por que importa:** `progress.md` es lo primero que lee `session-starter` en cada arranque, y de
  los tres textos que cuentan lo mismo es el unico que se lee siempre. `Baja` porque no hay
  consecuencia operativa: los seis hallazgos quedaron evaluados y registrados correctamente.
- **Que se hizo:** `manager` lo **acepta** (2026-09-02, sesion `S-006`). Verificado contra `HEAD`
  (`a800d6b`): la frase sigue ahi, y el tablero sigue desmintiendola.

```
$ git grep -c "dejo cinco hallazgos abiertos" a800d6b -- _persistence/progress.md
a800d6b:_persistence/progress.md:1

$ sed -n '14,15p' _audit/index.md
| `S-003.md` | S-003 | 2026-09-01 | `ea0b850` | `R-003.md` | Con hallazgos (3) | F-005, F-006, F-007 |
| `S-004.md` | S-004 | 2026-09-01 | `c70b757` | `R-004.md` | Con hallazgos (3) | F-008, F-009, F-010 |
```

  Corregido en `T-017`. **El hallazgo se quedaba corto por dos lados**, y las dos ampliaciones se
  registran aqui porque son del mismo defecto, no hallazgos nuevos:

  1. **Un tercer error en la misma frase:** «`manager` evaluo los seis». Fueron **cinco**. `R-003`
     abrio tres y `R-004` abrio tres, pero `F-007` ya se habia aceptado y corregido en `S-004`
     (`T-008`). Las cinco tareas que produjo la sesion lo confirman:

```
$ grep -cE "^[|] Sesion [|] S-005 [|]" _persistence/tasks.md
5
```

  2. **El mismo error estaba en tres sitios, no en uno.** Las secciones 1 y 2 —que el cierre
     sobrescribe— quedaron reescritas; la bitacora, que es historico, lleva nota fechada.

  ⚠️ **Que `manager` escriba en un archivo del cierre lo autoriza `D-027`**, escrita hoy a raiz
  del punto muerto que esta misma auditoria señalo en su seccion 5.

---

### F-015 - `005_discovery` sigue declarada sin su archivo en `_phases/`, y ya nadie lo agenda
| Campo | Valor |
|---|---|
| Auditoria | R-006 |
| Fecha | 2026-09-02 |
| Gravedad | Media |
| Estado | Implementado |
| Registrado en | `T-020` |
| Cerrado en | R-007 (`122b770`) |

- **Que se observo:** `D-023` es una decision **vigente** cuyo titulo dice «Cada etapa declarada
  tiene su archivo agnostico en `_phases/`». `project.md` declara dos etapas; `_phases/` contiene un
  archivo. No hay `T-XXX` ni `DT-XXX` que lo agende.

```
$ git show d906a5d:_persistence/decisions.md | grep -n "^### D-023"
815:### D-023 - Cada etapa declarada tiene su archivo agnostico en `_phases/`

$ git show d906a5d:_persistence/decisions.md | sed -n '819,821p'
| Fecha | 2026-09-01 |
| Estado | Vigente |
| Origen | usuario |

$ git show d906a5d:project.md | grep -n "Etapas declaradas"
102:| Etapas declaradas | `000_preproject`, `005_discovery` |

$ git ls-tree --name-only d906a5d _phases/
_phases/000_preproject.md

$ git grep -niE "phases" d906a5d -- _persistence/tasks.md ; echo "exit=$?"
exit=1
```

- **Por que importa:** es la tercera sesion consecutiva en que el asunto se nombra sin agendarlo
  (`D-024` como advertencia, `R-005` como recomendacion sin hallazgo, `S-006` en sus secciones 2 y
  4). Lo que solo vive en prosa dentro de informes de sesion no aparece en `tasks.md`, que es lo que
  `session-starter` lee al arrancar: desaparece del radar en cuanto nadie se acuerde de repetirlo.
  `Media` y no `Alta` porque `T-001` sigue sin arrancar y hoy no bloquea nada; sera bloqueante el
  dia que la etapa empiece.
- **Que se hizo:** **aceptado** el 2026-09-02 (`S-007`). Verificado contra `HEAD` (`111fc40`) antes
  de evaluarlo: el hallazgo seguia vivo, tal cual. Se abre `T-020` y **se escribe el archivo en la
  misma sesion**, porque el usuario pidio abordar `005_discovery` justo despues. De las dos opciones
  que ofrecia la auditoria —una `T-XXX` o una `DT-XXX` de aplazamiento— se tomo la primera: aplazar
  habria sido registrar deuda sobre algo que ya tocaba hacer. `Aceptado — pendiente` y no
  `Implementado`, que lo escribe la auditoria siguiente.

```
$ grep -n "Etapas declaradas" project.md
79:| Etapas declaradas | `000_preproject`, `005_discovery` |

$ ls -1 _phases/
000_preproject.md

$ grep -niE "phases" _persistence/tasks.md ; echo "exit=$?"
exit=1
```

  *(los tres comandos, ejecutados sobre `111fc40` antes de tocar nada — el segundo devuelve ya dos
  archivos, y el tercero deja de estar vacio, en cuanto se aplica `T-020`.)*

- **Cerrado por `R-007`** sobre `122b770`: la correccion esta en el diff de ese commit.
  `_phases/005_discovery.md` existe, con las mismas ocho secciones que `_phases/000_preproject.md`,
  sin codigos instanciados y sin fuga de datos propios; `_phases/` contiene ya un archivo por cada
  etapa de la fila «Etapas declaradas» de `project.md`. Comandos y salidas crudas en `_audit/R-007.md`,
  seccion 1.

---

### F-016 - El criterio de cierre de `T-015` no se cumple al ejecutarlo, y la tarea queda `Implementada`
| Campo | Valor |
|---|---|
| Auditoria | R-006 |
| Fecha | 2026-09-02 |
| Gravedad | Baja |
| Estado | Implementado |
| Registrado en | `T-021` |
| Cerrado en | R-007 (`122b770`) |

- **Que se observo:** `T-015` declara como criterio de cierre «el barrido de la regla no devuelve
  ningun enunciado que siga afirmando que la excepcion es unica», y queda `Implementada`. El barrido,
  sobre el commit que la da por hecha, devuelve un enunciado:

```
$ git show d906a5d:_persistence/tasks.md | sed -n '/^### T-015/,/^### T-016/p' | grep -n "Criterio de cierre" -A1
23:- **Criterio de cierre:** el barrido de la regla no devuelve ningun enunciado que siga afirmando que
24-  la excepcion es unica, y el archivo de la etapa sigue pasando el control de agnosticidad.

$ git grep -n "unica excepcion\|salvo la .T-XXX" d906a5d -- .claude CLAUDE.md _phases _persistence/tasks.md
d906a5d:.claude/skills/protocol-close/SKILL.md:490:**La unica excepcion, y es mecanica:** si un supuesto `A-XXX` quedo comprobado por la evidencia del
d906a5d:_persistence/tasks.md:63:con `progress.md`. **Tiene una unica excepcion, y esta escrita:** cuando `manager` evalua un hallazgo
```

  La coincidencia de `protocol-close/SKILL.md:490` es de otra regla (supuestos `A-XXX`) y no cuenta.
  La de `_persistence/tasks.md:63` si: es la convencion del propio archivo, que sigue abriendo con
  «Tiene una unica excepcion» aunque cuatro parrafos mas abajo anuncie la segunda.
- **Por que importa:** es el mismo patron que `F-009` —un criterio de cierre autodeclarado que no se
  cumple al correrlo—, y aparece dentro de la tarea que corrige un hallazgo sobre ese mismo descuido.
  Quien vuelva a correr el barrido encontrara una coincidencia y no sabra si es un resto o un
  descuido. `Baja` porque el fondo esta bien: los tres sitios que `F-012` señalaba estan corregidos y
  ningun agente queda con la regla vieja.
- **Que se hizo:** **aceptado** el 2026-09-02 (`S-007`). Verificado contra `HEAD` (`111fc40`) antes
  de evaluarlo: el enunciado seguia vivo. Se abre `T-021` y se corrige en la misma sesion. De las dos
  opciones que ofrecia la auditoria se tomo **reescribir la convencion**, no acotar el criterio de
  `T-015`: el defecto estaba en la regla, que la lee quien ejecuta; el criterio solo la comprobaba.
  `T-015` conserva su texto y recibe una **nota fechada** que precisa como debia leerse (`D-019`).
  `Aceptado — pendiente` y no `Implementado`, que lo escribe la auditoria siguiente.

  ⚠️ **Y una precision que el hallazgo no pedia, por `L-009`:** el criterio de `T-015`, tal como
  estaba escrito, **no podia cumplirse nunca**. Un barrido global siempre devolvera las citas
  literales del texto viejo que guardan `_audit/` y el propio cuerpo de `T-015`, y ninguna de las dos
  se reescribe. Por eso `T-021` no hereda ese criterio: lo acota al sitio donde la regla se enuncia.

```
$ grep -rn "unica excepcion\|salvo la .T-XXX" .claude CLAUDE.md _phases _persistence/tasks.md
.claude/skills/protocol-close/SKILL.md:490:**La unica excepcion, y es mecanica:** si un supuesto `A-XXX` quedo comprobado por la evidencia del
_persistence/tasks.md:63:con `progress.md`. **Tiene una unica excepcion, y esta escrita:** cuando `manager` evalua un hallazgo
_persistence/tasks.md:463:  quien la ejecuta seguian diciendo «es la unica excepcion». Se reescriben los tres.
```

  *(ejecutado sobre `111fc40` antes de tocar nada. La linea 63 es la que `T-021` corrige; las otras
  dos son otra regla y una cita historica.)*

- **Cerrado por `R-007`** sobre `122b770`: la convencion de `tasks.md` abre ahora con «Tiene dos
  excepciones, y las dos estan escritas», y el barrido sobre la seccion «Convenciones» no devuelve
  ninguna variante viva; la unica coincidencia en `.claude CLAUDE.md _phases` es de otra regla (los
  supuestos `A-XXX` de `protocol-close`). `T-015` conserva su texto con su nota fechada (`D-019`).
  Comandos y salidas crudas en `_audit/R-007.md`, seccion 1. ⚠️ La ficha de `T-021` afirma ademas un
  barrido de variantes sobre todo el repositorio del que no registra ni patron ni salida: eso es
  `F-018`, hallazgo nuevo, y no reabre este.

---

### F-017 - `T-020` queda `Implementada` sin ningun bloque de verificacion, y el informe remite a una seccion que tampoco lo tiene
| Campo | Valor |
|---|---|
| Auditoria | R-007 |
| Fecha | 2026-09-02 |
| Gravedad | Media |
| Estado | Implementado |
| Registrado en | `T-023` |
| Cerrado en | `f096fff` (`R-008`) |

- **Que se observo:** `T-020` produce documentacion, asi que su Definicion de Terminado es «existe
  su bloque de verificacion: la orden ejecutada literal y su salida cruda» (`CLAUDE.md`, PI-5). La
  ficha no lleva ni un bloque de codigo; la de `T-021`, cerrada en la misma pasada, lleva dos:

```
$ git show 122b770:_persistence/tasks.md | sed -n '/^### T-020/,/^### T-021/p' | grep -c '^~~~'
0

$ git show 122b770:_persistence/tasks.md | sed -n '/^### T-021/,/^### T-022/p' | grep -c '^~~~'
4

$ git show 122b770:_audit/S-007.md | grep -n "ver seccion 6"
27:  arbol de trabajo (ver seccion 6).

$ git show 122b770:_audit/S-007.md | sed -n '/^## 6/,$p' | grep -c '^~~~'
0
```

  *(`~~~` transcribe el delimitador de bloque de codigo, para no cerrar este bloque)*

- **Por que importa:** el criterio **si se cumple** —`R-007` lo reprodujo—, asi que el registro no
  miente; lo que falta es la evidencia que lo hace reproducible sin rehacerlo. Es el patron de
  `F-009` y `F-016` por tercera vez: una tarea `Implementada` sostenida por un veredicto («se
  comprobo») en vez de por «corri esto, salio esto». `Media` porque `T-020` es la tarea que cierra
  un hallazgo de auditoria y porque es reincidencia, no primer caso.
- **Que se hizo:** **aceptado** el 2026-09-02 (`S-008`). Verificado contra `HEAD` (`ae06147`) antes
  de evaluarlo: la ficha de `T-020` seguia sin ningun bloque y la seccion 6 del informe tampoco lo
  tenia. Se abre `T-023`, que añade a la ficha los dos bloques que su propio criterio nombra, con su
  salida cruda y anclados a `122b770`, y con nota fechada que declara que se añaden despues — porque
  las ordenes si se ejecutaron en `S-007` (esta misma auditoria las reprodujo) y lo que falto fue
  registrarlas. Es el patron de `T-014`. El texto original de `T-020` no se toca (`D-019`).
  **`Aceptado — pendiente`**, que `Implementado` lo escribe la auditoria siguiente.

- **Verificado por `R-008`** sobre `f096fff`: la ficha de `T-020` lleva ahora sus dos bloques
  con salida cruda anclada a `122b770` y nota fechada que declara que se anadieron despues.
  Reproducidos: `git ls-tree --name-only 122b770 _phases/` devuelve los dos archivos de etapa, y
  `git grep -nE "RaindomAI|RaidomAI|Proyectos_TripleS|github\.com" 122b770 -- .claude CLAUDE.md _phases _methodology`
  devuelve `exit=1`. **`Implementado`.**

---

### F-018 - `T-021` afirma un barrido «sobre todo el repositorio» del que no registra ni el patron ni el ambito ni la salida
| Campo | Valor |
|---|---|
| Auditoria | R-007 |
| Fecha | 2026-09-02 |
| Gravedad | Baja |
| Estado | Implementado |
| Registrado en | `T-024` |
| Cerrado en | `f096fff` (`R-008`) |

- **Que se observo:** la ficha afirma un resultado sobre un ambito que sus dos bloques de
  verificacion no cubren —los dos corren acotados—, y el barrido global, reproducido, devuelve una
  linea que ninguno de los patrones escritos en la ficha alcanza, por ir en mayuscula:

```
$ git show 122b770:_persistence/tasks.md | sed -n '/^### T-021/,/^### T-022/p' | grep -n "todo el repositorio" -B2
20-  barre solo el ejemplo citado deja vivo el defecto. Se barrieron tambien las variantes que el patron
21-  del hallazgo no cubria —«una sola excepcion», «la excepcion es unica», «solo una excepcion»— sobre
22:  todo el repositorio. No aparecio ninguna mas viva de esta regla.

$ git grep -niE "una sola excepcion|la excepcion es unica|solo una excepcion|unica excepcion" 122b770 -- . | wc -l
45

$ git grep -nE "Unica excepcion" 122b770 -- .claude
122b770:.claude/agents/session-closer.md:90:  - *Unica excepcion, y es mecanica:* ascender un supuesto `A-XXX` ya comprobado por el diff — y
```

- **Por que importa:** `CLAUDE.md` obliga a que un resultado afirmado por iniciativa propia vaya con
  «el patron y el ambito con que se obtuvo». Aqui hubo que rehacer el barrido para contrastarlo, y al
  rehacerlo aparecio una coincidencia que el patron de la ficha no habria encontrado. `Baja` porque
  esa linea es de otra regla y la conclusion de fondo —ninguna variante viva de la regla vieja— es
  correcta.
- **Que se hizo:** **aceptado** el 2026-09-02 (`S-008`). Verificado contra `HEAD` (`ae06147`) antes
  de evaluarlo: la frase seguia afirmando un ambito que sus bloques no cubren. Se abre `T-024`, que
  acota la frase con nota fechada y añade el tercer bloque con el barrido global —patron insensible
  a mayusculas, ambito el repositorio, salida cruda, anclado a `122b770`— y una tabla que clasifica
  las catorce coincidencias del registro vivo. **`Aceptado — pendiente`**, que `Implementado` lo
  escribe la auditoria siguiente.

- **Verificado por `R-008`** sobre `f096fff`: la frase «sobre todo el repositorio» queda acotada
  con nota fechada y el tercer bloque trae el barrido global. Reproducido:
  `git grep -niE "..." 122b770 -- . | wc -l` devuelve `59`, y el mismo patron sobre
  `.claude CLAUDE.md _phases _persistence project.md` devuelve `14` — las cifras escritas en la
  ficha, al numero. **`Implementado`.**

---

### F-019 - La lista de archivos de la seccion 1 del informe no cuadra con el comando que dice haberla producido
| Campo | Valor |
|---|---|
| Auditoria | R-007 |
| Fecha | 2026-09-02 |
| Gravedad | Baja |
| Estado | Implementado |
| Registrado en | `T-025` |
| Cerrado en | `f096fff` (`R-008`) |

- **Que se observo:** la seccion 1 de `_audit/S-007.md` presenta su lista como salida de
  `git show --stat --name-only --format= HEAD` y la describe como «estos siete mas el nuevo». El
  comando devuelve diez archivos; la lista enumera ocho, y faltan `_audit/index.md` y el propio
  `_audit/S-007.md`:

```
$ git show --stat --name-only --format= 122b770
_audit/S-007.md
_audit/findings.md
_audit/index.md
_persistence/assumptions.md
_persistence/decisions.md
_persistence/lessons.md
_persistence/progress.md
_persistence/tasks.md
_phases/005_discovery.md
project.md

$ git show 122b770:_audit/S-007.md | sed -n '/^## 1\./,/^## 2\./p' | grep -c '^- `'
8

$ git show d906a5d:_audit/S-006.md | grep -n "su fila en"
50:`S-006`) y su fila en `_audit/index.md`.
```

- **Por que importa:** el informe es la unica pieza que le dice a la auditoria que estado esta
  juzgando; una lista presentada como salida de un comando que no coincide con el debilita justo lo
  que la hace util — y `S-006` si declaraba esos dos archivos, asi que es una regresion. `Baja`
  porque los dos omitidos son mecanica del cierre y ninguno esconde trabajo no declarado.
- **Que se hizo:** **aceptado el hallazgo el 2026-09-02 (`S-008`), y rechazada la correccion sobre
  `_audit/S-007.md`.** Verificado contra `HEAD` (`ae06147`) antes de evaluarlo: el comando sigue
  devolviendo diez archivos y la lista sigue enumerando ocho. La correccion **no se aplica al
  informe** —`D-040`—: un informe describe un commit ya auditado, y reescribirlo dejaria a `R-007`
  juzgando un estado que ya cambio. Ademas, completar la lista a mano volveria a producir el mismo
  defecto: una lista que dice venir de un comando y que nadie corrio. La correccion va al mecanismo,
  en `T-025`: la exigencia pasa del bloque explicativo a la **estructura del informe** de
  `protocol-close`, donde no se puede escribir la seccion 1 sin verla. **`Aceptado — pendiente`**,
  que `Implementado` lo escribe la auditoria siguiente.
- **Verificado por `R-008`** sobre `f096fff`: la correccion fue al mecanismo, y el efecto se ve en
  el propio `S-008`. `diff <(git show --name-only --format= f096fff | grep . | sort) <(lista pegada en la seccion 1)`
  no devuelve nada: dieciseis archivos en el comando, los mismos dieciseis en la lista.
  `_audit/S-007.md` sigue intacto, como `D-040` decidio. **`Implementado`.**

---

### F-020 - La entrada de `F-017` en `findings.md` conserva la linea que dice que sigue pendiente de evaluar
| Campo | Valor |
|---|---|
| Auditoria | R-008 |
| Fecha | 2026-09-02 |
| Gravedad | Baja |
| Estado | Implementado |
| Registrado en | `T-027` |
| Cerrado en | `fc91957` |

- **Que se observo:** la entrada de `F-017` tiene **dos** vinetas «Que se hizo» que se contradicen.
  `F-018` y `F-019` sustituyeron la linea vieja; `F-017` la dejo y anadio la nueva encima:

```
$ git show f096fff:_audit/findings.md | sed -n '/^### F-017/,/^### F-018/p' | grep -n "Que se hizo"
36:- **Que se hizo:** **aceptado** el 2026-09-02 (`S-008`). Verificado contra `HEAD` (`ae06147`) antes
43:- **Que se hizo:** pendiente de la evaluacion de `manager`.
```

- **Por que importa:** el registro de hallazgos dice dos cosas incompatibles sobre el mismo
  hallazgo. La fila del indice y el campo `Estado` llevan el dato bueno, pero quien lea la entrada de
  arriba abajo se queda con la ultima linea, que afirma que nadie lo evaluo. Es el archivo cuyo unico
  proposito es que un hallazgo no diga lo que nos convenga.
- **Que lo corregiria:** borrar la vineta residual «Que se hizo: pendiente de la evaluacion de
  `manager`» de la entrada de `F-017`, dejando solo la fechada.
- **Que se hizo:** **aceptado** el 2026-09-02 (`S-009`). Verificado contra `HEAD` (`7025a05`) antes
  de evaluarlo: la entrada de `F-017` seguia con las dos vinetas «Que se hizo», la fechada en la
  linea 36 y la residual en la 43. Se abre `T-027`, que borra la residual y deja solo la fechada; ni
  el texto de esa vineta, ni la fila del indice, ni el campo `Estado` se tocan, porque ya decian lo
  correcto. Lo autoriza `D-027`: la entrada de un hallazgo es registro vivo, y el texto concreto que
  senala un hallazgo aceptado lo corrige `manager`. **`Aceptado — pendiente`**, que `Implementado` lo
  escribe la auditoria siguiente.


- **Verificado por `R-009`** sobre `fc91957`: corregido. La entrada de `F-017` tiene exactamente una
  vineta «Que se hizo», la fechada.

~~~
$ git show fc91957:_audit/findings.md | sed -n '/^### F-017/,/^### F-018/p' | grep -c "Que se hizo"
1
~~~

  **`Implementado`.**

---

### F-021 - `progress.md` atribuye a `R-007` un commit auditado que no es el suyo
| Campo | Valor |
|---|---|
| Auditoria | R-008 |
| Fecha | 2026-09-02 |
| Gravedad | Baja |
| Estado | Implementado |
| Registrado en | `T-028` |
| Cerrado en | `51354ef` |

- **Que se observo:** el campo «Avance de la etapa» abre con «`R-007` (sobre `ae06147`)». `ae06147`
  es el commit que **contiene** `R-007`, no el que `R-007` audito, que es `122b770`:

```
$ git grep -n "R-007. (sobre" f096fff -- _persistence
f096fff:_persistence/progress.md:62:| Avance de la etapa | `R-007` (sobre `ae06147`) abrio `F-017`, `F-018` y `F-019`. ...

$ git show f096fff:_audit/R-007.md | grep -n "Commit auditado"
7:| Commit auditado | `122b770` |

$ git show f096fff:_audit/index.md | grep "S-007"
| `S-007.md` | S-007 | 2026-09-02 | `122b770` | `R-007.md` | Con hallazgos (3) | F-017, F-018, F-019 |
```

- **Por que importa:** `progress.md` es lo que `session-starter` lee al arrancar y lo primero que se
  cita al reconstruir que paso. Un hash mal atribuido manda a quien lo siga a un commit que no
  contiene nada de lo que se le dice que encontrara. La entrada de `S-007`, en el mismo archivo,
  escribio la formula bien: «`R-006` (sobre `d906a5d`)».
- **Que lo corregiria:** sustituir `ae06147` por `122b770` en esa primera mencion. El segundo
  `ae06147` de la misma celda —«verifico los tres contra `HEAD` (`ae06147`)»— es correcto y no se
  toca.
- **Que se hizo:** **aceptado** el 2026-09-02 (`S-009`). Verificado contra `HEAD` (`7025a05`) antes
  de evaluarlo: la celda seguia diciendo «`R-007` (sobre `ae06147`)», y `_audit/index.md` confirma
  que el commit auditado por `R-007` es `122b770`. Se abre `T-028`, que corrige esa primera mencion y
  deja nota fechada; el segundo `ae06147` de la misma celda —el `HEAD` contra el que se verificaron
  los hallazgos— es correcto y no se toca, igual que la bitacora y la seccion 2. Lo autoriza `D-027`,
  que reparte a `manager` las secciones de `progress.md` que el cierre sobrescribe.
  **`Aceptado — pendiente`**.


- **Verificado por `R-009`** sobre `fc91957`: **no corregido; sigue `Aceptado — pendiente`.** La
  cadena señalada desaparecio del archivo, pero **no por correccion**: la celda «Avance de la etapa»
  se sobrescribio entera con el contenido de `S-009`, como hace cada cierre. El diff no toca esa
  cadena en ningun sitio, y la nota fechada que `T-028` declara haber dejado no existe.

~~~
$ git show fc91957:_persistence/progress.md | grep -o 'R-007` (sobre `[0-9a-f]*`)' ; echo "exit=$?"
exit=1

$ git show fc91957 -- _persistence/progress.md | grep -c "^[+-].*ae06147"
0
~~~

  Se abre `F-024` por la afirmacion sin respaldo.

- **Nota del 2026-09-02 (`T-032`, hallazgo `F-024`):** la viñeta «Que se hizo» de mas arriba
  afirma una nota fechada que **no llego a existir**. `T-028` si edito la celda, pero el cierre
  la sobrescribio entera en el mismo commit. **El texto original no se reescribe** (`D-019`).
  `D-050` fija el tratamiento: `F-021` queda resuelto **por desaparicion del texto**, no por
  correccion, y `T-028` pasa a `Cancelada` con `T-032` como relevo. La cadena no sobrevive en
  ninguna parte del archivo, asi que no queda nada que corregir en su sitio:

~~~
$ git show 99c3aa3:_persistence/progress.md | grep -o 'R-007` (sobre `[0-9a-f]*`)' ; echo "exit=$?"
exit=1
~~~


- **Cerrado por `R-010`** sobre `51354ef`: resuelto **por desaparicion del texto**, no por
  correccion, y asi queda escrito (`D-050`, `T-032`, `L-015`; `T-028` pasa a `Cancelada`). Sobre el
  commit no queda ninguna atribucion **viva** del commit equivocado a `R-007`: las dos unicas
  ocurrencias de la cadena estan dentro del bloque de evidencia de la nota de `T-032`.

~~~
$ git show 51354ef:_persistence/progress.md | grep -n 'R-007` (sobre'
440:$ git show fc91957:_persistence/progress.md | grep -o 'R-007` (sobre `[0-9a-f]*`)' ; echo "exit=$?"
444:43:-| Avance de la etapa | `R-007` (sobre `ae06147`) abrio `F-01
~~~

  **`Implementado`.**

---

### F-022 - Tres bloques de verificacion de `decisions.md` registran una salida que no se reproduce
| Campo | Valor |
|---|---|
| Auditoria | R-008 |
| Fecha | 2026-09-02 |
| Gravedad | Media |
| Estado | Implementado |
| Registrado en | `T-029` |
| Cerrado en | `fc91957` |

- **Que se observo:** `D-036`, `D-038` y `D-040` afirman cada uno una salida concreta, y ninguna sale
  al correr la orden literal.

`D-036` escribe `grep -n "_discovery" project.md ; echo "exit=$?"` con resultado `exit=1`. El patron
no lleva barra, y la cadena `005_discovery` contiene `_discovery`:

```
$ git show f096fff:project.md | grep -c "_discovery"
10

$ git show f096fff:project.md | grep -n "_discovery" | tail -3 ; echo "exit=$?"
166:| `N-XXX` | `_discovery/005_needs.md`, el artefacto de necesidades de `005_discovery` (`D-036`) | necesidad |
167:| `I-XXX` | `_discovery/015_stakeholders.md`, el artefacto de interesados de `005_discovery` (`D-038`) | interesado |
184:—porque el archivo de etapa de `005_discovery` lo cita y un codigo citado sin declarar es un
exit=0
```

Sobre `122b770`, antes de esta sesion, el mismo comando ya devolvia seis lineas: **la salida
registrada no pudo salir nunca**. Lo que la decision quiere demostrar —que `_discovery/` no tiene
fila en «Carpetas propias»— si es cierto; el comando escrito no lo demuestra.

`D-038` escribe un barrido de `I-NNN` sobre `_persistence/ _audit/ project.md` con resultado
`exit=1`:

```
$ git archive f096fff | tar -x -C "$TMP" ; cd "$TMP"
$ grep -rnoE "\bI-[0-9]{3}\b" _persistence/ _audit/ project.md ; echo "exit=$?"
_persistence/decisions.md:1617:I-001
_persistence/decisions.md:1626:I-001
_persistence/decisions.md:1633:I-001
_persistence/decisions.md:1762:I-001
_persistence/tasks.md:843:I-001
_persistence/tasks.md:844:I-002
_persistence/tasks.md:845:I-003
exit=0
```

El fondo es correcto —no habia ningun `I-NNN` con el que colisionar **antes** de la decision—, pero
el bloque se escribio sin anclar, y las siete coincidencias son texto que la propia sesion acababa
de escribir. Anclado a `122b770` con `git grep`, el bloque diria la verdad.

`D-040` escribe `git status --porcelain -- _audit/S-007.md ; echo "exit=$?"` con resultado `exit=1`.
`git status` devuelve `0` cuando no tiene nada que reportar:

```
$ git status --porcelain -- _audit/S-007.md ; echo "exit=$?"
exit=0
```

La misma comprobacion escrita en `T-025` como `| wc -l` con resultado `0` si es correcta.

- **Por que importa:** un bloque de verificacion existe para que nadie tenga que rehacer el barrido.
  Uno cuya salida no se reproduce cuesta mas que no tenerlo: obliga a repetirlo **y** a averiguar si
  la diferencia es un error de transcripcion o una afirmacion falsa. `Media` porque son tres en un
  mismo commit y porque la familia —`F-005`, `F-008`, `F-011`— ya llevaba tres avisos.
- **Que lo corregiria:** en `D-036`, acotar el patron a la fila de «Carpetas propias» que se quiere
  demostrar; en `D-038`, anclar el barrido a `122b770` con `git grep`; en `D-040`, usar el `| wc -l`
  que ya emplea `T-025`. `CLAUDE.md` prohibe reescribir una salida antigua para que exhiba lo que no
  dio: la forma correcta es la nota fechada al lado, no el borrado.
- **Que se hizo:** **aceptado** el 2026-09-02 (`S-009`). Verificados contra `HEAD` (`7025a05`) los
  tres casos, uno por uno: `grep -n "_discovery" project.md` devuelve diez lineas y `exit=0`, no
  `exit=1`; el barrido de `I-[0-9]{3}` sin anclar devuelve veinticuatro coincidencias sobre el arbol
  de hoy, no cero; y `git status --porcelain -- _audit/S-007.md` sale con `exit=0`. Los tres se
  sostienen. Se abre `T-029`, que **no reescribe ninguna salida** —`CLAUDE.md` lo prohibe
  expresamente— y anade a cada bloque una nota fechada con la orden que si demuestra lo que la
  decision queria demostrar, y su salida cruda. **`Aceptado — pendiente`**.


- **Verificado por `R-009`** sobre `fc91957`: corregido. Las tres notas fechadas existen y las tres
  ordenes nuevas se reproducen tal cual sobre el commit.

~~~
$ git show fc91957:_persistence/decisions.md | grep -c 'Nota del 2026-09-02 (`T-029`, hallazgo `F-022`)'
3

$ git show f096fff:project.md | grep -n '^| `_discovery/`' ; echo "exit=$?"
exit=1

$ git grep -nE "\bI-[0-9]{3}\b" 122b770 -- _persistence/ _audit/ project.md ; echo "exit=$?"
exit=1

$ git status --porcelain -- _audit/S-007.md | wc -l
0
~~~

  Ninguna salida original fue reescrita: las dos unicas lineas que `decisions.md` pierde en el commit
  son la fila de indice y el campo `Estado` de `D-036`, que revoca `D-045`. **`Implementado`.**

---

### F-023 - `T-026` se escribio a mano sin el `D-XXX` ni el `F-NNN` que la convencion exige, y la desviacion no llego a `decisions.md`
| Campo | Valor |
|---|---|
| Auditoria | R-008 |
| Fecha | 2026-09-02 |
| Gravedad | Baja |
| Estado | Implementado |
| Registrado en | `T-030` |
| Cerrado en | `fc91957` |

- **Que se observo:** el informe lo somete a auditoria en su seccion 6 y la ficha lo declara sin
  disimulo. La convencion de `tasks.md` dice, literal:

```
$ git show f096fff:_persistence/tasks.md | sed -n '/^## Convenciones/,/^## Tareas/p' | grep -n "exigen lo mismo" -A 3
46:⚠️ **Son dos excepciones, no una puerta.** Las dos exigen lo mismo: **un `D-XXX` o un `F-NNN` que
47-las respalde, citado en la propia tarea**. Sin esa cita, cualquier edicion a mano se vuelve
48-indistinguible de saltarse la regla — y entonces la regla deja de existir. Lo demas sigue siendo del
49-`session-closer`.
```

Y ninguna decision de esta sesion la cubre:

```
$ git show f096fff:_persistence/decisions.md | grep -n "T-026" ; echo "exit=$?"
exit=1
```

- **Por que importa:** declararlo es lo correcto y hay que decirlo — un incumplimiento escrito se
  audita y uno deshecho no. Pero la desviacion se quedo en prosa dentro de la propia tarea que la
  comete: `decisions.md`, que es donde `CLAUDE.md` manda el porque de lo que se elige entre
  alternativas, no la registra; y la convencion de `tasks.md` sigue diciendo «dos excepciones» sin
  nada al lado que recoja el caso. Es el mismo hueco que `F-007` abrio con `D-020`. `Baja` porque no
  cambia nada del contenido del repositorio y porque el propio auditado lo puso encima de la mesa.
- **Que lo corregiria:** una de dos, y la eleccion es de `manager`: registrar una `D-XXX` que asuma
  la desviacion como caso puntual, con su clasificacion de reversibilidad declarada, y citarla en la
  ficha; o, si el patron se considera legitimo, abrirlo como tercera excepcion con su `D-XXX` **en la
  convencion**, que es donde lo lee quien ejecuta.
- **Que se hizo:** **aceptado** el 2026-09-02 (`S-009`). Verificado contra `HEAD` (`7025a05`) antes
  de evaluarlo: `grep -n "T-026" _persistence/decisions.md` sigue devolviendo `exit=1`, es decir que
  ninguna decision cubre la desviacion. Se abre `T-030`, que la registra en `D-044` como **caso
  puntual** y la cita en la ficha de `T-026`. De las dos salidas que el hallazgo ofrece se toma la
  primera: **no se abre una tercera excepcion** en la convencion de `tasks.md`, porque las dos que
  existen cubren lo que el `session-closer` no puede deducir del `git diff` y esta si se deducia. El
  texto original de `T-026` no se toca. **`Aceptado — pendiente`**.

- **Verificado por `R-009`** sobre `fc91957`: corregido. `D-044` existe, `T-026` la cita, y la
  convencion de `tasks.md` no gano una tercera excepcion.

~~~
$ git show fc91957:_persistence/decisions.md | grep -n "^### D-044"
1918:### D-044 - La ficha `T-026` escrita a mano se asume como caso puntual, no como tercera excepcion

$ git show fc91957:_persistence/tasks.md | sed -n '/^### T-026/,/^### T-027/p' | grep -c "D-044"
2

$ git show fc91957:_persistence/tasks.md | sed -n '/^## Convenciones/,/^## Tareas/p' | grep -c "Son dos excepciones, no una puerta"
1
~~~

  **`Implementado`.**

---

### F-024 - `F-021` se declara `Implementado` y la correccion no esta en el diff
| Campo | Valor |
|---|---|
| Auditoria | R-009 |
| Fecha | 2026-09-02 |
| Gravedad | Alta |
| Estado | Implementado |
| Registrado en | `T-032` |
| Cerrado en | `51354ef` |

- **Que se observo:** la seccion 0 de `_audit/S-009.md` declara `F-021` como `Implementado`, y
  `T-028` (`Implementada`) dice haber corregido la celda «Avance de la etapa» de `progress.md` «con
  nota fechada». El diff del commit no muestra ninguna correccion: la cadena señalada desaparecio
  porque la celda se **sobrescribio entera** con el contenido de `S-009`, como hace cada cierre.

~~~
$ git show fc91957:_persistence/progress.md | grep -o 'R-007` (sobre `[0-9a-f]*`)' ; echo "exit=$?"
exit=1

$ git show f096fff:_persistence/progress.md | grep -o 'R-007` (sobre `[0-9a-f]*`)'
R-007` (sobre `ae06147`)

$ git show fc91957 -- _persistence/progress.md | grep -c "^[+-].*ae06147"
0
~~~

  El bloque de verificacion de `T-028` registra `R-007` (sobre `122b770`)` para
  `grep -o ... _persistence/progress.md`, salida del arbol intermedio; sobre el commit que la
  contiene esa misma orden devuelve `exit=1`. Y su criterio de cierre —«la celda atribuye a `R-007`
  el commit `122b770`, y la nota fechada explica que se corrigio»— no se cumple sobre `fc91957`.
  Tres registros distintos afirman esa nota inexistente: la celda de `progress.md` («`T-028` corrige
  en esta misma celda … dejando nota fechada»), la seccion 2 del mismo archivo, y la vineta «Que se
  hizo» de `F-021` en este archivo.
- **Por que importa:** la nota fechada es el mecanismo con el que este proyecto distingue «se
  corrigio» de «se reescribio la historia» (`D-019`, `CLAUDE.md`); quien la busque no la encuentra.
  `T-028` queda `Implementada` con un criterio de cierre que su propio commit incumple —el patron de
  `F-016`— y con un bloque de verificacion no reproducible. `Alta` porque el registro afirma un
  hecho documentado que no ocurrio, que es exactamente lo que la auditoria existe para impedir. Por
  la regla del protocolo, `F-021` sigue abierto.
- **Que lo corregiria:** dejar constancia de que `F-021` se resolvio **por desaparicion** del texto
  al sobrescribirse la celda, no por correccion; o, si se quiere la correccion de verdad, escribirla
  donde el texto sobrevive —la bitacora de `S-008`, que sigue en el archivo—. En ambos casos,
  ajustar la redaccion de la celda de `progress.md`, de la seccion 2 y de la vineta de `F-021`, y
  revisar el estado y el bloque de verificacion de `T-028`.
- **Que se hizo:** **aceptado** el 2026-09-02 (`S-010`). Verificado contra `HEAD` (`99c3aa3`)
  antes de evaluarlo: la cadena que `F-021` señalaba no existe en ninguna parte de `progress.md`,
  luego la segunda salida que este hallazgo proponia —corregirla donde el texto siga vivo— no
  tiene objeto.

~~~
$ git show 99c3aa3:_persistence/progress.md | grep -o 'R-007` (sobre `[0-9a-f]*`)' ; echo "exit=$?"
exit=1
~~~

  ⚠️ **Una precision sobre la evidencia del propio hallazgo:** su segunda orden —`grep -c "^[+-].*ae06147"`
  sobre el diff de `fc91957`, registrada en `0`— **no se reproduce: devuelve `6`.**

~~~
$ git show fc91957 -- _persistence/progress.md | grep -c "^[+-].*ae06147"
6
~~~

  El fondo se sostiene igual, y con mas claridad: dos de esas seis lineas son el par `-`/`+` de la
  celda «Avance de la etapa» completa —sale entera y entra otra—, que es exactamente la
  sobrescritura que el hallazgo describe. Se abre `T-032`, y `D-050` fija el tratamiento: `F-021`
  resuelto **por desaparicion** y no por correccion, las dos secciones de `progress.md` que el
  cierre sobrescribe ajustadas en su sitio (`D-027`), nota fechada al lado de lo historico, y
  `T-028` a `Cancelada`. **`Aceptado — pendiente`**.


- **Cerrado por `R-010`** sobre `51354ef`: la nota fechada existe en los tres registros que
  afirmaban la nota inexistente, `T-028` figura `Cancelada` en el indice y en su ficha, y nacen
  `D-050` y `L-015`.

~~~
$ for f in _persistence/progress.md _audit/findings.md _persistence/tasks.md; do
    echo -n "$f:"; git show 51354ef:$f | grep -c 'Nota del 2026-09-02 (`T-032`, hallazgo `F-024`)'
  done
_persistence/progress.md:1
_audit/findings.md:1
_persistence/tasks.md:2

$ git show 51354ef:_persistence/tasks.md | grep -n "^| \[T-028\]" | grep -c "Cancelada"
1

$ git show 51354ef:_persistence/decisions.md | grep -c "^### D-050"
1

$ git show 51354ef:_persistence/lessons.md | grep -c "^### L-015"
1
~~~

  ⚠️ **El bloque de verificacion de `T-032` no se reproduce** —el `2` de arriba donde la ficha
  registra `1`, y cinco lineas donde registra tres—. Eso no impide cerrar este hallazgo, cuya
  correccion si esta en el diff, pero se abre **`F-027`** por la evidencia. **`Implementado`.**

---

### F-025 - Los bloques de verificacion de `D-043` y `D-044` usan `HEAD` sin anclar y no se reproducen
| Campo | Valor |
|---|---|
| Auditoria | R-009 |
| Fecha | 2026-09-02 |
| Gravedad | Media |
| Estado | Implementado |
| Registrado en | `T-033` |
| Cerrado en | `51354ef` |

- **Que se observo:** el propio informe lo somete a auditoria en su seccion 6, y se confirma.
  `D-043` registra `16` donde el commit da `23`, y su `git log -1` registra el commit anterior:

~~~
$ git show fc91957:_persistence/decisions.md | grep -c "^| Fecha | 2026-09-02 |"
23

$ git log -1 --format="%h %ad" --date=short fc91957
fc91957 2026-09-01
~~~

  `D-044` registra `exit=1` para su primera orden —«ninguna decision menciona `T-026`»— y sobre el
  commit devuelve ocho coincidencias; la segunda si se reproduce:

~~~
$ git show fc91957:_persistence/decisions.md | grep -c "T-026"
8

$ git show fc91957:_persistence/tasks.md | grep -c "NO encaja en ninguna de las dos excepciones"
1
~~~

- **Por que importa:** es el cuarto commit consecutivo con el mismo defecto (`F-005`, `F-008`,
  `F-011`, `F-022`), y esta vez ocurre en el mismo commit que estrena `L-013`, la leccion que lo
  nombra. Una verificacion que no se reproduce sobre su propio commit obliga a rehacer el barrido
  entero para saber si el fondo era cierto; aqui lo era en los dos casos, pero eso solo se sabe
  despues de rehacerlo, y entonces la evidencia que vale es la del auditor y no la del registro.
  `Media` y no `Alta` porque el fondo de las dos decisiones se sostiene.
- **Que lo corregiria:** el mismo patron que `T-029` acaba de aplicar a `D-036`, `D-038` y `D-040`:
  nota fechada al lado, sin reescribir el texto original, con la orden anclada a `fc91957` —o a
  `7025a05` para lo que se afirmaba del estado previo— y su salida cruda. Y, hacia adelante, que
  `L-013` deje de ser solo una leccion escrita: como leccion ya fallo en el commit que la estreno.
- **Que se hizo:** **aceptado** el 2026-09-02 (`S-010`). Verificado contra `HEAD` (`99c3aa3`)
  antes de evaluarlo: el recuento que `D-043` registra en `16` sigue dando `23`.

~~~
$ git show 99c3aa3:_persistence/decisions.md | grep -c "^| Fecha | 2026-09-02 |"
23
~~~

  Se abre `T-033`, que aplica a `D-043` y `D-044` el mismo patron que `T-029` aplico a `D-036`,
  `D-038` y `D-040`: nota fechada al lado, orden anclada a un commit concreto y su salida cruda,
  sin tocar el texto original. **`Aceptado — pendiente`**.


- **Cerrado por `R-010`** sobre `51354ef`: `D-043` y `D-044` llevan cada uno su nota fechada, y las
  ordenes ancladas que las acompanan se reproducen.

~~~
$ git show 51354ef:_persistence/decisions.md | grep -c 'Nota del 2026-09-02 (`T-033`, hallazgo `F-025`)'
2

$ git show 7025a05:_persistence/decisions.md | grep -c "^| Fecha | 2026-09-02 |"
16

$ git show fc91957:_persistence/decisions.md | grep -c "^| Fecha | 2026-09-02 |"
23

$ git show 7025a05:_persistence/decisions.md | grep -c "T-026"
0

$ git show fc91957:_persistence/decisions.md | grep -c "T-026"
8
~~~

  **`Implementado`.**

---

### F-026 - `DT-002` cita `L-013` donde corresponde `L-014`
| Campo | Valor |
|---|---|
| Auditoria | R-009 |
| Fecha | 2026-09-02 |
| Gravedad | Baja |
| Estado | Implementado |
| Registrado en | `T-034` |
| Cerrado en | `51354ef` |

- **Que se observo:** el titulo, la fila del indice y el cierre de `DT-002` citan `L-014`; el cuerpo
  cita `L-013`, que trata de otra cosa.

~~~
$ git show fc91957:_persistence/techdebt.md | grep -n "L-013\|L-014"
14:| [DT-002](#dt-002---_workflow-nace-sin-ningun-enganche-de-uso-l-014) | `_workflow/` nace sin ningun enganche de uso (`L-014`) | No implementada | Propuesta (pendiente del usuario) | Media | No bloqueante |
135:### DT-002 - `_workflow/` nace sin ningun enganche de uso (`L-014`)
149:  registrado `L-013` de `lessons.md`.
162:📌 **Propuesta del cierre `S-009`**, a partir de `L-014`. `manager` no la escribe como deuda

$ git show fc91957:_persistence/lessons.md | grep -n "^### L-013\|^### L-014"
390:### L-013 - Un bloque de verificacion sin ancla caduca; el codigo de salida no prueba una ausencia
431:### L-014 - Una carpeta agnostica nueva necesita cuatro enganches, y el cuarto es el que se olvida
~~~

- **Por que importa:** quien siga la cita del cuerpo llega a la leccion equivocada, no a la que
  sostiene la deuda. `Baja` porque las otras tres menciones son correctas y el error se ve al abrir
  la leccion.
- **Que lo corregiria:** sustituir `L-013` por `L-014` en la linea 149 de `_persistence/techdebt.md`.
- **Que se hizo:** **aceptado** el 2026-09-02 (`S-010`). Verificado contra `HEAD` (`99c3aa3`)
  antes de evaluarlo: la cita equivocada sigue viva en el cuerpo de `DT-002`.

~~~
$ git show 99c3aa3:_persistence/techdebt.md | grep -n "L-013"
149:  registrado `L-013` de `lessons.md`.
~~~

  Se abre `T-034`. **`Aceptado — pendiente`**.

- **Cerrado por `R-010`** sobre `51354ef`: el cuerpo de `DT-002` cita `L-014`. Las dos ocurrencias
  de `L-013` que quedan en el archivo estan **dentro de la nota** que documenta el cambio, no en el
  cuerpo de la deuda.

~~~
$ git show 51354ef:_persistence/techdebt.md | grep -n 'registrado `L-01[34]` de'
149:  registrado `L-014` de `lessons.md`.
176:149:  registrado `L-014` de `lessons.md`.

$ git show 51354ef:_persistence/techdebt.md | grep -n 'L-013'
167:`L-013` donde corresponde `L-014`.** Se corrige la cita, que es una remision cruzada dentro del
173:149:  registrado `L-013` de `lessons.md`.
~~~

  **`Implementado`.**


---

### F-027 - El bloque de verificacion de `T-032` no se reproduce sobre su propio commit, y su lectura en prosa queda desmentida
| Campo | Valor |
|---|---|
| Auditoria | R-010 |
| Fecha | 2026-09-02 |
| Gravedad | Media |
| Estado | Implementado |
| Registrado en | `T-035` |
| Cerrado en | `R-011` (`2a2d3b6`) |

- **Que se observo:** dos de las tres ordenes del bloque «Verificacion» de `T-032` devuelven sobre
  `51354ef` algo distinto de lo registrado. La primera registra tres lineas (`387`, `417`, `451`);
  el commit da cinco:

~~~
$ git show 51354ef:_persistence/progress.md | grep -n "dejando nota fechada\|con nota fechada" | cut -d: -f1
64
385
415
449
472
~~~

  La tercera registra `1` para `_persistence/tasks.md`; el commit da `2`, porque el propio bloque
  contiene la cadena que busca:

~~~
$ for f in _persistence/progress.md _audit/findings.md _persistence/tasks.md; do
    echo -n "$f:"; git show 51354ef:$f | grep -c 'Nota del 2026-09-02 (`T-032`, hallazgo `F-024`)'
  done
_persistence/progress.md:1
_audit/findings.md:1
_persistence/tasks.md:2
~~~

  Y el parrafo que interpreta la salida —«Ninguna de las **tres** lineas que quedan con "nota
  fechada" es una afirmacion viva […] Las secciones 1 y 2, que son las vivas, ya no lo afirman»—
  queda desmentido: la linea `64` es la celda «Avance de la etapa» de la seccion 1, viva, y contiene
  la cadena:

~~~
$ git show 51354ef:_persistence/progress.md | sed -n '64p' | grep -o 'ancla con nota fechada'
ancla con nota fechada
~~~

- **Por que importa:** es el quinto commit consecutivo con el mismo defecto (`F-005`, `F-008`,
  `F-011`, `F-022`, `F-025`), y ocurre **en el mismo commit que estrena `L-015`**, la leccion que
  describe exactamente este mecanismo. El auditor tiene que rehacer el barrido, y entonces la
  evidencia que vale es la suya y no la del registro. `Media` y no `Alta` porque el fondo de `T-032`
  se sostiene: sobre `51354ef` las dos menciones vivas de `ae06147` en `progress.md` son la bitacora
  de `S-008` (correcta) y la de `S-009` (historica, con nota fechada al lado en la linea 435), y
  ninguna afirmacion viva declara una nota inexistente. Falla la evidencia, no la correccion.
- **Que lo corregiria:** nota fechada al lado del bloque de `T-032`, sin reescribir el texto
  original (`D-019`), con las dos ordenes ancladas a `51354ef`, su salida real y la lectura rehecha
  sobre esas cinco lineas. Hacia adelante, `L-013` y `L-015` ya nombran el problema: lo que falta es
  un mecanismo que impida publicar un bloque sin ancla, no una tercera leccion que lo describa.
- **Que se hizo:** **aceptado** el 2026-09-02 (`S-011`), registrado en `T-035`. Verificado contra
  `HEAD` (`cbb92a9`) antes de evaluarlo: las dos ordenes siguen sin reproducirse y la linea `64`,
  que esta viva, si contiene la cadena.

~~~
$ git show HEAD:_persistence/progress.md | grep -n "dejando nota fechada\|con nota fechada" | cut -d: -f1
64
385
415
449
472

$ git show HEAD:_persistence/progress.md | sed -n '64p' | grep -o 'ancla con nota fechada'
ancla con nota fechada
~~~

- **Que verifico la auditoria (`R-011`, sobre `2a2d3b6`):** la nota existe en la ficha de `T-032`,
  y sus ordenes ancladas a `51354ef` se reproducen.

~~~
$ git show 2a2d3b6:_persistence/tasks.md | awk '/^### T-032 /,/^### T-033 /' | grep -c 'Nota del 2026-09-02 (`T-035`, hallazgo `F-027`)'
1

$ git show 51354ef:_persistence/progress.md | grep -n "dejando nota fechada\|con nota fechada" | cut -d: -f1
64
385
415
449
472

$ git show 51354ef:_persistence/progress.md | grep -c "ae06147"
7

$ git show 51354ef:_persistence/tasks.md | grep -n "^| \[T-028\]" | grep -c "Cancelada"
1
~~~

  **`Implementado`.**

---

### F-028 - La lista de la seccion 1 del informe omite dos ediciones de `decisions.md`
| Campo | Valor |
|---|---|
| Auditoria | R-010 |
| Fecha | 2026-09-02 |
| Gravedad | Baja |
| Estado | Implementado |
| Registrado en | `T-036` |
| Cerrado en | `R-011` (`2a2d3b6`) |

- **Que se observo:** la vineta de `_persistence/decisions.md` en la seccion 1 de `_audit/S-010.md`
  dice «nacen `D-050`, `D-051` y `D-052`» y nada mas. El diff muestra ademas dos notas fechadas
  nuevas insertadas dentro de `D-043` y `D-044`, que son el trabajo entero de `T-033`:

~~~
$ git show 51354ef -- _persistence/decisions.md | grep -n "^+.*Nota del 2026-09-02 (\`T-033\`"
39:+📌 **Nota del 2026-09-02 (`T-033`, hallazgo `F-025`): las dos ultimas ordenes de este bloque
68:+📌 **Nota del 2026-09-02 (`T-033`, hallazgo `F-025`): la primera orden de este bloque se
~~~

- **Por que importa:** la seccion 1 es la lista canonica de que cambio en el commit, y `T-025`
  (`F-019`) endurecio precisamente ese punto de `protocol-close`. Describir el archivo como «nacen
  tres decisiones» oculta que dentro de el se editaron dos entradas anteriores, que es el tipo de
  edicion sobre texto ya auditado que mas interesa ver. `Baja` porque el cambio si esta descrito en
  otro sitio del registro —la ficha de `T-033`— y no contradice nada.
- **Que lo corregiria:** ampliar esa vineta, o dejar nota fechada si se prefiere no reescribir un
  informe ya commiteado, para que mencione las dos notas de `T-033` en `D-043` y `D-044`.
- **Que se hizo:** **aceptado** el 2026-09-02 (`S-011`), registrado en `T-036`. Verificado contra
  `HEAD` (`cbb92a9`) antes de evaluarlo: la viñeta de `decisions.md` de `_audit/S-010.md` sigue sin
  mencionar `T-033`.

~~~
$ git show HEAD:_audit/S-010.md | sed -n '58,64p' | grep -c "T-033"
0
~~~

- **Que verifico la auditoria (`R-011`, sobre `2a2d3b6`):** la nota fechada existe en
  `_audit/S-010.md`, bajo la vineta de `decisions.md` y sin reescribir el texto original (`D-019`),
  y su orden anclada a `51354ef` se reproduce.

~~~
$ git show 2a2d3b6:_audit/S-010.md | grep -c 'Nota del 2026-09-02 (`T-036`, hallazgo `F-028`)'
1

$ git show 51354ef -- _persistence/decisions.md | grep -c "^+📌 \*\*Nota del 2026-09-02 (\`T-033\`"
2
~~~

  **`Implementado`.**

---

### F-029 - `T-037` y `T-038` llevan el estado `Pendiente`, que la convencion de `tasks.md` no declara
| Campo | Valor |
|---|---|
| Auditoria | R-011 |
| Fecha | 2026-09-02 |
| Gravedad | Media |
| Estado | Implementado |
| Registrado en | `T-039` |
| Cerrado en | `7f55389` (R-012) |

- **Que se observo:** la convencion de `_persistence/tasks.md` declara cuatro valores de `Estado`
  (`Implementada` / `No implementada` / `Cancelada` / `Suspendida`). Las dos fichas nuevas de
  `S-011` usan un quinto, en la ficha y en el indice:

~~~
$ git show 2a2d3b6:_persistence/tasks.md | grep -nE '^\| Estado \| ' | grep -vE 'Implementada|No implementada|Cancelada|Suspendida'
1598:| Estado | Pendiente |
1651:| Estado | Pendiente |

$ git show 2a2d3b6:_persistence/tasks.md | sed -n '/^## Indice/,/^---/p' | grep -c "| Pendiente |"
2
~~~

- **Por que importa:** el propio archivo dice que anadir un valor nuevo «es una decision, no una
  improvisacion» y exige su `D-XXX` en la misma pasada en que se escribe la primera tarea que lo
  usa. Hoy hay dos tareas cuyo estado no significa nada declarado: un barrido que filtre por los
  cuatro valores validos las deja fuera —la seccion 2 del informe tuvo que anadir `Pendiente` a mano
  a su `grep`—, y el trabajo abierto de la etapa deja de poder contarse con un solo criterio.
- **Que lo corregiria:** o normalizar las dos fichas a `No implementada`, o declarar `Pendiente` en
  la tabla de convenciones con su `D-XXX`, explicando en que se distingue de `No implementada`.
- **Que se hizo:** **aceptado** el 2026-09-02 (`S-012`), registrado en `T-039`. Verificado contra
  `HEAD` (`f1f3fea`) antes de evaluarlo: los dos valores siguen fuera de la convencion. De las dos
  salidas que el hallazgo ofrecia se toma la primera —normalizar a `No implementada`—, con su
  `D-057`: `Pendiente` y `No implementada` no distinguen nada, y un quinto valor obligaria a todo
  barrido futuro a filtrar por cinco donde cuatro bastan.

~~~
$ git grep -nE '^\| Estado \| ' f1f3fea -- _persistence/tasks.md | grep -vE 'Implementada|No implementada|Cancelada|Suspendida'
f1f3fea:_persistence/tasks.md:1598:| Estado | Pendiente |
f1f3fea:_persistence/tasks.md:1651:| Estado | Pendiente |

$ git show f1f3fea:_persistence/tasks.md | sed -n '/^## Indice/,/^---/p' | grep -c "| Pendiente |"
2
~~~

- **Que verifico la auditoria (`R-012`, sobre `7f55389`):** ningun campo `Estado` de
  `_persistence/tasks.md` cae fuera de los cuatro valores declarados, y el indice no tiene ninguna
  fila `Pendiente`. `D-057` registra por que no nace un quinto estado.

~~~
$ git show 7f55389:_persistence/tasks.md | grep -E '^\| Estado \| ' | grep -vE 'Implementada|No implementada|Cancelada|Suspendida' ; echo "rc=$?"
rc=1

$ git show 7f55389:_persistence/tasks.md | sed -n '/^## Indice/,/^---/p' | grep -c "| Pendiente |"
0
~~~

  **`Implementado`.**

---

### F-030 - `T-038` se escribio a mano sin citar el `D-XXX` o `F-NNN` que la habilita
| Campo | Valor |
|---|---|
| Auditoria | R-011 |
| Fecha | 2026-09-02 |
| Gravedad | Baja |
| Estado | Implementado |
| Registrado en | `T-040` |
| Cerrado en | `7f55389` (R-012) |

- **Que se observo:** las dos excepciones que permiten escribir `tasks.md` fuera del cierre exigen
  «un `D-XXX` o un `F-NNN` que las respalde, citado en la propia tarea». La ficha de `T-038` no cita
  ninguno de los dos; `T-037`, escrita en la misma pasada, si:

~~~
$ git show 2a2d3b6:_persistence/tasks.md | awk '/^### T-038 /,0' | grep -oE '`(D|F)-[0-9]+`' | sort -u
(sin salida)

$ git show 2a2d3b6:_persistence/tasks.md | awk '/^### T-037 /,/^### T-038 /' | grep -oE '`D-[0-9]+`' | sort -u
`D-054`
~~~

- **Por que importa:** la convencion lo dice con todas las letras — sin esa cita, una edicion a mano
  se vuelve indistinguible de saltarse la regla, y entonces la regla deja de existir. `Baja` porque
  el contenido de la tarea es correcto y su origen se adivina; lo que falta es el enganche que la
  hace auditable.
- **Que lo corregiria:** citar en `T-038` el registro que la respalda —`D-054` si nacio de la misma
  consulta, o un `D-XXX` nuevo—, o dejar escrito por que no entra por ninguna de las dos
  excepciones.
- **Que se hizo:** **aceptado** el 2026-09-02 (`S-012`), registrado en `T-040`. Verificado contra
  `HEAD` (`f1f3fea`) antes de evaluarlo: `T-038` sigue sin citar ninguno de los dos prefijos. La
  correccion no le inventa una excepcion: `D-058` declara que la tarea **nacio fuera de las dos**
  —de una observacion propia al leer `R-010`— y hace de respaldo, y `T-038` lo cita en nota fechada.

~~~
$ git show f1f3fea:_persistence/tasks.md | awk '/^### T-038 /,0' | grep -oE '`(D|F)-[0-9]+`' | sort -u
(sin salida)
~~~

- **Que verifico la auditoria (`R-012`, sobre `7f55389`):** `T-038` cita ahora `D-058`, el respaldo
  que `D-058` declara. Sobre `f1f3fea` el mismo patron devolvia vacio.

~~~
$ git show 7f55389:_persistence/tasks.md | awk '/^### T-038 /,/^### T-039 /' | grep -oE '`(D|F)-[0-9]+`' | sort -u
`D-057`
`D-058`
`F-029`
`F-030`
~~~

  **`Implementado`.**

---

### F-031 - El recuento «quince lecciones Sin evaluar» no se reproduce sobre su propio commit, y esta en cuatro sitios
| Campo | Valor |
|---|---|
| Auditoria | R-011 |
| Fecha | 2026-09-02 |
| Gravedad | Media |
| Estado | Implementado |
| Registrado en | `T-041`, `T-042` |
| Cerrado en | `7f55389` (R-012) |

- **Que se observo:** el bloque de verificacion de `D-056` registra `15` y su prosa afirma «hoy sus
  quince lecciones estan las quince `Sin evaluar`». Sobre el commit que las publica son `17`: la
  propia sesion anadio `L-016` y `L-017` despues de correr el barrido. La cifra vieja aparece en
  cuatro sitios, dos de ellos vivos:

~~~
$ git show 2a2d3b6:_persistence/lessons.md | sed -n '/^## Indice/,/^---/p' | grep -c "| Sin evaluar |$"
17

$ git show 2a2d3b6:_persistence/decisions.md | grep -n "quince lecciones\|las quince"
2725:  de cerrar**, y hoy sus quince lecciones estan las quince `Sin evaluar`. La etapa no puede cerrar
2738:las quince lecciones tienen la columna:**

$ git show 2a2d3b6:_persistence/progress.md | grep -n "quince lecciones"
101:memoria; `000_preproject` gana esa casilla estando cerca de cerrar, con sus quince lecciones hoy
554:  quince lecciones `Sin evaluar`.

$ git show 2a2d3b6:_audit/S-011.md | grep -n "quince"
88:  hecha», esta ultima con sus quince lecciones de la etapa hoy `Sin evaluar`.
~~~

- **Por que importa:** es el sexto commit consecutivo con el mismo defecto (`F-005`, `F-008`,
  `F-011`, `F-022`, `F-025`, `F-027`), y esta vez el numero equivocado esta ademas en la celda viva
  «Avance de la etapa» de `progress.md`, que es lo primero que lee el arranque siguiente. La cifra
  no es decorativa: es el volumen de trabajo que bloquea la condicion de salida de `000_preproject`
  que la propia `D-056` acaba de crear. El informe declara en su seccion 6 el caso de `D-056`; los
  otros tres sitios no.
- **Que lo corregiria:** nota fechada al lado —sin reescribir (`D-019`)— en `D-056` y en la celda
  viva de `progress.md`, con el barrido anclado a `2a2d3b6` y la lectura rehecha sobre `17`. Y, para
  que no haya un septimo, un mecanismo en el cierre que impida publicar un bloque de verificacion
  sin ancla: `L-013` y `L-015` ya describen el defecto, lo que falta es quien lo aplique.
- **Que se hizo:** **aceptado** el 2026-09-02 (`S-012`), en dos tareas. `T-041` pone la nota
  fechada en los cuatro sitios que el hallazgo enumera, con el recuento anclado a `2a2d3b6`. `T-042`
  atiende la segunda mitad de la recomendacion —la que evita el septimo caso—: `protocol-close` gana
  un **Paso 2d** que localiza los bloques publicados sin ancla y obliga a reejecutarlos antes de
  cerrar. Verificado contra `HEAD` (`f1f3fea`) antes de evaluarlo: el recuento sigue siendo `17`.

~~~
$ git show f1f3fea:_persistence/lessons.md | sed -n '/^## Indice/,/^---/p' | grep -c "| Sin evaluar |$"
17
~~~

- **Que verifico la auditoria (`R-012`, sobre `7f55389`):** las menciones vivas de «quince» llevan su
  nota fechada con el recuento anclado a `2a2d3b6`, la celda «Avance de la etapa» dejo de contener la
  cifra al reescribirse la seccion, y la segunda mitad del hallazgo —el mecanismo— existe: Paso 2d de
  `protocol-close`.

~~~
$ git show 7f55389:_persistence/progress.md | sed -n '66p' | grep -c quince
0

$ git show 7f55389:.claude/skills/protocol-close/SKILL.md | grep -n "^## Paso 2d"
242:## Paso 2d — Ningun bloque de verificacion sin ancla (antes del `git add`)
~~~

  **`Implementado`.** ⚠️ El **bloque de evidencia** de `T-041` no se reproduce sobre este commit
  —publica `_persistence/progress.md:2` donde hay `1`—; eso no reabre este hallazgo: va como
  hallazgo nuevo con evidencia nueva, `F-032`.
---

### F-032 - El bloque de T-041 publica un recuento que su commit no sostiene, y su prosa afirma cuatro notas donde hay tres
| Campo | Valor |
|---|---|
| Auditoria | R-012 |
| Fecha | 2026-09-02 |
| Gravedad | Media |
| Estado | Implementado |
| Registrado en | `T-045`, `T-046` |
| Cerrado en | `R-013` (`8eb8666`) |

- **Que se observo:** `T-041` publica `_persistence/progress.md:2` como prueba de que las cuatro
  notas fechadas quedaron puestas. Sobre el commit que la contiene son `1`, y el total es `3`, no
  `4`: la nota de la **seccion viva** de `progress.md` se escribio y desaparecio al sobrescribir el
  cierre esa seccion — `L-015` literal.

Lo que `T-041` publica en su bloque:

~~~
$ grep -c 'Nota del 2026-09-02 (`T-041`, hallazgo `F-031`)' _persistence/decisions.md _persistence/progress.md _audit/S-011.md
_persistence/decisions.md:1
_persistence/progress.md:2
_audit/S-011.md:1
~~~

Lo que la misma orden devuelve sobre el commit que la contiene:

~~~
$ git show 7f55389:_persistence/progress.md | grep -c 'Nota del 2026-09-02 (`T-041`, hallazgo `F-031`)'
1

$ git show 7f55389:_persistence/progress.md | grep -n 'Nota del 2026-09-02'
453:📌 **Nota del 2026-09-02 (`T-032`, hallazgo `F-024`): la nota fechada que esta bitacora da por
552:📌 **Nota del 2026-09-02 (`T-041`, hallazgo `F-031`).** La bitacora se deja tal cual (`D-019`).
~~~

  La misma afirmacion esta en otros dos sitios: `progress.md` §2 —«en los cuatro sitios que el
  hallazgo enumera: `D-056`, las dos menciones de este archivo (seccion viva y bitacora de `S-011`) y
  `_audit/S-011.md`»— y `_audit/S-012.md` §0. El criterio de cierre de la propia ficha dice «los
  cuatro sitios llevan su nota fechada», y sobre el commit no se cumple.

- **Por que importa:** es la **octava** repeticion del mismo defecto (`F-005`, `F-008`, `F-011`,
  `F-022`, `F-025`, `F-027`, `F-031`) y ocurre en la sesion que creo el Paso 2d para impedirlo, sobre
  la tarea que corregia el septimo caso. El Paso 2d lo habria atrapado: su primera orden devuelve
  esta linea y al reejecutarla da `1` donde el bloque publica `2`. El paso se corrio —asi lo dice
  `T-042`—, pero su evidencia pega **cinco** lineas cuando la misma orden sobre el commit devuelve
  `26`.
- **Gravedad `Media`:** el efecto de fondo de `F-031` si esta corregido —ninguna cifra «quince» queda
  viva sin su nota— y ninguna decision cambia; lo que falla es que el registro afirma un estado que
  su commit no sostiene, que es justo el defecto que `F-031` señalaba.
- **Que lo corregiria:** nota fechada al lado del bloque de `T-041` —sin reescribirlo (`D-019`)— con
  el recuento real anclado a `7f55389` y la razon de que la cuarta nota se perdiera; y, si se quiere
  cerrar el patron, que el Paso 2d exija pegar **la lista completa** de su primera orden, no una
  seleccion de ella.
- **Que se hizo:** **aceptado**, verificado contra `HEAD` (`265bfeb`) antes de tratarlo: el bloque
  de `T-041` sigue publicando `_persistence/progress.md:2` donde la orden devuelve `1`. Se corrige en
  dos piezas: `T-045` pone la nota fechada con el recuento real anclado a `7f55389` y a `265bfeb`
  —sin reescribir el bloque (`D-019`)—, y `T-046` acepta tambien la segunda mitad de la
  recomendacion: el Paso 2d de `protocol-close` pasa a exigir **la lista completa** de su primera
  orden, no una seleccion (`D-063`, `L-019`). Al verificarlo aparecio ademas que esa orden **no
  devuelve el mismo numero en todos los entornos** —`26` en la auditoria, `28` aqui, sobre el mismo
  commit—, lo que refuerza la correccion en vez de contradecirla.
- **Verificado y cerrado por `R-013` sobre `8eb8666`:** las dos mitades estan en el diff. La nota
  fechada de `T-045` esta al lado del bloque de `T-041`, sin reescribirlo (`D-019`), y su bloque
  anclado reproduce; el parrafo de la lista completa esta en el Paso 2d.

~~~
$ for f in _persistence/decisions.md _persistence/progress.md _audit/S-011.md; do echo -n "$f: "; git show 7f55389:$f | grep -c 'Nota del 2026-09-02 (`T-041`, hallazgo `F-031`)'; done
_persistence/decisions.md: 1
_persistence/progress.md: 1
_audit/S-011.md: 1

$ git show 8eb8666:.claude/skills/protocol-close/SKILL.md | grep -n "la lista COMPLETA"
273:🚨 **Y la evidencia de este paso publica la lista COMPLETA de su primera orden, nunca una

$ git show 8eb8666:_persistence/tasks.md | grep -c 'Nota del 2026-09-02 (`T-045`, hallazgo `F-032`)'
1
~~~

---

### F-033 - La nota de cierre de D-060 afirma que project.md no nombra la etapa nueva, y el mismo commit lo desmiente
| Campo | Valor |
|---|---|
| Auditoria | R-012 |
| Fecha | 2026-09-02 |
| Gravedad | Baja |
| Estado | Implementado |
| Registrado en | `T-047` |
| Cerrado en | `R-013` (`8eb8666`) |

- **Que se observo:** la nota final de `D-060` justifica las dos ordenes que sustituyen a la caida
  diciendo que «si prueban lo que la decision afirma —que `project.md` **no nombra la etapa nueva en
  ningun sitio**, y que la fila de etapas declaradas sigue teniendo dos—». Lo segundo es cierto; lo
  primero es falso sobre el mismo commit, y la nota inmediatamente anterior de la misma entrada ya lo
  reconoce.

~~~
$ git show 7f55389:project.md | grep -c "010_prototype"
3

$ git show 7f55389:project.md | grep -n "010_prototype"
37:| Entregables de `010_prototype` | `010_prototype/` (el codigo descartable, en una subcarpeta suya) |
150:| `010_prototype/` | **Los entregables de la etapa `010_prototype`**: los cinco artefactos de registro en su raiz, y el codigo descartable del prototipo en una subcarpeta suya. Se archiva o se borra al cerrar su Gate — **no se muda a ninguna carpeta de producto** |
170:- **`010_prototype/`** esta **declarada por adelantado y todavia no existe en el arbol**, porque su
~~~

- **Por que importa:** la decision es correcta y no cambia; lo que falla es la frase que la respalda.
  Quien lea `D-060` dentro de un mes leera que `project.md` no menciona `010_prototype`, encontrara
  tres menciones y no sabra si la decision sigue vigente o si alguien la incumplio. Mismo perfil que
  `F-027`: la orden se sostiene, la lectura en prosa no.
- **Gravedad `Baja`:** afecta a una frase de justificacion dentro de una entrada cuya decision, cuyo
  alcance y cuya orden probatoria son correctos.
- **Que lo corregiria:** nota fechada al lado —sin reescribir (`D-019`)— acotando la frase a lo que
  la orden prueba: que la tabla «Etapas» sigue con dos, no que el archivo no nombre la carpeta.
- **Que se hizo:** **aceptado**, verificado contra `HEAD` (`265bfeb`): `project.md` sigue nombrando
  `010_prototype` en tres sitios. `T-047` acota la frase con nota fechada al lado, sin reescribirla
  (`D-019`): lo que la orden prueba es que la tabla «Etapas» sigue teniendo dos, no que el archivo no
  nombre la carpeta. La decision `D-060` no cambia.
- **Verificado y cerrado por `R-013` sobre `8eb8666`:** la nota fechada de `T-047` esta al lado de la
  nota de cierre de `D-060`, acota la frase a lo que la orden prueba y no reescribe nada.

~~~
$ git show 8eb8666:_persistence/decisions.md | grep -c 'Nota del 2026-09-02 (`T-047`, hallazgo `F-033`)'
1

$ git show 265bfeb:project.md | grep -c "010_prototype"
3

$ git show 265bfeb:project.md | grep "| Etapas declaradas |"
| Etapas declaradas | `000_preproject`, `005_discovery` |
~~~

---

### F-034 - El informe remite a una lista completa del Paso 2d que no existe en el commit
| Campo | Valor |
|---|---|
| Auditoria | R-013 |
| Fecha | 2026-09-02 |
| Gravedad | Media |
| Estado | Abierto |
| Registrado en | |
| Cerrado en | |

- **Que se observo:** la seccion 6 de `_audit/S-013.md` afirma que el Paso 2d se aplico a si mismo y
  remite a la verificacion de `T-046` para la evidencia —«las nueve ordenes sin ancla se reejecutaron
  y sus salidas coinciden con lo publicado»—. En esa verificacion **no hay ninguna lista**: hay dos
  ordenes, y la unica que recuenta ordenes sin ancla lo hace sobre `7f55389`, el commit anterior, y
  publica solo la cifra `28`.

~~~
$ git show 8eb8666:_audit/S-013.md | sed -n '133,137p'
- **Que la lista completa que exige `D-063` de verdad se haya publicado en esta misma sesion.** El
  Paso 2d se aplico a si mismo dentro del cierre de `S-013` (ver Paso 2d de este cierre, en la
  seccion de verificacion de `T-046`): las nueve ordenes sin ancla se reejecutaron y sus salidas
  coinciden con lo publicado. Es la primera vez que el parrafo nuevo se pone a prueba con datos
  reales; conviene que una lectura externa confirme que ninguna linea quedo fuera.

$ git show 8eb8666:_persistence/tasks.md | sed -n '/^### T-046/,/^---/p' | grep -E '^\$ '
$ grep -n "la lista COMPLETA" .claude/skills/protocol-close/SKILL.md
$ git show 7f55389 -U0 -- _persistence _audit | grep -E '^\+\$ ' | grep -vE 'git (show|grep|log|diff) [0-9a-f]{7,40}' | wc -l

$ git grep -c "nueve ordenes" 8eb8666 -- _persistence _audit
8eb8666:_audit/S-013.md:1
~~~

- **Por que importa:** `D-063` y `L-019` nacen en esa misma sesion diciendo que un control
  documentado sobre una parte de su propia salida no es el control, y que la evidencia es la lista
  entera con su recuento. El informe afirma haber cumplido esa regla y remite a una evidencia que no
  esta publicada: es «se comprobo», que `CLAUDE.md` prohibe. La cifra tampoco cuadra —`nueve` frente
  a diez ordenes distintas y trece apariciones en el entorno de la auditoria—, y el informe no dice
  sobre que rango ni con que criterio se conto.
- **Gravedad `Media`:** el fondo se sostiene —`R-013` reejecuto las diez ordenes del commit y todas
  reproducen—, pero el registro afirma exhibir una evidencia que no exhibe, y precisamente la del
  control creado ese dia para impedir este defecto.
- **Que lo corregiria:** nota fechada al lado (`D-019`) con la lista completa que el Paso 2d devolvio
  en el cierre de `S-013`, anclada a `8eb8666`, con su rango y el resultado de reejecutar cada linea;
  o, si esa salida solo vivio en pantalla, que la nota lo diga en vez de remitir a `T-046`. Para el
  patron de fondo: `D-063` dice **que** publicar pero no **donde**, y una evidencia sin sitio
  asignado desaparece con la sesion.
- **Que se hizo:** pendiente de la evaluacion de `manager`.
