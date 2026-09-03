---
name: protocol-close
description: Protocolo de cierre de sesion del proyecto. Recoge la evidencia real del trabajo (git status, git diff, git log), actualiza de forma obligatoria _persistence/progress.md y _persistence/tasks.md, propone entradas de techdebt.md, y solo revisa —sin escribirlos— decisions.md, assumptions.md, constraints.md y lessons.md; despues escribe el informe para la auditoria y deja la sesion cerrada con un commit y su push. Uso exclusivo del agente session-closer, que se lanza al terminar una jornada de trabajo o cuando el usuario pida "cerremos la sesion", "cierra la sesion", "finalicemos el trabajo", "guarda el avance", "terminamos por hoy" o algo similar.
---

# Protocolo de cierre de sesion

Este protocolo lo ejecuta **unicamente** el agente `session-closer`. Deja el proyecto en un estado
del que la proxima sesion pueda arrancar sola.

## Que es una sesion

🔑 **Una sesion es una jornada de trabajo, no un dia.** Puede ser una manana, una tarde, una
noche, o un dia completo. **Puede haber varias sesiones en la misma fecha**, y cada una tiene su
propio cierre y su propio `S-XXX`. Nunca asumas que una sesion equivale a un dia.

> 🔑 **La regla que gobierna todo el protocolo: se escribe desde la EVIDENCIA, no desde el
> relato.** No anotes «se hizo X» si X no aparece en el `git diff`.

Escribir desde lo que se recuerda de la conversacion es escribir rumores; escribir desde el diff
es escribir hechos. Si las dos cosas se contradicen, **manda el diff**.

## Los tres actores del proyecto

| Actor | Escribe | No escribe |
|---|---|---|
| **manager** (sesion de trabajo) | construye, y registra el porque en el momento | — |
| **El cierre** (este protocolo) | `progress.md`, `tasks.md`, propuestas a `techdebt.md`, el informe `_audit/S-XXX.md` | los cuatro del porque |
| **`report_auditor`** (agente) | `_audit/R-XXX.md`, `_audit/findings.md`, `_audit/index.md` | no construye, no corrige |

🚨 **`report_auditor` corre despues de ti, no a la vez.** Tu cierras y commiteas; el audita ese commit.
Por eso **no escribes nada en `_audit/R-XXX.md` ni en `_audit/findings.md`**: son suyos.

⚠️ Lo que venga de una auditoria se refleja en `_persistence/tasks.md` como tarea con
`Origen: report_auditor`, y solo despues de que `manager` la evalue y la considere correcta. **Tu no haces
esa evaluacion**: si aparece algo de la auditoria sin evaluar, lo dices en el reporte.

🚨 **Esa `T-XXX` puede existir ya cuando tu llegas, y es lo normal.** `manager` la escribe en el
momento de aceptar el hallazgo, porque la fila del hallazgo tiene que citar su codigo para ser
auditable. **No la dupliques ni la reescribas:** comprueba que esta y sigue.

🚨 **Y hay una segunda excepcion, del mismo tipo:** `manager` tambien escribe en `tasks.md` cuando el
cambio **nace de una decision ya registrada que tu no puedes deducir del `git diff`** —reasignar la
etapa de una tarea, cambiar la estructura del archivo porque lo pidio el usuario—. Tu arrancas en
frio: una orden del usuario no deja rastro en el diff.

⚠️ **Son dos excepciones, no una puerta, y las dos se reconocen igual: por la cita.** Toda fila
editada a mano lleva un `D-XXX` o un `F-NNN` que la respalde, escrito en la propia tarea. **Si la
cita esta, no es una infraccion: no la deshagas ni la reportes como desfase.** Si falta, eso si va al
reporte. Las dos estan escritas en la convencion del propio `tasks.md`; lo demas sigue siendo tuyo.

🚨 **No toques `temporal/`.** Es el area de trabajo del usuario, no parte del registro.

---

## Paso 0 — Los datos propios del proyecto

Empieza leyendo **`project.md`** (en la raiz, en minusculas): los datos propios de este proyecto
—nombre, rutas, remoto, carpetas declaradas—. Todo lo que en este protocolo aparece entre
`<angulos>` se resuelve ahi.

🚨 **Este protocolo no lleva dentro ni un dato del proyecto, y esa es su condicion de uso.** Se
copia a otro proyecto tal cual: lo unico que cambia es `project.md`. De ahi se sigue que un valor
que ese archivo **no declare** deja sin poder ejecutarse al control que lo usaba —los Pasos 1b y 2c
son los dos casos—, y entonces:

- **no lo inventes** ni lo reconstruyas por analogia con otro proyecto;
- **no des por correcto** el control que no pudiste correr;
- va al reporte del Paso 8 como `🚨 SIN COMPROBAR — <que falta en project.md>`.

🔑 Esa es la misma regla que rige el resto del protocolo: **«no pude comprobarlo» no es «esta
bien»**, y confundir las dos cosas es como se cuela todo lo que se cuela. Ademas, una linea
`SIN COMPROBAR` repetida sesion tras sesion es la unica forma de que el hueco se note.

---

## Paso 1 — Recoger la evidencia (antes de escribir nada)

En este orden y sin saltarte ninguno:

```
git status
git diff
git diff --staged
git log --oneline -5
```

De ahi sale **que paso de verdad hoy**: que archivos nacieron, cuales cambiaron y desde que punto
se venia.

Si `git status` sale limpio y no hay nada sin commitear, **dilo y detente**: no hay sesion que
cerrar. No inventes avance para llenar el reporte.

⚠️ **Excepcion unica — el primer cierre del repositorio.** Si `git log` falla porque todavia no
existe ningun commit, no es un error: es el commit inicial. Sigue el protocolo normal; la evidencia
es entonces `git status`, que lista todo como sin seguimiento. En ese primer cierre, **el Paso 2c
tampoco puede correr** —`git ls-tree HEAD` no tiene arbol contra el que comparar—, y va al reporte
como `SIN COMPROBAR — sin commits todavia`.

### 1b. El control de fuga de datos del proyecto

Con la evidencia delante, corre este control y **pega su salida cruda en el informe**:

```bash
git grep -nE "<nombre del proyecto>|<carpeta raiz de las rutas absolutas>|<host del remoto>" -- .claude CLAUDE.md _phases _methodology _templates _workflow
```

Los tres valores salen de `project.md`. Si alguno no esta declarado ahi, este control **no se puede
construir**: dilo en el reporte, no lo aproximes.

🔑 **La respuesta correcta es CERO lineas** (`exit 1`). Si devuelve alguna, un dato propio del
proyecto se ha colado en un archivo que deberia ser reutilizable tal cual, y **se reporta como
hallazgo propio en el informe**: no se arregla en silencio ni se omite.

🚨 **El ambito es parte del control, no un detalle de implementacion.** Se acota a `.claude/`,
`CLAUDE.md`, `_phases/`, `_methodology/`, `_templates/` y `_workflow/`, y a nada mas, porque son los
**unicos sitios donde «cero» es la respuesta correcta**: los seis tienen que poder copiarse a otro
proyecto tal cual. El mismo patron sobre el arbol entero da siempre positivos **legitimos**:

| Donde | Por que es correcto que aparezca |
|---|---|
| `project.md` | es su sitio, por diseño: el archivo existe justamente para concentrarlos |
| `_audit/S-XXX.md` | informes ya entregados; no se reescriben |
| `_persistence/` | registro historico: describe lo que paso, y el pasado no se reescribe |

⚠️ **Un control que avisa de todo termina apagado.** Si se ensancha el ambito «por si acaso», el
control pasa a devolver decenas de lineas correctas cada sesion, alguien deja de mirarlas, y
entonces no detecta nada — que es peor que no tenerlo, porque ademas se cree que existe.

📌 **Por que existe este control:** un protocolo con las rutas y los nombres del proyecto escritos
dentro deja de ser reutilizable y, peor, empieza a contradecir al archivo que deberia ser la unica
fuente de esos datos. La regresion es facil de cometer y **detectable sin ejecutar nada**, porque
es una busqueda de texto: cuesta un segundo. Va escrito con su patron literal precisamente para
que nadie tenga que reinventarlo cada sesion.

---

## Paso 2 — El traspaso, solo para el porque

La sesion puede dejar un traspaso corto: lo que se intento, lo que se descarto, con que se trabo el
usuario. Usalo **solo para explicar el porque** de lo que ya viste en el diff.

⚠️ **El traspaso nunca sustituye la evidencia.** Si el traspaso dice que se hizo algo y el diff no
lo muestra, manda el diff — y anotalo como discrepancia en el reporte.

Si no hay traspaso, el protocolo funciona igual, solo que con menos porque.

---

## Paso 2b — Coherencia indice ↔ detalle (antes del `git add`)

Cada archivo de `_persistence/` abre con un indice. **Los indices de este proyecto son tablas con
enlaces de ancla, no numeros de linea**: no se desfasan al editar el archivo, asi que no hay nada
que regenerar. Lo que si se rompe es otra cosa:

- una **entrada sin fila en el indice** es invisible: nadie la va a encontrar, porque nadie lee el
  archivo entero;
- una **fila de indice sin entrada** apunta al vacio.

Las dos formas de dejarlo a medias mienten igual. Esta comprobacion las detecta:

🚨 **El `awk` del principio de cada rama no es decoracion: descarta los bloques de codigo
cercados.** El registro guarda **salida cruda de comandos** como evidencia, y esos bloques
contienen encabezados y codigos identicos a los reales —`### C-001`, `| [T-001]…`— que son citas de
como estaba el archivo, no entradas. Sin el filtro, el control senala como huerfano lo que en
realidad es una prueba bien puesta. Y una alarma que siempre resulta falsa se aprende a ignorar:
el dia que sea verdadera tampoco se mirara.

