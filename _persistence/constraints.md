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
