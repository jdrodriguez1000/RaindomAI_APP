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

🔑 **Forma canonica: relativa y con `/`.** Las rutas relativas de esta tabla se escriben **tal
como se pegan en un comando**, con separador `/` y desde la raiz de este repositorio. Es la unica
forma valida, y por una razon concreta: funciona igual en Bash y en PowerShell. Quien copie un valor
de aqui a un bloque `bash` obtiene una orden que corre; no una que hay que traducir antes.

⚠️ **La absoluta de arriba es la excepcion declarada**, no una segunda forma a elegir: existe
porque nombra la ubicacion del repositorio en esta maquina, no porque sirva para navegar dentro de
el. **Para citar un archivo del proyecto se usa la relativa.**

## Reparto de autoridad

| Actor | Que hace | Que NO hace |
|---|---|---|
| **usuario** | decide alcance, prioridades y lo irreversible | — |
| **`manager`** (esta sesion) | dirige, coordina, construye, y registra el porque en el momento | **no audita su propio trabajo** |
| **`report_auditor`** (agente) | audita un commit ya cerrado, verifica y recomienda | **no construye, no corrige, no decide** |

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
| Etapas declaradas | `000_preproject`, `005_discovery` |
| Etapas posteriores a `005_discovery` | **no registradas** |

`000_preproject` es la etapa en la que no se construye producto: se monta la forma de trabajar
—protocolos, persistencia, canal con la auditoria—. Es deliberado que tenga nombre propio y no un
numero del flujo del producto: meterla en la nomenclatura de las demas seria fingir que el producto
avanza cuando lo que avanza es el andamio.

`005_discovery` es la etapa siguiente: la que define **alcance y objetivo** del proyecto, trabajo que
`000_preproject` tiene expresamente prohibido. Lo fija `D-024`, por decision del usuario.

🚨 **Lo que viene despues de `005_discovery` sigue sin decidir, y este archivo no lo va a inventar.**
El brief del cliente (`_brief/client_brief.md`, §22) **propone** una secuencia —Idea → Definicion del
producto → Especificacion → Diseño → Desarrollo asistido por IA → Pruebas → Iteracion—, pero **un
encargo no es una decision**: lo que el equipo adopte tiene que quedar como `D-XXX` en
`decisions.md`, y hoy no lo esta. Hasta entonces, la respuesta correcta a «que etapas tiene el
proyecto» son *«las dos declaradas, y nada mas»*.

⚠️ **Que `005_discovery` este declarada no cierra la tarea de declarar las etapas posteriores.** Se
nombro la inmediata para que las tareas de alcance tuvieran donde ir; la **secuencia completa** sigue
siendo trabajo pendiente, y su tarea vive ahora en `005_discovery`.

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
| `_audit/` | **Como se comprueba** el trabajo: el informe de cada sesion, la auditoria de cada una, el tablero y el registro de hallazgos |
| `_phases/` | **Que se hace en cada etapa**: un archivo por etapa declarada, con lo que autoriza, lo que prohibe, su procedimiento y su condicion de salida. Agnostica — no lleva dentro ningun dato de este proyecto, y el Paso 1b lo comprueba |
| `temporal/` | Area de trabajo del usuario. **Fuera del repositorio**, excluida en `.gitignore` |

🚨 **Esta tabla se contrasta contra el arbol en cada cierre de sesion** (Paso 2c de `protocol-close`):
las carpetas de primer nivel que existen, frente a las filas de aqui, **en las dos direcciones**. Una
carpeta sin declarar y una fila sin carpeta son el mismo defecto por sus dos caras.

⚠️ **Una fila va a salir señalada por ese control, y aqui esta escrita su razon:**

- **`temporal/`** existe en disco pero **nunca aparecera en el arbol versionado**, porque
  `.gitignore` la excluye. Es deliberado: es el area de trabajo del usuario, su contenido cambia o
  desaparece sin aviso, y los protocolos tienen prohibido leerla o tocarla. Sin esa exclusion, el
  `git add -A` del Paso 7 de `protocol-close` la commitearia entera.

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

🚨 **Ningun codigo se reutiliza, en ningun archivo.** Un id retirado queda retirado; la entrada que
lo llevaba conserva su texto para que se entienda que se creia y por que dejo de valer.

⚠️ **Los codigos del producto —necesidades, features, escenarios, slices, casos de prueba— no estan
definidos**, porque no hay producto declarado todavia. Se añaden a esta tabla en la misma pasada en
que se escriba el primero, con su `D-XXX`. Un codigo que aparece en un archivo antes que en esta
tabla es un desfase, no una novedad.

---

## Que NO va en este archivo

⚠️ **Solo lo estable.** Si algo cambia de una sesion a otra —el avance, las tareas abiertas, los
bloqueos, que se hizo ayer— **no va aqui: va en `_persistence/progress.md`**.

Un archivo de identidad que hay que actualizar cada jornada deja de ser fiable, porque nadie
recuerda mantenerlo y todos lo siguen citando.

⚠️ **Y tampoco va aqui el porque de nada.** Este archivo dice **que es cada cosa y donde esta**; por
que se decidio asi vive en `_persistence/decisions.md`. Las notas de arriba explican como usar un
dato, no justifican una decision.
