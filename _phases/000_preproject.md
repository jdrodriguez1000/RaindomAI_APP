# Etapa `000_preproject`

> **La etapa en la que no se construye producto: se monta la forma de trabajar.** Protocolos,
> persistencia y canal con la auditoria.
>
> **La lee:** `manager`, y cualquier agente que necesite saber que esta autorizado en esta etapa.
> **Definiciones:** `project.md` (que es cada cosa y donde esta) y `CLAUDE.md` (el metodo). Este
> archivo **no define conceptos ni repite datos** — dice **que se hace y que no** dentro de la etapa.

🔑 **Este archivo es agnostico y sirve para cualquier proyecto.** No lleva dentro ni un nombre, ni
una ruta, ni un codigo concreto: donde hace falta un dato del proyecto, se referencia `project.md`.
Los codigos aparecen siempre en su forma generica —`T-XXX`, `D-XXX`, `A-XXX`, `F-NNN`—, nunca
instanciados.

📌 **«Etapa» y «fase» son la misma cosa en esta metodologia**, y se usan indistintamente. La carpeta
se llama `_phases/` en ingles porque los nombres de archivos y carpetas van en ingles; el contenido
va en espanol.

---

## 1. Que autoriza esta etapa

- **Montar y modificar el metodo:** las skills y los agentes de `.claude/`, `CLAUDE.md` y
  `project.md`.
- **Montar y mantener los registros:** los archivos de `_persistence/` y los de `_audit/`.
- **Registrar el porque en el momento** — decisiones, restricciones, supuestos y lecciones **sobre la
  forma de trabajar**.
- **Leer el encargo del cliente** en `_brief/` para extraer supuestos, restricciones y preguntas para
  el usuario.
- **Evaluar los hallazgos `F-NNN` de la auditoria**, aceptarlos con su `T-XXX` o rechazarlos con su
  `D-XXX`.
- **Declarar los datos propios del proyecto** en `project.md`: nombre, rutas, remoto, carpetas y
  tabla de codigos.
- **Cerrar el ciclo completo al menos una vez** —arranque, trabajo, cierre, auditoria— y corregir lo
  que ese primer recorrido rompa. Es la unica forma de saber si el andamio se sostiene.

## 2. Que prohibe esta etapa

Es la seccion util del archivo: lo que se descarrila solo.

| ❌ Prohibido | Por que |
|---|---|
| **Definir el alcance y el objetivo del proyecto** | esta etapa monta el andamio, no decide el producto. El alcance es de la etapa siguiente |
| **Escribir codigo de producto** | no hay alcance definido todavia; no hay nada que rebanar en slices |
| **Disenar pantallas o flujos de producto** | todavia no se sabe que problema resuelven |
| **Declarar etapas posteriores como decididas** | mientras no exista su `D-XXX`, la respuesta correcta es «solo esta declarada la actual» |
| **Convertir el encargo del cliente en requisito** | `_brief/` es **entrada**, no registro. Lo que el equipo adopte va como `D-XXX` |
| **Anadir codigos de producto** —necesidades, features, slices, casos de prueba— | la tabla «Codigos» de `project.md` no los define todavia; un codigo que aparece antes que en esa tabla es un desfase |
| **Dar por cerrado un hallazgo propio** | `Implementado` lo escribe la auditoria siguiente, nunca `manager` |
| **Evaluar el propio trabajo** | quien construye no es su propio testigo |
| **Prometer alcance o fechas** | no hay evidencia todavia para prometer nada |
| **Anadir restricciones tecnicas por iniciativa propia** | una restriccion tecnica condiciona el producto, y el producto todavia no esta decidido: se escala al usuario |
| **Leer o tocar el area de trabajo del usuario** desde un protocolo | esta fuera del repositorio y su contenido cambia sin aviso |

> **Si en `000_preproject` aparece un archivo de producto, la etapa se rompio.** Lo que se produce
> aqui es andamio: metodo, registro y evidencia.

## 3. Entradas — que debe existir antes de empezar

1. **El encargo del cliente**, en `_brief/`. Que este completo es un supuesto, no un hecho: se
   registra como `A-XXX` con su forma de validarlo.
2. **Un repositorio con `git` y remoto declarado**, que es lo que hace auditable el trabajo — sin
   commit no hay nada que auditar.
3. **Acceso al usuario.** Es el stakeholder, y sin el no existe la «Doble validacion»: la revision
   tecnica del auditor **no la sustituye**.

Si falta el acceso al usuario, la etapa puede avanzar en lo mecanico pero **no puede cerrar nada que
requiera su firma**. No se sustituye con suposiciones: se registra como `A-XXX`.

## 4. Procedimiento

El procedimiento de esta etapa **es el ciclo de la jornada**. No hay otro, y no es casualidad: lo que
se construye aqui es precisamente ese ciclo.

### Paso 1 — Abrir con `session-starter`

La primera peticion de la conversacion dispara el arranque, sea cual sea. El reporte se retransmite
entero. **El arranque es de solo lectura:** si detecta un desfase —trabajo sin commitear, commits sin
subir, un indice que no cuadra— **no lo corrige**; lo corrige `manager` despues de que el usuario
decida.

