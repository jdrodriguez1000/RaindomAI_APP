# constraints.md

> Registro de las **limitaciones y restricciones** del proyecto: lo que obliga o impide,
> y no es negociable. Cada restriccion tiene codigo `C-XXX`.
> Lo que aun no esta confirmado no va aqui, va en `assumptions.md`.

---

## Indice

| Codigo | Restriccion | Tipo | Estado |
|---|---|---|---|
| [C-001](#c-001---el-producto-no-puede-depender-de-una-api-de-modelo-generativo) | El producto no puede depender de una API de modelo generativo | Negocio | Vigente |
| [C-002](#c-002---el-producto-se-despliega-en-vercel) | El producto se despliega en Vercel | Tecnica | Vigente |
| [C-003](#c-003---etapa-actual-000_preproject) | Etapa actual `000_preproject` | Proceso | Vigente |
| [C-004](#c-004---entorno-de-ejecucion-windows) | Entorno de ejecucion Windows | Entorno | Vigente |
| [C-005](#c-005---el-idioma-del-contenido-y-el-de-los-nombres-son-distintos) | El idioma del contenido y el de los nombres son distintos | Proceso | Vigente |
| [C-006](#c-006---los-principios-de-ingenieria-y-las-reglas-de-operacion-son-vinculantes) | Los principios de ingenieria y las reglas de operacion son vinculantes | Proceso | Vigente |
| [C-007](#c-007---las-fuentes-de-la-guia-de-metodo-no-se-editan) | Las fuentes de la guia de metodo no se editan | Proceso | Vigente |
| [C-008](#c-008---el-repositorio-no-tiene-un-final-de-linea-unico-y-no-se-normaliza) | El repositorio no tiene un final de linea unico, y no se normaliza | Entorno | Vigente |
| [C-009](#c-009---el-inventario-de-acciones-irreversibles-del-proyecto) | El inventario de acciones irreversibles del proyecto | Proceso | Vigente |

---

## Convenciones

| Campo | Valores posibles |
|---|---|
| Codigo | `C-XXX`, correlativo, no se reutiliza |
| Tipo | `Proceso` / `Tecnica` / `Negocio` / `Entorno` |
| Estado | `Vigente` / `Levantada` |
| Origen | `usuario` / `manager` / `report_auditor` |

🚨 **Aqui entra solo lo confirmado.** Una limitacion que se supone pero nadie ha confirmado es un
`A-XXX` en `assumptions.md`; llega aqui cuando se confirma.

⚠️ **Una restriccion no repite datos que viven en otro archivo.** Lo que obliga es el enunciado; si
para cumplir su funcion necesita una ruta, un nombre o un valor concreto, se referencia donde vive
y no se copia. Un duplicado obliga a acordarse de dos sitios cada vez que uno cambia.

🚨 **El indice se escribe a mano, sin generador.** Cada fila enlaza por ancla a su restriccion.

---

## Restricciones

### C-001 - El producto no puede depender de una API de modelo generativo
| Campo | Valor |
|---|---|
| Tipo | Negocio |
| Origen | usuario |
| Estado | Vigente |

- **Restriccion:** la aplicacion no realizara llamadas a OpenAI, Anthropic, Google Gemini ni a
  ningun otro modelo de lenguaje generativo. Su logica —generacion de numeros, analisis estadistico,
  comparacion de resultados— se ejecuta con codigo convencional y algoritmos determinísticos o
  aleatorios segun corresponda.
- **Implicacion:** ninguna decision tecnica puede apoyarse en un modelo como componente del
  producto. La IA si se usa **como asistente de desarrollo**, y esa distincion tiene que quedar
  clara en cualquier documento que hable del sistema.
- **Origen del dato:** `_brief/client_brief.md`, §21 y §19, enunciado por el cliente.

⚠️ **El nombre del proyecto tira en contra de esta restriccion.** `RaindomAI` lleva «AI» dentro y el
repositorio se llama igual. No es una contradiccion real —la IA es el asistente, no el motor— pero
es exactamente el tipo de detalle que confunde a quien llegue despues.

---

### C-002 - El producto se despliega en Vercel
| Campo | Valor |
|---|---|
| Tipo | Tecnica |
| Origen | usuario |
| Estado | Vigente |

- **Restriccion:** la aplicacion debe estar diseñada para desplegarse en Vercel: frontend, backend o
  API si hace falta, almacenamiento persistente, variables de entorno, tareas programadas y la
  conexion con la fuente externa de datos.
- **Implicacion:** las capacidades y los limites de esa plataforma acotan las decisiones de
  arquitectura antes de tomarlas, no despues. La arquitectura se mantiene lo mas sencilla posible,
  sin infraestructura adicional que el MVP no necesite.
- **Origen del dato:** `_brief/client_brief.md`, §24, enunciado por el cliente.

---

### C-003 - Etapa actual `000_preproject`
| Campo | Valor |
|---|---|
| Tipo | Proceso |
| Origen | usuario |
| Estado | Vigente |

- **Restriccion:** en esta etapa no se construye producto. Se monta la forma de trabajar
  —protocolos, persistencia, registro, auditoria—.
- **Implicacion:** no se toman decisiones de arquitectura, stack ni producto todavia, aunque el
  brief ya describa la aplicacion. Que un requisito este enunciado no significa que este decidido
  como se resuelve.

⚠️ **Que etapas vienen despues no esta decidido.** El brief propone una secuencia en su §22, pero un
encargo no es una decision: adoptarla exigiria su `D-XXX`, y hoy no existe.

---

### C-004 - Entorno de ejecucion Windows
| Campo | Valor |
|---|---|
| Tipo | Entorno |
| Origen | usuario |
| Estado | Vigente |

- **Restriccion:** el trabajo se ejecuta sobre Windows, con PowerShell y Git Bash disponibles.
- **Implicacion:** todo comando que se escriba en un protocolo tiene que correr en ese entorno. Por
  eso las rutas relativas de `project.md` se declaran en forma canonica con separador `/`: funcionan
  igual en los dos interpretes, mientras que la forma con `\` solo funciona en uno.

---

### C-005 - El idioma del contenido y el de los nombres son distintos
| Campo | Valor |
|---|---|
| Tipo | Proceso |
| Origen | usuario |
| Estado | Vigente |

- **Restriccion:** la conversacion, los reportes de los agentes y toda la documentacion se escriben
  en **espanol**; los nombres de archivos y de carpetas, en **ingles**. El enunciado completo vive
  en la seccion «Idioma» de `CLAUDE.md`, y el porque en `D-017`.
- **Implicacion:** afecta a cada archivo que se cree a partir de ahora, no solo a los de codigo.
  Un artefacto nuevo con nombre en espanol incumple, aunque su contenido sea correcto.
- **No es retroactiva:** lo heredado no se renombra por esta restriccion sola. Lo que ya incumple
  se deja y se registra como deuda tecnica — hoy, `DT-001`.

---

### C-006 - Los principios de ingenieria y las reglas de operacion son vinculantes
| Campo | Valor |
|---|---|
| Tipo | Proceso |
| Origen | usuario |
| Estado | Vigente |

- **Restriccion:** los cinco principios `PI-1`..`PI-5` y las siete reglas de operacion de
  `CLAUDE.md` obligan a cualquiera que trabaje en este repositorio, `manager` y agentes incluidos.
  El enunciado vive en `CLAUDE.md` y el porque en `D-018`; aqui no se copia.
- **Implicacion:** ninguna tarea se da por terminada sin su Definicion de Terminado —test en verde
  si produce codigo, bloque de verificacion si produce documentacion—, y ninguna ambiguedad se
  resuelve en silencio: se consulta.
- **Donde muerde de verdad:** «Separacion de roles» y «Revision independiente» prohiben que quien
  construyo evalue lo construido. Es la restriccion que `report_auditor` existe para hacer cumplir,
  y la unica que se rompe sin que nadie lo note si no se lanza.

---

### C-007 - Las fuentes de la guia de metodo no se editan
| Campo | Valor |
|---|---|
| Tipo | Proceso |
| Origen | usuario |
| Estado | Vigente |

- **Restriccion:** los tres archivos de `_methodology/sources/` se conservan **intactos**. No se
  corrigen, no se actualizan y no se alinean con el documento canonico, ni siquiera cuando este los
  contradice. El enunciado vive en el encabezado de `_methodology/000_method.md` y llego con el
  material; aqui no se copia.
- **Implicacion:** toda correccion del metodo se hace en `000_method.md`, y cuando el cambio
  contradice una fuente **se registra en su Anexo A** en vez de tocarla. Una fuente que se edita para
  que cuadre deja de ser fuente: pasa a ser una segunda copia del documento canonico, y entonces ya
  no se puede saber que decia el material original.
- **Donde muerde de verdad:** las fuentes conservan identificadores que el documento canonico ya
  cambio —`F-` para feature y `S-` para scenario, que `D-030` renombro a `FT-` y `SC-`—. Un barrido
  sobre `_methodology/` que espere cero apariciones **las va a encontrar, y es correcto que las
  encuentre**. Cualquier control que se escriba sobre esa carpeta tiene que acotar su ambito a
  `000_method.md`, o contar con ellas.
- **Lo que la restriccion NO impide:** el control de fuga de datos propios del Paso 1b, que si cubre
  `sources/` —ese barrido espera cero y hoy da cero—. Conservar el material original no autoriza a
  que lleve dentro datos de este proyecto; si algun dia los llevara, seria un hallazgo.

---

### C-008 - El repositorio no tiene un final de linea unico, y no se normaliza
| Campo | Valor |
|---|---|
| Tipo | Entorno |
| Origen | manager |
| Estado | Vigente |

- **Restriccion:** los archivos versionados de este repositorio **conviven con dos finales de linea
  distintos**. No es una hipotesis: se midio, y la orden y su salida estan en `L-032`.
- **Y no se normalizan.** Cambiar el final de linea de un archivo lo marca **entero** como modificado
  en el `git diff`, y eso sepultaria el cambio real de esa sesion bajo miles de lineas — que es
  exactamente lo que la auditoria necesita poder leer. El coste de normalizar se paga una vez y el de
  convivir se paga cada vez, pero el primero se paga **contra la auditabilidad**, que es lo unico que
  este repositorio no negocia.
- **Implicacion:** **toda edicion automatizada detecta el final de linea del archivo antes de
  construir su patron.** Un patron escrito con un solo salto de linea no aparece nunca en un archivo
  con el otro, y el error que devuelve —«no encontrado»— manda a buscar una diferencia de texto que no
  existe. El modo de fallo es benigno pero empuja a reintentar con patrones cada vez mas cortos, hasta
  que uno coincide por casualidad en un sitio que no era; ese si escribe.
- **Complementa a `C-004`**, que fija el entorno; esto fija una consecuencia suya que `C-004` no
  nombraba.

---

### C-009 - El inventario de acciones irreversibles del proyecto
| Campo | Valor |
|---|---|
| Tipo | Proceso |
| Estado | Vigente |
| Origen | usuario |

**Que obliga:** antes de ejecutar una accion de la primera tabla, **se pide permiso al usuario**.
Las de la segunda se ejecutan y se revisan despues. La clasificacion se lee **de aqui**, no se
improvisa en la respuesta.

🔑 **Por que existe una lista y no un criterio:** un criterio se aplica el dia que hace falta, con
prisa y con el trabajo a medio hacer — que es justo cuando peor se juzga. La lista se escribe antes
de necesitarla. Hasta hoy, cada clasificacion se declaraba a mano en la propia respuesta, que es una
regla sin mecanismo: funciona mientras alguien se acuerde.

#### Irreversible — permiso antes

| Accion | Por que no se deshace |
|---|---|
| `git push` al remoto | el historial publicado ya lo pudo clonar cualquiera; un `push --force` posterior no lo retira de donde ya esta |
| Escribir en el repositorio de lecciones globales | vive fuera de este repositorio y lo comparten otros proyectos: una entrada mala la heredan todos. Por eso su protocolo lleva puerta explicita |
| Escribir en el repositorio del esqueleto de arranque | igual que el anterior: vive fuera y de el partiran todos los proyectos nuevos, asi que un error se hereda hacia adelante. Su promocion lleva la misma puerta (`D-145`, `D-146`) |
| Desplegar a la plataforma | lo publicado queda accesible desde fuera, y puede quedar cacheado o indexado aunque se retire despues |
| Gastar en la plataforma de despliegue | el consumo facturado no se revierte borrando lo que lo causo |
| Datos que registre una persona usuaria | son dato personal: sobreviven al proyecto y su borrado no es cosa nuestra sola |
| Peticiones a la fuente oficial de datos | salen de nuestra maquina hacia un tercero: quedan en **su** registro, y el volumen puede afectar al trato que nos den |
| Borrar o reescribir una entrada del registro | el registro existe para decir lo que paso; reescribirlo no corrige el pasado, lo falsifica. La salida siempre es la nota fechada |
| Reescribir el historial ya publicado | `rebase`, `amend` o `--force` sobre lo que ya esta en el remoto rompen lo que otros tengan clonado |

#### Reversible — se hace y se revisa despues

| Accion | Por que se deshace |
|---|---|
| Escribir o editar codigo y archivos del arbol | mientras no este commiteado, `git checkout` lo devuelve; commiteado y sin subir, tambien |
| Un commit local | se revierte, se enmienda o se descarta sin que nadie mas lo haya visto |
| Editar una skill, un archivo de etapa o una plantilla | un commit lo revierte entero, y no toca ningun dato |
| Anadir una entrada nueva al registro | lo que se anade se puede anotar despues; lo irreversible es **quitar**, no poner |
| Crear o borrar una rama local | no ha salido de esta maquina |
| Correr un control, un barrido o un test | son de solo lectura sobre el arbol |

⚠️ **Las dos tablas importan, y la segunda no es relleno.** Una lista que solo enumera peligros se
lee como una lista de prohibiciones, y entonces se deja de consultar y todo empieza a parecer
delicado. Saber que algo **si** se deshace es lo que permite trabajar sin pedir permiso cada vez.

🚨 **Lo que no este en ninguna de las dos se clasifica a criterio, y se dice.** El inventario no
pretende ser completo: pretende que lo conocido no se decida improvisando. Ante una accion que no
aparece aqui, se declara la clasificacion en la propia respuesta —«lo clasifico como reversible a
criterio, porque…»— y, si se repite, **se anade a la tabla que le toque**. Un criterio declarado como
criterio se puede discutir; uno disfrazado de tabla, no.

⛔ **Esta entrada no decide permisos ni frenos, solo clasifica.** Como se pide el permiso, quien lo
da y que pasa si no llega es otra cosa, y viene despues de tener la lista, no antes.

- **Que la origina:** `T-037`, y una leccion global que pide escribir el inventario **antes** de
  necesitarlo. Su decision es `D-141`.

📌 **Nota del 2026-09-11 (`D-145`): la primera tabla crece por primera vez, y por la via prevista.**
La entrada decia que el inventario «no se levanta por si solo; crece». Al adoptarse el esqueleto de
arranque aparece un segundo repositorio externo con la misma naturaleza que el de lecciones, y entra
en la tabla con su `D-XXX` en la misma pasada en que nacio — no despues.
- **Se levanta cuando:** no se levanta por si sola; crece. Si una accion cambia de naturaleza
  —porque cambia la plataforma, la fuente o el trato con los datos— se mueve de tabla **con su
  `D-XXX`**, nunca en silencio.
