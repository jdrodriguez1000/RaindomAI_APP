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
| [T-014](#t-014---anclar-los-dos-recuentos-sobre-head-de-a-001-y-t-012-f-011) | Anclar los dos recuentos sobre `HEAD` de `A-001` y `T-012` (`F-011`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-015](#t-015---propagar-la-segunda-excepcion-de-d-025-a-los-tres-sitios-de-la-regla-f-012) | Propagar la segunda excepcion de `D-025` a los tres sitios de la regla (`F-012`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-016](#t-016---anotar-en-d-023-que-d-026-ya-amplio-el-ambito-del-paso-1b-f-013) | Anotar en `D-023` que `D-026` ya amplio el ambito del Paso 1b (`F-013`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-017](#t-017---corregir-el-recuento-de-hallazgos-de-progressmd-f-014) | Corregir el recuento de hallazgos de `progress.md` (`F-014`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-018](#t-018---corregir-la-convencion-viva-de-auditfindingsmd-f-010) | Corregir la convencion viva de `_audit/findings.md` (`F-010`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-019](#t-019---dar-mecanismo-a-d-022-en-el-paso-6-de-protocol-close) | Dar mecanismo a `D-022` en el Paso 6 de `protocol-close` | Implementada | Media | No bloqueante | `000_preproject` |

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

🕒 **Nota anadida el 2026-09-02 (`S-006`), tras el hallazgo `F-011` de `R-005`.** La cifra «12
archivos en `HEAD`» del primer punto se escribio sin decir cual era ese `HEAD`. Era `e61454b`, y
sobre ese hash se reproduce:

```
$ git grep -c "debtec" e61454b -- . | wc -l
12
```

Sobre `510d580` —el commit que contiene esta ficha— son 13, y sobre `a800d6b` son 14: el recuento
crece con cada registro que cita el nombre antiguo, que es exactamente el motivo por el que `D-022`
obliga a anclarlo o fecharlo. **La cifra era correcta; lo que faltaba era el ancla.** El fondo de la
tarea no cambia.

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

---

### T-014 - Anclar los dos recuentos sobre `HEAD` de `A-001` y `T-012` (`F-011`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-006 |

- **Que:** la nota de `S-005` bajo `A-001` cerraba la senal 2 rehecha con un `git grep ... HEAD` sin
  decir cual era ese `HEAD`, y la ficha de `T-012` afirmaba «12 archivos en `HEAD`» igual. Se anaden
  dos notas fechadas que las anclan a `e61454b`, el `HEAD` real del momento, sin reescribir los
  bloques originales (`D-019`).
- **Por que:** es el patron de `F-005`, `F-006` y `F-008` reapareciendo **dentro de la correccion de
  `F-005`**, y contra `D-022`, escrita en ese mismo commit. Quien reprodujera el bloque de `A-001`
  sobre `510d580` obtenia `exit=0` y concluia que la senal 2 **si** se disparo — lo contrario de lo
  que la nota afirma, sobre una de las dos senales que pueden refutar `A-001`.
- **Lo que la verificacion demostro:** las dos cifras **eran correctas**; lo que faltaba era el
  ancla. Sobre `e61454b` el comando de `A-001` da `exit=1` y el recuento da 12, tal como se
  registraron. El fondo de las dos entradas no cambia.
- **Criterio de cierre:** las dos notas existen, cada una con su hash y su salida cruda, los bloques
  originales quedan intactos, y la nota de `A-001` anade la comprobacion de hoy sobre `a800d6b`.

---

### T-015 - Propagar la segunda excepcion de `D-025` a los tres sitios de la regla (`F-012`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-006 |

- **Que:** `D-025` generalizo a dos casos la excepcion de escritura de `manager` sobre `tasks.md`,
  pero solo lo escribio en la convencion de `tasks.md`. Los tres sitios que enuncian la regla para
  quien la ejecuta seguian diciendo «es la unica excepcion». Se reescriben los tres.
- **Por que:** es `F-007` otra vez, y `F-007` se cerro en `S-004` arreglando **esos mismos tres
  sitios**. `L-007` —«una excepcion se escribe donde esta la regla, no donde se decidio»— lleva
  escrita desde entonces. El `session-closer` arranca en frio y lee su skill, no `decisions.md`: con
  el texto viejo, una fila legitima editada a mano se le lee como infraccion.
- **Que se hizo, ademas de propagar:** los tres textos pasan a describir la excepcion **por su
  senal, no por su numero** — toda fila editada a mano lleva un `D-XXX` o un `F-NNN` citado en la
  propia tarea. Es el criterio que `R-005` propuso: contar filas invitaria a repartir un mismo
  cambio en dos sesiones para pasar por debajo del umbral. Y se le dice explicitamente al agente que
  **si la cita esta, no lo reporte como desfase**, que era el dano concreto del hallazgo.
- **Criterio de cierre:** el barrido de la regla no devuelve ningun enunciado que siga afirmando que
  la excepcion es unica, y el archivo de la etapa sigue pasando el control de agnosticidad.

---

### T-016 - Anotar en `D-023` que `D-026` ya amplio el ambito del Paso 1b (`F-013`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-006 |

- **Que:** `D-023` cerraba con una advertencia —«esto todavia no entra en el ambito del Paso 1b...
  queda pendiente de acordarla con el usuario»— que `D-026`, en el mismo commit, ya habia
  desmentido. Se anade una nota fechada que remite a `D-026`, sin reescribir el original (`D-019`).
- **Por que:** una entrada `Vigente` afirmaba como pendiente algo ya hecho. Quien lea `D-023` sin
  llegar a `D-026` concluye que la agnosticidad de esos archivos no tiene control que la compruebe.
- **Lo que la verificacion anadio al hallazgo:** la advertencia tambien **describia mal el ambito
  anterior**. Decia que cubria tres rutas; sobre `c70b757` cubria dos, y la tercera nunca estuvo
  —es justo el archivo donde los datos propios **si** deben vivir—. Va con su comando y su salida.
- **Criterio de cierre:** la nota existe bajo `D-023`, remite a `D-026`, corrige la descripcion del
  ambito anterior con evidencia anclada, y el texto original queda intacto.

---

### T-017 - Corregir el recuento de hallazgos de `progress.md` (`F-014`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-006 |

- **Que:** la frase del «Avance de la etapa» atribuia a una sola auditoria cinco hallazgos que
  abrieron dos, y despues sumaba uno que ya estaba en su propia lista. Se reescribe con la
  procedencia real de cada uno.
- **Por que:** ese campo es lo primero que se lee en cada arranque, y de los tres textos que cuentan
  lo mismo es el unico que se lee siempre. Un recuento que se contradice dentro de la misma frase
  invita a desconfiar del resto.
- **Lo que la verificacion anadio al hallazgo:** habia un **tercer error** que `F-014` no nombra
  —«`manager` evaluo los seis»— cuando fueron **cinco**: una de las dos auditorias abrio tres y la
  otra tres, pero uno de esos seis ya se habia aceptado y corregido en la sesion anterior. Y el
  mismo error estaba en **tres sitios**, no solo en el que el hallazgo senala. Los dos que el cierre
  sobrescribe quedaron corregidos; el de la bitacora, que es historico, lleva nota fechada.
- **Por que `manager` escribe en un archivo del cierre:** lo autoriza `D-027`, escrita hoy — el
  texto que senala un hallazgo aceptado lo corrige `manager`, con los limites que esa entrada fija.
- **Criterio de cierre:** los dos textos reescribibles dicen cinco y nombran bien la procedencia, la
  bitacora lleva su nota con comando y salida cruda, y ninguna de las tres se contradice.

---

### T-018 - Corregir la convencion viva de `_audit/findings.md` (`F-010`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-006 |

- **Que:** una convencion vigente del registro de hallazgos seguia mandando comprobar una entrada
  en un archivo que `D-021` renombro y que ya no existe. Se corrige **solo esa linea**.
- **Por que estaba parada:** `T-013` entrego el criterio que permite tocarla —el registro de
  hallazgos es historico **salvo sus convenciones vivas**— pero la dejo «pendiente del propio
  `report_auditor`». `R-005` mostro que ahi no la podia corregir nadie: el auditor tiene prohibido
  corregir, y `manager` tenia prohibido escribir ahi. Un defecto reconocido por las dos partes y sin
  dueno. Lo desatasca `D-027`.
- **Alcance, y es lo que hace segura la correccion:** las demas apariciones del nombre antiguo en
  ese archivo son **citas de evidencia dentro de hallazgos ya entregados** y no se tocan. Se
  identifico la unica que vive en la seccion de convenciones y se cambio esa.
- **Criterio de cierre:** el barrido acotado a la seccion de convenciones devuelve cero, y el
  recuento del archivo entero solo baja en uno — prueba de que no se toco ninguna cita historica.
- **Lo que esta tarea NO hace:** cerrar `F-010`. Su fila sigue `Aceptado — pendiente`; el estado
  `Implementado` lo escribe la auditoria siguiente.

---

### T-019 - Dar mecanismo a `D-022` en el Paso 6 de `protocol-close`
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-006 |

- **Que:** `D-022` vivia solo como regla escrita en el registro de decisiones, sin nada que la
  aplicara. Se anade al Paso 6 del protocolo de cierre una comprobacion mecanica: sobre las entradas
  de la sesion en curso, marcar las que cumplan **las dos** condiciones —ambito alcanzable por el
  cierre **y** declararse reproducibles sobre su propio commit— y senalarlas en el reporte.
- **Por que:** `F-011` es la prueba empirica de que la regla escrita no basta: se incumplio en el
  mismo commit que la creo, y es la quinta repeticion del mismo patron. `L-008` ya describe
  exactamente esto —una leccion sin mecanismo que la aplique no evita la reincidencia—. Lo
  recomendo `R-005` en su seccion de recomendaciones sin hallazgo.
- **Por que en el cierre y no en la auditoria:** el cierre corre **antes** del commit, asi que
  atrapa el defecto en vez de abrirlo como hallazgo un dia despues.
- **Por que exige las dos condiciones:** un ambito acotado a lo que la sesion no toca **si** se
  reproduce, y un recuento global fechado esta bien escrito. Pedir una sola convertiria el control
  en ruido, y un control que avisa de todo termina apagado (`D-026`).
- **Que respeta:** el agente **senala, no corrige** — los cuatro archivos del porque siguen sin ser
  suyos. Y rige hacia adelante: entradas de la sesion en curso, no las antiguas.
- **Criterio de cierre:** el Paso 6 lleva la comprobacion con sus dos condiciones, su tabla de
  reconocimiento, el caso que no se arregla anclando, y la instruccion de senalar sin arreglar. El
  archivo sigue pasando el control de fuga de datos propios.
