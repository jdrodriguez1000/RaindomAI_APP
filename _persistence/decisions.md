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
| [D-021](#d-021---debtecmd-pasa-a-llamarse-techdebtmd) | `debtec.md` pasa a llamarse `techdebt.md` | 2026-09-01 | Vigente |
| [D-022](#d-022---un-recuento-de-ambito-global-se-fecha-no-se-declara-reproducible-sobre-su-commit) | Un recuento de ambito global se fecha, no se declara reproducible sobre su commit | 2026-09-01 | Vigente |
| [D-023](#d-023---cada-etapa-declarada-tiene-su-archivo-agnostico-en-_phases) | Cada etapa declarada tiene su archivo agnostico en `_phases/` | 2026-09-01 | Vigente |
| [D-024](#d-024---la-etapa-siguiente-a-000_preproject-se-llama-005_discovery) | La etapa siguiente a `000_preproject` se llama `005_discovery` | 2026-09-01 | Vigente |
| [D-025](#d-025---tasksmd-gana-el-campo-etapa-y-las-tareas-de-alcance-pasan-a-005_discovery) | `tasks.md` gana el campo `Etapa`, y las tareas de alcance pasan a `005_discovery` | 2026-09-01 | Vigente |
| [D-026](#d-026---el-control-de-fuga-de-datos-del-paso-1b-cubre-tambien-_phases) | El control de fuga de datos del Paso 1b cubre tambien `_phases/` | 2026-09-01 | Vigente |
| [D-027](#d-027---el-texto-que-señala-un-hallazgo-aceptado-lo-corrige-manager-aunque-el-archivo-sea-de-otro) | El texto que señala un hallazgo aceptado lo corrige `manager`, aunque el archivo sea de otro | 2026-09-02 | Vigente |
| [D-028](#d-028---_methodology-entra-al-repositorio-como-carpeta-agnostica-dentro-del-control-de-fuga) | `_methodology/` entra al repositorio como carpeta agnostica, dentro del control de fuga | 2026-09-02 | Vigente |
| [D-029](#d-029---000_methodmd-es-guia-de-metodo-vigente-y-no-declara-las-etapas-del-proyecto) | `000_method.md` es guia de metodo vigente, y no declara las etapas del proyecto | 2026-09-02 | Vigente |
| [D-030](#d-030---los-codigos-de-producto-del-metodo-se-renombran-a-ft--y-sc-) | Los codigos de producto del metodo se renombran a `FT-` y `SC-` | 2026-09-02 | Vigente |
| [D-031](#d-031---un-gate-lo-declara-el-usuario-sobre-el-veredicto-tecnico-de-report_auditor) | Un Gate lo declara el usuario, sobre el veredicto tecnico de `report_auditor` | 2026-09-02 | Vigente |
| [D-032](#d-032---las-entradas-de-esta-sesion-se-fechan-2026-09-02-por-continuidad-con-el-registro) | Las entradas de esta sesion se fechan 2026-09-02, por continuidad con el registro | 2026-09-02 | Vigente |
| [D-033](#d-033---el-archivo-de-etapa-de-descubrimiento-se-adapta-de-la-guia-del-usuario-no-se-copia) | El archivo de etapa de descubrimiento se adapta de la guia del usuario, no se copia | 2026-09-02 | Vigente |
| [D-034](#d-034---n-xxx-es-el-codigo-de-necesidad-los-supuestos-y-restricciones-siguen-siendo-a-xxx-y-c-xxx) | `N-XXX` es el codigo de necesidad; los supuestos y restricciones siguen siendo `A-XXX` y `C-XXX` | 2026-09-02 | Vigente |
| [D-035](#d-035---las-plantillas-de-los-artefactos-de-descubrimiento-viven-en-_templates005_discovery) | Las plantillas de los artefactos de descubrimiento viven en `_templates/005_discovery/` | 2026-09-02 | Vigente |

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

🕒 **Segunda nota, anadida el 2026-09-01 (`S-005`), tras el hallazgo `F-006` de `R-003`.** La nota
de arriba dice que su barrido se hizo «ya escrito el registro de esta sesion». No fue asi: se tomo
**antes** de que el cierre terminara de escribirlo. Sobre `ea0b850`, el commit que la contiene, el
mismo comando da otras cifras:

```
$ git grep -cE '`auditor`|\*\*auditor\*\*|Origen: auditor|agente auditor' ea0b850 -- . ; echo "exit=$?"
ea0b850:_audit/R-002.md:28
ea0b850:_audit/S-001.md:1
ea0b850:_audit/S-002.md:10
ea0b850:_audit/S-003.md:3
ea0b850:_audit/findings.md:6
ea0b850:_persistence/assumptions.md:1
ea0b850:_persistence/decisions.md:14
ea0b850:_persistence/lessons.md:3
ea0b850:_persistence/progress.md:8
ea0b850:_persistence/tasks.md:4
exit=0
```

Dos diferencias: `progress.md` da **8** y no 7, y aparece `_audit/S-003.md:3`, el informe de cierre
de esa misma sesion. Las dos son lineas escritas **despues** del barrido, y **ninguna es una
referencia viva al agente** —el informe de cierre y la narrativa de `progress.md` son historico, y
el ambito vivo sigue en `exit=1`, como muestra el segundo comando de la nota anterior—. El fondo se
sostiene; lo que no se sostiene es la declaracion de alcance temporal.

⚠️ **Leelo asi:** el recuento de la nota anterior es el estado **al momento de escribirla**, no
sobre el commit que la contiene. Que ese defecto aparezca dentro de la correccion de `F-001` es
exactamente lo que `L-006` queria evitar.

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

🕒 **Confirmada por el usuario el 2026-09-01 (`S-004`), y la tension queda cerrada.** Preguntado
si `manager` debe escribir en `tasks.md` al registrar un hallazgo de auditoria, el usuario dijo que
si. Con eso se hace lo que esta misma entrada anunciaba: **la excepcion pasa a estar escrita dentro
de la convencion de `tasks.md`**, y tambien en los dos sitios que describen el reparto de escritura
—`protocol-close` y `session-closer.md`—, para que el cierre no la duplique. Esto responde al
hallazgo `F-007` de `R-003`, cuyo defecto no era la lectura sino la contradiccion sin registro.

---

### D-021 - `debtec.md` pasa a llamarse `techdebt.md`
| Campo | Valor |
|---|---|
| Fecha | 2026-09-01 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** `D-017` fija nombres de archivo en ingles con efecto hacia adelante, y `debtec.md`
  quedo registrado como la unica excepcion conocida (`DT-001`, `Propuesta (pendiente del usuario)`).
  El usuario pidio renombrarlo revisando todas sus referencias: la peticion **confirma la deuda y
  ordena pagarla en el mismo acto**, asi que `DT-001` pasa a `Confirmada` e `Implementada`.
- **Decision:** `git mv _persistence/debtec.md _persistence/techdebt.md`, y se reescriben las
  **referencias vivas**: los tres skills, `session-closer.md`, `CLAUDE.md`, `project.md`, la tabla
  de estructura de `progress.md` y la cabecera del propio archivo.
- **Alcance, decidido por el usuario:** **no se reescribe lo historico.** Quedan citando `debtec.md`
  los informes y auditorias de `_audit/`, las entradas ya cerradas de `decisions.md` —esta incluida—
  y la narrativa de sesiones pasadas de `progress.md`. Describen lo que era cierto cuando se
  escribieron, y reescribirlos pondria un nombre que no existia en documentos ya auditados. Mismo
  criterio que `D-016`.
- **El titulo de `DT-001` tampoco cambia:** la convencion de `techdebt.md` dice que el titulo de una
  deuda nombra el defecto y no cambia al pagarla. Sigue diciendo `debtec.md`, y debe.
- **Alternativas descartadas:** reescribir tambien `_audit/` para dejar `git grep debtec` en cero
  (barrido limpio, a cambio de informes entregados que citan un nombre inexistente al escribirlos);
  no renombrar y mantener la excepcion (es lo que `DT-001` decia, y el usuario lo revoco).
- **Clasificacion:** **reversible a criterio** —un `git mv` mas sustituciones de texto, todo
  versionado y revertible con `git revert`—, y ademas ordenado por el usuario.

**Verificacion — cero referencias `debtec` en el ambito vivo (`.claude`, `CLAUDE.md`, `project.md`):**

```
$ git grep -n "debtec" -- .claude CLAUDE.md project.md ; echo "exit=$?"
exit=1

$ ls _persistence/
assumptions.md
constraints.md
decisions.md
lessons.md
progress.md
tasks.md
techdebt.md
```

Las referencias que siguen fuera de ese ambito son las historicas que el alcance deja fuera a
proposito, mas el titulo de `DT-001` y las 13 de esta misma entrada, que nombra el archivo viejo para
poder explicar el cambio. **El recuento se tomo con el registro de esta sesion ya escrito**, que es
lo que hace que se reproduzca sobre el commit que lo contiene:

```
$ git grep -nc "debtec" -- . ; echo "exit=$?"
_audit/R-001.md:2
_audit/R-002.md:9
_audit/R-003.md:5
_audit/S-001.md:2
_audit/S-002.md:4
_audit/S-003.md:2
_audit/findings.md:4
_persistence/decisions.md:13
_persistence/progress.md:2
_persistence/techdebt.md:4
exit=0
```

🕒 **Nota anadida el 2026-09-01 (`S-005`), tras el hallazgo `F-008` de `R-004`.** El bloque de
arriba **se deja tal cual se ejecuto** (`D-019`). Lo que se corrige es su frase final: **el recuento
no se reproduce sobre el commit que contiene esta entrada.** Se tomo antes de que el cierre
terminara de escribir el registro de la sesion. Sobre `c70b757`:

```
$ git grep -nc "debtec" c70b757 -- . ; echo "exit=$?"
c70b757:_audit/R-001.md:2
c70b757:_audit/R-002.md:9
c70b757:_audit/R-003.md:5
c70b757:_audit/S-001.md:2
c70b757:_audit/S-002.md:4
c70b757:_audit/S-003.md:2
c70b757:_audit/S-004.md:17
c70b757:_audit/findings.md:4
c70b757:_persistence/decisions.md:13
c70b757:_persistence/progress.md:6
c70b757:_persistence/techdebt.md:4
exit=0
```

Tres diferencias con lo registrado arriba: `progress.md` da **6** y no 2; falta la linea entera
`_audit/S-004.md:17`, que es el informe de cierre escrito despues del barrido; y **las 13 de
`decisions.md` no son «las 13 de esta misma entrada»** — solo **9** caen dentro de `D-021`, que
empieza en la linea 573. Las otras cuatro son la fila del indice y tres citas de entradas
anteriores:

```
$ git grep -n "debtec" c70b757 -- _persistence/decisions.md | head -4
c70b757:_persistence/decisions.md:32:| [D-021](#d-021---debtecmd-pasa-a-llamarse-techdebtmd) | `debtec.md` pasa a llamarse `techdebt.md` | 2026-09-01 | Vigente |
c70b757:_persistence/decisions.md:130:  **`manager`, en el momento en que las cosas pasan**. `debtec.md` admite propuestas del cierre,
c70b757:_persistence/decisions.md:470:  historia ya auditada. El unico archivo trackeado que la incumple es `debtec.md`; se deja y queda
c70b757:_persistence/decisions.md:472:- **Alternativas descartadas:** aplicarla retroactivamente y renombrar `debtec.md` a `techdebt.md`

$ git show c70b757:_persistence/decisions.md | grep -n "^### D-021"
573:### D-021 - `debtec.md` pasa a llamarse `techdebt.md`

$ git grep -n "debtec" c70b757 -- _persistence/decisions.md | awk -F: '$3>=573' | wc -l
9
```

⚠️ **Leelo asi:** el recuento del bloque anterior es el estado **al momento de escribir esta
entrada**, no sobre su commit. **Lo que si se sostiene sin matices es el ambito vivo** —el primer
comando del bloque, `exit=1` sobre `.claude`, `CLAUDE.md` y `project.md`—, que es el criterio de
cierre real de esta decision.

🔻 **El defecto no es la cifra, es la frase.** `D-021` es la primera entrada escrita despues de
`L-006`, y no solo omitio su alcance: **afirmo explicitamente una reproducibilidad que no tenia**.
Un registro que se autodeclara reproducible y no lo es cuesta mas que uno que calla, porque
desalienta la comprobacion.

🕒 **Segunda nota, anadida el 2026-09-01 (`S-005`), tras el hallazgo `F-010` de `R-004`. Alcance
acotado.** El apartado «Alcance» de arriba clasifica **`_audit/` entero** como historico. Eso es
correcto para los informes `S-XXX.md` y las auditorias `R-XXX.md`, que son documentos entregados y
no se reescriben — pero **`_audit/findings.md` y `_audit/index.md` no son documentos entregados**:
son registros vivos, y sus secciones de convenciones se siguen aplicando en cada pasada. El criterio
se aplico por carpeta en vez de por naturaleza del texto, y dejo fuera del barrido una regla vigente
que manda comprobar una entrada en un archivo que ya no existe:

```
$ git grep -n "debtec" HEAD -- _audit/findings.md | head -1
HEAD:_audit/findings.md:56:rechazo por coste sin entrada en `debtec.md` es, por si solo, un hallazgo nuevo — y no requiere

$ git ls-tree --name-only HEAD _persistence/ | grep -i debt
_persistence/techdebt.md
```

**El alcance de esta decision se lee, desde hoy, asi:** `_audit/` es historico **salvo las secciones
de convenciones de `findings.md` y de `index.md`**, que son ambito vivo y entran en el mismo criterio
que `.claude`, `CLAUDE.md` y `project.md`.

⚠️ **La correccion de esa linea no es de `manager`.** `_audit/findings.md` lo escribe
`report_auditor`; lo unico que `manager` toca ahi es la fila de estado de cada hallazgo. Lo que esta
nota entrega es el criterio que permite corregirla; el texto lo corrige el auditor en una pasada
posterior. Queda anotado en la fila de `F-010`.

---

### D-022 - Un recuento de ambito global se fecha, no se declara reproducible sobre su commit
| Campo | Valor |
|---|---|
| Fecha | 2026-09-01 |
| Estado | Vigente |
| Origen | manager |

- **Contexto:** tres hallazgos —`F-005`, `F-006` y `F-008`— son el mismo defecto en tres entradas
  distintas, y el ultimo se escribio **despues** de `L-006`, que ya lo describia. `L-006` pedia
  declarar el ambito **de rutas**; ninguno de los tres fallo por ahi. Fallaron por el ambito
  **temporal**: un recuento tomado durante la jornada y presentado como si valiera sobre el commit
  que acabaria conteniendolo.
- **El mecanismo, que es siempre el mismo:** un barrido sobre el repositorio entero —`git grep …
  -- .`, o `| Pendiente |` en `_audit/index.md`— se corre mientras se escribe la entrada. Despues el
  cierre anade `_audit/S-XXX.md`, cierra `progress.md` y escribe `tasks.md`, y **cambia el resultado
  del propio comando que la entrada acaba de registrar**. La cifra no envejece: nace desfasada.
- **Decision, en dos reglas:**
  1. **Un bloque cuyo ambito incluye archivos que la sesion todavia va a escribir se enuncia con su
     fecha**, no con su commit: «al momento de escribir esta entrada», nunca «se reproduce sobre el
     commit que la contiene».
  2. **Si lo que se quiere es reproducibilidad, se acota el ambito a lo que la sesion no escribe** y
     se dice cual es. El ambito vivo —`.claude`, `CLAUDE.md`, `project.md`— cumple eso, y por eso el
     primer comando de `D-021` si se reproduce; el global nunca lo hara.
- **Por que importa mas que la cifra:** una entrada que **se autodeclara reproducible y no lo es**
  cuesta mas que una que calla. La que calla invita a comprobar; la que lo afirma desalienta la
  comprobacion, y el error sobrevive hasta que alguien la corre igualmente. `F-008` es exactamente
  ese caso.
- **Caso especial, y es el que hace falta escribir:** `git grep -n "| Pendiente |" -- _audit/index.md`
  **no puede devolver `exit=1` en ningun commit de cierre**, porque el `session-closer` anade la fila
  de su sesion con `Pendiente` antes de commitear. Un control asi no mide lo que dice medir: mide si
  el commit es un cierre. Por eso la señal 2 de `A-001` se rehace con su momento de comprobacion —al
  abrirse la sesion siguiente— en la nota que entrega `T-009`.
- **Alternativas descartadas:** prohibir los recuentos globales en los bloques de verificacion
  (elimina el defecto y tambien la unica evidencia de ambito completo que `F-001` pedia); tomar
  siempre el recuento contra el commit anterior (se reproduce, pero mide un estado que no es el que
  la entrada describe); dejarlo en `L-006` y confiar en que se aplique (ya se probo: `D-021` es la
  entrada inmediatamente posterior y reincidio).
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — es una
  regla de redaccion sobre archivos de registro, sin efecto fuera del repositorio y revertible con
  `git revert`.
- **Lo que esta decision NO hace todavia:** llevar la regla a `CLAUDE.md` o a `protocol-close`, que
  es donde `L-007` diria que tiene que estar para que la aplique quien no leyo esta entrada. Queda
  pendiente de decidir con el usuario, y anotado aqui para que no se pierda.

**Verificacion — las dos formas, sobre `HEAD` (`e61454b`):**

```
$ git grep -n "debtec" HEAD -- .claude CLAUDE.md project.md ; echo "exit=$?"
exit=1

$ git grep -c "debtec" HEAD -- . | wc -l
12
```

El primero esta acotado a lo que la sesion no reescribe, y **se reproducira sobre el commit de este
cierre**. El segundo incluye `_persistence/` y `_audit/`, que esta sesion esta escribiendo ahora
mismo: vale **al momento de escribir esta entrada** y sera otro numero en el commit — que es
justamente lo que esta decision obliga a decir en vez de callar.

---

### D-023 - Cada etapa declarada tiene su archivo agnostico en `_phases/`
| Campo | Valor |
|---|---|
| Fecha | 2026-09-01 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** el usuario aporto `temporal/005_discovery.md`, un archivo de **otro metodo** que
  describe una etapa de Descubrimiento, y pidio escribir con esa guia el archivo equivalente para la
  etapa que este proyecto tiene en curso, `000_preproject`, en una carpeta `_phases/`.
- **Decision:** nace `_phases/`, con **un archivo por etapa declarada**, y el primero es
  `_phases/000_preproject.md`. Cada archivo dice **que autoriza la etapa, que prohibe, sus entradas,
  su procedimiento, sus artefactos, su condicion de salida, que registra y que entrega a la
  siguiente**. La carpeta queda declarada en la tabla «Carpetas propias» de `project.md`.
- 🚨 **Los archivos de `_phases/` son agnosticos**, y esa es la parte que mas condiciona como se
  escriben: el usuario los quiere reutilizables como guia en cualquier proyecto. No llevan dentro
  ningun nombre, ruta ni codigo instanciado; los codigos aparecen en forma generica —`T-XXX`,
  `D-XXX`, `A-XXX`, `F-NNN`—, y donde hace falta un dato del proyecto se referencia `project.md`.
  Es el mismo criterio que ya rige para `.claude/` y `CLAUDE.md`.
- 🚨 **`000_preproject` NO define el alcance ni el objetivo del proyecto**, y asi queda escrito en su
  tabla de prohibiciones. La etapa monta el andamio; decidir el producto es de la etapa siguiente. Se
  sale de `000_preproject` cuando el andamio se sostiene, no cuando se sabe que se va a construir.
- **Lo que la etapa entrega, fijado por el usuario, son cinco cosas:** la estructura minima de
  carpetas y archivos; la forma de trabajo entre los tres agentes; la memoria del proyecto en
  `_persistence/`; la gestion de las auditorias; y los datos propios del proyecto en `project.md`.
  **La condicion de salida es el espejo de esas cinco**, mas la exigencia de que no quede ningun
  `F-NNN` sin evaluar — lo unico que la etapa puede pedirle a la auditoria sin invadirla.
- **Vocabulario:** **«etapa» y «fase» son la misma cosa en esta metodologia**, y se usan
  indistintamente. Lo zanjo el usuario. La carpeta se llama `_phases/` en ingles por `D-017` y
  `C-005`, que separan el idioma del nombre del idioma del contenido.
- **Por que una carpeta propia y no `project.md` ni `CLAUDE.md`:** `project.md` guarda **datos** —que
  es cada cosa y donde esta— y dice explicitamente que el porque no va ahi; `CLAUDE.md` es el metodo
  entero y ya tiene que poder copiarse tal cual. Lo que una etapa autoriza y prohibe no es ninguna de
  las dos cosas: cambia de etapa en etapa, y con una etapa por archivo se lee solo la que esta en
  curso.
- **La guia se tomo como forma, no como contenido.** No se importaron de `005_discovery.md`: sus
  rutas (`methodology/`, `_memory/`, `_discovery/`, `templates/`, `tech-debt.md`), que aqui no
  existen; su reparto entre «terminal ejecutora» y «terminal auditora», que `D-012` revoco; ni sus
  codigos `N-xxx`, `RES-xxx` y `SUP-xxx`, que chocarian con `C-XXX` y `A-XXX` en la tabla «Codigos»
  de `project.md`. Tampoco se adopto su contenido de Descubrimiento —las nueve preguntas, la
  taxonomia de actores, la hipotesis con condicion de falsacion—: describe una etapa que este
  proyecto **no ha declarado**, y darla por adoptada seria convertir una propuesta en decision sin
  `D-XXX`. Ese material es el candidato natural para un `_phases/` de la etapa de descubrimiento el
  dia que se declare.
- **Alternativas descartadas:** meter la descripcion de la etapa dentro de `project.md` (un archivo
  menos, a cambio de mezclar datos estables con procedimiento y de hacer crecer sin limite el archivo
  que todo lo demas lee); escribirlo con los datos de este proyecto y generalizarlo despues (es como
  nacio `.claude/`, y costo un barrido y un control permanente —el Paso 1b— desenredarlo); copiar
  `005_discovery.md` tal cual y adaptarlo (arranca con vocabulario paralelo y carpetas inexistentes,
  y el arreglo cuesta mas que escribirlo desde la evidencia).
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — es crear
  un archivo y una fila en una tabla, sin efecto fuera del repositorio y revertible con `git revert`.

**Verificacion — el archivo no lleva datos del proyecto ni codigos instanciados:**

```
$ grep -nE "RaindomAI|RaidomAI|Proyectos_TripleS|github\.com" _phases/ -r ; echo "exit=$?"
exit=1

$ grep -nE "[A-Z]{1,2}-[0-9]+" _phases/000_preproject.md ; echo "exit=$?"
exit=1
```

El primer patron es el mismo que el Paso 1b de `protocol-close` aplica a `.claude`, `CLAUDE.md` y
`project.md`. El segundo caza cualquier codigo instanciado (`T-001`, `D-015`, `A-003`…) y no devuelve
ninguno: todos los del archivo estan en forma generica.

⚠️ **`_phases/` todavia no entra en el ambito del Paso 1b**, que hoy cubre solo `.claude`,
`CLAUDE.md` y `project.md`. Mientras no entre, la agnosticidad de estos archivos **depende de que
alguien se acuerde**, que es justo lo que `L-008` describe. Ampliar el ambito del control es una
modificacion del protocolo y queda pendiente de acordarla con el usuario.

🕒 **Nota anadida el 2026-09-02 (`S-006`), tras el hallazgo `F-013` de `R-005`.** El parrafo de
arriba **se deja tal cual se escribio** (`D-019`), pero **ya no describe el estado del control**:
`D-026`, en este mismo commit, amplio el ambito del Paso 1b a `_phases/`. Lo que quedaba «pendiente
de acordarla con el usuario» se acordo y se aplico antes de cerrar la sesion.

```
$ git grep -n "CLAUDE.md _phases" 510d580 -- .claude
510d580:.claude/skills/protocol-audit/SKILL.md:140:git grep -nE "<nombre del proyecto>|<carpeta raiz de las rutas absolutas>|<host del remoto>" <hash> -- .claude CLAUDE.md _phases
510d580:.claude/skills/protocol-close/SKILL.md:96:git grep -nE "<nombre del proyecto>|<carpeta raiz de las rutas absolutas>|<host del remoto>" -- .claude CLAUDE.md _phases
```

⚠️ **Y la descripcion del ambito anterior tambien estaba mal.** El parrafo dice que el Paso 1b
«cubre solo `.claude`, `CLAUDE.md` y `project.md`». Sobre `c70b757` —el commit inmediatamente
anterior, con el ambito todavia sin ampliar— cubria dos, no tres:

```
$ git grep -n 'host del remoto>" -- ' c70b757 -- .claude ; echo "exit=$?"
c70b757:.claude/skills/protocol-close/SKILL.md:96:git grep -nE "<nombre del proyecto>|<carpeta raiz de las rutas absolutas>|<host del remoto>" -- .claude CLAUDE.md
exit=0
```

`project.md` nunca estuvo en el ambito, y no es un olvido: es **el archivo donde los datos propios si
deben estar**, asi que incluirlo en un control de fuga lo haria devolver una linea correcta en cada
pasada. El ambito vigente lo fija `D-026` y hay que leerlo ahi, no aqui.

⚠️ **Consecuencia abierta, y no se resuelve aqui:** hay tareas registradas en `_persistence/tasks.md`
que definen alcance y objetivo del proyecto y declaran las etapas posteriores, nacidas dentro de
`000_preproject`. Con esta decision, ese trabajo **no es de esta etapa**. Que se haga con ellas
—moverlas a la etapa siguiente, o dejarlas donde estan como excepcion registrada— es del usuario y
queda anotado aqui para que no se pierda.

---

### D-024 - La etapa siguiente a `000_preproject` se llama `005_discovery`
| Campo | Valor |
|---|---|
| Fecha | 2026-09-01 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** `D-023` dejo escrito que `000_preproject` **no define alcance ni objetivo** del
  proyecto. Eso dejo sin etapa a las dos tareas que hacen justamente eso, que habian nacido dentro de
  `000_preproject` porque no habia otra declarada. Una tarea sin etapa a la que pertenecer no aparece
  en ninguna condicion de salida: ni bloquea la etapa actual ni pertenece a la siguiente.
- **Decision:** la etapa siguiente se llama **`005_discovery`**, y es la que define alcance y
  objetivo. Entra en la tabla «Etapas» de `project.md`, que pasa a declarar dos.
- **Por que solo la inmediata y no la secuencia entera:** porque lo unico que hacia falta resolver
  era **donde van las tareas de alcance**. Declarar de golpe toda la secuencia seria adoptar la
  propuesta del brief sin haberla evaluado — exactamente lo que `project.md` advierte que no se haga.
- 🚨 **Esto NO cierra la tarea de declarar las etapas posteriores.** Su criterio escrito —«la tabla
  «Etapas» lista mas de una etapa»— ya se cumple literalmente por efecto de esta decision, y aun asi
  la tarea sigue abierta: lo que la cierra es la **secuencia completa**, decidida y registrada. Queda
  anotado en la propia tarea y en `project.md` para que nadie la de por hecha leyendo la tabla.
- **Alternativas descartadas:** declarar la secuencia completa del brief (§22) en esta misma pasada
  (resuelve el problema y de paso adopta siete etapas que nadie ha evaluado); dejar las dos tareas en
  `000_preproject` como excepcion registrada (contradice `D-023` el mismo dia en que se escribio, y
  una etapa cuya prohibicion principal tiene excepcion no prohibe nada); crear la etapa con un
  identificador provisional (acaba citado en sitios que despues hay que renombrar).
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — es una
  fila en una tabla y un identificador que todavia no tiene archivos ni historia detras.

**Verificacion — la tabla «Etapas» de `project.md` declara dos:**

```
$ sed -n '/^| Etapas declaradas/,/^| Etapas posteriores/p' project.md
| Etapas declaradas | `000_preproject`, `005_discovery` |
| Etapas posteriores a `005_discovery` | **no registradas** |
```

⚠️ **`005_discovery` esta declarada pero todavia no tiene su archivo en `_phases/`.** `D-023` dice
que cada etapa declarada tiene el suyo, asi que hoy hay una etapa declarada sin describir. Se deja
constancia: es trabajo de la propia etapa, no de esta decision.

---

### D-025 - `tasks.md` gana el campo `Etapa`, y las tareas de alcance pasan a `005_discovery`
| Campo | Valor |
|---|---|
| Fecha | 2026-09-01 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** el usuario ordeno mover a `005_discovery` las dos tareas que definen alcance y
  declaran las etapas posteriores. `tasks.md` **no tenia ningun campo donde expresar eso**: sus
  campos eran `Estado`, `Importancia`, `Urgencia`, `Origen` y `Sesion`. `Sesion` dice **cuando** se
  registro la tarea, no **a que etapa pertenece**, y las dos cosas dejan de coincidir en cuanto una
  tarea sobrevive a su etapa.
- **Decision, en tres partes:**
  1. **`tasks.md` gana el campo `Etapa`**, obligatorio, con valor de la tabla «Etapas» de
     `project.md`. Va en la ficha, en la plantilla **y como columna del indice**.
  2. **Las dos tareas de alcance pasan a `005_discovery`**; las once restantes quedan en
     `000_preproject`. Cada una lleva su nota fechada; **ningun texto anterior se reescribe**.
  3. **La excepcion de escritura de `manager` sobre `tasks.md` se generaliza**, y queda escrita
     dentro de la convencion del archivo: ademas de la `T-XXX` que nace de un hallazgo aceptado,
     `manager` escribe aqui cuando el cambio **nace de una decision registrada que el
     `session-closer` no puede deducir del `git diff`**.
- **Por que el campo va tambien en el indice:** la condicion de salida de una etapa pregunta «que
  queda abierto **de esta etapa**». Con `Etapa` solo en la ficha, responder eso obliga a abrir las
  trece; con la columna, se lee de un vistazo. Un campo que hay que ir a buscar acaba sin llenarse.
- **Por que se generaliza la excepcion en vez de anadir una segunda a medida:** `L-007` ya costo un
  hallazgo —una excepcion escrita solo donde se decidio y no donde esta la regla—. Dos excepciones
  puntuales invitan a una tercera; el criterio de fondo es uno solo y se puede enunciar: **el cierre
  escribe lo que el diff demuestra, `manager` escribe lo que el diff no puede saber**.
- 🚨 **La excepcion exige su cita.** Toda edicion a mano tiene que apoyarse en un `D-XXX` o un
  `F-NNN` citado en la propia tarea. Sin esa cita no se distingue de saltarse la regla, y una regla
  que no se puede distinguir de su incumplimiento ya no rige.
- **Alternativas descartadas:** no anadir campo y expresar el traslado solo en el cuerpo de la tarea
  (mas barato, pero deja la pertenencia a una etapa fuera de todo control mecanico); usar el estado
  `Suspendida` para las dos (miente: no estan suspendidas, estan asignadas a otra etapa); dejar el
  campo solo en la ficha y no en el indice (menos diff hoy, peor lectura cada vez que se pregunte que
  falta de la etapa).
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — son
  campos de un archivo de registro, versionados y revertibles con `git revert`.

**Verificacion — el campo existe en las trece fichas, y las dos tareas estan en la etapa nueva:**

```
$ grep -oE "^\| Etapa \| .[0-9_a-z]+" _persistence/tasks.md | sort | uniq -c
     11 | Etapa | `000_preproject
      2 | Etapa | `005_discovery
      1 | Etapa | una

$ grep -n "005_discovery" _persistence/tasks.md | head -2
12:| [T-001](#t-001---definir-alcance-y-objetivo-del-proyecto) | Definir alcance y objetivo del proyecto | No implementada | Alta | Bloqueante | `005_discovery` |
13:| [T-002](#t-002---declarar-las-etapas-posteriores-a-000_preproject) | Declarar las etapas posteriores a `000_preproject` | No implementada | Media | No bloqueante | `005_discovery` |
```

11 + 2 = 13, que son todas las tareas registradas. La tercera linea —`| Etapa | una`— es la fila de
la tabla de convenciones, no una ficha; la de la plantilla no la cuenta este patron porque su valor
esta vacio.

---

### D-026 - El control de fuga de datos del Paso 1b cubre tambien `_phases/`
| Campo | Valor |
|---|---|
| Fecha | 2026-09-01 |
| Estado | Vigente |
| Origen | manager |

- **Contexto:** `D-023` exige que los archivos de `_phases/` sean agnosticos, reutilizables como guia
  en cualquier proyecto. El Paso 1b de `protocol-close` —el unico control que comprueba eso— se
  acotaba a `.claude/` y `CLAUDE.md`. La exigencia existia sin nada que la comprobara.
- **Decision:** el ambito del control pasa a `.claude CLAUDE.md _phases`, en `protocol-close`
  (Paso 1b) y en `protocol-audit` (control mecanico c). La prosa que declara el ambito se actualiza
  en la misma pasada, y `CLAUDE.md` y `project.md` pasan a nombrar `_phases/` entre lo que tiene que
  poder copiarse tal cual.
- **Por que ahora y no «cuando haga falta»:** `L-008` se escribio hoy mismo por esto — una regla que
  solo vive escrita, sin mecanismo que la aplique, depende de que alguien se acuerde, y ya se probo
  que eso no basta. El coste de ampliar el ambito es una palabra en un `git grep`.
- **Por que `_phases/` si y `_persistence/` no:** el control vale porque **cero es la respuesta
  correcta** en su ambito. `_persistence/` y `_audit/` estan llenos de nombres y rutas del proyecto
  de forma legitima; incluirlos convertiria el control en decenas de lineas correctas cada sesion, y
  un control que avisa de todo termina apagado. `_phases/` cumple el criterio: describe el metodo, no
  el proyecto.
- **Alternativas descartadas:** dejarlo en la exigencia escrita de `D-023` y confiar en la disciplina
  (es literalmente el patron que `L-008` describe); crear un control aparte solo para `_phases/` (dos
  controles que hacen lo mismo se desincronizan — `L-003`); ampliar el ambito al arbol entero (el
  control deja de distinguir fugas de menciones legitimas).
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — es un
  pathspec en dos skills y la prosa que lo declara.

**Verificacion — el control, con el ambito nuevo, sigue en cero:**

```
$ git grep -nE "RaindomAI|RaidomAI|Proyectos_TripleS|github\.com" -- .claude CLAUDE.md _phases ; echo "exit=$?"
exit=1
```

El patron instancia los tres valores que el Paso 1b toma de `project.md`: nombre del proyecto —en sus
dos grafias, la del remoto y la de la carpeta en disco—, carpeta raiz de las rutas absolutas y host
del remoto.

---

### D-027 - El texto que señala un hallazgo aceptado lo corrige `manager`, aunque el archivo sea de otro
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | report_auditor |

- **Contexto:** `R-005` dejo `F-010` en un punto muerto de autoria y pidio zanjarlo. El defecto vive
  en una **convencion vigente** de `_audit/findings.md`, archivo del auditor; pero el auditor tiene
  prohibido corregir —«ni una linea, ni aunque sea obvio»— y `manager` tiene prohibido escribir ahi
  mas alla de la fila de estado de cada hallazgo. Resultado: un defecto reconocido por las dos partes
  que **ninguna de las dos puede tocar**. `F-014` planteaba lo mismo en la otra direccion —texto de
  `progress.md`, archivo del `session-closer`—.
- **Decision:** cuando un hallazgo aceptado señala **un texto concreto**, ese texto lo corrige
  `manager`, aunque el archivo pertenezca a otro agente, citando el `F-NNN` en su `T-XXX`. La
  correccion no toca nada mas que lo señalado.
- **Limites, y son la mitad de la decision:**

| ✅ Si se puede corregir | ❌ No se puede corregir |
|---|---|
| convenciones, indices y tablas de estado — **registro vivo** | `_audit/R-XXX.md` y `_audit/S-XXX.md` — **documentos entregados**, se corrigen por hallazgo nuevo |
| las secciones de `progress.md` que el cierre sobrescribe en cada pasada | la bitacora de `progress.md` y los bloques de verificacion antiguos — son historico, y ahi manda `D-019`: nota fechada, nunca reescritura |

- **Por que `manager` y no ampliar el mandato del auditor:** el auditor vale por lo que **no** hace.
  Un auditor que corrige sobre el commit que audita deja de ser independiente en la pasada siguiente,
  porque estaria verificando su propia correccion — exactamente lo que la separacion de roles existe
  para impedir. `manager` corrige y el auditor lo verifica despues: los dos papeles siguen separados.
- **Por que no rompe «quien construye no evalua»:** `manager` no cambia el **estado** del hallazgo.
  Sigue escribiendo `Aceptado — pendiente`, y `Implementado` lo escribe la auditoria siguiente. Lo
  que esta decision reparte es **quien mueve el texto**, no quien declara que quedo bien.
- **Alternativas descartadas:** ampliar el mandato del auditor a las convenciones de `findings.md`
  (le da una mano para escribir en el archivo donde lleva la cuenta de sus propios hallazgos, y
  convierte la pasada siguiente en autoevaluacion); declarar que esa seccion es de `manager` y punto
  (resuelve `F-010` y deja `F-014` —y el caso simetrico en cualquier otro archivo— igual de
  atascados); dejarlo sin zanjar (es lo que `R-005` señalo: mientras no se decida, **`F-010` no lo
  puede cerrar nadie**).
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — es un
  reparto de escritura entre roles dentro del repositorio, sin efecto fuera de el y revertible con
  `git revert`.

**Verificacion — el defecto que `F-010` señala sigue vivo antes de aplicar esta decision:**

```
$ git grep -n "debtec" a800d6b -- _audit/findings.md
a800d6b:_audit/findings.md:56:rechazo por coste sin entrada en `debtec.md` es, por si solo, un hallazgo nuevo — y no requiere
```

Una sola linea, dentro de la seccion «Convenciones» —registro vivo, no cita historica—, que manda
comprobar una entrada en un archivo que `D-021` renombro y que ya no existe.

---

### D-028 - `_methodology/` entra al repositorio como carpeta agnostica, dentro del control de fuga
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** el usuario aporto una carpeta `_methodology/` con `000_method.md` —el metodo de
  desarrollo consolidado— y `sources/` con las tres fuentes de las que se consolido. Llego sin
  trackear, y el arranque de la sesion la señalo como carpeta sin declarar.
- **Decision:** entra al repositorio y se declara en la tabla «Carpetas propias» de `project.md`.
  `000_method.md` es el documento canonico; `sources/` se conserva **intacta** como registro de como
  se diseño el metodo, y no se edita — lo dice el propio encabezado del documento.
- **Y entra tambien en el ambito del Paso 1b**, junto a `.claude`, `CLAUDE.md` y `_phases`: en
  `protocol-close` y en `protocol-audit`, con la prosa de los dos actualizada en la misma pasada.
- **Por que en el ambito del control:** cumple el criterio que fijo `D-026` —**cero es la respuesta
  correcta**—. `_methodology/` describe el metodo, no el proyecto: no hay ninguna razon legitima para
  que aparezca ahi un nombre, una ruta o un host de este proyecto, asi que el control no genera ruido.
  Y la exigencia de agnosticidad sin mecanismo que la compruebe es exactamente lo que `L-008`
  describe.
- **Por que no dentro de `_phases/`:** son cosas distintas. `_phases/` dice **que se hace en una
  etapa** —que autoriza, que prohibe, cuando se sale—; `_methodology/` dice **con que criterio se
  construye el producto** y que etapas existen en el metodo. Un archivo de etapa se escribe cuando la
  etapa se declara; la guia existe antes que cualquiera de ellas.
- **Alternativas descartadas:** dejarla fuera del repositorio, en el area de trabajo del usuario
  (desaparece del registro y ningun control la ve — y es la guia que orienta el proyecto entero);
  anadirla a `.gitignore` (mismo efecto, ademas de dejar el arbol y `project.md` cuadrando por
  omision); meter el contenido dentro de `CLAUDE.md` (mezcla el metodo de desarrollo del producto con
  las reglas de operacion de la sesion, y hace crecer sin limite el archivo que todo lo demas lee);
  declararla sin meterla en el control (crea la exigencia de agnosticidad y ningun comando que la
  compruebe).
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — es
  anadir archivos ya existentes al control de versiones, una fila en una tabla y un pathspec en dos
  skills; revertible con `git revert` y sin efecto fuera del repositorio.

**Verificacion — el control, con el ambito nuevo, sigue en cero:**

```
$ grep -rnE "RaindomAI|RaidomAI|Proyectos_TripleS|github\.com" .claude CLAUDE.md _phases _methodology ; echo "exit=$?"
exit=1
```

El patron instancia los tres valores que el Paso 1b toma de `project.md`, con el nombre del proyecto
en sus dos grafias. Se corre sobre el arbol de trabajo y no sobre un commit **a proposito**:
`_methodology/` todavia no esta en ningun commit, asi que un `git grep` sobre un hash no la veria.

---

### D-029 - `000_method.md` es guia de metodo vigente, y no declara las etapas del proyecto
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** `000_method.md` describe un ciclo completo —descubrimiento, prototipo, gate, baseline,
  esqueleto, crecimiento, MVP, gate, evolucion—. `project.md` declara dos etapas y dice que lo
  posterior **no esta decidido**. Si el documento entra tal cual, el proyecto pasa a tener dos
  respuestas distintas a «que etapas tiene».
- **Decision:** `000_method.md` es la **guia de metodo vigente** —orienta como se trabaja el proyecto—
  y **no declara ninguna etapa**. Las declaradas siguen siendo las de la tabla «Etapas» de
  `project.md`, y hoy son dos. Adoptar cualquier otra exige su `D-XXX` y su archivo en `_phases/`.
  El usuario lo fijo asi expresamente: **por ahora no se detalla ninguna otra fase**; eso se hara mas
  adelante.
- **Como queda escrito, y en tres sitios porque es donde se puede confundir:** un bloque «Alcance de
  este documento» al principio de `000_method.md`; una nota en la seccion «Etapas» de `project.md`; y
  una fila nueva en la tabla de prohibiciones de `_phases/000_preproject.md` —dar por adoptado el
  ciclo de una guia—. Es `L-007` aplicada: la regla se escribe donde se aplica, no solo donde se
  decidio.
- **Y el documento gana una seccion que las fuentes no tenian:** el ciclo del metodo empieza en una
  **necesidad**, asi que la etapa de montar el andamio **no cabe en el**. Queda escrito que esa etapa
  previa existe, que es deliberado que no lleve numero del flujo del producto, y que su contenido vive
  en su archivo de etapa. Sin eso, quien lea la guia concluye que el proyecto va con retraso respecto
  a un diagrama al que nunca pertenecio.
- **Alternativas descartadas:** adoptar el ciclo completo y declarar todas las etapas en `project.md`
  (contradice la instruccion del usuario, y declararia como decidido lo que nadie ha decidido — la
  prohibicion que `_phases/000_preproject.md` ya tenia escrita); dejar el documento sin ese bloque y
  confiar en que nadie confunda guia con acta (`L-008`: una exigencia sin nada que la ponga delante
  depende de que alguien se acuerde); no incorporar el documento hasta que se declaren las etapas
  (deja fuera del registro justo el material que orienta la decision de declararlas).
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — es texto
  de encuadre en tres archivos del repositorio, revertible con `git revert`.

**Verificacion — la tabla de etapas no cambio, y sigue diciendo lo mismo que antes:**

```
$ sed -n '/^| Etapas declaradas/,/^| Etapas posteriores/p' project.md
| Etapas declaradas | `000_preproject`, `005_discovery` |
| Etapas posteriores a `005_discovery` | **no registradas** |

$ ls _phases/
000_preproject.md
```

Un solo archivo de etapa, y la tabla igual que antes de incorporar la guia: **la guia entro y no
declaro nada**, que es exactamente lo que esta decision fija.

---

### D-030 - Los codigos de producto del metodo se renombran a `FT-` y `SC-`
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | manager |

- **Contexto:** la seccion de identificadores de `000_method.md` declaraba `F-` para feature y `S-`
  para scenario. La tabla «Codigos» de `project.md` ya usa `F-NNN` para hallazgo de auditoria y
  `S-XXX` para sesion de trabajo. Dos prefijos, cuatro significados.
- **Decision:** en el metodo, feature pasa a `FT-` y scenario a `SC-`. Los del registro no se tocan.
  `N-`, `VS-`, `TC-` y `ADR-` no colisionan y quedan igual. `T-` se comparte **a proposito**: en el
  metodo es la tarea y en el registro tambien — es el mismo concepto, y darle dos nombres segun el
  archivo seria peor que compartirlo.
- **Por que se cambia el del metodo y no el del registro:** el registro **ya tiene historia
  escrita**. Renombrar `F-NNN` o `S-XXX` obligaria a reescribir los informes de sesion, las
  auditorias, el tablero y el registro de hallazgos — documentos entregados y ya auditados, que
  `D-021` clasifica como historico y que `D-019` prohibe reescribir. El metodo, en cambio, todavia no
  ha instanciado ni un solo codigo: cambiarlo cuesta una tabla.
- **Por que ahora y no cuando se escriba el primer codigo de producto:** porque el choque se ve hoy y
  no se vera despues. Cuando aparezca el primer `F-001` de feature, ya habra un `F-011` de hallazgo
  al lado y la ambiguedad estara escrita en dos sitios. Ademas queda en el documento **la regla
  general** —contrastar la tabla del metodo contra la del proyecto antes de escribir el primer
  identificador—, para el choque que aparezca con otro prefijo. Es `L-002` otra vez: un metodo traido
  de otro proyecto llega con sus codigos, y esos no viajan.
- **Alternativas descartadas:** renombrar los de auditoria (reescribe registro ya auditado — lo
  descarto el usuario); aplazar la decision con una advertencia en el documento y una entrada de
  deuda tecnica (el aplazamiento no ahorra nada: el trabajo es el mismo hoy que dentro de tres meses,
  y entre medias el documento dice algo que el registro desmiente); usar `FEAT-` y `SCEN-` (mas
  legibles sueltos, mas ruidosos dentro de una cadena de trazabilidad que se lee entera de un
  vistazo).
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — es una
  tabla de prefijos en un documento agnostico que todavia no ha instanciado ninguno.

**Verificacion — no queda ningun `F-` ni `S-` como codigo de producto en el documento:**

```
$ grep -nE '`F-0|`S-0' _methodology/000_method.md ; echo "exit=$?"
exit=1
```

⚠️ **Ese patron solo cubre `000_method.md`, y solo la forma entrecomillada.** Las fuentes de
`sources/` **conservan `F-` y `S-`**, y es deliberado: no se editan, por decision del propio
documento, y el Anexo A registra el cambio como decision de consolidacion. Ahi los identificadores
van dentro de un bloque de codigo y **sin comillas**, asi que el patron de arriba no los ve — hace
falta otro para verlos:

```
$ grep -rnE 'F-[0-9]{3}|S-[0-9]{3}' _methodology/sources/
_methodology/sources/005_vertical.md:461:F-001   Feature
_methodology/sources/005_vertical.md:462:S-001   Scenario
_methodology/sources/005_vertical.md:470:F-001
_methodology/sources/005_vertical.md:472:S-001
```

🔑 **Los dos patrones juntos dicen lo que uno solo no diria:** el documento canonico esta limpio
y las fuentes estan intactas. Con el primero a secas, alguien podria leer el `exit=1` como prueba de
que ya no queda `F-` en ningun sitio de `_methodology/`, y no es cierto.

---

### D-031 - Un Gate lo declara el usuario, sobre el veredicto tecnico de `report_auditor`
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** la seccion «Quien declara el Gate» de `000_method.md` era una adicion de
  consolidacion —ninguna de las tres fuentes asigna dueño al veredicto— y lo resolvia diciendo que
  lo declara **la terminal auditora**, conectandolo con un esquema de dos terminales que `D-012`
  revoco en este proyecto. Aqui no hay terminales: hay un agente `report_auditor` que tiene escrito
  que **no construye, no corrige y no decide**. Declarar un Gate es decidir.
- **Decision:** hacen falta **dos firmas, y ninguna sustituye a la otra**. `report_auditor` contrasta
  la evidencia registrada contra los criterios del Gate y emite el **veredicto tecnico**; el
  **usuario**, como stakeholder, **declara el Gate**; `manager` registra el resultado con su `D-XXX`,
  se apruebe o no. Es literalmente la «Doble validacion» de `CLAUDE.md`, aplicada al punto donde mas
  dinero se compromete.
- **Por que el auditor no decide, aunque sea quien mejor conoce la evidencia:** auditar y decidir son
  papeles incompatibles. Quien decide asume la consecuencia de la inversion; un auditor que ademas
  decide **no puede señalar el error de esa decision en la pasada siguiente**, porque estaria
  revisando la suya. Es el mismo argumento por el que `manager` no cierra sus propios hallazgos
  (`D-015`) y por el que la correccion la hace `manager` y no el auditor (`D-027`).
- **Como quedo escrito, y es mas de lo que se pregunto:** la seccion pasa a regir **los dos Gates**,
  no solo el primero — el segundo tampoco tenia dueño—; se enuncia en vocabulario agnostico —«quien
  audita», «quien patrocina», «quien coordina»— para que el documento siga siendo copiable a un
  proyecto que reparta los papeles de otra forma; y se conserva escrito el **limite honesto** del
  esquema: si a la revision independiente la convoca el propio evaluado, no lanzarla no lo nota nadie.
  Ese limite ya esta registrado en este proyecto como `A-001`, y el documento no debe fingir que no
  existe.
- **Alternativas descartadas:** mantener el sentido literal del metodo y dejar que el auditor declare
  el Gate (obliga a ampliar su mandato en `project.md`, `CLAUDE.md` y `protocol-audit`, y rompe la
  separacion de roles sobre la que se monto el esquema entero); dejar la seccion como principio
  negativo —«no lo declara quien construyo»— sin asignar dueño (es lo que hacian las fuentes, y es
  justo el vacio que la adicion existia para tapar: un Gate sin dueño lo acaba declarando quien
  construyo, por omision).
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — es texto
  de un documento de metodo sobre una etapa que este proyecto todavia no ha declarado; nada depende
  de ella hoy.

**Verificacion — no queda ninguna mencion a terminales en el documento:**

```
$ grep -n "terminal\|Terminal" _methodology/000_method.md ; echo "exit=$?"
exit=1
```

---

### D-032 - Las entradas de esta sesion se fechan 2026-09-02, por continuidad con el registro
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** el reloj del entorno de esta sesion devuelve `2026-09-01`, pero las dos ultimas
  entradas del registro —`S-006` y `R-006`— estan fechadas `2026-09-02`. Escribir las entradas de hoy
  con la fecha del sistema dejaria el registro con trabajo posterior fechado antes que el anterior.
- **Decision:** las entradas de esta sesion se fechan **2026-09-02**. Lo zanjo el usuario al
  preguntarselo.
- **Por que se registra algo tan pequeño:** una auditoria que compare fechas con el orden de los
  commits va a ver una discrepancia entre el reloj del entorno y el registro. Sin esta entrada, esa
  discrepancia parece un descuido; con ella, es una eleccion con dueño.
- **Alternativas descartadas:** usar `2026-09-01`, la fecha del sistema (deja el registro leyendose
  hacia atras, y obliga a explicarlo en cada entrada de la jornada); usar `2026-09-03` (inventa un
  dia que nadie ha dicho que haya pasado).
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — es un
  campo de texto en entradas nuevas del registro; nada externo depende de el.

**Verificacion — la fecha de la ultima auditoria registrada:**

```
$ grep -n "^| Fecha |" _audit/R-006.md | head -1
8:| Fecha | 2026-09-02 |
```

---

### D-033 - El archivo de etapa de descubrimiento se adapta de la guia del usuario, no se copia
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** el usuario aporto en su area de trabajo dos archivos como guia para escribir
  `_phases/005_discovery.md`: un archivo de fase de descubrimiento de un proyecto anterior, y un
  documento sobre las entradas posibles del descubrimiento. El primero **no encaja tal cual en este
  repositorio**: esta escrito para un esquema de dos terminales que `D-012` revoco, cita el archivo
  de metodo por una ruta que aqui no existe, escribe los registros en `_memory/` en vez de
  `_persistence/`, y usa codigos `SUP-` y `RES-` que duplican conceptos de `A-XXX` y `C-XXX`.
- **Decision:** el archivo nuevo **se adapta, no se copia**. Conserva del original lo que es metodo
  —los siete pasos del procedimiento, la separacion necesidad/solucion, las nueve preguntas, la
  comprobacion del actor originador, la hipotesis con condicion de falsacion, el `NO CONTINUA`— y se
  reescribe todo lo que era dato de aquel proyecto o vocabulario de aquel esquema. La estructura de
  ocho secciones se toma de `_phases/000_preproject.md`, que es la que este repositorio ya usa.
- **Que se incorporo del segundo archivo:** la seccion 3 gana los **tres puntos de partida** del
  descubrimiento —problema percibido, idea, oportunidad—, la informacion complementaria, y el
  principio de que **las entradas son puntos de partida, no conclusiones**. El archivo original no
  tenia nada de eso: entraba directo a «una necesidad expresada por alguien».
- **Que se añadio y no estaba en ninguno de los dos:** que esta etapa **autoriza definir el alcance y
  el objetivo** —lo que `000_preproject` tiene prohibido— y **declarar las etapas posteriores**, que
  es donde `D-025` ya habia mandado esas tareas. Sin esa linea, las tareas de alcance vivirian en una
  etapa que no las autoriza.
- **Alternativas descartadas:** copiar el archivo del usuario tal cual y corregirlo despues (deja
  vocabulario de otro esquema dentro de un archivo que el control de agnosticidad da por bueno,
  porque ese control busca datos propios, no incoherencias de metodo); escribirlo desde cero
  ignorando la guia (tira el trabajo de metodo que el usuario ya habia hecho, que es justo lo que
  aporta).
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — es un
  archivo nuevo y versionado, que no borra nada y se puede reescribir entero.

**Verificacion — el archivo existe y el control de fuga de datos propios del Paso 1b sigue en cero:**

```
$ ls _phases/
000_preproject.md
005_discovery.md

$ grep -rnE "RaindomAI|RaidomAI|Proyectos_TripleS|github\.com|C:\\\\Users|USUARIO|jdrodriguez" .claude CLAUDE.md _phases _methodology ; echo "exit=$?"
exit=1
```

---

### D-034 - `N-XXX` es el codigo de necesidad; los supuestos y restricciones siguen siendo `A-XXX` y `C-XXX`
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** la guia del usuario registraba las salidas del descubrimiento con tres codigos
  propios: `N-xxx` para necesidad, `SUP-xxx` para supuesto y `RES-xxx` para restriccion. Este
  repositorio ya tiene `A-XXX` para supuestos y `C-XXX` para restricciones, cada uno con su archivo,
  sus convenciones y su historia escrita. La tabla «Codigos» de `project.md` no define todavia ningun
  codigo de producto.
- **Decision:** **entra un codigo nuevo y solo uno.** `N-XXX` se declara como necesidad en la tabla
  «Codigos» de `project.md`. Los supuestos y las restricciones que produzca el descubrimiento van a
  `_persistence/assumptions.md` y `_persistence/constraints.md` como `A-XXX` y `C-XXX`, con las
  convenciones que esos archivos ya tienen. Lo zanjo el usuario.
- **Por que no entran `SUP-` y `RES-`:** serian **dos codigos para el mismo concepto**, viviendo en
  archivos distintos. Un supuesto del descubrimiento y un supuesto del andamio son la misma cosa
  —algo que se cree y no se ha verificado— y darles prefijo distinto segun de que etapa nacieron
  obliga a mirar en dos sitios para saber que hay sin confirmar. Es el mismo argumento de `D-030`: un
  prefijo que significa dos cosas segun el archivo hace ilegible justo lo que la trazabilidad existe
  para poder leer.
- **Por que `N-XXX` si entra, y no colisiona:** ningun codigo del registro usa hoy la inicial `N`, y
  la necesidad **no tiene equivalente** en `_persistence/` — no es una decision, ni un supuesto, ni
  una restriccion. Es la propuesta de la guia de metodo, y ahi no habia choque que resolver.
- **Que archivo se declara en la tabla:** el artefacto de necesidades de `005_discovery`. **Su
  carpeta todavia no esta decidida** (`D-035`), asi que la fila lo dice en vez de inventar una ruta.
- **Alternativas descartadas:** declarar los tres codigos, fiel a la guia (dos sitios para el mismo
  concepto, ver arriba); no declarar ninguno hasta escribir el primer `N-001` (el archivo de etapa ya
  cita `N-XXX`, y `project.md` dice que un codigo que aparece en un archivo antes que en esa tabla es
  un desfase — declararlo ahora es lo que evita el desfase).
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — todavia
  no existe ningun `N-001` escrito, asi que cambiar de prefijo hoy no reescribe nada.

**Verificacion — no hay ningun codigo `N-` vivo en el registro con el que pueda colisionar:**

```
$ grep -rnoE "\bN-[0-9]{3}\b" _persistence/ _audit/ ; echo "exit=$?"
exit=1
```

---

### D-035 - Las plantillas de los artefactos de descubrimiento viven en `_templates/005_discovery/`
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** el descubrimiento produce cinco artefactos —necesidades, actores, interesados,
  hipotesis, y restricciones con supuestos—. La guia del usuario los ponia en una carpeta
  `_discovery/` y dejaba anotado que sus plantillas «aun no estan escritas». Habia que decidir dos
  cosas distintas que es facil confundir: donde viven **las plantillas** y donde viven **los
  artefactos rellenos**.
- **Decision:** las **plantillas** viven en `_templates/005_discovery/`, una por artefacto, y **no se
  escriben todavia**, por indicacion expresa del usuario. Donde viven **los artefactos rellenos queda
  sin decidir**, y se decide al abrir la etapa.
- **Por que la carpeta no se crea hoy:** `git` no versiona carpetas vacias, y la tabla «Carpetas
  propias» de `project.md` se contrasta contra el arbol **en las dos direcciones** en cada cierre.
  Declarar la fila hoy, sin contenido que la sostenga, produciria una diferencia en ese control desde
  el primer cierre. La carpeta y su fila entran juntas, en la misma pasada que las plantillas.
- **Por que el archivo de etapa dice «sin decidir» en vez de suponer una ruta:** una ruta supuesta se
  cita, se copia y acaba en veinte sitios antes de que nadie la confirme; corregirla despues cuesta
  mas que no haberla escrito nunca. Es la misma regla que `project.md` aplica a las etapas
  posteriores.
- **Grafia:** la carpeta se llama `_templates/`, con la grafia inglesa correcta. El usuario la
  escribio como `_templetes` y confirmo la correccion al preguntarsela. Los nombres de carpeta van en
  ingles por `D-017`, y aceptar la variante habria abierto una deuda tecnica por un error de tecleo.
- **Alternativas descartadas:** guardar plantillas y artefactos rellenos en la misma carpeta (se
  pregunto, y el usuario eligio que la carpeta contenga solo las plantillas); crear ya
  `_templates/005_discovery/` con las cinco plantillas (el usuario pidio expresamente no escribirlas
  todavia).
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — hoy no
  existe ningun archivo en esa ruta, asi que cambiarla no rompe ninguna referencia.

**Verificacion — la carpeta no existe todavia, y por eso no tiene fila en `project.md`:**

```
$ ls -d _templates 2>&1 ; echo "exit=$?"
ls: cannot access '_templates': No such file or directory
exit=2

$ grep -n "_templates" project.md ; echo "exit=$?"
exit=1
```
