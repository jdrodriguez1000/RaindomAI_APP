# decisions.md

> Registro de las **decisiones tomadas** en el proyecto.
> Cada decision tiene codigo `D-XXX` y se considera vigente hasta que otra la revoque.

---

## Indice

| Codigo | Decision | Fecha | Estado |
|---|---|---|---|
| [D-001](#d-001---el-estado-del-proyecto-se-persiste-en-siete-archivos) | El estado del proyecto se persiste en siete archivos | 2026-08-31 | Vigente |
| [D-002](#d-002---los-archivos-de-persistencia-arrancan-vacios) | Los archivos de persistencia arrancan vacios | 2026-08-31 | Vigente |
| [D-003](#d-003---el-procedimiento-vive-en-la-skill-y-el-agente-solo-dice-quien-es) | El procedimiento vive en la skill, y el agente solo dice quien es | 2026-08-31 | Vigente |
| [D-004](#d-004---el-reparto-de-escritura-entre-el-cierre-y-manager) | El reparto de escritura entre el cierre y `manager` | 2026-08-31 | Vigente |
| [D-005](#d-005---control-de-versiones-con-git-y-remoto-en-github) | Control de versiones con git y remoto en GitHub | 2026-08-31 | Vigente |
| [D-006](#d-006---temporal-queda-fuera-del-repositorio) | `temporal/` queda fuera del repositorio | 2026-08-31 | Vigente |
| [D-007](#d-007---los-datos-propios-del-proyecto-viven-solo-en-projectmd) | Los datos propios del proyecto viven solo en `project.md` | 2026-08-31 | Vigente |
| [D-008](#d-008---modelo-de-trabajo-de-dos-terminales) | Modelo de trabajo de dos terminales | 2026-08-31 | Revocada por D-012 |
| [D-009](#d-009---el-informe-de-sesion-se-ancla-al-commit-que-lo-contiene) | El informe de sesion se ancla al commit que lo contiene | 2026-08-31 | Vigente |
| [D-010](#d-010---el-rol-de-esta-sesion-se-llama-manager) | El rol de esta sesion se llama `manager` | 2026-08-31 | Vigente |
| [D-011](#d-011---solo-projectmd-y-el-brief-pueden-llevar-datos-propios) | Solo `project.md` y el brief pueden llevar datos propios | 2026-08-31 | Vigente |
| [D-012](#d-012---la-auditoria-la-hace-un-agente-en-este-mismo-repositorio) | La auditoria la hace un agente en este mismo repositorio | 2026-08-31 | Vigente |
| [D-013](#d-013---la-auditoria-corre-despues-del-commit-no-antes) | La auditoria corre despues del commit, no antes | 2026-08-31 | Vigente |
| [D-014](#d-014---los-hallazgos-tienen-registro-propio-que-sobrevive-al-rechazo) | Los hallazgos tienen registro propio, que sobrevive al rechazo | 2026-08-31 | Vigente |
| [D-015](#d-015---cerrar-un-hallazgo-es-de-la-auditoria-no-de-manager) | Cerrar un hallazgo es de la auditoria, no de `manager` | 2026-08-31 | Vigente |
| [D-016](#d-016---el-agente-auditor-pasa-a-llamarse-report_auditor) | El agente auditor pasa a llamarse `report_auditor` | 2026-08-31 | Vigente |
| [D-017](#d-017---espanol-para-el-contenido-ingles-para-los-nombres-de-archivos-y-carpetas) | Espanol para el contenido, ingles para los nombres de archivos y carpetas | 2026-08-31 | Vigente |
| [D-018](#d-018---cinco-principios-de-ingenieria-y-siete-reglas-de-operacion-en-claudemd) | Cinco principios de ingenieria y siete reglas de operacion en `CLAUDE.md` | 2026-08-31 | Vigente |
| [D-019](#d-019---un-bloque-de-verificacion-antiguo-se-corrige-por-nota-fechada-nunca-reescribiendolo) | Un bloque de verificacion antiguo se corrige por nota fechada, nunca reescribiendolo | 2026-09-01 | Vigente |
| [D-020](#d-020---manager-escribe-en-tasksmd-al-registrar-un-hallazgo-de-auditoria) | `manager` escribe en `tasks.md` al registrar un hallazgo de auditoria | 2026-09-01 | Vigente |

---

## Convenciones

| Campo | Valores posibles |
|---|---|
| Codigo | `D-XXX`, correlativo, no se reutiliza |
| Estado | `Vigente` / `Revocada por D-XXX` |
| Origen | `usuario` / `manager` / `report_auditor` |

🚨 **Una decision no se borra ni se reescribe: se revoca.** La entrada antigua se queda con
`Revocada por D-XXX` en su estado, y la nueva explica que cambio y por que. El historial de por que
se penso distinto en su momento es parte del registro.

🚨 **Toda decision que verifica algo antes de aceptarlo lleva comando y salida cruda.** No se
escribe «se comprobo que…» de memoria: va el comando ejecutado y su salida literal.

⚠️ **El titulo nombra la decision, no su consecuencia**, y no cambia despues.

🚨 **El indice se escribe a mano, sin generador.** Cada fila enlaza por ancla a su decision.

---

## Decisiones

### D-001 - El estado del proyecto se persiste en siete archivos
| Campo | Valor |
|---|---|
| Fecha | 2026-08-31 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** el usuario aporto los archivos de persistencia de un proyecto anterior como guia de
  forma, y habia que decidir si se adoptaban aqui.
- **Decision:** el estado vive en `_persistence/`, en siete archivos con la misma forma: indice
  arriba, convenciones despues, detalle debajo. Cada uno con su codigo propio, correlativo y no
  reutilizable — `S-XXX`/`H-nn`, `T-XXX`, `D-XXX`, `C-XXX`, `A-XXX`, `L-XXX`, `DT-XXX`.
- **Por que:** un registro repartido en archivos con forma distinta obliga a aprender siete formatos
  y a decidir cada vez donde va cada cosa. Con forma unica, el indice responde casi siempre y el
  detalle es la excepcion — que es lo que permite que un archivo crezca sin que leerlo cueste una
  sesion entera.
- **Alternativas descartadas:** un unico archivo de bitacora (no se puede consultar por tipo, y
  crece sin techo); herramienta externa de tickets (saca el registro del repositorio, y entonces el
  `git diff` deja de poder contrastarlo).

---

### D-002 - Los archivos de persistencia arrancan vacios
| Campo | Valor |
|---|---|
| Fecha | 2026-08-31 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** los archivos del proyecto anterior venian llenos: 54 decisiones, 11 lecciones, 56
  tareas. Habia que decidir si se heredaba algo.
- **Decision:** se adopta **la forma** y se descarta **el contenido**. Los siete archivos arrancan
  con cabecera, indice y convenciones, sin ninguna entrada, y la numeracion empieza en 001.
- **Por que:** el contenido heredado citaba archivos, commits y auditorias que aqui no existen. Una
  entrada que apunta al vacio no es historia: es ruido con aspecto de historia, y quien la lea
  tendra que averiguar si le falta contexto o si el dato es falso.
- **Alternativas descartadas:** copiar todo tal cual (arrastra referencias muertas); heredar solo lo
  «de metodo» renumerado (obliga a decidir entrada por entrada que es metodo y que es proyecto, y
  esa frontera no es limpia).

---

### D-003 - El procedimiento vive en la skill, y el agente solo dice quien es
| Campo | Valor |
|---|---|
| Fecha | 2026-08-31 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** cada protocolo del ciclo de sesion se implemento como una pareja agente + skill.
- **Decision:** el archivo del agente dice **quien es y que no puede hacer**; la skill dice **que
  hacer**, paso a paso. El agente no replica ni un comando del procedimiento, y la skill es de uso
  exclusivo de su agente.
- **Por que:** un agente que se lleva el procedimiento en el cuerpo deja de delegar y empieza a
  competir con la skill. Ante una discrepancia seguiria su propia copia, **que es siempre la mas
  vieja**, y el desfase no daria error: daria un resultado plausible y equivocado.
- **Alternativas descartadas:** todo el procedimiento dentro del agente (un solo archivo, pero el
  procedimiento deja de poder reutilizarse y de poder auditarse por separado).

---

### D-004 - El reparto de escritura entre el cierre y `manager`
| Campo | Valor |
|---|---|
| Fecha | 2026-08-31 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** hay siete archivos de registro y dos actores que podrian escribirlos.
- **Decision:** `progress.md` y `tasks.md` los escribe **el cierre de sesion**, desde la evidencia
  del `git diff`. `decisions.md`, `constraints.md`, `assumptions.md` y `lessons.md` los escribe
  **`manager`, en el momento en que las cosas pasan**. `debtec.md` admite propuestas del cierre,
  marcadas como tales.
- **Por que:** un porque **no aparece en el `git diff`**: nace en la conversacion. El cierre arranca
  en frio y no estuvo ahi, asi que solo podria inventarlo. Y al reves: el avance real si esta en el
  diff, y escribirlo durante la jornada produce lo que se penso hacer en vez de lo que se hizo.
- **Alternativas descartadas:** que el cierre lo escriba todo (inventaria los porques); que
  `manager` lo escriba todo (se pierde la garantia de que el avance sale de la evidencia).

---

### D-005 - Control de versiones con git y remoto en GitHub
| Campo | Valor |
|---|---|
| Fecha | 2026-08-31 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** el proyecto no era repositorio, y varias reglas del metodo presuponen git.
- **Decision:** repositorio git en rama `main`, con remoto en GitHub. La ruta concreta esta en
  `project.md`. `_persistence/` y `_audit/` se versionan a proposito: son la historia del proyecto.
- **Por que:** sin commits no hay nada a lo que anclar el informe de sesion, y sin remoto un commit
  vive solo en un disco. Ademas, el `git diff` es lo que convierte el registro en verificable: sin
  el, todo el sistema descansa en creerse lo que dicen los archivos.
- **Alternativas descartadas:** trabajar sin git por ahora (deja el cierre sin evidencia y el
  informe sin ancla).

---

### D-006 - `temporal/` queda fuera del repositorio
| Campo | Valor |
|---|---|
| Fecha | 2026-08-31 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** `temporal/` es el area donde el usuario deja material de trabajo, y el `git add -A`
  del cierre la habria commiteado entera.
- **Decision:** se excluye en `.gitignore`, junto con `.env` y variantes. Se declara igualmente en
  la tabla de carpetas de `project.md`, con su razon escrita.
- **Por que:** su contenido cambia o desaparece sin aviso, y los protocolos tienen prohibido leerla.
  Versionar un area que nadie puede citar mete ruido permanente en el historial. Se declara aunque
  no se versione para que el control de carpetas no la señale cada sesion como carpeta desconocida.
- **Alternativas descartadas:** no declararla (el control del Paso 2c la marcaria en cada cierre y
  se aprenderia a ignorar la alarma).

---

### D-007 - Los datos propios del proyecto viven solo en `project.md`
| Campo | Valor |
|---|---|
| Fecha | 2026-08-31 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** los protocolos necesitan nombres, rutas y el host del remoto para funcionar.
- **Decision:** todos esos datos viven **unicamente** en `project.md`. Ni las skills, ni los
  agentes, ni `CLAUDE.md` los llevan escritos dentro: los leen de ahi. El Paso 1b de `protocol-close`
  lo comprueba en cada cierre con una busqueda de texto acotada a `.claude/` y `CLAUDE.md`.
- **Por que:** un dato duplicado obliga a acordarse de dos sitios cada vez que cambia, y el dia que
  no se acuerde nadie habra dos archivos diciendo cosas distintas y habra que decidir cual miente.
  El ambito del control es estrecho a proposito: es el unico sitio donde «cero coincidencias» es la
  respuesta correcta, porque en `project.md`, `_audit/` y `_persistence/` esos datos aparecen de
  forma legitima.
- **Alternativas descartadas:** ambito del control sobre todo el arbol (devolveria decenas de
  positivos correctos cada sesion, y un control que avisa de todo termina apagado).

---

### D-008 - Modelo de trabajo de dos terminales
| Campo | Valor |
|---|---|
| Fecha | 2026-08-31 |
| Estado | **Revocada por D-012** |
| Origen | usuario |

- **Contexto:** primera definicion del reparto de trabajo, al arrancar el proyecto.
- **Decision:** dos terminales en repositorios separados — una ejecutora y una auditora—, con un
  canal de vuelta por archivos, acuse de recibo, contrato entre ambas y emparejamiento 1:1 entre
  nuestros informes y sus auditorias.
- **Por que se decidio asi:** daba la independencia mas fuerte posible. El auditor decidia por su
  cuenta cuando auditar, escribia en su propio repositorio y no podia ser silenciado por la parte
  auditada.
- **Por que dejo de valer:** ver `D-012`. El coste de mantener dos repositorios sincronizados
  —contrato, canal, acuses, marca de auditoria huerfana— resulto ser la mayor parte del sistema, y
  todo el era **maquinaria de mensajeria**: existia porque dos partes asincronas pueden perderse
  mensajes, no porque hiciera falta para auditar.

⚠️ **Esta decision esta revocada y su texto se conserva a proposito.** Describe un esquema que ya
no rige. Antes de citarla, mira `D-012`.

---

### D-009 - El informe de sesion se ancla al commit que lo contiene
| Campo | Valor |
|---|---|
| Fecha | 2026-08-31 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** cada cierre produce un informe de la jornada para que alguien lo audite.
- **Decision:** el informe se escribe en `_audit/S-XXX.md` **antes del `git add`**, de forma que
  entra en el mismo commit que describe. Despues del commit se comprueba con `git show` que entro
  de verdad; si no entro, se hace un commit nuevo, nunca un `--amend`.
- **Por que:** con el hash delante, quien audita puede contrastar cada afirmacion del informe contra
  el diff real. Sin el, recibe un relato que no puede verificar contra ningun estado. Y la
  comprobacion posterior no es ceremonia: **un paso obligatorio cuyo cumplimiento nadie mira no es
  obligatorio, es una intencion**.
- **Alternativas descartadas:** escribir el informe despues del commit (describiria un estado que ya
  no es el del commit); anotar el hash dentro del propio informe (imposible: el hash no existe
  todavia cuando se escribe).

---

### D-010 - El rol de esta sesion se llama `manager`
| Campo | Valor |
|---|---|
| Fecha | 2026-08-31 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** el rol se llamaba `executor`, heredado del esquema de dos terminales, donde el
  contraste era con la terminal que no ejecutaba.
- **Decision:** pasa a llamarse **`manager`**: dirige y coordina el proyecto, y en algunos casos
  tambien lo ejecuta.
- **Por que:** el nombre describia mal el trabajo real. Construir con las propias manos es **uno de
  los medios**, no la definicion del puesto: lo que no se delega nunca es la coordinacion y el
  registro. Y sin segunda terminal, «ejecutor» perdia ademas el contraste que le daba sentido.
- **Alternativas descartadas:** dejarlo como estaba (inofensivo, pero el nombre seguiria sugiriendo
  que el trabajo por defecto es teclear).

---

### D-011 - Solo `project.md` y el brief pueden llevar datos propios
| Campo | Valor |
|---|---|
| Fecha | 2026-08-31 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** al revisar la maquinaria aparecio que varios archivos describian **el estado de
  hoy** —«hoy `project.md` esta vacio», «hoy no existe el contrato»— aunque no llevaran ningun
  nombre ni ruta.
- **Decision:** `.claude/` y `CLAUDE.md` son agnosticos y se copian a otro proyecto tal cual. Los
  datos propios viven en `project.md`; el encargo del cliente, en `_brief/`. Las afirmaciones sobre
  el estado actual se reescriben como **condiciones** («si `project.md` no declara X…»), nunca como
  fotos del momento.
- **Por que:** no es solo reutilizacion. Una foto del presente **envejece mintiendo**: el dia que
  `project.md` se llene, esas frases seguiran ahi afirmando lo contrario, y nadie las va a releer
  para corregirlas. Una condicion no caduca.
- **Alternativas descartadas:** dejar las frases de estado y confiar en actualizarlas (nadie relee
  un archivo que funciona).

⚠️ **`_persistence/` es la excepcion inevitable, y no por descuido:** es el registro historico del
proyecto, asi que contiene sus datos por definicion. Lo agnostico de esos archivos es su estructura
—indices, convenciones, estados—, y eso si lo es.

---

### D-012 - La auditoria la hace un agente en este mismo repositorio
| Campo | Valor |
|---|---|
| Fecha | 2026-08-31 |
| Estado | Vigente |
| Origen | usuario |
| Revoca | D-008 |

- **Contexto:** con el esquema de dos terminales ya montado entero, el usuario decidio no
  trabajar con una segunda terminal y tener en su lugar un agente que audite.
- **Decision:** la auditoria la ejecuta el agente `auditor`, dentro de este repositorio, con su
  skill `protocol-audit`. Se caen el contrato, el canal de vuelta, el acuse de recibo, la marca de
  auditoria huerfana y las rutas al otro repositorio — unas 250 lineas.
- **Por que:** lo que daba valor al esquema anterior era **que quien construye no fuera su propio
  testigo**, y eso lo conserva un agente: arranca en frio, no vio la conversacion y solo puede leer
  archivos y `git`. Todo lo demas era maquinaria de mensajeria entre dos partes asincronas, y sin
  dos partes no tiene a quien servir.
- **Alternativas descartadas:** mantener las dos terminales (coste alto y trabajo manual de
  sincronizacion, para una independencia que en la practica no se estaba usando).

🚨 **El limite de este esquema esta declarado, no disimulado:** a este auditor **lo lanza el propio
auditado**. Si `manager` no lo lanza, no hay auditoria y nadie lo nota. La mitigacion es que
lanzarlo sea el ultimo paso **obligatorio** del cierre, y que el arranque reporte como desfase toda
sesion cerrada sin auditar. Ver `A-001`.

---

### D-013 - La auditoria corre despues del commit, no antes
| Campo | Valor |
|---|---|
| Fecha | 2026-08-31 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** con el auditor dentro del repositorio, la auditoria podia correr antes del commit
  —y entonces los hallazgos se corregirian en la misma sesion— o despues.
- **Decision:** corre **despues del commit y de su push**. Sus hallazgos quedan registrados en
  `_audit/` y se trabajan en la sesion siguiente. No se corrigen en caliente.
- **Por que:** el valor entero de una auditoria es que se pueda reproducir. Con el hash delante,
  cualquiera corre `git show` y contrasta cada afirmacion contra el estado real; auditar trabajo sin
  commitear obliga a juzgar algo que ya no existira cuando alguien vaya a comprobarlo. Y corregir
  sobre el commit auditado deja el informe describiendo un estado que ya cambio.
- **Alternativas descartadas:** auditar antes del commit (gana una sesion de latencia y pierde el
  anclaje, que es lo unico que hace auditable la auditoria); auditar a demanda (un control que
  depende de acordarse no se ejecuta).

---

### D-014 - Los hallazgos tienen registro propio, que sobrevive al rechazo
| Campo | Valor |
|---|---|
| Fecha | 2026-08-31 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** con dos repositorios, un hallazgo sobrevivia porque vivia en el del auditor. Sin esa
  separacion, habia que decidir donde vive.
- **Decision:** `_audit/findings.md`, con codigos `F-NNN` correlativos y globales, y cuatro estados:
  `Abierto`, `Aceptado — pendiente`, `Implementado`, `No se implementa`. Acompañado de
  `_audit/index.md` como tablero y `_audit/R-XXX.md` con cada auditoria en detalle.
- **Por que:** la propiedad que habia que preservar es una sola — **que un hallazgo no desaparezca
  porque no nos gusto**. Sin registro propio, un hallazgo rechazado no queda en ningun sitio, y el
  registro pasa a decir lo que nos conviene. `Aceptado — pendiente` existe por lo mismo: sin ese
  estado, lo aceptado y no hecho no esta implementado ni rechazado, y se cae del radar.
- **Alternativas descartadas:** que cada hallazgo naciera directamente como `T-XXX` (pierde
  exactamente los rechazados, que son los que mas importa conservar); meterlos en `_persistence/`
  (mezcla el registro del trabajo con el de su comprobacion).

---

### D-015 - Cerrar un hallazgo es de la auditoria, no de `manager`
| Campo | Valor |
|---|---|
| Fecha | 2026-08-31 |
| Estado | Vigente |
| Origen | manager |

- **Contexto:** con auditor y auditado en el mismo repositorio, ambos podian escribir en
  `findings.md`, y habia que repartir quien cambia que estado.
- **Decision:** `manager` puede mover un hallazgo a `Aceptado — pendiente` o a `No se implementa`,
  citando su `T-XXX` o su `D-XXX`. **`Implementado` solo lo escribe una auditoria posterior**, y
  solo tras verificar la correccion sobre un commit posterior.
- **Por que:** si el auditado pudiera cerrar sus propios hallazgos, `findings.md` diria lo que
  quisieramos que dijera, y el archivo perderia la unica funcion por la que existe. Que una `T-XXX`
  figure como `Implementada` **no cierra su hallazgo**: lo que lo cierra es que la correccion este
  en el codigo, y eso se mira, no se declara.
- **Alternativas descartadas:** que `manager` cierre sus hallazgos tras corregirlos (rapido, y
  convierte el registro en autocertificacion).

---

### D-016 - El agente auditor pasa a llamarse `report_auditor`
| Campo | Valor |
|---|---|
| Fecha | 2026-08-31 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** el agente de auditoria se llamaba `auditor`, y su archivo
  `.claude/agents/auditor.md`. El usuario pidio que pasara a llamarse `report_auditor`.
- **Decision:** se renombra el archivo a `.claude/agents/report_auditor.md`, el `name:` de su
  frontmatter a `report_auditor`, y **todas las referencias vivas al agente**: `CLAUDE.md`,
  `project.md`, los tres skills, los otros dos agentes, y el valor de campo `Origen: auditor`, que
  pasa a `Origen: report_auditor` en las convenciones de los seis archivos de `_persistence/`.
- **Por que:** en Claude Code el nombre por el que se invoca un agente sale del `name:` de su
  frontmatter, no del archivo. Renombrar solo el archivo habria dejado el agente respondiendo a
  `auditor` con un archivo llamado `report_auditor.md` — dos nombres para la misma cosa, y el
  desalineamiento no falla en ningun sitio: simplemente confunde a quien lo lea despues.
- **Alcance del cambio, y lo que queda fuera:** se tocan los **identificadores** del agente
  (backticked, en negrita, el `name:`, la `description:` del skill y los valores de campo). **No se
  reescribe la palabra «auditor» cuando nombra el rol** —«un auditor externo», «al auditor le
  cuesta lo mismo»—: ahi es un sustantivo comun, no un handle.
- **Lo historico no se reescribe:** las entradas ya cerradas que citan `auditor` —`A-001`, `D-012`,
  los archivos de `_audit/` y la narrativa de `progress.md`— **se dejan tal cual**. Describen lo que
  se decidio en su momento, y el pasado no se reescribe para que cuadre con el presente. Esta
  entrada es lo que enlaza un nombre con el otro.
- **Alternativas descartadas:** renombrar solo el archivo y dejar `name: auditor` (mas barato, deja
  archivo y agente con nombres distintos); renombrar tambien la palabra «auditor» en toda la prosa
  (coherencia total, a cambio de un diff enorme y de frases que dejan de leerse en espanol).

**Verificacion — cero identificadores `auditor` vivos:**

```
$ git grep -nE '`auditor`|\*\*auditor\*\*|Origen: auditor|agente auditor' -- .claude CLAUDE.md project.md ; echo "exit=$?"
exit=1
```

🕒 **Nota anadida el 2026-09-01, tras el hallazgo `F-001` de `R-002`.** El bloque de arriba
se deja **tal cual se ejecuto**: no se reescribe lo que se corrio en su dia. Lo que se corrige es su
enunciado. Su titulo decia «cero identificadores `auditor` vivos» sin acotar ambito, pero el comando
solo cubre `.claude`, `CLAUDE.md` y `project.md` — **no** los seis archivos de `_persistence/` que
esta misma decision declara dentro del alcance. Leelo como **«cero identificadores `auditor` vivos
en `.claude`, `CLAUDE.md` y `project.md`»**, que es lo unico que prueba.

El barrido con el ambito completo, ya corregidas las dos fugas de `F-002` y ya escrito el registro
de esta sesion, cuenta las coincidencias que quedan por archivo:

```
$ git grep -cE '`auditor`|\*\*auditor\*\*|Origen: auditor|agente auditor' -- . ; echo "exit=$?"
_audit/R-002.md:28
_audit/S-001.md:1
_audit/S-002.md:10
_audit/findings.md:6
_persistence/assumptions.md:1
_persistence/decisions.md:14
_persistence/lessons.md:3
_persistence/progress.md:7
_persistence/tasks.md:4
exit=0

$ git grep -nE '`auditor`|\*\*auditor\*\*|Origen: auditor|agente auditor' -- .claude CLAUDE.md project.md ; echo "exit=$?"
exit=1
```

Las coincidencias que quedan son **historico, evidencia citada y registro de esta correccion**, todo
ello fuera del alcance que el apartado «Lo historico no se reescribe» dejo a proposito: los informes
de `_audit/`, la narrativa de `progress.md`, `A-001` en `assumptions.md`, `D-012` y esta misma
entrada en `decisions.md`, `L-005` y `L-006` en `lessons.md`, `T-004` y `T-005` en `tasks.md`, y
—en `findings.md`— los bloques de evidencia de `F-001` y `F-002`, que citan literal lo que la
auditoria vio. **Ninguna es una referencia viva al agente.**

---

### D-017 - Espanol para el contenido, ingles para los nombres de archivos y carpetas
| Campo | Valor |
|---|---|
| Fecha | 2026-08-31 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** el idioma del proyecto estaba declarado en `project.md` como «Espanol», sin
  distinguir entre lo que se escribe **dentro** de un archivo y **como se llama** el archivo. En la
  practica ya se seguian dos idiomas distintos sin que la regla estuviera escrita.
- **Decision:** **espanol** para la conversacion, los reportes de los agentes y toda la
  documentacion —`project.md`, `CLAUDE.md`, `_persistence/`, `_audit/`, mensajes de commit y
  comentarios del codigo—; **ingles** para los nombres de archivos y de carpetas. Queda escrito en
  la seccion «Idioma» de `CLAUDE.md` y en la fila «Idioma de trabajo» de `project.md`.
- **Por que:** el contenido lo lee el equipo y se lee mejor en su idioma; los nombres los manejan
  herramientas, y un nombre en ingles es ASCII, sin acentos ni enes, y no se rompe al cruzar
  sistemas, remotos ni terminales.
- **La regla rige hacia adelante, y esa parte la decidio el usuario:** lo que ya existe con otro
  nombre **no se renombra por esta regla sola**, porque renombrar rompe referencias y reescribe
  historia ya auditada. El unico archivo trackeado que la incumple es `debtec.md`; se deja y queda
  registrado como deuda tecnica (`DT-001`) en vez de disimularse.
- **Alternativas descartadas:** aplicarla retroactivamente y renombrar `debtec.md` a `techdebt.md`
  (coherente de inmediato, a cambio de tocar referencias en skills, agentes y registros que la
  auditoria `R-001` ya dio por buenos); dejar la regla sin escribir y seguir por costumbre (funciona
  hasta que entra alguien que no tiene la costumbre).

---

### D-018 - Cinco principios de ingenieria y siete reglas de operacion en `CLAUDE.md`
| Campo | Valor |
|---|---|
| Fecha | 2026-08-31 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** el usuario aporto un cuerpo de principios (`PI-1` a `PI-5`) y siete reglas de
  operacion, y pidio que los agentes los siguieran.
- **Decision:** entran en `CLAUDE.md` como dos secciones propias —«Principios de ingenieria» y
  «Reglas de operacion»—, colocadas antes de las secciones del ciclo de sesion, con el texto del
  usuario adaptado a la voz del archivo y **sin anadir ni quitar principios**.
- **Por que ahi y no en `project.md`:** son metodo, no datos del proyecto. `project.md` guarda lo
  que cambia al llevar el metodo a otro repositorio; estos principios viajan con el metodo.
- **`PI-5` se escribe con dos casillas, y esa es la unica adaptacion de fondo:** el enunciado
  original —«toda tarea tiene un test que la respalda, sin excepcion»— se cumple con **un test
  automatizado en verde** cuando la tarea produce codigo ejecutable, y con **el bloque de
  verificacion** —orden ejecutada literal y salida cruda— cuando produce documentacion, protocolo o
  registro. La segunda casilla no es una rebaja: es la exigencia que este repositorio ya aplicaba.
- **Por que no literal:** el proyecto esta en `000_preproject` y no tiene ni una linea de codigo ni
  runner de tests. Escrito literal, `PI-5` habria nacido incumplido en cada sesion de esta etapa, y
  una regla que se incumple desde el primer dia deja de leerse como regla.
- **Alternativas descartadas:** escribirlo literal y sin matiz (`PI-5` inaplicable hoy); acotarlo a
  tareas de codigo dejando la documentacion **sin** definicion de terminado (deja fuera justo el
  tipo de trabajo que hace este proyecto ahora mismo).
- **Tension declarada, no resuelta en silencio:** «Separacion de roles» y «Revision independiente»
  chocan con que `manager` «en algunos casos tambien ejecuta». Se resuelve apoyandose en lo que ya
  existe —`report_auditor` revisa lo que `manager` construyo— y queda escrito en `CLAUDE.md` que,
  donde choquen, manda el principio.

---

### D-019 - Un bloque de verificacion antiguo se corrige por nota fechada, nunca reescribiendolo
| Campo | Valor |
|---|---|
| Fecha | 2026-09-01 |
| Estado | Vigente |
| Origen | report_auditor |

- **Contexto:** `F-001` (`R-002`) encontro que el bloque de verificacion de `D-016` se titulaba
  «cero identificadores `auditor` vivos» sin acotar ambito, mientras su comando cubria solo tres
  rutas. El hallazgo se acepta: el enunciado afirmaba mas de lo que el comando probaba, y ese hueco
  tapo una fuga real (`F-002`).
- **Decision:** cuando un bloque de verificacion ya escrito afirma de mas, **el comando y su salida
  se dejan intactos** y se le anade debajo una **nota fechada** que (1) acota que probo de verdad y
  (2) aporta el barrido correcto con su patron, su ambito y su salida cruda. No se edita el bloque
  original ni se sustituye su comando por otro mas ancho.
- **Por que:** `CLAUDE.md` prohibe reescribir una entrada antigua para que exhiba evidencia que en
  su dia no se ejecuto —eso convierte «falta evidencia» en «hay evidencia falsa»—. Sustituir el
  comando viejo por el nuevo produciria exactamente eso: un registro donde parece que en `S-002` se
  corrio un barrido que nadie corrio. La nota deja las dos cosas visibles: lo que se probo entonces
  y lo que se probo despues.
- **Alternativas descartadas:** editar el titulo del bloque para acotarlo (mas limpio de leer, pero
  borra que la afirmacion ancha existio, que es justo lo que `F-001` documenta); dejarlo como estaba
  y anotar solo en `findings.md` (el defecto queda vivo en el archivo que la gente lee).
- **Clasificacion:** **reversible a criterio** —anadir texto a un archivo versionado, sin efecto
  fuera del repositorio—, asi que se decide y se registra sin escalar. Todavia no existe en
  `_persistence/` un inventario de acciones irreversibles.

---

### D-020 - `manager` escribe en `tasks.md` al registrar un hallazgo de auditoria
| Campo | Valor |
|---|---|
| Fecha | 2026-09-01 |
| Estado | Vigente |
| Origen | manager |

- **Contexto:** dos reglas se cruzan. `tasks.md` dice «este archivo no se escribe a mano durante la
  jornada: lo produce el cierre de sesion». `CLAUDE.md`, en «Que hacer con una auditoria», ordena a
  `manager` registrar cada hallazgo aceptado como **`T-XXX` con `Origen: report_auditor`** y citar
  esa `T-XXX` en la fila de `_audit/findings.md`.
- **Decision:** para el **unico** caso de registrar un hallazgo de auditoria, manda `CLAUDE.md`:
  `manager` escribe la `T-XXX` en el momento de evaluar el hallazgo. Todo lo demas de `tasks.md`
  sigue siendo del `session-closer`.
- **Por que:** la fila de `findings.md` exige citar la `T-XXX`, y una fila que cita una tarea que no
  existe no es auditable. Esperar al cierre dejaria el hallazgo evaluado y sin registro durante toda
  la jornada, que es exactamente el agujero que `Aceptado — pendiente` existe para tapar.
- **Alternativas descartadas:** dejar la `T-XXX` al `session-closer` y que `manager` solo anote en
  `findings.md` (rompe la fila, que pide el codigo); registrar el hallazgo solo en `decisions.md`
  (lo saca del unico tablero donde se mira que falta por hacer).
- **Clasificacion:** **reversible a criterio** —una entrada de texto en un archivo versionado—, asi
  que se decide y se registra sin escalar. Se deja **declarada como tension abierta**: si el usuario
  prefiere lo contrario, la regla de `tasks.md` deberia decirlo con la excepcion escrita dentro.