```bash
for f in tasks decisions constraints assumptions lessons techdebt progress; do
  echo "== $f"
  diff <(awk '/^```/{c=!c; next} !c' "_persistence/$f.md" | grep -oE '^\| \[?[A-Z]+-[0-9]+' | grep -oE '[A-Z]+-[0-9]+' | sort -u) \
       <(awk '/^```/{c=!c; next} !c' "_persistence/$f.md" | grep -oE '^#{3} [A-Z]+-[0-9]+'   | grep -oE '[A-Z]+-[0-9]+' | sort -u)
done
```

Sin salida bajo un archivo = indice y detalle coinciden. Una linea `<` es una fila de indice sin
entrada; una linea `>` es una entrada que falta en el indice.

**Por que va aqui y no mas abajo, y son tres razones:**

- **Antes del `git add`**, porque el dano no es tener algo mal en el disco: es meterlo en el commit.
- 🔑 **Antes de escribir `tasks.md` (Paso 4)**, porque esta comprobacion **produce tareas**.
  Corriendola despues de escribir, su resultado llegaria tarde y no habria donde anotarlo.
- **Despues de la puerta del Paso 1**, porque si no hay nada que cerrar tampoco hay nada que comprobar.

**Hay tres resultados, no dos:**

| Que sale | Que significa | Que haces |
|---|---|---|
| sin diferencias en los 7 | los indices estan al dia | sigue al Paso 2c |
| diferencias | falta una fila o sobra una | **arreglalo ahora** y dilo en el reporte |
| el comando falla | **no lo comprobaste** | commit igual, y a **Sin resolver** |

🚨 **La tercera fila es la importante.** «No pude comprobarlo» no es «esta bien».

⚠️ **Entre esta comprobacion y el `git add` no se edita ningun archivo de `_persistence/` ya
comprobado sin volver a correrla.** El control solo vale si en medio nadie toca lo que se comprobo.

🚨 **La linea del reporte sale siempre**, este al dia o no. Sin ella, un cierre que comprobo y uno
que no se leen identicos.

---

## Paso 2c — Las carpetas del arbol contra las declaradas (antes del `git add`)

El Paso 2b compara un archivo consigo mismo. Este compara **el repositorio contra su declaracion**:
los directorios de primer nivel que existen de verdad, frente a las filas de la tabla «Carpetas
propias» de `project.md`.

```bash
diff <(git ls-tree -d --name-only HEAD | sed 's|$|/|' | sort) \
     <(sed -n '/^## Carpetas propias/,/^## /p' project.md | grep -oE '^\| `[^`]+/`' | tr -d '|` ' | sort)
```

Si `project.md` no tiene todavia esa tabla, este control **no se puede correr**: va al reporte como
`SIN COMPROBAR`, con el motivo.

**Las dos direcciones importan, y dicen cosas distintas:**

| Lo que ves | Que significa | Que haces |
|---|---|---|
| `<` una carpeta que existe y **no** esta declarada | el repositorio crecio y el registro no se entero | 🚨 proponlo como `DT-XXX`, o declarala si es obvio |
| `>` una fila declarada cuya carpeta **no** existe | o se borro sin actualizar el registro, o esta declarada por adelantado a proposito | comprueba cual de las dos. Si es deliberado, **tiene que haber un `D-XXX` que lo diga** |

⚠️ **Una diferencia con motivo escrito no es un fallo; una sin el, si.** Este control no lleva lista
de excepciones dentro, y es deliberado: una lista de excepciones envejece sin que nadie la revise y
acaba tapando justo lo que el control existe para ver. Lo que se exige es que **cada diferencia que
sobreviva tenga su razon en `project.md` o en una `D-XXX`** — y si no la tiene, esa es la noticia.

📌 **Por que existe este paso:** una carpeta versionada que nadie declaro no avisa de nada. El
desfase no duele el dia que ocurre; duele meses despues, cuando alguien tiene que averiguar si esa
carpeta debia estar ahi. Un metodo cuyo disparador es «alguien lo nota» no falla ruidosamente:
falla en silencio, y no hay forma de saber cuantas veces no se activo. Esto puede **salir rojo**
sin que nadie sospeche nada, que es la unica diferencia entre un detector y una coartada.

⛔ **No sustituye a releer.** La relectura encuentra cosas que ninguna comparacion mecanica ve; lo
que no puede es ser el unico filtro para lo que si es mecanizable.

---

## Paso 2d — Ningun bloque de verificacion sin ancla (antes del `git add`)

Los Pasos 2b y 2c comprueban estructura. Este comprueba **lo que la jornada afirmo haber
verificado**: todo bloque de verificacion escrito hoy tiene que describir **el commit que lo va a
contener**, no el arbol de trabajo en el instante en que se corrio.

**Cual es el defecto exacto.** Una orden corrida sobre el arbol —`grep -c ... archivo.md`— da un
numero cierto **en ese momento**. Si despues, en la misma jornada, alguien añade una linea mas al
archivo, el numero publicado ya no se reproduce sobre el commit. Quien audite correra la orden y
obtendra otra cosa; y entonces el resultado que vale es el suyo, no el nuestro.

**Que se hace, en dos ordenes.** Primero, localizar los bloques que la jornada añadio y no estan
anclados:

```bash
git diff --cached -U0 -- _persistence _audit \
  | grep -E '^\+\$ ' \
  | grep -vE 'git (show|grep|log|diff) [0-9a-f]{7,40}'
```

Cada linea que salga es una orden publicada hoy **sin ancla a un commit**. Y despues, sobre cada
una: se vuelve a correr, y su salida tiene que ser la que el bloque publica.

**Las tres salidas posibles:**

| Lo que ves | Que significa | Que haces |
|---|---|---|
| ninguna linea | todo lo escrito hoy va anclado | sigue |
| una linea, y al reejecutarla da lo mismo que el bloque publica | la orden es reproducible aunque no lleve ancla | sigue, pero **anclala**: `git show <hash>:` cuesta un `git grep` |
| una linea, y al reejecutarla da **otra cosa** | 🚨 el bloque afirma algo que su commit no sostiene | no se cierra asi. O se corrige el numero, o el bloque va con su **nota fechada** al lado (`D-019`) |

🚨 **Y la evidencia de este paso publica la lista COMPLETA de su primera orden, nunca una
seleccion de ella.** Se pega la orden con **su recuento** y **todas** las lineas que devolvio, con el
resultado de reejecutar cada una. Pegar unas cuantas es lo que dejo pasar el octavo caso del defecto:
el paso se corrio, se documentaron cinco lineas de varias decenas, y la que fallaba estaba entre las
que no se pegaron. **Un control que se documenta sobre una parte de su propia salida no es el
control** — es una muestra, y elegida por quien se examina.

🚨 **El recuento que se publica es el de lineas que devolvio la orden, no el de ordenes
distintas.** Una misma orden citada en dos archivos sale dos veces, y las dos lineas van pegadas:
deduplicar es seleccionar, y seleccionar es justo lo que el parrafo anterior prohibe. Si ademas
interesa cuantas ordenes distintas hay, ese numero se da **aparte y con ese nombre**, nunca como
recuento de la salida. Dos cifras con dos nombres se contrastan; una cifra con el nombre de la otra
no reproduce, y quien la reejecute no puede saber si se equivoco el informe o cambio el repositorio.

🚨 **Y la orden se publica en la forma que reproduce contra el commit, que no es la que se corrio.**
El paso corre sobre el area de staging, cuando el informe todavia no existe; una vez commiteado, esa
misma orden encuentra tambien las ordenes citadas **dentro del propio informe** y devuelve mucho mas.
Por eso lo que se pega lleva el informe excluido y el commit por delante:

```bash
git diff -U0 <hash>^ <hash> -- _persistence _audit ":(exclude)_audit/S-XXX.md" \
  | grep -E '^\+\$ ' \
  | grep -vE 'git (show|grep|log|diff) [0-9a-f]{7,40}'
```

📌 **Y si el hash no se conoce aun al escribir la seccion, se pega la orden corrida y se dice al
lado cual es su equivalencia anclada** — la de arriba, con el hash que el cierre deje. Lo que no
vale es publicar una orden que, tal como esta escrita, devuelve otra cosa que la que hay debajo.

🚨 **Y esa lista tiene un sitio fijo: la seccion 7 del informe de `_audit/S-XXX.md`, y no la
pantalla.** Publicada solo en el reporte de cierre, la evidencia del control desaparece con la
sesion: al dia siguiente el informe afirma haber corrido el paso y no queda nada que mirar. `D-063`
decia **que** publicar; esto dice **donde**, que es lo que faltaba para que la regla se pudiera
comprobar. Si la lista sale vacia, la seccion 7 lo dice con su orden y su salida — «ninguna linea» es
tambien un resultado, y se publica igual.

🚨 **Y si anotas de que archivo sale cada orden, esa procedencia se deriva del diff — no se
escribe a mano mirando los bloques.** A mano es exactamente donde se equivoca: la orden se busca
en el bloque que uno recuerda haber escrito, y la memoria atribuye antes de comprobar. La orden que
la produce, y que se pega con su salida cruda:

```bash
git diff -U0 -- _persistence _audit | awk '/^\+\+\+ /{f=$2} /^\+\$ /{print f" :: "$0}' | grep -vE 'git (show|grep|log|diff) [0-9a-f]{7,40}'
```

📌 **La procedencia es del archivo, no de la entrada.** El diff sabe en que archivo entro cada
linea; **no** sabe si dentro de ese archivo cayo en `T-050` o en `D-065`. Si el informe nombra la
entrada, esa mitad si se mira a mano — y entonces se comprueba, una por una, contra el bloque que
se cita.

⚠️ **El recuento no es estable entre entornos, y por eso no basta con la cifra.** La misma orden
sobre el mismo commit puede devolver numeros distintos segun como expanda el patron cada shell; los
falsos positivos conocidos son parte de esa diferencia. Una lista se compara linea a linea; un numero
solo se puede creer.

⛔ **Lo que no vale es reescribir el bloque para que cuadre.** Sustituir la salida vieja por la
nueva convierte «falta evidencia» en «hay evidencia falsa», y esta vez sin nadie que lo note. La
salida correcta es la nota fechada: quedan visibles las dos cosas, lo que se probo entonces y lo que
se probo despues.

📌 **Por que existe este paso.** Es el defecto mas repetido de este repositorio —`F-005`, `F-008`,
`F-011`, `F-022`, `F-025`, `F-027` y `F-031`, siete hallazgos de la misma forma— y no se repite por
descuido: se repite porque **cuando ocurre nadie lo ve**. La orden se corre pronto, el archivo
crece despues, y entre las dos cosas no hay ningun momento en que algo chille. `L-013` y `L-015` ya
describen el defecto; lo que faltaba era quien lo aplicara, que es `L-008` literal — una regla sin
mecanismo no es una regla, es una intencion.

⚠️ **El patron `^\+\$ ` acota a proposito, y por eso no basta con el.** Recoge las lineas de orden
—las que empiezan por `$ ` dentro de un bloque— que el diff añade. No ve una orden escrita en prosa
ni una que la jornada dejo sin el prefijo `$ `, y no distingue un ancla legitima de un hash citado
por casualidad. Es un cedazo, no una prueba: **la relectura de lo escrito sigue siendo obligatoria**.

⚠️ **Un falso positivo conocido, visto la primera vez que se corrio el paso:** `git grep -nE
'<patron>' <hash> -- <ruta>` **si esta anclado**, pero el hash va detras del patron y la segunda
orden no lo reconoce. Sale en la lista, y al reejecutarla da lo mismo — fila segunda de la tabla,
no hay nada que corregir. Se deja asi a proposito: **un cedazo que deja pasar de mas no avisa de
nada, y uno que se afina hasta no dar falsos positivos acaba dejando pasar el caso que importa.**

---

## Como se escriben estos archivos

Los siete archivos de `_persistence/` tienen la misma forma: **indice arriba, convenciones despues,
y el detalle debajo** en secciones con su codigo. Las convenciones de cada archivo estan escritas
dentro del propio archivo, en su seccion `## Convenciones`: leelas antes de escribir.

Los codigos de este proyecto:

| Codigo | Archivo | Que es |
|---|---|---|
| `S-XXX` | `progress.md` | sesion de trabajo |
| `H-nn` | `progress.md` | hito |
| `T-XXX` | `tasks.md` | tarea |
| `D-XXX` | `decisions.md` | decision |
| `C-XXX` | `constraints.md` | restriccion |
| `A-XXX` | `assumptions.md` | supuesto sin comprobar |
| `L-XXX` | `lessons.md` | leccion aprendida |
| `DT-XXX` | `techdebt.md` | deuda tecnica |

> 🚨 **El indice y las entradas se actualizan juntos, en la misma pasada.** Ver Paso 2b.

Al anadir una entrada:

1. Dale el **siguiente id libre** (mira el ultimo del indice, no cuentes entradas). Los ids no se reutilizan.
2. Escribe la entrada en la seccion de detalle, con su tabla de campos.
3. Anade su fila al **indice**, con el enlace de ancla.
4. Vuelve a correr la comprobacion del Paso 2b sobre ese archivo.

⚠️ **Los archivos arrancan vacios de entradas, con un `—` de marcador.** La primera entrada real de
cada archivo **sustituye ese marcador**, en el indice y en el detalle. Un `—` que sobrevive junto a
una entrada real deja el indice diciendo dos cosas a la vez.

Fechas absolutas (`2026-08-31`), nunca «ayer» ni «la semana pasada». En el indice, titulos cortos:
tienen que caber en una fila y decidirse sin abrir la entrada.

---

## Paso 3 — `_persistence/progress.md` (obligatorio)

Es el archivo principal: da la vision general, **no detalla tareas**. Actualizalo **siempre**, en
tres sitios:

**a) La seccion `## 1. Estado general`.** Es lo primero que se lee al abrir sesion, asi que se
sobrescribe entera: etapa, fecha, salud, avance y bloqueos activos.

**b) Las secciones `## 2. Ultimo realizado` y `## 3. Siguiente paso`.** Tambien se sobrescriben.
El siguiente paso es concreto: no «seguir con el desarrollo», sino la primera accion de manana.

