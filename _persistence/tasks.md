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
existente —«usuario, pero por escrito», «auditor, pero de otra pasada»— no es un valor nuevo: va
en el cuerpo de la tarea. Si el criterio se cumple, el valor entra **en esta tabla en la misma
pasada** en que se escribe la primera tarea que lo usa, con su `D-XXX`.

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