### Paso 2 — Los hallazgos abiertos van primero

Un `F-NNN` sin evaluar es el primer asunto de la jornada, antes de cualquier tarea. Se **verifica
contra `HEAD`** —se abrio contra un commit anterior y puede estar ya corregido— y despues se
registra:

| El hallazgo… | va a… |
|---|---|
| se acepta | **`T-XXX`** con `Origen: report_auditor` |
| se rechaza **porque es incorrecto** | **`D-XXX`** con la evidencia que lo contradice |
| se rechaza **aunque tenga razon**, por coste o prioridad | **`D-XXX`** + **`DT-XXX`** |

Y su fila en el registro de hallazgos pasa a `Aceptado — pendiente` o a `No se implementa`. **Nunca a
`Implementado`.**

### Paso 3 — Trabajar, registrando el porque en el momento

`decisions.md`, `constraints.md`, `assumptions.md` y `lessons.md` los escribe `manager` **y solo el**,
al cerrar cada tema y antes de pasar al siguiente. Un porque no aparece en el `git diff`: nace en la
conversacion, y la conversacion no queda en ningun archivo.

🚨 **Comando y salida cruda, siempre.** Un resultado afirmado sin la orden que lo produjo no es
reproducible, y lo que no se puede reproducir hay que rehacerlo entero. «Se comprobo» es un veredicto,
no evidencia.

⚠️ **Y un recuento se fecha si su ambito incluye lo que la sesion todavia va a escribir.** Un barrido
sobre el repositorio entero se toma antes de que el cierre escriba su informe: vale «al momento de
escribir esta entrada», nunca «sobre el commit que la contiene».

### Paso 4 — Cerrar con `session-closer`

El agente recoge la evidencia con `git`, actualiza `progress.md` y `tasks.md`, propone entradas de
`techdebt.md`, escribe el informe de la sesion **dentro del mismo commit que describe**, y sube.
Arranca en frio a proposito: solo puede escribir desde el `git diff`.

### Paso 5 — Auditar con `report_auditor`

**El cierre no termina en el push: termina en la auditoria.** Se lanza sobre el commit ya subido, y si
el push fallo se lanza igual —el commit existe en local y es auditable—. No se le cuenta el contexto:
un auditor al que se le explica lo que paso deja de auditar y pasa a confirmar.

⚠️ **Sus hallazgos no se arreglan en el momento**, por pequenos que parezcan. Corregir despues del
commit auditado deja la auditoria describiendo un estado que ya cambio.

### Paso 6 — Y mientras tanto, construir lo que la etapa entrega

Los cinco pasos anteriores son el **ciclo**; no son el objetivo. Lo que la etapa tiene que dejar
montado son los cinco entregables de la seccion 8, y se construyen dentro de ese ciclo, jornada a
jornada, no en una pasada aparte.

## 5. Artefactos que produce

Todo vive en el repositorio del proyecto. Esta etapa **no produce artefactos de producto**.

```
.claude/          <- el metodo: agentes y skills. Agnostico, sin datos del proyecto
CLAUDE.md         <- las reglas: identidad, principios, ciclo de sesion
project.md        <- los datos propios: nombre, rutas, remoto, carpetas, codigos
_brief/           <- el encargo del cliente. Entrada, no registro
_persistence/     <- como va el trabajo: indice arriba y detalle debajo, un archivo por tipo
_audit/           <- como se comprueba: informe de sesion, auditoria, tablero y hallazgos
_phases/          <- que se hace en cada etapa. Un archivo por etapa declarada
```

⚠️ **Toda carpeta de primer nivel se declara en la tabla «Carpetas propias» de `project.md`.** El
cierre contrasta el arbol contra esa tabla **en las dos direcciones**: una carpeta sin fila y una fila
sin carpeta son el mismo defecto por sus dos caras. Si una diferencia es deliberada, tiene que llevar
su razon escrita.

## 6. Condicion de salida

La etapa termina cuando **las seis son ciertas**. Son el espejo de los cinco entregables de la
seccion 8, mas la unica exigencia que la etapa puede hacerle a la auditoria:

- [ ] **La estructura minima existe:** las carpetas de la seccion 5, cada una declarada en
      `project.md`, y el control de carpetas del cierre sin diferencias sin justificar.
- [ ] **Los tres agentes existen y su reparto esta escrito:** `session-starter`, `session-closer` y
      `report_auditor`, cada uno con su protocolo y con su frontera —quien construye, quien registra,
      quien audita— enunciada donde se aplica.
- [ ] **El ciclo corrio entero al menos una vez**, con evidencia: una sesion abierta, cerrada con
      commit y push, y auditada sobre ese commit.
- [ ] **`_persistence/` esta operativo:** cada archivo con su indice, sus convenciones y sus estados
      validos escritos dentro, e indice y detalle cuadrando.
- [ ] **`_audit/` esta operativo:** tablero y registro de hallazgos, con al menos una auditoria
      registrada y sus hallazgos con estado.
