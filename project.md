# project.md

> **Los datos propios de este proyecto, en un solo sitio.** Todo lo que en los protocolos, agentes
> y `CLAUDE.md` aparece como «el proyecto», «el remoto» o «las carpetas declaradas» se
> resuelve aqui.
>
> 🔑 **Es lo unico que cambia al llevar este metodo a otro proyecto.** Si un archivo necesita saber
> un nombre o una ruta, lo lee de aqui en vez de llevarlo escrito dentro.

---

## Identidad

| Campo | Valor |
|---|---|
| Nombre del proyecto | RaindomAI |
| Rol de esta sesion | `manager` |
| Auditoria | agente `report_auditor`, dentro de este mismo repositorio |
| Idioma de trabajo | **espanol** para la comunicacion y la documentacion; **ingles** para los nombres de archivos y de carpetas |
| Etapa actual | vive en `_persistence/progress.md`, no aqui |

📌 **La grafia correcta es `RaindomAI`** —con `n`—, y coincide con el remoto. La carpeta de
trabajo en disco se llama `RaidomAI_App`, sin la `n`; **eso no afecta a ningun control**, porque el
Paso 1b de `protocol-close` toma de las rutas absolutas el segmento comun `Proyectos_TripleS`, no el
nombre de la carpeta del repositorio. Se deja anotado para que la diferencia no se lea como un error
la proxima vez que alguien la vea.

## Rutas

| Campo | Valor |
|---|---|
| Repositorio del proyecto | `C:\Users\USUARIO\Documents\Company_TripleS\Proyectos_TripleS\RaidomAI_App` |
| Informes de sesion | `_audit/S-XXX.md` |
| Auditorias | `_audit/R-XXX.md` |
| Tablero de auditorias | `_audit/index.md` |
| Estado de los hallazgos | `_audit/findings.md` |
| Entregables de `010_prototype` | `010_prototype/` (el codigo descartable, en una subcarpeta suya) |
| Lecciones globales — repositorio | `C:\Users\USUARIO\Documents\Company_TripleS\TripleS_Lessons` |
| Lecciones globales — archivo | `global_lessons.md`, en la raiz de ese repositorio |
| Lecciones globales — remoto | `https://github.com/jdrodriguez1000/TripleS_Lessons.git` (privado) |
| Esqueleto de arranque — repositorio | `C:\Users\USUARIO\Documents\Company_TripleS\SDAI_TripleS` |
| Esqueleto de arranque — remoto | `https://github.com/jdrodriguez1000/SDAI_TripleS.git` (privado) |

🔑 **Forma canonica: relativa y con `/`.** Las rutas relativas de esta tabla se escriben **tal
como se pegan en un comando**, con separador `/` y desde la raiz de este repositorio. Es la unica
forma valida, y por una razon concreta: funciona igual en Bash y en PowerShell. Quien copie un valor
de aqui a un bloque `bash` obtiene una orden que corre; no una que hay que traducir antes.

⚠️ **Las tres rutas absolutas de arriba son excepciones declaradas**, no una segunda forma a elegir:
existen porque nombran **una ubicacion en esta maquina** —la de este repositorio, la del
repositorio de lecciones y la del esqueleto de arranque—, no porque sirvan para navegar dentro de
ellos. **Para citar un archivo
del proyecto se usa la relativa.**

📌 **Las tres filas de «Lecciones globales» son la ubicacion que `CLAUDE.md` no puede llevar
dentro.** La regla —que existen, para que sirven y cuando se consultan— vive en `CLAUDE.md`, que es
copiable y por eso no nombra ni una ruta. **El donde vive aqui**, que es el unico archivo del
proyecto que guarda datos propios. Si el repositorio de lecciones se mueve, se cambia en un sitio.

⚠️ **Ese repositorio no es una carpeta de este proyecto**, y por eso **no** le toca fila en
«Carpetas propias» ni la mira el control de carpetas del cierre. Es un recurso externo que se
consulta, como lo seria una documentacion en linea.

📌 **Las dos filas de «Esqueleto de arranque» son la ubicacion que ni `CLAUDE.md` ni las skills pueden
llevar dentro**, por la misma razon que las de lecciones globales: los dos mecanismos que usan ese
dato —el barrido de desfase del cierre y la promocion del andamiaje— viven en archivos que tienen que
poder copiarse a otro proyecto tal cual. **El donde vive aqui.** Si el esqueleto se mueve, se cambia
en un sitio.

