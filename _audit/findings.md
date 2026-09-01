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
| [F-015](#f-015---005_discovery-sigue-declarada-sin-su-archivo-en-_phases-y-ya-nadie-lo-agenda) | `005_discovery` sigue declarada sin su archivo en `_phases/`, y ya nadie lo agenda | R-006 | Media | Abierto |
| [F-016](#f-016---el-criterio-de-cierre-de-t-015-no-se-cumple-al-ejecutarlo-y-la-tarea-queda-implementada) | El criterio de cierre de `T-015` no se cumple al ejecutarlo, y la tarea queda `Implementada` | R-006 | Baja | Abierto |

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
| Estado | Abierto |
| Registrado en | |
| Cerrado en | |

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
- **Que se hizo:** pendiente de la evaluacion de `manager`.

---

### F-016 - El criterio de cierre de `T-015` no se cumple al ejecutarlo, y la tarea queda `Implementada`
| Campo | Valor |
|---|---|
| Auditoria | R-006 |
| Fecha | 2026-09-02 |
| Gravedad | Baja |
| Estado | Abierto |
| Registrado en | |
| Cerrado en | |

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
- **Que se hizo:** pendiente de la evaluacion de `manager`.
