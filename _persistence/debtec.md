# debtec.md

> Registro de la **deuda tecnica** del proyecto: atajos conscientes, soluciones provisionales
> y pendientes de calidad. Cada item tiene codigo `DT-XXX`, estado, importancia y urgencia.
> La deuda se registra en el momento en que se contrae.

---

## Indice

| Codigo | Deuda tecnica | Estado | Confirmacion | Importancia | Urgencia |
|---|---|---|---|---|---|
| [DT-001](#dt-001---debtecmd-incumple-la-regla-de-nombres-en-ingles) | `debtec.md` incumple la regla de nombres en ingles | No implementada | Propuesta (pendiente del usuario) | Baja | No bloqueante |

---

## Convenciones

| Campo | Valores posibles |
|---|---|
| Codigo | `DT-XXX`, correlativo, no se reutiliza |
| Estado | `Implementada` / `No implementada` / `Cancelada` / `Suspendida` |
| Importancia | `Alta` / `Media` / `Baja` |
| Urgencia | `Bloqueante` / `No bloqueante` |
| Origen | `usuario` / `manager` / `report_auditor` |
| Confirmacion | `Confirmada` / `Propuesta (pendiente de <quien>)` |

`Implementada` = la deuda ya fue pagada (corregida). `No implementada` = sigue pendiente de pago.

🚨 **`Confirmacion` y `Estado` son ejes distintos, y por eso son dos campos.** `Estado` dice si la
deuda **se pago**; `Confirmacion` dice si **es deuda**. Una entrada puede estar confirmada y sin
pagar —lo normal— pero tambien propuesta y sin confirmar: alguien la detecto y nadie ha dicho
todavia que el atajo fuera un atajo.

🚨 **`Propuesta` lleva dueno dentro del valor, siempre.** No existe `Propuesta` a secas: quien
confirma va escrito (`Propuesta (pendiente del usuario)`), porque una propuesta sin dueno no espera
—se queda propuesta para siempre—. Si no sabes quien confirma, entonces lo que falta no es la
confirmacion: es saber de quien es la decision, y eso es una `T-XXX`.

⚠️ **El caracter provisional va en el indice, no solo en el detalle.** El ojo entra por la tabla de
arriba; una entrada `Propuesta` que en el indice se ve igual que una confirmada es, en la practica,
una confirmada.

⚠️ **El titulo de una deuda nombra el defecto, y no cambia al pagarla.** Al pasar a `Implementada`,
lo que se fecha es el cuerpo —«🕐 estado al AAAA-MM-DD, ya corregido»— para que no siga hablando en
presente de algo ya resuelto.

🚨 **El indice se escribe a mano, sin generador.** Cada fila enlaza por ancla a su deuda.

---

## Deuda registrada

<!--
Plantilla:

### DT-XXX - Titulo
| Campo | Valor |
|---|---|
| Estado | No implementada |
| Confirmacion | |
| Importancia | |
| Urgencia | |
| Origen | |
| Fecha | AAAA-MM-DD |

- **Deuda:** que atajo se tomo.
- **Por que se tomo:** que se gano a cambio.
- **Costo de no pagarla:** que pasa si se queda.
- **Como se paga:** que habria que hacer.
-->

### DT-001 - `debtec.md` incumple la regla de nombres en ingles
| Campo | Valor |
|---|---|
| Estado | No implementada |
| Confirmacion | Propuesta (pendiente del usuario) |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Origen | usuario |
| Fecha | 2026-08-31 |

- **Deuda:** `D-017` fija que los nombres de archivos y carpetas van en ingles. `debtec.md`
  —abreviatura de «deuda tecnica»— es el unico archivo trackeado que no cumple. Se deja como esta.
- **Por que se tomo:** la regla se decidio con efecto **hacia adelante**. Renombrar obligaria a
  tocar sus referencias en los tres skills, en los agentes, en `project.md` y en `CLAUDE.md`, sobre
  un estado que la auditoria `R-001` ya dio por bueno; el beneficio es de coherencia, no funcional.
- **Costo de no pagarla:** el registro exhibe una excepcion a su propia regla. Mientras este
  escrita aqui es una excepcion conocida; si nadie la anota, en dos sesiones se lee como que la
  regla no existe, y el siguiente nombre en espanol entra sin que nadie lo discuta.
- **Como se paga:** renombrar a `techdebt.md` con `git mv`, actualizar todas sus referencias, y
  comprobar con `git grep -n "debtec" -- .` que no queda ninguna.

🕒 **`Confirmacion` revertida a `Propuesta (pendiente del usuario)` el 2026-09-01, tras el
hallazgo `F-003` de `R-002`.** La entrada nacio en el cierre de `S-002` con `Confirmada`, y el Paso 5
de `protocol-close` prohibe expresamente ese valor al `session-closer`: lo que el escribe va
**marcado como propuesta**, para que el usuario la confirme o la tumbe. El propio `S-002` §6 admite
que el valor descansaba en el traspaso de la sesion, no en el diff, y no existe ningun `D-XXX` que
ampare la excepcion. `manager` **tampoco puede confirmarla**: quien confirma esta escrito dentro del
valor, y es el usuario. El campo `Origen: usuario` se deja como esta — dice de quien nacio la deuda,
no que la confirmacion se haya producido.
