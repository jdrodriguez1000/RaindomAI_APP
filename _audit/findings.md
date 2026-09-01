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
| [F-001](#f-001---el-bloque-de-verificacion-de-d-016-afirma-mas-de-lo-que-su-comando-comprueba) | El bloque de verificacion de `D-016` afirma mas de lo que su comando comprueba | R-002 | Media | Aceptado — pendiente |
| [F-002](#f-002---quedan-identificadores-auditor-vivos-fuera-del-ambito-del-barrido) | Quedan identificadores `auditor` vivos fuera del ambito del barrido | R-002 | Baja | Aceptado — pendiente |
| [F-003](#f-003---dt-001-se-registro-como-confirmada-contra-el-paso-5-de-protocol-close) | `DT-001` se registro como `Confirmada` contra el Paso 5 de `protocol-close` | R-002 | Media | Aceptado — pendiente |
| [F-004](#f-004---session-closermd-describe-a-report_auditor-en-su-propio-repositorio) | `session-closer.md` describe a `report_auditor` en «su propio repositorio» | R-002 | Media | Aceptado — pendiente |

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
rechazo por coste sin entrada en `debtec.md` es, por si solo, un hallazgo nuevo — y no requiere
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
| Estado | Aceptado — pendiente |
| Registrado en | T-004 |
| Cerrado en | |

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
| Estado | Aceptado — pendiente |
| Registrado en | T-005 |
| Cerrado en | |

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
| Estado | Aceptado — pendiente |
| Registrado en | T-006 |
| Cerrado en | |

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
| Estado | Aceptado — pendiente |
| Registrado en | T-007 |
| Cerrado en | |

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
