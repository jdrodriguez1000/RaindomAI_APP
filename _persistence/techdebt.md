# techdebt.md

> Registro de la **deuda tecnica** del proyecto: atajos conscientes, soluciones provisionales
> y pendientes de calidad. Cada item tiene codigo `DT-XXX`, estado, importancia y urgencia.
> La deuda se registra en el momento en que se contrae.

---

## Indice

| Codigo | Deuda tecnica | Estado | Confirmacion | Importancia | Urgencia |
|---|---|---|---|---|---|
| [DT-001](#dt-001---debtecmd-incumple-la-regla-de-nombres-en-ingles) | `debtec.md` incumple la regla de nombres en ingles | Implementada | Confirmada | Baja | No bloqueante |
| [DT-002](#dt-002---_workflow-nace-sin-ningun-enganche-de-uso-l-014) | `_workflow/` nace sin ningun enganche de uso (`L-014`) | No implementada | Propuesta (pendiente del usuario) | Media | No bloqueante |

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
| Estado | Implementada |
| Confirmacion | Confirmada |
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

🕒 **Estado al 2026-09-01: confirmada y pagada.** El usuario confirmo la deuda y pidio pagarla
en la misma peticion —ordenar el renombrado es confirmar que el atajo era un atajo—, asi que
`Confirmacion` pasa a `Confirmada` y `Estado` a `Implementada` en la misma pasada. El archivo es
ahora `_persistence/techdebt.md` (`git mv`), y se reescribieron las **referencias vivas**: los tres
skills, `session-closer.md`, `CLAUDE.md`, `project.md` y la tabla de estructura de `progress.md`.
**El titulo de esta entrada se deja como esta**, porque nombra el defecto que hubo y no el estado de
hoy. Alcance y verificacion, en `D-021`.

🕒 **Nota anadida el 2026-09-01 (`S-005`), tras el hallazgo `F-009` de `R-004`.** El campo «Como se
paga» de arriba **se deja tal cual se escribio** y pide `git grep -n "debtec" -- .` en cero, sin
acotar ambito. Ese criterio literal **no se cumple y no se pretendio cumplir**: `D-021` acoto el
pago al ambito vivo y dejo lo historico intacto a proposito. Escrito el criterio absoluto y no la
excepcion, quien lo aplique tal cual concluye que la deuda no esta pagada.

**El criterio de cierre realmente aplicado es este:** cero referencias `debtec` en `.claude`,
`CLAUDE.md` y `project.md` —el ambito vivo que fija `D-021`—, con lo historico de `_audit/`,
`decisions.md` y la narrativa de `progress.md` intacto por decision del usuario. Sobre `HEAD`:

```
$ git grep -n "debtec" HEAD -- .claude CLAUDE.md project.md ; echo "exit=$?"
exit=1

$ git ls-tree --name-only HEAD _persistence/ | grep -i debt
_persistence/techdebt.md
```

⚠️ Con ese criterio, `DT-001` esta pagada. Con el literal de «Como se paga», no lo estaria nunca
—reescribir `_audit/` es justo lo que `D-021` descarto—. **Manda el de esta nota.**

🕒 **`Confirmacion` revertida a `Propuesta (pendiente del usuario)` el 2026-09-01, tras el
hallazgo `F-003` de `R-002`.** La entrada nacio en el cierre de `S-002` con `Confirmada`, y el Paso 5
de `protocol-close` prohibe expresamente ese valor al `session-closer`: lo que el escribe va
**marcado como propuesta**, para que el usuario la confirme o la tumbe. El propio `S-002` §6 admite
que el valor descansaba en el traspaso de la sesion, no en el diff, y no existe ningun `D-XXX` que
ampare la excepcion. `manager` **tampoco puede confirmarla**: quien confirma esta escrito dentro del
valor, y es el usuario. El campo `Origen: usuario` se deja como esta — dice de quien nacio la deuda,
no que la confirmacion se haya producido.

---

### DT-002 - `_workflow/` nace sin ningun enganche de uso (`L-014`)
| Campo | Valor |
|---|---|
| Estado | No implementada |
| Confirmacion | Propuesta (pendiente del usuario) |
| Importancia | Media |
| Urgencia | No bloqueante |
| Origen | manager |
| Fecha | 2026-09-02 |

- **Deuda:** `_workflow/` nacio en esta sesion (`D-046`) con sus tres enganches de **control** —fila
  en «Carpetas propias» de `project.md`, entrada en la lista de lo copiable tal cual de `CLAUDE.md`,
  ambito del Paso 1b de `protocol-close`—, pero **ningun** enganche de **uso**: nada en `_phases/`
  ni en ningun protocolo manda leer `team.md` o `ai_levels.md` en el momento en que aplican. Lo deja
  registrado `L-013` de `lessons.md`.
- **Por que se tomo:** los tres enganches de control eran los que ya se sabia que hacian falta,
  porque `_templates/` habia pasado por lo mismo. El cuarto —que alguien tenga que abrir la
  carpeta— exige decidir **en que punto de que etapa** se consulta, y esa es una decision de
  `_phases/` que le toca al usuario, no algo que el cierre de sesion pueda resolver.
- **Costo de no pagarla:** ninguno de los tres controles existentes detecta esta deuda —una carpeta
  agnostica, declarada y sin fugas, pero que nadie abre nunca, deja el repositorio «coherente» con
  material muerto dentro—. Sin el cuarto enganche, `_workflow/` corre el riesgo de quedar como
  documentacion que nadie consulta cuando llegue el momento de repartir trabajo o elegir un nivel de
  sistema de IA.
- **Como se paga:** decidir en que archivo de `_phases/` (o en que otro punto del metodo) se cita
  `_workflow/team.md` y `_workflow/ai_levels.md`, y con que `D-XXX`.

📌 **Propuesta del cierre `S-009`**, a partir de `L-014`. `manager` no la escribe como deuda
confirmada porque resolverla implica una decision de diseño —donde exactamente se engancha— que le
corresponde al usuario.