🚨 **Y va con una nota que no aplicara a ningun otro proyecto: este proyecto NO salio del esqueleto —
el esqueleto salio de este proyecto.** Todos los proyectos siguientes arrancaran clonandolo y llevaran
una fila mas, «version del esqueleto de la que partio», con el hash de origen. Este no la lleva, y no
es un olvido: es el unico que no puede llevarla.

🔑 **Sin esta nota el hueco se lee como un descuido.** Dentro de un ano, alguien que compare este
`project.md` con el de otro proyecto vera que aqui falta una fila y no tendra forma de saber si falta
por error o si nunca existio. La nota contesta eso de antemano, que es lo unico que no se puede
reconstruir despues.

⚠️ **Ese repositorio tampoco es una carpeta de este proyecto**, igual que el de lecciones: **no** le
toca fila en «Carpetas propias» ni lo mira el control de carpetas del cierre.

## Reparto de autoridad

| Actor | Que hace | Que NO hace |
|---|---|---|
| **usuario** | decide alcance, prioridades y lo irreversible | — |
| **`manager`** (esta sesion) | dirige, coordina, construye, y registra el porque en el momento | **no audita su propio trabajo** |
| **`report_auditor`** (agente) | audita un commit ya cerrado, verifica y recomienda | **no construye, no corrige, no decide** |
| **`gate1_auditor`** (agente) | emite el **dictamen tecnico** del Gate 1 sobre la evidencia del prototipo | **no construye, no corrige, y no decide si se construye el MVP** |
| **`gate2_auditor`** (agente) | emite el **dictamen tecnico** del Gate 2 sobre la evidencia del crecimiento | **no construye, no corrige, y no decide si se sigue invirtiendo** |
| **`phase_exit_auditor`** (agente) | emite la **revision tecnica** del acta de cierre de una etapa: verifica sus casillas de salida una por una | **no construye, no corrige, y no decide si la etapa esta cerrada** |

🚨 **Un Gate necesita dos firmas, y ninguna sustituye a la otra.** `gate1_auditor` dice si la
evidencia satisface los criterios, uno por uno, y ahi termina su papel; **quien decide si se
construye el MVP, se replantea o se detiene es el usuario, como patrocinador**, y esa decision queda
en `_persistence/decisions.md` con su `D-XXX`. Auditar y decidir son papeles incompatibles: quien
decide asume la consecuencia de la inversion, y quien la asume ya no puede señalar el error de esa
decision en la pasada siguiente.

⚠️ **El patrocinador puede decidir contra el dictamen; lo que no puede es cambiarlo.** Un criterio
`NO CUMPLE` es un hecho verificable contra los archivos. Si se decide construir igual, la `D-XXX`
dice por que — y eso vale mucho mas que un dictamen ablandado.

🚨 **Quien construye no puede ser su propio testigo, y por eso el auditor es un agente aparte.**
Arranca en frio: no vio la conversacion de la jornada, y solo puede leer archivos y `git`. Esa
distancia es toda su utilidad — un auditor al que se le cuenta lo que paso deja de auditar y pasa
a confirmar.

⚠️ **Y aqui esta el limite honesto de este esquema, escrito para que no se olvide:** a diferencia
de un auditor externo, **a este lo lanza el propio auditado**. Si `manager` no lo lanza, no hay
auditoria y nadie lo nota. Por eso lanzarlo **no es opcional ni queda a criterio**: es el ultimo
paso del cierre de sesion, igual que el arranque se dispara con la primera peticion y no con un
momento de arranque que nunca llega.

🚨 **Una recomendacion del auditor no se ejecuta por venir de el.** Entra como tarea con
`Origen: report_auditor` en `_persistence/tasks.md`, y solo despues de que `manager` la evalue y la
considere correcta. El rechazo tambien se registra, con su `D-XXX`.

🚨 **El estado de un hallazgo solo lo cambia una auditoria, nunca `manager`.** Un hallazgo se
cierra **verificando la correccion sobre un commit posterior**, y eso lo hace el auditor en su
siguiente pasada. Que nos parezca resuelto no lo resuelve: si el auditado pudiera cerrar sus propios
hallazgos, el registro diria lo que quisieramos que dijera.

## Etapas