**c) Una entrada nueva `S-XXX`** en `## 5. Bitacora`, mas su fila en el indice de sesiones, con:

1. **En que etapa va el proyecto.**
2. **Que quedo hecho hoy** — solo lo que esta en el diff.
3. **Cual es el siguiente paso concreto.**

Y si algun hito de `## 4. Hitos` cambio de estado, actualizalo.

### 🚨 La pregunta NO es «esta el archivo al dia?»

Es: **«tiene ESTA sesion su propia fila, con un id nuevo?»**

```bash
grep -n '^| \[S-' _persistence/progress.md | tail -1
```

🚨 **El criterio es el ID, no la fecha.** Esa fila tiene que llevar un `S-XXX` **mas alto** que el
que habia al arrancar. Si sigue el mismo id con el que empezaste, **falta la entrada** — y hay que
escribirla, diga lo que diga `Estado general`.

⚠️ **Por que el criterio no puede ser la fecha.** Puede haber **varios cierres el mismo dia**.
Comparar fechas no distingue dos tramos de la misma jornada: la ultima fila ya llevaria la fecha de
hoy siendo de otra sesion, y el control daria verde con la sesion entera sin registrar.

🔑 **Dos senales van a enganarte, y las dos se repiten:**

- **`Estado general` puede estar ya escrita**, porque `manager` la actualiza durante el dia.
  **Un archivo medio actualizado es peor que uno sin tocar: el trozo bueno avala al malo.**
- **Un arbol limpio no prueba que la entrada este escrita.** Significa «no queda trabajo», pero
  tambien puede significar «el trabajo se commiteo antes de que llegara el cierre».

---

## Paso 4 — `_persistence/tasks.md` (obligatorio)

Aqui el indice **es** el tablero: el estado de cada tarea vive en su fila, y se repite en la tabla
de campos de su entrada. **Las dos se actualizan juntas.**

**Los estados de este proyecto** (no hay otros, no inventes ninguno):

`Implementada` · `No implementada` · `Cancelada` · `Suspendida`

Y cada tarea lleva ademas **Importancia** (`Alta` / `Media` / `Baja`) y **Urgencia**
(`Bloqueante` / `No bloqueante`), mas **Origen** (`usuario` / `manager` / `report_auditor`).

- Mueve a `Implementada` solo lo que la evidencia respalde.
- Lo que quedo a medias **sigue en `No implementada`**, y su entrada de detalle dice **en que punto
  quedo**. No existe un estado intermedio: media tarea no es una tarea hecha.
- `Cancelada` y `Suspendida` **requieren razon registrada** en la entrada. Si no tienes la razon,
  no cambies el estado: preguntalo en el reporte.
- Anade las tareas nuevas que aparecieron hoy, con su id, su estado y su importancia/urgencia.
  🚨 **Importancia y urgencia no son tuyas para decidir a ojo:** si el diff o el traspaso no las
  dejan claras, ponles `Media` / `No bloqueante` y **marcalo en el reporte como pendiente de
  confirmar**.
- 🚨 **`Origen` es obligatorio y sale de la lista de `tasks.md`.** Si una tarea nace de algo que
  ninguno de los valores cubre, **no inventes un valor nuevo**: eso es una decision del usuario.
  Ponle el mas cercano y dilo en el reporte.
- Si una tarea estaba marcada `Implementada` y el diff la contradice, **desmarcala** y dilo en el
  reporte.

**Aqui entra tambien lo que produjeron los Pasos 2b y 2c**: si salieron al dia, no hay nada que
anotar; si algo fallo, la tarea nueva se anade con su id. Ese es el motivo de que aquellos
controles vayan arriba y no abajo.

Una tarea que se entiende en una linea **se queda en el indice** y su entrada de detalle es minima.
No infles el archivo.

### 🚨 Lo unico que NO puede entrar aqui: el resultado del push

**El push no se anota en `tasks.md`, y no es un olvido: es imposible.** Para saber si el push
funciono, el commit ya tiene que existir — y `tasks.md` va dentro de ese commit. Cualquier cosa que
quisieras escribir aqui sobre el push se escribiria antes de que el push ocurriera.