- [ ] **No queda ningun `F-NNN` sin evaluar:** todos estan `Implementado`, `Aceptado — pendiente` con
      su `T-XXX`, o `No se implementa` con su `D-XXX`.

⚠️ **La ultima no exige que los hallazgos esten cerrados**, y no es un descuido: cerrar un hallazgo es
de la auditoria siguiente. Lo que la etapa si puede exigir es que ninguno se quede sin evaluar.

🔑 **Ninguna de las seis habla del producto**, y ahi esta el criterio entero de la etapa: se sale de
`000_preproject` cuando el andamio se sostiene, no cuando se sabe que se va a construir. Eso es lo
primero que hace la etapa siguiente.

## 7. Que registra `manager` en `_persistence/`

| Archivo | Que se escribe aqui en esta etapa | Quien lo escribe |
|---|---|---|
| `progress.md` | el estado, la bitacora de sesiones, el siguiente paso | **`session-closer`** |
| `tasks.md` | las tareas y su estado | **`session-closer`**, salvo la `T-XXX` que nace de un hallazgo aceptado |
| `decisions.md` | toda eleccion sobre el metodo, con sus **alternativas descartadas** | **`manager`** |
| `constraints.md` | los limites ya no negociables | **`manager`** |
| `assumptions.md` | lo no confirmado, **con su forma de validarlo y su disparador** | **`manager`** |
| `lessons.md` | lo que fallo y se corrigio, o la practica que demostro funcionar | **`manager`** |
| `techdebt.md` | los atajos aceptados a conciencia | `session-closer` **propone**; confirma el **usuario** |

🚨 **Los cuatro del porque no son del `session-closer`, y por eso son los que se pierden.** El agente
arranca en frio y solo ve archivos; si `manager` llega al cierre sin haberlos escrito, esa informacion
**ya se perdio** — no hay diff del que reconstruirla.

## 8. Lo que esta etapa le entrega a la siguiente

Cinco cosas. Ninguna es producto, y todas son condicion para poder construirlo.

### 1. La estructura de carpetas y archivos minima para iniciar

El arbol de la seccion 5, creado y declarado. No es una convencion de orden: cada carpeta es la
respuesta a una pregunta distinta —**con que** se construye (`.claude/`), **que** se pidio
(`_brief/`), **como va** (`_persistence/`), **como se comprueba** (`_audit/`), **que se hace en cada
etapa** (`_phases/`)—. Un proyecto que empieza sin ellas las improvisa a mitad de camino, y entonces
ya hay trabajo hecho que no encaja en ninguna.

### 2. La forma de trabajo entre los tres agentes

`session-starter` abre y **solo lee**; `session-closer` cierra, commitea y sube; `report_auditor`
audita el commit cerrado y **no corrige ni decide**. Los tres arrancan en frio, y esa es toda su
utilidad: ninguno vio la conversacion, asi que ninguno puede confirmar la version de `manager` en vez
de la evidencia.

🚨 **Lo que la etapa entrega no son tres archivos de agente: es la frontera entre ellos, escrita donde
se aplica.** Quien construye no evalua, quien revisa no reescribe, y quien audita no cierra su propio
trabajo. Sin esa frontera, los tres agentes son tres formas de decir lo mismo.

### 3. La memoria del proyecto, en los archivos de `_persistence/`

Lo decidido, lo asumido, lo limitado y lo aprendido, cada cosa en su archivo, con indice arriba y
detalle debajo. **Es lo que sobrevive al cierre de la conversacion**, que es lo unico que no
sobrevive por si solo: el codigo queda en `git`, pero el porque de cada eleccion solo queda si
alguien lo escribio en el momento.

La etapa entrega los archivos **y sus convenciones**: que estados son validos, que campos son
obligatorios y quien escribe cada uno. Un registro sin convenciones escritas dura hasta el primer
desacuerdo sobre como llenarlo.

### 4. La gestion de las auditorias

El circuito completo: informe de sesion dentro del commit que describe, auditoria sobre ese commit,
tablero de que sesion fue auditada y con que veredicto, y registro de hallazgos donde **cada `F-NNN`
queda con su estado, incluidos los rechazados y su razon**.

⚠️ **Ese ultimo detalle es el que hace que el circuito valga algo.** Un hallazgo que desaparece
porque no convencio convierte el registro en la version que preferiamos. Y el estado `Implementado`
lo escribe **la auditoria siguiente**, nunca el auditado: si el auditado pudiera cerrar sus propios
hallazgos, el registro diria lo que quisieramos que dijera.

### 5. Los datos propios del proyecto, en `project.md`

Nombre, rutas, remoto, carpetas declaradas y tabla de codigos, **en un solo sitio**. Es lo unico que
cambia al llevar este metodo a otro proyecto: los protocolos, los agentes y `CLAUDE.md` no llevan
dentro ni un nombre ni una ruta, los leen de aqui.

🔑 **Por eso `project.md` es un entregable y no un archivo de servicio.** Mientras un dato del
proyecto viva escrito dentro del metodo, el metodo no es reutilizable — y nadie lo descubre hasta que
intenta copiarlo.