| Campo | Valor |
|---|---|
| Etapas declaradas | `000_preproject`, `005_discovery`, `010_prototype`, `020_baseline`, `025_wslt`, `030_growth`, `040_evol` |
| Secuencia adoptada | `000_preproject` → `005_discovery` → `010_prototype` → **[Gate 1]** → `020_baseline` → `025_wslt` → `030_growth` → **[Gate 2]** → `040_evol` |

`000_preproject` es la etapa en la que no se construye producto: se monta la forma de trabajar
—protocolos, persistencia, canal con la auditoria—. Es deliberado que tenga nombre propio y no un
numero del flujo del producto: meterla en la nomenclatura de las demas seria fingir que el producto
avanza cuando lo que avanza es el andamio.

`005_discovery` es la etapa siguiente: la que define **alcance y objetivo** del proyecto, trabajo que
`000_preproject` tiene expresamente prohibido. Lo fija `D-024`, por decision del usuario.

📌 **Las etapas posteriores quedaron adoptadas el 2026-09-10 por `D-142`, por decision del usuario.**
Hasta entonces esta tabla declaraba dos etapas y decia que lo demas seguia sin decidir. Lo adoptado
es la secuencia del **metodo VERTICAL** —la que describe la guia de metodo en su ciclo completo—, y
cada etapa tiene ya su archivo en `_phases/`.

⚠️ **Se descarto la secuencia del brief del cliente** (`_brief/client_brief.md`, §22: Idea →
Definicion del producto → Especificacion → Diseño → Desarrollo asistido por IA → Pruebas →
Iteracion). No por ser peor, sino porque **un encargo no es una decision** y porque adoptarla habria
obligado a escribir siete archivos de etapa nuevos y a decidir que pasaba con los Gates y con los
siete ya escritos. El porque completo vive en `D-142`, no aqui.

🚨 **Que `_methodology/000_method.md` describa un ciclo completo no declara ninguna de sus
etapas.** Ese archivo es la **guia de metodo**: dice que etapas existen en el metodo y que pregunta
responde cada una. Lo que este proyecto ha adoptado es lo que diga la tabla de arriba —hoy, las
siete—, y lo adoptado lo fija una decision, no la guia. Adoptar cualquier otra exigiria su `D-XXX` y
su archivo en `_phases/`. **Una guia no es un acta**, aunque esta vez el acta diga lo mismo que la
guia.

### Un Gate no es una etapa

🚨 **Los Gates del metodo no se declaran en la tabla de arriba, y no tienen archivo en `_phases/`.**
Una etapa es un **tramo de trabajo**: dura sesiones, autoriza producir unas cosas y prohibe otras, y
acumula artefactos. Un Gate es un **acto de juicio**: lee evidencia ya escrita, la contrasta contra
unos criterios y devuelve un dictamen. No produce producto y no dura.

Por eso un Gate se monta con la misma forma que los demas actos del repositorio —**un agente y su
skill**—, y no con un archivo de etapa. Lo fija `D-067`.

| Gate | Agente | Skill | Donde deja su dictamen |
|---|---|---|---|
| **Gate 1** — ¿vale la pena construir el MVP? | `gate1_auditor` | `protocol-gate1` | `_audit/015_gate1/` |
| **Gate 2** — ¿vale la pena seguir invirtiendo? | `gate2_auditor` | `protocol-gate2` | `_audit/035_gate2/` |

⚠️ **El prefijo numerico marca donde cae en el ciclo, no que sea una etapa.** `015_` se eligio
para que se lea junto a `010_prototype`, y `035_` junto a `030_growth` — en cada caso, la etapa cuya
evidencia juzga.

📌 **El Gate 2 se monto en `S-023`, por peticion del usuario** (`D-094`). Hasta entonces este
archivo decia que no se adelantaba; se adelanto porque se pidio, y el porque vive en esa decision, no
aqui. **Adoptar un Gate no adopta su etapa**, y durante quince sesiones fue asi: el Gate 2 existia
mientras `030_growth` no estaba declarada. Desde `D-142` las dos cosas coinciden, pero **siguen
siendo independientes** — montar un Gate no declara nada, y declarar una etapa no monta su Gate.

🔑 **Lo que el segundo comparte con el primero, ahora que existe:** la forma —agente y skill—, el
vocabulario del dictamen —`CRITERIOS SATISFECHOS`, `CRITERIOS NO SATISFECHOS`, `NO AUDITABLE`—, la
regla de las dos firmas, y que su ultimo criterio es del patrocinador y no se evalua.