🔑 **Un segundo commit tampoco lo arregla:** tendria exactamente el mismo problema con su propio
push, y asi hasta el infinito. No hay orden de pasos que lo resuelva.

**Su sitio es el reporte de hoy**, en «Sin resolver» (Paso 8). Y el arranque de manana debe leer
`git status -sb` —no `--short`— porque `--short` no imprime la linea de la rama y un commit sin
subir le resulta **invisible**.

---

## Paso 5 — `_persistence/techdebt.md`: aqui si propones

La deuda tecnica es el unico registro del porque que **si deja rastro en la evidencia**: algo a
medias, un `TODO`, una comprobacion que quedo sin hacer, un archivo que quedo inconsistente.

Por eso, a diferencia de los cuatro de abajo, **puedes proponer entradas** — con dos condiciones:

1. **Solo lo que el diff respalde.** Nada de deuda intuida.
2. **Marcada como propuesta**, tanto en el campo `Confirmacion` de la entrada como en el reporte,
   para que el usuario la confirme o la tumbe.

🚨 **`Confirmacion` lleva dueno dentro del valor:** `Propuesta (pendiente del usuario)`, nunca
`Propuesta` a secas. Una propuesta sin dueno no espera a nadie — se queda propuesta para siempre.

Estados (los mismos cuatro): `Implementada` · `No implementada` · `Cancelada` · `Suspendida`,
donde `Implementada` significa deuda **ya pagada**. Mas Importancia y Urgencia, igual que en tareas.

⚠️ **`Cancelada` y `Suspendida` no las escribes tu:** significan «esto dejo de ser deuda» y
«decidimos convivir con esto por ahora», y las dos son decisiones del usuario, no lecturas del diff.

---

## Paso 6 — Los otros cuatro: **revisalos, no los escribas**

`decisions.md`, `assumptions.md`, `constraints.md` y `lessons.md` **no son del cierre**. Los escribe
`manager` en el momento en que las cosas pasan, porque una decision no aparece en el `git diff`:
nace en la conversacion, y tu no estuviste ahi.

**Lo que si haces: comprobar que no se quedaron cortos.**

1. Leelos.
2. Comparalos con lo que muestra el diff.
3. Si el diff ensena algo que **claramente fue una decision** y no esta anotado —se eligio una
   alternativa, se cambio una estructura, se descarto un camino— **no lo escribas tu**: senalalo en
   el reporte, para que lo dicte el usuario.

🚨 **Los cuatro se reportan siempre, aunque no falte nada.** El Paso 8 tiene una seccion propia para
ellos: cada uno sale con «al dia» o con lo que falta por anotar. Sin esa linea, un cierre que reviso
y uno que no reviso se ven igual.

### 🚨 Una comprobacion concreta sobre `decisions.md`: las que verifican, con comando y salida

Al leer `decisions.md`, mira **las entradas de esta sesion que afirmen un resultado comprobado**.
Cada una debe llevar un bloque de verificacion con la **orden ejecutada literal** y **su salida
cruda**. Son dos grupos, y el segundo se olvida:

| Grupo | Ejemplos |
|---|---|
| las de `Origen: report_auditor` | «verificado que el hallazgo persiste en `HEAD`» |
| **las de iniciativa propia que afirman un resultado** | «no hay secretos en el archivo», «cero coincidencias», «los dos numeros cuadran» |

⚠️ **El segundo grupo no lo pidio nadie, y por eso se cuela sin evidencia.** Una comprobacion que
hacemos por nuestra cuenta se siente como parte del trabajo, no como una afirmacion auditable —
pero en el registro se lee igual que cualquier otra. Sin patron ni ambito escritos, el auditor tiene
que rehacer el barrido entero para contrastarlo.

| Que dice la entrada | Que es | Que haces |
|---|---|---|
| «corri `git log -1 …`», y debajo lo que salio | evidencia | nada, esta bien |
| «se comprobo», «verificado», «existe y es legible» | **un veredicto sin evidencia** | 🚨 senalalo en el reporte del Paso 8 |

⛔ **No lo arregles tu, y menos aun reconstruyendo el comando ahora.** Vale lo mismo que en el resto
del paso: los cuatro archivos no son tuyos. Y aqui hay una razon extra — un bloque de verificacion
que no se ejecuto cuando dice haberse ejecutado es **peor que su ausencia**: convierte «falta
evidencia» en «hay evidencia falsa». Senalar, no rellenar.

⚠️ **Rige hacia adelante.** Las entradas antiguas que solo dijeron «se comprobo» se quedan como
estan; no las reportes como pendientes.

#### 🚨 Y una segunda pasada sobre los mismos bloques: el **ambito temporal**

El bloque puede llevar su comando y su salida cruda —y aun asi estar mal— si **afirma reproducirse
sobre un commit que todavia no existia cuando se ejecuto**. Es un defecto distinto del anterior y se
cuela justo despues de corregirlo.

**El mecanismo es siempre el mismo, y por eso se puede buscar:** el barrido se corre *mientras* se
escribe la entrada; despues **tu** anades el informe de la sesion, cierras el archivo de estado y
escribes el de tareas — y con eso cambias el resultado del comando que la entrada acaba de
registrar. La cifra no envejece: **nace desfasada.**

Sobre las entradas **de esta sesion**, marca las que cumplan las dos condiciones a la vez:

| Condicion | Como se reconoce |
|---|---|
| **Ambito alcanzable por el cierre** | el comando barre el repositorio entero (`-- .`, o sin `pathspec`), o nombra una ruta que tu vas a escribir en esta misma pasada |
| **Se declara reproducible sobre su propio commit** | dice «se reproduce sobre el commit que la contiene», o usa `HEAD` **sin decir cual era** |

Un bloque que cumple una sola no es hallazgo: el ambito acotado a lo que la sesion no toca **si** se
reproduce, y un recuento global **fechado** —«al momento de escribir esta entrada»— esta bien escrito.

**Como se corrige, y no lo haces tu:** basta **anclarlo a un hash** (`git grep … <hash> -- …`) o
**fecharlo**. Lo señalas en el reporte del Paso 8 con la entrada y el bloque; `manager` decide cual
de las dos aplica antes del commit.

⚠️ **Un caso que no se arregla anclando, y conviene reconocerlo:** si el comando mide algo que **tu
mismo produces en cada cierre** —una fila que escribes siempre antes de commitear—, entonces no
devuelve nunca el valor «limpio» en un commit de cierre: no mide lo que dice medir, mide que el
commit es un cierre. Ahi el arreglo no es el ancla sino **el momento de comprobacion**, y eso lo
replantea `manager`, no tu.

⚠️ **Rige hacia adelante**, igual que la comprobacion anterior: entradas de esta sesion, no las
antiguas.

### 🚨 Un riesgo nombrado en el informe y en ningun otro sitio: senalalo

Al leer el borrador del informe, busca los riesgos que **el propio texto reconoce** —«si algun dia
X, hoy nada lo detectaria», «esto asume que Y», «queda por confirmar Z»— y comprueba si cada uno
tiene **codigo** en `_persistence/`: un `A-XXX`, una `T-XXX` o un `DT-XXX`. Si no lo tiene,
**senalalo en el reporte del Paso 8**.

