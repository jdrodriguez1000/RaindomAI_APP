# lessons.md

> Registro de las **lecciones aprendidas** durante la ejecucion del proyecto.
> Cada leccion tiene codigo `L-XXX`.

---

## Indice

| Codigo | Leccion | Fecha | Etapa | Portabilidad |
|---|---|---|---|---|
| [L-001](#l-001---un-archivo-que-describe-el-estado-de-hoy-envejece-mintiendo) | Un archivo que describe el estado de hoy envejece mintiendo | 2026-08-31 | 000_preproject | Sin evaluar |
| [L-002](#l-002---un-metodo-traido-de-otro-proyecto-llega-con-sus-codigos-y-esos-no-viajan) | Un metodo traido de otro proyecto llega con sus codigos, y esos no viajan | 2026-08-31 | 000_preproject | Sin evaluar |
| [L-003](#l-003---el-mismo-control-en-dos-sitios-tiene-que-ser-literalmente-el-mismo-comando) | El mismo control en dos sitios tiene que ser literalmente el mismo comando | 2026-08-31 | 000_preproject | Sin evaluar |
| [L-004](#l-004---un-encabezado-que-cuenta-se-desincroniza-de-lo-que-cuenta) | Un encabezado que cuenta se desincroniza de lo que cuenta | 2026-08-31 | 000_preproject | Sin evaluar |
| [L-005](#l-005---renombrar-un-agente-no-es-renombrar-su-archivo) | Renombrar un agente no es renombrar su archivo | 2026-08-31 | 000_preproject | Sin evaluar |
| [L-006](#l-006---un-bloque-de-verificacion-declara-su-ambito-dentro-del-enunciado) | Un bloque de verificacion declara su ambito dentro del enunciado | 2026-09-01 | 000_preproject | Sin evaluar |
| [L-007](#l-007---una-excepcion-se-escribe-donde-esta-la-regla-no-donde-se-decidio) | Una excepcion se escribe donde esta la regla, no donde se decidio | 2026-09-01 | 000_preproject | Sin evaluar |
| [L-008](#l-008---una-leccion-escrita-solo-como-leccion-no-cambia-la-entrada-siguiente) | Una leccion escrita solo como leccion no cambia la entrada siguiente | 2026-09-01 | 000_preproject | Sin evaluar |
| [L-009](#l-009---un-hallazgo-acota-su-ejemplo-no-el-defecto) | Un hallazgo acota su ejemplo, no el defecto | 2026-09-02 | 000_preproject | Sin evaluar |
| [L-010](#l-010---un-criterio-de-cierre-cuyo-ambito-incluye-el-registro-no-puede-cumplirse-nunca) | Un criterio de cierre cuyo ambito incluye el registro no puede cumplirse nunca | 2026-09-02 | 000_preproject | Sin evaluar |
| [L-011](#l-011---un-mecanismo-escrito-como-aviso-se-salta-escrito-como-hueco-de-la-plantilla-no) | Un mecanismo escrito como aviso se salta; escrito como hueco de la plantilla, no | 2026-09-02 | 000_preproject | Sin evaluar |
| [L-012](#l-012---un-barrido-que-busca-texto-de-prosa-se-corre-insensible-a-mayusculas-o-no-barre) | Un barrido que busca texto de prosa se corre insensible a mayusculas, o no barre | 2026-09-02 | 000_preproject | Sin evaluar |
| [L-013](#l-013---un-bloque-de-verificacion-sin-ancla-caduca-el-codigo-de-salida-no-prueba-una-ausencia) | Un bloque de verificacion sin ancla caduca; el codigo de salida no prueba una ausencia | 2026-09-02 | 000_preproject | Sin evaluar |
| [L-014](#l-014---una-carpeta-agnostica-nueva-necesita-cuatro-enganches-y-el-cuarto-es-el-que-se-olvida) | Una carpeta agnostica nueva necesita cuatro enganches, y el cuarto es el que se olvida | 2026-09-02 | 000_preproject | Sin evaluar |
| [L-015](#l-015---una-correccion-escrita-en-una-seccion-que-el-cierre-sobrescribe-no-es-una-correccion) | Una correccion escrita en una seccion que el cierre sobrescribe no es una correccion | 2026-09-02 | 000_preproject | Sin evaluar |
| [L-016](#l-016---una-consulta-que-cambia-lo-que-haces-no-deja-rastro-y-sin-rastro-no-ocurrio) | Una consulta que cambia lo que haces no deja rastro, y sin rastro no ocurrio | 2026-09-02 | 000_preproject | Sin evaluar |
| [L-017](#l-017---una-condicion-de-salida-no-es-una-tarea-pendiente-y-confundirlas-desactiva-el-disparador) | Una condicion de salida no es una tarea pendiente, y confundirlas desactiva el disparador | 2026-09-02 | 000_preproject | Sin evaluar |
| [L-018](#l-018---un-archivo-traido-de-otro-proyecto-destapa-contradicciones-que-alli-no-existian) | Un archivo traido de otro proyecto destapa contradicciones que alli no existian | 2026-09-02 | 000_preproject | Sin evaluar |
| [L-019](#l-019---un-control-documentado-sobre-una-parte-de-su-propia-salida-no-es-el-control) | Un control documentado sobre una parte de su propia salida no es el control | 2026-09-02 | 000_preproject | Sin evaluar |
| [L-020](#l-020---una-regla-que-dice-que-registrar-pero-no-donde-no-se-incumple-se-evapora) | Una regla que dice QUE registrar pero no DONDE no se incumple: se evapora | 2026-09-03 | 000_preproject | Sin evaluar |
| [L-021](#l-021---un-barrido-con-git-grep-sobre-archivos-sin-versionar-devuelve-cero-por-no-verlos) | Un barrido con `git grep` sobre archivos sin versionar devuelve cero por no verlos | 2026-09-02 | 000_preproject | Sin evaluar |
| [L-022](#l-022---una-garantia-se-comprueba-contra-el-mecanismo-no-contra-lo-que-el-mecanismo-sugiere) | Una garantia se comprueba contra el mecanismo, no contra lo que el mecanismo sugiere | 2026-09-03 | 000_preproject | Sin evaluar |
| [L-023](#l-023---un-dato-derivable-escrito-a-mano-se-equivoca-justo-donde-nadie-lo-vuelve-a-mirar) | Un dato derivable escrito a mano se equivoca justo donde nadie lo vuelve a mirar | 2026-09-03 | 000_preproject | Sin evaluar |
| [L-024](#l-024---una-orden-publicada-se-reejecuta-antes-de-publicarla-copiarla-la-puede-corromper-en-silencio) | Una orden publicada se reejecuta antes de publicarla: copiarla la puede corromper en silencio | 2026-09-03 | 000_preproject | Sin evaluar |
| [L-025](#l-025---un-patron-con-limite-de-palabra-es-ciego-a-los-prefijos-mas-largos-que-empiezan-igual) | Un patron con limite de palabra es ciego a los prefijos mas largos que empiezan igual | 2026-09-03 | 000_preproject | Sin evaluar |
| [L-026](#l-026---un-enganche-de-uso-escrito-en-generico-no-engancha-tiene-que-nombrar-el-archivo) | Un enganche de uso escrito en generico no engancha: tiene que nombrar el archivo | 2026-09-03 | 000_preproject | Sin evaluar |
| [L-027](#l-027---cuando-existe-la-orden-que-produce-una-lista-escribirla-a-mano-es-el-error-no-el-atajo) | Cuando existe la orden que produce una lista, escribirla a mano es el error, no el atajo | 2026-09-03 | 000_preproject | Sin evaluar |

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

**Y una columna que solo vive en el indice: `Portabilidad`.** Dice si esa leccion sube al archivo de
lecciones globales, y es lo que hace que la cosecha se pueda comprobar.

| Valor | Significa |
|---|---|
| `Sin evaluar` | todavia no ha pasado por los cuatro filtros. Es el valor de partida de toda leccion nueva |
| `Global candidata` | pasa los cuatro filtros y esta pendiente de subir |
| `Promovida a LG-NN` | ya esta en el archivo global, con su codigo |
| `Ya cubierta por LG-NN` | el archivo global ya lo dice. **No se sube**, y se anota cual lo cubre |
| `Solo proyecto` | no sobrevive al cambio de lenguaje, libreria o dominio |

🔑 **Vive en el indice y en ningun sitio mas.** No se repite dentro de la ficha: un estado escrito en
dos sitios acaba diciendo dos cosas, y entonces no se sabe cual manda. Ademas la cosecha es un
barrido —se lee una columna, no quince fichas—, y para eso el indice es el sitio.

⚠️ **`Sin evaluar` no significa «no sube»: significa que nadie lo ha mirado.** Los dos se parecen al
leerlos deprisa, y confundirlos deja la cosecha hecha sobre lecciones que nunca se evaluaron.

🚨 **Los cuatro filtros no estan aqui: viven en el archivo global**, en su seccion de promocion, y se
leen alli en el momento de cosechar. Copiarlos a este archivo crearia una segunda copia que
envejeceria por su cuenta.

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

> 📌 **Reincidencia del 2026-09-03 (sesion `S-017`).** El defecto volvio, esta vez en
> `_phases/020_baseline.md` §5: el texto decia «Ocho artefactos de registro» sobre una tabla de
> **nueve** filas. Se corrigio a «Nueve» por decision del usuario (`D-074`).
>
> ```
> $ sed -n '/^## 5. Artefactos que produce/,/^Y \*\*el esqueleto/p' _phases/020_baseline.md | grep -c "^| \*\*"
> 9
> ```
>
> 🔑 **Lo que enseña la reincidencia no es el error, es su alcance.** La leccion se escribio mirando
> un protocolo y se aplico a los protocolos; nadie la llevo a `_phases/`, que se escribio despues.
> Una leccion se aplica donde se mira, y donde no se mira sigue intacta — que es exactamente lo que
> dice `L-008`.

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

📌 **Nota del 2026-09-02 (`S-012`) — esta leccion se cumplio a si misma.** `D-059` abrio una
excepcion a `PI-5` y la escribio **solo** en el archivo de etapa; `CLAUDE.md` siguio diciendo «No hay
una tercera casilla» en absoluto. Es `L-007` incumplida **por quien la tenia escrita y la habia
leido esa misma jornada** — y no se detecto sola: la encontro el usuario al pedir «revisa que otros
archivos se deben actualizar». Es la prueba mas directa de lo que esta leccion dice: **una leccion
escrita no cambia la pasada siguiente si nada la dispara.** Lo que faltaba no era conocerla, sino un
paso que preguntara «¿esta `D-XXX` abre una excepcion a una regla ya escrita?» en el momento de
registrarla.

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

---

### L-010 - Un criterio de cierre cuyo ambito incluye el registro no puede cumplirse nunca
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Etapa | 000_preproject |
| Origen | manager |

- **Contexto:** `T-015` se cerro con el criterio «el barrido de la regla no devuelve ningun enunciado
  que siga afirmando que la excepcion es unica». `F-016` lo corrio y devolvio uno. Al corregirlo,
  aparecio algo que el hallazgo no decia: **ese criterio no podia dar cero en ningun escenario**. El
  barrido incluye `_persistence/tasks.md`, y el cuerpo de la propia `T-015` cita el texto viejo
  literalmente para explicar que se corrigio; `_audit/` guarda lo mismo en cada hallazgo. Ninguno de
  los dos se reescribe (`D-019`).
- **Que ocurrio:** el criterio no fallo por lo que no se hizo, sino por como estaba escrito. Y el
  intento de verificarlo cayo en el mismo agujero: **el primer bloque de verificacion que escribi
  para `T-021` se barria a si mismo** —el patron estaba dentro del ambito, en el archivo que el
  bloque estaba escribiendo—, y por tanto tampoco se reproducia sobre su propio commit.
- **Por que es distinto de `L-006` y `D-022`, aunque suene igual:** aquello era sobre **recuentos de
  ambito global** en un archivo que la sesion todavia iba a tocar, y se resolvia fechandolos. Esto es
  sobre **criterios de cierre**, y fecharlos no arregla nada: un criterio existe para poder correrse
  mas tarde. Lo que hay que acotar es el ambito, no la fecha.
- **Leccion:** un criterio de cierre se escribe sobre **el sitio donde vive el defecto**, nunca sobre
  el repositorio entero. Todo registro que documenta una correccion —el hallazgo, la tarea, la
  auditoria— cita el texto defectuoso para explicarse; incluir ese registro en el ambito garantiza
  coincidencias para siempre, y entonces el criterio no mide si se arreglo, mide si alguien lo
  escribio.
- **Como aplicarla, y hay dos casillas:**
  - **Al escribir el criterio:** nombra el ambito —«en `.claude`, `CLAUDE.md` y `_phases/`»— y
    **enumera lo que puede quedar y por que no cuenta**. Un criterio que espera exactamente dos
    coincidencias conocidas es mas util que uno que espera cero y nunca lo consigue.
  - **Al escribir el bloque que lo verifica:** comprueba que el ambito **no incluye el archivo donde
    estas escribiendo el bloque**. Si lo incluye, el bloque se caza a si mismo en cuanto se guarda.
- **Donde queda aplicada:** `T-021` lleva el criterio acotado y sus dos bloques de verificacion
  reproducibles, y `T-015` lleva la nota fechada que precisa como debia leerse el suyo.

⚠️ **Esta leccion todavia no tiene mecanismo**, y por `L-008` eso significa que depende de que quien
escriba el proximo criterio se acuerde. El Paso 6 de `protocol-close` (`T-019`) ya marca los bloques
de verificacion cuyo ambito alcanza lo que el cierre reescribe — es el mismo tipo de control, y
ampliarlo a los criterios de cierre es candidato natural si el patron reaparece.

---

### L-011 - Un mecanismo escrito como aviso se salta; escrito como hueco de la plantilla, no
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Etapa | 000_preproject |
| Origen | manager |

- **Contexto:** `F-019` señalo que la seccion 1 de `_audit/S-007.md` presenta su lista de archivos
  como salida de un comando y no coincide con el. Al ir a corregirlo aparecio lo incomodo: **el
  mecanismo ya existia**. `protocol-close` avisa desde antes de que las dos listas del informe se
  generan, y ademas advierte de que «el cierre anade archivos que no son de contenido —la fila de
  `_audit/index.md`, el propio informe— y son justo los que se olvidan al escribir de memoria».
  Estaba escrito, con el ejemplo exacto del error que despues se cometio.
- **Que ocurrio:** el aviso vivia en un bloque explicativo, tres pantallas por encima de la
  estructura del informe. Se lee una vez, al aprender el protocolo; no se vuelve a leer al escribir
  la seccion. La estructura, en cambio, se tiene delante mientras se redacta.
- **Por que no es `L-008` otra vez:** `L-008` dice que una **leccion** sin mecanismo no evita la
  reincidencia. Esto es un paso mas alla y mas desagradable: **habia mecanismo, y tampoco la
  evito**, porque estaba en el sitio donde se explica y no en el sitio donde se ejecuta.
- **Leccion:** un mecanismo se pone **donde se hace el trabajo**, no donde se explica el trabajo. La
  prueba es concreta: si la regla se puede incumplir sin haber tenido que leerla, todavia no es un
  mecanismo — es un aviso.
- **Como aplicarla:** cuando una regla diga «esto se genera, no se escribe de memoria», el sitio
  correcto es **el hueco de la plantilla**, redactado como orden de pegar la salida. Una salida
  pegada tampoco puede quedarse corta: o esta entera, o se nota. Un texto redactado a partir de ella
  siempre puede.
- **Donde queda aplicada:** `T-025`, en la estructura del informe de `protocol-close`.

---

### L-012 - Un barrido que busca texto de prosa se corre insensible a mayusculas, o no barre
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Etapa | 000_preproject |
| Origen | report_auditor |

- **Contexto:** `T-021` barrio las variantes de una regla mal enunciada y concluyo que no quedaba
  ninguna viva. `F-018` rehizo el barrido y encontro una que sus patrones no alcanzaban:
  `.claude/agents/session-closer.md:90`, que abre frase y por tanto escribe «Unica excepcion» con
  mayuscula inicial.
- **Que ocurrio:** el fondo de `T-021` estaba bien —esa linea es de otra regla, la de los supuestos
  `A-XXX`— pero **lo estaba por casualidad**. El patron escrito no la habria encontrado nunca, y si
  hubiera sido un resto de la regla vieja habria sobrevivido al barrido sin que nadie lo notara.
- **Leccion:** un barrido sobre **texto de prosa** —una frase, un enunciado, una regla redactada—
  corre con `-i`. La misma frase aparece en minuscula en mitad de un parrafo, en mayuscula al
  empezar uno, y en cursiva o negrita en el tercero. Un barrido sobre **identificadores** (`T-020`,
  `F-017`, `A-XXX`) es lo contrario: ahi la mayuscula es parte del codigo y `-i` mete ruido.
- **Como aplicarla:** al escribir el bloque de verificacion, pregunta que se esta buscando. **Prosa
  → `grep -i`.** **Codigo → `grep` sin `-i`.** Y si el resultado esperado es «cero», correr las dos
  formas cuesta un segundo y la diferencia entre ellas es exactamente el agujero.
- **Un aviso de este entorno, que costo descubrir:** las clases de caracteres acentuados
  (`[aeiou]` con tildes) **no son fiables** con el `grep` de este `git bash`: compara byte a byte, y
  la tilde comparte primer byte con la eñe, asi que un patron de vocales acentuadas devuelve lineas
  que solo llevan eñes. Para comprobar acentos hay que usar `python`, no `grep`.
- **Donde queda aplicada:** `T-024`, en el tercer bloque de verificacion de `T-021`.

---

### L-013 - Un bloque de verificacion sin ancla caduca; el codigo de salida no prueba una ausencia
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Etapa | 000_preproject |
| Origen | report_auditor |

- **Contexto:** `F-022` desmintio de una sola pasada los bloques de verificacion de `D-036`, `D-038`
  y `D-040`. Los tres afirmaban un resultado que no sale al correr su orden literal, y en los tres el
  **fondo era correcto**: lo que fallaba era la orden escrita, no lo que se quiso demostrar.
- **Que ocurrio, y son tres fallos distintos con la misma consecuencia:**
  1. **Patron demasiado ancho.** `grep -n "_discovery" project.md` se escribio para probar que la
     carpeta no tenia fila propia, pero `_discovery` sin barra tambien casa con `005_discovery`, que
     el archivo ya usaba diez veces.
  2. **Barrido sin anclar.** `grep -rnoE "\bI-[0-9]{3}\b" ...` daba cero **antes** de escribir la
     decision y deja de darlo en cuanto la decision se escribe: la propia entrada introduce las
     coincidencias que decia no haber. Al dia siguiente el bloque se lee como una falsedad.
  3. **Codigo de salida usado como prueba de ausencia.** `git status --porcelain ; echo "exit=$?"`
     sale con `0` tanto si hay cambios como si no. El codigo de salida de `git status` no dice nada
     sobre si hubo salida.
- **Leccion:** un bloque de verificacion tiene que seguir siendo cierto **manana**, corrido por
  alguien que no vivio la sesion. Tres reglas, una por fallo: **el patron se acota a lo que se quiere
  demostrar** (si se prueba una fila, se busca la fila, no la cadena suelta); **lo que la propia
  entrada va a cambiar se ancla al commit** con `git grep <sha>` o `git show <sha>:archivo`, nunca al
  arbol de trabajo; y **una ausencia se prueba con el recuento** (`| wc -l` → `0`) o con la salida
  vacia pegada, jamas con `exit=`, salvo en las ordenes cuyo codigo de salida si significa «no hubo
  coincidencias», como `grep`.
- **Por que importa mas de lo que parece:** un bloque que no se reproduce **cuesta mas que no
  tenerlo**. Obliga a rehacer el barrido y ademas a averiguar si la diferencia es un error de
  transcripcion o una afirmacion falsa — y el auditor acaba haciendo el trabajo entero como si nunca
  se hubiera escrito. La familia `F-005`, `F-008`, `F-011` y `F-022` es la mas reincidente del
  registro.
- **Y una consecuencia que no es obvia:** cuando el fallo se descubre despues, **la salida vieja no
  se reescribe**. Va una nota fechada al lado con la orden que si funciona. Reescribirla convertiria
  «falta evidencia» en «hay evidencia falsa», esta vez sin nadie que lo note.
- **Donde queda aplicada:** `T-029`, en las notas fechadas de `D-036`, `D-038` y `D-040`; y en los
  bloques de `D-043`, `D-044`, `D-045` y `T-027` a `T-031`, todos anclados con `git show HEAD:` o
  `git grep <sha>` donde el arbol iba a cambiar.

---

### L-014 - Una carpeta agnostica nueva necesita cuatro enganches, y el cuarto es el que se olvida
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Etapa | 000_preproject |
| Origen | manager |

- **Contexto:** al nacer `_workflow/` hubo que engancharla en tres sitios: la fila de «Carpetas
  propias» de `project.md`, la lista de lo copiable tal cual de `CLAUDE.md`, y el ambito del Paso 1b
  de `protocol-close`. Los tres estaban identificados de antemano porque `_templates/` habia pasado
  por lo mismo dos sesiones antes —`T-026`, y antes `D-026` con `_phases/`—.
- **Que ocurrio:** los tres se hicieron, y aun asi la carpeta quedo **inalcanzable**. Nada en
  `_phases/` ni en ningun protocolo manda leerla, asi que en la practica nadie la abriria. Los tres
  enganches conocidos son de **control** —que la carpeta este declarada y que no filtre datos
  propios—; ninguno es de **uso**.
- **Leccion:** una carpeta agnostica nueva necesita **cuatro** enganches, no tres:

| # | Enganche | Responde a |
|---|---|---|
| 1 | fila en «Carpetas propias» de `project.md` | ¿esta declarada? |
| 2 | lista de lo copiable tal cual de `CLAUDE.md` | ¿se sabe que es agnostica? |
| 3 | ambito del Paso 1b de `protocol-close` | ¿se comprueba que lo sigue siendo? |
| 4 | **algo que mande leerla en el momento en que sirve** | ¿la va a abrir alguien? |

- **Por que el cuarto es distinto de los otros tres:** los tres primeros **tienen control que los
  detecta**. Una carpeta sin fila la señala el Paso 2c; una fuga la señala el Paso 1b. El cuarto **no
  tiene ningun control**: una carpeta que nadie abre no dispara nada, no rompe ningun barrido, y el
  repositorio queda perfectamente coherente con material muerto dentro. Es `L-008` en su forma mas
  cara — una regla escrita sin mecanismo que la aplique—, y aqui aplicada a un archivo entero.
- **Como aplicarla:** al crear una carpeta agnostica, la pregunta que cierra el trabajo no es «¿esta
  declarada y limpia?» sino **«¿quien la abre, cuando, y que se lo dice?»**. Si la respuesta es «se
  entiende que hay que leerla», no hay respuesta.
- **Donde queda aplicada:** se detecto en `S-009` y **se dejo abierta a proposito**, no resuelta: el
  enganche que falta toca un archivo de `_phases/`, y esa es una decision del usuario, no de
  `manager`. Queda señalada en el reporte de la sesion.

---

### L-015 - Una correccion escrita en una seccion que el cierre sobrescribe no es una correccion
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Etapa | 000_preproject |
| Origen | manager |

- **Contexto:** `F-021` señalaba un hash mal atribuido en la celda «Avance de la etapa» de
  `progress.md`. `T-028` lo corrigio ahi mismo, en su sitio, y dejo nota fechada al lado — el
  procedimiento correcto para cualquier otro archivo del registro.
- **Que ocurrio:** la correccion no llego al commit. Las secciones 1 y 2 de `progress.md` las
  **sobrescribe entera el cierre** en cada pasada: cuando `session-closer` escribio el estado de
  `S-009`, la celda corregida fue reemplazada por la nueva, y con ella desaparecieron el hash
  corregido y la nota. Tres registros distintos quedaron afirmando una nota fechada que nunca
  existio, y la auditoria siguiente lo levanto como `F-024`, con gravedad `Alta`.
- **Leccion:** antes de corregir un texto, hay que preguntar **quien escribe ese texto**. Un archivo
  del registro tiene dos clases de contenido, y solo una admite correccion en su sitio:

| Clase | Ejemplos | Corregir ahi… |
|---|---|---|
| **Durable** | una ficha `T-XXX`, una `D-XXX`, un `F-NNN`, una entrada de bitacora | **funciona**: nadie la reescribe |
| **Volatil** | las secciones de `progress.md` que el cierre sobrescribe en cada pasada | **no funciona**: la proxima pasada se la lleva |

- **Como aplicarla:** cuando un hallazgo señala un texto que vive en una seccion volatil, la
  correccion se escribe **donde el texto sobrevive** —la bitacora, la ficha, la entrada del
  hallazgo—, y en la seccion volatil se ajusta la redaccion sabiendo que es efimera. Si el texto no
  sobrevive en ningun sitio, entonces el hallazgo se resuelve **por desaparicion**, y eso es lo que
  hay que escribir; afirmar una correccion que el diff no muestra es peor que no corregir nada.
- **Por que no lo detecto ningun control:** el bloque de verificacion de `T-028` se corrio **sobre el
  arbol de trabajo**, antes del cierre, y en ese momento era cierto. Es `L-013` otra vez —un bloque
  sin ancla caduca—, pero con un agravante propio: aqui no caduco por el paso del tiempo sino por
  **el propio commit que lo publicaba**.
- **Donde queda aplicada:** `D-050` y `T-032`.

---

### L-016 - Una consulta que cambia lo que haces no deja rastro, y sin rastro no ocurrio
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Etapa | 000_preproject |
| Origen | usuario |

- **Contexto:** se consultaron los bloques D y E del archivo de lecciones globales (`D-054`), y la
  consulta funciono: dos lecciones señalaron que `A-003` era un supuesto que se **averigua** y que no
  dependia de `A-004`, y otras dos dictaron **con que** verificarlo —sin navegador, porque el
  instrumento tiene que poder ver el fallo que se descarta—.
- **Que ocurrio:** `manager` paso directamente a ejecutar esa verificacion, y el usuario pregunto
  *«¿pero que tiene que ver eso con las lecciones aprendidas?»*. La pregunta era correcta: en
  pantalla solo se veia a alguien corriendo `curl` contra una web. Las lecciones habian elegido la
  tarea y dictado el metodo, y nada de eso era visible.
- **Leccion:** este mecanismo tiene un modo de fallo que los demas no tienen: **cuando funciona, no
  se ve**. No produce un documento ni un artefacto — produce que hagas **otra cosa**, y una cosa
  distinta se parece mucho a una cosa cualquiera. Un archivo que solo se nota cuando falla es un
  archivo del que nadie podra decidir nunca si vale la pena.
- **Como aplicarla:** toda consulta deja su rastro **en el momento**, no al final: la decision o la
  tarea que cambio, en `decisions.md` o en `tasks.md`, **citando el codigo de la leccion**. Y al
  narrarla, decir cual eligio la tarea y cual dicto el metodo. Si de una consulta no sale ningun
  codigo citado en ningun sitio, la consulta no ocurrio para nadie que no estuviera delante — y eso
  incluye a quien vuelva dentro de tres meses.
- **Donde queda aplicada:** `CLAUDE.md`, seccion «Las lecciones globales», que hace obligatorio ese
  rastro y avisa de este modo de fallo; y la casilla de arranque de `_phases/000_preproject.md` §6,
  que exige la consulta **y su registro**, no solo la consulta.

---

### L-017 - Una condicion de salida no es una tarea pendiente, y confundirlas desactiva el disparador
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Etapa | 000_preproject |
| Origen | usuario |

- **Contexto:** se añadio a la condicion de salida de cada etapa la casilla de la cosecha (`D-056`),
  que dispara la promocion de lecciones al archivo global **al cerrar la etapa**.
- **Que ocurrio:** en el mismo reporte, `manager` escribio que `000_preproject` «ya no puede cerrar»
  y ofrecio «la primera cosecha» como una de las tres opciones de trabajo inmediato. El usuario lo
  corto: *«¿por que me estas pidiendo cosechar si aun no vamos a cerrar la fase?»*.
- **Leccion:** una condicion de salida y una tarea se parecen —las dos son trabajo escrito que hay
  que hacer— pero **responden a preguntas distintas**: la tarea pregunta *«¿que hago ahora?»* y la
  condicion pregunta *«¿puedo cerrar ya?»*. Pasar una condicion a la lista de trabajo la adelanta a
  un momento que no es el suyo, y **destruye justo lo que la hacia util**: si la cosecha se hace
  cuando apetece, la casilla deja de ser el disparador y vuelve a ser una nota — que es el problema
  que `D-056` acababa de resolver.
- **Por que el error es facil:** quien acaba de construir un mecanismo tiene ganas de verlo correr, y
  ejecutarlo se siente como terminar el trabajo. Pero un disparador se prueba **cuando se dispara**;
  correrlo a mano no demuestra que funcione, demuestra que se puede hacer sin el.
- **Como aplicarla:** al añadir una condicion de salida, **no se propone su cumplimiento como
  siguiente tarea**. Se dice en que momento se satisfara y se deja ahi. Y al enunciarla, evitar la
  forma «esto ya no puede cerrar»: una condicion de salida nunca bloquea el trabajo en curso, solo el
  cierre — decirlo al reves convierte una regla nueva en una alarma falsa.
- **Donde queda aplicada:** la cosecha se retiro de la lista de trabajo inmediato en la misma sesion,
  y `D-056` deja escrito que su momento es el cierre de etapa.


---

### L-018 - Un archivo traido de otro proyecto destapa contradicciones que alli no existian
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Etapa | 000_preproject |
| Origen | manager |

- **Contexto:** el usuario aporto un archivo de etapa de prototipo procedente de otro proyecto, para
  adaptarlo a esta metodologia (`T-043`).
- **Que ocurrio:** el trabajo previsto era de traduccion —rutas, codigos, nombres de actores—, y
  todo eso salio mecanico. Lo que no era mecanico aparecio al comparar el contenido con `CLAUDE.md`:
  la etapa produce codigo ejecutable y prohibe los tests, mientras `PI-5` exige un test en verde y
  declara que «no hay una tercera casilla». **En el proyecto de origen esa contradiccion no existia**,
  porque alli no regia `PI-5`.
- **Leccion:** adaptar un archivo ajeno no es traducirlo. Sus reglas venian equilibradas con **otro
  conjunto de reglas**, y al aterrizarlo se cruzan con las nuestras: lo que alla era coherente aqui
  puede chocar de frente con un principio vigente. **La parte cara de la adaptacion no son las
  rutas: son los choques que solo se ven leyendo el archivo destino al lado del importado.**
- **Por que se escapa con facilidad:** un archivo importado se lee como material terminado. Se
  revisa lo que se ve distinto —nombres, rutas, codigos— y se da por bueno lo que se ve familiar,
  que es justamente donde vive el choque: dos reglas correctas por separado.
- **Como aplicarla:** al importar un artefacto de otro proyecto, **la pasada obligatoria no es sobre
  el artefacto sino sobre las reglas propias que toca**. Se lista que principios del proyecto entran
  en juego y se comprueba uno por uno; y cuando aparezca un choque, **se declara con su `D-XXX`**
  —dentro del archivo adaptado— en vez de resolverlo en silencio hacia un lado. Una contradiccion
  escrita se puede discutir; una tacita solo se puede descubrir, y la descubre una auditoria.
- **Donde queda aplicada:** `D-059` declara la excepcion a `PI-5` dentro de
  `_phases/010_prototype.md`, con su alcance y su limite; `D-060` deja escrito que el archivo se
  adelanto sin declarar la etapa.

---

### L-019 - Un control documentado sobre una parte de su propia salida no es el control
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Etapa | 000_preproject |
| Origen | report_auditor |

- **Contexto:** `S-012` nacio el Paso 2d de `protocol-close` precisamente para atrapar el defecto
  mas repetido del repositorio —un bloque de verificacion que su commit no sostiene—, y lo corrio en
  su propio cierre.
- **Que ocurrio:** el paso se corrio de verdad, y aun asi el defecto volvio a pasar. Su primera
  orden devuelve varias decenas de lineas; la evidencia publicada pego **cinco**. La linea que
  fallaba estaba entre las que no se pegaron, y la auditoria siguiente la encontro (`F-032`,
  **octava** repeticion del mismo patron).
- **Leccion:** **correr un control y documentar una parte de su salida no es haberlo corrido.** Un
  control que se documenta con una muestra de si mismo produce exactamente el efecto contrario al
  que busca: deja el registro diciendo que se verifico, y ademas da confianza. Es la version de
  control de lo que `CLAUDE.md` dice de los tests —uno escrito para pasar es documentacion
  disfrazada de evidencia—.
- **Por que se escapa con facilidad:** la muestra se elige de buena fe, y se elige por lo que se ve
  representativo. Lo que falla nunca parece representativo: **si lo pareciera, ya se habria visto**.
  El sesgo no esta en la mala intencion, esta en que quien elige la muestra es el mismo que se
  examina.
- **Como aplicarla:** cuando un paso de un protocolo produzca una lista, **la evidencia es la lista
  entera con su recuento**, no una seleccion. Y si la lista es larga, esa es una razon para pegarla,
  no para recortarla. Cuando ademas el recuento no sea estable entre entornos —como aqui, donde la
  misma orden sobre el mismo commit devuelve `26` y `28` segun quien la corra—, la lista es lo unico
  comparable: **una lista se compara linea a linea; un numero solo se puede creer.**
- **Donde queda aplicada:** `D-063` y el parrafo nuevo del Paso 2d de `protocol-close` (`T-046`).

> 📌 **Reincidencia del 2026-09-03 (`F-039`, `T-059`).** El defecto volvio en la seccion 7 de
> `_audit/S-016.md`, pero **por otra puerta**: no se recorto la lista, se **deduplico**. La orden
> devuelve 21 lineas —seis ordenes citadas a la vez en `decisions.md` y en `tasks.md`— y el bloque
> publico las 15 distintas llamandolas «Quince lineas».
>
> ```
> $ git diff -U0 bd8a9ff^ bd8a9ff -- _persistence _audit ":(exclude)_audit/S-016.md" | grep -E '^\+\$ ' | grep -vE 'git (show|grep|log|diff) [0-9a-f]{7,40}' | wc -l
> 21
>
> $ git show bd8a9ff:_audit/S-016.md | awk '/^\$ git diff -U0 -- _persistence _audit \| grep -E/{f=1;next} f&&/^```$/{exit} f' | grep -c '^+\$ '
> 15
> ```
>
> 🔑 **Lo que amplia la leccion: deduplicar tambien es seleccionar**, y no se siente asi. Recortar se
> sabe recorte; quitar repeticiones se siente limpieza — y el resultado es el mismo bloque que dice
> ser una salida cruda sin serlo. La regla del Paso 2d pasa a nombrar las dos cifras por separado:
> el recuento publicado es el de **lineas**, y el de ordenes distintas va aparte y con ese nombre.
>
> ⚠️ **Y aparecio un segundo filo que la leccion no cubria:** la orden se publico en la forma en que
> se **corrio** —sobre el area de staging, antes de que el informe existiera— y no en la que
> **reproduce** contra el commit. Corregido en el mismo sitio (`T-059`).

> 🔁 **Reincidencia numero dos, del 2026-09-03 (`T-062`, hallazgo `F-041`).** Tercera vez que esta
> leccion se cumple, y la primera con una causa **mecanica** en vez de editorial. En `F-035` el
> control cubria parte de su salida por como se redacto; en `F-039`, por deduplicarla. Aqui el
> bloque publica su salida **entera y sin tocar** —no hay recorte, no hay deduplicacion— y aun asi
> no sostiene la frase, porque **el patron no podia ver lo que faltaba**: un `\b` delante de una
> alternancia de una letra es ciego a los prefijos de dos. Es lo que le da el filo nuevo: hasta hoy,
> «publica la salida entera» bastaba para cumplir esta leccion. Ya no. Lo que hay que contrastar es
> el **ambito del patron** contra el **alcance de la frase**, y eso no se ve mirando la salida.
> Registrado aparte como `L-025`, porque el mecanismo es reutilizable y esta leccion no lo cubre.

---

### L-020 - Una regla que dice QUE registrar pero no DONDE no se incumple: se evapora
| Campo | Valor |
|---|---|
| Fecha | 2026-09-03 |
| Etapa | 000_preproject |
| Origen | report_auditor |

- **Contexto:** `D-063` y `L-019` nacieron en `S-013` para cerrar el octavo caso del defecto mas
  repetido del repositorio: exigen que el Paso 2d publique **la lista completa** de su primera orden,
  con su recuento. El mismo cierre que las escribio corrio el paso.
- **Que ocurrio:** el paso se corrio y su salida se miro — y aun asi no quedo en ningun archivo. El
  informe afirmo haberla publicado y remitio a la verificacion de una tarea donde no habia ninguna
  lista (`F-034`, novena repeticion de la familia). La regla nueva se incumplio **en su primera
  aplicacion, y por quien la habia escrito el dia anterior**.
- **Leccion:** una regla de registro tiene **dos mitades**, y solo se cumple la que tiene sitio.
  `D-063` decia **que** publicar y no **donde**; una evidencia sin destino asignado no genera ningun
  momento en que se eche en falta — se produce, se mira, y desaparece con la sesion. No se incumple
  de forma visible: **se evapora**, que es peor, porque nada chilla.
- **Por que se escapa con facilidad:** al escribir la regla, el «donde» parece obvio —«pues donde
  toque»—. Al aplicarla, cada sitio candidato tiene un argumento razonable en contra, y el que gana
  es la pantalla. Es el mismo hueco que describe `L-008` —una regla sin mecanismo es una intencion—,
  pero un escalon mas adentro: aqui **habia** mecanismo, y lo que faltaba era destino.
- **Como aplicarla:** toda regla que obligue a registrar algo nombra **el archivo y la seccion**
  donde aterriza, en la misma pasada en que se escribe. Si al escribirla no se sabe donde va, esa es
  la senal de que falta la mitad, no de que se decidira sobre la marcha. Y el destino se declara
  aunque el resultado sea vacio: «ninguna linea» tambien es un resultado, y una seccion vacia se ve;
  una seccion que no existe, no.
- **Donde queda aplicada:** `D-065` — la seccion 7 del informe de sesion, creada como destino fijo de
  la evidencia del Paso 2d, y el parrafo del propio paso que la nombra (`T-050`).

---

### L-021 - Un barrido con `git grep` sobre archivos sin versionar devuelve cero por no verlos
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Etapa | 000_preproject |
| Origen | manager |

- **Contexto:** la sesion creo tres archivos nuevos en carpetas agnosticas —`.claude/agents/`,
  `.claude/skills/` y `_templates/`—, que son exactamente el ambito donde el control de fuga del
  Paso 1b exige **cero lineas**. Antes de registrar la decision se corrio ese control con el patron
  documentado, para poder afirmar que lo nuevo no filtraba datos propios del proyecto.
- **Que ocurrio:** el control se corrio con `git grep`, tal como esta escrito en `protocol-close`, y
  devolvio `exit=1` — cero coincidencias. **Pero los tres archivos todavia no estaban versionados**, y
  `git grep` solo recorre el indice: el cero no decia «no hay fuga», decia «no he mirado ahi». El
  barrido se repitio con `grep -r`, que si los alcanza, y esta vez el cero fue real.
- **Leccion:** un barrido tiene **dos partes que se confunden con facilidad**: el patron y el ambito
  efectivo. El patron era correcto; el ambito real era mas pequeño que el declarado, y **la salida es
  identica en los dos casos**. Un cero no distingue entre «no hay» y «no se ha mirado» — y lo hace en
  silencio, que es lo que lo vuelve peligroso.
- **Por que se escapa con facilidad:** el control esta escrito con `git grep` y ahi es correcto, porque
  el cierre lo corre **despues** del `git add`, cuando todo esta en el indice. El fallo aparece al
  reutilizar el mismo comando **fuera de ese momento**, para comprobar trabajo recien escrito. La
  orden es la misma, la salida es la misma, y solo cambia algo que no se ve.
- **Es la familia de `L-013`, un escalon mas adentro.** Alli el problema era que un codigo de salida
  no prueba una ausencia; aqui el codigo de salida es correcto y lo que engaña es **el conjunto sobre
  el que se calculo**. Un ambito no declarado se lee como el ambito que uno esperaba.
- **Como aplicarla:** un barrido que se corra **antes** del `git add` usa `grep -r`, no `git grep`; y
  si se usa `git grep` fuera del cierre, se corre primero `git status --porcelain` para saber que
  queda fuera. En cualquier caso, **el bloque de verificacion dice con cual de los dos se obtuvo el
  cero**: sin eso, quien lo lea despues no puede distinguir un cero real de uno vacio.
- **Donde queda aplicada:** el bloque de verificacion de `D-067`, que publica el barrido con `grep -r`
  y añade la nota que explica por que no se uso `git grep` y que el `git grep` previo no valia.

---

### L-022 - Una garantia se comprueba contra el mecanismo, no contra lo que el mecanismo sugiere
| Campo | Valor |
|---|---|
| Fecha | 2026-09-03 |
| Etapa | 000_preproject |
| Origen | report_auditor |

- **Contexto:** la Comprobacion 0 del Gate 1 se monto para detectar evidencia escrita a posteriori, y
  se apoyo entera en una frase: «las fechas del historial no se pueden convencer». Sobre esa frase se
  construyo un resultado nuevo del Gate, se escribio en tres archivos y se repitio en la bitacora.
- **Que ocurrio:** la comprobacion comparaba `%ad`, la fecha de autor, que se sobrescribe con una
  variable de entorno. Una auditoria lo demostro en un repositorio desechable con dos commits: una
  hipotesis escrita **despues** de la sesion y fechada **antes** pasaba la comprobacion. El dato que
  si resistia —el orden del grafo— salia en la misma pantalla, y el protocolo no mandaba mirarlo.
- **Leccion:** cuando un control se apoya en una propiedad —«esto no se puede falsificar», «esto es
  unico», «esto no cambia»—, la propiedad hay que **comprobarla contra el mecanismo**, no contra lo
  que el mecanismo evoca. Una fecha **parece** un hecho del pasado; es un campo editable. La
  diferencia entre las dos lecturas no aparece nunca al leer el codigo: aparece al intentar romperlo.
- **Por que se escapa con facilidad:** la frase absoluta es lo que hace convincente al control, y por
  eso se escribe pronto y se copia a los demas archivos antes de que nadie la ponga a prueba. Cuanto
  mas rotunda, menos se comprueba — y cuando falla, ya esta en tres sitios.
- **Como aplicarla:** ningun control se cierra con una propiedad afirmada. Se escribe **el intento de
  romperlo** —la orden concreta que lo burlaria— y se pega su salida. Si el intento tiene exito, el
  control no vale; si falla, la frase ya no es una creencia. Y la frase que quede escrita dice
  **hasta donde llega** la garantia, no que sea absoluta.
- **Donde queda aplicada:** `D-071`, que sustituye la comparacion de fechas por orden del grafo y
  escribe el limite honesto de lo que ese orden demuestra, en el protocolo, en la plantilla del
  dictamen y como nota fechada en `D-069`.

---

### L-023 - Un dato derivable escrito a mano se equivoca justo donde nadie lo vuelve a mirar
| Campo | Valor |
|---|---|
| Fecha | 2026-09-03 |
| Etapa | 000_preproject |
| Origen | report_auditor |

- **Contexto:** un paso del cierre exige publicar la lista completa de ordenes sin ancla que la
  sesion escribio. La lista se publico entera y sus recuentos reproducian; al lado de cada linea se
  anoto **de que archivo salia**, y esa anotacion se escribio a mano mirando los bloques.
- **Que ocurrio:** tres de las once atribuciones eran falsas. Las ordenes existian, los numeros
  cuadraban, y el puntero llevaba a un sitio donde la orden no estaba — el mismo defecto que el paso
  se habia creado para cerrar, una vuelta antes.
- **Leccion:** cuando un dato **se puede derivar** de una fuente que ya se tiene delante, escribirlo
  a mano no es un atajo: es introducir una copia que nadie va a contrastar. El recuento se comprueba
  solo —se reejecuta la orden y el numero cuadra o no—; la **atribucion** no se comprueba sola, y por
  eso es exactamente donde se cuela el error.
- **Por que se escapa con facilidad:** anotar la procedencia se siente como transcribir, no como
  afirmar. Se busca la orden en el bloque que uno recuerda haber escrito, y la memoria atribuye antes
  de comprobar. Ademas la anotacion es correcta en la mayoria de las lineas, y una lista casi entera
  correcta no despierta a nadie.
- **Como aplicarla:** si el dato se puede derivar, **se deriva y se pega la orden que lo produjo**. Y
  si una parte no es derivable —el archivo si lo sabe el diff, la entrada concreta dentro del archivo
  no—, se dice cual es esa parte y se comprueba una por una contra lo que se cita, en vez de mezclar
  las dos mitades en una anotacion que parece toda del mismo tipo.
- **Donde queda aplicada:** `T-053`, que deja la procedencia real derivada del diff como nota fechada
  al lado del bloque original, y hace que el paso del cierre pida derivarla asi en adelante.

---

### L-024 - Una orden publicada se reejecuta antes de publicarla: copiarla la puede corromper en silencio
| Campo | Valor |
|---|---|
| Fecha | 2026-09-03 |
| Etapa | 000_preproject |
| Origen | manager |

- **Contexto:** al escribir el bloque de verificacion de `D-073` y `D-074` se publicaron ordenes con
  `\\b` (limite de palabra de una expresion regular). El texto se escribio a traves de una capa que
  interpreta escapes, y `\\b` llego al archivo como el **caracter de retroceso** `0x08`, invisible al
  leer.
- **Que ocurrio:** el bloque publicado se ve correcto en pantalla y **no se puede reejecutar**: quien
  copie esa linea le pasa al interprete un caracter de control en vez de un limite de palabra, y
  obtiene otro resultado. El barrido que lo destapo encontro **seis lineas** afectadas en el registro
  —una de esta sesion, ya reparada, y **cinco anteriores**, que no se tocan—. Son veinte apariciones
  del caracter repartidas en esas seis lineas; el recuento por lineas y el recuento por apariciones
  se dicen aqui con su nombre y no se mezclan (`T-064`, hallazgo `F-043`).

```
$ python -c "import io,re; pat=re.compile(u'[\x00-\x08\x0b\x0c\x0e-\x1f]'); [print(f,i,repr(m.group())) for f in ['_persistence/decisions.md','_persistence/tasks.md'] for i,l in enumerate(io.open(f,encoding='utf-8'),1) for m in pat.finditer(l)]"
_persistence/decisions.md 917 '\\x08'
_persistence/decisions.md 917 '\\x08'
_persistence/decisions.md 1304 '\\x08'
_persistence/decisions.md 1304 '\\x08'
_persistence/tasks.md 1212 '\\x08'
_persistence/tasks.md 1212 '\\x08'
_persistence/tasks.md 1931 '\\x08'   (x10)
_persistence/tasks.md 1987 '\\x08'
_persistence/tasks.md 1987 '\\x08'
```

📌 **La salida de arriba esta abreviada en la linea 1931**, que devuelve diez apariciones y se anota
como `(x10)`; el total del barrido fue **veinte apariciones en seis lineas**. Se dice aqui para que
el recuento no se lea como una lista completa — que es justo el defecto de `L-019`.

📌 **Y la orden se reejecuta ya reparada la linea de esta sesion**, por eso no aparece
`_persistence/decisions.md:3869`: devuelve **dieciocho apariciones en cinco lineas**, las cinco
anteriores. Antes de reparar la de hoy eran veinte en seis.

- **Leccion:** **un bloque de verificacion se prueba como texto, no solo como resultado.** Todo el
  cuidado del registro esta puesto en que el resultado sea cierto; nadie comprueba que la **orden**
  sobreviviera al viaje hasta el archivo. Y una orden corrompida es peor que un resultado erroneo:
  el resultado erroneo se detecta al reejecutar, la orden corrompida hace que la reejecucion falle
  o devuelva otra cosa, y entonces lo que se pone en duda es el repositorio.
- **Por que se escapa con facilidad:** el caracter es **invisible**. El bloque se relee, se ve bien,
  y se da por bueno. Solo aparece con un barrido que busque caracteres de control, y nadie lo corre
  porque nadie sospecha que exista el problema.
- **Como aplicarla:** cuando una orden publicada lleve `\\b`, `\\d`, `\\t`, `\\n` o cualquier escape de
  expresion regular, **se copia del archivo y se reejecuta desde ahi** antes de dar el bloque por
  bueno. Si la reejecucion no reproduce, la orden se corrompio al escribirla.
- **Lo que queda pendiente, y por que no se hizo hoy:** las **cinco lineas anteriores** no se
  reescriben. Reescribir un bloque antiguo para que exhiba una orden que en su dia no se ejecuto asi
  convierte «falta evidencia» en «hay evidencia falsa», y esta vez sin nadie que lo note. Se dejan
  como estan y se anotan con una nota fechada que diga que la orden publicada lleva un caracter
  corrompido y cual es su forma reejecutable.

  > 📌 **Nota del 2026-09-03 (`T-063`, hallazgo `F-042`).** La frase original decia que esto **«lo
  > decide una auditoria», no `manager`**, y eso estaba mal repartido: `project.md` dice que
  > `report_auditor` «no construye, no corrige y no decide». Un pendiente delegado en quien por
  > definicion no puede decidirlo no espera a nadie. La decision es de `manager` —evaluar— y del
  > usuario —confirmar la deuda—; queda registrada en **`DT-003`**, y asi la ve el arranque de
  > sesion, que lee tareas y deuda y no el cuerpo de las lecciones.
- **Donde queda aplicada:** los bloques de `D-073` y `D-074` de esta sesion, reparados y reejecutados.

---

### L-025 - Un patron con limite de palabra es ciego a los prefijos mas largos que empiezan igual
| Campo | Valor |
|---|---|
| Fecha | 2026-09-03 |
| Etapa | 000_preproject |
| Origen | report_auditor |

- **Contexto:** el control que comprueba que una plantilla no lleva codigos instanciados del registro
  se corre con `\b(N|T|D|A|C|I|F|L|S|R|DT)-[0-9]{3}\b`, y su salida se publica como bloque de
  verificacion. Sobre las nueve plantillas de la etapa de la baseline devolvio dos lineas, y con esas
  dos se escribio la frase «sin codigos instanciados mas alla del primero».
- **Que ocurrio:** el patron **no puede** encontrar `FT-001` ni `SC-001`. El limite de palabra
  inicial exige que delante de la `F` no haya un caracter de palabra, y en `FT-` lo hay: la propia
  `F` de la alternativa casa, pero entonces queda `T-001` precedido de `F`, y ahi el `\b` falla. El
  resultado es un cero limpio que parece un barrido en verde. Con el patron ampliado a dos letras
  aparecen cinco codigos, y tres de ellos no son «el primero».

```
$ grep -rnoE "\b(N|T|D|A|C|I|F|L|S|R|DT)-[0-9]{3}\b" _templates/020_baseline/
_templates/020_baseline/015_features.md:189:N-001
_templates/020_baseline/045_traceability.md:199:N-001

$ grep -rnoE "\b(FT|SC|VS|TC|ADR)-[0-9]{3}\b" _templates/020_baseline/ | grep -vE "(FT|SC)-00[12]"
_templates/020_baseline/015_features.md:72:FT-003
_templates/020_baseline/020_scenarios.md:72:SC-003
_templates/020_baseline/025_specification.md:236:SC-003
_templates/020_baseline/045_traceability.md:200:SC-007
_templates/020_baseline/045_traceability.md:200:FT-004
```

- **Leccion:** **cuando una alternativa del patron es prefijo de otra que existe, el barrido tiene un
  punto ciego exactamente ahi.** Y el punto ciego no se manifiesta como error: se manifiesta como un
  resultado corto, que es la forma en que un control miente sin que nadie lo note. Vale para
  cualquier familia de identificadores donde convivan prefijos de una y de dos letras — que en este
  metodo es la norma y no la excepcion, porque los codigos de producto se alargaron a proposito para
  no chocar con los del registro.
- **Por que se escapa con facilidad:** el patron se escribio cuando **solo existian** prefijos de una
  letra, y era correcto entonces. No se rompio al cambiar el patron: se rompio al aparecer un codigo
  nuevo que el patron no contemplaba, y un patron no avisa de lo que no busca. Ademas el cero salio
  acompañado de dos aciertos —`N-001` dos veces—, que es lo que le dio credibilidad.
- **Como aplicarla:** **antes de publicar un barrido de identificadores, se enumera contra que tabla
  de codigos se esta barriendo y se comprueba que el patron cubre todas sus filas.** Si algun prefijo
  es prefijo de otro, se ordenan de mas largo a mas corto en la alternancia, o se sustituye el `\b`
  inicial por un delimitador explicito. Y la frase que acompaña al bloque dice **que familia** se
  barrio, no «no hay codigos instanciados».
- **Donde queda aplicada:** las notas fechadas de `D-073` y `T-057` (`T-062`), que publican el patron
  ampliado y su salida real sin reescribir los bloques originales.

---

### L-026 - Un enganche de uso escrito en generico no engancha: tiene que nombrar el archivo
| Campo | Valor |
|---|---|
| Fecha | 2026-09-03 |
| Etapa | 000_preproject |
| Origen | manager |

- **Contexto:** cada archivo de reparto de `_workflow/` cierra con un bloque de verificacion de dos
  ordenes. La segunda —`grep -n "_workflow/<etapa>" _phases/<etapa>.md`— **no comprueba el archivo:
  comprueba que la etapa manda leerlo**. Es el «cuarto enganche» de `L-014`, el de uso, y es la razon
  entera de que ese bloque tenga dos ordenes y no una.
- **Que ocurrio:** al escribir el reparto de la baseline, esa orden devolvia vacio. El archivo de
  etapa **si** invocaba el reparto, dos veces, pero escrito en generico: «el archivo de esta etapa en
  `_workflow/`» y «el reparto de `_workflow/`». Los dos archivos de etapa anteriores lo nombran
  entero. La invocacion existia y era legible para una persona; para el control, no existia.

```
$ git show 6b42d0f:_phases/020_baseline.md | grep -c "_workflow/020_baseline"
0

$ git show 6b42d0f:_phases/005_discovery.md | grep -c "_workflow/005_discovery"
1

$ git show 6b42d0f:_phases/010_prototype.md | grep -c "_workflow/010_prototype"
2
```

- **Leccion:** **una referencia en prosa generica cumple para el lector humano y desaparece para el
  control.** Y aqui el coste es doble, porque en esta etapa el reparto no es material de consulta
  sino **condicion de entrada**: si la cita no se puede encontrar, lo que se pierde no es una
  recomendacion de lectura, es la condicion que impide abrir la etapa sin saber quien hace cada paso
  — y se pierde en silencio, porque el archivo sigue existiendo y el control sigue devolviendo cero
  sin que nadie sepa si es que falta la cita o que falta el archivo.
- **Por que se escapa con facilidad:** escribir «el archivo de esta etapa en `_workflow/`» se siente
  **mas limpio**, y hasta mas correcto: evita repetir un nombre que se deduce del contexto. Es la
  forma en que un texto bien redactado desactiva un control automatico, y no hay ninguna señal
  mientras el archivo referido no existe todavia — que es justo cuando se escribe el archivo de
  etapa.
- **Como aplicarla:** **toda referencia de la que dependa un control se escribe con el nombre
  completo del archivo, aunque el contexto lo haga obvio.** Y al escribir un archivo cuyo bloque de
  verificacion incluya un enganche de uso, ese enganche se corre **antes** de dar el archivo por
  terminado: si devuelve vacio, lo que falta no es el archivo nuevo, es la cita en el que lo invoca.
- **Donde queda aplicada:** `_phases/020_baseline.md` §4 y §5 nombran ahora
  `_workflow/020_baseline.md` entero (`T-057`), y el enganche devuelve dos lineas.

---

### L-027 - Cuando existe la orden que produce una lista, escribirla a mano es el error, no el atajo
| Campo | Valor |
|---|---|
| Fecha | 2026-09-03 |
| Etapa | 000_preproject |
| Origen | report_auditor |

- **Contexto:** `R-018` abre tres hallazgos sobre el mismo commit —`F-045`, `F-046` y `F-047`— y los
  tres tienen la misma forma. En los tres, **la orden que daba la respuesta correcta ya estaba
  escrita en el protocolo o era trivial de escribir**, y en los tres se resolvio a ojo:

  | Hallazgo | Lo que se hizo a mano | La orden que existia |
  |---|---|---|
  | `F-045` | numerar las 26 lineas de la seccion 7 y marcar cuales se repetian | `cat -n` y `sort \| uniq -d` |
  | `F-046` | decir en que entrada de `lessons.md` cayo la nota nueva | `git diff -U0 <c>^ <c> -- <archivo>` mapeado a los `### ` |
  | `F-047` | escribir la alternancia de prefijos del barrido | derivarla de la tabla «Codigos» de `project.md` |

- **Que ocurrio:** ninguno de los tres fallos se manifesto como error. El primero se manifesto como
  una numeracion corrida **una posicion**, que dejo una orden sin salida publicada mientras el
  informe declaraba que todas reprodujeron. El segundo, como un codigo vecino —`L-020` por `L-019`—,
  que es peor que la omision: quien va a comprobarlo abre la entrada equivocada, no encuentra nada, y
  concluye que el informe exagera. El tercero, como un cero limpio.
- **Leccion:** **una lista derivable escrita a mano no se equivoca por descuido: se equivoca por el
  sitio exacto donde la mano y la orden difieren, que es siempre un desplazamiento pequeno y
  plausible.** Un numero corrido, un codigo vecino, un prefijo que falta. Ninguno de los tres se ve
  releyendo, porque los tres son **exactamente lo que uno esperaba leer**. Por eso la regla no puede
  ser «revisar mejor»: reviso quien lo escribio, y lo dio por bueno tres veces en el mismo commit.
- **Por que se escapa con facilidad:** escribir la lista a mano se siente **mas rapido y mas
  legible**, y casi siempre lo es. La orden equivalente es fea, larga y hay que pensarla; la lista
  escrita sale sola y encima queda bien formateada. El coste no aparece al escribirla — aparece
  cuando alguien la contrasta, que puede ser nunca. Y hay un agravante propio de este repositorio:
  `S-018` es el commit que **endurecio la regla de derivar del diff** (`T-065`, `F-044`) y en el
  mismo commit la incumplio (`F-046`). Escribir la regla no la aplica.
- **Como aplicarla:** **antes de teclear una enumeracion dentro de un bloque de evidencia, se
  pregunta si hay una orden que la produzca. Si la hay, se corre y se pega su salida — y la orden va
  pegada con ella.** Si no la hay, se dice que se escribio a mano y contra que se contrasto. Y donde
  la mano es inevitable —rotular cada salida con su posicion—, los rotulos salen de `cat -n`, no de
  contar.
- **Donde queda aplicada:** el Paso 2d de `protocol-close` incorpora la numeracion con `cat -n` y las
  repetidas con `uniq -d` (`T-066`); el Paso 6b incorpora las dos ordenes que derivan las entradas
  editadas de cada archivo de registro (`T-067`); y `D-077` sustituye la alternancia escrita a mano
  del control de codigos instanciados por una derivada de las tablas (`T-068`).

```
$ grep -c 'cat -n' .claude/skills/protocol-close/SKILL.md
2

$ grep -c 'que entrada contiene cada punto tocado' .claude/skills/protocol-close/SKILL.md
1

$ grep -c 'D-077' _persistence/decisions.md
3
```
