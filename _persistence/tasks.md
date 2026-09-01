# tasks.md

> Registro de las tareas **realizadas** y de las tareas **por realizar**.
> Cada tarea tiene codigo `T-XXX`, estado, importancia y urgencia.

---

## Indice

| Codigo | Tarea | Estado | Importancia | Urgencia |
|---|---|---|---|---|
| [T-001](#t-001---definir-alcance-y-objetivo-del-proyecto) | Definir alcance y objetivo del proyecto | No implementada | Alta | Bloqueante |
| [T-002](#t-002---declarar-las-etapas-posteriores-a-000_preproject) | Declarar las etapas posteriores a `000_preproject` | No implementada | Media | No bloqueante |
| [T-003](#t-003---verificar-si-el-historico-de-la-fuente-oficial-es-obtenible-a-003) | Verificar si el historico de la fuente oficial es obtenible (`A-003`) | No implementada | Alta | Bloqueante |
| [T-004](#t-004---acotar-el-enunciado-del-bloque-de-verificacion-de-d-016-f-001) | Acotar el enunciado del bloque de verificacion de `D-016` (`F-001`) | Implementada | Media | No bloqueante |
| [T-005](#t-005---corregir-los-dos-identificadores-auditor-vivos-f-002) | Corregir los dos identificadores `auditor` vivos (`F-002`) | Implementada | Baja | No bloqueante |
| [T-006](#t-006---devolver-dt-001-a-propuesta-pendiente-del-usuario-f-003) | Devolver `DT-001` a `Propuesta (pendiente del usuario)` (`F-003`) | Implementada | Media | No bloqueante |
| [T-007](#t-007---corregir-la-tabla-de-actores-de-session-closermd-f-004) | Corregir la tabla de actores de `session-closer.md` (`F-004`) | Implementada | Media | No bloqueante |

---

## Convenciones

| Campo | Valores posibles |
|---|---|
| Codigo | `T-XXX`, correlativo, no se reutiliza |
| Estado | `Implementada` / `No implementada` / `Cancelada` / `Suspendida` |
| Importancia | `Alta` / `Media` / `Baja` |
| Urgencia | `Bloqueante` / `No bloqueante` |
| Origen | `usuario` / `manager` / `report_auditor` |

**`Origen` es obligatorio y su valor sale de esta lista.** Que significa cada uno:

| Valor | La tarea nace de… |
|---|---|
| `usuario` | una peticion o una decision del usuario |
| `manager` | iniciativa propia al ejecutar |
| `report_auditor` | un hallazgo `F-NNN` de una auditoria |

🚨 **Anadir un valor nuevo es una decision, no una improvisacion.** El criterio es uno solo:
**nombra un origen de demanda que ninguno de los ya existentes cubre**. Un matiz de un origen
existente —«usuario, pero por escrito», «report_auditor, pero de otra pasada»— no es un
valor nuevo: va en el cuerpo de la tarea. Si el criterio se cumple, el valor entra **en esta
tabla en la misma pasada** en que se escribe la primera tarea que lo usa, con su `D-XXX`.

Regla: una tarea con origen `report_auditor` solo pasa a ejecutarse despues de que `manager` evalue la
recomendacion y la considere correcta.

🚨 **Este archivo no se escribe a mano durante la jornada.** Lo produce el cierre de sesion, junto
con `progress.md`.

🚨 **El indice se escribe a mano, sin generador.** Cada fila enlaza por ancla a su tarea.

---

## Tareas

<!--
Plantilla:

### T-XXX - Titulo
| Campo | Valor |
|---|---|
| Estado | No implementada |
| Importancia | |
| Urgencia | |
| Origen | |
| Sesion | S-XXX |

- **Que:** que hay que hacer.
- **Por que:** que problema resuelve.
- **Criterio de cierre:** como se sabe que quedo hecha.
-->

### T-001 - Definir alcance y objetivo del proyecto
| Campo | Valor |
|---|---|
| Estado | No implementada |
| Importancia | Alta |
| Urgencia | Bloqueante |
| Origen | manager |
| Sesion | S-001 |

- **Que:** definir el alcance y el objetivo del proyecto, contrastando `_brief/client_brief.md`
  punto por punto (ver `A-002`), y registrar la decision resultante con su `D-XXX`.
- **Por que:** `project.md` declara que hoy solo esta registrada la etapa `000_preproject`; las
  etapas posteriores y el producto mismo dependen de que exista esa definicion. Un encargo del
  cliente no es una decision del proyecto.
- **Criterio de cierre:** existe un `D-XXX` en `decisions.md` que fija alcance y objetivo, y
  `project.md` deja de decir que las etapas posteriores no estan registradas.

---

### T-002 - Declarar las etapas posteriores a `000_preproject`
| Campo | Valor |
|---|---|
| Estado | No implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Origen | manager |
| Sesion | S-001 |

- **Que:** decidir y registrar en `project.md` (tabla «Etapas») que etapas siguen a
  `000_preproject`, tomando como propuesta de partida —no como decision— la secuencia del brief
  (`_brief/client_brief.md`, §22).
- **Por que:** `project.md` dice explicitamente que esto no esta decidido y que un encargo no
  sustituye a una decision registrada.
- **Criterio de cierre:** la tabla «Etapas» de `project.md` lista mas de una etapa, con su `D-XXX`.

---

### T-003 - Verificar si el historico de la fuente oficial es obtenible (`A-003`)
| Campo | Valor |
|---|---|
| Estado | No implementada |
| Importancia | Alta |
| Urgencia | Bloqueante |
| Origen | manager |
| Sesion | S-001 |

- **Que:** comprobar si el historico completo de resultados de la fuente oficial se puede obtener
  de forma repetible desde el entorno de despliegue (`C-002`, Vercel), tal como lo supone `A-003`.
- **Por que:** `A-003` señala que si este supuesto resulta falso, no cae una funcionalidad sino el
  ciclo entero del producto, porque las secciones 5 a 19 del brief dependen todas del historico.
- **Criterio de cierre:** `A-003` pasa a `Confirmado` (y se traslada a `decisions.md` o
  `constraints.md`) o a `Refutado`, segun lo que se encuentre.

---

### T-004 - Acotar el enunciado del bloque de verificacion de `D-016` (`F-001`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Origen | report_auditor |
| Sesion | S-003 |

- **Que:** el bloque de verificacion de `D-016` se titulaba «cero identificadores `auditor` vivos»
  sin acotar ambito, mientras su comando cubria solo `.claude`, `CLAUDE.md` y `project.md`. Se anade
  bajo el bloque —sin tocar el comando ya ejecutado— una nota fechada que declara el ambito real y
  registra el barrido con ambito completo, con su patron y su salida cruda.
- **Por que:** un enunciado mas ancho que su comando da por cerrado lo que nadie miro. En este caso
  concreto tapo una fuga real, que es `F-002`.
- **Criterio de cierre:** `D-016` lleva la nota de ambito con los dos barridos y sus salidas crudas.
  Verificado en el diff de esta sesion.

---

### T-005 - Corregir los dos identificadores `auditor` vivos (`F-002`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Origen | report_auditor |
| Sesion | S-003 |

- **Que:** `_audit/findings.md:3` —cabecera viva de un registro activo— y el ejemplo de
  `_persistence/tasks.md` que nombra el valor del campo `Origen` pasan de `auditor` a
  `report_auditor`. Los dos son identificadores del agente, no el sustantivo comun que `D-016`
  excluye, y ninguno es historico.
- **Por que:** son las dos unicas referencias vivas que el barrido acotado de `D-016` no alcanzo.
- **Criterio de cierre:** el barrido con ambito completo ya no las devuelve; lo que queda en
  `findings.md` es evidencia citada de `F-001` y `F-002`. Registrado en la nota de ambito de `D-016`.

---

### T-006 - Devolver `DT-001` a `Propuesta (pendiente del usuario)` (`F-003`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Origen | report_auditor |
| Sesion | S-003 |

- **Que:** `DT-001` se registro como `Confirmada` en el cierre de `S-002`, valor que el Paso 5 de
  `protocol-close` prohibe al `session-closer`. Vuelve a `Propuesta (pendiente del usuario)` en el
  indice y en el detalle, con nota fechada que explica el cambio.
- **Por que:** `Confirmacion` existe para distinguir lo confirmado de lo supuesto. Escrito por quien
  el protocolo se lo prohibe, el campo deja de significar nada. `manager` tampoco puede confirmarla:
  el dueno de la confirmacion va dentro del valor, y es el usuario.
- **Criterio de cierre:** las dos apariciones dicen `Propuesta (pendiente del usuario)`, y la
  confirmacion queda pedida al usuario. Verificado en el diff de esta sesion.

---

### T-007 - Corregir la tabla de actores de `session-closer.md` (`F-004`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Origen | report_auditor |
| Sesion | S-003 |

- **Que:** la fila de `report_auditor` en la tabla de actores decia «su propio repositorio», resto
  del esquema de dos terminales que `D-012` revoco. Pasa a nombrar lo que escribe de verdad:
  `_audit/R-XXX.md`, `_audit/findings.md` y `_audit/index.md`, en este mismo repositorio.
- **Por que:** contradecia a `project.md`, a `CLAUDE.md` y a las dos lineas siguientes de su propio
  archivo, en una tabla que el `session-closer` lee en cada cierre.
- **Criterio de cierre:** `git grep -n "su propio repositorio" -- .claude` ya no devuelve esa linea.
  Verificado en el diff de esta sesion.