🔑 **El informe es el canal, no el registro.** Un riesgo escrito solo ahi se lee mientras ese
informe sea el ultimo, y deja de leerse en cuanto llega el siguiente. Peor si el riesgo colgaba de
una deuda que se marca `Implementada` en la misma sesion: **desaparece del radar en el momento
exacto en que se cierra lo que lo contenia**, porque una entrada pagada ya no se relee.

⛔ **No lo registres tu** —los cuatro archivos del porque no son tuyos—: senalalo, con la frase del
informe que lo enuncia, para que `manager` le ponga codigo antes del commit.

**La unica excepcion, y es mecanica:** si un supuesto `A-XXX` quedo comprobado por la evidencia del
diff, puedes moverlo a `decisions.md` o `lessons.md` y marcarlo `Confirmado` en `assumptions.md`.
Eso no es interpretar, es aplicar la regla del ascenso — y **dilo en el reporte**. Al moverlo, toca
**los dos indices**, con id nuevo en el destino.

### 🚨 Una casilla mas, obligatoria: que entra al repositorio remoto

**Este proyecto sube a un remoto —el que declare `project.md`—, y `_persistence/` va a Git a
proposito**: es la historia del proyecto. Asi que pregunta, en voz alta, sobre el diff de hoy:

> **Entro algo que no deberia salir de esta maquina?** Credenciales, tokens, rutas personales,
> datos de terceros, contenido de fuentes externas copiado sin necesidad.

Si entro, **sale** — y se sustituye por un equivalente inventado, dicho como inventado.

⚠️ **Honestidad sobre su fuerza, y va escrito porque importa: esto pregunta, no detecta.** No es un
test y no muerde. `.gitignore` cubre `.env`, pero **no cubre una credencial pegada dentro de una
leccion**. Ese es el camino por el que algo se escapa sin que ninguna herramienta lo note.
**Marcarla sin haber mirado el diff es marcarla con una intencion.**

📌 Se reporta siempre, igual que los cuatro.

---

## Paso 6b — El informe para la auditoria (obligatorio)

Escribe **`_audit/S-XXX.md`**, con el mismo id que la entrada que acabas de crear en `progress.md`.
Un archivo por sesion. Si `_audit/` no existe, creala.

🚨 **Va antes del `git add`, y no es un detalle de orden: es lo que hace auditable la auditoria.**
Al entrar en el mismo commit que el trabajo que describe, el auditor puede averiguar exactamente
que estado esta juzgando:

```bash
git log -1 -- _audit/S-XXX.md
```

Con ese hash el auditor puede ir al `git show` y **verificar cada afirmacion del informe contra el
diff real**, en vez de creersela. Un informe que no se puede anclar a un commit deja al auditor
juzgando un relato.

### Para quien escribes

El auditor **arranca en frio: no vivio la sesion y nadie va a contarsela**. Lo unico que tendra son
este informe, los archivos y `git`. No escribas como si compartiera contexto:

- **Cita siempre codigo y ruta** —tal como aparecen en tu registro, p. ej. `T-NNN`, `D-NNN`,
  `_persistence/tasks.md`—. Son su unica via para ir a comprobar.
- **Explica lo que no se deduce del diff**, pero no repitas los archivos enteros: el informe cuenta
  **esta sesion**, no el proyecto entero.
- 🚨 **Escribe el informe completo, sin resumir.** Lo que se ahorre aqui es exactamente lo que el
  auditor tendra que reconstruir, y lo reconstruira adivinando.

### 🚨 Las dos listas del informe se **generan**; escribirlas de memoria es como se quedan cortas

Las secciones 1 y 2 llevan cada una una enumeracion, y **una enumeracion sin salvedad se lee como
exhaustiva**. Es justo el tipo de frase que el auditor usa como atajo para no recorrer el diff
entero — asi que una lista corta no se queda en un descuido: **ensena a confiar en algo que no se
puede contrastar sin rehacerlo**.

Las dos son generables. Sacalas de aqui, no de lo que recuerdes haber tocado:

```bash
git show --stat --name-only --format= <commit>          # seccion 1: archivos tocados
sed -n '/^## Indice/,/^---/p' _persistence/tasks.md \
  | grep "No implementada"                              # seccion 2: tareas abiertas
```

⚠️ **El cierre anade archivos que no son «de contenido»** —la fila de `_audit/index.md`, el propio
informe— y son justo los que se olvidan al escribir de memoria. Si prefieres listar solo los de
contenido, **dilo**: «los archivos de contenido; el cierre anade ademas…». Una lista declarada
parcial es honesta; una lista corta presentada como completa, no.

🚨 **Y por eso la seccion 1 no lleva una lista redactada: lleva la salida pegada.** La estructura de
abajo lo pide asi, y no es una preferencia de formato. Este mismo aviso ya existia cuando `S-007`
escribio una lista de ocho contra un comando que devolvia diez, y no lo evito: un aviso dentro de un
bloque explicativo se lee una vez, mientras que un hueco en la plantilla se ve cada vez que se
escribe la seccion. Una salida pegada tampoco puede quedarse corta — o esta entera, o se nota.

🚨 **Y no filtres «las relevantes» sin decirlo.** Si la seccion 2 solo cubre algunas tareas
abiertas, la frase lo tiene que decir. El coste de la version correcta es cero; el de la incorrecta
es que la proxima omision, cuando importe, llegue con la misma cara de completa.

### Estructura del informe

```markdown
# Informe de auditoria — S-XXX

| Campo | Valor |
|---|---|
| Sesion | S-XXX |
| Fecha | AAAA-MM-DD |
| Etapa | |
| Rama | la rama principal, segun `project.md` |
| Commit auditado | el commit que contiene este archivo (`git log -1 -- _audit/S-XXX.md`) |

## 0. Respuesta a la auditoria anterior     <-- omitir solo si no hay ninguna sin responder

| Hallazgo | Veredicto | Evidencia / Razon |
|---|---|---|
| F-NNN — <resumen> | Implementado | `T-NNN`, en este commit |
| F-NNN — <resumen> | Aceptado — pendiente | `T-NNN`, `No implementada` |
| F-NNN — <resumen> | No se implementa | `D-NNN` |

## 1. Que se hizo

<PEGA AQUI, sin editar, la salida cruda de:>
<`git show --stat --name-only --format= <commit>`>
<es la lista completa e incluye los archivos que anade el propio cierre: el informe y la fila de `_audit/index.md`>

<y debajo, lo que muestra el diff: con codigos y rutas, que archivos nacieron, cuales cambiaron y por que>

## 2. Que NO se hizo, y por que
<lo que quedo pendiente o a medias, y en que punto quedo>
<las tareas abiertas salen del indice de `tasks.md` filtrando `No implementada`, no de la memoria>

## 3. Decisiones tomadas
<cada `D-XXX` de esta sesion: que se decidio, por que, y **las alternativas descartadas**>

## 4. Supuestos vigentes y riesgos
<`A-XXX` abiertos, que se apoya en ellos, y que pasa si resultan falsos>

## 5. Siguiente tarea propuesta
<la primera accion concreta de la proxima sesion, con su codigo, importancia y urgencia>

## 6. Que pedimos auditar
<nuestros propios puntos debiles: lo que quedo flojo, la decision de la que menos seguros
estamos, el supuesto en el que nos apoyamos sin confirmar>

## 7. Evidencia del Paso 2d
<la lista COMPLETA que devolvio la primera orden del Paso 2d, con la orden literal, su recuento y
todas sus lineas — nunca una seleccion, y sin deduplicar>
<el recuento es el de LINEAS devueltas; si se da el de ordenes distintas, va aparte y con ese nombre>
<la orden se escribe en su forma anclada al commit y con el propio informe excluido
(`":(exclude)_audit/S-XXX.md"`), o se dice al lado cual es esa equivalencia>
<y debajo, el resultado de reejecutar cada una: la que reproduce y la que no>
<si una orden no es reproducible por naturaleza (describe el area de staging), se dice, y se da su
equivalencia anclada al commit>
<si la lista salio vacia, se publica igual: la orden y su salida vacia>
<y si se anota de que archivo sale cada orden, esa procedencia se DERIVA del diff, nunca se
escribe a mano: se pega la orden que la produce y su salida cruda>
```

