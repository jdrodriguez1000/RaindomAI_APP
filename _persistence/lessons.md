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
| [L-028](#l-028---un-recuento-sobre-los-archivos-que-toque-no-es-un-barrido-el-diff-sabe-cuales-son-la-memoria-no) | Un recuento sobre «los archivos que toque» no es un barrido: el diff sabe cuales son, la memoria no | 2026-09-04 | 000_preproject | Sin evaluar |
| [L-029](#l-029---la-herramienta-con-la-que-se-documenta-un-defecto-de-escape-lo-reproduce-y-el-barrido-del-cierre-llega-tarde) | La herramienta con la que se documenta un defecto de escape lo reproduce, y el barrido del cierre llega tarde | 2026-09-05 | 000_preproject | Sin evaluar |
| [L-030](#l-030---una-nota-que-explica-de-donde-sale-un-cambio-filtra-codigos-y-la-buena-intencion-es-lo-que-la-hace-invisible) | Una nota que explica de donde sale un cambio filtra codigos, y la buena intencion es lo que la hace invisible | 2026-09-06 | 000_preproject | Sin evaluar |
| [L-031](#l-031---un-guion-que-abre-el-archivo-para-escribir-antes-de-tener-el-contenido-lo-destruye-si-falla) | Un guion que abre el archivo para escribir antes de tener el contenido lo destruye si falla | 2026-09-06 | 000_preproject | Sin evaluar |
| [L-032](#l-032---el-repositorio-mezcla-finales-de-linea-y-una-sustitucion-literal-falla-sin-decir-por-que) | El repositorio mezcla finales de linea, y una sustitucion literal falla sin decir por que | 2026-09-06 | 000_preproject | Sin evaluar |
| [L-033](#l-033---una-autorizacion-para-sustituir-texto-necesita-un-borde-que-se-vea-no-una-prohibicion-al-lado) | Una autorizacion para sustituir texto necesita un borde que se vea, no una prohibicion al lado | 2026-09-07 | 000_preproject | Sin evaluar |
| [L-034](#l-034---un-pre-compromiso-que-no-distingue-el-fallo-total-del-parcial-se-renegocia-en-su-primera-aplicacion) | Un pre-compromiso que no distingue el fallo total del parcial se renegocia en su primera aplicacion | 2026-09-07 | 000_preproject | Sin evaluar |
| [L-035](#l-035---una-regla-que-nombra-un-archivo-se-cumple-en-ese-archivo-y-se-incumple-en-el-de-al-lado) | Una regla que nombra un archivo se cumple en ese archivo y se incumple en el de al lado | 2026-09-07 | 000_preproject | Sin evaluar |
| [L-036](#l-036---una-condicion-de-parada-que-no-se-puede-cumplir-se-convierte-en-una-excepcion-redactada-cada-vez) | Una condicion de parada que no se puede cumplir se convierte en una excepcion redactada cada vez | 2026-09-07 | 000_preproject | Sin evaluar |
| [L-037](#l-037---un-criterio-que-cita-el-texto-que-comprueba-se-acierta-a-si-mismo) | Un criterio que cita el texto que comprueba se acierta a si mismo | 2026-09-07 | 000_preproject | Sin evaluar |
| [L-038](#l-038---un-patron-con-b-escrito-por-un-script-llega-al-archivo-como-caracter-de-control) | Un patron con `\b` escrito por un script llega al archivo como caracter de control | 2026-09-08 | 000_preproject | Sin evaluar |
| [L-039](#l-039---un-archivo-escrito-al-principio-de-su-etapa-describe-un-andamiaje-que-la-etapa-aun-no-habia-construido) | Un archivo escrito al principio de su etapa describe un andamiaje que la etapa aun no habia construido | 2026-09-08 | 000_preproject | Sin evaluar |
| [L-040](#l-040---una-prohibicion-que-ya-reincidio-no-se-arregla-escribiendola-mejor) | Una prohibicion que ya reincidio no se arregla escribiendola mejor | 2026-09-08 | 000_preproject | Sin evaluar |
| [L-041](#l-041---un-criterio-sin-artefacto-donde-firmarse-no-falla-hasta-que-alguien-intenta-usarlo) | Un criterio sin artefacto donde firmarse no falla hasta que alguien intenta usarlo | 2026-09-08 | 000_preproject | Sin evaluar |
| [L-042](#l-042---el-dato-que-siempre-sale-falso-suele-ser-el-que-nadie-usa-y-entonces-la-correccion-es-quitarlo) | El dato que siempre sale falso suele ser el que nadie usa, y entonces la correccion es quitarlo | 2026-09-08 | 000_preproject | Sin evaluar |
| [L-043](#l-043---una-condicion-escrita-en-prosa-se-recorre-mecanicamente-pero-no-se-verifica-entera-y-eso-pide-un-tercer-valor) | Una condicion escrita en prosa se recorre mecanicamente, pero no se verifica entera — y eso pide un tercer valor | 2026-09-08 | 000_preproject | Sin evaluar |
| [L-044](#l-044---lo-que-crees-saber-de-tu-propio-repositorio-se-comprueba-con-una-orden-sobre-todo-cuando-parece-obvio) | Lo que crees saber de tu propio repositorio se comprueba con una orden, sobre todo cuando parece obvio | 2026-09-08 | 000_preproject | Sin evaluar |
| [L-045](#l-045---un-contraste-solo-prueba-lo-que-su-ambito-alcanza-y-el-ambito-no-se-comprueba-a-si-mismo) | Un contraste solo prueba lo que su ambito alcanza, y el ambito no se comprueba a si mismo | 2026-09-10 | 000_preproject | Sin evaluar |
| [L-046](#l-046---un-cambio-en-el-registro-y-el-mismo-cambio-en-su-plantilla-son-dos-cambios-y-se-cuentan) | Un cambio en el registro y el mismo cambio en su plantilla son dos cambios, y se cuentan | 2026-09-10 | 000_preproject | Sin evaluar |
| [L-047](#l-047---una-regla-que-nombra-el-sitio-solo-protege-ese-sitio) | Una regla que nombra el sitio solo protege ese sitio | 2026-09-10 | 000_preproject | Sin evaluar |
| [L-048](#l-048---un-criterio-que-busca-una-frase-no-distingue-el-texto-corregido-de-su-cita) | Un criterio que busca una frase no distingue el texto corregido de su cita | 2026-09-10 | 000_preproject | Sin evaluar |
| [L-049](#l-049---medir-un-control-y-descartarlo-prueba-que-ese-ambito-no-sirve-no-que-no-exista-uno-que-si) | Medir un control y descartarlo prueba que ESE ambito no sirve, no que no exista uno que si | 2026-09-10 | 000_preproject | Sin evaluar |
| [L-050](#l-050---un-control-que-enumera-casos-caduca-solo-uno-que-reconoce-la-forma-no) | Un control que enumera casos caduca solo; uno que reconoce la forma, no | 2026-09-10 | 000_preproject | Sin evaluar |
| [L-051](#l-051---una-tarea-escrita-para-mas-adelante-describe-el-repositorio-del-dia-que-se-escribio) | Una tarea escrita para «mas adelante» describe el repositorio del dia que se escribio | 2026-09-10 | 000_preproject | Sin evaluar |

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

> 🕒 **Nota de reincidencia del 2026-09-10.** Volvio a pasar, y en la forma mas pura posible: un
> criterio de cierre buscaba una frase de prosa en el archivo de decisiones, y **la propia orden
> contenia esa frase**, asi que se contaba a si misma y devolvia `2` donde el criterio decia `1`.
> Se detecto por correrla antes de publicarla, no por releerla.
>
> 🔑 **Lo que anade sobre el enunciado original:** ahi el ambito era un archivo entero; aqui es **la
> linea misma**. Un patron que cita texto literal de prosa acaba dentro del archivo que barre en
> cuanto el bloque se escribe en ese mismo archivo — y los registros de este repositorio son justo
> eso. La defensa que funciono fue **anclar el patron a la forma de la linea de prosa** (`^- ` mas su
> marca), que la orden no reproduce.
>
> ⚠️ **Y confirma la unica defensa real, que no es escribir mejor el patron:** correr el criterio
> **antes** de darlo por bueno. Escrito y no corrido, este habria entrado al commit afirmando `1` con
> la orden devolviendo `2`, y lo habria cazado la auditoria una pasada despues.
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

### L-028 - Un recuento sobre «los archivos que toque» no es un barrido: el diff sabe cuales son, la memoria no
| Campo | Valor |
|---|---|
| Fecha | 2026-09-04 |
| Etapa | 000_preproject |
| Origen | report_auditor |

- **Contexto:** `F-049` señala que `DT-004` declara siete lineas nuevas con el caracter `0x08` en dos
  archivos, cuando en el commit hay diez en cuatro. La entrada no se invento la cifra: la conto bien
  **sobre los dos archivos que tenia delante**, que eran los que el Paso 6 del cierre estaba
  revisando en ese momento. Los otros dos se habian editado antes, en la misma sesion.
- **Que ocurrio:** el defecto no se manifesto como una cifra absurda. Se manifesto como una cifra
  **plausible y corta**, con su ambito escrito al lado —«cinco en un archivo y dos en otro»— y una
  seccion del informe declarando explicitamente que el barrido no habia sido completo y enumerando
  los archivos no cubiertos. **Esa enumeracion tambien se escribio a mano, y tambien omitio los dos
  que importaban.** Es decir: la salvedad que existia para acotar el alcance repitio el mismo error
  que acotaba.
- **Y las tres lineas que faltaban eran las peores del lote.** Dos caian dentro de la nota fechada
  que corregia `F-045`, y no en prosa: en la transcripcion de la **salida cruda** de dos ordenes. La
  nota que existia para dejar de publicar cifras falsas publicaba una salida que la orden no
  devuelve.
- **Leccion:** **cuando el alcance de un recuento es «los archivos que se tocaron», ese alcance se
  deriva del diff — nunca de recordar cuales fueron.** No es una variante de `L-027`: `L-027` dice
  que la **lista** se saca de una orden; esto dice que **el conjunto sobre el que la orden corre** se
  saca de otra. Una orden impecable sobre un conjunto elegido a mano devuelve un resultado impecable
  y falso, y encima parece mas riguroso que no haberlo corrido.
- **Por que se escapa con facilidad:** los archivos que uno recuerda haber tocado son los del final
  de la sesion. Los del principio ya se cerraron mentalmente hace horas — y son justo los que llevan
  mas rato acumulando defectos sin que nadie los vuelva a mirar. Ademas, declarar la salvedad
  («no se barrio todo, faltan estos») **produce sensacion de rigor** y desactiva la pregunta: quien
  lee ve un limite declarado y da por hecho que quien lo declaro sabia cual era.
- **Como aplicarla:** **antes de publicar un recuento cuyo alcance sean unos archivos, la lista de
  archivos sale de `git diff --cached --name-only` (o de `git ls-tree` si el alcance es el arbol
  entero), y el recuento se calcula recorriendola.** Si el alcance de verdad es parcial, el recorte
  tambien se deriva: se dice con que orden se filtro, no que archivos se recuerdan.
- **Que cambio por esta leccion:** nace el **Paso 2e** de `protocol-close` (`T-074`), que barre los
  caracteres de control sobre los archivos que el commit toca —derivados del diff— y publica su
  resultado en la seccion 8 del informe, tambien cuando sale vacio. El `0x08` llevaba tres sesiones
  apareciendo y las tres se detecto a mano y por casualidad; es `L-008` otra vez, una regla sin
  mecanismo.

```
$ grep -c '^## Paso 2e' .claude/skills/protocol-close/SKILL.md
1

$ grep -c '^## 8. Evidencia del Paso 2e' .claude/skills/protocol-close/SKILL.md
1

$ for f in $(git ls-tree -r --name-only 1b30e16 | grep -E '\.md$'); do n=$(git show 1b30e16:"$f" | grep -c $'\x08'); if [ "$n" -gt 0 ]; then echo "$f: $n"; fi; done
_audit/S-018.md: 2
_audit/S-019.md: 1
_audit/findings.md: 1
_persistence/decisions.md: 7
_persistence/tasks.md: 5
```

---

### L-029 - La herramienta con la que se documenta un defecto de escape lo reproduce, y el barrido del cierre llega tarde
| Campo | Valor |
|---|---|
| Fecha | 2026-09-05 |
| Etapa | 000_preproject |
| Origen | manager |

- **Contexto:** al escribir la nota fechada que corrige `F-051` —cuyo asunto es, literalmente, el
  recuento de lineas con caracteres de control— el script que la inserto **introdujo un caracter de
  control nuevo** en `_audit/S-020.md`. El barrido de control subio de 14 a 15 sobre los mismos
  archivos.
- **Que ocurrio, en concreto:** la nota pega una orden de shell que contiene la clase
  `[\x01-\x08...]`. Esa cadena viajo dentro de una cadena de Python que **no era cruda**, asi que
  `\x01` dejo de ser texto y paso a ser el byte. El archivo resultante se ve identico en pantalla:

```
$ grep -n $'[\x01-\x08\x0b\x0c\x0e-\x1f]' _audit/S-020.md | cat -A | cut -c1-120
351:> $ git diff --name-only --diff-filter=d f09d1f7^ f09d1f7 | while read f; do n=$(git show f09d1f7:"$f" | grep -c $'[^A-^H^K^L^N-^_]'
```

- **Leccion:** **una orden que contiene secuencias de escape no sobrevive a ser escrita por un
  programa que tambien las interpreta.** El defecto no lo introduce el descuido: lo introduce la capa
  de por medio, y por eso reaparece justo cuando alguien se pone a documentarlo. `DT-003` nacio asi,
  `DT-004` lo repitio, y esto lo repitio una tercera vez **dentro de su propia correccion**.
- **Por que es peligroso mas alla de la anecdota:** el resultado se ve bien. Nada falla, nada avisa,
  y el texto renderizado es indistinguible del correcto. La unica senal es un barrido de bytes, y un
  barrido solo se corre si alguien decidio correrlo.
- **Y el Paso 2e no lo habria atrapado a tiempo.** Existe, funciona y esta bien puesto — pero corre
  **en el cierre**, cuando el archivo ya lleva horas escrito. Aqui se detecto antes solo porque la
  cifra formaba parte de un criterio de cierre que se estaba reejecutando; sin esa casualidad, habria
  llegado al commit y el hallazgo lo habria abierto la auditoria siguiente.
- **Como aplicarla:** **cuando un archivo vaya a contener una orden con secuencias de escape,
  escribirla en una cadena cruda y correr el barrido de control sobre ese archivo en el momento, no
  al cerrar.** Y si el archivo se genera con un script, el barrido se corre sobre la salida del
  script — no sobre lo que uno cree que escribio.

---

### L-030 - Una nota que explica de donde sale un cambio filtra codigos, y la buena intencion es lo que la hace invisible
| Campo | Valor |
|---|---|
| Fecha | 2026-09-06 |
| Etapa | 000_preproject |
| Origen | manager |

- **Contexto:** `_phases/` tenia **cero codigos instanciados** en toda la carpeta. La sesion anterior
  anadio a un archivo de etapa una nota fechada que empezaba citando la tarea y la decision que la
  producian, y con eso introdujo las dos primeras ocurrencias de la carpeta entera (`F-055`).
- **Que ocurrio, en concreto:** la nota se escribio **para dejar trazabilidad**, que es exactamente
  lo que el resto del repositorio pide hacer en todas partes. En `_persistence/` citar el codigo es
  obligatorio; en `_phases/` esta prohibido, porque la carpeta tiene que poder copiarse a otro
  proyecto tal cual. La misma frase es buena practica en un archivo y fuga en el de al lado.
- **Leccion:** **una regla que cambia de signo segun la carpeta no se sostiene con atencion**, porque
  el gesto correcto y el incorrecto se escriben igual y se sienten igual al escribirlos. Lo que la
  hace cumplible es un control que mire la carpeta, no la intencion.
- **Por que es peligroso mas alla de la anecdota:** una fuga hecha con mala forma se ve al releer
  —desentona—; esta **no desentona**, porque parece rigor. Y el control que existia para las fugas de
  `_phases/` buscaba nombre, ruta y host: un codigo con su numero le pasa por delante sin sonar.
- **Como aplicarla:** **antes de anotar en una carpeta agnostica, comprobar contra que cero se esta
  escribiendo.** Y en general: cuando un archivo tenga cero de algo, esa cifra vale como control
  —cualquier linea nueva es la primera—, asi que conviene barrerla antes de commitear y no despues.
  El Paso 1c del cierre hace exactamente eso sobre `_phases/` y `_workflow/` (`D-087`).

---

### L-031 - Un guion que abre el archivo para escribir antes de tener el contenido lo destruye si falla
| Campo | Valor |
|---|---|
| Fecha | 2026-09-06 |
| Etapa | 000_preproject |
| Origen | manager |

- **Contexto:** al corregir `F-061` se edito `_audit/index.md` con un guion de Python que leia el
  archivo, sustituia un bloque y lo volvia a escribir. El guion fallo al codificar la salida — el
  archivo contiene caracteres que la codificacion por defecto no acepta — y **dejo `_audit/index.md`
  con cero bytes**.
- **Que ocurrio, en concreto:** la escritura se hizo con `open(ruta, 'w')`. Esa llamada **trunca el
  archivo en el momento de abrirlo**, antes de escribir nada. Cuando la excepcion salto en la linea
  siguiente, el contenido original ya no existia. El intento de reparacion inmediato fallo tambien, y
  con un mensaje que no tenia nada que ver —«bloque no encontrado»—, porque estaba buscando en un
  archivo vacio.
- **Como se recupero:** `git show HEAD:_audit/index.md > _audit/index.md`. Se eligio esa forma y no
  `git checkout --`, que el repositorio tiene prohibida en sus protocolos: redirigir la salida de
  `git show` **solo escribe un archivo**, no toca el indice ni el arbol ni la historia.
- **Leccion:** **una edicion en el sitio no es atomica, y su punto de fallo esta antes de escribir.**
  Un guion que abre para escribir apuesta a que todo lo que viene despues funcione; el dia que no
  funciona, el archivo original es la unica copia que habia.
- **Por que es peligroso mas alla de la anecdota:** el archivo destruido era un **tablero de
  auditoria** con veintidos filas de historia. Se recupero porque estaba commiteado y sin cambios;
  con trabajo sin commitear encima, se habria perdido. Y el fallo no avisa de lo que hizo: avisa de
  la codificacion, que es la mitad menos importante.
- **Como aplicarla:** **tener el contenido completo en memoria antes de abrir nada para escribir**, y
  escribir en bytes cuando el archivo pueda llevar caracteres fuera de lo esperado. En la practica:
  leer con `open(ruta, 'rb')`, operar sobre bytes, y no llamar a `open(..., 'wb')` hasta tener el
  resultado entero. **Y comprobar el tamano despues**, que cuesta un `wc -c` — un archivo que ha
  quedado en cero no se distingue de uno correcto hasta que alguien lo abre.

---

### L-032 - El repositorio mezcla finales de linea, y una sustitucion literal falla sin decir por que
| Campo | Valor |
|---|---|
| Fecha | 2026-09-06 |
| Etapa | 000_preproject |
| Origen | manager |

- **Contexto:** tres sustituciones seguidas fallaron con «el bloque no aparece» sobre bloques que
  estaban delante, copiados literalmente de la salida de `sed`. La causa no era el texto: era el final
  de linea.
- **Que ocurrio, en concreto:** este repositorio **no tiene un solo final de linea**. `CLAUDE.md` y
  `project.md` usan `CRLF`; `_persistence/`, `_audit/` y los archivos de `.claude/` usan `LF`. Un
  patron escrito con `\n` no aparece nunca en un archivo `CRLF`, y el error que se recibe —«no
  encontrado»— manda a buscar una diferencia de texto que no existe.
- **Y por que no se vio antes:** `cat -A` lo dice, pero solo si se mira el final de la linea. La
  salida se habia cortado a noventa columnas para que cupiera, y el `^M` cae justo despues.
- **Leccion:** **cuando una sustitucion literal falla sobre un bloque que se acaba de ver, lo primero
  que hay que sospechar no es el texto, es el byte invisible.** Y en un repositorio con finales
  mezclados, esa sospecha acierta la mayoria de las veces.
- **Por que es peligroso mas alla de la anecdota:** el modo de fallo es benigno —no encuentra y no
  escribe—, pero **empuja a reintentar con patrones cada vez mas cortos** hasta que uno coincide por
  casualidad en un sitio que no era. Ese si escribe, y en el archivo equivocado.
- **Como aplicarla:** **detectar el final de linea del archivo y adaptar el patron**, en vez de
  escribirlo a mano por archivo. Una linea basta:

```
$ for f in CLAUDE.md project.md _persistence/decisions.md _audit/index.md .claude/skills/protocol-close/SKILL.md; do
      printf '%-50s ' "$f"
      grep -qU $'\r' "$f" && echo CRLF || echo LF
  done
CLAUDE.md                                          CRLF
project.md                                         CRLF
_persistence/decisions.md                          LF
_audit/index.md                                    LF
.claude/skills/protocol-close/SKILL.md             LF
```

⚠️ **Y no se arregla normalizando el repositorio.** Cambiar el final de linea de un archivo lo marca
entero como modificado en el `git diff`, y eso sepultaria el cambio real de esa sesion bajo miles de
lineas — que es exactamente lo que la auditoria necesita poder leer.
---

### L-033 - Una autorizacion para sustituir texto necesita un borde que se vea, no una prohibicion al lado
| Campo | Valor |
|---|---|
| Fecha | 2026-09-07 |
| Etapa | 000_preproject |
| Origen | manager |

- **Contexto:** el Paso 7c-bis del cierre autoriza sustituir una cosa —la orden vieja por su forma
  anclada— y prohibe tocar otra —la prosa—. Las dos frases estaban escritas, juntas, en la misma
  tabla. Su **primera ejecucion** borro tres lineas de prosa (`F-062`).
- **Que ocurrio, en concreto:** el ejecutor no ignoro la prohibicion. Sustituyo un `⚠️` por un `📌`
  que hablaba **del mismo asunto**, dentro de la **misma entrada** que estaba anclando, y eso se
  parece mucho a la sustitucion que si tenia autorizada. En la entrada de al lado, en la misma
  pasada, el mismo paso lo hizo bien.
- **Leccion:** **cuando un procedimiento autoriza sustituir texto, lo que hace falta no es repetir
  mas fuerte que hay cosas que no se tocan: es decir DONDE termina la zona de sustitucion, con un
  limite visible en el propio archivo.** «No toques la prosa» es una categoria que hay que deducir
  mirando cada linea; «solo dentro del bloque de codigo» es un borde que se ve sin pensar.
- **Por que es peligroso mas alla de la anecdota:** un limite que hay que deducir se deduce bien casi
  siempre, y ese «casi» es indistinguible del cumplimiento hasta que alguien audita. **Cumplirlo la
  mitad de las veces produce exactamente la misma sensacion que cumplirlo entero** para quien lo
  ejecuta.
- **Como aplicarla:** al escribir un paso que autorice modificar un archivo ajeno, la autorizacion se
  formula por **region sintactica** —dentro de este bloque, entre estas marcas, en esta tabla—, nunca
  por **categoria semantica** —«lo mecanico si, el porque no»—. Y si la region no se puede nombrar
  asi, es señal de que el paso todavia no esta acotado.

---

### L-034 - Un pre-compromiso que no distingue el fallo total del parcial se renegocia en su primera aplicacion
| Campo | Valor |
|---|---|
| Fecha | 2026-09-07 |
| Etapa | 000_preproject |
| Origen | manager |

- **Contexto:** `A-010` supuso que una excepcion nueva no se desbordaria, y escribio de antemano que
  hacer si se desbordaba: **retirarla**, con la frase «no se acota con una excepcion nueva». Se
  refuto en su primera oportunidad (`F-062`). Y no se retiro: se acoto (`D-099`).
- **Que ocurrio, en concreto:** la refutacion real no fue la que el supuesto imaginaba. `A-010`
  pensaba en un limite que no se sostiene; lo que hubo fue un limite que se cumplio en una entrada y
  fallo en la de al lado, **en la misma pasada**, por una causa señalable. El pre-compromiso estaba
  escrito para el primer caso y se aplicaba, por su letra, tambien al segundo.
- **Leccion:** **un pre-compromiso vale por lo que impide, no por lo que ordena — y lo que impide es
  que la decision se tome en silencio.** Escribir la consecuencia por adelantado sigue siendo
  correcto; lo que hay que esperar es que el dia que se dispare aparezca un caso que no se previo, y
  **entonces la disciplina no es obedecer la letra: es no poder renegociarla sin dejar rastro.**
- **Por que es peligroso mas alla de la anecdota:** el que renegocia es siempre la parte que se
  beneficia, y siempre tiene un argumento razonable —lo tuvo aqui—. Un pre-compromiso que se
  renegocia **sin registro** desaparece sin que nadie lo note; uno que se renegocia con su decision,
  su razon y la firma de quien lo zanjo sigue costando algo, que es todo lo que se le puede pedir.
- **Como aplicarla:** dos cosas concretas. **(1)** Al escribir un supuesto, la consecuencia se
  redacta con el grado del fallo dentro —«si falla siempre, X; si falla una vez y la causa es
  señalable, Y»—, no como una sola orden. **(2)** Cuando se renegocie de todas formas, **lo decide
  quien no lo escribio** —aqui, el usuario— y va a `decisions.md` con las alternativas descartadas.
  Un pre-compromiso renegociado por su propio autor no dejo de existir: nunca existio.

---

### L-035 - Una regla que nombra un archivo se cumple en ese archivo y se incumple en el de al lado
| Campo | Valor |
|---|---|
| Fecha | 2026-09-07 |
| Etapa | 000_preproject |
| Origen | manager |

- **Contexto:** `F-059` abrio el hueco de las ordenes publicadas con `<hash>` sin anclar. `S-024` lo
  cerro: el Paso 7c-bis anclo `decisions.md`, y `D-096` amplio la convencion a «toda orden que se
  escriba en **este archivo**». En la misma pasada, esa sesion dejo doce ordenes con `<hash>` en
  `tasks.md` — el archivo de al lado, con bloques identicos. Lo encontro `F-067` una auditoria
  despues (`D-102`).
- **Que ocurrio, en concreto:** la ampliacion se escribio con el vocabulario del sitio donde dolia.
  «Toda orden **de este archivo**» suena a generalizacion —pasa de un bloque a un archivo entero—, y
  por eso se leyo como si cerrara el asunto. Lo que hacia era mover la frontera un paso, dejandola
  igual de arbitraria.
- **Leccion:** **al ampliar una regla, la pregunta no es «¿que mas cabe en este archivo?», sino
  «¿que otro sitio tiene la misma forma?».** Un defecto que aparece en un bloque de un archivo esta
  casi siempre en todos los archivos que usan ese bloque; la ampliacion que se queda en el archivo
  donde salio produce la sensacion de haber cerrado el agujero y deja abierto el de al lado.
- **Por que cuesta verlo desde dentro:** el que amplia la regla acaba de corregir el caso concreto y
  lo tiene delante; el archivo vecino no esta en el diff, ni en el hallazgo, ni en la conversacion.
  La unica cosa que los une es la **forma** del bloque, y la forma no aparece en ningun barrido que
  busque por nombre.
- **Como aplicarla:** dos cosas concretas. **(1)** Al ampliar una regla que nace de un hallazgo,
  antes de escribirla se corre el barrido de su patron **sobre todo el repositorio**, no sobre el
  archivo del hallazgo: si el patron aparece en otro sitio, o entra en la regla o queda como
  excepcion escrita. **(2)** La regla se enuncia por la **forma** del artefacto —«todo bloque
  Criterio de cierre»—, y solo despues se lista donde vive hoy. Enunciada por el nombre del archivo,
  caduca el dia que nace el segundo.


---

### L-036 - Una condicion de parada que no se puede cumplir se convierte en una excepcion redactada cada vez
| Campo | Valor |
|---|---|
| Fecha | 2026-09-07 |
| Etapa | 000_preproject |
| Origen | manager |

- **Contexto:** `D-101` escribio un control nuevo en el Paso 7c del cierre — un barrido universal
  cuya salida «tiene que estar VACIA», y una linea obliga a detenerse y reportar. En **su primera
  ejecucion**, en esa misma sesion, devolvio tres lineas. El cierre no se detuvo: escribio «no sale
  vacio, y se explica cada linea en vez de forzarla a cero», justifico las tres en prosa y siguio.
  Lo abrio `F-071` (`D-107`).
- **Que ocurrio, en concreto:** la condicion no era alcanzable, y no por descuido en la ejecucion.
  El patron acertaba en tres clases de linea y solo una era un pendiente real: las otras dos —
  ordenes que llevan el marcador como **dato buscado**, y bloques de sesiones anteriores que `D-019`
  **congela** y que ya tienen su nota fechada — iban a salir en cada cierre futuro, para siempre.
  Una regla asi no se incumple una vez: se incumple **todas**.
- **Y lo caro no fue la parada que no ocurrio, sino lo que la sustituyo.** Al no poder cumplir la
  condicion, el informe redacto la excepcion en su propio texto. Esa prosa —tres parrafos que
  explicaban cada linea y una frase de cierre que las resumia— es donde entraron los otros tres
  hallazgos de la misma auditoria (`F-070`, `F-072`, `F-073`): cifras escritas a mano al lado de una
  salida que ya las contenia.
- **Leccion:** **antes de escribir una condicion de parada, se corre contra el estado actual del
  repositorio.** Si no sale limpia el primer dia, no es un control: es una excepcion que alguien va a
  redactar en cada pasada, y esa redaccion es codigo sin revisar escrito en prosa. El sintoma que hay
  que reconocer es concreto — **el que enuncia la regla y el que la ejecuta la primera vez son el
  mismo**, y por eso la excepcion parece razonable en vez de parecer un incumplimiento.
- **Como aplicarla:** dos cosas concretas. **(1)** Toda condicion binaria que se escriba en un
  protocolo se ejecuta contra `HEAD` **en la misma pasada en que se escribe**, y su salida se publica
  con la decision que la crea; si no sale limpia, se acota la condicion antes de adoptarla, no
  despues. **(2)** Cuando un control legitimo devuelve casos que no son defectos, se parte en dos —
  uno que **informa** y no juzga, y otro **acotado a lo que se puede cumplir**, que es el que detiene.
  Explicar las excepciones en prosa es siempre la tercera opcion, y es la que produce hallazgos.

---

### L-037 - Un criterio que cita el texto que comprueba se acierta a si mismo
| Campo | Valor |
|---|---|
| Fecha | 2026-09-07 |
| Etapa | 000_preproject |
| Origen | manager |

- **Contexto:** al corregir `F-075` se restauro en `T-105` la linea original de su «Criterio de
  cierre» y se escribio el criterio de la decision que lo ordena (`D-111`) como tres `grep -c` sobre
  `_persistence/tasks.md`: uno que la linea original este, otro que la nota de restauracion este, y
  otro que la linea acotada **no** este. Al correrlos dieron `3`, `2` y `1` en vez de `1`, `1` y `0`.
- **Que ocurrio:** la propia correccion **cita** los dos enunciados. La nota de restauracion
  transcribe la linea acotada para que se vea de que se venia, y `T-111` transcribe la original para
  decir que se restauro. Un patron suelto no distingue **la linea que es el criterio** de **una linea
  que la menciona**, asi que el tercer `grep` —el que tenia que devolver cero— devolvia uno, y lo
  devolvia por culpa del texto escrito para corregir el defecto.
- **Y el modo de fallo es el peligroso, no el ruidoso.** Aqui salio de mas y se vio. Al reves —un
  criterio que exige que algo **este** y acierta en su propia cita— sale en verde sin que el archivo
  contenga lo que se afirma, y nadie lo mira otra vez.
- **Leccion:** **un criterio que se escribe con el mismo texto que comprueba tiene que anclarse a la
  forma de la linea, no a su contenido.** `^- \*\*Criterio de cierre:\*\* …$` cuenta criterios;
  el mismo texto sin anclas cuenta menciones. Es el mismo argumento que separa el CENSO del CONTROL
  en `D-107` —la forma literal al principio de la orden—, aplicado a la prosa del registro en vez de
  a las ordenes.
- **Como aplicarla:** cuando la evidencia de una entrada cite el texto que su propio criterio busca,
  el patron lleva `^` y `$` y la parte estructural de la linea —el guion, el `**Criterio de
  cierre:**`, el encabezado—. Y se corre **antes** de publicarlo, no despues: la cifra esperada se
  escribe habiendola visto salir. Lo mismo vale para cualquier archivo que documente sus propios
  barridos, que en este repositorio son casi todos.

📌 **Nota de reincidencia del 2026-09-08.** Volvio a ocurrir al escribir el criterio de cierre de una
tarea nacida de un hallazgo: el criterio buscaba la cadena de su propia nota en el mismo archivo
donde vive la tarea, asi que al correrlo devolvia `2` —la nota y la propia orden que la busca— y no
podia devolver menos de `1` pasara lo que pasara. Se detecto corriendolo antes de publicarlo y se
sustituyo por un criterio que comprueba **el hecho** (las cifras que la nota publica salen de sus
ordenes) en vez del texto. Refuerza la leccion por el lado que no estaba escrito: cuando el criterio
y lo que comprueba viven en el **mismo archivo**, anclar el patron no basta — hay que cambiar de
pregunta.

---

### L-038 - Un patron con `\b` escrito por un script llega al archivo como caracter de control
| Campo | Valor |
|---|---|
| Fecha | 2026-09-08 |
| Etapa | 000_preproject |
| Origen | manager |

- **Contexto:** al registrar una decision cuyo criterio de cierre publica un `grep -E` con limites de
  palabra, la entrada se escribio con un script de Python en vez de a mano.
- **Que ocurrio:** el patron llego al archivo con **`0x08` en lugar de `\b`**, en las dos ordenes
  publicadas. El texto se ve identico en pantalla; `cat -A` lo delata como `^H`. Es el mismo defecto
  que ya tiene deuda registrada en `techdebt.md`, pero por un vector distinto: alli lo introducia
  copiar y pegar una orden ya publicada, aqui lo introduce **la herramienta que escribe**, que
  interpreta la secuencia antes de que llegue al disco. Se detecto porque la orden publicada se
  reejecuto antes de darla por buena, y se corrigio en el acto — la entrada no estaba commiteada.
- **Leccion:** cualquier capa que interprete secuencias de escape —un lenguaje de script, una shell,
  un formateador— puede corromper un patron **en silencio** entre que se escribe y que se guarda. El
  riesgo no esta en el patron: esta en el numero de capas que atraviesa.
- **Como aplicarla:** cuando una orden que se va a **publicar** lleve `\b`, `\d`, `\s` o cualquier
  escape, escribirla con la herramienta de edicion directa y no via script; y comprobar el resultado
  con `cat -A` o un conteo de bytes de control **antes** de dar la entrada por escrita, nunca solo
  releyendola en pantalla. Un caracter de control invisible pasa cualquier revision visual.

📌 **Nota de reincidencia del 2026-09-08.** Volvio a ocurrir en la sesion siguiente, y por el mismo
vector: una decision escrita con un script de Python publico su barrido con `0x08` donde decia `\b`.
Se detecto igual que la primera vez —reejecutando la orden publicada antes de darla por buena, y
confirmando con `cat -A`— y se corrigio antes del commit. Que reaparezca una jornada despues dice que
la parte de «como aplicarla» que pide **no escribir por script** es la que no se sostiene sola: el
script sigue siendo la forma comoda de insertar un bloque largo. Lo que si funciono las dos veces fue
la comprobacion posterior, asi que esa es la mitad que hay que tratar como obligatoria.

---

### L-039 - Un archivo escrito al principio de su etapa describe un andamiaje que la etapa aun no habia construido
| Campo | Valor |
|---|---|
| Fecha | 2026-09-08 |
| Etapa | 000_preproject |
| Origen | usuario |

- **Contexto:** el archivo de etapa de `000_preproject` se escribio pronto, cuando la etapa llevaba
  poco recorrido. Despues la etapa siguio construyendo: nacieron tres carpetas del andamiaje y dos
  agentes mas, cada uno con su decision registrada.
- **Que ocurrio:** el archivo nunca se volvio a leer entero. Seguia enumerando seis carpetas donde ya
  habia ocho, tres agentes donde ya habia cinco, y su condicion de salida afirmaba ser «el espejo de
  los cinco entregables» con una casilla desplazada y una ausente. **Ningun control lo detecto**, y no
  por descuido: los controles del cierre comprueban que el arbol coincida con el registro del
  proyecto y que los archivos agnosticos no filtren datos propios; ninguno compara **un archivo de
  etapa con lo que la etapa ha ido produciendo**. El archivo era coherente consigo mismo y falso
  respecto del repositorio.
- **Leccion:** un archivo que describe una etapa **desde dentro de esa etapa** envejece al ritmo del
  trabajo que describe, y es el unico documento del que nadie sospecha, porque se leyo al principio y
  «ya estaba escrito». Es el caso peor de una carpeta declarada que nadie abre: aqui si se abre, pero
  para consultar una seccion suelta —que autoriza, que prohibe— y nunca para contrastarlo entero.
- **Como aplicarla:** **al cerrar una etapa, releer su archivo de etapa completo contra lo que la
  etapa produjo**, antes de dar la condicion de salida por cumplida — y muy especialmente cuando la
  etapa haya creado carpetas o agentes que el archivo no nombraba el dia que se escribio. La pregunta
  util no es «¿el archivo esta bien?» sino **«¿cuantas cosas nombra, y cuantas hay?»**, que se
  contesta contando, no leyendo. Vale para cualquier etapa, y con mas motivo para la primera: es la
  unica cuyo objeto es construir el sistema que despues comprueba a las demas.

---

### L-040 - Una prohibicion que ya reincidio no se arregla escribiendola mejor
| Campo | Valor |
|---|---|
| Fecha | 2026-09-08 |
| Etapa | 000_preproject |
| Origen | report_auditor |

- **Contexto:** una auditoria abrio que el paso de anclaje del cierre habia borrado prosa del
  registro. Se corrigio reforzando el texto del paso: se enuncio la frontera con mas precision —«lo
  que se reescribe vive dentro del bloque de codigo»— y se repitio la prohibicion en tres sitios
  distintos del mismo paso. El hallazgo se cerro como `Implementado` en la auditoria siguiente.
- **Que ocurrio:** tres sesiones despues, el mismo paso volvio a borrar prosa, en dos entradas, y una
  de las lineas perdidas era **el enunciado del criterio** — la mitad que permite juzgar si la salida
  publicada lo cumple. El texto reforzado seguia ahi, literal y sin tocar.
- **Y lo que hace util el caso es que la primera correccion no fue floja.** Estaba bien escrita, bien
  colocada y era correcta. Simplemente pertenecia a una clase de correccion que no puede funcionar
  sola: **las que dependen de que quien ejecuta lea y aplique**. Con el volumen de un protocolo largo,
  esa dependencia falla tarde o temprano, y falla en silencio.
- **Leccion:** **la reincidencia es informacion sobre la clase de correccion, no sobre la disciplina
  de quien la incumplio.** Cuando una conducta prohibida vuelve, la pregunta deja de ser «¿como lo
  digo mejor?» y pasa a ser «¿que orden lo detecta?». Un hallazgo cerrado con texto y uno cerrado con
  un control estan cerrados de dos maneras distintas, y solo la segunda sobrevive a que nadie se
  acuerde.
- ⚠️ **Y el corolario incomodo:** un `Implementado` cuya correccion fue anadir texto **no es garantia
  de nada** para el futuro; es garantia de que en ese commit el texto estaba. Vale la pena mirarlo
  asi al evaluar hallazgos que se parecen a otros ya cerrados.
- **Como aplicarla:** al aceptar un hallazgo, comprobar si ya hubo uno de la misma forma. Si lo hubo
  y se cerro con texto, la correccion de esta vez **incluye un control ejecutable** —una orden que
  devuelve lineas o no las devuelve— y no solo una redaccion mejor. El control se escribe en el paso
  que puede romperse, se declara obligatorio, y lleva su tabla de «que sale / que significa / que
  haces», con la fila de «el comando fallo» incluida.

---

### L-041 - Un criterio sin artefacto donde firmarse no falla hasta que alguien intenta usarlo
| Campo | Valor |
|---|---|
| Fecha | 2026-09-08 |
| Etapa | 000_preproject |
| Origen | usuario |

- **Contexto:** el archivo de la etapa preparatoria lleva veintiocho sesiones declarando su condicion
  de salida, y la ultima linea de esa seccion exige desde hace tiempo que **cada casilla se compruebe
  con una orden y su salida cruda**. El usuario pregunto si no faltaria un archivo que certificase el
  cierre de la etapa.
- **Que ocurrio:** faltaba. No el criterio —el criterio estaba escrito, revisado y auditado— sino
  **el sitio donde el resultado queda y las firmas que lo cierran**. Y nadie lo habia notado, ni
  `manager` ni cuatro auditorias seguidas, por una razon simple: **la etapa nunca habia intentado
  cerrar**. Un criterio que no se ejerce se lee bien indefinidamente.
- **Leccion:** **un criterio y el artefacto que lo registra son dos cosas, y solo la primera se nota
  cuando falta la segunda.** Una condicion de salida sin acta produce una etapa que se cierra por
  consenso tacito: nadie pega evidencia, nadie firma, y el paso a la etapa siguiente ocurre porque
  alguien empezo a trabajar en ella.
- **Y el modo de fallo es el silencioso:** no hay error, no hay contradiccion, no hay linea que un
  barrido devuelva. El archivo dice lo correcto; simplemente no hay donde escribir la respuesta.
- **Como aplicarla:** al escribir una condicion de salida —de una etapa, de un Gate, de lo que sea—
  se escribe **en la misma pasada** donde queda su resultado y quien lo firma. Y la pregunta que lo
  destapa, que conviene hacerse en voz alta: *«cuando esto se cumpla, ¿en que archivo se ve, y quien
  lo firma?»*. Si la respuesta es «se sabra», no hay artefacto.

---

### L-042 - El dato que siempre sale falso suele ser el que nadie usa, y entonces la correccion es quitarlo
| Campo | Valor |
|---|---|
| Fecha | 2026-09-08 |
| Etapa | 000_preproject |
| Origen | report_auditor |

- **Contexto:** un paso del cierre publicaba dos cifras sobre la misma lista: una **principal** —el
  numero de lineas que devolvia la orden— y una **accesoria** —cuantas de esas lineas eran ordenes
  distintas—. Tres auditorias distintas abrieron el mismo hallazgo: la accesoria era falsa. Las tres
  veces la principal estaba bien.
- **Que ocurrio:** las dos primeras correcciones fueron reglas escritas, y las dos eran razonables —
  «va aparte y con ese nombre», «va con SU orden y su salida cruda, no se estima». Las dos seguian
  vivas, literales y sin tocar, el dia que se escribio la tercera cifra falsa.
- **Lo que la tercera vez dejo ver, y las dos primeras no:** no era una cifra dificil de calcular. Era
  una cifra que **ninguna otra parte del protocolo consumia**. Nadie la leia, nadie la comparaba con
  nada, ningun control dependia de ella — y por eso era exactamente la que se escribia a ojo mientras
  la principal, que si se usaba, salia siempre bien.
- **Leccion:** **cuando un dato sale falso una y otra vez, hay que mirar quien lo consume antes de
  reforzar la regla que lo vigila.** Si no lo consume nadie, no es un problema de disciplina: es un
  dato que existe por inercia, y la correccion que funciona es **suprimirlo**. Un dato que no se
  publica no se puede publicar mal.
- 🔑 **Y esto no contradice a `L-040`, lo completa.** Aquella dice que una prohibicion reincidente
  se cierra con un control ejecutable en vez de con mas texto. Esta anade el paso previo: antes de
  elegir el control, preguntar si lo vigilado hace falta. Un control cuesta escribirlo, correrlo y
  mantenerlo cada sesion; suprimir cuesta una vez y quita el fallo entero, no lo detecta.
- ⚠️ **Y el limite, porque es facil pasarse:** esto vale para lo **accesorio**, no para lo incomodo.
  La pregunta es «¿quien lee esto?», no «¿me molesta calcularlo?». Si algo lo consume —un control,
  una decision, una casilla de salida—, sigue haciendo falta y se defiende con un contraste mecanico.
- **Como aplicarla:** al aceptar el tercer hallazgo sobre la misma cifra, listar que la usa. Si la
  lista sale vacia, la correccion es la supresion, con su decision y sus alternativas escritas —
  incluida la de vigilarla mejor, para que conste que se considero.

---

### L-043 - Una condicion escrita en prosa se recorre mecanicamente, pero no se verifica entera — y eso pide un tercer valor
| Campo | Valor |
|---|---|
| Fecha | 2026-09-08 |
| Etapa | 000_preproject |
| Origen | manager |

- **Contexto:** se iba a construir un agente generico que verificara la condicion de salida de
  cualquier etapa leyendola del archivo de esa etapa. Habia un supuesto abierto detras: que las
  condiciones fueran lo bastante uniformes para que un solo procedimiento las recorriera.
- **Que ocurrio al comprobarlo:** el supuesto se parte limpiamente en dos mitades, y solo una
  aguanta. **Localizar la seccion, extraer las casillas y contrastar su recuento** funciona identico
  en las siete etapas, sin cambiar una letra de la orden. **Verificar cada casilla, no.** Una parte de
  ellas pregunta por un hecho —«existe el archivo», «el barrido devuelve cero lineas»— y de ahi sale
  una orden; otra parte pregunta por un juicio —si un actor es «alcanzable», si un enunciado nombra o
  no una pantalla— y esas **no tienen orden posible, ni hoy ni nunca**.
- **Leccion:** **que una condicion se pueda recorrer con una orden no significa que se pueda
  comprobar con una orden, y confundir las dos cosas produce el peor de los resultados.** Si el
  procedimiento solo admite «cumple» y «no cumple», las casillas de juicio se van a resolver
  inventando una orden que se les parezca — un `grep` que cuenta apariciones de una palabra— y esa
  cifra se leera despues como si alguien hubiera verificado el juicio.
- 🔑 **La salida no es reescribir las casillas para que sean todas mecanicas.** Muchas no lo pueden
  ser sin dejar de decir lo que importan: «alcanzable» no tiene sustituto contable. La salida es
  **un tercer valor de primera clase** —`NO COMPROBABLE`, con su razon escrita— que sea una respuesta
  legitima y no una rendicion. Con el, un procedimiento generico basta; sin el, hacen falta
  instrucciones por etapa o mentiras por casilla.
- ⚠️ **Y el tercer valor solo funciona si esta prohibido redondearlo.** `NO COMPROBABLE` que se
  redondea a `CUMPLE` da exactamente el mismo verde que una verificacion, y entonces vuelve a ser
  peor que no tenerlo.
- **Como aplicarla:** al escribir un procedimiento que verifique una lista de condiciones en prosa,
  clasificar primero cada una en **hecho** o **juicio**, y dar al procedimiento los tres valores desde
  el principio — con la prohibicion explicita de fabricar una orden para un juicio. La pregunta que lo
  destapa: *«¿que orden devolveria un numero distinto si esto fuera falso?»*. Si no hay ninguna, es
  juicio.

---

### L-044 - Lo que crees saber de tu propio repositorio se comprueba con una orden, sobre todo cuando parece obvio
| Campo | Valor |
|---|---|
| Fecha | 2026-09-08 |
| Etapa | 000_preproject |
| Origen | manager |

- **Contexto:** al registrar por que un agente nuevo corria con un modelo distinto, `manager` escribio
  la decision apoyandose en una premisa que le parecia evidente: que todos los agentes anteriores
  usaban el mismo modelo, y que el nuevo seria la primera excepcion.
- **Que ocurrio:** era falso. Corrida la orden —`grep -H '^model:' .claude/agents/*.md`— aparecieron
  **tres modelos distintos** ya en uso. La decision entera estaba construida sobre un contraste que no
  existia, empezando por su titulo.
- **Como se detecto, que es la parte util:** no por releerla. Se detecto porque el criterio de cierre
  de esa misma decision **exigia pegar la salida de la orden**, y al correrla para pegarla salio otra
  cosa. La regla de «toda afirmacion con su orden y su salida cruda» se escribio pensando en el
  auditor; aqui cazo un error **antes** de que llegara a existir en el commit.
- **Leccion:** **una premisa sobre el estado del propio repositorio no es conocimiento, es memoria — y
  la memoria de un repositorio que se edita a diario esta desactualizada por defecto.** El riesgo es
  peor cuanto mas obvia parece la premisa, porque lo obvio es justo lo que nadie corre.
- 🔑 **Y hay un patron que lo hace evidente:** las premisas peligrosas son las que empiezan por «los
  cinco», «todos los», «el unico que», «siempre se ha». Un cuantificador sobre el propio repositorio
  es una orden esperando a ser escrita.
- ⚠️ **Lo que salvo el caso no fue el cuidado, fue el orden de trabajo.** El criterio de cierre se
  escribio **antes** de dar la decision por terminada, y correrlo fue lo que rompio la premisa. Si el
  bloque de verificacion se hubiera dejado para el final —o para el cierre—, la decision falsa ya
  estaria commiteada y habria que corregirla por nota fechada.
- **Como aplicarla:** cualquier afirmacion cuantificada sobre el repositorio va con su orden **en la
  misma pasada en que se escribe**, no al revisar. Y si la orden devuelve algo distinto de lo
  esperado, lo que se reescribe es la afirmacion — incluido su titulo, si hace falta.

---

### L-045 - Un contraste solo prueba lo que su ambito alcanza, y el ambito no se comprueba a si mismo
| Campo | Valor |
|---|---|
| Fecha | 2026-09-10 |
| Etapa | 000_preproject |
| Origen | manager |

- **Contexto:** un paso del cierre barre caracteres de control sobre «los archivos que el commit
  toca». La sesion anterior le anadio **dos contrastes** precisamente porque la tabla se habia
  transcrito a mano: uno cuenta cuantas filas debe tener, el otro suma el total por otro camino.
- **Que ocurrio:** la tabla, sus dos contrastes y su conclusion cuadraron perfectamente entre si — y
  los tres estaban cortos. El barrido medía el area de staging del momento, y el cierre escribe tres
  archivos **despues** de ese momento. Los dos contrastes se derivaban del mismo staging, asi que no
  podian ver lo que faltaba.
- **Leccion:** **dos ordenes que preguntan lo mismo por caminos distintos siguen sin ver nada si
  parten del mismo ambito.** Un contraste valida la transcripcion, no la delimitacion. Y el ambito es
  justo lo que ninguna de las dos ordenes puede cuestionar, porque las dos lo dan por dado.
- 🔑 **La senal que lo delata:** cuando la frase que declara el ambito y la orden que lo produce usan
  palabras distintas. «Los archivos que el commit toca» y `git diff --cached` **no** son lo mismo, y
  la distancia entre las dos frases es exactamente el agujero.
- **Como aplicarla:** al escribir un control, comprobar que su orden **produce** el ambito que su
  prosa **declara**. Si no lo produce —porque el ambito aun no esta completo cuando el control
  corre—, el control se repite mas tarde sobre el ambito real, y esa segunda salida se publica.

---

### L-046 - Un cambio en el registro y el mismo cambio en su plantilla son dos cambios, y se cuentan
| Campo | Valor |
|---|---|
| Fecha | 2026-09-10 |
| Etapa | 000_preproject |
| Origen | manager |

- **Contexto:** una sesion actualizo dos filas de `project.md` y describio en su informe que la
  plantilla de la que ese archivo nace habia recibido «el mismo cambio».
- **Que ocurrio:** habia recibido uno de los dos. La plantilla quedo describiendo una carpeta que ya
  no coincide con lo que el repositorio hace — y una plantilla existe para copiarse, asi que el
  defecto no se queda donde nace: viaja al siguiente proyecto.
- **Leccion:** **«el mismo cambio» es una afirmacion sobre dos archivos, y se verifica sobre los
  dos.** La forma barata de hacerlo es la que ya usa el resto del repositorio: la misma cadena
  buscada en los dos sitios, con sus dos salidas.
- 🔑 **Por que se cuela con tanta facilidad:** el par registro/plantilla se edita en la misma pasada
  mental, y al segundo archivo se llega con el primero ya resuelto. La memoria dice «hecho» cuando lo
  hecho es la mitad.
- **Como aplicarla:** cuando un cambio toca un archivo que tiene plantilla, la evidencia son **dos**
  ordenes con la misma cadena, una por archivo. Si las dos no devuelven lo mismo, el cambio esta a
  medias — y decirlo «el mismo cambio» lo oculta.

---

### L-047 - Una regla que nombra el sitio solo protege ese sitio
| Campo | Valor |
|---|---|
| Fecha | 2026-09-10 |
| Etapa | 000_preproject |
| Origen | manager |

- **Contexto:** un mismo defecto —una cifra tecleada al lado de la orden que la desmiente— aparecio
  cinco veces en informes sucesivos. Cada vez se corrigio con una regla nueva, y cada regla se
  escribio **para la seccion donde el defecto acababa de aparecer**: una para la seccion de
  supuestos, otra para el desglose de la nota de cierre.
- **Que ocurrio:** el commit que estreno las dos reglas las incumplio las dos, y no donde miraban:
  una cifra en la prosa de **otra** seccion, y una lista que la primera regla **autorizaba
  expresamente** a escribir a mano. Las reglas funcionaron: lo que fallo es que su alcance era el
  lugar del ultimo caso, no la forma del defecto.
- **Leccion:** **una regla redactada alrededor del sitio donde algo fallo deja intacto el sitio de al
  lado, y ahi es exactamente donde vuelve a fallar.** Peor: al nombrar un lugar, la regla insinua que
  los demas estan permitidos — la lista tecleada de la quinta ocurrencia no se colo pese a la regla,
  se colo **amparada** por ella.
- 🔑 **La senal que lo delata:** la regla se puede enunciar nombrando una seccion, un archivo o un
  paso. Si al quitarle el complemento de lugar la frase sigue siendo verdadera y util, el lugar
  sobraba y estaba haciendo dano.
- **Como aplicarla:** al corregir una reincidencia, escribir la regla **sin lugar** y comprobar dos
  cosas: que ninguna regla anterior autorice como excepcion lo que la nueva prohibe, y que la forma
  del defecto —no su ultimo domicilio— sea lo que queda descrito.
- ⚠️ **Y esto no pide un control mecanico automatico.** Cuando se midio uno para este defecto marcaba
  del orden de 130 lineas legitimas en un solo archivo: hay defectos cuya unica defensa es la forma
  de redactar, y confundirlos con los que se barren produce ruido que despues nadie mira.

> 📌 **Nota del 2026-09-10 (`F-093`, `D-137`).** La viñeta de arriba **no se reescribe**, pero su
> ultima frase quedo desmentida por los hechos: la regla generica que esta leccion pedia se escribio,
> y el mismo commit que la estreno volvio a incumplirla. Existe un ambito de control que si funciona
> —la prosa que sigue a un bloque de salida cruda—, y devuelve del orden de diez lineas por informe
> en vez de 130. Lo que se habia medido y descartado era **otro** barrido, el de todos los numeros de
> la prosa. `D-137` lo adopta y `L-049` recoge la leccion de fondo.
>
> 🔑 **Lo que la nota no cambia:** el cuerpo de la leccion se sostiene entero. Una regla que nombra
> el sitio sigue protegiendo solo ese sitio, y quitarle el lugar sigue siendo lo correcto. Lo que se
> demostro falso es que la regla **bastara** por si sola.

---

### L-048 - Un criterio que busca una frase no distingue el texto corregido de su cita
| Campo | Valor |
|---|---|
| Fecha | 2026-09-10 |
| Etapa | 000_preproject |
| Origen | manager |

- **Contexto:** una tarea movia una fila de una tabla a otro sitio de un protocolo. Su criterio de
  cierre buscaba, con `grep -c`, la frase que esa fila contenia, y esperaba `0`.
- **Que ocurrio:** la tarea quedo bien hecha y el criterio devolvio `1`. El motivo es que el mismo
  cambio anadia una nota explicando **por que** la fila se habia movido, y esa nota **citaba la frase
  entre comillas**. El criterio no estaba viendo la fila: estaba viendo su explicacion.
- **Leccion:** **un `grep` de una frase no sabe si lo que encuentra es el defecto o el texto que
  cuenta como se corrigio.** Y este repositorio corrige casi siempre citando lo corregido —notas
  fechadas, decisiones con alternativas descartadas, reglas que explican de que fallo nacieron—, asi
  que la colision no es rara: es la forma normal de trabajar aqui.
- 🔑 **La senal que lo delata:** el criterio busca **prosa**. Si la cadena buscada es una frase que
  alguien podria citar al explicar el cambio, el criterio esta mal apuntado.
- **Como aplicarla:** anclar el criterio a la **forma estructural** de lo que cambia, no a su
  redaccion — la fila de una tabla por su patron de fila (`^| ...`), un encabezado por su nivel, un
  campo por su clave. Y cuando se espera un `0`, comprobarlo **antes** de dar la tarea por hecha: un
  criterio que falla con el trabajo bien hecho se corrige entonces, o se convierte en una discusion
  con la auditoria siguiente.
- ⚠️ **La direccion contraria es peor y menos visible:** un criterio que espera `1` y encuentra su
  propia cita **pasa**, con el trabajo sin hacer. Aqui salto a la vista porque esperaba `0`.

---

### L-049 - Medir un control y descartarlo prueba que ESE ambito no sirve, no que no exista uno que si
| Campo | Valor |
|---|---|
| Fecha | 2026-09-10 |
| Etapa | 000_preproject |
| Origen | manager |

- **Contexto:** un defecto reincidente —una cifra tecleada al lado de la orden que la desmiente— se
  intento atajar tres veces seguidas reescribiendo la regla que lo prohibia. La segunda vez se
  planteo ademas un control mecanico, se **midio** antes de adoptarlo, y se descarto con razon: un
  barrido de numeros en la prosa de un informe marcaba 129 lineas, casi todas legitimas.
- **Que ocurrio:** la regla reescrita fallo otra vez, en el commit que la estrenaba. Al volver sobre
  el control descartado resulto que **lo que sobraba era el ambito, no la idea**: acotado a la prosa
  que sigue a un bloque de salida cruda —los tres renglones de despues—, el mismo barrido devuelve
  del orden de diez lineas por informe y atrapa los dos defectos que habian motivado las reglas.
- **Leccion:** **una medicion que descarta un control descarta el control que se midio, y solo ese.**
  Escrita en el registro como «no hay control mecanico que cubra esto», la conclusion se lee despues
  como si el espacio de ambitos posibles se hubiera agotado — y nadie vuelve a mirar. El coste de esa
  frase de mas fueron dos reincidencias.
- 🔑 **La senal que lo delata:** la conclusion descartada esta enunciada **sin su ambito**. «Se midio
  y es ruido» oculta cual era el barrido; «un barrido de TODOS los numeros de la prosa es ruido» deja
  a la vista el adjetivo que se puede estrechar.
- **Como aplicarla:** al descartar un control por ruidoso, registrar **el ambito exacto que se midio**
  junto a la cifra, y enunciar el descarte acotado a el. Y cuando el defecto reincida pese a la regla
  de redaccion, el primer sitio donde mirar es el control descartado: casi siempre existe un recorte
  del ambito que separa la senal del ruido.
- ⚠️ **Y el criterio de exito de un control asi no es que salga vacio.** Este devuelve unas diez
  lineas legitimas por informe a proposito; lo que lo hace util es que **agrupa** las cifras que
  hablan de lo mismo, que en el archivo estan a decenas de lineas unas de otras. Un control cuya
  respuesta correcta no es cero necesita su condicion de parada escrita, o se lee como una alarma
  rota y se acaba ignorando.

---

### L-050 - Un control que enumera casos caduca solo; uno que reconoce la forma, no
| Campo | Valor |
|---|---|
| Fecha | 2026-09-10 |
| Etapa | 000_preproject |
| Origen | manager |

- **Contexto:** un control buscaba una fuga citando **la lista de prefijos de codigo que existian el
  dia que se escribio**. Con el tiempo nacieron diez prefijos mas, y ninguno se anadio a la lista:
  nadie recuerda tocar un control cuando lo que cambia es otra cosa.
- **Que ocurrio:** el control devolvia cero, y ese cero se leia como «limpio». Inyectando dos citas
  reales en el archivo que vigilaba, **siguio devolviendo cero**. Llevaba ciego un tiempo
  indeterminado sin que nada lo delatara, porque un instrumento ciego y uno limpio dan la misma
  salida.
- **Leccion:** **un control que enumera los casos que conoce se degrada cada vez que nace un caso
  nuevo, y se degrada en silencio.** Su mantenimiento depende de que alguien, mientras hace otra
  cosa, se acuerde de el — y el dia que no se acuerde es exactamente el dia que el control hacia
  falta. Reconocer la **forma** de lo que se busca (`[A-Z]{1,2}-[0-9]+` en vez de dieciocho prefijos)
  no necesita mantenimiento: los casos nuevos entran solos.
- 🔑 **La senal que lo delata:** el control lleva dentro una lista, y esa lista es una copia de algo
  que vive en otro sitio y crece por su cuenta. Si al nacer una entrada nueva en el original hay que
  ir a tocar el control, el control ya esta caducando.
- **Como aplicarla:** buscar por forma y **declarar las excepciones una a una**, en vez de enumerar
  lo incluido. La lista de excepciones es corta, estable y se justifica; la de casos incluidos es
  larga, crece y nadie la mantiene. Y cuando la forma produzca ruido legitimo, medirlo antes de
  decidir: aqui eran 14 lineas, todas de una misma serie, que se excluyo declarandola.
- ⚠️ **Un control no se da por bueno porque devuelva cero: se da por bueno cuando se ha visto
  fallar.** La unica prueba que vale es inyectar la fuga que deberia detectar, comprobar que la ve, y
  deshacer. Cuesta dos ordenes y es la diferencia entre un control y la creencia de tener uno.

---

### L-051 - Una tarea escrita para «mas adelante» describe el repositorio del dia que se escribio
| Campo | Valor |
|---|---|
| Fecha | 2026-09-10 |
| Etapa | 000_preproject |
| Origen | manager |

- **Contexto:** una tarea pedia **anadir** un control a un protocolo. Al ir a implementarla, cinco
  sesiones despues, el control ya existia — y no lo habia hecho nadie entretanto: **existia ya el dia
  que la tarea se escribio**, en el commit de esa misma sesion, en un paso contiguo al que la tarea
  nombraba.
- **Que ocurrio:** no se perdio trabajo, porque al implementarla lo primero fue mirar el estado real
  y aparecio el control. Pero durante cinco sesiones el registro de tareas afirmo que faltaba algo
  que estaba hecho, y eso es lo que el arranque lee cada manana para decidir por donde seguir.
- **Leccion:** **una tarea no es una descripcion del trabajo pendiente: es una foto de lo que su
  autor creia el dia que la escribio.** Cuanto mas tarda en ejecutarse, mas probable es que describa
  un repositorio que ya no existe — y su enunciado se lee con la misma autoridad el primer dia que el
  quincuagesimo.
- 🔑 **La senal que lo delata:** la tarea dice «anadir», «crear» o «escribir» algo, y han pasado
  sesiones desde que se registro. Ese verbo es una afirmacion sobre el presente, y nadie la ha vuelto
  a comprobar.
- **Como aplicarla:** al abrir una tarea vieja, **verificar su premisa contra `HEAD` antes de
  ejecutarla**, con su orden y su salida — exactamente igual que se hace con un hallazgo de
  auditoria, y por el mismo motivo. Si la premisa cayo, la tarea no se borra: se cierra dejando
  escrito **que se encontro en su lugar**, que casi siempre es un trabajo distinto y mas pequeño.
- ⚠️ **Y conviene mirar el paso de al lado, no solo el que la tarea nombra.** Aqui el control estaba
  en el paso contiguo con otro numero: buscando solo donde la tarea decia, no habria aparecido.
