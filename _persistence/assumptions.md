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
| [A-004](#a-004---existe-acceso-al-patrocinador-y-a-personas-que-puedan-hablar-del-proceso-real) | Existe acceso al patrocinador y a personas que puedan hablar del proceso real | 2026-09-02 | Abierto |
| [A-005](#a-005---la-parte-de-ai_levelsmd-escrita-sin-experiencia-propia-es-correcta) | La parte de `ai_levels.md` escrita sin experiencia propia es correcta | 2026-09-02 | Abierto |

---

## Convenciones

| Campo | Valores posibles |
|---|---|
| Codigo | `A-XXX`, correlativo, no se reutiliza |
| Estado | `Abierto` / `Confirmado` / `Refutado` / `Riesgo abierto` |
| Origen | `usuario` / `manager` / `report_auditor` |
| Dueño | quien tiene que ir a verificarlo — un nombre, no un rol vago |

🚨 **`Dueño` y `Riesgo abierto` entran el 2026-09-02 por `D-037`**, y no son adorno: son lo unico
que la plantilla de restricciones y supuestos del descubrimiento aportaba y este archivo no tenia.
Entran aqui, que es donde sirven a cualquier etapa y no solo a una.

| Novedad | Que resuelve |
|---|---|
| **`Dueño`** | un supuesto sin dueño no se verifica nunca. El disparador dice **cuando** alguien lo mirara; el dueño dice **quien** |
| **`Riesgo abierto`** | un supuesto que **no se puede verificar antes de necesitarlo**, y se acepta a sabiendas. Va con **quien lo acepto** y por que no se pudo verificar |

⚠️ **`Riesgo abierto` es una decision, no un cajon de sastre.** Un supuesto que lleva meses
`Abierto` sin que nadie lo mire **ya es un riesgo abierto**, solo que sin nadie que lo haya
decidido. La diferencia entre los dos estados no es el tiempo que llevan: es si alguien firmo.

📌 **No es retroactivo.** Los `A-XXX` escritos antes de esta fecha no llevan `Dueño`, y no se les
añade uno inventado a posteriori — se les pone cuando se toquen por otra razon.

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

🕒 **Nota anadida el 2026-09-02 (`S-006`), tras el hallazgo `F-011` de `R-005`.** Los dos bloques
de arriba **se dejan tal cual se ejecutaron** (`D-019`); lo que se anade es su ancla.

**El bloque de la «señal 2, rehecha» se tomo sobre `HEAD` sin decir cual era.** Cuando se escribio,
`HEAD` era `e61454b` —el commit anterior al que acabaria conteniendo la nota—, y sobre ese hash el
resultado registrado se reproduce:

```
$ git grep -n "| Pendiente |" e61454b -- _audit/index.md ; echo "exit=$?"
exit=1
```

Sobre `510d580`, el commit que **si** contiene la nota, devuelve lo contrario, porque el
`session-closer` ya habia escrito la fila de su propia sesion:

```
$ git grep -n "| Pendiente |" 510d580 -- _audit/index.md ; echo "exit=$?"
510d580:_audit/index.md:16:| `S-005.md` | S-005 | 2026-09-01 | Pendiente | Pendiente | Pendiente | - |
exit=0
```

⚠️ **La cifra no estaba mal; la declaracion de ambito si.** `_audit/index.md` es justo uno de los
archivos que el cierre todavia iba a tocar, asi que el recuento cae de lleno en la regla 1 de `D-022`
—escrita en ese mismo commit—: se fecha o se ancla, nunca se declara reproducible sobre el commit que
lo contiene. **Leido con el ancla, el enunciado se sostiene entero:** la señal 2 rehecha —«sigue en
`Pendiente` **al abrirse la sesion siguiente**»— sigue sin cumplirse, y hoy tampoco:

```
$ git grep -n "| Pendiente |" a800d6b -- _audit/index.md ; echo "exit=$?"
exit=1
```

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

📌 **Nota del 2026-09-02 (`S-011`): se empezo a verificar y quedo a medias. El supuesto sigue
`Abierto`.** La consulta de los bloques D y E del archivo de lecciones globales (`D-054`) señalo
este supuesto como el walking skeleton del producto (`LG-47`) y como trabajo disponible pese al
bloqueo de `A-004` (`LG-52`). Se corrio la primera comprobacion y se interrumpio antes de concluir.

**Con que se probo, y por que asi:** con `curl`, sin navegador y sin ejecutar JavaScript, que es lo
mas parecido a una funcion serverless en la plataforma de despliegue (`C-002`). Abrir la pagina en un
navegador **no** verifica este supuesto: confirma que un humano con Chrome ve datos (`LG-01`, y
`LG-04` sobre el instrumento que tiene que poder ver el fallo que se descarta).

```
$ curl -sS -o /dev/null -w "http=%{http_code} tipo=%{content_type} bytes=%{size_download} tiempo=%{time_total}s\n" -L --max-time 25 "https://baloto.com/"
http=200 tipo=text/html; charset=utf-8 bytes=130243 tiempo=0.821238s

$ curl -sS -L --max-time 30 "https://baloto.com/resultados" -o baloto_res.html -w "http=%{http_code} bytes=%{size_download}\n"
http=200 bytes=101502

$ grep -oE "[0-9]{1,2} de [a-zA-Z]+ de [0-9]{4}" baloto_res.html | sort -u | head -5
22 de Agosto de 2026
24 de Agosto de 2026
26 de Agosto de 2026
29 de Agosto de 2026
31 de Agosto de 2026

$ grep -oE 'class="[^"]*(ball|balota|number)[^"]*"' baloto_res.html | sort | uniq -c
     10 class="balota-red-results"
     43 class="baloto-number rounded"
      2 class="red-ball gotham-medium"
     16 class="superbalota-number rounded"
     10 class="yellow-ball gotham-medium"
```

**Lo que esto SI indica:** el sitio responde `200` a `curl` sin cabeceras de navegador, no se
detectaron marcadores de framework de renderizado en cliente en el HTML de la portada, y
`/resultados` trae **fechas y clases de balotas en el HTML crudo** — es decir, los datos no se pintan
solo con JavaScript.

⛔ **Lo que esto NO prueba, y por eso el supuesto sigue `Abierto`:** (1) que exista **historico
completo** y no solo los ultimos sorteos —es la tercera forma de refutacion de la ficha, y es la que
mas importa—; (2) que se puedan extraer los **siete campos por sorteo** que el brief §3 exige,
incluidos los premios de los dos juegos; (3) que funcione **desde la plataforma de despliegue**, que
es otra IP, otro limite de tiempo y otro entorno; (4) si las condiciones de uso del sitio permiten la
extraccion automatizada — una cuarta forma de refutacion que esta ficha no recogia y que conviene
mirar antes de construir encima.

⚠️ **Las cuatro ordenes se corrieron sobre un sitio externo y vivo**, asi que no son reproducibles en
el sentido en que lo es un `git show`: la pagina puede cambiar. Se registran con su fecha por eso —
valen como «esto devolvia el 2026-09-02», no como un hecho permanente.

---

### A-004 - Existe acceso al patrocinador y a personas que puedan hablar del proceso real
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Abierto |
| Origen | manager |

- **Supuesto:** hay alguien alcanzable a quien preguntar —el patrocinador del encargo, y personas que
  hoy hacen el trabajo que la aplicacion pretende tocar— y ese acceso durara lo que dure la etapa de
  descubrimiento.
- **Por que se supone:** el archivo de etapa que se escribio en esta sesion lo pone como **entrada
  obligatoria**: «si falta el acceso, la etapa no puede empezar». Se escribio esa regla sin que nadie
  haya confirmado que el acceso existe. Hoy la unica entrada real del proyecto es el encargo escrito
  en `_brief/`, que es un documento, no una persona.
- **Por que se registra ahora y no al abrir la etapa:** porque **ya se construyo encima**. La etapa
  esta declarada, su archivo existe, y las tareas de alcance (`T-001`, `T-002`) estan asignadas a
  ella. Si el acceso no existe, ninguna de las tres cosas sirve tal como estan escritas.
- **Como se refuta:** que no haya un interlocutor identificable para el encargo; o que lo haya pero
  no responda; o que responda y no conozca el proceso real —un patrocinador que solo puede describir
  la solucion que imagina, y nadie que pueda describir como se hace hoy el trabajo.
- **Disparador:** **la primera tarea de `005_discovery` que requiera preguntarle algo a alguien**, que
  sera `T-001`. No se abre la etapa sin resolverlo antes.

🚨 **Si este supuesto es falso, lo que sale de la etapa no es descubrimiento: es invencion
documentada.** Y es peor que no tenerla, porque llega con la forma de un artefacto validado. El
resultado correcto en ese caso no es rellenar los cinco artefactos con lo que dice el brief, sino
escalarlo al usuario y decidir si la etapa puede empezar.

⚠️ **No lo confunde con `A-002`.** Aquel supone que el brief **esta completo**; este supone que hay
**alguien a quien preguntar** cuando no lo este. Un brief completo no sustituye el acceso: el
descubrimiento existe para contrastar lo escrito contra lo que pasa de verdad.

---

### A-005 - La parte de `ai_levels.md` escrita sin experiencia propia es correcta
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Abierto |
| Origen | manager |
| Dueño | `manager` |

- **Supuesto:** lo que `_workflow/ai_levels.md` afirma sobre **harness, observabilidad,
  evaluaciones, rubricas y metricas** —secciones 3, 4, 5 y 6— es correcto y sera util cuando haga
  falta aplicarlo.
- **Por que se supone, y no se afirma:** de todo lo que hay en `_workflow/`, esa mitad es la unica
  que **no se pudo contrastar contra nada**. El reparto de `team.md` se escribio con un ejemplo
  vivido delante —el propio sistema de trabajo de este metodo, que es nivel 4 sin harness— y por eso
  cada afirmacion tiene donde comprobarse. Del harness hacia arriba no hay ninguna experiencia: se
  adapto de un documento aportado por el usuario, se le añadio la rubrica de seleccion que le
  faltaba, y **nadie ha construido todavia un sistema con el que contrastarlo**.
- **Por que se registra ahora:** porque **ya se va a construir encima**. Ese archivo existe para
  guiar decisiones futuras, y la primera que guie heredara lo que aqui se dio por bueno. Registrarlo
  despues seria registrarlo cuando ya no se puede separar de sus consecuencias.
- **Lo que este supuesto NO cubre:** la mitad de `team.md`, ni las secciones 1, 2, 7, 8, 9 y 10 de
  `ai_levels.md`. La rubrica de §6 **si** entra: es aportacion propia y nunca se ha usado para
  elegir nada.
- **Como se refuta:** que al declarar el primer nivel real la rubrica de §6 **no discrimine** —dos
  niveles distintos empatan, o el resultado contradice el juicio de quien lo aplica y no se puede
  argumentar contra los ejes—; o que al instrumentar el primer harness resulte que las metricas de
  §5.4 no son las que hacen falta, o que falta una pieza que el archivo no nombra.
- **Disparador:** **la primera vez que se declare un nivel de sistema de IA con su `D-XXX`**, que por
  `ai_levels.md` §8 sera en la linea base del producto. Ahi se aplica la rubrica de verdad, y ahi se
  ve si sirve.

⚠️ **No es un supuesto sobre si el archivo debia escribirse.** Se decidio escribirlo hoy, y la razon
esta registrada: un documento de referencia no existe para aplicarse hoy, sino para que cuando
llegue el momento no se improvise — el mismo criterio con el que existe `_methodology/`, que
describe el ciclo entero sin que ninguna de sus etapas posteriores este declarada. Lo que este
supuesto anota es otra cosa: **que el contenido acierte**, que es justo lo que no se puede saber sin
haberlo usado.