### Los tres veredictos de la seccion 0, y nada mas

| Veredicto | Cuando |
|---|---|
| `Implementado` | hecho, y esta en este commit |
| `Aceptado — pendiente` | de acuerdo, pero aun no hecho — **con su `T-XXX`** |
| `No se implementa` | rechazado — **con su `D-XXX`** |

### 🚨 Esa tabla se audita fila a fila. Cada veredicto exige algo comprobable

| Veredicto | Lo que el auditor va a comprobar | Si no esta |
|---|---|---|
| `Implementado` | que la correccion **aparezca en el diff de este commit** | es un hallazgo, y el original **sigue abierto** |
| `Aceptado — pendiente` | que cite su `T-XXX`, y que esa tarea **exista y siga abierta** | el hallazgo no se da por recogido |
| `No se implementa` | que cite su `D-XXX` | un rechazo sin decision registrada **no es auditable** |

⚠️ **No marques `Implementado` lo que el diff no muestre.** Si estas de acuerdo pero no esta hecho,
su veredicto es `Aceptado — pendiente` con su tarea abierta. Marcarlo hecho no lo adelanta: lo
convierte en un hallazgo nuevo y deja el original abierto igual.

### 🚨 La tabla va completa: un hallazgo omitido NO cuenta como contestado

**Todos los hallazgos entregados y no cerrados entran en la tabla**, uno por fila, incluso los que
no tocaste esta sesion. Un `F-NNN` que no aparezca **sigue entregado y el auditor lo reclama**: no
se interpreta como aceptado ni como rechazado por omision.

Si un hallazgo no se atendio y no sabes por que, **ponlo igual** y dilo en «Sin resolver» del
reporte. Una fila incomoda vale mas que una ausencia silenciosa.

🚨 **`Aceptado — pendiente` no es opcional ni un adorno.** Sin el, un hallazgo con el que estamos de
acuerdo pero que aun no hicimos no esta implementado ni rechazado: **no aparece en ningun sitio y
desaparece del radar.** Esa es la forma en que se pierden los hallazgos buenos.

⚠️ Un hallazgo rechazado **por coste o prioridad** —no por ser incorrecto— es deuda tecnica por
definicion y exige su `DT-XXX`. Un rechazo por coste sin entrada en `techdebt.md` es, por si solo, un
hallazgo del auditor, y no requiere criterio: se comprueba mirando si la entrada existe.

### 🚨 Si el rechazo clasifica el asunto como reversible o irreversible, dilo como criterio

Un `No se implementa` que apoye su razon en ese eje **tiene que declarar que la clasificacion se
hizo a criterio**, en la propia fila o en el `D-XXX` que cita: «reversible a criterio, porque…».
Mientras no exista un inventario de acciones irreversibles registrado en `_persistence/`, escribir
«es reversible» a secas **presenta una tabla que no existe**, y el auditor no tiene como distinguir
un criterio de una consulta.

### 🚨 La seccion 6 es obligatoria y no puede quedar vacia

Un informe que solo cuenta lo bien que fue todo produce auditorias flojas: el auditor gasta su turno
redescubriendo lo que nosotros ya sabiamos.

**Senalar nuestros propios puntos debiles lo manda directo a lo que importa.** Escribe al menos un
punto real. «Nada que senalar» **no es una respuesta valida**: si de verdad no encuentras ninguno,
di que no lo encontraste y que eso mismo conviene revisarlo.

⚠️ Sigue rigiendo la regla de siempre: **solo lo que la evidencia respalde**. Un punto debil
inventado desperdicia la auditoria igual que uno omitido.

### Y su fila en `_audit/index.md`

El informe no sirve de nada si la auditoria no sabe que existe. **Anade su fila** al tablero, con
`Pendiente` en las columnas que todavia no puedes rellenar:

```markdown
| `S-XXX.md` | S-XXX | AAAA-MM-DD | Pendiente | Pendiente | Pendiente | - |
```

Las columnas son `Informe | Sesion | Fecha | Commit auditado | Auditoria | Veredicto | Hallazgos`.
Sus convenciones estan escritas dentro del propio `_audit/index.md`: **leelas antes de escribir**.

🚨 **`Pendiente` es lo unico que escribes tu en las tres ultimas columnas.** El veredicto y los
hallazgos los pone el agente `report_auditor` cuando corra — tu no puedes saber que va a encontrar alguien
que todavia no ha mirado.

⚠️ **Y el commit auditado tampoco lo escribes, aunque parezca que si.** No puedes: la fila se
escribe **antes** del commit que la contiene. Lo rellena la auditoria, que ya lo tiene delante con
`git log -1 --format=%h -- _audit/S-XXX.md`. Es la misma imposibilidad que la del push (Paso 4), y
la misma solucion: preguntarle a git en vez de intentar escribirlo.

⚠️ **Este informe no reemplaza a `_persistence/`.** Es una vista de **esta sesion** para un lector
que arranca en frio, no una copia del registro.

⛔ **No toques `_audit/findings.md`.** Ese archivo es del auditor: registra lo que encontro y en que
acabo cada hallazgo. Tu no has abierto ninguno.

---

## Paso 7 — El commit y el push

**Primero la verificacion, despues el commit.** Nunca al reves.

```
git status
```

🚨 Comprueba que **no aparezca ningun archivo de secretos** (`.env` y variantes). Si aparece,
**detente**, no anadas nada y reportalo: falta una linea en `.gitignore`. Git no olvida — si una
credencial entra al historial, borrar el archivo despues no la borra.

Si esta limpio:

```
git add -A
git commit -m "..."
```

El mensaje dice **que avanzo y por que**, no que archivos cambiaron: eso ya lo sabe Git. Primera
linea corta, y debajo lo que valga la pena. Termina siempre con:

```
Co-Authored-By: Claude Opus 5 <noreply@anthropic.com>
```

