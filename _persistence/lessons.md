# lessons.md

> Registro de las **lecciones aprendidas** durante la ejecucion del proyecto.
> Cada leccion tiene codigo `L-XXX`.

---

## Indice

| Codigo | Leccion | Fecha | Etapa |
|---|---|---|---|
| [L-001](#l-001---un-archivo-que-describe-el-estado-de-hoy-envejece-mintiendo) | Un archivo que describe el estado de hoy envejece mintiendo | 2026-08-31 | 000_preproject |
| [L-002](#l-002---un-metodo-traido-de-otro-proyecto-llega-con-sus-codigos-y-esos-no-viajan) | Un metodo traido de otro proyecto llega con sus codigos, y esos no viajan | 2026-08-31 | 000_preproject |
| [L-003](#l-003---el-mismo-control-en-dos-sitios-tiene-que-ser-literalmente-el-mismo-comando) | El mismo control en dos sitios tiene que ser literalmente el mismo comando | 2026-08-31 | 000_preproject |
| [L-004](#l-004---un-encabezado-que-cuenta-se-desincroniza-de-lo-que-cuenta) | Un encabezado que cuenta se desincroniza de lo que cuenta | 2026-08-31 | 000_preproject |
| [L-005](#l-005---renombrar-un-agente-no-es-renombrar-su-archivo) | Renombrar un agente no es renombrar su archivo | 2026-08-31 | 000_preproject |
| [L-006](#l-006---un-bloque-de-verificacion-declara-su-ambito-dentro-del-enunciado) | Un bloque de verificacion declara su ambito dentro del enunciado | 2026-09-01 | 000_preproject |
| [L-007](#l-007---una-excepcion-se-escribe-donde-esta-la-regla-no-donde-se-decidio) | Una excepcion se escribe donde esta la regla, no donde se decidio | 2026-09-01 | 000_preproject |
| [L-008](#l-008---una-leccion-escrita-solo-como-leccion-no-cambia-la-entrada-siguiente) | Una leccion escrita solo como leccion no cambia la entrada siguiente | 2026-09-01 | 000_preproject |
| [L-009](#l-009---un-hallazgo-acota-su-ejemplo-no-el-defecto) | Un hallazgo acota su ejemplo, no el defecto | 2026-09-02 | 000_preproject |

---

## Convenciones

| Campo | Valores posibles |
|---|---|
| Codigo | `L-XXX`, correlativo, no se reutiliza |
| Origen | `usuario` / `manager` / `report_auditor` |

Cada leccion registra: contexto, que ocurrio, leccion y como aplicarla.

🚨 **Una leccion sin «como aplicarla» es una anecdota.** El campo que la convierte en leccion es la
accion concreta a futuro; si no se puede escribir, lo que hay todavia no es una leccion.

⚠️ **El titulo enuncia la leccion, no el incidente.** Se lee como regla, no como cronica.

🚨 **El indice se escribe a mano, sin generador.** Cada fila enlaza por ancla a su leccion.

---

## Lecciones

### L-001 - Un archivo que describe el estado de hoy envejece mintiendo
| Campo | Valor |
|---|---|
| Fecha | 2026-08-31 |
| Etapa | 000_preproject |
| Origen | usuario |

- **Contexto:** al pedir que toda la maquinaria fuera agnostica, el barrido no encontro ni un
  nombre, ni una ruta, ni un host fuera de `project.md`.
- **Que ocurrio:** lo que si encontro fueron ocho frases que describian **el momento presente**:
  «hoy `project.md` esta vacio», «hoy no existe el contrato», «no existe ninguna tabla de acciones
  irreversibles». Ninguna llevaba un dato propio, y todas eran no agnosticas.
- **Leccion:** un dato del proyecto se detecta con un `grep`; **una foto del presente, no**. Y es
  peor que el dato, porque el dato solo estorba al copiar el archivo: la foto **caduca en su sitio**
  y sigue ahi afirmando lo contrario, sin que nadie relea un archivo que funciona.
- **Como aplicarla:** en cualquier archivo reutilizable, escribir **condiciones y no estados**: «si
  `project.md` no declara X…», nunca «hoy X esta vacio». Si una frase empieza por «hoy», «todavia no»
  o «por ahora», o se reescribe como condicion o se muda al archivo de estado.

---

### L-002 - Un metodo traido de otro proyecto llega con sus codigos, y esos no viajan
| Campo | Valor |
|---|---|
| Fecha | 2026-08-31 |
| Etapa | 000_preproject |
| Origen | usuario |

- **Contexto:** los protocolos, agentes y archivos de persistencia se adaptaron desde un proyecto
  anterior que el usuario aporto como guia.
- **Que ocurrio:** el material venia tejido con codigos de aquel proyecto —decisiones, hallazgos,
  auditorias, tareas— usados justamente para **justificar por que existe cada control**. Aqui no
  apuntaban a nada. Borrarlos sin mas habria dejado reglas sin argumento; conservarlos habria
  prometido una trazabilidad inexistente.
- **Leccion:** al adoptar un metodo ajeno hay que separar **la regla de su procedencia**. La regla
  viaja; la traza no. Y el argumento que sostiene la regla **tambien viaja**, reescrito como
  principio en vez de como anecdota.
- **Como aplicarla:** al traer material de fuera, `grep` de los patrones de codigo del origen antes
  de darlo por adaptado, y reescribir cada justificacion en forma general —«un control que avisa de
  todo termina apagado»— en lugar de citar el incidente que la origino. **Un control sin argumento
  escrito es el primero que alguien borra por ruidoso.**

---

### L-003 - El mismo control en dos sitios tiene que ser literalmente el mismo comando
| Campo | Valor |
|---|---|
| Fecha | 2026-08-31 |
| Etapa | 000_preproject |
| Origen | manager |

- **Contexto:** la comprobacion de coherencia entre el indice y el detalle de los archivos de
  `_persistence/` la corren dos protocolos distintos: el cierre y el arranque.
- **Que ocurrio:** el material de origen traia **dos versiones del mismo control**. La del cierre
  filtraba los bloques de codigo cercados con `awk`; la del arranque, no. Con el registro guardando
  salida cruda de comandos como evidencia, la version sin filtro habria señalado como huerfano
  cualquier codigo citado dentro de un bloque de ejemplo.
- **Leccion:** dos controles que dicen comprobar lo mismo y no son el mismo comando **acaban dando
  respuestas distintas**, y entonces uno de los dos miente sin que nadie sepa cual. Una alarma que
  siempre resulta falsa se aprende a ignorar, y el dia que sea verdadera tampoco se mirara.
- **Como aplicarla:** cuando un control aparezca en mas de un sitio, copiarlo **literal** y dejar
  escrito en ambos que tiene que seguir siendo el mismo. Si conviene que difieran, esa diferencia es
  una decision y va con su razon escrita.

---

### L-004 - Un encabezado que cuenta se desincroniza de lo que cuenta
| Campo | Valor |
|---|---|
| Fecha | 2026-08-31 |
| Etapa | 000_preproject |
| Origen | manager |

- **Contexto:** el protocolo de arranque traia una seccion titulada «Cinco desfases que hay que
  reportar».
- **Que ocurrio:** la tabla listaba **seis** filas, y el texto de debajo se referia a «la cuarta»,
  «la quinta» y «la tercera» contando sobre seis. El encabezado era lo unico equivocado: alguien
  añadio una fila y no toco el titulo.
- **Leccion:** un numero escrito en prosa **es un duplicado del contenido**, y como todo duplicado
  se desincroniza en cuanto uno de los dos cambia. Aqui ademas era un duplicado silencioso: nada
  falla, solo queda un titulo que miente.
- **Como aplicarla:** no poner recuentos en titulos ni en prosa cuando lo contado esta en una tabla
  al lado. Si hay que referirse a filas concretas, **numerar la tabla** y citar por numero de fila,
  que es lo que se hizo aqui.

---

### L-005 - Renombrar un agente no es renombrar su archivo
| Campo | Valor |
|---|---|
| Fecha | 2026-08-31 |
| Etapa | 000_preproject |
| Origen | manager |

- **Contexto:** se pidio que el agente de auditoria pasara a llamarse `report_auditor.md`. La
  peticion nombraba un archivo.
- **Que ocurrio:** el nombre por el que se invoca un agente sale del campo `name:` de su
  frontmatter, no de como se llame el archivo. Renombrar solo el archivo habria dejado el agente
  respondiendo todavia a `auditor`, con un `.md` llamado de otra forma. **No falla en ningun sitio:**
  el agente sigue funcionando, y la incoherencia solo la paga quien lea el repositorio despues.
- **Leccion:** el identificador de un agente vive en tres capas —nombre de archivo, `name:` del
  frontmatter, y cada referencia escrita en protocolos y registros—, y un rename solo esta hecho
  cuando las tres coinciden.
- **Como aplicarla:** ante cualquier rename de agente o skill, cambiar archivo y `name:` a la vez, y
  cerrar con un barrido de identificadores cuya salida esperada sea **cero lineas**:

```bash
git grep -nE '`<viejo>`|\*\*<viejo>\*\*|name: <viejo>' -- .claude CLAUDE.md project.md
```

  Lo que salga fuera de ese ambito —entradas ya cerradas, informes entregados— **no se toca**: se
  deja y se enlaza con la `D-XXX` del rename.

🕒 **Matizado el 2026-09-01 por `L-006`, tras `F-001` y `F-002`.** Acotar el barrido a esas
tres rutas **antes** de mirar es lo que dejo fuera dos referencias vivas. El barrido se corre sobre
el repositorio entero y **luego** se clasifica cada coincidencia en viva o historica.

---

### L-006 - Un bloque de verificacion declara su ambito dentro del enunciado
| Campo | Valor |
|---|---|
| Fecha | 2026-09-01 |
| Etapa | 000_preproject |
| Origen | report_auditor |

- **Contexto:** el rename de `auditor` a `report_auditor` (`D-016`) se cerro con un bloque titulado
  «Verificacion — cero identificadores `auditor` vivos» y un `git grep` con `exit=1`. El titulo no
  decia sobre que corrio; el comando cubria `.claude`, `CLAUDE.md` y `project.md`.
- **Que ocurrio:** la auditoria `R-002` corrio el mismo patron sobre `_persistence/` y devolvio 18
  lineas, y encontro dos referencias vivas al handle viejo (`F-002`). El `exit=1` era cierto; lo
  falso era la frase que lo acompanaba. Nada fallo: el registro simplemente dio por cerrado un
  ambito que nadie habia mirado.
- **Leccion:** un `exit=1` solo prueba lo que estaba dentro del `--` del comando. **El enunciado de
  un bloque de verificacion no puede ser mas ancho que su ambito**, y un barrido acotado antes de
  mirar es una conclusion disfrazada de comprobacion.
- **Como aplicarla:** dos reglas, y las dos son baratas:
  1. **Barrer primero el repositorio entero**, y solo despues clasificar cada coincidencia. Acotar
     es el ultimo paso, no el primero.
  2. **El titulo del bloque nombra su ambito**, literal: «cero identificadores `X` vivos **en
     `.claude`, `CLAUDE.md` y `project.md`**». Si el titulo no cabe sin el ambito, el ambito es el
     que esta mal.

  Cuando un bloque ya escrito afirma de mas, se corrige por nota fechada y no reescribiendolo:
  `D-019`.

---

### L-007 - Una excepcion se escribe donde esta la regla, no donde se decidio
| Campo | Valor |
|---|---|
| Fecha | 2026-09-01 |
| Etapa | 000_preproject |
| Origen | report_auditor |

- **Contexto:** `D-020` decidio que `manager` puede escribir en `tasks.md` al registrar un hallazgo
  aceptado, y dejo la tension **declarada dentro de la propia decision**. La convencion de
  `tasks.md` siguio diciendo, en absoluto, que el archivo no se escribe a mano durante la jornada.
- **Que ocurrio:** `R-003` lo abrio como `F-007`. Nada fallo al ejecutar: la excepcion era correcta
  y el usuario la confirmo despues. Lo que fallaba era **donde estaba escrita**. Quien abriera
  `tasks.md` sin haber leido `D-020` veia una prohibicion absoluta y cuatro tareas incumpliendola a
  la vista, y de ahi solo salen dos lecturas, las dos malas: que la regla no rige, o que el trabajo
  esta mal hecho.
- **Leccion:** declarar una tension en el cuerpo de la decision que la crea **no la registra**: la
  deja donde solo la encuentra quien ya sabia que existia. Una regla y su excepcion se leen juntas o
  no se leen — y la regla es el sitio donde la gente mira, no la decision.
- **Como aplicarla:** al registrar una `D-XXX` que abre una excepcion a una regla ya escrita, la
  misma pasada toca **los dos sitios**: la decision, con su porque; y **el texto de la regla**, con
  la excepcion enunciada, acotada y citando la `D-XXX`. Si la regla vive en mas de un archivo
  —protocolo, agente, convencion—, van todos, o el siguiente lector encontrara el que quedo sin
  tocar. La comprobacion es barata: `git grep` del enunciado absoluto, y que cada sitio que lo
  repite lleve la excepcion al lado.

---

### L-008 - Una leccion escrita solo como leccion no cambia la entrada siguiente
| Campo | Valor |
|---|---|
| Fecha | 2026-09-01 |
| Etapa | 000_preproject |
| Origen | report_auditor |

- **Contexto:** `L-006` —«un bloque de verificacion declara su ambito dentro del enunciado»— se
  escribio en `S-003` a raiz de `F-001`. La entrada inmediatamente posterior, `D-021`, escrita en
  `S-004`, reincidio en el mismo defecto: `R-004` la abrio como `F-008`. Entre medias, `F-006`
  encontro el mismo fallo **dentro de la propia correccion de `F-001`**.
- **Que ocurrio:** tres hallazgos del mismo patron en tres sesiones seguidas, con la leccion ya
  escrita en las tres. Nadie la incumplio por descuido de lectura: `L-006` hablaba del ambito **de
  rutas**, y lo que fallaba era el **temporal** —un recuento tomado antes de que el cierre
  terminara de escribir el registro—. La leccion era correcta y no cubria el caso, y como estaba
  guardada en `lessons.md` y no en el sitio donde se escriben los bloques, nada la puso delante de
  quien iba a repetir el fallo.
- **Leccion:** una leccion que solo vive en `lessons.md` **no tiene ningun mecanismo que la
  aplique**. `lessons.md` es memoria, no control: lo lee quien va a buscarla, y quien esta a punto
  de repetir el error no sabe que tiene que buscarla. La reincidencia en la entrada siguiente no es
  una anecdota — es la prueba de que el registro se hizo y el cambio no.
- **Como aplicarla:** cuando una leccion se repita, deja de tratarla como leccion. Convertirla en
  **una regla escrita donde se hace el trabajo** —la convencion del archivo, el paso del protocolo,
  la plantilla— que es lo que dice `L-007`; y, si se puede, en **un comando que la compruebe**, que
  es lo unico que no depende de que alguien se acuerde. `D-022` es ese paso para este caso concreto:
  la regla existe, y lo que queda pendiente es llevarla al sitio donde se aplica.
- ⚠️ **La señal que hay que mirar:** una leccion con dos hallazgos del mismo patron detras ya
  fallo como leccion. La tercera repeticion no aporta informacion nueva; solo confirma que se estaba
  registrando en vez de corrigiendo.

---

### L-009 - Un hallazgo acota su ejemplo, no el defecto
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Etapa | 000_preproject |
| Origen | manager |

- **Contexto:** al corregir los cuatro hallazgos de `R-005`, dos de ellos resultaron describir menos
  de lo que pasaba. `F-013` decia que una entrada conservaba una advertencia ya desmentida; ademas,
  esa advertencia **describia mal el ambito anterior del control** —nombraba tres rutas donde habia
  dos—. `F-014` señalaba una frase con dos errores en una seccion; el mismo error estaba en **tres
  secciones**, y llevaba ademas un **tercer** error de recuento que el hallazgo no menciona.
- **Que ocurrio:** en los dos casos, corregir literalmente lo que el hallazgo cita habria dejado el
  defecto vivo en sitios que nadie estaba mirando — y con la fila del hallazgo diciendo
  `Aceptado — pendiente`, es decir, con el asunto aparentemente encaminado.
- **Por que pasa, y no es un descuido del auditor:** el auditor abre un hallazgo **con la evidencia
  que encontro**, y con una es suficiente para abrirlo. Localizar todas las instancias es trabajo de
  la correccion, no de la deteccion. Un hallazgo bien escrito prueba que el defecto existe; **no
  promete que sea el unico sitio donde vive.**
- **Leccion:** la cita de un hallazgo es **una muestra, no un inventario**. Aceptar un hallazgo
  obliga a barrer el defecto entero antes de darlo por corregido; leerlo como una lista de tareas
  cerrada convierte la correccion en parcial y, peor, en **parcial con aspecto de completa**.
- **Como aplicarla:** al aceptar un `F-NNN`, antes de corregir, **construye el patron que caza el
  defecto** y correlo sobre el ambito donde pueda vivir. Si devuelve mas lineas que las citadas, esas
  entran en la misma `T-XXX` — no son hallazgos nuevos, son el mismo defecto. Y **el patron y su
  ambito se registran** en la tarea, junto con lo que devolvio: es lo unico que distingue «corregi
  todas» de «corregi las que me señalaron».
- **Donde queda aplicada:** `T-015`, `T-016`, `T-017` y `T-018` llevan cada una el barrido con el que
  se comprobo el alcance real, y `T-017` y `T-016` registran explicitamente lo que el hallazgo no
  nombraba.
