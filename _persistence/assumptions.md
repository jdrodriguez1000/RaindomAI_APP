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
| [A-006](#a-006---los-codigos-de-feature-y-escenario-que-el-proyecto-declaro-son-los-que-acabara-usando) | Los codigos de feature y escenario que el proyecto declaro son los que acabara usando | 2026-09-03 | Abierto |
| [A-007](#a-007---habra-un-humano-disponible-para-ejecutar-cada-despliegue-de-la-etapa-del-esqueleto) | Habra un humano disponible para ejecutar cada despliegue de la etapa del esqueleto | 2026-09-03 | Abierto |
| [A-008](#a-008---los-huecos-de-codigo-que-dejan-las-plantillas-del-crecimiento-seran-rellenables-cuando-la-etapa-se-abra) | Los huecos de codigo que dejan las plantillas del crecimiento seran rellenables cuando la etapa se abra | 2026-09-05 | Abierto |
| [A-009](#a-009---_phases-y-_workflow-podran-seguir-en-cero-codigos-instanciados-sin-perder-nada) | `_phases/` y `_workflow/` podran seguir en cero codigos instanciados sin perder nada | 2026-09-06 | Abierto |
| [A-010](#a-010---el-anclaje-del-paso-7c-bis-se-queda-en-mecanico-y-no-se-desliza-a-escribir-el-porque) | El anclaje del Paso 7c-bis se queda en mecanico y no se desliza a escribir el porque | 2026-09-06 | Refutado |
| [A-011](#a-011---el-paso-7c-bis-podra-seguir-escribiendo-solo-en-dos-archivos-porque-los-criterios-de-cierre-no-nacen-en-otros) | El Paso 7c-bis podra seguir escribiendo solo en dos archivos, porque los criterios de cierre no nacen en otros | 2026-09-07 | Abierto |
| [A-012](#a-012---opera-de-forma-sostenida-con-usuarios-reales-se-lee-sobre-el-sistema-de-trabajo-no-sobre-el-producto) | «Opera de forma sostenida con usuarios reales» se lee sobre el sistema de trabajo, no sobre el producto | 2026-09-07 | Abierto |

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

---

### A-006 - Los codigos de feature y escenario que el proyecto declaro son los que acabara usando
| Campo | Valor |
|---|---|
| Fecha | 2026-09-03 |
| Estado | Abierto |
| Origen | manager |
| Dueño | `manager` |

- **Supuesto:** `D-075` declaro `FT-XXX` y `SC-XXX` en la tabla «Codigos» de `project.md`. Eso da por
  cierto que **este proyecto va a adoptar la etapa de la baseline con el juego de codigos de la guia
  de metodo**, y que cuando llegue el momento seguiran sirviendo tal cual.
- **Por que se supone, y no se afirma:** la etapa `020_baseline` **no esta declarada** —la tabla
  «Etapas» sigue teniendo solo `000_preproject` y `005_discovery`—, y declarar las etapas posteriores
  es trabajo de `005_discovery` (`T-002`), que aun no ha empezado. La declaracion de los dos codigos
  no se hizo porque hubiera producto: se hizo porque las plantillas ya los escribian y un codigo
  citado antes de declararse es un desfase. **Es una regularizacion, no una eleccion de diseño**, y
  esa diferencia es exactamente lo que este supuesto guarda.
- **Por que se registra ahora:** porque la fila ya esta en la tabla, y una fila en la tabla de
  codigos se lee, a los pocos meses, como un codigo elegido. Sin este supuesto, el dia que
  `005_discovery` decida las etapas posteriores nadie sabra que estos dos entraron por la puerta de
  atras y que nunca se contrastaron contra el producto real.
- **Lo que este supuesto NO cubre:** `N-XXX` e `I-XXX`, que entraron por el mismo argumento pero
  para una etapa **si declarada**; ni `VS-`, `TC-` y `ADR-`, que deliberadamente **no** se
  declararon y siguen siendo propuesta.
- **Como se refuta:** que las etapas posteriores se declaren con un metodo distinto que no tenga
  features ni escenarios; que la etapa de la baseline se adopte con otros nombres para esos dos
  conceptos; o que al llegar al Paso 3 de esa etapa el contraste contra el registro obligue a
  cambiar alguno de los dos. En cualquiera de los tres casos la fila sobra o cambia, y **la retirada
  se registra con su `D-XXX`** citando `D-075` — no se borra en silencio.
- **Disparador:** **la decision que declare las etapas posteriores a `005_discovery`** (`T-002`), y
  en su defecto el Paso 3 de la etapa de la baseline el dia que se abra. Lo que llegue primero.

---

### A-007 - Habra un humano disponible para ejecutar cada despliegue de la etapa del esqueleto
| Campo | Valor |
|---|---|
| Fecha | 2026-09-03 |
| Estado | Abierto |
| Origen | manager |
| Dueño | `manager` |

- **Supuesto:** `D-080` puntua el eje «Impacto de un error» de la etapa del esqueleto en **2**, y de
  ahi sale la lectura **nivel 2** de `_workflow/ai_levels.md` §6. Ese 2 se sostiene **solo** porque
  `_workflow/025_wslt.md` §3 le quita a la IA el despliegue y el empuje de historial. Y quitarselos
  da por cierto lo que este supuesto guarda: **que cuando llegue el momento habra una persona
  disponible para ejecutarlos y firmarlos**.
- **Por que se supone, y no se afirma:** hoy no hay etapa declarada, no hay entorno, no hay codigo y
  no hay nadie asignado. El reparto reparte trabajo entre participantes que todavia no han hecho
  nada. Que exista quien ejecute el Paso 4 no esta confirmado por nada: **esta asumido por la propia
  forma del reparto**.
- **Por que se registra ahora, y no cuando se abra la etapa:** porque `D-080` **ya se apoya en el**.
  Una puntuacion de rubrica que descansa en un supuesto no escrito se lee, a los pocos meses, como
  una propiedad de la etapa — y entonces nadie sabe que hay algo que comprobar. Es el mismo caso que
  `A-006`: lo que se guarda no es el dato, es **la diferencia entre lo elegido y lo asumido**.
- **Que pasa si resulta falso, y por que importa mas de lo que parece:** no pasa que la etapa se
  retrase. Pasa que alguien delega el despliegue **«solo esta vez»**, y en ese momento el eje se va
  al **3** sin que nadie lo escriba. `_workflow/ai_levels.md` §6 dice que cualquier eje en 3 pide
  **nivel 5** con harness obligatorio, y que «impacto de un error en 3 no se compensa con nada».
  🚨 **El fallo silencioso es exactamente ese: la puntuacion sigue diciendo 2 y ya no es cierta**, y
  ningun control del repositorio lo mira.
- **Lo que este supuesto NO cubre:** que el humano disponible sea competente para diagnosticar lo
  que rompa el despliegue —eso es otra cosa y no se registra aqui—, ni el segundo supuesto que
  `_workflow/025_wslt.md` §7 nombra: que habra quien revise **cada** tramo de codigo del Paso 3. Ese
  segundo entra al registro el dia que la etapa se adopte, con el `D-XXX` del reparto.
- **Como se refuta:** que al abrir la etapa no haya nadie asignado al Paso 4; o que se registre una
  decision que delegue el despliegue, sea a un agente o a un proceso automatico. En cualquiera de
  los dos casos **`D-080` hay que rehacerlo diciendo que eje se movio**, y no se corrige en silencio.
- **Disparador:** **el `D-XXX` que adopte el reparto al abrir la etapa del esqueleto** — que es el
  momento en que se dice con nombre quien ejecuta cada paso. Y antes que ese, cualquier decision que
  automatice un despliegue en este proyecto, aunque sea fuera de esa etapa.

⚠️ **No se confunde con `C-002`.** Aquella fija **donde** se despliega, y es una restriccion
confirmada. Este supone **quien** lo ejecuta, y no lo esta.

---

### A-008 - Los huecos de codigo que dejan las plantillas del crecimiento seran rellenables cuando la etapa se abra
| Campo | Valor |
|---|---|
| Fecha | 2026-09-05 |
| Estado | Abierto |
| Origen | manager |
| Dueno | `manager` |

- **Supuesto:** `D-085` decidio que las tres plantillas de `_templates/030_growth/` **no estrenen
  ningun codigo de producto**, y dejen en su lugar huecos que remiten a la tabla «Codigos» de
  `project.md`. Los huecos son tres: **el codigo de slice**, **el codigo de la tarea de producto** y
  **el del caso de prueba**. Esa decision da por cierto que, cuando la etapa se abra, **esos tres
  codigos existiran en la tabla** y el hueco se podra rellenar sin rehacer la plantilla.
- **Por que se supone, y no se afirma:** hoy ninguno de los tres esta declarado. `A-006` ya lo dice
  con esas palabras — `VS-`, `TC-` y `ADR-` «deliberadamente no se declararon y siguen siendo
  propuesta». Y el de la tarea de producto es peor que no estar declarado: **la guia de metodo le da
  la misma inicial que `project.md` ya usa para la tarea de jornada**, y donde se registran las
  tareas de una slice sigue sin decidirse.
- **Sobre que se construyo encima:** sobre esto se escribieron las tres plantillas, y en concreto la
  tabla de tareas de `010_slice_NNN.md` §2 y las columnas de codigo de `005_iteration_NNN.md` §2 y
  §4. Si el supuesto es falso, esas tablas no se pueden rellenar tal como estan.
- **Por que se registro despues de construir, y no antes:** por descuido, y conviene que conste. La
  regla es registrarlo **antes** de construir encima; aqui la decision de dejar huecos se tomo al
  escribir las plantillas y el supuesto que la sostiene no se separo de la decision hasta revisar los
  cuatro archivos del porque al cerrar. Se registra en la misma sesion, que es lo unico que salva la
  situacion — un dia mas y habria quedado dentro de `D-085` sin que nadie lo leyera como un supuesto.
- **Que pasa si resulta falso:** hay dos formas de que lo sea, y cuestan cosas distintas.
  1. **Que el proyecto adopte otro juego de codigos** —o ninguno, si decide identificar las slices
     por su enunciado—. Coste bajo: se rellenan los huecos con lo que haya, que es justo para lo que
     el hueco existe.
  2. **Que la colision del prefijo de la tarea no se resuelva antes de la primera slice.** Coste
     alto: el Paso 3 del archivo de etapa exige tenerlo decidido **antes de escribir la primera
     tarea**, porque un proyecto que descubre a mitad de la tercera slice que tiene dos registros de
     tareas ya no puede unificarlos sin reescribir historia. La plantilla pone el recuadro que obliga
     a mirarlo, pero un recuadro no decide nada.
- **Como se refuta:** que la etapa del crecimiento se abra —o que se escriba la primera slice— sin
  que la tabla «Codigos» tenga los tres codigos, o sin una decision registrada sobre donde viven las
  tareas de una slice. En ese caso el supuesto queda refutado y **se marca, no se borra**, con la
  decision que lo sustituya.
- **Disparador:** **la decision que adopte la etapa de la baseline** —que es quien estrena los
  codigos de producto y a quien `D-082` remitio la colision— y, en su defecto, el Paso 1 de la
  primera iteracion del crecimiento. Lo que llegue primero.

📌 **Este supuesto no cubre `ADR-`**, aunque `A-006` lo nombre junto a los otros dos: las decisiones
arquitectonicas de esta etapa usan la plantilla que ya existe en `_templates/020_baseline/`, y su
codigo es problema de aquella etapa, no de estas tres plantillas.

---

### A-009 - `_phases/` y `_workflow/` podran seguir en cero codigos instanciados sin perder nada
| Campo | Valor |
|---|---|
| Fecha | 2026-09-06 |
| Estado | Abierto |
| Origen | manager |
| Dueno | `manager` |

- **Supuesto:** `D-087` crea el Paso 1c del cierre, que exige **cero** codigos instanciados en
  `_phases/` y `_workflow/`. Ese cero no es una observacion: es una **apuesta a futuro**. Da por
  cierto que ninguna necesidad legitima va a pedir citar un `T-XXX` o un `D-XXX` con su numero dentro
  de esas dos carpetas — es decir, que **todo lo que haya que trazar desde ahi se puede trazar sin
  numero**, remitiendo al registro sin citarlo.
- **Por que se supone, y no se afirma:** la fuga que motivo el control entro precisamente por una
  necesidad razonable —explicar de donde salia un cambio— y no por descuido (`L-030`). Que esa
  necesidad se pudiera satisfacer sin numero se comprobo **una vez**, en la nota del §5 del archivo de
  etapa del crecimiento: bastaba con la fecha. Una vez no es una muestra.
- **Sobre que se construyo encima:** sobre esto se construyo un control mecanico que corre en **cada
  cierre** y cuya respuesta correcta es cero. Un control cuyo cero deja de ser alcanzable no se queda
  quieto: empieza a devolver una linea legitima cada sesion, alguien la aprueba «porque esta bien», y
  a la tercera vez nadie mira las demas. Es el fallo que el propio Paso 1b describe sobre su ambito.
- **Como se refuta:** aparece una necesidad de trazabilidad **dentro de una de las dos carpetas** que
  no se puede satisfacer con una fecha ni con una referencia sin numero — por ejemplo, una nota que
  tenga que distinguir entre dos decisiones que dicen lo contrario, donde el numero es lo unico que
  las separa.
- 🚨 **Y donde se distingue su fallo de su funcionamiento:** en la **salida del propio Paso 1c**. Si
  algun cierre devuelve una linea y la evaluacion honesta es «esta bien puesta», el supuesto acaba de
  quedar refutado — no se aprueba la excepcion y se sigue. Es un control que se autodiagnostica: su
  primer falso positivo real es la refutacion.
- **Disparador:** cada ejecucion del Paso 1c. No hace falta una fecha: el control corre en todos los
  cierres, y este supuesto se mira con el.
- **Que pasa si resulta falso:** el control no se apaga, se acota. La salida sera declarar la
  excepcion con su `D-XXX` —que codigo, en que archivo y por que ahi hace falta el numero— y anadir
  esa exclusion al patron, con la regla de que **cada exclusion lleva su decision**; una lista de
  excepciones sin razones escritas envejece y acaba tapando lo que el control existe para ver, que es
  lo que el Paso 2c ya advierte de no hacer.

---

### A-010 - El anclaje del Paso 7c-bis se queda en mecanico, y no se desliza a escribir el porque
| Campo | Valor |
|---|---|
| Fecha | 2026-09-06 |
| Estado | Refutado |
| Origen | manager |
| Dueno | `manager` |

- **Supuesto:** `D-092` abre la **primera grieta** en una regla que hasta hoy no tenia ninguna — que
  el cierre no escribe en los cuatro archivos del porque. La grieta se justifica en que sustituir el
  ancla de una orden ya escrita y pegar su salida **no pide ni un dato de la conversacion**. Eso da
  por cierto que la frontera entre «anclar» y «redactar» **se sostiene en la practica**, con un agente
  que arranca en frio, que ve el archivo entero delante, y al que la orden que acaba de correr le
  devuelve algo que no cuadra.
- **Por que se supone, y no se afirma:** la frontera esta escrita con todo el detalle que se pudo
  —que puede tocar, que no, y que hacer ante una discrepancia—, pero **no se ha ejecutado ni una
  vez**. Todo lo que hoy la sostiene es que el argumento parece bueno, y un argumento que parece bueno
  es exactamente lo que precede a la mayoria de las reglas que despues hay que acotar.
- **La situacion concreta en la que se rompe, y va a ocurrir:** el Paso 7c-bis corre una orden anclada
  y la salida **no coincide** con la publicada. Ya paso hoy, en `D-088`, y la nota lo documenta. La
  regla dice detenerse y reportar; la tentacion es corregir el numero, porque es un numero, porque es
  obvio cual es el bueno, y porque cuesta un segundo. **Ese segundo es la grieta entera.**
- **Sobre que se construyo encima:** sobre esto se construyo un paso obligatorio del cierre que toca
  el archivo mas sensible del registro. Si el limite se desliza, lo que se pierde no es una linea: es
  la garantia de que `decisions.md` lo escribio quien vivio la jornada — y esa garantia es la razon de
  que los cuatro archivos sean de `manager`.
- **Como se refuta:** una auditoria encuentra en un commit de anclaje **cualquier cambio en
  `decisions.md` que no sea una orden anclada o su salida** — una palabra de prosa, una salida
  corregida en vez de reportada, o el bloque de una decision de una sesion anterior. Se ve en una
  linea:

```
git show <commit-de-anclaje> -- _persistence/decisions.md
```

- **Disparador:** cada cierre que abra alguna decision, a partir de la sesion siguiente. El commit de
  anclaje es publico y su diff es pequeño por definicion: revisarlo cuesta segundos, y es la unica
  ventana en que este supuesto se puede mirar.
- **Que pasa si resulta falso:** la excepcion se retira y se vuelve a la alternativa que se descarto
  —que `manager` ancle en la sesion siguiente—, asumiendo su coste conocido: el commit que la
  auditoria juzga lleva siempre los criterios sin anclar. **No se acota con una excepcion nueva**: una
  grieta que ya se ensancho una vez no se estrecha escribiendo mas letra.

> 🚨 **Nota del 2026-09-07 — REFUTADO (`F-062`, sesion S-024).** El disparador era «cada cierre que
> abra alguna decision»; la primera ejecucion real fue el commit de anclaje `a48411a`, y el control
> que este supuesto escribio para refutarse —`git show <commit-de-anclaje> -- _persistence/decisions.md`—
> devuelve exactamente lo que decia que no debia aparecer: **tres lineas de prosa borradas** en
> `D-092`.
>
> ```
> $ git diff a48411a^ a48411a -- _persistence/decisions.md | grep -E '^-[^-]' | grep -vE '^-\$ ' | grep -vE '^-[0-9]+:'
> -CLAUDE.md:1
> -.claude/agents/session-closer.md:1
> -⚠️ **Las cuatro ordenes se corren sobre el arbol de trabajo, y el Paso 7c-bis que esta misma
> -decision crea las anclara al commit** — es el primer caso al que se aplica la regla. Los numeros de
> -linea de la primera son los que mas se mueven, y por eso el anclaje importa.
> -.claude/skills/protocol-gate2/SKILL.md:15
> -_templates/035_gate2/005_verdict.md:11
> ```
>
> ⚠️ **Las cinco lineas que no son prosa son salidas de ordenes**, y esas si podia tocarlas: son el
> resultado viejo que la forma anclada sustituye. Las tres del medio no: son texto explicativo
> escrito por `manager`.
>
> 🔑 **Se refuto en su primera oportunidad, que es lo mejor que le puede pasar a un supuesto.** El
> disparador funciono, el control elegido distinguio el fallo del funcionamiento, y el coste de
> saberlo fue una auditoria.
>
> ⛔ **Y la consecuencia que este supuesto dejo escrita NO se cumple, a proposito.** Decia «la
> excepcion se retira» y «no se acota con una excepcion nueva». Se ha acotado. **Eso es renegociar un
> pre-compromiso, y no se disimula: se registra con su razon en `D-099`, y lo zanjo el usuario.**

---

### A-011 - El Paso 7c-bis podra seguir escribiendo solo en dos archivos, porque los criterios de cierre no nacen en otros
| Campo | Valor |
|---|---|
| Fecha | 2026-09-07 |
| Estado | Abierto |
| Origen | manager |
| Dueno | `manager` |

- **Supuesto:** `D-101` y `D-102` dejan el Paso 7c-bis con **deteccion universal y escritura acotada**:
  el barrido de la nota de la seccion 7 recorre todos los archivos de `_persistence` y `_audit`, pero
  lo que el paso puede anclar sigue siendo `decisions.md` y `tasks.md`. Eso da por cierto que **los
  bloques «Criterio de cierre» no van a nacer en ningun otro archivo** — que ninguna entrada de
  `constraints.md`, `assumptions.md`, `lessons.md` o `techdebt.md` va a publicar una orden con
  `<hash>` que necesite anclarse despues del commit.
- **Por que se supone, y no se afirma:** hoy es cierto y se comprobo, pero es cierto **por costumbre,
  no por regla**. Ninguna convencion prohibe que una entrada de `constraints.md` publique manana un
  criterio con su orden; al contrario, la convencion de `decisions.md` que `D-096` estreno hace que
  publicar ordenes ancladas sea **lo normal**, y esa costumbre se contagia. Verificado contra el arbol
  de esta sesion, antes de escribir el barrido:

```
$ for f in _persistence/*.md _audit/*.md; do n=$(grep -cE '^\$ .*<hash>' "$f"); [ "$n" != "0" ] && echo "$f: $n"; done
_persistence/decisions.md: 22
_persistence/tasks.md: 28
_audit/S-017.md: 1
_audit/S-024.md: 1
```

  Los dos de `_audit/` son listados de la seccion 7, que citan ordenes ajenas y no son criterios de
  cierre. Fuera de `decisions.md` y `tasks.md` no hay ninguno — **hoy**.

- **Sobre que se construyo encima:** sobre esto se construyo el control que cierra la nota de la
  seccion 7. Si el supuesto falla, el control **hace exactamente lo que debe** —senala el archivo y
  el paso se detiene—, asi que el fallo no es silencioso. Lo que se paga es que el cierre se para y
  hay que decidir en el momento: ampliar la autorizacion del paso, o mover el criterio a un archivo
  que si la tenga.
- **Por que se acota la escritura en vez de ampliarla ya:** ampliar la excepcion a los cuatro
  archivos del porque por si acaso es justo lo que `A-010` vigila. `CLAUDE.md` se los prohibe al
  `session-closer` con una razon, y `tasks.md` entro porque **ya era suyo**, no porque hiciera falta
  sitio. Un permiso concedido para un caso que aun no ha ocurrido no se puede retirar despues, porque
  nadie sabra si se estaba usando.
- **Como se refuta:** el barrido de la nota de la seccion 7 devuelve una linea de un archivo distinto
  de `_persistence/decisions.md` y `_persistence/tasks.md`.

```
$ for f in $(git ls-tree -r --name-only <commit> _persistence _audit | grep -v '_audit/S-'); do n=$(git show <commit>:"$f" | grep -cE '^\$ .*<hash>'); [ "$n" != "0" ] && echo "$f: $n"; done
```

- **Disparador:** cada cierre de sesion, en el Paso 7c. No hace falta ir a mirarlo aparte: el control
  ya corre ahi, y su salida vacia **es** la confirmacion de este supuesto en esa pasada.
- **Y por eso este supuesto no necesita fecha limite.** Se comprueba solo, una vez por sesion, en el
  sitio donde importa. Lo que hay que hacer el dia que falle esta escrito arriba.

📌 **Nota del 2026-09-07 (`D-107`, `F-071`) — este supuesto sigue `Abierto`, pero su criterio de
refutacion era el equivocado y se sustituye.** El supuesto no se reescribe (`D-019`): su enunciado
—que los bloques «Criterio de cierre» no nacen fuera de `decisions.md` y `tasks.md`— **se sostiene**,
y se comprueba con la orden que le corresponde, anclada:

```
$ for f in $(git ls-tree -r --name-only 3bf61d4 _persistence); do n=$(git show 3bf61d4:"$f" | grep -c '^- \*\*Criterio de cierre:\*\*'); [ "$n" != "0" ] && echo "$f: $n"; done
_persistence/decisions.md: 25
_persistence/tasks.md: 105
```

**Cero criterios de cierre fuera de los dos archivos autorizados.** Ese es el enunciado, y es el que
manda.

⛔ **Lo que falla es el control que la entrada nombro como «Como se refuta».** Barre toda linea que
lleve `<hash>`, no los bloques «Criterio de cierre», y por eso **acierta en cosas que no son el
supuesto** — empezando por las dos ordenes de esta misma entrada. Las convenciones de este archivo lo
prohiben con todas las letras: *«un supuesto se valida donde su fallo se distingue de su
funcionamiento»*. Este control da la misma salida tanto si el supuesto es cierto como si es falso.

**El criterio de refutacion pasa a ser este, y sustituye al de arriba:**

> El barrido de bloques «Criterio de cierre» devuelve una linea de un archivo distinto de
> `_persistence/decisions.md` y `_persistence/tasks.md`.

⚠️ **Y el CENSO del protocolo si señala algo real, aunque no sea la refutacion de este supuesto.**
El censo que `D-107` estrena —universal y anclado— devuelve `assumptions.md` sobre el commit que creo
esta entrada; el CONTROL no, porque ninguna de las dos es una ranura de ancla vacia
(`git show <hash>:` al principio de la orden), sino el marcador dentro de un patron entrecomillado:

```
$ for f in $(git ls-tree -r --name-only f1f2291 _persistence _audit | grep -v '_audit/S-'); do n=$(git show f1f2291:"$f" | grep -cE '^\$ .*<hash>'); [ "$n" != "0" ] && echo "$f: $n"; done
_persistence/assumptions.md: 2
_persistence/decisions.md: 22
_persistence/tasks.md: 28

$ for f in $(git diff --name-only f1f2291^ f1f2291 -- _persistence _audit ":(exclude)_audit/S-025.md"); do n=$(git diff -U0 f1f2291^ f1f2291 -- "$f" | grep -cE '^\+\$ git show <hash>:'); [ "$n" != "0" ] && echo "$f: $n"; done
_persistence/decisions.md: 19
_persistence/tasks.md: 14
```

🔑 **Y esa diferencia entre los dos barridos es exactamente el reparto que `D-107` busca.** El
censo informa: hay dos lineas en un archivo que el Paso 7c-bis no puede tocar. El control no detiene
el cierre, porque ninguna de las dos esta **esperando un commit**. Lo que queda no es un fallo del
protocolo: es trabajo de `manager`, que es quien publica y quien ancla en este archivo — y es lo que
hace la nota de abajo.

**La primera de las dos, republicada en su forma anclada.** La original se corrio sobre el **arbol de
trabajo** —el mismo defecto que `F-070`—, y su salida corresponde al estado en que se escribio, antes
de que esta entrada existiera. Anclada al commit que la contiene devuelve otra cosa, y las dos van
aqui:

```
$ for f in $(git ls-tree -r --name-only f1f2291 _persistence _audit); do n=$(git show f1f2291:"$f" | grep -cE '^\$ .*<hash>'); [ "$n" != "0" ] && echo "$f: $n"; done
_audit/S-017.md: 1
_audit/S-024.md: 1
_audit/S-025.md: 13
_persistence/assumptions.md: 2
_persistence/decisions.md: 22
_persistence/tasks.md: 28
```

🔑 **La diferencia con lo publicado arriba se explica entera y no cambia la conclusion.**
`assumptions.md: 2` son las dos ordenes de esta entrada, que no existian cuando la orden se corrio;
`_audit/S-025.md: 13` es el informe de la sesion, que la orden original excluia. Los dos archivos que
importaban entonces —`decisions.md: 22` y `tasks.md: 28`— reproducen exactamente.

⚠️ **La segunda orden de esta entrada no se ancla, y no es un olvido:** es una **plantilla** del
criterio de refutacion, sin salida publicada. No afirma nada, asi que no hay nada que reproducir. Y
queda sustituida por el criterio nuevo de esta nota.

---

### A-012 - «Opera de forma sostenida con usuarios reales» se lee sobre el sistema de trabajo, no sobre el producto
| Campo | Valor |
|---|---|
| Fecha | 2026-09-07 |
| Estado | Abierto |
| Origen | manager |
| Dueno | `manager` |

- **Supuesto:** `_workflow/ai_levels.md` §6 separa el nivel 5 del 6 con una sola linea —«lo anterior
  **y** opera de forma sostenida con usuarios reales»— y no dice **quien** son esos usuarios.
  `_workflow/040_evol.md` §6 la lee sobre el **sistema de trabajo**: los usuarios son el equipo, y lo
  que sostiene la operacion es que la etapa **no tiene condicion de salida**. Sobre esa lectura
  descansa que el reparto de esa etapa se declare en **nivel 6**, el unico del metodo.
- **Por que se supone, y no se afirma:** la otra lectura es igual de defendible con el texto delante.
  Si «usuarios reales» son los del **producto**, la linea la cumpliria tambien la etapa del
  crecimiento —que termina con el producto desplegado y en uso real— y sin embargo su reparto se
  declaro en **5**. Las dos lecturas no pueden ser ciertas a la vez sin que uno de los dos archivos
  este mal, y hoy no hay nada en el metodo que zanje cual es.
- **Sobre que se construyo encima:** sobre esto se construyo la lectura de `_workflow/040_evol.md` §6
  y, con ella, su §6.1 — la cuarta pieza del harness, la **serie** de las tres metricas a lo largo de
  las vueltas, que es lo unico que el 6 anade sobre el 5. Si el supuesto cae, esa pieza sobra y el
  archivo dice de mas.
- **Lo que NO depende de esto, y conviene separarlo:** los tres ejes en `3` —impacto, variabilidad de
  la entrada y volumen— no dependen de ninguna lectura: salen de lo que `_phases/040_evol.md` dice de
  si misma. Con o sin este supuesto, el nivel **no baja de 5** y el harness sigue sin ser opcional.
  Lo que esta en juego es el escalon, no la obligacion.
- **Como se refuta:** que el usuario, o una revision independiente, lea la linea sobre los usuarios
  del **producto**; o que otro archivo de reparto del metodo aplique la lectura contraria a la misma
  linea, lo que dejaria dos lecturas vivas del mismo criterio.
- **Disparador:** el momento en que se adopte el reparto de esa etapa —su `D-XXX`, al abrirla—, que
  es cuando la lectura deja de ser una linea escrita y pasa a costar dinero. Y antes de eso,
  cualquier auditoria que lea `_workflow/040_evol.md` §6.
- ⚠️ **No se escala hoy porque no hay nada que decidir todavia.** La etapa esta a dos Gates de
  distancia y sin declarar; lo clasifico como reversible a criterio —es un parrafo de un archivo
  agnostico que nadie ha adoptado—, y por eso se registra como supuesto en vez de bloquear.