⚠️ **Y lo que NO comparte, que es lo que obligo a escribirlo entero en vez de copiarlo:** el
primero comprueba que la **evidencia** naciera antes de las sesiones; el segundo comprueba que la
**medicion** —metrica, ventana y umbral— naciera antes del primer dato, y ademas **quien genero el
uso**. Son dos comprobaciones que el primero no tiene y que aqui deciden el dictamen.

⚠️ **Aqui va el vocabulario, no el avance: que etapas existen, no en cual estamos.** En cual
estamos vive en `_persistence/progress.md`, que es lo que cambia. Declararlo tambien aqui crearia
dos sitios que hay que acordarse de actualizar a la vez, y el dia que uno se olvide habria que
decidir cual miente.

## Control de versiones

| Campo | Valor |
|---|---|
| Remoto | `https://github.com/jdrodriguez1000/RaindomAI_APP.git` |
| Rama principal | `main` |
| Host del remoto | `github.com` |

📌 **La fila «Host del remoto» existe para el Paso 1b de `protocol-close`**, que la usa literal
dentro de su patron de busqueda. Va separada del remoto completo a proposito: buscar la URL entera
no encontraria una fuga escrita como `github.com/otra-cosa`, y buscar `github` a secas devolveria
cada mencion legitima de la palabra. **Un control que devuelve ruido acaba apagado.**

## Carpetas propias

| Carpeta | Que es |
|---|---|
| `.claude/` | **Con que** se construye: los agentes y las skills que ejecutan los protocolos. Agnostica — no lleva dentro ningun dato de este proyecto, y el Paso 1b lo comprueba |
| `_brief/` | El encargo del cliente, tal como llego. **Entrada al proyecto, no registro de el** |
| `_persistence/` | **Como va** el trabajo: siete archivos, indice arriba y detalle debajo |
| `_audit/` | **Como se comprueba** el trabajo: el informe de cada sesion, la auditoria de cada una, el tablero y el registro de hallazgos. En `015_gate1/` y `035_gate2/`, ademas, los dictamenes de cada Gate; y en una subcarpeta con el nombre de cada etapa, las **actas de cierre de esa etapa**. Ni unos ni otras son auditorias de sesion: **no** entran en el tablero ni en `findings.md` |
| `_methodology/` | **Con que criterio** se construye: el metodo de desarrollo —`000_method.md`, el documento canonico— y en `sources/` las fuentes de las que se consolido, que no se editan. Agnostica — no lleva dentro ningun dato de este proyecto, y el Paso 1b lo comprueba |
| `_phases/` | **Que se hace en cada etapa**: un archivo por etapa declarada, con lo que autoriza, lo que prohibe, su procedimiento y su condicion de salida. Agnostica — no lleva dentro ningun dato de este proyecto, y el Paso 1b lo comprueba |
| `_templates/` | **Con que forma** se escribe cada artefacto: una subcarpeta por **etapa o gate** que tenga artefactos con plantilla, y dentro una plantilla por artefacto. Guarda solo plantillas en blanco; lo relleno vive en la carpeta de su etapa —o, para un gate, en `_audit/`. Agnostica — no lleva dentro ningun dato de este proyecto, y el Paso 1b lo comprueba |
| `_workflow/` | **Quien hace cada cosa y con cuanto sistema**: `team.md`, el reparto del trabajo entre Humano, Software e IA; `ai_levels.md`, los niveles de sistema de IA y la rubrica para elegir uno; y **un archivo por etapa** que aplica los dos a sus actividades, con el mismo nombre que la etapa. Aplica a todas las etapas declaradas salvo `000_preproject`. Agnostica — no lleva dentro ningun dato de este proyecto, y el Paso 1b lo comprueba |
| `010_prototype/` | **Los entregables de la etapa `010_prototype`**: los cinco artefactos de registro en su raiz, y el codigo descartable del prototipo en una subcarpeta suya. Se archiva o se borra al cerrar su Gate — **no se muda a ninguna carpeta de producto** |
| `_outbound/` | **Lo redactado aqui cuyo destino es OTRO repositorio**, esperando su puerta. Un archivo por pieza; se borra cuando la pieza se publica fuera |
| `temporal/` | Area de trabajo del usuario. **Fuera del repositorio**, excluida en `.gitignore` |

🚨 **Esta tabla se contrasta contra el arbol en cada cierre de sesion** (Paso 2c de `protocol-close`):
las carpetas de primer nivel que existen, frente a las filas de aqui, **en las dos direcciones**. Una
carpeta sin declarar y una fila sin carpeta son el mismo defecto por sus dos caras.

