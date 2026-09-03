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
| [D-036](#d-036---los-artefactos-rellenos-del-descubrimiento-viven-en-_discovery) | Los artefactos rellenos del descubrimiento viven en `_discovery/` | 2026-09-02 | Revocada por D-045 |
| [D-037](#d-037---el-descubrimiento-no-lleva-plantilla-de-restricciones-y-supuestos-se-registran-en-_persistence) | El descubrimiento no lleva plantilla de restricciones y supuestos: se registran en `_persistence/` | 2026-09-02 | Vigente |
| [D-038](#d-038---i-xxx-es-el-codigo-de-interesado) | `I-XXX` es el codigo de interesado | 2026-09-02 | Vigente |
| [D-039](#d-039---t-022-se-reetiqueta-a-000_preproject-escribir-plantillas-es-andamiaje) | `T-022` se reetiqueta a `000_preproject`: escribir plantillas es andamiaje | 2026-09-02 | Vigente |
| [D-040](#d-040---_audits-007md-no-se-reescribe-para-corregir-f-019-la-correccion-va-al-mecanismo) | `_audit/S-007.md` no se reescribe para corregir `F-019`: la correccion va al mecanismo | 2026-09-02 | Vigente |
| [D-041](#d-041---las-cuatro-plantillas-se-adaptan-de-las-del-usuario-no-se-copian) | Las cuatro plantillas se adaptan de las del usuario, no se copian | 2026-09-02 | Vigente |
| [D-042](#d-042---las-entradas-de-esta-sesion-se-fechan-2026-09-02-por-continuidad-con-el-registro) | Las entradas de esta sesion se fechan 2026-09-02, por continuidad con el registro | 2026-09-02 | Vigente |
| [D-043](#d-043---las-entradas-de-s-009-se-fechan-2026-09-02-por-continuidad-con-el-registro) | Las entradas de `S-009` se fechan 2026-09-02, por continuidad con el registro | 2026-09-02 | Vigente |
| [D-044](#d-044---la-ficha-t-026-escrita-a-mano-se-asume-como-caso-puntual-no-como-tercera-excepcion) | La ficha `T-026` escrita a mano se asume como caso puntual, no como tercera excepcion | 2026-09-02 | Vigente |
| [D-045](#d-045---los-artefactos-rellenos-del-descubrimiento-viven-en-005_discovery) | Los artefactos rellenos del descubrimiento viven en `005_discovery/` | 2026-09-02 | Vigente |
| [D-046](#d-046---nace-_workflow-carpeta-agnostica-con-teammd-y-ai_levelsmd) | Nace `_workflow/`, carpeta agnostica con `team.md` y `ai_levels.md` | 2026-09-02 | Vigente |
| [D-047](#d-047---_workflow-aplica-a-todas-las-etapas-declaradas-salvo-000_preproject) | `_workflow/` aplica a todas las etapas declaradas salvo `000_preproject` | 2026-09-02 | Vigente |
| [D-048](#d-048---la-secuencia-de-fases-del-documento-fuente-no-entra-en-el-repositorio) | La secuencia de fases del documento fuente no entra en el repositorio | 2026-09-02 | Vigente |
| [D-049](#d-049---la-frontera-entre-teammd-y-ai_levelsmd-uno-nombra-los-niveles-el-otro-los-desarrolla) | La frontera entre `team.md` y `ai_levels.md`: uno nombra los niveles, el otro los desarrolla | 2026-09-02 | Vigente |
| [D-050](#d-050---f-021-se-trata-como-resuelto-por-desaparicion-y-t-028-pasa-a-cancelada) | `F-021` se trata como resuelto por desaparicion, y `T-028` pasa a `Cancelada` | 2026-09-02 | Vigente |
| [D-051](#d-051---_workflow-gana-un-archivo-por-etapa-y-ese-archivo-es-el-cuarto-enganche) | `_workflow/` gana un archivo por etapa, y ese archivo es el cuarto enganche | 2026-09-02 | Vigente |
| [D-052](#d-052---el-reparto-de-005_discovery-no-se-adopta-todavia-se-adopta-al-abrir-la-etapa) | El reparto de `005_discovery` no se adopta todavia: se adopta al abrir la etapa | 2026-09-02 | Vigente |
| [D-053](#d-053---global_lessonsmd-nace-en-triples_lessons-dentro-de-este-repositorio-de-forma-transitoria) | `global_lessons.md` nace en `TripleS_Lessons/` dentro de este repositorio, de forma transitoria | 2026-09-02 | Vigente |
| [D-054](#d-054---se-consultan-los-bloques-d-y-e-de-global_lessonsmd-antes-de-abrir-005_discovery) | Se consultan los bloques D y E de `global_lessons.md` antes de abrir `005_discovery` | 2026-09-02 | Vigente |
| [D-055](#d-055---el-puntero-a-las-lecciones-globales-la-regla-en-claudemd-el-donde-en-projectmd-el-control-en-la-etapa) | El puntero a las lecciones globales: la regla en `CLAUDE.md`, el donde en `project.md`, el control en la etapa | 2026-09-02 | Vigente |
| [D-056](#d-056---la-cosecha-gana-disparador-una-casilla-por-etapa-y-la-columna-portabilidad-que-la-hace-comprobable) | La cosecha gana disparador: una casilla por etapa, y la columna `Portabilidad` que la hace comprobable | 2026-09-02 | Vigente |
| [D-057](#d-057---no-nace-un-quinto-estado-de-tarea-pendiente-se-normaliza-a-no-implementada) | No nace un quinto estado de tarea: `Pendiente` se normaliza a `No implementada` | 2026-09-02 | Vigente |
| [D-058](#d-058---t-038-se-regulariza-declarando-que-nacio-fuera-de-las-dos-excepciones) | `T-038` se regulariza declarando que nacio fuera de las dos excepciones | 2026-09-02 | Vigente |
| [D-059](#d-059---el-prototipo-descartable-es-la-unica-excepcion-a-pi-5-y-se-declara-en-el-archivo-de-etapa) | El prototipo descartable es la unica excepcion a `PI-5`, y se declara en el archivo de etapa | 2026-09-02 | Vigente |
| [D-060](#d-060---el-archivo-de-etapa-del-prototipo-se-escribe-por-adelantado-sin-declarar-la-etapa) | El archivo de etapa del prototipo se escribe por adelantado, sin declarar la etapa | 2026-09-02 | Vigente |
| [D-061](#d-061---una-carpeta-de-entregables-se-llama-como-su-etapa-y-se-declara-por-adelantado) | Una carpeta de entregables se llama como su etapa, y se declara por adelantado | 2026-09-02 | Vigente |
| [D-062](#d-062---el-numero-de-participantes-lo-fija-el-proyecto-porque-la-guia-de-metodo-no-lo-fija) | El numero de participantes lo fija el proyecto, porque la guia de metodo no lo fija | 2026-09-02 | Vigente |
| [D-063](#d-063---el-paso-2d-publica-la-lista-completa-de-su-primera-orden-no-una-seleccion) | El Paso 2d publica la lista completa de su primera orden, no una seleccion | 2026-09-02 | Vigente |
| [D-064](#d-064---las-cinco-plantillas-del-prototipo-se-adaptan-de-las-del-usuario-no-se-copian) | Las cinco plantillas del prototipo se adaptan de las del usuario, no se copian | 2026-09-02 | Vigente |
| [D-065](#d-065---la-evidencia-del-paso-2d-tiene-sitio-fijo-la-seccion-7-del-informe-de-sesion) | La evidencia del Paso 2d tiene sitio fijo: la seccion 7 del informe de sesion | 2026-09-03 | Vigente |
| [D-066](#d-066---el-reparto-del-prototipo-la-ia-construye-no-facilita-y-clasifica-sin-pesar) | El reparto del prototipo: la IA construye, no facilita, y clasifica sin pesar | 2026-09-03 | Vigente |
| [D-067](#d-067---el-gate-1-no-es-una-etapa-se-monta-como-agente-y-skill) | El Gate 1 no es una etapa: se monta como agente y skill | 2026-09-02 | Vigente |
| [D-068](#d-068---el-gate-1-son-dos-firmas-gate1_auditor-dictamina-y-el-patrocinador-decide) | El Gate 1 son dos firmas: `gate1_auditor` dictamina y el patrocinador decide | 2026-09-02 | Vigente |
| [D-069](#d-069---no-auditable-es-un-tercer-resultado-del-gate-1-que-la-guia-de-metodo-no-tiene) | `NO AUDITABLE` es un tercer resultado del Gate 1, que la guia de metodo no tiene | 2026-09-02 | Vigente |
| [D-070](#d-070---los-dictamenes-del-gate-1-son-correlativos-y-ninguno-se-sobrescribe) | Los dictamenes del Gate 1 son correlativos, y ninguno se sobrescribe | 2026-09-02 | Vigente |
| [D-071](#d-071---la-comprobacion-0-del-gate-1-resuelve-el-antes-por-orden-del-grafo-no-por-fecha) | La Comprobacion 0 del Gate 1 resuelve el «antes» por orden del grafo, no por fecha | 2026-09-03 | Vigente |
| [D-072](#d-072---el-archivo-de-etapa-de-la-baseline-se-escribe-por-adelantado-y-la-etapa-no-queda-adoptada) | El archivo de etapa de la baseline se escribe por adelantado, y la etapa NO queda adoptada | 2026-09-03 | Vigente |
| [D-073](#d-073---las-plantillas-de-la-baseline-se-numeran-por-orden-de-procedimiento-no-por-el-orden-de-la-tabla-de-artefactos) | Las plantillas de la baseline se numeran por orden de procedimiento, no por el orden de la tabla de artefactos | 2026-09-03 | Vigente |
| [D-074](#d-074---la-seccion-5-del-archivo-de-etapa-de-la-baseline-dice-nueve-artefactos-no-ocho) | La seccion 5 del archivo de etapa de la baseline dice nueve artefactos, no ocho | 2026-09-03 | Vigente |

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

---

### D-036 - Los artefactos rellenos del descubrimiento viven en `_discovery/`
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Revocada por D-045 |
| Origen | usuario |

📌 **Nota del 2026-09-02: revocada por `D-045`.** El usuario cambio el nombre de la carpeta a
`005_discovery/`. Lo que sigue es el texto original, que no se reescribe: el porque de haber
elegido carpeta de primer nivel —y no `_persistence/`— sigue siendo el mismo y es lo que `D-045`
hereda; lo unico que cambia es el nombre.

- **Contexto:** `D-035` decidio donde viven **las plantillas** —`_templates/005_discovery/`— y dejo
  expresamente sin decidir donde viven **los artefactos rellenos**, los que llevaran los `N-XXX`
  reales del cliente. Al ir a escribir las plantillas, esa mitad abierta dejo de ser aplazable: las
  plantillas se citan entre si por ruta y sus bloques de comprobacion llevan la ruta escrita dentro.
  Una plantilla con la ruta en blanco no se puede ejecutar ni enlazar.
- **Decision:** los artefactos rellenos viven en **`_discovery/`**, carpeta propia de primer nivel.
  Lo zanjo el usuario. `_templates/005_discovery/` contiene solo las plantillas en blanco;
  `_discovery/` contiene lo que se rellena.
- **Por que carpeta aparte y no dentro de `_persistence/`:** son dos cosas distintas y mezclarlas
  cuesta despues. `_persistence/` registra **como va el trabajo** —sesiones, tareas, decisiones— y
  sus siete archivos tienen indice, convenciones y estados propios. `_discovery/` registra **que se
  entendio del producto**, y sus archivos nacen, se cierran y dejan de tocarse. Meterlos en
  `_persistence/` obligaria a que sus convenciones cubrieran dos regimenes distintos.
- **Cuando se crea la carpeta:** **no hoy.** No existe ningun artefacto relleno que la sostenga,
  `git` no versiona carpetas vacias, y la tabla «Carpetas propias» de `project.md` se contrasta
  contra el arbol en las dos direcciones en cada cierre. La carpeta y su fila entran juntas cuando
  se rellene la primera plantilla — el mismo argumento que `D-035` uso para `_templates/`.
- **Por que la ruta si va escrita en las plantillas y no en `_phases/005_discovery.md`:** son dos
  papeles distintos. El archivo de etapa **describe** —dice que artefactos hay y que contiene cada
  uno— y por eso remite a `project.md` donde haria falta una ruta. Las plantillas son **el
  instrumento**: sus bloques de comprobacion se copian y se corren tal cual, y un comando con un
  hueco dentro no se puede correr. ⚠️ **`_discovery/` no es un dato propio de este proyecto** —es un
  nombre generico de metodo, en ingles, igual que `_phases/` o `_templates/`—, asi que escribirlo
  dentro de `_templates/` no rompe la agnosticidad ni dispara el barrido del Paso 1b.
- **Alternativas descartadas:** meterlos en `_persistence/` (mezcla los dos regimenes, ver arriba);
  dejarlo sin decidir y escribir las plantillas con la ruta como hueco (deja los bloques de
  comprobacion sin poder ejecutarse y los enlaces cruzados rotos, que es justo lo que las plantillas
  existen para evitar).
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — hoy no
  existe ningun archivo en esa ruta, asi que cambiarla no rompe ninguna referencia fuera de las
  cuatro plantillas.

**Verificacion — la carpeta no existe todavia, y por eso no tiene fila en `project.md`:**

```
$ ls -d _discovery 2>&1 ; echo "exit=$?"
ls: cannot access '_discovery': No such file or directory
exit=2

$ grep -n "_discovery" project.md ; echo "exit=$?"
exit=1
```

📌 **Nota del 2026-09-02 (`T-029`, hallazgo `F-022`): la segunda orden de este bloque esta mal
escrita y su salida no se reproduce.** El patron `_discovery` sin barra tambien casa con la cadena
`005_discovery`, que `project.md` ya usaba, asi que devolvia lineas y `exit=0`, no `exit=1`. **El
texto original no se reescribe** (`CLAUDE.md`: una salida antigua no se retoca para que exhiba lo
que no dio). Lo que la decision queria demostrar —que la carpeta de los artefactos rellenos no
tiene fila en «Carpetas propias»— si es cierto, y esta es la orden que si lo demuestra, anclada al
commit de aquella sesion:

```
$ git show f096fff:project.md | grep -n '^| `_discovery/`' ; echo "exit=$?"
exit=1
```

---

### D-037 - El descubrimiento no lleva plantilla de restricciones y supuestos: se registran en `_persistence/`
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** `_phases/005_discovery.md` §5 enumera cinco artefactos, y el quinto es
  «restricciones y supuestos». La guia del usuario traia para el una plantilla completa
  (`025_constraints.md`) con su tabla de `RES-xxx`, su tabla de `SUP-xxx`, sus estados y su rastro de
  resueltos. Pero `D-034` ya habia zanjado que los supuestos y las restricciones del descubrimiento
  van a `_persistence/assumptions.md` y `_persistence/constraints.md` como `A-XXX` y `C-XXX`.
  Escribir esa plantilla habria creado **un segundo registro del mismo concepto**, que es
  exactamente lo que `D-034` rechazo.
- **Decision:** **no se escribe esa plantilla.** `_templates/005_discovery/` lleva cuatro
  —necesidades, actores, interesados e hipotesis—. Las restricciones y los supuestos que produzca la
  etapa nacen directamente en `_persistence/constraints.md` y `_persistence/assumptions.md`, con las
  convenciones que esos archivos ya tienen. Lo zanjo el usuario.
- **Que se pierde y donde se recupera:** la plantilla descartada aportaba tres cosas que
  `_persistence/` no tenia. Las tres entran ahi, que es donde sirven a todas las etapas y no solo a
  una:

| Que aportaba la plantilla | Donde entra |
|---|---|
| **Dueño** del supuesto — quien tiene que ir a verificarlo | campo nuevo en las convenciones de `_persistence/assumptions.md` |
| Estado **`Riesgo abierto`** — no se puede verificar antes de necesitarlo, y se acepta a sabiendas, con quien lo acepto | valor nuevo en la tabla de estados de `assumptions.md` |
| **«Lo que se decidio NO averiguar todavia»** | una `D-XXX` por caso: posponer una averiguacion es una eleccion entre alternativas, y `decisions.md` ya es su sitio |

- **Que hay que corregir por esta decision:** `_phases/005_discovery.md` §5 decia «Cinco documentos»
  y «Las plantillas de los cinco viven en `_templates/005_discovery/`». Se reescribe: cuatro con
  plantilla, y el quinto artefacto remitido a `_persistence/`. El titulo de `T-022` deja de decir
  «las cinco».
- **Lo que NO cambia:** el descubrimiento **sigue produciendo cinco artefactos**. Lo que cambia es
  que uno de ellos no tiene plantilla propia porque su sitio ya existe. `_phases/005_discovery.md`
  §4 paso 6 sigue mandando lo mismo que mandaba.
- **Alternativas descartadas:** escribirla completa, adaptando `SUP-`/`RES-` a `A-XXX`/`C-XXX` (dos
  sitios donde mirar lo que hay sin confirmar, y la obligacion de acordarse de los dos cada vez);
  escribirla delgada, solo con lo que `_persistence/` no cubre (mismo defecto en pequeño: sigue
  siendo un segundo sitio, y ademas uno que solo esta medio lleno).
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — no borra
  ningun archivo; si algun dia hiciera falta, escribir la quinta plantilla es trabajo nuevo, no una
  restauracion.

**Verificacion — no existe ningun `SUP-` ni `RES-` vivo en el registro, y `A-XXX`/`C-XXX` ya estan
en su sitio:**

```
$ grep -rnoE "\b(SUP|RES)-[0-9]{3}\b" _persistence/ _audit/ _phases/ project.md ; echo "exit=$?"
exit=1

$ grep -c "^### A-" _persistence/assumptions.md ; grep -c "^### C-" _persistence/constraints.md
4
7
```

---

### D-038 - `I-XXX` es el codigo de interesado
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** la plantilla de interesados necesita una forma estable de citar a cada uno: la ficha
  de una restriccion dice «quien la impone», la de un actor dice si ademas es interesado, y la tabla
  de aprobaciones dice quien aprueba que. La guia del usuario usaba `I-001` sin declararlo en ningun
  sitio. `project.md` es explicito: **un codigo que aparece en un archivo antes que en su tabla
  «Codigos» es un desfase, no una novedad.**
- **Decision:** `I-XXX` se declara en la tabla «Codigos» de `project.md` como **interesado**, en la
  misma pasada en que se escribe la plantilla que lo usa. Lo zanjo el usuario. Su archivo es el
  artefacto de interesados de `005_discovery`, en `_discovery/` (`D-036`).
- **Por que no colisiona:** ningun codigo del registro usa hoy la inicial `I`, y el interesado no
  tiene equivalente en `_persistence/` — no es una decision, ni un supuesto, ni una restriccion, ni
  un actor. Es el mismo razonamiento que `D-034` hizo con `N-XXX`.
- **Por que se declara ahora y no cuando se escriba el primer `I-001`:** porque la plantilla ya lo
  cita, y una plantilla es un archivo del repositorio como cualquier otro. Declararlo hoy es lo que
  evita el desfase — la misma razon que `D-034` dio para `N-XXX`.
- **Alternativas descartadas:** listar los interesados sin identificador, solo por nombre y rol (deja
  sin forma estable de citarlos desde las otras plantillas, y un nombre cambia de grafia cada vez que
  se teclea); reutilizar `A-XXX` o `C-XXX` (no es ni un supuesto ni una restriccion: es una persona).
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — todavia
  no existe ningun `I-001` escrito, asi que cambiar de prefijo hoy no reescribe nada.

**Verificacion — no hay ningun codigo `I-` vivo en el registro con el que pueda colisionar:**

```
$ grep -rnoE "\bI-[0-9]{3}\b" _persistence/ _audit/ project.md ; echo "exit=$?"
exit=1
```

📌 **Nota del 2026-09-02 (`T-029`, hallazgo `F-022`): esta orden se escribio sin anclar, y sobre el
arbol de trabajo ya no da `exit=1`.** Al correrla sobre el commit que la contiene devuelve siete
coincidencias —todas `I-001` a `I-003` que la propia sesion acababa de escribir—, no cero. **El
texto original no se reescribe.** El fondo si era correcto: antes de la decision no habia ningun
`I-NNN` con el que colisionar, y esta es la orden anclada que lo demuestra:

```
$ git grep -nE "\bI-[0-9]{3}\b" 122b770 -- _persistence/ _audit/ project.md ; echo "exit=$?"
exit=1
```

---

### D-039 - `T-022` se reetiqueta a `000_preproject`: escribir plantillas es andamiaje
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** `R-007` lo observo en sus «recomendaciones sin hallazgo»: `T-022` estaba etiquetada
  `005_discovery`, pero escribir plantillas no responde ninguna pregunta sobre la necesidad del
  cliente. No lo abrio como hallazgo porque hoy ningun archivo obliga a lo contrario.
- **Decision:** `T-022` pasa a `000_preproject`. Lo zanjo el usuario.
- **Por que:** `000_preproject` es, por definicion, la etapa en la que **no se construye producto: se
  monta la forma de trabajar**. Una plantilla es forma de trabajar. Si `T-022` se quedara dentro de
  `005_discovery`, la condicion de salida de esa etapa —seis casillas, todas sobre lo que se entendio
  del cliente— convivria con una tarea de metodo que no responde a ninguna de las seis.
- **Que no cambia:** el contenido de la tarea. Cambia **cuando** se hace, no **que** se hace — igual
  que `D-024` hizo con `T-001` en sentido contrario.
- **Respaldo de escribirlo a mano en `tasks.md`:** la segunda excepcion de la convencion de ese
  archivo (`D-025`): un cambio que nace de una decision del usuario y que el `session-closer` no
  puede deducir del `git diff`.
- **Alternativas descartadas:** dejarla en `005_discovery` (mezcla la condicion de salida de la etapa
  con trabajo de metodo, que es justo lo que `R-007` señalo).
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — es una
  celda de una tabla, y la nota fechada de la ficha conserva de donde venia.

**Verificacion — la ficha y su fila en el indice dicen lo mismo:**

```
$ grep -n "^| \[T-022\]" _persistence/tasks.md | grep -o "| \`0[0-9_a-z]*\` |$"
| `000_preproject` |

$ sed -n '/^### T-022/,/^| Origen/p' _persistence/tasks.md | grep -n "Etapa"
7:| Etapa | `000_preproject` |
```

---

### D-040 - `_audit/S-007.md` no se reescribe para corregir `F-019`: la correccion va al mecanismo
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | manager |

- **Contexto:** `F-019` tiene razon. La seccion 1 de `_audit/S-007.md` presenta su lista de archivos
  como salida de `git show --stat --name-only --format= HEAD`; el comando devuelve diez y la lista
  enumera ocho, faltando `_audit/index.md` y el propio informe. La correccion obvia seria completar
  la lista en ese archivo.
- **Decision:** **no se toca `_audit/S-007.md`.** Se acepta el hallazgo y la correccion se aplica al
  mecanismo que lo produjo, en `.claude/skills/protocol-close/SKILL.md` (`T-025`).
- **Por que:** un informe de sesion no es un documento vivo — es la descripcion de **un commit
  concreto**, y `R-007` ya lo juzgo como estaba. Reescribirlo hoy dejaria a la auditoria describiendo
  un estado que ya cambio, y a quien lea `R-007` mañana sin poder contrastar ni una linea. Es lo
  mismo que `CLAUDE.md` prohibe cuando dice que los hallazgos **no se arreglan en el momento**.
- **Y hay una razon mas, especifica de este hallazgo:** el defecto de `S-007` no es que la lista este
  corta, es que se **presenta como generada** sin serlo. Completarla a mano hoy produciria
  exactamente el mismo defecto una vez mas — una lista que dice venir de un comando y que nadie
  corrio.
- **Lo incomodo, y se escribe:** el mecanismo ya existia. `SKILL.md` avisa desde antes de que «el
  cierre anade archivos que no son de contenido —la fila de `_audit/index.md`, el propio informe— y
  son justo los que se olvidan al escribir de memoria». `S-007` no lo siguio. Por eso `T-025` no
  inventa una regla nueva: la mueve de un bloque explicativo a la **estructura del informe**, donde
  no se puede escribir la seccion sin verla. Es `L-008` otra vez: una regla sin mecanismo que la
  aplique no evita la reincidencia.
- **Alternativas descartadas:** completar la lista en `S-007.md` (reescribe historia auditada, y
  vuelve a producir una lista no generada); no hacer nada y anotar la leccion (`L-008` dice que una
  leccion sin mecanismo no evita la reincidencia, y esta ya iba por la segunda vez).
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — no se
  borra ni se publica nada; se elige donde poner el arreglo, y la eleccion se puede rehacer.

**Verificacion — el hallazgo se sostiene, y el archivo que lo contiene sigue intacto:**

```
$ git show --stat --name-only --format= 122b770 | wc -l
10

$ git show 122b770:_audit/S-007.md | sed -n '/^## 1\./,/^## 2\./p' | grep -c '^- `'
8

$ git status --porcelain -- _audit/S-007.md ; echo "exit=$?"
exit=1
```

📌 **Nota del 2026-09-02 (`T-029`, hallazgo `F-022`): la tercera orden de este bloque devuelve
`exit=0`, no `exit=1`.** `git status` sale con `0` cuando no tiene nada que reportar; lo que se
queria mostrar era la **ausencia de salida**, y para eso el codigo de salida no sirve. **El texto
original no se reescribe.** El fondo si era correcto —`_audit/S-007.md` sigue intacto— y esta es la
forma que si lo dice, la misma que `T-025` ya usaba:

```
$ git status --porcelain -- _audit/S-007.md | wc -l
0
```

---

### D-041 - Las cuatro plantillas se adaptan de las del usuario, no se copian
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** el usuario aporto en su area de trabajo cinco plantillas de descubrimiento de un
  proyecto anterior. Son buen material de metodo —las nueve preguntas, la ficha del Actor Generador,
  la hipotesis sellada, las tablas de errores que cada plantilla existe para evitar— pero **no
  encajan tal cual en este repositorio**: estan escritas para el esquema de dos terminales que
  `D-012` revoco, usan los codigos `SUP-`/`RES-` que `D-034` rechazo, escriben los registros en
  `_memory/` en vez de `_persistence/`, y citan un archivo de Gate que este proyecto no ha declarado.
- **Decision:** las plantillas **se adaptan, no se copian**. Es el mismo criterio que `D-033` aplico
  al archivo de etapa, y por la misma razon.
- **Que se conserva, porque es metodo:** las nueve preguntas; la ficha de necesidad y la prohibicion
  de nombrar una pantalla; la ficha del Actor Generador con su veredicto `NO CONTINUA`; la tabla de
  tipos de actor ausentes; la separacion actor/interesado; la hipotesis de un solo commit con su
  condicion de falsacion, su umbral y su ventana; el perfil del usuario representativo; las tablas de
  «errores que esta plantilla existe para evitar»; y la seccion «Guia de llenado» que se borra al
  cerrar el artefacto.
- **Que se cambia, y por que:**

| # | Que traia | Que se escribe | Por que |
|---|---|---|---|
| 1 | `Escrito por: terminal ejecutora` | `Escrito por: manager` | `D-012` revoco el esquema de dos terminales |
| 2 | «la auditora», veredicto `NO AUDITABLE` | `report_auditor`, y la consecuencia remitida a su protocolo | ese vocabulario no existe en este repositorio |
| 3 | `SUP-xxx` / `RES-xxx` | `A-XXX` y `C-XXX` en `_persistence/` | `D-034` |
| 4 | `_memory/`, y el paso de copiar ahi al cerrar | desaparece | los `A-XXX`/`C-XXX` **nacen** ya en `_persistence/`; no hay que trasladarlos (`D-037`) |
| 5 | `methodology/000_method.md`, `phases/005_discovery.md` | `_methodology/000_method.md`, `_phases/005_discovery.md` | son las rutas reales |
| 6 | `phases/015_gate1.md` §3 | «un Gate posterior», sin ruta | esa etapa no esta declarada, y `project.md` prohibe citar una que no lo este |
| 7 | referencias a `025_constraints.md` | a `_persistence/assumptions.md` y `_persistence/constraints.md` | `D-037` |
| 8 | rutas `_discovery/...` heredadas | las mismas, pero ya decididas | `D-036` las hace ciertas, no supuestas |
| 9 | `I-001` sin declarar | `I-XXX`, declarado | `D-038` |
| 10 | texto con acentos | sin acentos | el resto de la documentacion del repositorio se escribe asi |

- **Que se conserva y podria sorprender:** los ejemplos de la app de recogida de reciclaje. Son de
  **otro dominio**, no datos de este proyecto, y por eso no disparan el control de agnosticidad; y
  una plantilla sin ejemplo se rellena peor. El hueco `<NOMBRE DEL PROYECTO>` se conserva igual.
- **Alternativas descartadas:** copiarlas y corregirlas despues (deja vocabulario de otro esquema
  dentro de archivos que el control de agnosticidad da por buenos, porque ese control busca datos
  propios, no incoherencias de metodo — es el mismo argumento de `D-033`); escribirlas desde cero
  (tira el trabajo de metodo que el usuario ya habia hecho, que es justo lo que aportan).
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — son
  archivos nuevos y versionados, que no borran nada.

**Verificacion — las plantillas existen y no arrastran el vocabulario del esquema revocado:**

```
$ ls _templates/005_discovery/
005_needs.md
010_actors.md
015_stakeholders.md
020_hypothesis.md

$ grep -rnE "SUP-[0-9]|RES-[0-9]|_memory/|terminal ejecutora|NO AUDITABLE|015_gate1" _templates/ ; echo "exit=$?"
exit=1
```

---

### D-042 - Las entradas de esta sesion se fechan 2026-09-02, por continuidad con el registro
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | manager |

- **Contexto:** el reloj del entorno marca `2026-09-01`, y los commits de `git` llevan esa fecha.
  Pero `D-032` ya decidio fechar `S-007` como `2026-09-02`, y `R-007` uso la misma. Escribir hoy
  `2026-09-01` pondria a `S-008` **antes** que la sesion que la precede.
- **Decision:** las entradas de `S-008` se fechan **`2026-09-02`**, la misma que `S-007` y `R-007`.
- **Por que la misma fecha y no la siguiente:** `CLAUDE.md` dice expresamente que **puede haber
  varias sesiones en la misma fecha**, cada una con su `S-XXX`. Compartir fecha con `S-007` es normal
  y no ambiguo; inventar `2026-09-03` seria fabricar un dia que no existio en ningun reloj ni en
  ningun commit.
- **Lo que esto NO hace:** no cambia ninguna fecha ya escrita, y no toca las fechas de `git`, que
  siguen siendo las que son. La divergencia entre el reloj del entorno y el registro se declara aqui
  —igual que la declaro `D-032`— para que no se lea como un descuido.
- **Alternativas descartadas:** usar `2026-09-01`, la del reloj (dejaria a `S-008` fechada antes que
  `S-007`, y el orden del registro es lo unico que permite leerlo); usar `2026-09-03` (un dia sin
  respaldo en ningun reloj ni en ningun commit).
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — es una
  convencion de escritura, y corregirla despues solo cuesta reescribir fechas.

**Verificacion — el reloj y el ultimo commit dicen `2026-09-01`; el registro viene fechado
`2026-09-02` desde `D-032`:**

```
$ date +%F
2026-09-01

$ git log -1 --format="%h %ad" --date=short
ae06147 2026-09-01

$ grep -c "^| Fecha | 2026-09-02 |" _persistence/decisions.md
16
```

---

### D-043 - Las entradas de `S-009` se fechan 2026-09-02, por continuidad con el registro
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | manager |

- **Contexto:** es el mismo caso que `D-042` resolvio para `S-008`, y se repite sin cambios: el reloj
  del entorno marca `2026-09-01` y los commits llevan esa fecha, pero el registro viene fechado
  `2026-09-02` desde `D-032`. Escribir hoy `2026-09-01` pondria a `S-009` **antes** que `S-007` y
  `S-008`.
- **Decision:** las entradas de `S-009` se fechan **`2026-09-02`**, la misma que `S-007`, `S-008`,
  `R-007` y `R-008`.
- **Por que se escribe otra decision y no basta con `D-042`:** `D-042` decide sobre las entradas de
  `S-008`, y su titulo lo dice. Reaprovecharla para una sesion que no nombra obligaria a leerla como
  si dijera algo mas amplio de lo que dice. ⚠️ **Si el caso vuelve a repetirse, lo que toca no es una
  cuarta decision identica sino una regla general** —«el registro se fecha por continuidad mientras
  el reloj del entorno no alcance al registro»—, y esa si valdria una `D-XXX` con vocacion de
  quedarse.
- **Alternativas descartadas:** usar `2026-09-01`, la del reloj (deja `S-009` fechada antes que las
  dos sesiones que la preceden); usar `2026-09-03` (un dia sin respaldo en ningun reloj ni commit);
  fechar en silencio sin registrar nada (`CLAUDE.md`: cero decisiones silenciosas).
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — es una
  convencion de escritura dentro del repositorio, y rehacerla solo cuesta reescribir fechas.

**Verificacion — el reloj y el ultimo commit siguen en `2026-09-01`, y el registro ya venia en
`2026-09-02`:**

```
$ date +%F
2026-09-01

$ git log -1 --format="%h %ad" --date=short
7025a05 2026-09-01

$ git show HEAD:_persistence/decisions.md | grep -c "^| Fecha | 2026-09-02 |"
16
```

📌 **Nota del 2026-09-02 (`T-033`, hallazgo `F-025`): las dos ultimas ordenes de este bloque
se escribieron sin anclar, y sobre el commit que las contiene no se reproducen.** `HEAD`, mientras
se escribia la decision, era todavia `7025a05` —el commit **anterior**—, asi que el bloque describe
el estado de partida y no el del commit que lo publica. **El texto original no se reescribe**
(`CLAUDE.md`: una salida antigua no se retoca para que exhiba lo que no dio). El fondo era cierto,
y estas son las mismas ordenes ancladas a los dos commits, que lo demuestran:

```
$ git log -1 --format="%h %ad" --date=short 7025a05
7025a05 2026-09-01

$ git show 7025a05:_persistence/decisions.md | grep -c "^| Fecha | 2026-09-02 |"
16

$ git show fc91957:_persistence/decisions.md | grep -c "^| Fecha | 2026-09-02 |"
23
```

Los `16` del bloque original son los de `7025a05`; sobre `fc91957`, el commit que contiene esta
decision, son `23` —las siete entradas que la propia sesion añadio—. El reloj seguia en
`2026-09-01` en los dos.

---

### D-044 - La ficha `T-026` escrita a mano se asume como caso puntual, no como tercera excepcion
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | report_auditor |

- **Contexto:** `F-023` tiene razon. La convencion de `tasks.md` admite dos excepciones para escribir
  una ficha a mano, y las dos exigen **un `D-XXX` o un `F-NNN` citado en la propia tarea**. `T-026`
  no cita ninguno: no nace de un hallazgo —`R-007` no la abrio— y su cambio si se deduce del
  `git diff`, que toca `CLAUDE.md` y `SKILL.md`. La ficha lo declara en prosa, pero la desviacion
  nunca llego a `decisions.md`, que es donde `CLAUDE.md` manda el porque de lo que se elige.
- **Decision:** se asume la desviacion como **caso puntual**. Esta decision es el `D-XXX` que a
  `T-026` le faltaba, y se cita en su ficha. **No se abre una tercera excepcion** en la convencion de
  `tasks.md`, que queda igual que estaba.
- **Por que caso puntual y no tercera excepcion:** las dos excepciones existentes cubren cosas que el
  `session-closer` **no puede** deducir —un hallazgo evaluado hoy, una orden del usuario que no deja
  rastro en el diff—. `T-026` no es ninguna de las dos: el cierre la habria escrito igual de bien.
  Una tercera excepcion que diga «tambien cuando a `manager` le venga de paso» no acota nada; es la
  puerta que la propia convencion avisa de no abrir. Lo correcto habria sido esperar al cierre.
- **Por que no se borra la ficha para que la reescriba el cierre:** ya lo razona la propia `T-026`, y
  el razonamiento se mantiene: borrarla no cambiaria nada del repositorio salvo quien la tecleo, y
  borraria el rastro de que la regla se salto. Un incumplimiento declarado se audita; uno deshecho,
  no.
- **Lo incomodo, y se escribe:** esta decision se escribe **despues** del hecho, y eso no la
  convierte en una autorizacion previa. Lo que hace es dejar el caso donde se busca en vez de
  enterrado en la ficha que lo comete. ⚠️ **Si el patron reaparece, ya no es caso puntual:** el
  segundo es un hallazgo, no otra `D-XXX` como esta.
- **Alternativas descartadas:** abrir la tercera excepcion en la convencion (no acota nada, ver
  arriba); no registrar nada y dejarlo en la prosa de la ficha (es exactamente lo que `F-023`
  señala, y el mismo hueco que `F-007` abrio con `D-020`); borrar la ficha y dejar que la reescriba
  el cierre (borra el rastro del incumplimiento).
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — no se
  borra ni se publica nada; se registra un porque, y un registro se corrige con otra entrada.

**Verificacion — la desviacion existe y no estaba registrada antes de esta entrada:**

```
$ git show HEAD:_persistence/decisions.md | grep -n "T-026" ; echo "exit=$?"
exit=1

$ git show HEAD:_persistence/tasks.md | grep -c "NO encaja en ninguna de las dos excepciones"
1
```

📌 **Nota del 2026-09-02 (`T-033`, hallazgo `F-025`): la primera orden de este bloque se
escribio sin anclar y sobre el commit que la contiene no se reproduce.** `HEAD`, mientras se
escribia, era `7025a05`; sobre `fc91957` la misma orden devuelve ocho coincidencias, porque esta
decision y la ficha de `T-026` ya la citan. **El texto original no se reescribe.** Lo que la
decision queria demostrar —que la desviacion no estaba registrada **antes** de esta entrada— si es
cierto, y esta es la orden anclada que lo demuestra:

```
$ git show 7025a05:_persistence/decisions.md | grep -c "T-026"
0

$ git show fc91957:_persistence/decisions.md | grep -c "T-026"
8
```

La segunda orden del bloque original si se reproduce sobre `fc91957`, y da `1`.

---

### D-045 - Los artefactos rellenos del descubrimiento viven en `005_discovery/`
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** `D-036` decidio que los artefactos rellenos del descubrimiento vivieran en
  `_discovery/`, y esa ruta quedo escrita dentro de las cuatro plantillas de
  `_templates/005_discovery/` y en dos filas de la tabla «Codigos» de `project.md`. El usuario
  ordeno que los entregables de la etapa vayan a `005_discovery/`.
- **Decision:** los artefactos rellenos viven en **`005_discovery/`**, carpeta propia de primer
  nivel. `D-036` queda **revocada por esta**. Lo unico que cambia es el nombre: el resto de `D-036`
  —carpeta aparte y no dentro de `_persistence/`, la carpeta no se crea hasta que exista un artefacto
  que la sostenga, la ruta va escrita dentro de las plantillas y no en `_phases/005_discovery.md`— se
  mantiene igual, y esta decision lo hereda entero.
- **Por que el nombre nuevo es mejor:** la carpeta pasa a llamarse **como la etapa que la produce**.
  `_phases/005_discovery.md` describe la etapa, `_templates/005_discovery/` guarda sus plantillas y
  `005_discovery/` guarda sus artefactos: los tres nombres coinciden, y cuando existan mas etapas la
  correspondencia se lee sola. `_discovery/` no decia de que etapa venia.
- **Que NO cambia:** no se crea ninguna carpeta hoy —sigue sin haber artefacto relleno que la
  sostenga, y `git` no versiona carpetas vacias—, y `project.md` sigue sin fila en «Carpetas propias»
  hasta que exista. Es el mismo criterio de `D-035` y `D-036`.
- **Sobre la agnosticidad:** `005_discovery/` es un nombre generico de metodo, en ingles, igual que
  `_phases/` o `_templates/`. Escribirlo dentro de `_templates/` no dispara el barrido del Paso 1b,
  que busca datos propios de este proyecto.
- **Alternativas descartadas:** mantener `_discovery/` (no dice de que etapa viene, y el usuario
  zanjo lo contrario); `discovery/` sin prefijo (pierde el numero, que es lo que ordena las etapas
  entre si).
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — la
  carpeta todavia no existe y no hay ni un archivo dentro, asi que el cambio no rompe ninguna
  referencia fuera de las cuatro plantillas y las dos filas de `project.md`, que se actualizan en
  `T-031`.

**Verificacion — donde estaba escrita la ruta vieja antes de cambiarla, sobre el commit auditado:**

```
$ git grep -n -- "_discovery/" HEAD -- _templates project.md
HEAD:_templates/005_discovery/005_needs.md:5:| Artefacto | `_discovery/005_needs.md` |
HEAD:_templates/005_discovery/005_needs.md:105:grep -n "<" _discovery/005_needs.md                 # debe no devolver nada
HEAD:_templates/005_discovery/005_needs.md:106:grep -n "Guia de llenado" _discovery/005_needs.md   # debe no devolver nada
HEAD:_templates/005_discovery/005_needs.md:107:grep -n "^| Estado |" _discovery/005_needs.md       # debe decir CERRADO
HEAD:_templates/005_discovery/010_actors.md:5:| Artefacto | `_discovery/010_actors.md` |
HEAD:_templates/005_discovery/010_actors.md:130:grep -n "<" _discovery/010_actors.md                 # debe no devolver nada
HEAD:_templates/005_discovery/010_actors.md:131:grep -n "Guia de llenado" _discovery/010_actors.md   # debe no devolver nada
HEAD:_templates/005_discovery/010_actors.md:132:grep -ni "invitado" _discovery/010_actors.md         # SOLO la advertencia de §4, ni una linea mas
HEAD:_templates/005_discovery/015_stakeholders.md:5:| Artefacto | `_discovery/015_stakeholders.md` |
HEAD:_templates/005_discovery/015_stakeholders.md:113:grep -n "<" _discovery/015_stakeholders.md                 # debe no devolver nada
HEAD:_templates/005_discovery/015_stakeholders.md:114:grep -n "Guia de llenado" _discovery/015_stakeholders.md   # debe no devolver nada
HEAD:_templates/005_discovery/015_stakeholders.md:115:grep -n "TODAVIA NO" _discovery/015_stakeholders.md        # cada linea necesita su A-XXX
HEAD:_templates/005_discovery/020_hypothesis.md:5:| Artefacto | `_discovery/020_hypothesis.md` |
HEAD:_templates/005_discovery/020_hypothesis.md:16:> 2. Que **no cambio durante la etapa** → `git log --oneline -- _discovery/020_hypothesis.md` debe
HEAD:_templates/005_discovery/020_hypothesis.md:123:grep -n "<" _discovery/020_hypothesis.md                 # debe no devolver nada
HEAD:_templates/005_discovery/020_hypothesis.md:124:grep -n "Guia de llenado" _discovery/020_hypothesis.md   # debe no devolver nada
HEAD:_templates/005_discovery/020_hypothesis.md:125:git log --oneline -- _discovery/020_hypothesis.md        # debe devolver UNA sola linea
HEAD:project.md:166:| `N-XXX` | `_discovery/005_needs.md`, el artefacto de necesidades de `005_discovery` (`D-036`) | necesidad |
HEAD:project.md:167:| `I-XXX` | `_discovery/015_stakeholders.md`, el artefacto de interesados de `005_discovery` (`D-038`) | interesado |
```

---

### D-046 - Nace `_workflow/`, carpeta agnostica con `team.md` y `ai_levels.md`
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** el usuario aporto en su area de trabajo un documento con notas en desorden sobre
  cuando trabajar con humanos, cuando con software y cuando con IA, mas los niveles de sistema de IA
  que puede tener un proyecto. Pidio convertirlo en material del repositorio, agnostico y alineado
  con el metodo.
- **Decision:** nace **`_workflow/`**, carpeta propia de primer nivel, con **dos** archivos:
  `team.md` —el reparto del trabajo entre Humano, Software e IA— y `ai_levels.md` —los niveles de
  sistema de IA y la rubrica para elegir uno—. La carpeta entra en los tres sitios que la hacen
  existir de verdad: la fila de «Carpetas propias» de `project.md`, la lista de lo copiable tal cual
  de `CLAUDE.md`, y el **ambito del Paso 1b** de `protocol-close`, que pasa de cinco rutas a seis.
- **Por que carpeta propia y no dentro de `_methodology/`:** son dos cosas distintas.
  `_methodology/` es el metodo de desarrollo recibido —que etapas existen y que pregunta responde
  cada una—, y sus fuentes en `sources/` **no se editan**. `_workflow/` es doctrina de proceso
  escrita por nosotros, adaptada, que se aplica **dentro** de cualquier etapa. Meterla en
  `_methodology/` la haria pasar por metodo canonico recibido, que no lo es.
- **Por que tampoco dentro de `_phases/`:** un archivo de etapa dice **que** trabajo se autoriza y
  cual se prohibe. `_workflow/` dice **quien** hace el trabajo ya definido. Si el reparto se escribe
  dentro de cada etapa hay que repetirlo en todas, y a la tercera dejan de decir lo mismo.
- **Los tres sitios entran en la misma pasada, y eso es deliberado:** una carpeta sin fila la
  señalaria el control del Paso 2c; una carpeta agnostica fuera del ambito del Paso 1b dejaria el
  control de fuga de datos mirando a otro lado — que es exactamente lo que `T-026` corrigio para
  `_templates/`.
- **Alternativas descartadas:** un unico archivo con todo (mezcla dos naturalezas —quien hace el
  trabajo y cuanto sistema pide— y el nombre `team.md` describiria mal la segunda mitad); dejarlo en
  `_methodology/` (lo haria pasar por fuente canonica no editable); no crear carpeta y meter el
  reparto en cada archivo de etapa (se repite en todas y se desincroniza).
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — son dos
  archivos nuevos y tres lineas en archivos existentes; se deshace con `git revert` y no hay nada
  publicado ni borrado.

**Verificacion — la carpeta existe con sus dos archivos, esta declarada, y pasa los dos controles
que le aplican:**

```
$ ls _workflow/
ai_levels.md
team.md

$ diff <(git ls-files --cached --others --exclude-standard | grep "/" | cut -d/ -f1 | sort -u | sed 's|$|/|') \
       <(sed -n '/^## Carpetas propias/,/^## Codigos/p' project.md | grep -oE '^\| `[^`]+/`' | tr -d '|` ' | sort)
8a9
> temporal/

$ grep -rnE "RaindomAI|RaidomAI|Proyectos_TripleS|github\.com|C:\\Users|USUARIO|jdrodriguez" .claude CLAUDE.md _phases _methodology _templates _workflow ; echo "exit=$?"
exit=1

$ grep -rn "<" _workflow/ ; echo "exit=$?"
exit=1
```

La unica diferencia del segundo control es `temporal/`, que **tiene su motivo escrito** en
`project.md`: existe en disco y nunca aparece en el arbol porque `.gitignore` la excluye.
`_workflow/` ya no aparece: carpeta y fila entraron juntas.

---

### D-047 - `_workflow/` aplica a todas las etapas declaradas salvo `000_preproject`
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** el usuario fijo el alcance al pedir el trabajo: el reparto debe aplicar a todas las
  fases del proyecto **excepto** `000_preproject`.
- **Decision:** los dos archivos de `_workflow/` aplican a **todas las etapas declaradas en
  `project.md` salvo `000_preproject`**, y cada uno lo declara en su seccion «Alcance».
- **Por que la excepcion es correcta y no un hueco:** `000_preproject` no reparte trabajo sobre un
  producto — **construye el sistema de trabajo que hace posible el reparto**. Aplicarse a si misma no
  aporta nada y confunde el andamio con la obra. Es el mismo argumento con el que `_methodology/`
  deja esa etapa fuera del ciclo: *«no responde ninguna pregunta sobre el producto»*.
- **Y hay un segundo motivo, que ademas resuelve un problema de redaccion:** lo que `000_preproject`
  monto —un humano que dirige, unos protocolos deterministas y unos agentes especializados— **ya es**
  un reparto Humano/Software/IA en funcionamiento. Asi que la etapa excluida entra en `team.md` §11
  como **ejemplo trabajado**, y el archivo se explica con algo que existe en vez de con un caso
  inventado.
- **Lo que esto NO significa:** que en `000_preproject` se pueda repartir trabajo sin criterio. Ahi
  siguen mandando `CLAUDE.md` y `_phases/000_preproject.md`, que ya dicen quien hace que y que no se
  delega.
- **Alternativas descartadas:** aplicarlo tambien a `000_preproject` (obligaria a repartir trabajo
  sobre un producto que todavia no existe, y dejaria el archivo sin su mejor ejemplo); no fijar
  alcance y dejarlo implicito (un archivo sin alcance escrito se aplica donde a cada uno le parece).
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — es una
  frase en la seccion «Alcance» de dos archivos.

**Verificacion — los dos archivos declaran la excepcion, y cada uno una sola vez:**

```
$ grep -c "000_preproject" _workflow/team.md _workflow/ai_levels.md
_workflow/team.md:1
_workflow/ai_levels.md:1
```

---

### D-048 - La secuencia de fases del documento fuente no entra en el repositorio
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | manager |

- **Contexto:** el documento que aporto el usuario trae **su propia lista de fases**, y la repite dos
  veces: `DISCOVER → AUDIT → MODEL → DECIDE → DEFINE → BUILD → EVALUATE → DEPLOY → MEASURE → LEARN`.
  No es la del metodo que seguimos, que va de descubrimiento a prototipo, Gate 1, linea base,
  esqueleto, crecimiento, MVP, Gate 2 y evolucion.
- **Decision:** esa secuencia **no entra**. Ni en `team.md`, ni en `ai_levels.md`, ni en ningun otro
  archivo del repositorio. Los dos archivos hablan de «cada etapa» y remiten a `project.md` para
  saber cuales estan declaradas.
- **Por que:** dos juegos de fases conviviendo es el error que `_methodology/` avisa expresamente en
  su «Alcance» — *describe el metodo; no declara las etapas de ningun proyecto*. Y este proyecto
  tiene declaradas dos, `000_preproject` y `005_discovery`, con `T-002` todavia abierta para el
  resto. Meter una tercera lista dejaria tres respuestas distintas a «¿que etapas tiene esto?».
- **Lo que si se conserva del documento fuente:** el principio de que el reparto se decide **en cada
  fase** segun el trabajo que haya. Eso es cierto con cualquier lista de fases, y es lo que hace el
  material reutilizable.
- **Alternativas descartadas:** incluir la secuencia como referencia informativa (una lista de fases
  escrita en un archivo del repositorio se acaba leyendo como declaracion, por mucho que la nota diga
  lo contrario); mapear las dos secuencias en una tabla de equivalencias (inventa correspondencias
  que nadie ha decidido, y las inventa antes de que existan las etapas posteriores).
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — es una
  omision deliberada; añadirla despues cuesta escribirla.

**Verificacion — ninguno de los diez nombres de esa secuencia aparece en `_workflow/`:**

```
$ grep -rnE "\b(DISCOVER|AUDIT|MODEL|DECIDE|DEFINE|BUILD|EVALUATE|DEPLOY|MEASURE|LEARN)\b" _workflow/ ; echo "exit=$?"
exit=1
```

📌 El patron va **con delimitadores de palabra**, y no es un adorno: sin ellos, `MODEL` casa con
`MODELO` y el control devuelve tres lineas de los diagramas de `ai_levels.md` que no tienen nada que
ver con la secuencia. Es `L-013` aplicada en el mismo dia que se escribio.

---

### D-049 - La frontera entre `team.md` y `ai_levels.md`: uno nombra los niveles, el otro los desarrolla
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | manager |

- **Contexto:** los niveles de sistema de IA tienen que aparecer en los dos archivos. En `team.md`
  porque, una vez que el reparto asigna trabajo a la IA, la pregunta inmediata es cuanto sistema pide
  ese trabajo. En `ai_levels.md` porque es su tema. Sin una frontera escrita, la misma doctrina acaba
  contada dos veces, y a la tercera edicion los dos archivos dicen cosas distintas (`L-001`).
- **Decision:** **`team.md` nombra; `ai_levels.md` desarrolla.**

| En `team.md` (§7) | En `ai_levels.md` |
|---|---|
| los siete niveles en una tabla, una linea cada uno | una seccion por nivel, con su diagrama y cuando se elige |
| la regla del menor nivel suficiente | orquestador y especialistas, comportamiento probabilistico, harness, observabilidad, evaluaciones, rubricas, metricas y experimentos |
| el aviso de que nombrar no es declarar | la **rubrica de seleccion** y el momento del metodo en que se declara el nivel |

- **Por que esa linea y no otra:** `team.md` necesita los niveles para **cerrar su propio
  razonamiento** —reparto, autonomia, cuanto sistema—, y para eso basta con nombrarlos. Todo lo que
  va mas alla de nombrarlos es diseño de sistema, y ahi `team.md` ya no aporta nada.
- **Lo que se añadio y no estaba en el documento fuente:** la **rubrica de seleccion** de
  `ai_levels.md` §6. El documento enumera los factores —riesgo, autonomia, complejidad, variabilidad,
  impacto de un error— y **nunca dice como se combinan**. Sin eso, el archivo es una lista de niveles
  y no una forma de elegir uno. Es el mismo criterio de `D-041`: se adapta, no se copia — y lo que se
  añade es justamente lo que a la fuente le faltaba.
- **Alternativas descartadas:** un solo archivo con todo (el nombre `team.md` describe bien el
  reparto y mal los niveles de ingenieria, y el archivo pasaria de doscientas lineas a mas de
  cuatrocientas mezclando dos naturalezas); que `team.md` no mencionara los niveles en absoluto
  (dejaria su razonamiento a medias, sin decir que hacer despues de asignar trabajo a la IA).
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — es un
  reparto de contenido entre dos archivos nuevos, sin ninguna referencia externa que lo ate.

**Verificacion — el desarrollo esta en un archivo y no en el otro:**

```
$ grep -c "^### Nivel" _workflow/ai_levels.md
7

$ grep -c "^### Nivel" _workflow/team.md
0

$ grep -c "^| \*\*[0-6]\*\* |" _workflow/team.md
7
```

Siete secciones de desarrollo en `ai_levels.md`, ninguna en `team.md`, y en `team.md` los siete
niveles como siete filas de una tabla. La frontera se sostiene.

---

### D-050 - `F-021` se trata como resuelto por desaparicion, y `T-028` pasa a `Cancelada`

| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | report_auditor |

- **Contexto:** `F-024` tiene razon. `T-028` corrigio la celda «Avance de la etapa» de
  `progress.md`, pero esa celda la **sobrescribe entera el cierre** en cada pasada: cuando
  `session-closer` escribio el estado de `S-009`, la correccion desaparecio junto con el texto que
  corregia. En el commit `fc91957` no queda ni el hash mal atribuido ni la nota fechada que tres
  registros distintos afirman haber dejado. La cadena tampoco sobrevive en ninguna otra parte del
  archivo, asi que la segunda salida que `F-024` proponia —corregirla donde el texto siga vivo— no
  tiene objeto.
- **Decision:** se registra que `F-021` quedo **resuelto por desaparicion del texto**, no por
  correccion; se ajusta la redaccion de los tres sitios que afirman una nota fechada inexistente; y
  `T-028` pasa de `Implementada` a **`Cancelada`**, con nota fechada que explica por que. Su relevo
  es `T-032`, que es la tarea que si deja rastro auditable.
- **Por que `Cancelada` y no `Implementada`:** `PI-5` no admite una tercera casilla. El criterio de
  cierre de `T-028` —«la celda atribuye a `R-007` el commit `122b770`»— **no se cumple sobre el
  commit que la contiene**, y una tarea `Implementada` cuyo criterio su propio commit incumple es
  exactamente el patron que `F-016` abrio. `Cancelada` dice la verdad completa: se ejecuto, su
  efecto no sobrevivio, y **no procede reintentarla** porque su objeto ya no existe.
- **Por que no se reescriben las viñetas antiguas:** `D-019` y `CLAUDE.md` prohiben retocar una
  salida o una afirmacion pasada para que exhiba lo que no dio. Lo que se hace es lo mismo que
  `T-029` hizo con `D-036`, `D-038` y `D-040`: **nota fechada al lado**, con la orden anclada y su
  salida cruda. La excepcion son las secciones 1 y 2 de `progress.md`, que `D-027` reparte a
  `manager` y que el cierre sobrescribe de todos modos: ahi la afirmacion falsa se corrige en su
  sitio.
- **La leccion que esto deja, y va a `lessons.md`:** una correccion escrita **dentro de una seccion
  que el cierre sobrescribe** no es una correccion, es un borrador. El sitio durable es la ficha, el
  hallazgo o la bitacora.
- **Alternativas descartadas:** dejar `T-028` en `Implementada` y anotar el fallo (mantiene en el
  indice un `Implementada` que el commit desmiente, que es el defecto que `F-016` ya señalo);
  devolverla a `No implementada` (leeria como pendiente, y no hay nada pendiente: el texto que
  corregia ya no existe); reescribir las tres afirmaciones sin dejar constancia de que fueron falsas
  (convierte «falta evidencia» en «hay evidencia falsa», que es peor y ya nadie lo notaria);
  corregir el hash en la bitacora de `S-008` (no tiene objeto — ahi el `ae06147` que aparece es el
  correcto, el `HEAD` contra el que se verificaron los hallazgos).
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — es un
  cambio de estado y unas lineas de redaccion dentro del registro, todo en control de versiones, y
  se deshace con otra entrada.

**Verificacion — la cadena no sobrevive en ningun sitio del archivo, y por eso no hay nada que
corregir en su sitio:**

```
$ git show 99c3aa3:_persistence/progress.md | grep -o 'R-007` (sobre `[0-9a-f]*`)' ; echo "exit=$?"
exit=1

$ git show 99c3aa3:_persistence/progress.md | grep -c 'ae06147'
5

$ git show 99c3aa3:_persistence/progress.md | grep -n 'ae06147' | cut -c1-100
63:| Avance de la etapa | `R-008` (sobre `f096fff`) abrio `F-020`, `F-021`, `F-022` y `F-023`. `mana
75:commit que la propia bitacora de `S-008` atribuia a `R-007` —`ae06147`, que es el commit que
77:`ae06147` de la misma celda, el `HEAD` contra el que se verificaron los hallazgos, no se toca.
381:  `F-018`, `F-019`), verifico cada uno contra `HEAD` (`ae06147`) y los acepto los tres. `T-023`
413:  `ae06147`— con nota fechada. `T-029` no reescribe los tres bloques de verificacion de
```

Cinco menciones vivas de `ae06147`, y no todas son el mismo caso:

| Linea | Que dice | Que se hace |
|---|---|---|
| 63 | la celda de la seccion 1, que afirma la nota fechada | se ajusta en su sitio (`D-027`) |
| 75 y 77 | la seccion 2, que afirma lo mismo | se ajusta en su sitio (`D-027`) |
| 381 | la bitacora de `S-008`: el `HEAD` contra el que se verificaron los hallazgos | **correcta, no se toca** |
| 413 | la bitacora de `S-009`, que afirma la nota fechada | **historica: nota fechada al lado, sin reescribirla** |

---

### D-051 - `_workflow/` gana un archivo por etapa, y ese archivo es el cuarto enganche

| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** `D-046` creo `_workflow/` con dos archivos de doctrina —`team.md`, que dice quien
  hace que, y `ai_levels.md`, que dice cuanto sistema pide el trabajo—. Los dos son generales por
  diseño: ninguno baja a las actividades concretas de una etapa. `L-014` y `DT-002` señalaron el
  hueco por el otro lado: la carpeta nacio sin **enganche de uso**, nada mandaba abrirla.
- **Decision:** `_workflow/` gana **un archivo por etapa declarada**, con el mismo nombre que la
  etapa, que aplica `team.md` y `ai_levels.md` a las actividades de su procedimiento — una fila por
  paso, ni una mas. El primero es `_workflow/005_discovery.md`. Y **`_phases/<etapa>.md` lo manda
  leer antes del Paso 1 de su procedimiento**, que es el momento de entrada que `team.md` §8 ya
  fijaba.
- **Por que un archivo por etapa y no una seccion dentro de `team.md`:** `team.md` es doctrina
  agnostica de metodo y no conoce los pasos de ninguna etapa; meterle siete filas de una etapa
  concreta lo ataria a ella y romperia la frontera que `D-049` acaba de fijar. Un archivo por etapa
  se copia, se borra o se reescribe con su etapa, sin tocar la doctrina.
- **Por que esto paga la deuda `DT-002`:** el cuarto enganche de `L-014` es «algo que mande leerla
  en el momento en que sirve». Ahora existe y **tiene control**: la verificacion de §8 del archivo
  nuevo incluye `grep -n "_workflow/005_discovery" _phases/005_discovery.md`, asi que el archivo no
  se da por terminado hasta que la etapa lo cita. La cadena completa es `_phases/` → archivo de
  etapa de `_workflow/` → `team.md` y `ai_levels.md`. ⚠️ **`DT-002` no se marca `Implementada`
  aqui:** su estado es `Propuesta (pendiente del usuario)` y el que confirma una deuda es el usuario.
- **Que arrastra, y se hace en la misma pasada:** la fila de `_workflow/` en «Carpetas propias» de
  `project.md` y el parrafo de `CLAUDE.md` describian una carpeta de exactamente dos archivos. Los
  dos se amplian; el de `CLAUDE.md` gana ademas la distincion que el archivo nuevo obliga a decir
  —**lo que un participante puede hacer** vive en `_workflow/`, **lo que el proyecto adopta** vive en
  `decisions.md`—.
- **Alternativas descartadas:** dejar el reparto de cada etapa solo en `decisions.md` (obligaria a
  rehacer el analisis entero en cada proyecto, que es justo lo que un metodo agnostico existe para
  evitar); meterlo dentro del archivo de `_phases/` (mezcla «que hay que hacer» con «quien lo hace»,
  las dos cosas que `team.md` separa expresamente, y engorda un archivo que ya es largo); enganchar
  `team.md` y `ai_levels.md` directamente desde `_phases/` sin archivo intermedio (manda leer
  doctrina general en el momento de ejecutar, que es cuando menos se lee, y deja el trabajo de
  aplicarla sin hacer y sin registrar).
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — es un
  archivo nuevo y dos parrafos ampliados, todo en control de versiones y sin nada publicado fuera.

**Verificacion — el archivo existe con sus siete filas, la etapa lo cita, y sigue siendo agnostico:**

```
$ grep -c "^| \*\*[1-7] · " _workflow/005_discovery.md
7

$ grep -n "_workflow/005_discovery" _phases/005_discovery.md
117:**`_workflow/005_discovery.md`**, que se lee ahora y no despues. Ese reparto se adopta con su

$ grep -rnE "RaindomAI|RaidomAI|Proyectos_TripleS|github\.com|jdrodriguez|USUARIO" .claude CLAUDE.md _phases _methodology _templates _workflow ; echo "exit=$?"
exit=1

$ grep -rniE "triple ?s|raindom|raidom|_brief" _workflow ; echo "exit=$?"
exit=1
```

---

### D-052 - El reparto de `005_discovery` no se adopta todavia: se adopta al abrir la etapa

| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | manager |

- **Contexto:** `_workflow/005_discovery.md` queda escrito, y `team.md` §8 manda que el reparto de
  una etapa se registre con su `D-XXX`. Es tentador escribir ese `D-XXX` ahora, con el archivo
  recien hecho y el razonamiento fresco.
- **Decision:** **no se escribe.** El proyecto sigue en `000_preproject`; `005_discovery` no esta
  abierta y `team.md` §8 fija el momento de entrada con precision: **al abrir la etapa, despues de
  leer su archivo de `_phases/` y antes del primer paso de su procedimiento.** El `D-XXX` de
  adopcion se escribe entonces, y no antes.
- **Por que importa la diferencia:** un reparto adoptado hoy diria que hace este proyecto con unas
  actividades que todavia no ha empezado, y quedaria escrito **antes** de conocer las dos entradas
  que `_phases/005_discovery.md` §3.3 exige —una necesidad expresada y acceso a quien pueda hablar
  del proceso real—. Ese acceso es hoy `A-004`, sin confirmar. Un reparto que da por hecho un acceso
  que no existe reparte trabajo que quiza no se pueda hacer.
- **Que queda pendiente para ese momento, y se escribe aqui para que no se pierda:** al abrir la
  etapa hay que registrar (1) el reparto adoptado con lo descartado, (2) la **discrepancia de §6**
  del archivo nuevo con la tabla de lectura de `ai_levels.md` §6 —variabilidad en `3` no lleva a
  nivel 5 aqui, y el propio `ai_levels.md` pide que la discrepancia se registre—, y (3) los `A-XXX`
  que el reparto de por ciertos sin confirmar.
- **Alternativas descartadas:** adoptarlo ahora (rompe el momento de entrada de `team.md` §8 y
  reparte sobre entradas que no existen); no dejar nada escrito y confiar en acordarse al abrir la
  etapa (es exactamente lo que `CLAUDE.md` llama registrar al final: lo acumulado se pierde).
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — es
  aplazar una escritura en el registro; adelantarla o retrasarla no consume nada.

**Verificacion — la etapa declarada sigue siendo la preparatoria, y el acceso sigue sin confirmar:**

```
$ grep -n "^| Etapa actual" _persistence/progress.md
60:| Etapa actual | `000_preproject` |

$ grep -n "^### A-004" _persistence/assumptions.md
220:### A-004 - Existe acceso al patrocinador y a personas que puedan hablar del proceso real

$ sed -n '/^### A-004/,/^### A-005/p' _persistence/assumptions.md | grep -n "^| Estado |"
5:| Estado | Abierto |
```

---

### D-053 - `global_lessons.md` nace en `TripleS_Lessons/` dentro de este repositorio, de forma transitoria

| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** el usuario aporto en `temporal/` dos archivos de un proyecto anterior:
  `lessons-global.md` (98 lecciones transversales, v2, destiladas de `Edu_TripleS` y
  `AIzar_Auditor`) y `work-with-lessons-global.md` (una propuesta de integracion redactada por una
  instancia anterior de este mismo proyecto, que nunca llego al registro). El objetivo que el
  usuario enuncio no es auditar con ellas: es **poder usar lo aprendido en un proyecto al abrir el
  siguiente**.
- **Decision:** el archivo se construye como `TripleS_Lessons/global_lessons.md`, **dentro de este
  repositorio y de forma transitoria**, con las 98 lecciones importadas y una capa de navegacion
  nueva. El original definitivo vivira en un repositorio propio, y **donde se crea ese repositorio
  esta pendiente de acordar con el usuario**, que lo dejo explicitamente como paso siguiente.
- **Por que aqui y no en `_methodology/`:** `_methodology/` es una de las seis carpetas que tienen
  que poder copiarse tal cual a otro proyecto. Meter ahi el archivo lo convertiria en **una copia
  por proyecto**, que es exactamente la forma de distribucion que hace divergir el material
  compartido: hoy ya hay dos origenes distintos (`Edu_TripleS` dio la v1, `AIzar_Auditor` la v2) y
  cuatro proyectos en disco. Una carpeta aparte deja claro que esto es un **invitado en transito**,
  no material de este proyecto.
- **Que se hizo con el contenido, y esta es la frontera:** la **capa de navegacion es nueva**
  —cabecera, «Como se busca aqui», y los indices §1 por momento de trabajo, §2 por sintoma y §3 por
  bloque—; **las 98 lecciones y las tres secciones finales se importaron literales**, sin tocar una
  coma. Nada del contenido heredado se reescribio.
- **Por que no se adapto el contenido:** adaptar es una pasada aparte, con sus propias decisiones
  (el Bloque H describe un montaje de dos terminales que no es el nuestro; la seccion «Uso en
  auditoria» dice «los nueve» bloques cuando son diez y usa codigos `H-NN` de otro proyecto). Hacerlo
  en la misma pasada que la importacion mezclaria «lo que vino» con «lo que cambiamos», y entonces
  no habria forma de contrastar el archivo contra su origen.
- **Alternativas descartadas:** (1) meterlo en `_methodology/` ahora —es lo que proponia
  `work-with-lessons-global.md`, y produce N copias divergentes, que es `LG-98` del propio archivo—;
  (2) crear ya el repositorio aparte —el usuario pidio expresamente detenerse antes de eso—;
  (3) dejarlo en `temporal/` —`project.md` declara esa carpeta fuera del repositorio y prohibida a
  los protocolos, asi que ahi el archivo no existe para el proyecto.
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — es
  crear una carpeta y un archivo nuevos en un repositorio con historia; mover la carpeta o borrarla
  no destruye nada, porque el original sigue en `temporal/` y el destino final esta por decidir.
- **Que queda pendiente:** acordar donde vive el repositorio propio, crearlo con su `git` y
  enlazarlo a GitHub; y **despues** la pasada de adaptacion del contenido.

**Verificacion — el archivo existe, las 98 lecciones estan completas y sin duplicados, y el cuerpo
importado es identico al de origen:**

```
$ grep -oE "^\| \*\*LG-[0-9]+" TripleS_Lessons/global_lessons.md | grep -oE "LG-[0-9]+" > /tmp/got.txt
$ wc -l < /tmp/got.txt ; sort -u /tmp/got.txt | wc -l
98
98

$ for i in $(seq -w 1 98); do echo "LG-$i"; done > /tmp/want.txt
$ diff <(sort /tmp/want.txt) <(sort /tmp/got.txt) ; echo "exit=$?"
exit=0

$ diff <(sed -n '43,297p' temporal/lessons-global.md) \
       <(sed -n '/^## Los seis principios raíz$/,$p' TripleS_Lessons/global_lessons.md) ; echo "exit=$?"
exit=0
```

⚠️ **La tercera orden no se podra reproducir desde el repositorio**, y se escribe sabiendolo:
`temporal/` esta excluida por `.gitignore`, asi que el archivo de origen no queda versionado. Es la
razon por la que las dos primeras ordenes —que si son reproducibles sobre el arbol— van al lado.

📌 **Nota del 2026-09-02: la condicion que esta decision dejo abierta ya se cumplio.** El
repositorio propio existe, es privado, y `global_lessons.md` esta subido en el. En consecuencia
`TripleS_Lessons/` **se borra de este repositorio** y su fila sale de «Carpetas propias» de
`project.md`. El texto de arriba no se reescribe (`D-019`): describe lo que era cierto cuando se
tomo la decision.

- **Donde vive ahora:** `C:\Users\USUARIO\Documents\Company_TripleS\TripleS_Lessons`, enlazado a
  `https://github.com/jdrodriguez1000/TripleS_Lessons.git`.
- **Visibilidad:** el repositorio remoto se creo **publico**. Antes de subir nada se paso a
  **privado** por decision del usuario, porque el archivo lleva nombres de proyectos internos como
  marca de procedencia (`Edu_TripleS`, `AIzar_Auditor`, `RandomAI`) y describe fallos concretos de
  esos proyectos. La procedencia se conserva: es lo que permite volver al caso real de cada leccion.
- **La carpeta nunca llego a estar versionada aqui:** se creo y se borro dentro de la misma sesion,
  sin pasar por ningun commit. Por eso su fila de `project.md` se borra en vez de anotarse.

**Verificacion — el archivo esta en el remoto con las 98 lecciones, la copia borrada era identica a
la subida, y el repositorio es privado:**

```
$ git -C <ruta del repo nuevo> ls-tree -r --name-only origin/main
global_lessons.md
$ git -C <ruta del repo nuevo> show origin/main:global_lessons.md | grep -c "^| \*\*LG-"
98

$ diff <(git -C <ruta del repo nuevo> show origin/main:global_lessons.md) TripleS_Lessons/global_lessons.md ; echo "exit=$?"
exit=0

$ gh repo view jdrodriguez1000/TripleS_Lessons --json visibility,isEmpty,defaultBranchRef,pushedAt
{"defaultBranchRef":{"name":"main"},"isEmpty":false,"pushedAt":"2026-09-02T13:48:18Z","visibility":"PRIVATE"}
```

⚠️ **Las tres primeras ordenes se corrieron antes de borrar la carpeta y no se pueden reproducir
desde este repositorio**, y se escriben sabiendolo: el `diff` compara contra un archivo que esta
decision manda borrar, y el repositorio nuevo no es este. La cuarta si es reproducible.

🚨 **La ruta absoluta y el host del remoto se escriben con hueco a proposito.** `project.md` es el
unico sitio donde van los datos propios, y esta decision vive en `_persistence/`; ademas el
repositorio nuevo no es una carpeta de este proyecto, asi que no le toca fila en «Carpetas propias».
Los datos concretos estan en el cuerpo de esta nota, que es prosa del registro, no un control.

---

### D-054 - Se consultan los bloques D y E de `global_lessons.md` antes de abrir `005_discovery`

| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | manager |

- **Contexto:** `global_lessons.md` vive en un repositorio propio y externo (`D-053`). De sus tres
  usos —arranque, guia y vara de auditoria— los dos primeros **no exigen traer el archivo al
  proyecto**: se consulta en su ruta y lo que aterriza aqui es la decision que cambio. El tercero si
  lo exigira, porque `report_auditor` arranca en frio y solo lee este repositorio.
- **Decision:** se consultan **los bloques D (`LG-38`–`LG-45`) y E (`LG-46`–`LG-54`)**, 17 lecciones,
  antes de abrir `005_discovery`. **No se baja ninguna copia** al proyecto.
- **Por que ahora y no despues:** `LG-39` dice que las decisiones de arquitectura se toman con la
  menor cantidad de informacion que se va a tener en todo el proyecto, y `005_discovery` es donde se
  define alcance y objetivo. Leidas despues, estas lecciones confirman lo ya decidido en vez de
  informarlo — que es `LG-40`: si el documento no cambia nada, no lo estabas usando, lo estabas
  obedeciendo.
- **La vara queda anclada**, para que esta lectura se pueda repetir contra lo mismo:
  `TripleS_Lessons` v2, commit `fa03813`.

**Lo que la lectura produjo — seis lecciones muerden, dos ya estaban cubiertas:**

| Leccion | Que señala aqui | Donde queda |
|---|---|---|
| `LG-38` | **no existe la lista de lo irreversible** del proyecto, y `CLAUDE.md` ya lo sabe: parchea su ausencia obligando a declarar la clasificacion en cada respuesta | **`T-037`** |
| `LG-39` | el brief §23 aplaza **dos puertas de una via**: tecnologia/runtime (#1) y tipo de base de datos (#2). `LG-39` las pone en la lista de «decide ahora» | `005_discovery` |
| `LG-48` | el brief §20 es una **lista de alcance de 14 viñetas en orden de flujo**, no un MVP. Sin MVP definido antes, los cortes salen feature por feature y no en diagonal | `005_discovery` |
| `LG-54` | **evaluacion, observabilidad y seguridad no tienen dueño ni sitio.** No se construyen hoy: se les asigna. El dia 1 es ahora | `005_discovery` |
| `LG-47` + `LG-52` | el **walking skeleton** de este producto es traer un sorteo real de la fuente, guardarlo y mostrarlo — que es exactamente `A-003`. Y `LG-52` añade que un supuesto es algo que hay que **averiguar**, no construir: `A-003` no depende de `A-004` | **`T-003`**, ya existente |
| `LG-45` | las tres formulas que el brief §23 aplaza (#6 intervalo promedio, #7 proxima aparicion, #8 «estadisticamente esperado») son **numeros derivados**, y un numero derivado se lee como un hecho de la naturaleza. El «indicador estadistico» del §9 es el caso literal | `005_discovery` |

**Lo que salio limpio, y se dice para no declararlo por omision:** `LG-42` (decision con su porque,
fechada y reversable) esta cubierto por `decisions.md`, que hace mas de lo que la leccion pide; y
`LG-51` (criterio de cierre escrito antes) esta cubierto por la convencion de `tasks.md`.

**Lo que no se evaluo y por que:** `LG-41`, `LG-43`, `LG-46`, `LG-49`, `LG-50` y `LG-53` aplican
cuando exista codigo, despliegue o un plan cortado en trozos. Nada de eso existe. **No se declaran
limpias: se declaran NO MIRADAS** (`LG-85`).

- **Que NO decide esta entrada:** las cinco filas que caen en `005_discovery` son de producto y de
  alcance, y las decide el usuario al abrir la etapa. Aqui quedan **registradas para que no se
  pierdan**, no adoptadas.
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — es leer
  un archivo externo y registrar lo que produjo; no consume nada ni cierra ninguna puerta.

**Verificacion — la vara consultada existe, esta anclada, y los dos bloques suman las 17 lecciones
que esta entrada dice haber recorrido:**

```
$ git -C <ruta de TripleS_Lessons> log -1 --format="%h"
fa03813

$ git -C <ruta de TripleS_Lessons> show fa03813:global_lessons.md | grep -n "^> \*\*Versión"
26:> **Versión: 2 · 2026-08-28** · 98 lecciones · 10 bloques

$ git -C <ruta de TripleS_Lessons> show fa03813:global_lessons.md \
  | awk '/^## Bloque [DE] /{b=1} /^## Bloque F/{b=0} /^\| \*\*LG-/{if(b)n++} END{print n}'
17
```

⚠️ **Las tres ordenes se corren contra un repositorio que no es este**, y por eso llevan la ruta
como hueco: el dato propio vive en `project.md`, y ese repositorio no es una carpeta de este
proyecto. Quien las repita necesita el repositorio externo delante; el ancla `fa03813` es lo que
garantiza que lea la misma vara y no una posterior (`LG-95`).

---

### D-055 - El puntero a las lecciones globales: la regla en `CLAUDE.md`, el donde en `project.md`, el control en la etapa

| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** `D-053` dejo las lecciones globales en un repositorio externo y `D-054` las consulto
  por primera vez. Pero nada en este repositorio mandaba consultarlas: funciono porque el usuario y
  `manager` estaban en la conversacion. En el proyecto siguiente no habria conversacion, y el
  mecanismo no se dispararia. Es `L-014` exacta: **el cuarto enganche —algo que mande leerla— es el
  que se olvida**, y es el unico que no tiene ningun control que detecte su ausencia.
- **Decision:** el puntero se construye en **tres piezas**, y ninguna sirve sin las otras dos:

| Pieza | Donde | Que lleva |
|---|---|---|
| **La regla** | `CLAUDE.md`, seccion «Las lecciones globales» | que existen, los tres usos, cual exige copia y cual no, que aterriza en el proyecto, y que no se lee entero |
| **El donde** | `project.md`, tabla «Rutas» | las tres filas con el repositorio, el archivo y el remoto |
| **El control** | `_phases/000_preproject.md` §6 | una casilla en la condicion de salida: la consulta de arranque hecha y **registrada** |

- **Por que partido en tres y no en uno:** `CLAUDE.md` y `_phases/` **tienen que poder copiarse tal
  cual a otro proyecto**, y el Paso 1b lo comprueba en cada cierre. Si la regla llevara dentro la
  ruta o el remoto, la copia llegaria al proyecto siguiente apuntando al disco de esta maquina. Por
  eso la regla se escribe sin un solo dato propio y el dato vive donde vive todo lo propio.
- **Por que hacen falta la regla y el control, y no basta uno:** son enganches distintos. La regla es
  **de uso** —dispara la lectura en el momento en que sirve—; la casilla es **de control** —detecta
  que no se hizo—. `L-014` señala justo que los enganches de control no sustituyen al de uso: una
  casilla sin regla avisa tarde, y una regla sin casilla se salta en silencio.
- **Que NO se construyo, y es deliberado:** el disparador de la **cosecha** —el camino de vuelta,
  que sube lo aprendido al original al cerrar una etapa—. La regla de `CLAUDE.md` lo enuncia, pero
  **no tiene todavia su casilla** en ninguna condicion de salida. Queda como el mismo hueco que esta
  decision acaba de tapar en la otra direccion, y se dice aqui para que no se descubra tarde.
- **Alternativas descartadas:** (1) escribir la ruta dentro de `CLAUDE.md` —rompe el Paso 1b y viaja
  rota—; (2) solo la casilla de la condicion de salida —avisa cuando ya se decidio el alcance, que
  es cuando la lectura ya no informa nada (`LG-40`)—; (3) solo la regla —se salta sin que nada lo
  note, que es el defecto original—; (4) un archivo nuevo en `_methodology/` que explique todo esto
  —cuesta los cuatro enganches otra vez, para decir lo que cabe en una seccion.
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — son
  tres bloques de texto en archivos versionados; quitarlos es un `git revert`.

**Verificacion — las tres piezas existen, y lo copiable sigue sin datos propios:**

```
$ grep -c "^## Las lecciones globales$" CLAUDE.md
1
$ grep -c "consulta de arranque a las lecciones globales" _phases/000_preproject.md
1
$ grep -c "^| Lecciones globales" project.md
3

$ grep -rnE "RaindomAI|RaidomAI|Proyectos_TripleS|github\.com" .claude CLAUDE.md _phases _methodology _templates _workflow ; echo "exit=$?"
exit=1
```

⚠️ **Las tres primeras ordenes van acotadas cada una a su archivo a proposito**, y ninguna a
`_persistence/`: si se corrieran sobre el arbol entero, esta misma entrada —que nombra las tres
piezas— se contaria a si misma y los numeros dirian otra cosa en cuanto el cierre la commitee. Es
`L-010`, y es el defecto que `F-027` acaba de señalar por quinta vez.

📌 **La cuarta orden es el Paso 1b de `protocol-close` corrido sobre el arbol de trabajo**, con los
tres valores que `project.md` declara para el —nombre del proyecto, carpeta raiz de las rutas
absolutas y host del remoto—, mas la grafia `RaidomAI` de la carpeta en disco. Cero lineas es lo
correcto: ninguna de las dos ediciones en lo copiable metio un dato de este proyecto.

---

### D-056 - La cosecha gana disparador: una casilla por etapa, y la columna `Portabilidad` que la hace comprobable

| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** `D-055` construyo el camino de ida —algo que manda leer las lecciones globales— y
  dejo escrito que el de vuelta seguia sin disparador: la **cosecha**, que sube al archivo global lo
  que este proyecto aprendio. La regla de `CLAUDE.md` la enunciaba, pero ninguna condicion de salida
  la exigia, que es la definicion exacta de `L-008` — una regla sin mecanismo que la aplique.
- **Decision:** dos piezas, y la segunda no es un extra:

| Pieza | Donde | Que hace |
|---|---|---|
| **La casilla** | condicion de salida de **cada etapa declarada** | dispara la cosecha al cerrar la etapa, y bloquea el cierre si no se hizo |
| **La columna `Portabilidad`** | indice de `_persistence/lessons.md` | registra el resultado por leccion, y es **lo que hace la casilla comprobable** |

- **Por que la columna no es opcional:** sin ella la casilla dice «cada `L-XXX` paso por los cuatro
  filtros» y **no hay forma de comprobarlo**. Seria una casilla que se marca por memoria, que es un
  veredicto disfrazado de control (`PI-5`: lo que no se puede comprobar no esta hecho, esta
  afirmado). Con la columna, la comprobacion es un barrido: si queda un `Sin evaluar` de esa etapa,
  la casilla es falsa.
- **Por que la columna va en el indice y no en la ficha:** un estado escrito en dos sitios acaba
  diciendo dos cosas y nadie sabe cual manda —es `L-003` aplicada a un campo—. Y la cosecha es un
  barrido de una columna, no una relectura de quince fichas: el indice es el sitio donde eso cuesta
  un vistazo.
- **Por que los cuatro filtros no se copian aqui:** viven en el archivo global, en su seccion de
  promocion. Copiarlos a `lessons.md` crearia una segunda copia que envejeceria por su cuenta,
  exactamente el defecto que `D-053` evito al no meter el archivo entero en `_methodology/`.
- **La duplicacion entre etapas es deliberada:** la misma casilla queda en los dos archivos de
  `_phases/`. Lo que se duplica es **un puntero, no la regla** —la regla vive en `CLAUDE.md`—, y es
  el mismo patron que el repositorio ya usa con `project.md`. Una casilla por etapa es lo que hace
  que la cosecha ocurra **en cada cierre de etapa** y no una sola vez en la vida del proyecto.
- **Lo que esto cuesta, dicho antes:** `000_preproject` gana una condicion de salida **estando cerca
  de cerrar**, y hoy sus quince lecciones estan las quince `Sin evaluar`. La etapa no puede cerrar
  hasta que se cosechen. Es deliberado: la alternativa es cerrarla sin cosechar, y entonces lo
  aprendido en la primera etapa del primer proyecto no llega a ningun sitio — que es justo lo que
  este mecanismo existe para impedir.
- **Alternativas descartadas:** (1) una sola casilla, al cerrar el proyecto —la cosecha se haria una
  vez, sobre un `lessons.md` enorme y frio, que es cuando peor se distingue la forma del fallo de la
  anecdota—; (2) la casilla sin la columna —no comprobable—; (3) la columna sin la casilla —nadie la
  rellenaria nunca, que es el punto de partida de esta decision—; (4) un campo dentro de cada ficha
  ademas del indice —dos sitios para el mismo estado.
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — son dos
  casillas y una columna en archivos versionados.

**Verificacion — las casillas existen en las dos etapas, los recuentos en prosa cuadran con ellas, y
las quince lecciones tienen la columna:**

```
$ grep -c "La cosecha esta hecha" _phases/000_preproject.md _phases/005_discovery.md
_phases/000_preproject.md:1
_phases/005_discovery.md:1

$ for f in _phases/000_preproject.md _phases/005_discovery.md; do
    echo -n "$f: "; sed -n '/^## 6\. Condicion de salida/,/^## 7\./p' $f | grep -c "^- \[ \]"
  done
_phases/000_preproject.md: 8
_phases/005_discovery.md: 7

$ grep -nE "las (seis|siete|ocho) son ciertas|Ninguna de las (seis|siete|ocho)" _phases/000_preproject.md _phases/005_discovery.md
_phases/000_preproject.md:155:La etapa termina cuando **las ocho son ciertas**. Las cinco primeras son el espejo de los cinco
_phases/000_preproject.md:184:🔑 **Ninguna de las ocho habla del producto**, y ahi esta el criterio entero de la etapa: se sale de
_phases/005_discovery.md:264:La etapa termina cuando **las siete son ciertas**:
_phases/005_discovery.md:286:⚠️ **Ninguna de las siete exige que exista la etapa siguiente.** Cual sea se declara dentro de esta

$ sed -n '/^## Indice/,/^---/p' _persistence/lessons.md | grep -c "| Sin evaluar |$"
15

$ grep -rnE "RaindomAI|RaidomAI|Proyectos_TripleS|github\.com" .claude CLAUDE.md _phases _methodology _templates _workflow ; echo "exit=$?"
exit=1
```

⚠️ **La tercera orden se escribe con su numero de linea sabiendo que caducara.** Los cuatro
recuentos se comprobaron aqui **contra el numero de casillas de la orden anterior**, que es lo que
importa: `8` casillas y «las ocho», `7` casillas y «las siete». Si una edicion posterior mueve las
lineas, lo que hay que rehacer es la comparacion, no buscar estos numeros.

📌 **Ninguna orden se corre sobre `_persistence/decisions.md`, y es a proposito:** esta misma entrada
nombra las casillas y la columna, y un barrido sin acotar se contaria a si mismo (`L-010`, el defecto
que `F-027` señalo por quinta vez).

📌 **Nota del 2026-09-02 (`T-041`, hallazgo `F-031`).** El bloque de arriba **se deja tal cual se
ejecuto** (`D-019`). Lo que no se sostiene son su cuarta orden y la prosa que la acompaña: la cifra
`15` se obtuvo sobre el arbol de trabajo **antes** de que la propia sesion añadiera `L-016` y
`L-017`, asi que sobre el commit que publica esta entrada el recuento es `17` — y no `15`. La frase
«hoy sus quince lecciones estan las quince `Sin evaluar`» debe leerse **«sus diecisiete lecciones
estan las diecisiete `Sin evaluar`»**, y el titulo del bloque, «las diecisiete lecciones tienen la
columna». Nada de lo que la decision decide cambia: el volumen que bloquea la condicion de salida de
`000_preproject` es mayor del que se escribio, no menor.

**Verificacion — el recuento anclado al commit que contiene la entrada, y a `HEAD`:**

```
$ git show 2a2d3b6:_persistence/lessons.md | sed -n '/^## Indice/,/^---/p' | grep -c "| Sin evaluar |$"
17

$ git show f1f3fea:_persistence/lessons.md | sed -n '/^## Indice/,/^---/p' | grep -c "| Sin evaluar |$"
17
```

---

### D-057 - No nace un quinto estado de tarea: `Pendiente` se normaliza a `No implementada`
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | report_auditor |

- **Contexto:** `F-029` (`R-011`) encontro que `T-037` y `T-038` nacieron con el
  estado `Pendiente`, valor que la tabla de convenciones de `tasks.md` no declara. El hallazgo se
  acepta: el archivo declara cuatro valores de `Estado` y esas dos fichas usan un quinto, en la
  ficha y en el indice. Cualquier barrido que filtre por los cuatro validos las deja fuera.
- **Decision:** **no se declara un quinto estado.** Las dos fichas y sus filas del indice pasan a
  `No implementada`, que es el valor que ya usan `T-001`, `T-002` y `T-003` para exactamente lo
  mismo: una tarea escrita y todavia sin hacer.
- **Por que:** `Pendiente` y `No implementada` no distinguen nada. Un estado existe para separar
  dos situaciones que hay que tratar distinto, y aqui no hay dos: `T-037` y `T-038` estan en el
  mismo sitio que `T-001`. Anadir el valor obligaria ademas a explicar en que se diferencia de
  `No implementada`, y no hay respuesta — que es la senal de que el valor sobra (`PI-2`).
- **Alternativas descartadas:** (1) declarar `Pendiente` en la tabla con su `D-XXX` —duplica un
  estado existente y obliga a todo barrido futuro a filtrar por cinco valores donde cuatro
  bastan—; (2) dejarlo y anotarlo —el archivo seguiria declarando cuatro valores y usando cinco,
  que es el defecto entero del hallazgo.
- **Por que esto no es reescribir historia:** el `Estado` de una tarea es un **campo vivo**, no un
  bloque de verificacion. `D-019` rige sobre lo que registra una ejecucion pasada; un estado
  registra la situacion de hoy y se actualiza por definicion. La constancia de que nacieron con
  otro valor queda en `F-029`, en esta decision y en la bitacora de `S-011`, que no se tocan.
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — son
  cuatro celdas de texto en un archivo versionado.

**Verificacion — antes de tocar, los dos valores fuera de la convencion sobre `HEAD` (`f1f3fea`):**

```
$ git grep -nE '^\| Estado \| ' f1f3fea -- _persistence/tasks.md | grep -vE 'Implementada|No implementada|Cancelada|Suspendida'
f1f3fea:_persistence/tasks.md:1598:| Estado | Pendiente |
f1f3fea:_persistence/tasks.md:1651:| Estado | Pendiente |

$ git show f1f3fea:_persistence/tasks.md | sed -n '/^## Indice/,/^---/p' | grep -c "| Pendiente |"
2
```

---

### D-058 - `T-038` se regulariza declarando que nacio fuera de las dos excepciones
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | report_auditor |

- **Contexto:** `F-030` (`R-011`) encontro que `T-038` se escribio a mano en `tasks.md` sin citar
  el `D-XXX` ni el `F-NNN` que las dos excepciones de la convencion exigen. El hallazgo se acepta.
- **Que paso de verdad, y conviene escribirlo sin adornarlo:** `T-038` **no entra por ninguna de
  las dos excepciones**. No nace de aceptar un hallazgo (`D-020`) ni de una decision ya registrada
  que el cierre no pueda deducir del diff (`D-025`): nace de que `manager`, leyendo `R-010`, se dio
  cuenta de que el barrido de fuga de `protocol-audit` cubre menos carpetas que el de
  `protocol-close`. Es una observacion propia, y la convencion no la contempla.
- **Decision:** **esta entrada es el respaldo que faltaba.** `T-038` la cita, y con eso queda
  auditable. No se amplia la convencion con una tercera excepcion.
- **Por que no una tercera excepcion:** el camino normal para una observacion propia ya existe y es
  el cierre — `session-closer` escribe `tasks.md`, y una observacion de `manager` llega ahi por la
  conversacion de la jornada. Abrir una excepcion «cuando a `manager` se le ocurre algo» convierte
  las dos excepciones en una puerta, que es literalmente lo que la convencion advierte.
- **Que hacer la proxima vez:** una observacion propia que no se quiera perder se registra **como
  decision primero** —esta misma forma— y la tarea la cita; o se deja para el cierre. Lo que no se
  puede es escribir la tarea suelta.
- **Alternativas descartadas:** (1) borrar `T-038` y esperar al cierre —perderia el hueco, que es
  real y sigue abierto—; (2) citar `D-054` como si hubiera nacido de la consulta a las lecciones
  globales —seria falso: nacio de leer `R-010`—; (3) declarar una tercera excepcion.
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio — es texto en un archivo
  versionado.

**Verificacion — sobre `HEAD` (`f1f3fea`), `T-038` no cita ninguno de los dos y `T-037` si:**

```
$ git show f1f3fea:_persistence/tasks.md | awk '/^### T-038 /,0' | grep -oE '`(D|F)-[0-9]+`' | sort -u
(sin salida)

$ git show f1f3fea:_persistence/tasks.md | awk '/^### T-037 /,/^### T-038 /' | grep -oE '`D-[0-9]+`' | sort -u
`D-054`
```


---

### D-059 - El prototipo descartable es la unica excepcion a `PI-5`, y se declara en el archivo de etapa
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** al adaptar el archivo de etapa del prototipo aparecio un choque frontal entre dos
  reglas vigentes. `CLAUDE.md` (`PI-5`) fija que una tarea que produce **codigo ejecutable** esta
  Terminada cuando **un test automatizado pasa en verde**, y anade que «no hay una tercera casilla».
  La guia de metodo, en cambio, define el prototipo como **descartable** y el archivo fuente prohibia
  los tests con un argumento correcto: un test protege lo que se va a conservar.
- **Decision:** se declara **una excepcion explicita y acotada**. El prototipo —el artefacto
  descartable del camino feliz— tiene como Definicion de Terminado **la evidencia registrada de las
  sesiones** (un archivo por sesion, con estado, bloqueos y comentarios) en vez de un test en verde.
  La excepcion queda escrita **en el propio archivo de etapa**, con su alcance y su limite.
- **Por que declararla en vez de resolverla en un sentido o en otro:** exigir tests encarece
  justamente la etapa que existe para ser barata, y ademas hace mas dificil tirar el artefacto —lo
  que un test protege, alguien lo quiere conservar—. Prohibirlos sin decir nada dejaria a `PI-5`
  contradicho en silencio, y la primera auditoria que leyera los dos archivos lo encontraria, con
  razon. **Una excepcion escrita se puede discutir; una excepcion tacita solo se puede descubrir.**
- **Por que no vacia `PI-5`:** el principio exige que nada se de por hecho sin algo que lo
  compruebe, y aqui lo hay — el comportamiento de usuarios reales frente a una tarea, registrado
  mientras ocurre. **Cambia el instrumento, no la exigencia:** un prototipo sin sesiones registradas
  no esta Terminado.
- **Su limite, que es la mitad de la decision:** la excepcion alcanza **al artefacto descartable y a
  nada mas**. No se extiende «al codigo de esa etapa» ni «a lo que sea rapido», y deja de aplicar en
  el instante en que el artefacto deja de ser descartable.
- **Alternativas descartadas:** (1) exigir tests de humo minimos —respeta `PI-5` sin excepciones,
  pero contradice al metodo y encarece la etapa—; (2) escribir el archivo prohibiendo tests sin
  mencionar `PI-5` —deja viva la contradiccion y sin registrar—; (3) reescribir `PI-5` en
  `CLAUDE.md` para admitir un tercer caso —tocaria una regla que gobierna todas las etapas para
  resolver el caso de una sola.
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — es
  texto en archivos versionados, y la etapa que regula ni siquiera esta adoptada todavia.

**Verificacion — la excepcion esta escrita en el archivo de etapa, con su alcance y su limite:**

```
$ grep -c "La excepcion a .PI-5.\|La excepcion cubre el prototipo y nada mas" _phases/010_prototype.md
2
```

⚠️ **La orden se escribio primero con `-n` y publico las lineas `92` y `111`; ediciones posteriores
de la misma sesion las movieron a `98` y `117`.** Se cambia a `-c` antes de commitear: lo que la
decision afirma es que **las dos frases existen**, y para eso el numero de linea no aporta nada y
caduca solo. Es `L-013` aplicada antes de que se convirtiera en hallazgo.

📌 **Nota del 2026-09-02 (`T-044`).** Esta decision se registro **incumpliendo `L-007`**, y conviene
que quede escrito: la excepcion se escribio solo en el archivo de etapa, mientras `CLAUDE.md` seguia
diciendo «No hay una tercera casilla» en absoluto. Es el mismo defecto que `F-007` abrio en su dia
—una regla y su excepcion en sitios distintos—, cometido por quien ya tenia la leccion escrita. El
usuario lo pidio revisar y se corrigio en la misma sesion: **`PI-5` lleva ahora el puntero**, escrito
en generico —una etapa cuyo producto es deliberadamente descartable— sin nombrar ninguna etapa, para
que `CLAUDE.md` siga siendo copiable.

```
$ grep -n "Hay una sola excepcion posible" CLAUDE.md
64:⚠️ **Hay una sola excepcion posible, y no se decide aqui: la declara un archivo de etapa.** Una
```

---

### D-060 - El archivo de etapa del prototipo se escribe por adelantado, sin declarar la etapa
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** el usuario aporto un archivo de etapa de prototipo procedente de otro proyecto, para
  adaptarlo a esta metodologia. Pero `_phases/005_discovery.md` §1 dice que **declarar las etapas
  posteriores es trabajo del descubrimiento**, y su §6 que mientras una etapa no tenga su `D-XXX` y
  su archivo, la respuesta a «¿que viene despues?» es *«sin decidir»*. El descubrimiento no ha
  empezado: depende de `A-004`.
- **Decision:** **se escribe el archivo y no se declara la etapa.** `_phases/010_prototype.md` existe
  como preparacion; `project.md` **no** gana ninguna fila de etapa nueva, y la adopcion —si llega—
  la decide el descubrimiento con su propio `D-XXX`. El archivo lo dice de si mismo en su cabecera,
  para que nadie lo lea como calendario.
- **Por que no declararla hoy:** decidir la secuencia de etapas antes de entender la necesidad es
  exactamente lo que el descubrimiento existe para evitar. El metodo describe un ciclo; **que un
  proyecto lo adopte entero es una decision suya**, y tomarla hoy seria darla por hecha.
- **Por que tampoco dejarlo sin registro:** un archivo de etapa que aparece en `_phases/` sin nadie
  que explique por que esta ahi se lee dentro de un mes como una etapa adoptada. La cabecera del
  archivo y esta entrada son las dos mitades del mismo aviso.
- **Lo que esto deja pendiente, dicho antes de que sorprenda:** el archivo referencia plantillas en
  `_templates/` y un archivo de reparto en `_workflow/` **que hoy no existen**. No es un descuido:
  son condicion para abrir la etapa, no trabajo de dentro de ella, y el propio archivo lo declara.
- **Alternativas descartadas:** (1) declarar la etapa hoy en `project.md` —coherente entre archivo y
  registro, pero decide la secuencia antes de entender la necesidad—; (2) escribir el archivo sin
  ningun registro —barato hoy, ilegible en un mes—; (3) dejarlo en la carpeta de trabajo del usuario
  hasta que el descubrimiento lo pida —conserva la regla, pero el trabajo de adaptacion se pierde o
  se rehace.
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio — es un archivo nuevo en
  una carpeta ya declarada, sin efecto sobre ningun registro vivo.

**Verificacion — el archivo existe, avisa de su propia condicion, y `project.md` no declara la etapa:**

```
$ ls _phases/
000_preproject.md
005_discovery.md
010_prototype.md

$ grep -n "Que este archivo exista no significa que la etapa este adoptada" _phases/010_prototype.md
28:🚨 **Que este archivo exista no significa que la etapa este adoptada.** Adoptar una etapa exige su

$ grep -c "010_prototype" project.md
0

$ grep "| Etapas declaradas |" project.md
| Etapas declaradas | `000_preproject`, `005_discovery` |
```

⚠️ **Sin `-n` a proposito:** lo que prueba esta orden es **el contenido de la fila** —que siguen
siendo dos etapas—, y el numero de linea se movio dentro de la misma sesion al añadir `D-061` sus
filas a `project.md`.

📌 **Nota del 2026-09-02 (`T-044`).** `D-061`, del mismo dia, **si añade filas a `project.md`** —una
carpeta de entregables en «Carpetas propias» y su ruta—, y eso puede leerse como si contradijera lo
de arriba. No lo hace: **declarar donde iran los entregables no es declarar la etapa.** La tabla
«Etapas» sigue con dos, y esta decision sigue vigente sin cambios. La primera orden del bloque
—`grep -c "010_prototype" project.md`, que devolvia `0`— **ya no se reproduce por eso**, y no se
reescribe (`D-019`): lo que la sustituye es la de `| Etapas declaradas |`, que es la que de verdad
prueba lo que esta entrada afirma.

⚠️ **La cuarta orden se escribio primero como un recuento sobre la seccion «Etapas» y devolvia `8`,
no `1`:** el patron contaba tambien las menciones en prosa. Se sustituye antes de publicarla por las
dos de arriba, que si prueban lo que la decision afirma —que `project.md` no nombra la etapa nueva en
ningun sitio, y que la fila de etapas declaradas sigue teniendo dos—. Es el Paso 2d del cierre
haciendo su trabajo sobre esta misma entrada.

📌 **Nota del 2026-09-02 (`T-047`, hallazgo `F-033`).** La frase con que cierra la nota
anterior —«que `project.md` **no nombra la etapa nueva en ningun sitio**»— **es falsa sobre el mismo
commit**, y la nota inmediatamente anterior de esta misma entrada ya lo reconocia. Lo que las dos
ordenes prueban es solo lo segundo: **que la tabla «Etapas» sigue teniendo dos**. `project.md` si
nombra `010_prototype` en tres sitios —los tres de la carpeta de entregables que declara `D-061`—, y
**ninguno de los tres declara la etapa**, que es lo que esta decision afirma. La decision no cambia;
se acota la frase que la respalda, sin reescribirla (`D-019`).

```
$ git show 265bfeb:project.md | grep -c "010_prototype"
3

$ git show 265bfeb:project.md | grep "| Etapas declaradas |"
| Etapas declaradas | `000_preproject`, `005_discovery` |
```

---

### D-061 - Una carpeta de entregables se llama como su etapa, y se declara por adelantado
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** el archivo de etapa del prototipo (`T-043`) decia que los entregables van a «la
  carpeta de artefactos de la etapa» y que **cual es la dice `project.md`** — pero `project.md` no
  lo decia de ninguna etapa. `005_discovery` lleva desde su creacion con la misma frase y sin
  carpeta detras. El usuario zanjo donde van los del prototipo.
- **Decision:** dos piezas, y la segunda es la que la hace convencion en vez de un caso suelto:

| Pieza | Que fija |
|---|---|
| **El nombre** | una carpeta de entregables se llama **igual que su etapa**, en la raiz del repositorio |
| **El contenido** | los artefactos de registro en su raiz, y el codigo —cuando la etapa produzca codigo— en una **subcarpeta** suya |

Para el prototipo eso es `010_prototype/`, declarada ya en «Carpetas propias» y en «Rutas».

- **Por que el mismo nombre y no un prefijo aparte:** una etapa ya vive en cuatro sitios —su archivo
  en `_phases/`, su subcarpeta en `_templates/`, su archivo en `_workflow/` y ahora su carpeta de
  entregables—. Con el mismo nombre en los cuatro, **el nombre de la etapa es la unica coordenada
  que hay que recordar**; con un prefijo distinto habria que recordar la traduccion, y una
  traduccion que solo esta en la cabeza de alguien se pierde en la primera sesion que no la tenga
  delante. La propuesta inicial fue `015_prototype`, y el usuario la corrigio a `010_prototype`
  precisamente por eso.
- **Por que se declara antes de que exista:** fijar donde van los entregables **antes del primero**
  cuesta cero; hacerlo despues obliga a mover archivos ya citados desde otros sitios. Y `git` no
  versiona carpetas vacias, asi que la fila estara sin carpeta hasta que la etapa arranque — con su
  razon escrita en `project.md`, que es lo que el control de carpetas del cierre exige a cualquier
  diferencia que sobreviva.
- **Su limite, dicho porque esta regla se puede estirar:** vale para una carpeta **cuya etapa esta
  escrita y cuyo contenido esta enumerado**. No autoriza declarar carpetas «por si acaso»: una fila
  para algo que aun no se sabe que sera convierte el control en ruido, y un control con ruido deja
  de mirarse.
- **Lo que esta decision NO hace:** no adopta la etapa. `010_prototype` sigue sin fila en la tabla
  «Etapas», y `D-060` sigue vigente. **Se declara donde iran los entregables, no que se vayan a
  producir** — igual que tener el archivo de etapa no significa haber entrado en ella.
- **Alternativas descartadas:** (1) `015_prototype`, la propuesta inicial —introduce un desfase
  entre el nombre de la etapa y el de su carpeta, sin ganar nada—; (2) una carpeta contenedora con
  una subcarpeta por etapa —un nivel mas de profundidad para la misma informacion—; (3) declararla
  solo cuando nazca el primer artefacto —evita la fila sin carpeta, pero deja la decision para el
  momento en que ya estorba.
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — es una
  fila de tabla y una carpeta que hoy ni siquiera tiene contenido.

**Verificacion — las dos filas nuevas, y el control de carpetas señalando exactamente las dos
diferencias que tienen razon escrita:**

```
$ grep -n "010_prototype" project.md
37:| Entregables de `010_prototype` | `010_prototype/` (el codigo descartable, en una subcarpeta suya) |
150:| `010_prototype/` | **Los entregables de la etapa `010_prototype`**: los cinco artefactos de registro en su raiz, y el codigo descartable del prototipo en una subcarpeta suya. Se archiva o se borra al cerrar su Gate — **no se muda a ninguna carpeta de producto** |
170:- **`010_prototype/`** esta **declarada por adelantado y todavia no existe en el arbol**, porque su

$ diff <(git ls-tree -d --name-only HEAD | sed 's|$|/|' | sort) <(sed -n '/^## Carpetas propias/,/^## /p' project.md | grep -oE '^| `[^`]+/`' | tr -d '|` ' | sort)
1a2
> 010_prototype/
8a10
> temporal/
```

📌 **Las dos lineas `>` son filas declaradas sin carpeta en el arbol, y las dos tienen su razon
escrita en `project.md`** — que es exactamente lo que el Paso 2c pide de una diferencia que
sobrevive. La orden se corre contra `HEAD` a proposito: el control compara el **arbol versionado**,
y una carpeta vacia no llega a el.


---

### D-062 - El numero de participantes lo fija el proyecto, porque la guia de metodo no lo fija
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | manager |

- **Contexto:** al revisar `_phases/010_prototype.md` para el agnosticismo (`T-044`), su Paso 3 pedia
  «un minimo que **la guia de metodo** o el proyecto fijen». Se comprobo contra `_methodology/000_method.md`
  y **la guia no fija ninguna cantidad**: exige «usuarios representativos» y nada mas. El archivo
  fuente del que se adapto si traia una cifra —minimo 3, recomendado 5—, marcada alli como adicion
  propia con la nota de que las fuentes no la respaldan.
- **Decision:** el archivo de etapa **no inventa la cifra ni finge que la guia la trae**. Declara que
  la guia no la fija, y que **el numero lo fija el proyecto con su `D-XXX` antes de la primera
  sesion**, escribiendo por que ese y no otro.
- **Por que no copiar el «minimo 3, recomendado 5» del fuente:** venia marcado en origen como una
  adicion sin respaldo. Copiarla a un archivo de etapa la convertiria en **regla del metodo por el
  solo hecho de aparecer ahi**, sin que nadie pueda ya distinguirla de lo que si esta respaldado. Es
  el mismo defecto que `L-002`: lo que viaja de otro proyecto llega con cosas que alli tenian su
  contexto y aqui lo pierden.
- **Por que tampoco dejarlo como estaba:** «un minimo que la guia de metodo fije» manda a buscar una
  cifra que no existe. Quien la busque no la encontrara y la decidira sobre la marcha — **que es
  exactamente lo que el Paso 3 prohibe**, y encima creyendo que cumple.
- **Lo que el archivo añade ademas, y no es adorno:** que un numero sin su `D-XXX` es peor que no
  tenerlo. Parece una regla del metodo, nadie lo discute, y cuando la ronda se alarga se recorta sin
  que conste que se recorto.
- **Alternativas descartadas:** (1) copiar la cifra del fuente —la asciende a regla sin respaldo—;
  (2) fijar aqui un minimo para este proyecto —no hay con que decidirlo hasta saber cuantos usuarios
  del actor originador son alcanzables, que es dato del descubrimiento—; (3) dejar la redaccion
  ambigua —manda a buscar lo que no hay.
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio — es la redaccion de un
  paso en un archivo de etapa que no esta adoptada.

**Verificacion — la guia no fija cantidad, y el archivo de etapa ya lo dice:**

```
$ grep -cEi "minimo 3|minimo tres|recomendado 5|cuantos usuarios|numero de usuarios" _methodology/000_method.md
0

$ grep -nEi "usuarios representativos" _methodology/000_method.md
413:9. Usar usuarios representativos.
544:> Usuarios representativos del Actor evaluado **completan de forma autónoma** el

$ grep -c "La guia de metodo no fija cuantos" _phases/010_prototype.md
1
```

---

### D-063 - El Paso 2d publica la lista completa de su primera orden, no una seleccion
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | report_auditor |

- **Contexto:** `S-012` creo el Paso 2d de `protocol-close` para impedir que se publicara un bloque
  de verificacion sin ancla, y lo corrio en su propio cierre. Aun asi, `R-012` abrio `F-032` sobre
  una orden de esa misma sesion: la evidencia del paso pegaba **cinco** lineas, cuando la orden
  sobre el commit devuelve varias decenas, y la que fallaba estaba entre las que no se pegaron.
- **Decision:** el Paso 2d **exige publicar la lista completa** que devuelve su primera orden, con
  su recuento, y el resultado de reejecutar cada linea. Se escribe dentro del propio paso.
- **Por que ahi y no como aviso:** `L-008` —una regla sin mecanismo es una intencion— y `L-011` —un
  mecanismo escrito como aviso se salta; escrito como hueco de la plantilla, no—. El paso ya existia;
  lo que faltaba era decir **que cuenta como haberlo corrido**.
- **Lo que esto no arregla, dicho para que no se lea como resuelto:** el paso sigue siendo un cedazo
  —no ve ordenes escritas en prosa ni sin el prefijo `$ `— y su propio archivo ya lo declaraba. Lo
  que cambia es que la parte mecanizable deja de depender de que quien la corre elija bien que
  pegar. **La relectura sigue siendo obligatoria.**
- **Y una limitacion que aparecio al verificarlo:** la orden **no devuelve el mismo numero en todos
  los entornos**. `R-012` publica `26` sobre `7f55389`; la misma orden aqui devuelve `28`. Es una
  razon mas para la decision: una lista se compara linea a linea, un numero solo se puede creer.
- **Alternativas descartadas:** (1) dejarlo como estaba y confiar en la relectura —es lo que ya
  fallo ocho veces—; (2) afinar el patron hasta eliminar los falsos positivos —el propio paso
  explica por que no: un cedazo afinado acaba dejando pasar el caso que importa—; (3) exigir que
  toda orden vaya anclada desde el principio —seria mejor, pero obliga a conocer el hash antes de
  que el commit exista, que es imposible en la primera pasada.
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — es un
  parrafo en una skill, sin efecto sobre ningun registro ya escrito.

**Verificacion — el parrafo existe en el paso que endurece:**

```
$ grep -n "la lista COMPLETA" .claude/skills/protocol-close/SKILL.md
273:🚨 **Y la evidencia de este paso publica la lista COMPLETA de su primera orden, nunca una

$ grep -n "^## Paso 2d" .claude/skills/protocol-close/SKILL.md
242:## Paso 2d — Ningun bloque de verificacion sin ancla (antes del `git add`)
```

---

### D-064 - Las cinco plantillas del prototipo se adaptan de las del usuario, no se copian
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** el usuario aporto cinco archivos en su carpeta de trabajo, procedentes de otro
  proyecto, como material para las plantillas de la etapa del prototipo (`T-048`). Es el mismo caso
  que `D-041` con las del descubrimiento y `D-033` con el archivo de etapa.
- **Decision:** **se adaptan, no se copian.** Nacen las cinco plantillas de
  `_templates/010_prototype/`, una por artefacto de `_phases/010_prototype.md` §5, con la forma de
  las de `_templates/005_discovery/`.
- **Que hubo que cambiar, y las tres ultimas filas no son cosmeticas:**

| Del material de origen | A esta metodologia |
|---|---|
| rutas de otro proyecto (`_prototype/`, `_memory/`, `phases/`, `methodology/`) | las de este metodo: `010_prototype/`, `_persistence/`, `_phases/`, `_methodology/` |
| «terminal ejecutora» / «terminal auditora» / «sponsor» | `manager`, `report_auditor`, el usuario y el patrocinador, que son los actores reales |
| codigos ajenos de supuestos y restricciones | los genericos del registro, `A-XXX` y `C-XXX` |
| vocales acentuadas | sin tildes, como el resto del repositorio |
| **«el metodo pide minimo 3, recomendado 5»** | **la guia de metodo no fija ninguna cantidad**: lo fija el proyecto con su `D-XXX` (`D-062`) |
| **referencias a un archivo de etapa de Gate y a sus comprobaciones numeradas** | «la revision independiente del Gate», y el aviso de que **la etapa del Gate no esta declarada** |
| **codigos de participante y de observacion escritos ya instanciados** | huecos, con el aviso de que un codigo de producto se declara antes en `project.md` |

- **Por que la quinta fila es la mas importante:** el material traia una cifra de participantes que
  **en su origen estaba marcada como adicion sin respaldo**. Copiarla a una plantilla la habria
  convertido en regla del metodo por el solo hecho de aparecer ahi, y nadie podria ya distinguirla
  de lo que si esta respaldado. Es `L-002` otra vez: lo que viaja de otro proyecto llega con cosas
  que alli tenian su contexto y aqui lo pierden.
- **Por que la sexta:** las plantillas apuntaban a un archivo de etapa de Gate que **este proyecto
  no tiene**, con numeros de comprobacion incluidos. Una plantilla que cita un archivo inexistente
  manda a buscar lo que no hay — el mismo defecto que `D-062` corrigio en el archivo de etapa.
- **Por que la septima:** `_phases/010_prototype.md` §7 exige que un codigo de producto se declare en
  la tabla «Codigos» de `project.md` **antes de escribir el primero**. La plantilla no puede
  adelantarlo: deja el hueco y el aviso.
- **Lo que esto NO hace:** no adopta la etapa —`D-060` sigue vigente— y **no completa la condicion
  de entrada**: falta `_workflow/010_prototype.md`, que hoy no existe.
- **Alternativas descartadas:** (1) copiar los cinco archivos tal cual —trae rutas, actores y una
  cifra que aqui no se sostienen—; (2) escribirlas desde cero ignorando el material —se pierde
  trabajo bueno: la estructura, los errores que cada plantilla existe para evitar y los ejemplos—;
  (3) dejarlas para cuando la etapa arranque —es cuando peor salen, y `_phases/010_prototype.md` §5
  las declara condicion de entrada, no trabajo de dentro.
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio — son cinco archivos
  nuevos en una carpeta ya declarada, sin efecto sobre ningun registro vivo.

⚠️ **El material se leyo de la carpeta de trabajo del usuario porque el usuario lo pidio.** Esa
carpeta esta fuera del repositorio y **los protocolos tienen prohibido tocarla**; lo que se hizo aqui
lo hizo `manager` por peticion expresa, y lo que entra al repositorio es el resultado adaptado, nunca
el original.

**Verificacion — las cinco plantillas existen y no traen residuo del origen:**

```
$ ls _templates/010_prototype/
005_happy_path.md
010_participants.md
015_session_NNN.md
020_observations.md
025_business_validation.md

$ grep -rniE "(^|[^0-9])_prototype/|_memory/|015_gate1|terminal (ejecutora|auditora)|sponsor|020_baseline|minimo 3|recomendado 5|SUP-|RES-" _templates/010_prototype/ ; echo "exit=$?"
exit=1

$ grep -rlc "Guia de llenado" _templates/010_prototype/
_templates/010_prototype/005_happy_path.md
_templates/010_prototype/010_participants.md
_templates/010_prototype/015_session_NNN.md
_templates/010_prototype/020_observations.md
_templates/010_prototype/025_business_validation.md

$ grep -c "sin decidir" _templates/010_prototype/*.md
_templates/010_prototype/005_happy_path.md:1
_templates/010_prototype/010_participants.md:1
_templates/010_prototype/015_session_NNN.md:1
_templates/010_prototype/020_observations.md:3
_templates/010_prototype/025_business_validation.md:1
```

📌 **La cuarta orden comprueba la fila sexta de la tabla:** las cinco plantillas cierran
diciendo que, mientras la etapa del Gate no tenga su `D-XXX` y su archivo en `_phases/`, la respuesta
correcta a «que viene despues» es *«sin decidir»*. Es la misma formula con que cierran las plantillas
del descubrimiento. **`020_observations.md` devuelve `3` y no `1`** porque ademas usa la formula
dos veces en el cuerpo: las categorias que no pesan en el Gate van a «una etapa posterior» que
tampoco esta declarada. Se publica la salida entera y se explica la diferencia, en vez de acotar el
patron para que devolviera cinco unos (`L-019`).

---

### D-065 - La evidencia del Paso 2d tiene sitio fijo: la seccion 7 del informe de sesion
| Campo | Valor |
|---|---|
| Fecha | 2026-09-03 |
| Estado | Vigente |
| Origen | report_auditor |

- **Contexto:** `D-063` fijo el dia anterior **que** el Paso 2d publica la lista completa de su
  primera orden. `R-013` abrio `F-034` sobre esa misma sesion: el informe de `S-013` afirmo haberlo
  cumplido y remitio a la verificacion de `T-046`, donde no hay ninguna lista. La salida solo vivio
  en pantalla, y con la sesion desaparecio.
- **La causa, y no es descuido:** `D-063` dice **que** publicar y no **donde**. Una evidencia sin
  sitio asignado no tiene ningun momento en que se eche en falta: el cierre la produce, la mira, y
  nada obliga a que aterrice en un archivo. Es el mismo hueco que `L-008` describe —una regla sin
  mecanismo es una intencion—, aplicado a una regla que ya tenia mecanismo pero no destino.
- **Decision:** la lista completa del Paso 2d se publica en **la seccion 7 del informe
  `_audit/S-XXX.md`**, que nace con esta decision. Dos cambios en `protocol-close`: el Paso 2d dice
  donde va, y la estructura del informe gana la seccion con sus huecos. Una lista vacia se publica
  igual —«ninguna linea» tambien es un resultado.
- **Por que en el informe y no en `tasks.md`:** la evidencia del Paso 2d no pertenece a ninguna
  tarea. Es evidencia del **cierre**, se produce una vez por sesion y describe el commit entero;
  colgarla de la tarea que toco es lo que hizo `S-013`, y por eso quedo colgada de una que no la
  contenia. El informe es tambien lo que lee la auditoria, que es quien la va a contrastar.
- **Alternativas descartadas:** (1) dejar el `donde` implicito y confiar en que el cierre lo pegue
  donde toque —es exactamente lo que fallo—; (2) un archivo propio por sesion en `_audit/` —un
  artefacto mas que mantener para algo que ya tiene contenedor natural, contra `PI-2`—; (3) exigirlo
  en `_persistence/tasks.md` bajo la tarea del cierre —no hay tal tarea, y ademas mezcla evidencia de
  sesion con evidencia de tarea.
- **Lo que esto no arregla:** la seccion 7 obliga a que la lista aterrice, no a que este completa.
  Que lo este lo sigue comprobando la auditoria reejecutando la orden por su cuenta (Control e de
  `protocol-audit`), que es la unica lectura que no depende de lo que el cierre eligio pegar.
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — son
  quince lineas insertadas en una skill, sin borrar ni reescribir nada y sin efecto sobre ningun
  informe ya escrito.

**Verificacion — los dos cambios existen, y el diff es solo insercion:**

```
$ grep -n "seccion 7 del informe" .claude/skills/protocol-close/SKILL.md
280:🚨 **Y esa lista tiene un sitio fijo: la seccion 7 del informe de `_audit/S-XXX.md`, y no la

$ grep -n "^## 7. Evidencia del Paso 2d" .claude/skills/protocol-close/SKILL.md
694:## 7. Evidencia del Paso 2d

$ git diff --numstat -- .claude/skills/protocol-close/SKILL.md
15      0       .claude/skills/protocol-close/SKILL.md
```

---

### D-066 - El reparto del prototipo: la IA construye, no facilita, y clasifica sin pesar
| Campo | Valor |
|---|---|
| Fecha | 2026-09-03 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** `_phases/010_prototype.md` §5 declara `_workflow/010_prototype.md` **condicion de
  entrada** de la etapa, junto con las plantillas: sin el, la etapa no puede abrirse aunque sus cinco
  entradas esten completas. `S-013` escribio las plantillas y dejo el reparto pendiente; `R-013` lo
  senalo como recomendacion sin hallazgo. El usuario lo pidio hoy.
- **Decision:** nace `_workflow/010_prototype.md`, derivado de `_workflow/team.md` y
  `_workflow/ai_levels.md`, con una fila por cada uno de los nueve pasos del procedimiento. Las
  cinco asignaciones que lo definen:
  1. **Paso 4 — la IA construye el prototipo**, y es la primera vez en el metodo que la IA escribe
     codigo. Con autonomia de **reversible y de impacto relevante**: el humano lo revisa entero
     antes de la primera sesion, no por muestreo.
  2. **Pasos 5 y 9 — la IA queda fuera de las sesiones**, las de usuario y la de negocio. Puede
     preparar el guion antes; durante, nada.
  3. **Paso 6 — la inmovilidad del prototipo la vigila el historial, no una promesa.**
  4. **Paso 8 — la IA propone la categoria de cada observacion; el peso contra el Gate lo decide un
     humano.**
  5. **Nivel de sistema de IA para el trabajo de la etapa: 2**, no 0–1, porque la IA escribe
     archivos y eso es una herramienta que escribe.
- **Por que la autonomia del Paso 4 no es la baja:** el prototipo se puede rehacer, pero **la ronda
  no se puede repetir** — un usuario que ya vio el artefacto dejo de ser un usuario que lo ve por
  primera vez, y esa es justo la condicion que la etapa mide. Un error de construccion no cuesta el
  prototipo: cuesta los participantes.
- **Alternativas descartadas:**
  1. **Que el prototipo lo construya un humano.** Descartada: es generacion sobre lenguaje con un
     artefacto barato al otro lado, la capacidad que `_workflow/team.md` §1 asigna a la IA, y poner
     a un humano ahi es el antipatron «humano de software» de su §12.
  2. **Autonomia baja en el Paso 4 —ejecutar y reportar, revision por muestreo—.** Descartada por lo
     de arriba: el muestreo detecta el fallo despues de haberlo mostrado a alguien.
  3. **La IA como facilitadora con guion en el Paso 5.** Descartada: los principios de no sesgo
     describen a una persona leyendo a otra —un titubeo, una mano que vuelve atras—, y nada de eso
     es texto.
  4. **Sesiones simuladas con usuario de IA para completar el numero fijado.** Descartada de raiz, y
     escrita como prohibicion explicita: produce evidencia inventada con forma de evidencia
     validada, y el Gate decidiria una inversion sobre ella.
  5. **Que la IA senale que observaciones son las importantes.** Descartada: solo tres de las nueve
     categorias pesan en el Gate, y preguntarle cuales le parecen importantes devuelve exactamente
     la opinion que la evaluacion por comportamiento existe para sacar de en medio.
  6. **Aplazar este archivo hasta que la etapa se abra.** Descartada: es condicion de entrada, y una
     condicion de entrada escrita el dia que se entra no condiciona nada.
- **La discrepancia con la rubrica, declarada y no disimulada:** la tabla de lectura de
  `_workflow/ai_levels.md` §6 manda al nivel 5 en cuanto cualquier eje esta en 3, y «variabilidad de
  la entrada» lo esta. Se discute contra los ejes, como el propio archivo permite: impacto en 2 y
  autonomia en 1 —los dos que protege su regla 2—, la variabilidad alta cae en las **notas de
  sesion**, que las escribe un humano que estuvo delante, y el volumen en 1 esta acotado por el
  limite de duracion de la etapa. **Si algun dia la IA produce el registro de las sesiones en vez de
  transcribir notas humanas, el eje que se mueve es «impacto de un error» y la lectura ya no es
  esta.**
- **Lo que esto NO hace:** no adopta la etapa `010_prototype` —sigue sin fila en la tabla «Etapas»
  de `project.md`, con `D-060` vigente— y no reparte nada por si solo. `_workflow/team.md` §8 es
  explicito: leer la tabla no reparte; repartir es el `D-XXX` que se escriba **al abrir la etapa**,
  con lo que se adopta y lo que se descarta.
- **Una diferencia con el archivo hermano, dicha para que no se lea como descuido:** este archivo
  **no cita ningun codigo instanciado**; `_workflow/005_discovery.md` cita uno (`L-014`). El nuevo
  cumple la regla de codigos genericos que los dos declaran en su cabecera; el anterior no se toca
  por esta decision — `PI-3`, y renombrar o borrar una cita en un archivo ya auditado es trabajo con
  su propio riesgo.
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — es un
  archivo nuevo en una carpeta ya declarada, no borra ni publica nada, y ninguna etapa esta abierta
  todavia para que rija sobre trabajo en curso.

**Verificacion — el archivo existe, tiene una fila por paso, la etapa lo cita, y es agnostico:**

```
$ grep -c "^| \*\*[1-9] · " _workflow/010_prototype.md
9

$ grep -n "_workflow/010_prototype" _phases/010_prototype.md
144:**`_workflow/010_prototype.md`**, que se lee ahora y no despues. Ese reparto se adopta con su `D-XXX` en el
314:🚨 **Las plantillas y el reparto de `_workflow/010_prototype.md` son condicion de entrada, no

$ grep -rnE "RaindomAI|RaidomAI|Proyectos_TripleS|github.com" .claude CLAUDE.md _phases _methodology _templates _workflow ; echo "exit=$?"
exit=1

$ grep -nE "(N|T|D|A|C|I|F|L|S|R|DT)-[0-9]+" _workflow/010_prototype.md ; echo "exit=$?"
exit=1

$ grep -nE "(N|T|D|A|C|I|F|L|S|R|DT)-[0-9]+" _workflow/005_discovery.md ; echo "exit=$?"
188:manda leer es material muerto que ningun control detecta — el cuarto enganche de `L-014`.
exit=0
```

📌 **La quinta orden se publica aunque sea del archivo hermano y no del nuevo.** Es la evidencia de
la diferencia que declara la vineta de arriba: sin ella, «el nuevo cumple y el viejo no» seria un
veredicto sin su comando.

---

### D-067 - El Gate 1 no es una etapa: se monta como agente y skill
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** el usuario trajo a `temporal/015_gate1.md` un borrador del Gate 1 y pidio analizarlo
  para construir `_phases/015_gate1.md`. Al contrastarlo con `_methodology/000_method.md` §28–§32 y
  con los tres archivos de `_phases/` aparecio una pregunta previa: **si el Gate es una etapa.**
- **La distincion que decide:** una etapa es un **tramo de trabajo** —dura sesiones, autoriza
  producir unas cosas y prohibe otras, acumula artefactos—, y por eso su archivo tiene las secciones
  «que autoriza», «que prohibe» y «condicion de salida». Un Gate es un **acto de juicio**: lee
  evidencia ya escrita, la contrasta contra criterios y devuelve un dictamen. No produce producto y
  no dura. Sus secciones §1 y §2 habrian sido la carta de un agente, no la de una etapa.
- **Decision:** el Gate 1 **no se declara como etapa** y no tiene archivo en `_phases/`. Se monta con
  la forma que este repositorio ya usa para los actos: **un agente y su skill** —`gate1_auditor` y
  `protocol-gate1`—, como los tres pares que ya existen. Su plantilla vive en `_templates/015_gate1/`
  y su dictamen en `_audit/015_gate1/`.
- **Por que esa forma y no otra:** los tres protocolos del repositorio —arranque, cierre, auditoria—
  son exactamente esto: un procedimiento determinista, un agente que arranca en frio, un artefacto de
  salida y un sitio fijo donde escribirlo. El Gate encaja sin forzar nada.
- **Lo que ademas se evita:** como etapa arrastraba cinco artefactos —fila en `project.md`, `D-XXX`
  de adopcion, `_workflow/015_gate1.md`, `_templates/015_gate1/` y carpeta de entregables— para un
  acto que dura una sesion. Como protocolo arrastra dos. Ademas desaparece el parrafo de «existe pero
  no esta adoptada» que `010_prototype.md` tuvo que escribir, porque **un protocolo no se adopta: se
  invoca**.
- **Y coincide con la guia de metodo:** §5 dibuja los Gates como rombos **entre** etapas, y la tabla
  de §4 —«cada etapa responde una pregunta»— lista PROTOTIPO, MVP y EVOL. Los Gates no estan ahi. La
  guia nunca los llamo etapas.
- **Nomenclatura:** la carpeta es `015_gate1`, no `015_gate_1`. El patron vigente es `NNN_palabra`
  —`000_preproject`, `005_discovery`, `010_prototype`— y no separa el digito final. El prefijo `015_`
  marca **donde cae en el ciclo**, no que sea una etapa.
- **Alternativas descartadas:** (1) declararlo etapa con archivo en `_phases/` —era la peticion
  literal, y arrastra cinco artefactos de ceremonia para un acto de un dia, contra `PI-2`—;
  (2) dejarlo solo en `_methodology/` como parte de la guia —describiria el Gate sin que nadie pueda
  ejecutarlo, y §28–§32 ya lo describe—; (3) escribir el archivo en `_phases/` pero aclarando dentro
  que no es una etapa —rompe la definicion que `project.md` da de esa carpeta, «un archivo por etapa
  declarada», y deja la carpeta significando dos cosas.
- **Lo que esto no resuelve:** un protocolo se invoca cuando alguien quiere, mientras que una etapa
  se cierra con condiciones. El Gate hereda el limite conocido de `report_auditor` —lo lanza el
  propio evaluado—, y el antidoto es el mismo: se anclo en `_phases/010_prototype.md` §6 como ultimo
  paso obligatorio de la etapa, no como algo que se hace cuando toca.
- **Gate 2:** no se adelanta. Se montara cuando exista, con lo que entonces se sepa que comparte de
  verdad con el primero, en vez de adivinarlo hoy (`PI-2`).
- **Clasificacion:** **reversible a criterio**, y lo declaro como criterio y no como tabla — son
  archivos nuevos y tres inserciones en `project.md`; nada se borro y nada se renombro. Si mañana se
  decidiera que si es etapa, el contenido se muda sin perdida.

**Verificacion — el par existe, y `_phases/` sigue con tres archivos:**

```
$ ls -1 .claude/agents/ .claude/skills/
.claude/agents/:
gate1_auditor.md
report_auditor.md
session-closer.md
session-starter.md

.claude/skills/:
protocol-audit
protocol-close
protocol-gate1
protocol-start

$ ls -1 _phases/
000_preproject.md
005_discovery.md
010_prototype.md

$ ls -1 _templates/015_gate1/
005_verdict.md
```

**Verificacion — lo nuevo no filtra datos propios (patron del Paso 1b, sobre los seis directorios):**

```
$ grep -rnE "RaindomAI|RaidomAI_App|C:\\Users\\USUARIO|github\.com" .claude CLAUDE.md _phases _methodology _templates _workflow
exit=1
```

📌 **Se uso `grep -r` y no `git grep` a proposito:** `git grep` solo mira archivos versionados, y los
de esta decision todavia no lo estaban cuando se corrio — el `git grep` que se probo antes devolvio
cero por no verlos, no por estar limpios. El barrido del Paso 1b los cubrira ya versionados.

---

### D-068 - El Gate 1 son dos firmas: `gate1_auditor` dictamina y el patrocinador decide
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** el borrador de `temporal/015_gate1.md` daba a la revision independiente un unico
  archivo encabezado `VEREDICTO GATE 1: APROBADO | NO APROBADO | NO AUDITABLE`. «Aprobado» es una
  **decision de inversion**, no un dictamen tecnico — y con esa forma la revision decide, que es lo
  que `CLAUDE.md` prohibe a un auditor y lo que `000_method.md` §32 separa en dos firmas.
- **Donde se veia el colapso:** el borrador metia los **siete** criterios de §29 en la tabla que
  audita la revision, incluido el 6 —«hay confianza suficiente para la inversion del MVP»—. Ese
  criterio **no tiene ningun artefacto contra el que verificarse**: es literalmente la firma del
  patrocinador. Los otros seis si se leen contra archivos.
- **Decision:** el Gate 1 produce **dos cosas separadas, y ninguna sustituye a la otra**:

| Firma | Quien | Que produce | Donde queda |
|---|---|---|---|
| **Dictamen tecnico** | `gate1_auditor` | `CRITERIOS SATISFECHOS` · `CRITERIOS NO SATISFECHOS` · `NO AUDITABLE` | `_audit/015_gate1/005_verdict_NNN.md` |
| **Decision de inversion** | el usuario, como patrocinador | construir el MVP · replantear · detener | `_persistence/decisions.md`, con su `D-XXX` |

- **Consecuencias concretas:** el agente audita **seis** criterios, no siete; el 6 aparece en su
  tabla marcado `— corresponde al patrocinador`, para que se vea que no se paso por alto y no como un
  hueco; y las palabras `APROBADO` y `NO APROBADO` **no aparecen como valor** en ningun artefacto del
  Gate.
- **El patrocinador puede decidir contra el dictamen, y es legitimo.** Lo que no puede es cambiarlo:
  un `NO CUMPLE` es un hecho verificable contra los archivos. Si se decide construir igual, la
  `D-XXX` dice por que — y eso vale mucho mas que un dictamen ablandado, porque dentro de seis meses
  se puede leer que se sabia y que se decidio a pesar de ello.
- **Por que el dictamen y la decision viven en sitios distintos:** el dictamen es producto de una
  revision independiente y va donde va todo lo que produce una —`_audit/`—; la decision es del
  negocio y va donde han ido todas las decisiones del proyecto. Juntarlos en un archivo es lo que
  hacia el borrador, y es lo que permitia que una firma se leyera como la otra.
- **Alternativas descartadas:** (1) un solo archivo con las dos firmas dentro —lo del borrador; la
  proximidad fisica es justo lo que colapsa los papeles—; (2) que el agente emita `APROBADO` y el
  patrocinador solo lo ratifique —convierte la segunda firma en un tramite y traslada la decision de
  inversion a quien no la asume—; (3) que el agente evalue tambien el criterio 6 declarandolo
  `NO COMPROBABLE` siempre —tecnicamente cierto, pero enseña a leer `NO COMPROBABLE` como ruido de
  formulario justo en la tabla donde ese valor tiene que pesar.
- **Clasificacion:** **reversible a criterio** — es la forma de dos artefactos que todavia no se han
  producido ni una vez; no hay ningun Gate corrido al que afecte.

**Verificacion — el criterio 6 esta marcado como del patrocinador, y `APROBADO` solo aparece prohibido:**

```
$ grep -n "corresponde al patrocinador" .claude/skills/protocol-gate1/SKILL.md _templates/015_gate1/005_verdict.md
.claude/skills/protocol-gate1/SKILL.md:232:te prohibe. En el dictamen aparece con `— corresponde al patrocinador`, para que se vea que no se
.claude/skills/protocol-gate1/SKILL.md:410:| 6 | — | corresponde al patrocinador |
.claude/skills/protocol-gate1/SKILL.md:437:- **El criterio 6 no es tuyo.** Se marca `— corresponde al patrocinador`, no se evalua.
_templates/015_gate1/005_verdict.md:136:| 6 | Hay confianza suficiente para la inversion del MVP | **—** | **corresponde al patrocinador** |

$ grep -nE "NO APROBADO|APROBADO" _templates/015_gate1/005_verdict.md
29:> ⛔ **Las palabras `APROBADO` y `NO APROBADO` no aparecen en este archivo.** Nombran la decision, y
```

📌 **La unica aparicion en la plantilla es la linea que las prohibe.** Ninguna como valor.

---

### D-069 - `NO AUDITABLE` es un tercer resultado del Gate 1, que la guia de metodo no tiene
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** `_methodology/000_method.md` §31 solo contempla dos resultados para el Gate 1:
  **Aprobado** y **No aprobado**. El borrador del usuario añadia un tercero, `NO AUDITABLE`, con su
  argumento.
- **La distincion, y es real:** «no aprobado» dice que la evidencia existe, es legitima **y dice que
  no**. `NO AUDITABLE` dice que **no se puede saber lo que dice**. El prototipo pudo haber ido
  perfecto — pero si la hipotesis se escribio despues de las sesiones, describe lo que salio, y no
  hay nada contra que medirla. Colapsarlos obliga a elegir entre dar un verde que no se sostiene o un
  rojo que acusa a un trabajo que quiza estuvo bien.
- **Decision:** se adopta `NO AUDITABLE` como tercer resultado, y **se declara aqui como adicion**:
  la guia de metodo no lo tiene, y `protocol-gate1` lo dice en vez de presentarlo como si lo leyera
  de §31. Se determina en la **Comprobacion 0**, que corre **antes** que ningun criterio y se
  resuelve **con fechas del historial de `git`**, no preguntando: que la hipotesis, la tarea, el
  perfil y el numero existieran antes de la primera sesion; que lo sellado no cambiara; que el
  prototipo no cambiara entre sesiones; y que cada sesion se escribiera el dia que ocurrio.
- **Que lo hace valioso, y no es la etiqueta:** es la unica comprobacion del metodo **imposible de
  aprobar a posteriori**. Todo lo demas se puede redactar mejor; el orden en que se escribieron esas
  cuatro cosas, no. Las fechas del historial no se pueden convencer.

  > 📌 **Nota del 2026-09-03 (`T-055`, hallazgo `F-037`).** La viñeta de arriba **no se reescribe**,
  > y esta nota dice en que se paso de largo. «Las fechas del historial no se pueden convencer» es
  > **falso tal como estaba implementado**: la Comprobacion 0 resolvia el «antes» con `%ad`, la fecha
  > de autor, que se sobrescribe con una variable de entorno. Comprobado en un repositorio
  > desechable, fuera de este proyecto:
  >
  > ```
  > $ GIT_AUTHOR_DATE="2026-01-10T10:00:00" GIT_COMMITTER_DATE="2026-01-10T10:00:00" git commit -q -m "sesion 1"
  > $ GIT_AUTHOR_DATE="2026-01-01T10:00:00" GIT_COMMITTER_DATE="2026-01-01T10:00:00" git commit -q -m "hipotesis (escrita DESPUES, fechada ANTES)"
  > $ git log --diff-filter=A --format="%ad %h %s" --date=short -- 020_hypothesis.md
  > 2026-01-01 19cbaec hipotesis (escrita DESPUES, fechada ANTES)
  > ```
  >
  > Lo que si resiste es el **orden del grafo**, que el mismo `git log` ya mostraba y que el
  > protocolo no mandaba mirar. `D-071` lo adopta: las tres lecturas de «antes» pasan a
  > `git merge-base --is-ancestor`, y `%ad` queda como dato informativo. **La decision de tener un
  > tercer resultado `NO AUDITABLE` sigue vigente**; lo que cambia es con que se determina.
- **Consecuencias:** `NO AUDITABLE` **corta el protocolo** —no se rellena la tabla de criterios— y
  **no llega al patrocinador**: no hay decision de inversion que tomar sobre una evidencia que no se
  puede leer. Lo que se produce es la lista de que evidencia hay que rehacer, y **no se rehace el
  prototipo: se rehace solo la evidencia que fallo**.
- **Adicion hermana, del mismo origen y por la misma razon:** cada criterio se resuelve con **tres**
  valores —`CUMPLE`, `NO CUMPLE`, `NO COMPROBABLE`— y no con dos. `NO COMPROBABLE` **no se redondea a
  `CUMPLE`**: un revisor que calla lo que no supo mirar miente por omision, y da exactamente el mismo
  verde que uno que comprobo. La guia tampoco tiene esta gradacion.
- **Alternativas descartadas:** (1) quedarse con los dos resultados de §31 y tratar la evidencia
  inauditable como `No aprobado` —acusa de fracaso a un prototipo que quiza funciono, y ademas oculta
  el fallo real, que es de procedimiento—; (2) tratarla como `Aprobado` con salvedades —es el peor de
  los tres: autoriza la inversion mas cara del proyecto sobre evidencia que nadie pudo leer—;
  (3) proponer el cambio a `_methodology/000_method.md` y esperar —la guia es documento canonico
  consolidado, y tocarla exige su propia vuelta; se registra la adicion y se decide despues si sube.
- **Lo que esto no arregla:** `NO AUDITABLE` detecta que la evidencia no se puede leer, no impide que
  se produzca asi. Lo que lo previene es el orden de los pasos 2 y 3 antes del 4 en
  `_phases/010_prototype.md`, que ya estaba escrito.
- **Clasificacion:** **reversible a criterio** — es una adicion declarada en un protocolo que aun no
  se ha ejecutado; no reescribe la guia de metodo ni ningun dictamen anterior, porque no hay ninguno.

**Verificacion — la guia tiene dos resultados, y el protocolo declara el tercero:**

```
$ sed -n '/^## 31. Resultados posibles/,/^↳/p' _methodology/000_method.md
## 31. Resultados posibles

| Resultado | Consecuencia |
|---|---|
| **Aprobado** | → Product Baseline → WSLT |
| **No aprobado** | → aprender, replantear la hipótesis, o detener |

Detener aquí es un **resultado válido y barato**. Es el propósito de la etapa.

↳ *005 §3 · 015 §14, §15*

$ grep -c "NO AUDITABLE" .claude/skills/protocol-gate1/SKILL.md _templates/015_gate1/005_verdict.md
.claude/skills/protocol-gate1/SKILL.md:10
_templates/015_gate1/005_verdict.md:8
```

---

### D-070 - Los dictamenes del Gate 1 son correlativos, y ninguno se sobrescribe
| Campo | Valor |
|---|---|
| Fecha | 2026-09-02 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** `D-069` admite que un Gate acabe en `NO AUDITABLE`, y en ese caso la evidencia se
  rehace y el Gate **se vuelve a correr**. Eso significa que un mismo Gate 1 puede producir varios
  dictamenes.
- **El riesgo que aparece con eso:** un Gate que se puede repetir se puede repetir hasta que salga.
  Si cada pasada sobrescribe la anterior, el registro final muestra un solo dictamen limpio y nadie
  sabra nunca cuantos intentos hicieron falta ni por que fallaron.
- **Decision:** los dictamenes se numeran `005_verdict_001.md`, `005_verdict_002.md`, … en
  `_audit/015_gate1/`. **El numero no se reutiliza, ninguno se borra y ninguno se sobrescribe.**
  Antes de escribir el suyo, `gate1_auditor` **lee los anteriores**: si el mismo fallo de
  Comprobacion 0 ya salio, eso es un hallazgo de **importancia alta** por si mismo, porque el
  problema ya no es la evidencia — es que la etapa se esta corriendo al reves.
- **Por que la regla necesita el archivo:** «`NO AUDITABLE` no puede repetirse dos veces por la misma
  causa» es incomprobable si el dictamen anterior no existe. La regla y la conservacion son la misma
  decision vista por sus dos caras — es el hueco que `L-008` describe: una regla sin mecanismo es una
  intencion.
- **Alternativas descartadas:** (1) un solo archivo que se reescribe en cada pasada —hace invisible
  la repeticion, que es justo lo que hay que ver—; (2) conservar los anteriores solo en el historial
  de `git` y sobrescribir el archivo —tecnicamente recuperable, pero exige saber que hay que mirar el
  historial, y una comprobacion que depende de que alguien sospeche no se corre nunca—; (3) un indice
  de pasadas aparte —un artefacto mas para algo que el nombre correlativo ya ordena, contra `PI-2`.
- **Clasificacion:** **reversible a criterio** — fija el nombre de archivos que aun no existen.

**Verificacion — la regla y su mecanismo estan escritos en los dos artefactos:**

```
$ grep -n "no puede repetirse dos veces" .claude/skills/protocol-gate1/SKILL.md
348:🚨 **`NO AUDITABLE` no puede repetirse dos veces por la misma causa.** Antes de escribir el tuyo,

$ grep -n "ya salio en un dictamen anterior" _templates/015_gate1/005_verdict.md
213:**¿Este mismo fallo ya salio en un dictamen anterior?** `<NO / SI — 005_verdict_<NNN>.md>`
```

---

### D-071 - La Comprobacion 0 del Gate 1 resuelve el «antes» por orden del grafo, no por fecha
| Campo | Valor |
|---|---|
| Fecha | 2026-09-03 |
| Estado | Vigente |
| Origen | report_auditor |

- **Contexto:** `D-069` adopto `NO AUDITABLE` como tercer resultado del Gate 1 y lo apoyo entero en
  una propiedad: que las fechas del historial «no se pueden convencer». `F-037` (`R-015`) demostro
  que esa propiedad no existe tal como estaba implementada — la Comprobacion 0 comparaba `%ad`, la
  fecha de autor, que se sobrescribe con `GIT_AUTHOR_DATE`.
- **Decision:** las tres lecturas de «antes» de la Comprobacion 0 —hipotesis antes de la sesion 1,
  tarea antes del prototipo, perfil y numero antes de la sesion 1— pasan a resolverse con
  **`git merge-base --is-ancestor`**, que responde por el orden del grafo. `%ad` se conserva como
  **dato informativo** y para la unica lectura que necesariamente es de fecha (que cada sesion se
  escribiera el dia que ocurrio). La comprobacion «el prototipo no cambio entre sesiones» pasa a
  `git log $SES1..$SESN -- $PROTO_DIR`, que es tambien orden y no fecha.
- **Y la afirmacion se ajusta a lo que el mecanismo garantiza**, en los tres sitios que la hacian:
  el skill, la plantilla del dictamen y `D-069` (con nota fechada, sin reescribir). Lo que se
  demuestra es que **en el historial publicado esas cuatro cosas entraron antes**; no que nadie
  pudiera haber montado ese historial a posteriori.
- **Alternativas descartadas:** (1) usar `%cd` (fecha de commit) en vez de `%ad` — se sobrescribe
  igual, con `GIT_COMMITTER_DATE`: cambia el nombre del campo, no el agujero; (2) firmar los commits
  con GPG y verificar la firma — resuelve quien, no cuando, y ademas impone al proyecto una
  infraestructura de claves para una comprobacion que el orden del grafo ya cubre; (3) dejarlo como
  estaba y anotar el limite — el limite no era un matiz: la comprobacion daba `PASA` sobre evidencia
  fabricada, que es exactamente el caso para el que existe.
- **Clasificacion:** **reversible a criterio** — se edita un protocolo que todavia no se ha
  ejecutado ni una vez (`_audit/015_gate1/` no existe), no se reescribe ningun dictamen porque no
  hay ninguno, y `D-069` conserva su texto con la nota al lado.

**Verificacion — la Comprobacion 0 ya no decide por fecha, y el limite queda escrito:**

```
$ grep -c "merge-base --is-ancestor" .claude/skills/protocol-gate1/SKILL.md
3

$ grep -n "No uses \`%ad\` para decidir que fue antes" .claude/skills/protocol-gate1/SKILL.md
123:⛔ **No uses `%ad` para decidir que fue antes.** La fecha de autor es un campo del commit y se

$ grep -rc "imposible de aprobar a posteriori" .claude/skills/protocol-gate1/SKILL.md _templates/015_gate1/005_verdict.md
.claude/skills/protocol-gate1/SKILL.md:0
_templates/015_gate1/005_verdict.md:0
```

---

### D-072 - El archivo de etapa de la baseline se escribe por adelantado, y la etapa NO queda adoptada
| Campo | Valor |
|---|---|
| Fecha | 2026-09-03 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** el usuario trajo un borrador propio de la etapa de la baseline
  (`temporal/020_baseline.md`) y pidio construir con el `_phases/020_baseline.md`, tomando ademas
  como guia los dos archivos de etapa que ya existen y `_methodology/000_method.md`. `project.md`
  declara hoy dos etapas —`000_preproject` y `005_discovery`—, y declarar las posteriores es trabajo
  de `005_discovery` (`T-002`), que no ha arrancado.
- **Decision:** se escribe `_phases/020_baseline.md` **y no se toca la tabla «Etapas» de
  `project.md`**. El archivo describe **que se hace si se entra**, no que se vaya a entrar — la misma
  situacion que `D-060` dejo registrada para `_phases/010_prototype.md`, y por la misma razon: un
  archivo de etapa sin decision al lado se lee, a los pocos meses, como una etapa adoptada que nadie
  decidio.
- **Que se corrigio del borrador al portarlo, y por que:** el borrador venia de otro esquema de
  trabajo y traia datos que aqui no valen. Usaba `F-xxx` para Feature y `S-xxx` para Scenario —los
  dos prefijos ya tomados en este registro por el hallazgo y por la sesion, y por eso el metodo usa
  `FT-` y `SC-` (`D-030`, `_methodology/000_method.md` §46)—; `RES-xxx` y `SUP-xxx` donde aqui van
  `C-XXX` y `A-XXX` (`D-034`); rutas propias de aquel proyecto (`_baseline\`, `_memory/`,
  `<Proyecto>_AUDIT/gates/`, `_prototype/`, `templates/`, `tech-debt.md`) donde aqui se referencia
  `project.md`; y hablaba de «terminal ejecutora» donde aqui el lector es `manager`.
- **Lo que el borrador aportaba y se conserva:** la pregunta que corta la etapa —«¿cuanto es
  suficiente?», respondida como «lo que hace falta para el WSLT y la primera slice»—, la lista del
  «no» con razon y destino, las tres preguntas (evaluacion, observabilidad, seguridad) declaradas
  con artefacto y no con intencion, y el criterio de salida de las Features huerfanas.
- **Alternativas descartadas:** (1) adoptar la etapa a la vez que se escribe su archivo — declarar
  etapas es trabajo de `005_discovery`, y adoptarlas desde aqui las daria por decididas sin haber
  entendido todavia que se va a construir; (2) copiar el borrador tal cual a `_phases/` — rompe el
  agnosticismo que el Paso 1b del cierre comprueba sobre esa carpeta, y mete dos prefijos que
  colisionan con el registro; (3) esperar a que `005_discovery` declare las etapas — el archivo no
  cuesta nada ahora y el borrador existe hoy; escrito mas tarde se reconstruye peor.
- **Clasificacion:** **reversible a criterio** — se añade un archivo nuevo a una carpeta agnostica,
  no se adopta ninguna etapa, no se toca `project.md` y nada depende todavia de el.

**Verificacion — el archivo existe, y la tabla de etapas sigue diciendo dos:**

```
$ ls -1 _phases/
000_preproject.md
005_discovery.md
010_prototype.md
020_baseline.md

$ grep -n "Etapas declaradas" project.md
105:| Etapas declaradas | `000_preproject`, `005_discovery` |

$ grep -nE "(N|T|D|A|C|I|F|L|S|R|DT)-[0-9]{3}" _phases/020_baseline.md ; echo "exit=$?"
exit=1

$ grep -rnE "RaindomAI|RaidomAI|Proyectos_TripleS|github.com" _phases/020_baseline.md ; echo "exit=$?"
exit=1
```


---

### D-073 - Las plantillas de la baseline se numeran por orden de procedimiento, no por el orden de la tabla de artefactos
| Campo | Valor |
|---|---|
| Fecha | 2026-09-03 |
| Estado | Vigente |
| Origen | manager |

- **Contexto:** el usuario pidio construir las plantillas de los entregables de la etapa de la
  baseline en `_templates/020_baseline/`, agnosticas y alineadas con `_phases/020_baseline.md` y
  `_methodology/000_method.md`, tomando como guia las de `_templates/005_discovery/` y
  `_templates/010_prototype/`. La tabla de artefactos de `_phases/020_baseline.md` §5 los lista en
  un orden —producto, alcance, features, escenarios, especificacion, arquitectura, tres preguntas,
  trazabilidad, decisiones arquitectonicas— que **no** coincide con el orden en que el §4 los manda
  escribir: el alcance es el Paso 2 y el documento de producto el Paso 4.
- **Decision:** las nueve plantillas se numeran por **orden de procedimiento**, y cada una declara
  en su cabecera de que Paso sale. Queda: `005_scope` (Paso 2), `010_product` (Paso 4),
  `015_features` y `020_scenarios` (Paso 5), `025_specification` (Paso 6), `030_architecture`
  (Paso 7), `035_adr_NNN` (Paso 8), `040_three_questions` (Paso 9), `045_traceability` (Paso 10).
- **Por que:** es el criterio que ya siguen las plantillas de `_templates/010_prototype/`, cuyos
  numeros van con los Pasos 2, 3, 7, 8 y 9 de su etapa. Y hay una razon de fondo: el documento de
  producto **copia** las dos listas del alcance, y la trazabilidad **deriva** de features y
  escenarios. Numerarlas al reves invita a escribirlas al reves, y escrito al reves el alcance se
  inventa dos veces y la trazabilidad deja de ser un control para volverse una copia.
- **Alternativas descartadas:** (1) seguir el orden de la tabla §5 — coincidiria con el archivo de
  etapa, pero pone primero un artefacto que depende de otro y contradice el precedente del
  prototipo; (2) numerarlas y ademas reordenar la tabla §5 para que cuadren — toca un archivo ya
  auditado por un motivo cosmetico, y `PI-3` lo desaconseja; (3) no numerarlas y usar solo nombres
  — las otras dos carpetas de plantillas si numeran, y romper la convencion en la tercera obliga a
  explicarlo cada vez.
- **Clasificacion:** **reversible a criterio** — son archivos nuevos en una carpeta agnostica, sin
  etapa adoptada, sin artefacto escrito todavia contra ellos y sin nada que dependa de sus nombres.

**Verificacion — las nueve existen, y ni fuga de datos propios ni codigos instanciados del registro
mas alla del primero que la regla de `_templates/` permite:**

```
$ ls -1 _templates/020_baseline/
005_scope.md
010_product.md
015_features.md
020_scenarios.md
025_specification.md
030_architecture.md
035_adr_NNN.md
040_three_questions.md
045_traceability.md

$ grep -rnE "RaindomAI|RaidomAI|Proyectos_TripleS|github.com" _templates/020_baseline/ ; echo "exit=$?"
exit=1

$ grep -rnoE "\b(N|T|D|A|C|I|F|L|S|R|DT)-[0-9]{3}\b" _templates/020_baseline/
_templates/020_baseline/015_features.md:189:N-001
_templates/020_baseline/045_traceability.md:199:N-001
```


---

### D-074 - La seccion 5 del archivo de etapa de la baseline dice nueve artefactos, no ocho
| Campo | Valor |
|---|---|
| Fecha | 2026-09-03 |
| Estado | Vigente |
| Origen | usuario |

- **Contexto:** al escribir las plantillas de `_templates/020_baseline/` (`D-073`) hizo falta saber
  cuantos artefactos produce la etapa. `_phases/020_baseline.md` §5 abria con «Ocho artefactos de
  registro, mas el esqueleto del repositorio» y su tabla listaba **nueve** filas. Las dos lecturas
  posibles eran distintas: o el texto se quedo atras, o el conteo excluia a proposito las decisiones
  arquitectonicas por vivir en subcarpeta.
- **Decision:** el usuario zanja que **son nueve**. El texto pasa a «Nueve artefactos de registro»;
  la tabla no se toca.
- **Por que asi y no al reves:** la tabla es el contenido y el numero en prosa es su duplicado, que
  es justo la forma de desincronizarse que `L-004` ya tenia registrada. Corregir el duplicado y
  dejar el original es la direccion barata; la contraria habria obligado a decidir que fila sobra.
- **Alternativas descartadas:** (1) dejar el texto y anotar la discrepancia — deja al lector
  siguiente eligiendo entre dos cifras, que es el estado que la correccion existe para terminar;
  (2) quitar la fila de decisiones arquitectonicas de la tabla para que cuadre en ocho — el propio
  §5 la nombra con su subcarpeta y §4 tiene un Paso entero para ella; (3) sustituir el numero por
  «los artefactos» sin cifra — evita el defecto pero pierde el recuento que hace comprobable la
  condicion de salida.
- **Clasificacion:** **reversible a criterio** — es una palabra en un archivo de metodo, sin etapa
  adoptada y sin ningun artefacto escrito todavia contra el.

**Verificacion — el texto y la tabla dicen ahora el mismo numero:**

```
$ sed -n '287p' _phases/020_baseline.md
Nueve artefactos de registro, mas el esqueleto del repositorio. **Ninguno es codigo de producto.**

$ sed -n '/^## 5. Artefactos que produce/,/^Y \*\*el esqueleto/p' _phases/020_baseline.md | grep -c "^| \*\*"
9

$ grep -nEi "\bocho\b" _phases/020_baseline.md ; echo "exit=$?"
exit=1
```
