# assumptions.md

> Registro de los **supuestos vigentes**: lo que se da por cierto sin confirmacion explicita.
> Cada supuesto tiene codigo `A-XXX`. Al confirmarse pasa a `constraints.md` o `decisions.md`;
> al refutarse se marca como refutado.

---

## Indice

| Codigo | Supuesto | Fecha | Estado |
|---|---|---|---|
| [A-001](#a-001---un-auditor-lanzado-por-el-auditado-conserva-independencia-suficiente) | Un auditor lanzado por el auditado conserva independencia suficiente | 2026-08-31 | Abierto |
| [A-002](#a-002---el-brief-recibido-es-el-encargo-completo) | El brief recibido es el encargo completo | 2026-08-31 | Abierto |
| [A-003](#a-003---el-historico-de-la-fuente-oficial-es-obtenible-de-forma-automatizable) | El historico de la fuente oficial es obtenible de forma automatizable | 2026-08-31 | Abierto |

---

## Convenciones

| Campo | Valores posibles |
|---|---|
| Codigo | `A-XXX`, correlativo, no se reutiliza |
| Estado | `Abierto` / `Confirmado` / `Refutado` |
| Origen | `usuario` / `manager` / `report_auditor` |

🚨 **Un supuesto que no dice como se refuta no es un supuesto: es una creencia.** Cada entrada
lleva **como se refuta** y **su disparador** —el momento concreto en que alguien lo va a mirar—.
Sin disparador, el supuesto se queda abierto para siempre porque nadie tiene la obligacion de
volver a el.

🚨 **Un supuesto se valida donde su fallo se distingue de su funcionamiento.** Si el control elegido
da el mismo resultado tanto si el supuesto es cierto como si es falso, ese control no lo valida.

⚠️ **Un supuesto refutado no se borra.** Se marca `Refutado`, con la fecha y con lo que se supo.
Un supuesto reescrito conserva su enunciado anterior recuperable desde el propio archivo.

🚨 **El indice se escribe a mano, sin generador.** Cada fila enlaza por ancla a su supuesto.

---

## Supuestos

### A-001 - Un auditor lanzado por el auditado conserva independencia suficiente
| Campo | Valor |
|---|---|
| Fecha | 2026-08-31 |
| Estado | Abierto |
| Origen | manager |
| Decision relacionada | D-012 |

- **Supuesto:** un agente `auditor` que arranca en frio, lee solo archivos y `git`, y no recibe el
  contexto de la conversacion, produce una auditoria util **aunque lo lance la misma parte a la que
  audita**.
- **Por que se supone:** lo que daba valor al esquema de dos terminales era que quien construye no
  fuera su propio testigo, y esa parte la conserva un agente que no vio la jornada. Lo que **no**
  conserva es que el auditor decida por su cuenta cuando auditar y que no pueda ser silenciado.
- **Como se refuta:** dos señales, y cualquiera de las dos basta.
  1. Las auditorias devuelven `Sin hallazgos` de forma sostenida mientras el arranque —u otra
     comprobacion— detecta desfases reales que la auditoria tenia delante y no abrio.
  2. Aparecen sesiones cerradas con `Auditoria: Pendiente` en `_audit/index.md`: el paso obligatorio
     se saltó y nadie lo noto en el momento.
- **Disparador:** el **Paso 1c de `protocol-start`**, en cada arranque, que mira exactamente esas
  dos cosas. Y una revision explicita cuando haya **tres auditorias registradas**, para contrastar
  si lo que encontraron se corresponde con lo que despues resulto estar mal.

⚠️ **La segunda señal es la que hace este supuesto refutable de verdad.** La primera podria
explicarse por un trabajo sin defectos; la segunda no admite otra lectura.

🕒 **Observacion del 2026-09-01 (`S-003`), primer disparador con material real.** Ninguna de
las dos señales de refutacion se cumple, y hay evidencia a favor: `R-002` abrio cuatro hallazgos
sobre trabajo que `manager` habia hecho el dia anterior, y los cuatro se verificaron ciertos contra
`HEAD` antes de aceptarlos. Un auditor complaciente es justo el que no los habria abierto.

```
$ git grep -n "| Pendiente |" -- _audit/index.md ; echo "exit=$?"
exit=1

$ git grep -nc "Aceptado — pendiente |" -- _audit/findings.md ; echo "exit=$?"
_audit/findings.md:8
exit=0
```

Cero sesiones cerradas sin auditar (señal 2), y cero auditorias `Sin hallazgos` sostenidas
(señal 1). El supuesto **sigue `Abierto`**: una sola pasada no lo confirma, y la revision explicita
esta fijada a las **tres auditorias registradas** —hoy hay dos, `R-001` y `R-002`—.

🕒 **Nota anadida el 2026-09-01 (`S-005`), tras el hallazgo `F-005` de `R-003`.** El bloque de
arriba **se deja tal cual se ejecuto** (`D-019`); lo que se corrige es lo que se le puede pedir.

**Lo que el bloque probaba de verdad.** El `exit=1` se tomo **antes de que el cierre escribiera la
fila de su propia sesion**. Sobre `ea0b850`, el commit que contiene esa afirmacion, el mismo comando
devuelve una linea:

```
$ git grep -n "| Pendiente |" ea0b850 -- _audit/index.md ; echo "exit=$?"
ea0b850:_audit/index.md:14:| `S-003.md` | S-003 | 2026-09-01 | Pendiente | Pendiente | Pendiente | - |
exit=0
```

**Y el defecto de fondo no es la cifra: es que la señal 2 no podia dispararse nunca.** El
`session-closer` anade la fila de su sesion con `Auditoria: Pendiente` **antes** de commitear, asi
que ese comando devuelve `exit=0` en todo commit de cierre —incluido uno en el que la auditoria si
se lanzo despues— y `exit=1` solo una vez que la auditoria ya paso. Como criterio de refutacion, lo
que medi no era «una sesion se quedo sin auditar» sino «este commit es un cierre».

**Señal 2, rehecha con su momento de comprobacion.** Una sesion cerrada cuenta como **sin auditar**
cuando su fila de `_audit/index.md` sigue en `Pendiente` **al abrirse la sesion siguiente**, no en el
instante del cierre. Ese es el momento en que el Paso 1c de `protocol-start` la mira, y el unico en
que el valor `Pendiente` significa algo. Medido asi, hoy la señal sigue sin cumplirse:

```
$ git grep -n "| Pendiente |" HEAD -- _audit/index.md ; echo "exit=$?"
exit=1
```

El supuesto **sigue `Abierto`**: van tres auditorias registradas (`R-001`, `R-002`, `R-003`) mas
`R-004`, asi que la revision explicita fijada en el disparador ya toca — queda como asunto propio,
no se despacha en esta nota.

---

### A-002 - El brief recibido es el encargo completo
| Campo | Valor |
|---|---|
| Fecha | 2026-08-31 |
| Estado | Abierto |
| Origen | manager |

- **Supuesto:** `_brief/client_brief.md` contiene el encargo entero, y no hay requisitos relevantes
  que vivan solo en la cabeza del usuario o en conversaciones no registradas.
- **Por que se supone:** el brief llego como documento cerrado, con 27 secciones numeradas, una
  lista explicita de decisiones pendientes (§23) y un anexo sobre el proceso manual actual. Tiene
  forma de encargo completo.
- **Como se refuta:** que aparezca un requisito funcional no contemplado en ninguna de las 27
  secciones al definir el alcance, o que el usuario corrija o amplie el brief.
- **Disparador:** la tarea de recibir alcance y objetivo, que es la que abre la etapa siguiente. Es
  el momento en que el brief se contrasta punto por punto en vez de leerse.

⚠️ **El brief ya tiene al menos una tension interna sin resolver**, y eso es un indicio a favor de
mirarlo despacio: su §26 excluye los numeros del ultimo sorteo **del juego priorizado**, mientras
que el anexo describe excluir los que salieron **en cualquiera de los dos**. Son reglas distintas.

---

### A-003 - El historico de la fuente oficial es obtenible de forma automatizable
| Campo | Valor |
|---|---|
| Fecha | 2026-08-31 |
| Estado | Abierto |
| Origen | manager |

- **Supuesto:** el historico completo de resultados —fechas, balotas, superbalotas y premios de los
  dos juegos— se puede obtener de la fuente oficial de forma repetible desde el entorno de
  despliegue, y actualizarse despues de forma incremental.
- **Por que se supone:** el brief lo da por hecho en su §3 y construye sobre ello todo el ciclo de
  la aplicacion: sin historico no hay estadistica, no hay indicador y no hay comparacion.
- **Como se refuta:** que no exista una via estable de obtencion, o que la que exista quede fuera de
  lo que permite la plataforma de despliegue (`C-002`), o que la fuente no publique el historico
  completo sino solo los ultimos sorteos.
- **Disparador:** el diseño tecnico de la obtencion de datos, que el propio brief deja pendiente en
  su §23 punto 3. **No se construye nada encima antes de resolverlo.**

🚨 **Es el supuesto mas caro de los tres.** Si resulta falso, no cae una funcionalidad: cae el ciclo
entero de la aplicacion, porque las secciones 5 a 19 del brief dependen todas del historico.