🔑 **La convencion de las carpetas de entregables: se llaman como su etapa.** Una etapa que produzca
artefactos tiene **una carpeta de primer nivel con el mismo nombre que la etapa** —el mismo que
lleva su archivo en `_phases/` y su subcarpeta en `_templates/`—, y dentro van sus entregables. No
hay un prefijo distinto ni una carpeta contenedora: **el nombre de la etapa es la unica coordenada
que hay que recordar**, y sirve para los cuatro sitios. Cada carpeta nace cuando su etapa arranca,
no todas de golpe.

⚠️ **Dos filas van a salir señaladas por ese control, y aqui estan escritas sus razones:**

- **`temporal/`** existe en disco pero **nunca aparecera en el arbol versionado**, porque
  `.gitignore` la excluye. Es deliberado: es el area de trabajo del usuario, su contenido cambia o
  desaparece sin aviso, y los protocolos tienen prohibido leerla o tocarla. Sin esa exclusion, el
  `git add -A` del Paso 7 de `protocol-close` la commitearia entera.
- **`010_prototype/`** esta **declarada por adelantado y todavia no existe en el arbol**, porque su
  etapa no ha arrancado y `git` no versiona carpetas vacias. Es deliberado: la fila fija **donde
  iran** los entregables antes de que haya el primero, que es cuando esa decision cuesta cero. Lo
  fija `D-061`. La diferencia desaparece sola el dia que se escriba el primer artefacto — y si ese
  dia no desaparece, **el control estara señalando algo real**.

📌 **`_outbound/` no es una tercera excepcion: existe en el arbol y esta declarada, asi que el
control no la senala.** Se escribe aqui porque es la unica carpeta cuyo contenido **esta destinado a
salir**: lo que guarda es texto ya redactado y ya verificado que espera la puerta de `C-009` para
escribirse en otro repositorio. **No es un cajon de borradores** — lo que no este listo para publicar
no entra—, y **se vacia**: publicada la pieza, su archivo se borra en la misma pasada. Una carpeta de
salida que acumula deja de decir que hay pendiente.

⛔ **Lo que esta segunda razon no autoriza es declarar carpetas «por si acaso».** Vale para una
carpeta cuya etapa esta escrita y cuyo contenido esta enumerado; una fila para algo que aun no se
sabe que sera convierte este control en ruido, y un control con ruido deja de mirarse.

🔑 **Una diferencia con motivo escrito no es un fallo; una sin el, si.** Por eso las dos razones de
arriba viven aqui y no en una lista de excepciones dentro del control: una lista de excepciones
envejece sin que nadie la revise y acaba tapando justo lo que el control existe para ver.

## Codigos

| Codigo | Archivo | Que es |
|---|---|---|
| `S-XXX` | `_persistence/progress.md` | sesion de trabajo |
| `H-nn` | `_persistence/progress.md` | hito |
| `T-XXX` | `_persistence/tasks.md` | tarea |
| `D-XXX` | `_persistence/decisions.md` | decision |
| `C-XXX` | `_persistence/constraints.md` | restriccion |
| `A-XXX` | `_persistence/assumptions.md` | supuesto |
| `L-XXX` | `_persistence/lessons.md` | leccion aprendida |
| `DT-XXX` | `_persistence/techdebt.md` | deuda tecnica |
| `F-NNN` | `_audit/findings.md` | hallazgo de auditoria |
| `R-XXX` | `_audit/R-XXX.md` | auditoria de una sesion |
| `N-XXX` | `005_discovery/005_needs.md`, el artefacto de necesidades de `005_discovery` (`D-045`) | necesidad |
| `I-XXX` | `005_discovery/015_stakeholders.md`, el artefacto de interesados de `005_discovery` (`D-038`, ruta por `D-045`) | interesado |
| `FT-XXX` | el artefacto de features de `020_baseline` (ruta por declarar: la etapa esta declarada, no iniciada) | feature |
| `SC-XXX` | el artefacto de escenarios de `020_baseline` (ruta por declarar: la etapa esta declarada, no iniciada) | scenario |

🚨 **Ningun codigo se reutiliza, en ningun archivo.** Un id retirado queda retirado; la entrada que
lo llevaba conserva su texto para que se entienda que se creia y por que dejo de valer.

