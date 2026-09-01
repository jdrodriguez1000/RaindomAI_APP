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
