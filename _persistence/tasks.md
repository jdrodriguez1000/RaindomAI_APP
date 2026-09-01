# tasks.md

> Registro de las tareas **realizadas** y de las tareas **por realizar**.
> Cada tarea tiene codigo `T-XXX`, estado, importancia y urgencia.

---

## Indice

| Codigo | Tarea | Estado | Importancia | Urgencia | Etapa |
|---|---|---|---|---|---|
| [T-001](#t-001---definir-alcance-y-objetivo-del-proyecto) | Definir alcance y objetivo del proyecto | No implementada | Alta | Bloqueante | `005_discovery` |
| [T-002](#t-002---declarar-las-etapas-posteriores-a-000_preproject) | Declarar las etapas posteriores a `000_preproject` | No implementada | Media | No bloqueante | `005_discovery` |
| [T-003](#t-003---verificar-si-el-historico-de-la-fuente-oficial-es-obtenible-a-003) | Verificar si el historico de la fuente oficial es obtenible (`A-003`) | No implementada | Alta | Bloqueante | `000_preproject` |
| [T-004](#t-004---acotar-el-enunciado-del-bloque-de-verificacion-de-d-016-f-001) | Acotar el enunciado del bloque de verificacion de `D-016` (`F-001`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-005](#t-005---corregir-los-dos-identificadores-auditor-vivos-f-002) | Corregir los dos identificadores `auditor` vivos (`F-002`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-006](#t-006---devolver-dt-001-a-propuesta-pendiente-del-usuario-f-003) | Devolver `DT-001` a `Propuesta (pendiente del usuario)` (`F-003`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-007](#t-007---corregir-la-tabla-de-actores-de-session-closermd-f-004) | Corregir la tabla de actores de `session-closer.md` (`F-004`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-008](#t-008---escribir-en-la-convencion-de-tasksmd-la-excepcion-que-fija-d-020-f-007) | Escribir en la convencion de `tasks.md` la excepcion que fija `D-020` (`F-007`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-009](#t-009---acotar-la-observacion-de-a-001-y-rehacer-su-criterio-de-refutacion-f-005) | Acotar la observacion de `A-001` y rehacer su criterio de refutacion (`F-005`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-010](#t-010---acotar-los-recuentos-de-la-nota-de-d-016-f-006) | Acotar los recuentos de la nota de `D-016` (`F-006`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-011](#t-011---acotar-el-bloque-de-verificacion-de-d-021-f-008) | Acotar el bloque de verificacion de `D-021` (`F-008`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-012](#t-012---escribir-en-dt-001-el-criterio-de-cierre-realmente-aplicado-f-009) | Escribir en `DT-001` el criterio de cierre realmente aplicado (`F-009`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-013](#t-013---acotar-el-alcance-historico-de-d-021-f-010) | Acotar el alcance historico de `D-021` (`F-010`) | Implementada | Baja | No bloqueante | `000_preproject` |

---

## Convenciones

| Campo | Valores posibles |
|---|---|
| Codigo | `T-XXX`, correlativo, no se reutiliza |
| Estado | `Implementada` / `No implementada` / `Cancelada` / `Suspendida` |
| Importancia | `Alta` / `Media` / `Baja` |
| Urgencia | `Bloqueante` / `No bloqueante` |
| Origen | `usuario` / `manager` / `report_auditor` |
| Etapa | una de las etapas declaradas en la tabla «Etapas» de `project.md` |

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
con `progress.md`. **Tiene una unica excepcion, y esta escrita:** cuando `manager` evalua un hallazgo
`F-NNN` de una auditoria y lo acepta, escribe **en ese momento** la `T-XXX` con
`Origen: report_auditor`, sin esperar al cierre. Lo fija `D-020`, confirmada por el usuario el
2026-09-01.

🔑 **Por que esa excepcion existe.** La fila del hallazgo en `_audit/findings.md` tiene que
citar el codigo de su tarea para ser auditable, y una fila que cita una `T-XXX` inexistente no lo es.
Esperar al cierre dejaria el hallazgo evaluado y sin registro durante toda la jornada — el agujero
que el estado `Aceptado — pendiente` existe justamente para tapar.

**Y tiene una segunda excepcion, escrita el 2026-09-01 (`D-025`):** `manager` tambien escribe aqui
cuando el cambio **nace de una decision ya registrada que el `session-closer` no puede deducir del
`git diff`** — reasignar la etapa de una tarea, o cambiar la estructura del archivo porque lo pidio
el usuario. El agente arranca en frio y solo ve archivos: una orden del usuario no deja rastro en el
diff, y esperar al cierre significa perderla.

⚠️ **Son dos excepciones, no una puerta.** Las dos exigen lo mismo: **un `D-XXX` o un `F-NNN` que
las respalde, citado en la propia tarea**. Sin esa cita, cualquier edicion a mano se vuelve
indistinguible de saltarse la regla — y entonces la regla deja de existir. Lo demas sigue siendo del
`session-closer`.

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
| Etapa | |
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
| Etapa | `005_discovery` |
| Origen | manager |
| Sesion | S-001 |

- **Que:** definir el alcance y el objetivo del proyecto, contrastando `_brief/client_brief.md`
  punto por punto (ver `A-002`), y registrar la decision resultante con su `D-XXX`.
- **Por que:** `project.md` declara que hoy solo esta registrada la etapa `000_preproject`; las
  etapas posteriores y el producto mismo dependen de que exista esa definicion. Un encargo del
  cliente no es una decision del proyecto.
- **Criterio de cierre:** existe un `D-XXX` en `decisions.md` que fija alcance y objetivo, y
  `project.md` deja de decir que las etapas posteriores no estan registradas.

🕒 **Nota del 2026-09-01 (`S-005`): esta tarea cambia de etapa.** Nacio en `000_preproject`, pero
`D-023` dejo escrito que esa etapa **no define alcance ni objetivo** — monta el andamio y nada mas—.
Por decision del usuario (`D-024`, `D-025`) pasa a **`005_discovery`**. No cambia nada de su
contenido: cambia cuando se hace.

---

### T-002 - Declarar las etapas posteriores a `000_preproject`
| Campo | Valor |
|---|---|
| Estado | No implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `005_discovery` |
| Origen | manager |
| Sesion | S-001 |

- **Que:** decidir y registrar en `project.md` (tabla «Etapas») que etapas siguen a
  `000_preproject`, tomando como propuesta de partida —no como decision— la secuencia del brief
  (`_brief/client_brief.md`, §22).
- **Por que:** `project.md` dice explicitamente que esto no esta decidido y que un encargo no
  sustituye a una decision registrada.
- **Criterio de cierre:** la tabla «Etapas» de `project.md` lista mas de una etapa, con su `D-XXX`.

🕒 **Nota del 2026-09-01 (`S-005`): cambia de etapa, y su criterio de cierre se queda corto.** Pasa a
**`005_discovery`** por la misma razon que `T-001` (`D-023`, `D-024`, `D-025`). Ademas, `D-024` acaba
de declarar `005_discovery` en la tabla «Etapas», con lo que el criterio escrito arriba —«lista mas
de una etapa»— **ya se cumple literalmente sin que la tarea este hecha**. El criterio original **no
se reescribe**; leelo asi: lo que cierra esta tarea es **la secuencia completa** de etapas
posteriores, decidida y registrada, no haber nombrado la inmediata para que las tareas de alcance
tuvieran donde ir.

---

### T-003 - Verificar si el historico de la fuente oficial es obtenible (`A-003`)
| Campo | Valor |
|---|---|
| Estado | No implementada |
| Importancia | Alta |
| Urgencia | Bloqueante |
| Etapa | `000_preproject` |
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
| Etapa | `000_preproject` |
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
| Etapa | `000_preproject` |
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
| Etapa | `000_preproject` |
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
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-003 |

- **Que:** la fila de `report_auditor` en la tabla de actores decia «su propio repositorio», resto
  del esquema de dos terminales que `D-012` revoco. Pasa a nombrar lo que escribe de verdad:
  `_audit/R-XXX.md`, `_audit/findings.md` y `_audit/index.md`, en este mismo repositorio.
- **Por que:** contradecia a `project.md`, a `CLAUDE.md` y a las dos lineas siguientes de su propio
  archivo, en una tabla que el `session-closer` lee en cada cierre.
- **Criterio de cierre:** `git grep -n "su propio repositorio" -- .claude` ya no devuelve esa linea.
  Verificado en el diff de esta sesion.

---

### T-008 - Escribir en la convencion de `tasks.md` la excepcion que fija `D-020` (`F-007`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-004 |

- **Que:** la convencion de este archivo prohibia en absoluto escribirlo a mano durante la jornada,
  mientras `D-020` permitia a `manager` hacerlo al registrar un hallazgo aceptado. Se escribe la
  excepcion **dentro de la convencion**, acotada a ese unico caso y con su motivo, y se refleja
  tambien en `protocol-close` y en `session-closer.md` para que el cierre no duplique la tarea.
- **Por que:** quien abriera este archivo sin conocer `D-020` leia una prohibicion que ya no regia,
  con `T-004`..`T-007` incumpliendola a la vista. El defecto no era la lectura de `D-020` sino la
  contradiccion sin registro.
- **Criterio de cierre:** la convencion enuncia la excepcion y cita `D-020`; el usuario confirmo la
  lectura el 2026-09-01, y esa confirmacion quedo anotada en `D-020`. Verificado en el diff de esta
  sesion.

---

### T-009 - Acotar la observacion de `A-001` y rehacer su criterio de refutacion (`F-005`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-005 |

- **Que:** la observacion del 2026-09-01 bajo `A-001` registra `git grep -n "| Pendiente |" --
  _audit/index.md` con `exit=1` y concluye «cero sesiones cerradas sin auditar». Sobre el commit que
  contiene esa afirmacion el comando devuelve una linea. El bloque **no se reescribe** (`D-019`): se
  le anade debajo una nota fechada que declara su ambito real —recuento tomado antes de que el
  cierre escribiera la fila de su propia sesion— y que **rehace la señal 2** para que sea
  comprobable: una sesion cerrada sigue sin auditar cuando su fila continua en `Pendiente` **al
  abrirse la sesion siguiente**, no en el instante del cierre.
- **Por que:** tal como estaba escrita, la señal 2 no podia dispararse nunca. El `session-closer`
  anade la fila de su sesion con `Pendiente` **antes** de commitear, asi que el comando devuelve
  `exit=0` en todo commit de cierre y `exit=1` solo despues de la auditoria. Una señal de refutacion
  que no puede activarse deja `A-001` sin la unica de sus dos señales que no admite otra lectura.
- **Criterio de cierre:** bajo la observacion de `A-001` hay una nota fechada que (a) acota el
  bloque original a lo que probaba y (b) enuncia la señal 2 con su momento de comprobacion. El
  bloque original queda intacto.

---

### T-010 - Acotar los recuentos de la nota de `D-016` (`F-006`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-005 |

- **Que:** la nota del 2026-09-01 bajo el bloque de verificacion de `D-016` afirma que el barrido se
  hizo «ya escrito el registro de esta sesion» y registra `_persistence/progress.md:7` sin
  `_audit/S-003.md`. Sobre `ea0b850`, el commit que la contiene, son `progress.md:8` y
  `_audit/S-003.md:3`. Se anade una segunda nota fechada que declara el momento real del recuento.
- **Por que:** la correccion de `F-001` repite dentro de si misma el defecto que `F-001` describe
  —declarar mas ambito del que el comando tuvo—, y eso le resta valor a `L-006`. Las diferencias son
  lineas escritas despues del barrido y ninguna es una referencia viva: el fondo es correcto, lo que
  falla es la declaracion de alcance temporal.
- **Criterio de cierre:** la nota lleva su recuento sobre `ea0b850` con comando y salida cruda, y
  dice que el recuento anterior se tomo antes de cerrar el registro de la sesion. Los dos bloques
  anteriores quedan intactos.

---

### T-011 - Acotar el bloque de verificacion de `D-021` (`F-008`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-005 |

- **Que:** `D-021` afirma literalmente que su recuento «se tomo con el registro de esta sesion ya
  escrito, que es lo que hace que se reproduzca sobre el commit que lo contiene», y no se reproduce:
  sobre `c70b757` `progress.md` da **6** y no 2, falta la linea `_audit/S-004.md:17`, y de las 13 de
  `decisions.md` solo **9** caen dentro de la entrada (empieza en la linea 573). Se anade una nota
  fechada con el recuento real sobre `c70b757` y sobre `HEAD`.
- **Por que:** el defecto no es la cifra, es la frase. `D-021` es la primera entrada escrita despues
  de `L-006` y reincide, ademas **afirmando una reproducibilidad que no tiene**: un registro que se
  autodeclara reproducible y no lo es desalienta la comprobacion en vez de solo omitirla.
- **Criterio de cierre:** bajo el bloque de `D-021` hay una nota fechada que corrige la frase, da el
  recuento sobre `c70b757` con su comando y su salida cruda, y separa las 9 coincidencias internas
  de las 4 externas. El bloque original queda intacto.

---

### T-012 - Escribir en `DT-001` el criterio de cierre realmente aplicado (`F-009`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-005 |

- **Que:** el campo «Como se paga» de `DT-001` exige `git grep -n "debtec" -- .` en cero, criterio
  absoluto que la entrada no cumple —el comando devuelve 12 archivos en `HEAD`— mientras su estado
  ya es `Implementada`. Se anade a la nota fechada existente el criterio de cierre realmente
  aplicado, sin reescribir el «Como se paga» original.
- **Por que:** es el mismo defecto que `F-007`, cuya leccion `L-007` —«una excepcion se escribe
  donde esta la regla, no donde se decidio»— se escribio en el mismo commit. La informacion correcta
  esta en la entrada (la nota remite a `D-021`), pero quien aplique el criterio literal concluye que
  la deuda no esta pagada.
- **Criterio de cierre:** la nota de `DT-001` enuncia el criterio aplicado —cero en `.claude`,
  `CLAUDE.md` y `project.md`, historico intacto por `D-021`— con su comando y su salida cruda. El
  campo «Como se paga» original queda intacto.

---

### T-013 - Acotar el alcance historico de `D-021` (`F-010`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-005 |

- **Que:** `D-021` clasifico `_audit/` entero como historico, y por eso `_audit/findings.md:56`
  sigue mandando comprobar una entrada en `debtec.md`, archivo que ya no existe — dentro de una
  **convencion vigente**, no de una cita historica. Se anade a `D-021` una nota fechada que acota el
  criterio: `_audit/` es historico **salvo las convenciones de `findings.md` y de `index.md`**, que
  son registro vivo.
- **Por que:** el criterio se aplico por carpeta y no por naturaleza del texto. Los `S-XXX.md` y los
  `R-XXX.md` son documentos entregados y no deben reescribirse; `findings.md` e `index.md` son
  registros vivos cuyas convenciones se siguen aplicando en cada pasada.
- **Que queda fuera de esta tarea:** la correccion del texto de `_audit/findings.md:56`. Ese archivo
  no lo escribe `manager` mas alla de la fila de estado de cada hallazgo; la linea la corrige
  `report_auditor` en una pasada posterior. Lo que esta tarea entrega es el criterio que se lo
  permite.
- **Criterio de cierre:** `D-021` lleva la nota fechada con la excepcion enunciada y su motivo, y la
  fila de `F-010` en `_audit/findings.md` cita esta tarea y deja constancia de que la correccion del
  texto es del auditor.