⚠️ **De los codigos del producto estan declarados `N-XXX`, `I-XXX`, `FT-XXX` y `SC-XXX`.** Los dos
primeros son lo que `005_discovery` produce con codigo propio; sus supuestos y restricciones van a
`A-XXX` y `C-XXX`, que ya existian (`D-034`), y no tiene codigo propio ni el actor ni la hipotesis,
que se identifican por su tipo y por su archivo. **Slices, casos de prueba y decisiones
arquitectonicas siguen sin definir**, porque no hay producto declarado todavia. Se añaden a esta
tabla en la misma pasada en que se escriba el primero, con su `D-XXX`. Un codigo que aparece en un
archivo antes que en esta tabla es un desfase, no una novedad.

🚨 **`FT-XXX` y `SC-XXX` entraron por esa ultima frase, no porque haya producto** (`D-075`,
hallazgo `F-040`). Las plantillas de `_templates/020_baseline/` los escriben en sus ejemplos desde
`S-017`, y un codigo citado antes de declararse es un desfase — el mismo argumento que metio
`N-XXX` (`D-034`) e `I-XXX` (`D-038`). **Declararlos no adoptaba `020_baseline`**: cuando entraron, la
etapa no estaba en la tabla «Etapas», y por eso la columna «Archivo» de esas dos filas dice «ruta
por declarar» en vez de inventarse una.

⚠️ **Nota del 2026-09-11 (`F-095`, `T-152`): esa razon caduco, y la columna sigue igual.** `D-142`
declaro `020_baseline` en la tabla «Etapas» el 2026-09-10, asi que «la etapa no esta adoptada» dejo
de ser cierto en ese mismo commit. Lo que no cambio es el hueco: **la ruta de esos dos artefactos
sigue sin fijarse**, ahora porque la etapa esta declarada pero **no iniciada** y no hay producto que
la llene. Se escribira con su `D-XXX` en la pasada en que se decida, y hasta entonces la columna dice
«ruta por declarar» por ese motivo, no por el anterior.

📌 **Hay una propuesta escrita, y esta en `_methodology/000_method.md` (§46):** `N-`
necesidad, `FT-` feature, `SC-` scenario, `VS-` vertical slice, `T-` task, `TC-` caso de prueba,
`ADR-` decision arquitectonica. **Propuesta, no declarada:** de esos, `N-` ya entro por `D-034`
—porque el archivo de etapa de `005_discovery` lo cita y un codigo citado sin declarar es un
desfase—; los demas no entran hasta que haya producto y su `D-XXX`.

📌 **`I-XXX` no sale de esa propuesta: no estaba en ninguna parte.** Entro por `D-038`, con el mismo
argumento que `N-XXX`: la plantilla de interesados lo cita, y un codigo citado antes de declararse
es un desfase. La inicial `I` estaba libre en esta tabla.

🚨 **Los supuestos y las restricciones del descubrimiento no traen codigo propio.** La guia de
metodo hablaba de `SUP-` y `RES-`; aqui van a `A-XXX` y `C-XXX`, que ya existen y significan lo
mismo. Dos prefijos para el mismo concepto obligan a buscar en dos sitios lo que hay sin confirmar
(`D-034`).

🚨 **Dos de esos prefijos ya estan tomados en esta tabla, y por eso el metodo usa dos letras.**
`F-` es el hallazgo de auditoria y `S-` la sesion de trabajo; las fuentes del metodo los usaban para
feature y scenario. Se cambio el del metodo —`FT-` y `SC-`— y no el del registro, porque el registro
ya tiene historia escrita en `_audit/` y renombrarlo reescribiria trabajo ya auditado (`D-030`).
`T-` es la unica coincidencia deliberada: **es el mismo concepto**, la tarea, y darle dos nombres
segun el archivo seria peor que compartirlo.

---

## Que NO va en este archivo

⚠️ **Solo lo estable.** Si algo cambia de una sesion a otra —el avance, las tareas abiertas, los
bloqueos, que se hizo ayer— **no va aqui: va en `_persistence/progress.md`**.

Un archivo de identidad que hay que actualizar cada jornada deja de ser fiable, porque nadie
recuerda mantenerlo y todos lo siguen citando.

⚠️ **Y tampoco va aqui el porque de nada.** Este archivo dice **que es cada cosa y donde esta**; por
que se decidio asi vive en `_persistence/decisions.md`. Las notas de arriba explican como usar un
dato, no justifican una decision.