### 7b — Que el informe entro en el commit (obligatorio)

**Ya hay un hash. Preguntale a git si el informe esta dentro de el:**

```bash
git show --stat --name-only HEAD -- _audit/S-XXX.md
git show --stat --name-only HEAD -- _audit/index.md
```

Si el archivo aparece en la salida, entro. Si la salida esta vacia, **no entro**.

🚨 **Esta comprobacion es la que sostiene el Paso 6b entero.** El anclaje del informe al commit es
todo su valor: sin el, el auditor recibe un relato que no puede contrastar contra ningun estado. Un
paso obligatorio cuyo cumplimiento nadie mira **no es obligatorio, es una intencion**.

**Hay tres resultados, no dos** —los mismos que el Paso 2b, y por la misma razon:

| Que sale | Que significa | Que haces |
|---|---|---|
| los dos archivos aparecen | el informe quedo anclado | sigue al push |
| alguno falta | **el commit no lo lleva** | 🚨 **detente**: escribelo o anadelo y **haz un commit nuevo** que lo incluya, nunca un `--amend`. Dilo en el reporte |
| el comando falla | **no lo comprobaste** | push igual, y a **Sin resolver** con `🚨 SIN COMPROBAR` |

🚨 **La tercera fila otra vez.** «No pude comprobarlo» no es «esta bien». Y la segunda no se arregla
reescribiendo el commit: los comandos de abajo siguen prohibidos, tambien aqui.

⛔ **Comandos prohibidos, sin excepcion:** `git commit --amend`, `git reset`, `git checkout --`,
`git restore`, `git rebase`, `git clean`, `git push --force` y cualquier otra cosa con `--force`.
El trabajo del cierre es **anadir** historia, nunca reescribir ni borrar la que hay. Si crees que
hace falta uno de esos, **detente y dilo**: esa decision es del usuario.

### El cierre no acaba en el commit

```
git push
```

⚠️ **Si es el primer push del repositorio**, la rama todavia no existe en el remoto:

```
git push -u origin main
```

🔑 **Un `git push` a secas solo anade, y por eso si entra en el protocolo** — encaja con la regla de
arriba, no la rompe. Lo que reescribe historia es `--force`, y ese sigue prohibido.

Despues, siempre:

```
git status -sb
```

🚨 **Si la primera linea todavia dice `ahead`, el push no ocurrio** —remoto sin configurar,
credenciales, red— y el trabajo existe solo en este disco. **No lo tapes:** va en el reporte, en
«Sin resolver», con lo que salio mal. Un disco roto esa noche se lleva la sesion entera.

⚠️ **Y ahi se queda: en el reporte.** No vuelvas atras a anotarlo en `tasks.md` —ya esta
commiteado— ni abras un commit nuevo para arreglarlo. El porque esta en el Paso 4.

> 🔑 La regla no es «si no hay hash, no hubo cierre»: eso se cumple entero y el trabajo se queda sin
> subir igual, porque **un commit es local**. La regla es **«si el hash no esta en `origin`, no hubo
> cierre»**, y se comprueba con `git status -sb`, no con el hash.

---

## Paso 8 — Reporte en pantalla

En espanol, sin relleno. **Entregalo completo**, no un resumen diciendo que «ya actualice los
archivos».

🚨 El mensaje final del agente no llega al usuario por si solo: lo recibe `manager`, que lo
retransmite. Un reporte recortado se recorta dos veces.

```
## Cierre de sesion — <fecha>

### Lo que dice la evidencia
- <N> archivos tocados: <los principales>
- <que quedo hecho, segun el diff>

### _persistence/ actualizado
- progress.md — <S-XXX nueva> · <en una linea, que cambio en «Estado general»>
- tasks.md — <N implementadas, N pendientes, N nuevas>
- techdebt.md — <sin novedad | PROPUESTA: DT-XXX ... (pendiente de confirmar)>

### Los cuatro del porque — revisados, no escritos
- decisions.md — <al dia | falta anotar: ... | 🚨 D-XXX verifica sin comando ni salida>
- assumptions.md — <al dia | falta anotar: ... | ascendido A-XXX → D-XXX>
- constraints.md — <al dia | falta anotar: ...>
- lessons.md — <al dia | falta anotar: ...>
- 🚨 Repositorio remoto — <nada sensible, diff mirado | 🚨 SACAR: ...>

### Controles
Fuga de datos propios (1b) — <cero lineas | 🚨 <las lineas> | 🚨 SIN COMPROBAR — <que falta en project.md>>
Indices de `_persistence/` (2b) — <al dia | corregidos | 🚨 SIN COMPROBAR — <que fallo>>
Carpetas declaradas (2c) — <coinciden | <las diferencias y su razon> | 🚨 SIN COMPROBAR — <por que>>

### Commit
Informe de auditoria — <`_audit/S-XXX.md` y su fila en `_audit/index.md`, **comprobados en el commit** (Paso 7b) | 🚨 NO ENTRO — <que falto y en que commit nuevo entro> | 🚨 SIN COMPROBAR — <que fallo>>
<hash corto> — <primera linea del mensaje>
<"subido a origin, `git status -sb` sin ahead" | 🚨 "SIN SUBIR — <que fallo>">

### Informe para la auditoria
`_audit/S-XXX.md` — version corta:
- **Se hizo:** <una linea>
- **Quedo pendiente:** <una linea>
- **Siguiente tarea propuesta:** <codigo y accion>
- **Pedimos auditar:** <los puntos de la seccion 6, en una lista breve>

### Falta la auditoria
El commit existe: **`manager` tiene que lanzar ahora el agente `report_auditor`** sobre <hash corto>.
La sesion no esta cerrada hasta que esa auditoria este registrada en `_audit/`.

### Para manana
<el siguiente paso concreto, tal como quedo en progress.md>

### Sin resolver        <-- omitir si no hay nada
- <discrepancias entre el traspaso y el diff>
- <lo que quedo a medias y en que punto>
- <lo que hay que preguntarle al usuario>
```

---

## Reglas del protocolo

- **No inventes** avances, fechas, decisiones ni tareas. Si un archivo esta vacio o falta
  informacion, **dilo en el reporte** en lugar de rellenarlo.
- **No escribas codigo** ni arregles nada, aunque veas algo roto. Anotalo en `tasks.md` y sigue.
  Cerrar la sesion no es el momento de abrirla otra vez.
- **No toques `temporal/`** ni los archivos del auditor (`_audit/R-XXX.md`, `_audit/findings.md`).
- **No dupliques.** Cada archivo tiene un trabajo: `progress.md` da la vision general y no detalla
  tareas; el detalle de tareas vive solo en `tasks.md`.
- **Escribe corto.** Un `progress.md` que nadie lee no orienta a nadie.
- 🚨 **Tu no lanzas la auditoria, pero la reclamas.** El agente `report_auditor` corre despues de ti,
  sobre el commit que acabas de hacer, y lo lanza `manager`. Tu ultima linea util es recordarselo:
  un cierre sin auditoria deja el trabajo commiteado y sin revisar, que es exactamente el estado que
  este sistema existe para evitar.
