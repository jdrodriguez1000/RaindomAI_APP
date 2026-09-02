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
| [T-020](#t-020---escribir-el-archivo-de-etapa-_phases005_discoverymd-f-015) | Escribir el archivo de etapa `_phases/005_discovery.md` (`F-015`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-021](#t-021---reescribir-la-apertura-de-la-convencion-de-tasksmd-f-016) | Reescribir la apertura de la convencion de `tasks.md` (`F-016`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-022](#t-022---escribir-las-plantillas-de-_templates005_discovery) | Escribir las plantillas de `_templates/005_discovery/` | Implementada | Media | No bloqueante | `000_preproject` |
| [T-023](#t-023---registrar-el-bloque-de-verificacion-de-t-020-f-017) | Registrar el bloque de verificacion de `T-020` (`F-017`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-024](#t-024---registrar-el-barrido-de-variantes-de-t-021-con-su-patron-y-su-ambito-f-018) | Registrar el barrido de variantes de `T-021` con su patron y su ambito (`F-018`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-025](#t-025---endurecer-en-protocol-close-la-lista-de-la-seccion-1-del-informe-f-019) | Endurecer en `protocol-close` la lista de la seccion 1 del informe (`F-019`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-026](#t-026---extender-el-paso-1b-de-protocol-close-a-_templates) | Extender el Paso 1b de `protocol-close` a `_templates/` | Implementada | Media | No bloqueante | `000_preproject` |
| [T-027](#t-027---borrar-la-viñeta-residual-de-f-017-en-findingsmd-f-020) | Borrar la viñeta residual de `F-017` en `findings.md` (`F-020`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-028](#t-028---corregir-en-progressmd-el-commit-que-se-atribuye-a-r-007-f-021) | Corregir en `progress.md` el commit que se atribuye a `R-007` (`F-021`) | Cancelada | Baja | No bloqueante | `000_preproject` |
| [T-029](#t-029---anotar-los-tres-bloques-de-verificacion-de-decisionsmd-que-no-se-reproducen-f-022) | Anotar los tres bloques de verificacion de `decisions.md` que no se reproducen (`F-022`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-030](#t-030---registrar-en-decisionsmd-la-desviacion-de-t-026-f-023) | Registrar en `decisions.md` la desviacion de `T-026` (`F-023`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-031](#t-031---mover-a-005_discovery-la-ruta-de-los-artefactos-del-descubrimiento-d-045) | Mover a `005_discovery/` la ruta de los artefactos del descubrimiento (`D-045`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-032](#t-032---dejar-constancia-de-que-f-021-se-resolvio-por-desaparicion-no-por-correccion-f-024) | Dejar constancia de que `F-021` se resolvio por desaparicion, no por correccion (`F-024`) | Implementada | Alta | No bloqueante | `000_preproject` |
| [T-033](#t-033---anotar-los-bloques-de-verificacion-de-d-043-y-d-044-que-no-se-reproducen-f-025) | Anotar los bloques de verificacion de `D-043` y `D-044` que no se reproducen (`F-025`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-034](#t-034---corregir-la-cita-cruzada-l-013-de-dt-002-f-026) | Corregir la cita cruzada `L-013` de `DT-002` (`F-026`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-035](#t-035---anclar-el-bloque-de-verificacion-de-t-032-que-no-se-reproduce-sobre-su-commit-f-027) | Anclar el bloque de verificacion de `T-032`, que no se reproduce sobre su commit (`F-027`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-036](#t-036---completar-en-s-010-la-viñeta-de-decisionsmd-que-omite-dos-ediciones-f-028) | Completar en `S-010` la viñeta de `decisions.md`, que omite dos ediciones (`F-028`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-037](#t-037---escribir-el-inventario-de-acciones-irreversibles-del-proyecto-lg-38) | Escribir el inventario de acciones irreversibles del proyecto (`LG-38`) | Pendiente | Alta | No bloqueante | `000_preproject` |
| [T-038](#t-038---igualar-el-barrido-de-fuga-de-protocol-audit-con-el-de-protocol-close) | Igualar el barrido de fuga de `protocol-audit` con el de `protocol-close` | Pendiente | Media | No bloqueante | `000_preproject` |

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
con `progress.md`. **Tiene dos excepciones, y las dos estan escritas.** La primera: cuando `manager`
evalua un hallazgo `F-NNN` de una auditoria y lo acepta, escribe **en ese momento** la `T-XXX` con
`Origen: report_auditor`, sin esperar al cierre. Lo fija `D-020`, confirmada por el usuario el
2026-09-01.

🔑 **Por que esa primera excepcion existe.** La fila del hallazgo en `_audit/findings.md` tiene que
citar el codigo de su tarea para ser auditable, y una fila que cita una `T-XXX` inexistente no lo es.
Esperar al cierre dejaria el hallazgo evaluado y sin registro durante toda la jornada — el agujero
que el estado `Aceptado — pendiente` existe justamente para tapar.

**La segunda, escrita el 2026-09-01 (`D-025`):** `manager` tambien escribe aqui
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

🕒 **Nota anadida el 2026-09-02 (`S-007`), tras el hallazgo `F-016` de `R-006`.** El criterio de
arriba **se deja tal cual se escribio** (`D-019`), y hay que leerlo con esta precision: «ningun
enunciado» significaba **ningun enunciado vivo de esta regla**, no ninguna coincidencia del patron.
Tal como quedo redactado, el barrido no puede dar cero nunca: siempre devolvera la regla de los
supuestos `A-XXX` de `protocol-close`, que es otra, y la cita historica que esta tarea hace del texto
viejo cuatro lineas mas arriba. El criterio corregido —enumerando lo que si puede quedar— vive en
`T-021`, que es donde se atendio el hallazgo.

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

---

### T-020 - Escribir el archivo de etapa `_phases/005_discovery.md` (`F-015`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-007 |

- **Que:** `D-023` es una decision vigente cuyo cuerpo dice «un archivo por etapa declarada».
  `project.md` declara dos etapas y `_phases/` contenia una. Se escribe el archivo que faltaba,
  siguiendo la estructura de ocho secciones de `_phases/000_preproject.md`.
- **Por que:** era la tercera sesion consecutiva en que el asunto se nombraba sin agendarse —`D-024`
  lo anoto como advertencia, `R-005` lo repitio sin hallazgo, `S-006` lo volvio a nombrar—. Un
  incumplimiento de una decision vigente que solo vive en prosa dentro de informes **no aparece en
  este archivo, que es lo que `session-starter` lee al arrancar**: desaparece del radar en cuanto
  nadie se acuerde de repetirlo.
- **De donde sale el contenido:** de dos archivos que el usuario aporto como guia, adaptados y no
  copiados (`D-033`), y de la guia de metodo del proyecto para la taxonomia de actores, los
  interesados y el Gate. Los codigos se resolvieron en `D-034` y la ubicacion de las plantillas en
  `D-035`.
- **Que se resolvio de paso, y no lo pedia el hallazgo:** el archivo **autoriza explicitamente
  definir el alcance y el objetivo, y declarar las etapas posteriores**. `D-025` ya habia mandado
  esas tareas a `005_discovery`, pero ningun archivo decia que la etapa las autorizara — vivian en
  una etapa sin permiso escrito para ejecutarlas.
- **Criterio de cierre:** `_phases/` contiene un archivo por cada etapa de la fila «Etapas
  declaradas» de `project.md`, y el control de fuga de datos propios del Paso 1b sigue devolviendo
  cero lineas sobre `.claude CLAUDE.md _phases _methodology`.

🕒 **Nota del 2026-09-02 (`S-008`, `T-023`, hallazgo `F-017`): los dos bloques de abajo se añaden
despues.** El criterio se comprobo en `S-007` contra el arbol de trabajo, pero la ficha se cerro con
un veredicto —«se comprobo»— en vez de con la orden y su salida. Los bloques **no se presentan como
evidencia contemporanea**: se anclan a `122b770`, el commit sobre el que la tarea quedo
`Implementada`, y cualquiera puede reproducirlos contra ese hash. El texto de arriba no se toca
(`D-019`).

**Verificacion 1 — `_phases/` contiene un archivo por cada etapa declarada, sobre `122b770`:**

```
$ git ls-tree --name-only 122b770 _phases/
_phases/000_preproject.md
_phases/005_discovery.md

$ git show 122b770:project.md | grep -n "Etapas declaradas"
79:| Etapas declaradas | `000_preproject`, `005_discovery` |
```

Dos etapas declaradas, dos archivos. Se cumple.

**Verificacion 2 — el control de fuga de datos propios del Paso 1b, sobre `122b770` y con el ambito
literal que el criterio nombra:**

```
$ git grep -nE "RaindomAI|RaidomAI|Proyectos_TripleS|github\.com" 122b770 -- .claude CLAUDE.md _phases _methodology ; echo "exit=$?"
exit=1
```

Cero lineas. Se cumple.

---

### T-021 - Reescribir la apertura de la convencion de `tasks.md` (`F-016`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-007 |

- **Que:** la convencion de este archivo seguia abriendo con «Tiene una unica excepcion, y esta
  escrita» aunque cuatro parrafos mas abajo anunciaba la segunda (`D-025`). Se reescribe a «Tiene dos
  excepciones, y las dos estan escritas», y se ajustan los dos parrafos que la seguian para que no
  las presenten como una y un añadido.
- **Por que:** era el mismo patron de `F-009` —un criterio de cierre autodeclarado que no se cumple
  al correrlo—, y aparecia dentro de la tarea que corrigio un hallazgo sobre ese mismo descuido.
  Quien volviera a correr el barrido de `T-015` encontraria una coincidencia y no sabria si era un
  resto o un descuido.
- **Que se hizo ademas, por `L-009`:** el hallazgo citaba **un** enunciado, y una correccion que
  barre solo el ejemplo citado deja vivo el defecto. Se barrieron tambien las variantes que el patron
  del hallazgo no cubria —«una sola excepcion», «la excepcion es unica», «solo una excepcion»—. No
  aparecio ninguna mas viva de esta regla. 🕒 **El alcance de esta frase se corrige el 2026-09-02
  (`T-024`, hallazgo `F-018`):** decia «sobre todo el repositorio» y ninguno de los dos bloques de
  abajo cubre ese ambito. El barrido global, con su patron y su salida, esta en el tercer bloque.
- **Por que esta opcion y no la otra:** `R-006` ofrecia dos caminos —reescribir la convencion, o
  acotar el criterio de cierre de `T-015`—. Se hizo el primero porque es donde estaba el defecto: la
  regla mal enunciada la lee quien ejecuta, y el criterio de `T-015` solo la comprueba. `T-015` queda
  con su texto intacto y una **nota fechada** que precisa como debia leerse (`D-019`), porque
  reescribir el criterio de una tarea ya cerrada seria cambiar la historia auditada.
- **Criterio de cierre, y viene acotado a proposito:** el barrido corre sobre **el sitio donde la
  regla se enuncia**, no sobre el repositorio entero. En `.claude`, `CLAUDE.md` y `_phases/` deja una
  sola coincidencia, y es de otra regla —la de los supuestos `A-XXX` en `protocol-close`—; y en la
  seccion «Convenciones» de este archivo no deja ninguna, en ninguna de sus variantes.
- **Por que acotado, y no «cero coincidencias en el repositorio»:** ese es el enunciado que hundio a
  `T-015` y abrio `F-016`. Un barrido global **no puede dar cero nunca**: `_audit/` guarda los
  hallazgos que citan el texto viejo literalmente, y el cuerpo de `T-015` tambien lo cita — y ninguno
  de los dos se reescribe (`D-019`). Un criterio que no puede cumplirse no mide nada.

**Verificacion — donde la regla se enuncia para quien la ejecuta:**

```
$ grep -rn "unica excepcion\|salvo la .T-XXX" .claude CLAUDE.md _phases ; echo "exit=$?"
.claude/skills/protocol-close/SKILL.md:490:**La unica excepcion, y es mecanica:** si un supuesto `A-XXX` quedo comprobado por la evidencia del
exit=0
```

**Y la seccion «Convenciones» de este archivo, con las tres variantes que el hallazgo no citaba:**

```
$ sed -n '/^## Convenciones/,/^## Tareas/p' _persistence/tasks.md | grep -n "unica excepcion\|una sola excepcion\|la excepcion es unica\|solo una excepcion" ; echo "exit=$?"
exit=1
```

🕒 **Nota del 2026-09-02 (`S-008`, `T-024`, hallazgo `F-018`): el tercer bloque se añade despues.**
Los dos de arriba corren acotados y no sostienen la frase «sobre todo el repositorio» que la ficha
llevaba. El de abajo se ancla a `122b770`, el commit sobre el que la tarea quedo `Implementada`, y
lleva el patron **insensible a mayusculas** — la variante que a `T-021` se le escapo. El texto
original no se reescribe (`D-019`); se acota arriba y se completa aqui.

**Verificacion 3 — el barrido global, con su patron y su ambito, sobre `122b770`:**

```
$ git grep -niE "una sola excepcion|la excepcion es unica|solo una excepcion|unica excepcion" 122b770 -- . | wc -l
59
```

Cincuenta y nueve lineas, y **es correcto que las haya**: `_audit/` guarda los hallazgos que citan
el texto viejo literalmente, y el cuerpo de `T-015` tambien lo cita — ninguno se reescribe (`D-019`).
Lo que hay que mirar es el registro vivo y el metodo, sin `_audit/`:

```
$ git grep -niE "una sola excepcion|la excepcion es unica|solo una excepcion|unica excepcion" 122b770 -- .claude CLAUDE.md _phases _persistence project.md
122b770:.claude/agents/session-closer.md:90:  - *Unica excepcion, y es mecanica:* ascender un supuesto `A-XXX` ya comprobado por el diff — y
122b770:.claude/skills/protocol-close/SKILL.md:490:**La unica excepcion, y es mecanica:** si un supuesto `A-XXX` quedo comprobado por la evidencia del
122b770:_persistence/decisions.md:625:  quedo registrado como la unica excepcion conocida (`DT-001`, `Propuesta (pendiente del usuario)`).
122b770:_persistence/lessons.md:293:  que siga afirmando que la excepcion es unica». `F-016` lo corrio y devolvio uno. Al corregirlo,
122b770:_persistence/progress.md:61:| Avance de la etapa | `R-006` (sobre `d906a5d`) abrio `F-015` y `F-016`. ... «una unica excepcion» cuatro parrafos despues de escribir la segunda. ... |
122b770:_persistence/progress.md:176:  literal, decision del usuario. `debtec.md` quedo registrado como la unica excepcion conocida a la
122b770:_persistence/progress.md:346:  apertura de la convencion de `tasks.md`, que anunciaba «una unica excepcion» cuatro parrafos
122b770:_persistence/tasks.md:466:  quien la ejecuta seguian diciendo «es la unica excepcion». Se reescriben los tres.
122b770:_persistence/tasks.md:477:  la excepcion es unica, y el archivo de la etapa sigue pasando el control de agnosticidad.
122b770:_persistence/tasks.md:640:- **Que:** la convencion de este archivo seguia abriendo con «Tiene una unica excepcion, y esta
122b770:_persistence/tasks.md:650:  del hallazgo no cubria —«una sola excepcion», «la excepcion es unica», «solo una excepcion»— sobre
122b770:_persistence/tasks.md:669:$ grep -rn "unica excepcion\|salvo la .T-XXX" .claude CLAUDE.md _phases ; echo "exit=$?"
122b770:_persistence/tasks.md:670:.claude/skills/protocol-close/SKILL.md:490:**La unica excepcion, y es mecanica:** si un supuesto `A-XXX` quedo comprobado por la evidencia del
122b770:_persistence/tasks.md:677:$ sed -n '/^## Convenciones/,/^## Tareas/p' _persistence/tasks.md | grep -n "unica excepcion\|una sola excepcion\|la excepcion es unica\|solo una excepcion" ; echo "exit=$?"
```

📌 **La linea de `progress.md:61` se abrevia con `...` porque es una celda de tabla de mas de dos mil
caracteres**; el resto de la salida es literal. Y **ninguna de estas catorce lineas es un resto vivo
de la regla vieja:**

| Donde | Que es |
|---|---|
| `session-closer.md:90`, `protocol-close/SKILL.md:490` | **otra regla**: la excepcion mecanica de los supuestos `A-XXX`. La primera va en mayuscula, y es justo la que el patron de `T-021` no alcanzaba |
| `decisions.md:625`, `progress.md:176` | **otra regla todavia**: `debtec.md` como unica excepcion conocida a la grafia inglesa |
| `lessons.md:293`, `progress.md:61`, `progress.md:346`, `tasks.md:466`, `tasks.md:477`, `tasks.md:640`, `tasks.md:650`, `tasks.md:669-677` | **el rastro de la propia correccion**: `L-009`, `F-016`, `T-015` y esta misma ficha citando el texto que se corrigio. No se reescriben (`D-019`) |

---

### T-022 - Escribir las plantillas de `_templates/005_discovery/`
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | usuario |
| Sesion | S-007 |

- **Que:** escribir las plantillas de los artefactos del descubrimiento en
  `_templates/005_discovery/`, crear la carpeta y declararla en la tabla «Carpetas propias» de
  `project.md`.
- **Por que:** `_phases/005_discovery.md` remite a esas plantillas y no existian; mientras no
  existan, un artefacto de la etapa se escribe a mano y no hay adherencia a plantilla que comprobar
  —que es una de las reglas de operacion de `CLAUDE.md`.
- **Por que no se hizo en `S-007`:** el usuario pidio expresamente no escribirlas todavia (`D-035`).
  La carpeta y su fila en `project.md` entran **en esta misma tarea y no antes**, porque `git` no
  versiona carpetas vacias y una fila sin carpeta produce una diferencia en el control de carpetas
  de cada cierre.
- **Respaldo de la escritura a mano en este archivo:** `D-035`, decision del usuario que el
  `session-closer` no puede deducir del `git diff` — la segunda excepcion de la convencion de arriba.
- **Criterio de cierre:** `_templates/005_discovery/` existe con sus plantillas, tiene su fila en
  «Carpetas propias» de `project.md`, ninguna plantilla arrastra vocabulario del esquema revocado, y
  el barrido de agnosticidad sobre `_templates/` devuelve cero.

🕒 **Nota del 2026-09-02 (`S-008`): esta tarea cambia de etapa y de alcance, y las dos cosas se
decidieron despues de escribirla.**

- **Etapa: de `005_discovery` a `000_preproject` (`D-039`).** `R-007` lo observo sin abrirlo como
  hallazgo: escribir plantillas es andamiaje, no descubrimiento — no responde ninguna pregunta sobre
  la necesidad del cliente. Dejarla dentro mezclaria la condicion de salida de `005_discovery` con
  trabajo de metodo.
- **Alcance: de cinco plantillas a cuatro (`D-037`).** La quinta —restricciones y supuestos—
  duplicaba `_persistence/constraints.md` y `_persistence/assumptions.md`, que es donde `D-034` ya
  habia mandado los `C-XXX` y los `A-XXX` del descubrimiento. Por eso el titulo deja de decir «las
  cinco».
- **Lo que ya no queda pendiente:** donde viven los artefactos **rellenos** dejo de estar sin
  decidir — es `_discovery/`, por `D-036`.

**Verificacion 1 — las cuatro plantillas existen:**

```
$ ls _templates/005_discovery/
005_needs.md
010_actors.md
015_stakeholders.md
020_hypothesis.md
```

**Verificacion 2 — ninguna arrastra vocabulario del esquema revocado ni rutas inexistentes:**

```
$ grep -rnE "SUP-[0-9]|RES-[0-9]|_memory/|terminal ejecutora|NO AUDITABLE|015_gate1" _templates/ ; echo "exit=$?"
exit=1
```

**Verificacion 3 — `_templates/` pasa el barrido de agnosticidad, ya con el ambito ampliado por
`T-026`:**

```
$ grep -rnE "RaindomAI|RaidomAI|Proyectos_TripleS|github\.com|C:\\Users|USUARIO|jdrodriguez" .claude CLAUDE.md _phases _methodology _templates ; echo "exit=$?"
exit=1
```

**Verificacion 4 — la carpeta tiene su fila en «Carpetas propias» de `project.md`:**

```
$ grep -c "^| \`_templates/\`" project.md
1
```

**Verificacion 5, por iniciativa propia — que codigos instanciados llevan dentro las plantillas.**
`CLAUDE.md` exige codigos genericos en `_phases/`, y al meter `_templates/` en la misma lista habia
que mirar si la exigencia se traslada. El barrido devuelve solo `N-00X` e `I-00X`, que son el numero
de la primera ficha y los de los ejemplos — no codigos de este proyecto con contenido detras:

```
$ grep -rnoE "\b(T|D|C|A|L|S|R|N|I|DT|F)-[0-9]{3}\b" _templates/ | grep -oE "[A-Z]+-[0-9]{3}" | sort | uniq -c
      5 I-001
      3 I-002
      3 I-003
      5 N-001
      4 N-002
      1 N-003
```

📌 **La diferencia con `_phases/` queda escrita en `CLAUDE.md`**, para que un barrido futuro sobre
`_templates/` no lea estas veintiuna lineas como un defecto.

---

### T-023 - Registrar el bloque de verificacion de `T-020` (`F-017`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-008 |

- **Que:** añadir a la ficha de `T-020` los dos bloques de verificacion que su propio criterio de
  cierre nombra —el listado de `_phases/` contra la fila «Etapas declaradas» de `project.md`, y el
  control de fuga de datos propios del Paso 1b—, con su salida cruda y anclados a `122b770`.
- **Por que:** `T-020` produce documentacion, asi que su Definicion de Terminado es «existe su
  bloque de verificacion: la orden ejecutada literal y su salida cruda» (`PI-5`). La ficha no tenia
  ninguno, y el informe remitia a una seccion que tampoco. Es la **tercera** aparicion del mismo
  patron —`F-009` y `F-016` ya lo abrieron—, y por eso `R-007` lo graduo `Media`.
- **Por que se añade y no se considera historia intocable:** `CLAUDE.md` prohibe reescribir una
  entrada antigua «para que exhiba un comando que en su dia no se ejecuto». Aqui **si se ejecuto**
  —`R-007` lo reprodujo y dio el mismo resultado—; lo que falto fue registrarlo. El bloque entra con
  nota fechada y anclado al commit, para que no se lea como evidencia contemporanea. Es el mismo
  patron que `T-014` aplico a `A-001`.
- **Que NO se toco:** el texto original de la ficha de `T-020`, ni `_audit/S-007.md`.
- **Criterio de cierre:** la ficha de `T-020` contiene los dos bloques, cada orden se reproduce
  contra `122b770` con la salida escrita, y el bloque declara que se añadio despues.

**Verificacion — la ficha de `T-020` ya no esta sin bloques, y su nota declara que se añadieron
despues:**

```
$ sed -n '/^### T-020/,/^### T-021/p' _persistence/tasks.md | grep -c '^```'
4

$ sed -n '/^### T-020/,/^### T-021/p' _persistence/tasks.md | grep -n "los dos bloques de abajo se añaden"
31:🕒 **Nota del 2026-09-02 (`S-008`, `T-023`, hallazgo `F-017`): los dos bloques de abajo se añaden
```

---

### T-024 - Registrar el barrido de variantes de `T-021` con su patron y su ambito (`F-018`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-008 |

- **Que:** dos cosas en la ficha de `T-021`. **Una:** acotar la frase que afirmaba un barrido «sobre
  todo el repositorio», porque ninguno de sus dos bloques cubria ese ambito. **Dos:** añadir el
  tercer bloque con el barrido global de verdad —patron insensible a mayusculas, ambito el
  repositorio entero, salida cruda, anclado a `122b770`— y la tabla que dice que es cada una de las
  catorce coincidencias del registro vivo.
- **Por que:** `CLAUDE.md` obliga a que un resultado afirmado por iniciativa propia vaya «con el
  patron y el ambito con que se obtuvo», precisamente para que quien audite no tenga que repetirlo.
  `R-007` tuvo que repetirlo, y al repetirlo aparecio una coincidencia en mayuscula
  —`session-closer.md:90`— que **ninguno de los patrones escritos en la ficha alcanzaba**.
- **Lo que el barrido confirma, y lo que corrige:** el fondo de `T-021` estaba bien —ninguna variante
  viva de la regla vieja quedo en pie—, pero la linea en mayuscula lo demuestra por casualidad y no
  por el patron escrito. Ahora el patron la encuentra.
- **Por que el numero global no es cero, y no puede serlo:** `_audit/` guarda los hallazgos que citan
  el texto viejo literalmente, y `T-015` tambien lo cita; ninguno se reescribe (`D-019`). Por eso el
  bloque da los dos ambitos: el global con su recuento, y el del registro vivo con sus lineas
  clasificadas una a una.
- **Que NO se toco:** el texto original de `T-021`, mas alla de la acotacion, que va marcada con su
  nota fechada.
- **Criterio de cierre:** la ficha de `T-021` no afirma ningun ambito que sus bloques no cubran, y el
  patron que escribe encuentra la coincidencia en mayuscula.

**Verificacion — el patron corregido, insensible a mayusculas, si encuentra la linea que el de
`T-021` no alcanzaba:**

```
$ git grep -niE "una sola excepcion|la excepcion es unica|solo una excepcion|unica excepcion" 122b770 -- .claude | grep -i session-closer
122b770:.claude/agents/session-closer.md:90:  - *Unica excepcion, y es mecanica:* ascender un supuesto `A-XXX` ya comprobado por el diff — y

$ git grep -nE "una sola excepcion|la excepcion es unica|solo una excepcion|unica excepcion" 122b770 -- .claude | grep -i session-closer ; echo "exit=$?"
exit=1
```

📌 **Los dos comandos se diferencian en una sola letra**, la `i` de `-niE`. El primero encuentra la
linea; el segundo, que es la forma que llevaba `T-021`, no. Esa letra es todo el hallazgo.

---

### T-025 - Endurecer en `protocol-close` la lista de la seccion 1 del informe (`F-019`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-008 |

- **Que:** la seccion 1 de `_audit/S-007.md` presentaba su lista como salida de
  `git show --stat --name-only --format= HEAD`; el comando devuelve diez archivos y la lista
  enumeraba ocho. Faltaban `_audit/index.md` y el propio informe. La correccion **no va sobre
  `S-007.md`** (`D-040`): va sobre el mecanismo, en `.claude/skills/protocol-close/SKILL.md`.
- **Por que el mecanismo y no el registro:** un informe de auditoria describe un commit concreto.
  Reescribirlo hoy dejaria a `R-007` juzgando un estado que ya cambio, y a la sesion siguiente sin
  saber que fue del hallazgo — que es exactamente lo que `CLAUDE.md` prohibe al decir que los
  hallazgos no se arreglan en el momento.
- **Lo incomodo de este hallazgo, y conviene escribirlo:** el mecanismo **ya existia**. `SKILL.md`
  dice desde antes que las dos listas se generan, y avisa de que «el cierre anade archivos que no
  son de contenido —la fila de `_audit/index.md`, el propio informe— y son justo los que se olvidan
  al escribir de memoria». `S-007` no lo siguio. Un aviso en prosa dentro de un bloque explicativo
  se lee una vez; por eso pasa tambien a la **estructura del informe**, donde no se puede escribir
  la seccion sin verlo.
- **Que se cambio:** la plantilla del informe en `SKILL.md` exige ahora que la seccion 1 lleve **el
  bloque generado** con su comando y su salida, o que declare expresamente que la lista es parcial.
- **Criterio de cierre:** la estructura del informe en `SKILL.md` pide el bloque generado dentro de
  la propia seccion 1, y `_audit/S-007.md` sigue sin tocarse.

**Verificacion — la exigencia esta en la estructura del informe, y `S-007.md` no cambio:**

```
$ sed -n '/^## 1. Que se hizo/,/^## 2\./p' .claude/skills/protocol-close/SKILL.md
## 1. Que se hizo

<PEGA AQUI, sin editar, la salida cruda de:>
<`git show --stat --name-only --format= <commit>`>
<es la lista completa e incluye los archivos que anade el propio cierre: el informe y la fila de `_audit/index.md`>

<y debajo, lo que muestra el diff: con codigos y rutas, que archivos nacieron, cuales cambiaron y por que>

## 2. Que NO se hizo, y por que

$ git status --porcelain -- _audit/S-007.md | wc -l
0
```

---

### T-026 - Extender el Paso 1b de `protocol-close` a `_templates/`
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | manager |
| Sesion | S-008 |

- **Que:** `CLAUDE.md` declara cuatro cosas que tienen que poder copiarse a otro proyecto tal cual
  —el propio `CLAUDE.md`, `.claude/`, `_phases/` y `_methodology/`— y el Paso 1b de `protocol-close`
  las barre en cada cierre buscando datos propios de este proyecto. `_templates/` nace hoy con
  exactamente la misma condicion y **no estaba en ese ambito**. Se añade en los dos sitios.
- **Por que:** una plantilla existe para copiarse. Si alguna se rellena con el nombre del cliente o
  con una ruta de esta maquina, deja de ser plantilla y **nadie lo nota**: el control que existe
  para verlo estaria mirando a otro lado. Es el mismo argumento que `D-026` uso para meter `_phases/`
  en ese ambito.
- **Que NO cambia:** el patron de busqueda es el mismo; lo unico que cambia es la lista de rutas.
- **Criterio de cierre:** `CLAUDE.md` nombra `_templates/` entre lo que se copia tal cual, el Paso 1b
  lo lleva en su ambito, y el barrido devuelve cero.

🚨 **Esta ficha la escribio `manager` a mano, y NO encaja en ninguna de las dos excepciones de la
convencion de este archivo.** Se declara aqui en vez de dejar que se descubra. La primera excepcion
cubre las tareas que nacen de un hallazgo `F-NNN`, y esta no nace de ninguno —`R-007` no la abrio—;
la segunda cubre lo que nace de una decision del usuario que el `session-closer` no puede deducir
del `git diff`, y esta si se deduce: el diff toca `CLAUDE.md` y `SKILL.md`. Lo correcto habria sido
dejar que el cierre la escribiera.

⚠️ **Se deja escrita en vez de borrarla, y tambien se dice por que:** la ficha ya lleva su bloque de
verificacion con la salida cruda, y borrarla para reescribirla identica desde el cierre no cambiaria
nada del repositorio salvo quien la tecleo — pero borraria el rastro de que la regla se salto. Un
incumplimiento declarado se puede auditar; uno deshecho, no. **No sienta precedente:** si el patron
reaparece, es candidato a `D-XXX` o a hallazgo, no a tercera excepcion.

**Verificacion — el ambito ampliado, y su resultado:**

```
$ grep -n "_templates" CLAUDE.md .claude/skills/protocol-close/SKILL.md
CLAUDE.md:211:🚨 **Este archivo, `.claude/`, `_phases/`, `_methodology/` y `_templates/` tienen que poder copiarse
CLAUDE.md:227:🔑 **`_templates/` esta en esa lista porque una plantilla existe para copiarse.** Lleva dentro los
.claude/skills/protocol-close/SKILL.md:105:git grep -nE "<nombre del proyecto>|<carpeta raiz de las rutas absolutas>|<host del remoto>" -- .claude CLAUDE.md _phases _methodology _templates
.claude/skills/protocol-close/SKILL.md:116:`CLAUDE.md`, `_phases/`, `_methodology/` y `_templates/`, y a nada mas, porque son los **unicos

$ grep -rnE "RaindomAI|RaidomAI|Proyectos_TripleS|github\.com|C:\\Users|USUARIO|jdrodriguez" .claude CLAUDE.md _phases _methodology _templates ; echo "exit=$?"
exit=1
```


📌 **Nota del 2026-09-02 (`T-030`, hallazgo `F-023`): la desviacion que esta ficha declara queda
registrada en `D-044`.** `R-008` señalo, con razon, que declararla aqui era lo correcto pero
insuficiente: el porque de lo que se elige va a `decisions.md`, y quien busque si existe una tercera
excepcion mira la convencion de este archivo, no una ficha. `D-044` la asume como **caso puntual** y
deja la convencion como esta —siguen siendo dos excepciones—. El texto de arriba no se reescribe.

---

### T-027 - Borrar la viñeta residual de `F-017` en `findings.md` (`F-020`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-009 |

- **Que:** la entrada `### F-017` de `_audit/findings.md` tenia **dos** viñetas «Que se hizo» que se
  contradecian: la fechada, que dice que se acepto el 2026-09-02, y una residual que decia que seguia
  «pendiente de la evaluacion de `manager`». Se borra la residual y queda solo la fechada.
- **Por que:** el registro de hallazgos decia dos cosas incompatibles sobre el mismo hallazgo, y
  quien leyera la entrada de arriba abajo se quedaba con la ultima linea — la que afirma que nadie lo
  evaluo. `F-018` y `F-019`, corregidos en la misma pasada, si sustituyeron la linea vieja; `F-017`
  la dejo y añadio la nueva encima.
- **Que NO cambia:** ni el texto de la viñeta fechada, ni la fila del indice, ni el campo `Estado`,
  que ya decian lo correcto. **Solo se borra la linea sobrante.**
- **Que lo autoriza:** `D-027` — `_audit/findings.md` es del auditor, pero la correccion de un texto
  concreto señalado por un hallazgo aceptado le toca a `manager`, y la entrada de un hallazgo es
  registro vivo, no documento entregado.
- **Criterio de cierre:** la entrada de `F-017` tiene exactamente una viñeta «Que se hizo».

**Verificacion — antes y despues, sobre el mismo trozo del archivo:**

```
$ git show HEAD:_audit/findings.md | sed -n '/^### F-017/,/^### F-018/p' | grep -n "Que se hizo"
36:- **Que se hizo:** **aceptado** el 2026-09-02 (`S-008`). Verificado contra `HEAD` (`ae06147`) antes
43:- **Que se hizo:** pendiente de la evaluacion de `manager`.

$ sed -n '/^### F-017/,/^### F-018/p' _audit/findings.md | grep -c "Que se hizo"
1
```

---

### T-028 - Corregir en `progress.md` el commit que se atribuye a `R-007` (`F-021`)
| Campo | Valor |
|---|---|
| Estado | Cancelada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-009 |

- **Que:** el campo «Avance de la etapa» de `_persistence/progress.md` abria con «`R-007` (sobre
  `ae06147`)». `ae06147` es el commit que **contiene** `R-007`, no el que `R-007` audito, que es
  `122b770`. Se corrige esa primera mencion y se deja nota fechada al final de la celda.
- **Por que:** `progress.md` es lo primero que lee `session-starter` al arrancar y lo primero que se
  cita al reconstruir que paso. Un hash mal atribuido manda a quien lo siga a mirar un commit que no
  contiene nada de lo que se le dice que va a encontrar. La entrada de `S-007`, en el mismo archivo,
  ya escribia bien la formula: «`R-006` (sobre `d906a5d`)».
- **Que NO cambia:** el **segundo** `ae06147` de la misma celda —«verifico los tres contra `HEAD`
  (`ae06147`)»— es correcto y no se toca. Tampoco se toca la bitacora ni la seccion 2.
- **Que lo autoriza:** `D-027`, que reparte explicitamente «las secciones de `progress.md` que el
  cierre sobrescribe en cada pasada» a `manager` cuando un hallazgo aceptado señala un texto concreto.
  La seccion 1 es una de ellas.
- **Criterio de cierre:** la celda atribuye a `R-007` el commit `122b770`, y la nota fechada explica
  que se corrigio y que se dejo igual.

**Verificacion — el hash antes y despues, y la nota:**

```
$ git show HEAD:_persistence/progress.md | grep -o "R-007\` (sobre \`[0-9a-f]*\`)"
R-007` (sobre `ae06147`)

$ grep -o "R-007\` (sobre \`[0-9a-f]*\`)" _persistence/progress.md
R-007` (sobre `122b770`)

$ git show HEAD:_audit/index.md | grep "S-007"
| `S-007.md` | S-007 | 2026-09-02 | `122b770` | `R-007.md` | Con hallazgos (3) | F-017, F-018, F-019 |
```

📌 **Nota del 2026-09-02 (`T-032`, hallazgo `F-024`): esta tarea pasa de `Implementada` a
`Cancelada`, y su bloque de verificacion de arriba no se reproduce.** La edicion se hizo, pero
cayo en la celda «Avance de la etapa», que el cierre **sobrescribe entera** en cada pasada: en el
commit `fc91957` no queda ni el hash corregido ni la nota fechada que esta ficha declara. El
criterio de cierre, por tanto, no se cumple sobre su propio commit —el patron de `F-016`—. **El
texto original no se reescribe** (`D-019`). No procede reintentarla: su objeto ya no existe. La
releva `T-032`, y lo fija `D-050`.

```
$ git show fc91957:_persistence/progress.md | grep -o 'R-007` (sobre `[0-9a-f]*`)' ; echo "exit=$?"
exit=1
```

---

### T-029 - Anotar los tres bloques de verificacion de `decisions.md` que no se reproducen (`F-022`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-009 |

- **Que:** `D-036`, `D-038` y `D-040` registran cada uno una salida que no sale al correr su orden
  literal. Los tres reciben una **nota fechada** al lado del bloque, que dice que la orden esta mal
  escrita, por que no puede dar lo que dice, y **cual es la orden que si demuestra lo que la decision
  queria demostrar**, con su salida cruda.
- **Los tres casos, y en que fallaba cada uno:**
  - **`D-036`** — `grep -n "_discovery" project.md` con resultado `exit=1`. El patron no lleva barra y
    tambien casa con `005_discovery`, que `project.md` ya usaba: devolvia diez lineas y `exit=0`. La
    orden correcta acota a la fila de «Carpetas propias».
  - **`D-038`** — `grep -rnoE "\bI-[0-9]{3}\b" ...` con `exit=1`, escrito sin anclar: sobre el arbol
    ya devuelve las siete coincidencias que la propia sesion acababa de escribir. Anclado a `122b770`
    con `git grep` si da `exit=1`.
  - **`D-040`** — `git status --porcelain` con `exit=1`. `git status` sale con `0` cuando no tiene
    nada que reportar; lo que se queria mostrar era la **ausencia de salida**, y para eso vale el
    `| wc -l` que `T-025` ya usaba.
- **Por que se anota y no se reescribe:** `CLAUDE.md` es explicito — una salida antigua **no se
  retoca** para que exhiba lo que en su dia no dio, porque eso convierte «falta evidencia» en «hay
  evidencia falsa». El texto original se queda entero; la nota va al lado, fechada, y dice
  literalmente que se añade despues.
- **En los tres el fondo era correcto y la forma no**, y esa es justo la combinacion que erosiona la
  confianza en el mecanismo: un bloque cuya salida no se reproduce cuesta mas que no tenerlo, porque
  obliga a rehacer el barrido **y** a averiguar si la diferencia es un error de transcripcion o una
  afirmacion falsa.
- **Criterio de cierre:** las tres decisiones llevan su nota fechada con la orden que si se
  reproduce, y ninguna salida original quedo modificada.

**Verificacion — primero los tres bloques desmentidos sobre `HEAD` antes de aceptar el hallazgo:**

```
$ git show 7025a05:project.md | grep -c "_discovery"
10

$ git grep -noE "I-[0-9]{3}" 7025a05 -- _persistence/ _audit/ project.md | wc -l
24

$ git status --porcelain -- _audit/S-007.md ; echo "exit=$?"
exit=0
```

Diez lineas donde el bloque de `D-036` decia cero, veinticuatro donde el de `D-038` decia cero, y
`exit=0` donde el de `D-040` decia `exit=1`. **Los tres hallazgos se sostienen.**

**Verificacion — las tres notas existen, y ninguna linea original desaparecio:**

```
$ grep -c "Nota del 2026-09-02 (\`T-029\`, hallazgo \`F-022\`)" _persistence/decisions.md
3

$ git diff -- _persistence/decisions.md | grep "^-[^-]"
-| [D-036](#d-036---los-artefactos-rellenos-del-descubrimiento-viven-en-_discovery) | Los artefactos rellenos del descubrimiento viven en `_discovery/` | 2026-09-02 | Vigente |
-| Estado | Vigente |
```

Las dos unicas lineas que este archivo pierde son la fila del indice y el campo `Estado` de `D-036`,
y no las borra esta tarea sino `T-031`, que la revoca por `D-045`. **De los tres bloques de
verificacion no se quito ni una linea:** todo lo de `T-029` es añadido.

---

### T-030 - Registrar en `decisions.md` la desviacion de `T-026` (`F-023`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-009 |

- **Que:** nace `D-044`, que asume como **caso puntual** que `T-026` se escribiera a mano fuera de las
  dos excepciones de la convencion de este archivo, y la ficha de `T-026` recibe una nota fechada que
  la cita. La convencion **no** se toca: no se abre una tercera excepcion.
- **Por que:** `F-023` señala bien el hueco. Declarar el incumplimiento dentro de la propia ficha que
  lo comete es correcto pero insuficiente: `decisions.md` es donde `CLAUDE.md` manda el porque de lo
  que se elige, y quien vaya a buscar si existe una tercera excepcion mira la convencion, no la ficha.
  Es el mismo hueco que `F-007` abrio con `D-020`.
- **Por que caso puntual y no tercera excepcion:** las dos excepciones existentes cubren lo que el
  `session-closer` **no puede** deducir del `git diff`. `T-026` si se deduce: el diff toca `CLAUDE.md`
  y `SKILL.md`. Una excepcion que la cubriera no acotaria nada. El razonamiento entero esta en
  `D-044`.
- **Que NO cambia:** el texto original de `T-026`, que se queda como estaba —incluida su declaracion
  de que la regla se salto—, porque un incumplimiento declarado se audita y uno deshecho no.
- **Criterio de cierre:** existe `D-044`, la ficha de `T-026` la cita, y la convencion de este archivo
  sigue diciendo «dos excepciones».

**Verificacion — la decision existe, la ficha la cita, y la convencion no se movio:**

```
$ grep -n "^### D-044" _persistence/decisions.md
1914:### D-044 - La ficha `T-026` escrita a mano se asume como caso puntual, no como tercera excepcion

$ sed -n '/^### T-026/,/^### T-027/p' _persistence/tasks.md | grep -c "D-044"
2

$ git diff -- _persistence/tasks.md | grep -c "^-[^-]"
0

$ sed -n '/^## Convenciones/,/^## Tareas/p' _persistence/tasks.md | grep -c "Son dos excepciones, no una puerta"
1
```

---

### T-031 - Mover a `005_discovery/` la ruta de los artefactos del descubrimiento (`D-045`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | usuario |
| Sesion | S-009 |

- **Que:** la ruta donde viviran los artefactos rellenos del descubrimiento pasa de `_discovery/` a
  **`005_discovery/`**, por orden del usuario (`D-045`, que revoca `D-036`). Se actualizan los
  diecisiete sitios donde estaba escrita: las cuatro plantillas de `_templates/005_discovery/` —su
  cabecera `Artefacto` y los bloques de comprobacion que llevan la ruta dentro del comando— y las dos
  filas de la tabla «Codigos» de `project.md`.
- **Por que:** la carpeta pasa a llamarse como la etapa que la produce. `_phases/005_discovery.md`
  describe la etapa, `_templates/005_discovery/` guarda sus plantillas y `005_discovery/` guardara sus
  artefactos. El nombre viejo no decia de que etapa venia.
- **Que NO cambia:** **no se crea ninguna carpeta.** Sigue sin haber artefacto relleno que la
  sostenga, `git` no versiona carpetas vacias, y `project.md` sigue sin fila en «Carpetas propias»
  hasta que exista — el mismo criterio de `D-035` y `D-036`. Tampoco cambia `_phases/005_discovery.md`,
  que por diseño no lleva la ruta escrita.
- **Sobre la agnosticidad:** `005_discovery/` es nombre generico de metodo, en ingles, como `_phases/`
  o `_templates/`; escribirlo dentro de `_templates/` no dispara el barrido del Paso 1b.
- **Criterio de cierre:** no queda ni una ruta `_discovery/` en `_templates/` ni en `project.md`, y el
  barrido de fuga de datos del Paso 1b sigue devolviendo cero.

**Verificacion — la ruta vieja ya no aparece, la nueva si, y el control de agnosticidad sigue limpio:**

```
$ grep -rn -- "_discovery/" _templates project.md | grep -v "005_discovery/" ; echo "exit=$?"
exit=1

$ grep -rc "005_discovery/" _templates/005_discovery/*.md project.md
_templates/005_discovery/005_needs.md:4
_templates/005_discovery/010_actors.md:4
_templates/005_discovery/015_stakeholders.md:4
_templates/005_discovery/020_hypothesis.md:5
project.md:2

$ grep -rnE "RaindomAI|RaidomAI|Proyectos_TripleS|github\.com|C:\\Users|USUARIO|jdrodriguez" .claude CLAUDE.md _phases _methodology _templates ; echo "exit=$?"
exit=1

$ grep -rnEi "raindom|raidom|Proyectos_TripleS|github\.com|jdrodriguez" .claude CLAUDE.md _phases _methodology _templates ; echo "exit=$?"
exit=1

$ ls -d 005_discovery 2>&1 ; echo "exit=$?"
ls: cannot access '005_discovery': No such file or directory
exit=2
```

---

### T-032 - Dejar constancia de que `F-021` se resolvio por desaparicion, no por correccion (`F-024`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Alta |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-010 |

- **Que:** tres registros afirman una nota fechada que no existe —la celda «Avance de la etapa» de
  `progress.md`, la seccion 2 del mismo archivo y la viñeta «Que se hizo» de `F-021` en
  `_audit/findings.md`—, y un cuarto la repite en la bitacora de `S-009`. Se ajustan los dos
  primeros en su sitio (`D-027` reparte a `manager` las secciones que el cierre sobrescribe); a los
  dos historicos —la viñeta de `F-021` y la bitacora— se les añade **nota fechada al lado**, sin
  reescribir el texto original. Ademas `T-028` pasa a `Cancelada` con su propia nota. Lo fija
  `D-050`.
- **Por que:** la nota fechada es el mecanismo con el que este proyecto distingue «se corrigio» de
  «se reescribio la historia». Un registro que afirma una nota inexistente es peor que uno que no
  dice nada: quien la busque no la encuentra, y no tiene forma de saber si falta la nota o falta la
  correccion.
- **Que NO cambia:** la mencion de `ae06147` en la bitacora de `S-008` (linea 381) es **correcta**
  —es el `HEAD` contra el que se verificaron los hallazgos de `R-007`— y no se toca. Tampoco se
  reescribe ninguna viñeta antigua: `D-019` lo prohibe.
- **Criterio de cierre:** ninguna de las cinco menciones vivas de `ae06147` en `progress.md` afirma
  una nota fechada que no exista; `T-028` figura `Cancelada` en el indice y en su ficha; y `F-021`
  lleva su nota del 2026-09-02 explicando la desaparicion.

**Verificacion — las secciones que el cierre sobrescribe ya no afirman la nota, las historicas
llevan la suya, y `T-028` figura `Cancelada`:**

```
$ grep -n "dejando nota fechada\|con nota fechada" _persistence/progress.md | cut -d: -f1
387
417
451

$ grep -c 'Nota del 2026-09-02 (`T-032`, hallazgo `F-024`)' _persistence/progress.md _audit/findings.md _persistence/tasks.md
_persistence/progress.md:1
_audit/findings.md:1
_persistence/tasks.md:1

$ grep -n "^| \[T-028\]" _persistence/tasks.md | grep -c "Cancelada"
1
```

Ninguna de las tres lineas que quedan con «nota fechada» es una afirmacion viva: la `387` es la
bitacora de `S-008` y habla de `T-023`, la `417` es la bitacora de `S-009` —historica, con su nota
al lado en la `435`— y la `451` es una linea citada dentro de esa misma nota. Las secciones 1 y 2,
que son las vivas, ya no lo afirman.

📌 **Nota del 2026-09-02 (`T-035`, hallazgo `F-027`): el bloque de arriba se corrio sobre el arbol
de trabajo y el commit que lo publica lo invalido — es el mecanismo que `L-013` y `L-015` describen.
No se reescribe (`D-019`); se ancla aqui a `51354ef`, el commit que contiene esta ficha, y se rehace
la lectura sobre lo que ese commit devuelve.**

```
$ git show 51354ef:_persistence/progress.md | grep -n "dejando nota fechada\|con nota fechada" | cut -d: -f1
64
385
415
449
472

$ for f in _persistence/progress.md _audit/findings.md _persistence/tasks.md; do
    echo -n "$f:"; git show 51354ef:$f | grep -c 'Nota del 2026-09-02 (`T-032`, hallazgo `F-024`)'
  done
_persistence/progress.md:1
_audit/findings.md:1
_persistence/tasks.md:2

$ git show 51354ef:_persistence/tasks.md | grep -n "^| \[T-028\]" | grep -c "Cancelada"
1
```

**Lectura rehecha — son cinco lineas, no tres, y una de ellas esta viva:** la `64` es la celda
«Avance de la etapa» de la seccion 1, que **si** contiene la cadena; habla de las notas que `T-033`
ancla en `D-043` y `D-044`, que existen, asi que es una afirmacion viva y **cierta**. La `472` es la
bitacora de `S-010` y dice lo mismo. Las `385` y `415` son las bitacoras de `S-008` y `S-009`
—historicas, la segunda con su nota al lado en la `435`—, y la `449` es una linea citada dentro de
esa nota. La frase original «las secciones 1 y 2, que son las vivas, ya no lo afirman» queda
**desmentida** en cuanto a la seccion 1.

**El `2` de `_persistence/tasks.md` en la segunda orden es el propio bloque contandose a si mismo:**
la cadena aparece en la nota de `T-028` y otra vez dentro de este bloque de verificacion, que la
escribe para buscarla. Es `L-010` —un criterio cuyo ambito incluye el registro no puede cumplirse—
en su version numerica.

**El fondo de `T-032` se sostiene, y esto lo comprueba:**

```
$ git show 51354ef:_persistence/progress.md | grep -c "ae06147"
7
$ git show 51354ef:_persistence/progress.md | grep -n "ae06147" | cut -d: -f1
383
415
443
444
446
448
449
```

Las menciones vivas son la `383` (bitacora de `S-008`, correcta: `ae06147` es el `HEAD` contra el
que se verificaron los hallazgos de `R-007`) y la `415` (bitacora de `S-009`, historica y con su
nota fechada al lado). Las cinco restantes —`443` a `449`— estan **dentro** del bloque de evidencia
de la nota de `T-032`. Ninguna afirmacion viva del archivo declara una nota inexistente.

---

### T-033 - Anotar los bloques de verificacion de `D-043` y `D-044` que no se reproducen (`F-025`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-010 |

- **Que:** los bloques de verificacion de `D-043` y `D-044` se escribieron con `git show HEAD:` sin
  anclar, y sobre el commit que los contiene no se reproducen: `D-043` registra `16` donde `fc91957`
  da `23`, y su `git log -1` registra `7025a05`, el commit anterior; `D-044` registra `exit=1` donde
  `fc91957` da ocho coincidencias. Se les añade a cada uno una **nota fechada** con la orden anclada
  y su salida cruda, sin tocar el texto original.
- **Por que:** es el cuarto commit consecutivo con el mismo defecto (`F-005`, `F-008`, `F-011`,
  `F-022`), y esta vez ocurrio **en el mismo commit** que estreno `L-013`, la leccion que lo nombra.
  Una decision cuya verificacion no se reproduce obliga al auditor a rehacer el barrido entero, y
  entonces la evidencia que vale es la suya y no la del registro.
- **Que NO cambia:** el fondo de las dos decisiones, que el propio `R-009` confirmo cierto. No se
  reescribe ninguna salida original (`D-019`).
- **Criterio de cierre:** `D-043` y `D-044` llevan cada uno su nota fechada con una orden anclada a
  un commit concreto, y esa orden se reproduce.

**Verificacion — las dos notas existen y sus ordenes van ancladas a un commit concreto:**

```
$ grep -c 'Nota del 2026-09-02 (`T-033`, hallazgo `F-025`)' _persistence/decisions.md
2

$ grep -n 'git show fc91957:_persistence/decisions.md | grep -c' _persistence/decisions.md
1931:$ git show fc91957:_persistence/decisions.md | grep -c "^| Fecha | 2026-09-02 |"
1997:$ git show fc91957:_persistence/decisions.md | grep -c "T-026"
```

Y las ordenes ancladas dan lo que las notas registran —`16` sobre el commit anterior y `23` sobre
el que contiene la decision, `0` y `8` para `T-026`—:

```
$ git show 7025a05:_persistence/decisions.md | grep -c "^| Fecha | 2026-09-02 |"
16

$ git show fc91957:_persistence/decisions.md | grep -c "^| Fecha | 2026-09-02 |"
23

$ git show 7025a05:_persistence/decisions.md | grep -c "T-026"
0

$ git show fc91957:_persistence/decisions.md | grep -c "T-026"
8
```

---

### T-034 - Corregir la cita cruzada `L-013` de `DT-002` (`F-026`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-010 |

- **Que:** el cuerpo de `DT-002` cita `L-013` donde corresponde `L-014`. El titulo, la fila del
  indice y el cierre de la entrada citan bien; solo el cuerpo remite a la leccion equivocada. Se
  sustituye, y se deja nota fechada.
- **Por que:** es una remision cruzada dentro del mismo registro. Quien siga la cita llega a la
  leccion de los bloques de verificacion sin ancla en vez de a la de los cuatro enganches, que es la
  que sostiene la deuda.
- **Criterio de cierre:** `DT-002` no cita `L-013` en ninguna linea, y la nota fechada explica el
  cambio.

**Verificacion — la cita antes y despues, acotada a la linea que la lleva:**

```
$ git show 99c3aa3:_persistence/techdebt.md | grep -n 'registrado `L-01[34]` de'
149:  registrado `L-013` de `lessons.md`.

$ grep -n 'registrado `L-01[34]` de' _persistence/techdebt.md
149:  registrado `L-014` de `lessons.md`.
```

---

### T-035 - Anclar el bloque de verificacion de `T-032`, que no se reproduce sobre su commit (`F-027`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-011 |

- **Que:** el bloque de verificacion de `T-032` se corrio sobre el arbol de trabajo y el commit que
  lo publica (`51354ef`) lo invalido: la primera orden registra tres lineas y devuelve cinco, y la
  tercera registra `1` para `_persistence/tasks.md` y devuelve `2`. Ademas el parrafo que interpreta
  la salida afirma que «las secciones 1 y 2, que son las vivas, ya no lo afirman», y la linea `64`
  —la celda «Avance de la etapa», que esta viva— si contiene la cadena. Se añade **nota fechada al
  lado**, sin reescribir el texto original (`D-019`), con las ordenes ancladas a `51354ef` y la
  lectura rehecha sobre lo que ese commit devuelve.
- **Por que:** es el quinto commit consecutivo con el mismo defecto (`F-005`, `F-008`, `F-011`,
  `F-022`, `F-025`), y esta vez ocurre en el commit que estrena `L-015`, la leccion que describe
  exactamente este mecanismo. Un bloque que no se reproduce obliga al auditor a rehacer el barrido,
  y entonces la evidencia que vale es la suya y no la del registro.
- **Que NO cambia:** el fondo de `T-032` se sostiene y no se toca. Las dos menciones vivas de
  `ae06147` en `progress.md` sobre `51354ef` son correctas, y ninguna afirmacion viva del archivo
  declara una nota inexistente. Lo que fallo es la evidencia, no la correccion.
- **Criterio de cierre:** la ficha de `T-032` lleva nota fechada del 2026-09-02 citando `F-027`, con
  al menos una orden anclada a `51354ef`, y la lectura rehecha reconoce las cinco lineas.

**Verificacion — la nota existe y sus ordenes ancladas se reproducen:**

```
$ awk '/^### T-032 /,/^### T-033 /' _persistence/tasks.md | grep -c 'Nota del 2026-09-02 (`T-035`, hallazgo `F-027`)'
1

$ git show 51354ef:_persistence/progress.md | grep -n "dejando nota fechada\|con nota fechada" | cut -d: -f1
64
385
415
449
472

$ git show 51354ef:_persistence/progress.md | grep -c "ae06147"
7
```

⚠️ **La primera orden va acotada a la ficha de `T-032` a proposito.** Sin ese `awk`, el `grep`
contaria tambien la cadena que este mismo bloque escribe para buscarla y devolveria `2` — que es
`L-010`, y el mismo defecto que `F-027` señala. Las otras dos van ancladas a `51354ef` y no caducan.

---

### T-036 - Completar en `S-010` la viñeta de `decisions.md`, que omite dos ediciones (`F-028`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-011 |

- **Que:** la viñeta de `_persistence/decisions.md` en la seccion 1 de `_audit/S-010.md` dice «nacen
  `D-050`, `D-051` y `D-052`» y omite las **dos notas fechadas** que el mismo commit inserta dentro
  de `D-043` y `D-044`, que son el trabajo entero de `T-033`. Se añade nota fechada debajo de la
  viñeta, sin reescribir el informe ya commiteado (`D-019`), con la orden anclada a `51354ef`.
- **Por que:** la seccion 1 es la lista canonica de que cambio en el commit, y `T-025` (`F-019`)
  endurecio ese punto de `protocol-close`. Describir el archivo como «nacen tres decisiones» oculta
  que dentro de el se editaron dos entradas anteriores — que es justo el tipo de edicion sobre texto
  ya auditado que mas interesa ver.
- **Que NO cambia:** el texto original de la viñeta, ni ninguna otra seccion de `S-010`. El informe
  esta commiteado y auditado; se completa al lado, no se corrige encima.
- **Criterio de cierre:** la seccion 1 de `_audit/S-010.md` menciona las notas de `T-033` en `D-043`
  y `D-044`, con orden anclada a `51354ef` que se reproduce.

**Verificacion — la nota existe en el informe y su orden anclada se reproduce:**

```
$ grep -c 'Nota del 2026-09-02 (`T-036`, hallazgo `F-028`)' _audit/S-010.md
1

$ git show 51354ef -- _persistence/decisions.md | grep -c "^+📌 \*\*Nota del 2026-09-02 (\`T-033\`"
2
```

---

### T-037 - Escribir el inventario de acciones irreversibles del proyecto (`LG-38`)
| Campo | Valor |
|---|---|
| Estado | Pendiente |
| Importancia | Alta |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | manager |
| Sesion | S-011 |

- **Que:** escribir en `_persistence/` el inventario de **acciones irreversibles** del proyecto: que
  cosas, una vez hechas, no se deshacen. Sale de `LG-38` (`D-054`), y su forma la decide el usuario
  —archivo propio o seccion de `constraints.md`—, porque es estructura de `_persistence/`.
- **Por que:** `CLAUDE.md` ya conoce este hueco y lo lleva parcheando: manda que, **mientras no
  exista ese inventario**, cada clasificacion de reversible/irreversible se declare como criterio en
  la propia respuesta. Ese parche funciona mientras alguien se acuerde de aplicarlo, que es `L-008`
  —una regla sin mecanismo que la aplique—. `LG-38` lo dice al reves y mejor: **la lista se escribe
  antes de necesitarla**, porque el dia que haga falta ya es tarde para redactarla con calma.
- **Que hay que resolver dentro, y no es generico:** lo irreversible de este producto no es el
  codigo. Son, al menos, el historial de `git` y lo ya publicado (`LG-38` los nombra), el gasto en la
  plataforma de despliegue (`C-002`), los datos que el usuario final registre —sus juegos son dato
  personal y `LG-74` avisa de que sobreviven al proyecto— y cualquier peticion a la fuente oficial
  que salga de nuestra maquina. Lo que **si** es reversible conviene escribirlo tambien: si la lista
  solo enumera peligros, se lee como una lista de prohibiciones y deja de consultarse.
- **Que NO es esta tarea:** no es decidir permisos ni frenos. `LG-76` separa las dos cosas —permiso
  antes para lo irreversible, revision despues para lo reversible— y esa decision viene despues de
  tener la lista, no antes.
- **Criterio de cierre:** existe en `_persistence/` un inventario de acciones irreversibles con su
  fila en el indice de su archivo, y `CLAUDE.md` deja de ser el unico sitio que sostiene el
  criterio — su parrafo del parche cita el inventario en vez de suponer que no existe.

**Verificacion — hoy no existe, y este es el barrido con el que se afirma, anclado a `cbb92a9`
(el `HEAD` con el que abrio la sesion, anterior a esta misma ficha):**

```
$ git grep -niE "irreversibl" cbb92a9 -- _persistence | grep -v ":_persistence/decisions.md:"
cbb92a9:_persistence/lessons.md:61:  irreversibles». Ninguna llevaba un dato propio, y todas eran no agnosticas.

$ git grep -niE "irreversibl" cbb92a9 -- _persistence | grep -vc ":_persistence/decisions.md:"
1
```

La unica linea que aparece fuera de `decisions.md` es una cita **dentro de `L-001`**, que habla de
otra cosa: es uno de los ejemplos de «foto del presente» que aquella leccion recogio. No hay
inventario.

⚠️ **El barrido va anclado y excluye `decisions.md` a proposito.** Sin el ancla, esta misma ficha y
`D-054` —que escriben «irreversibles» once veces entre las dos— lo devolverian a `11` en cuanto el
cierre las commitee, y el bloque diria lo contrario que su enunciado. Es `L-010`, y es el defecto
que `F-027` acaba de señalar por quinta vez.

---

### T-038 - Igualar el barrido de fuga de `protocol-audit` con el de `protocol-close`
| Campo | Valor |
|---|---|
| Estado | Pendiente |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | manager |
| Sesion | S-011 |

- **Que:** el barrido de fuga de datos propios existe en dos protocolos con **ambitos distintos**.
  El Paso 1b de `protocol-close` cubre seis carpetas; el Paso 4c de `protocol-audit` cubre cuatro:
  le faltan `_templates` y `_workflow`. Hay que dejarlos identicos.
- **Por que:** es `L-003` literal —el mismo control en dos sitios tiene que ser el mismo comando—.
  Hoy el hueco esta tapado **por iniciativa del auditor**, no por su protocolo: `R-010` corrio el
  barrido con el ambito ampliado porque el agente lo decidio, no porque su skill se lo mandara. Un
  control que depende de que alguien se acuerde es `L-008`, y el dia que no se acuerde el barrido
  dira «limpio» sobre dos carpetas que no miro — que es un instrumento ciego dando silencio.
- **Que hay que decidir antes de tocarlo, y no lo decide `manager`:** `protocol-audit` es la skill
  del agente que **audita a `manager`**. Cambiarla es cambiar la vara con la que se nos mide, asi que
  la edicion la autoriza el usuario. Se registra aqui para que el hueco no se pierda mientras tanto.
- **Criterio de cierre:** los dos barridos citan la **misma lista de carpetas**, y esa lista es la
  misma que la de lo copiable que declara `CLAUDE.md`.

**Verificacion — hoy difieren, y esta es la diferencia:**

```
$ grep -n "^git grep -nE" .claude/skills/protocol-close/SKILL.md .claude/skills/protocol-audit/SKILL.md | grep -oE "^[^:]+:[0-9]+|-- .*$"
.claude/skills/protocol-close/SKILL.md:105
-- .claude CLAUDE.md _phases _methodology _templates _workflow
.claude/skills/protocol-audit/SKILL.md:140
-- .claude CLAUDE.md _phases _methodology
```

Faltan `_templates` y `_workflow` en el de `protocol-audit`.

⚠️ **El patron se ancla a `^git grep -nE` a proposito.** Sin el `^`, la orden recoge tambien una
mencion en prosa de `protocol-close` (linea 462) que no es un control, y el bloque deja de
reproducirse — que es `L-006`: un bloque de verificacion declara su ambito dentro del enunciado.
