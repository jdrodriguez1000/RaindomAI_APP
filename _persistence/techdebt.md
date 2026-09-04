# techdebt.md

> Registro de la **deuda tecnica** del proyecto: atajos conscientes, soluciones provisionales
> y pendientes de calidad. Cada item tiene codigo `DT-XXX`, estado, importancia y urgencia.
> La deuda se registra en el momento en que se contrae.

---

## Indice

| Codigo | Deuda tecnica | Estado | Confirmacion | Importancia | Urgencia |
|---|---|---|---|---|---|
| [DT-001](#dt-001---debtecmd-incumple-la-regla-de-nombres-en-ingles) | `debtec.md` incumple la regla de nombres en ingles | Implementada | Confirmada | Baja | No bloqueante |
| [DT-002](#dt-002---_workflow-nace-sin-ningun-enganche-de-uso-l-014) | `_workflow/` nace sin ningun enganche de uso (`L-014`) | No implementada | Propuesta (pendiente del usuario) | Media | No bloqueante |
| [DT-003](#dt-003---cinco-lineas-del-registro-publican-ordenes-con-un-caracter-de-control-x08-y-no-se-reejecutan-l-024) | Cinco lineas del registro publican ordenes con un caracter de control `\x08` y no se reejecutan (`L-024`) | No implementada | Propuesta (pendiente del usuario) | Media | No bloqueante |
| [DT-004](#dt-004---siete-lineas-nuevas-de-s-019-repiten-el-defecto-de-dt-003-en-decisionsmd-y-tasksmd) | Siete lineas nuevas de `S-019` repiten el defecto de `DT-003`, en `decisions.md` y `tasks.md` | No implementada | Propuesta (pendiente del usuario) | Media | No bloqueante |

---

## Convenciones

| Campo | Valores posibles |
|---|---|
| Codigo | `DT-XXX`, correlativo, no se reutiliza |
| Estado | `Implementada` / `No implementada` / `Cancelada` / `Suspendida` |
| Importancia | `Alta` / `Media` / `Baja` |
| Urgencia | `Bloqueante` / `No bloqueante` |
| Origen | `usuario` / `manager` / `report_auditor` |
| Confirmacion | `Confirmada` / `Propuesta (pendiente de <quien>)` |

`Implementada` = la deuda ya fue pagada (corregida). `No implementada` = sigue pendiente de pago.

🚨 **`Confirmacion` y `Estado` son ejes distintos, y por eso son dos campos.** `Estado` dice si la
deuda **se pago**; `Confirmacion` dice si **es deuda**. Una entrada puede estar confirmada y sin
pagar —lo normal— pero tambien propuesta y sin confirmar: alguien la detecto y nadie ha dicho
todavia que el atajo fuera un atajo.

🚨 **`Propuesta` lleva dueno dentro del valor, siempre.** No existe `Propuesta` a secas: quien
confirma va escrito (`Propuesta (pendiente del usuario)`), porque una propuesta sin dueno no espera
—se queda propuesta para siempre—. Si no sabes quien confirma, entonces lo que falta no es la
confirmacion: es saber de quien es la decision, y eso es una `T-XXX`.

⚠️ **El caracter provisional va en el indice, no solo en el detalle.** El ojo entra por la tabla de
arriba; una entrada `Propuesta` que en el indice se ve igual que una confirmada es, en la practica,
una confirmada.

⚠️ **El titulo de una deuda nombra el defecto, y no cambia al pagarla.** Al pasar a `Implementada`,
lo que se fecha es el cuerpo —«🕐 estado al AAAA-MM-DD, ya corregido»— para que no siga hablando en
presente de algo ya resuelto.

🚨 **El indice se escribe a mano, sin generador.** Cada fila enlaza por ancla a su deuda.

---

## Deuda registrada

<!--
Plantilla:

### DT-XXX - Titulo
| Campo | Valor |
|---|---|
| Estado | No implementada |
| Confirmacion | |
| Importancia | |
| Urgencia | |
| Origen | |
| Fecha | AAAA-MM-DD |

- **Deuda:** que atajo se tomo.
- **Por que se tomo:** que se gano a cambio.
- **Costo de no pagarla:** que pasa si se queda.
- **Como se paga:** que habria que hacer.
-->

### DT-001 - `debtec.md` incumple la regla de nombres en ingles
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Confirmacion | Confirmada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Origen | usuario |
| Fecha | 2026-08-31 |

- **Deuda:** `D-017` fija que los nombres de archivos y carpetas van en ingles. `debtec.md`
  —abreviatura de «deuda tecnica»— es el unico archivo trackeado que no cumple. Se deja como esta.
- **Por que se tomo:** la regla se decidio con efecto **hacia adelante**. Renombrar obligaria a
  tocar sus referencias en los tres skills, en los agentes, en `project.md` y en `CLAUDE.md`, sobre
  un estado que la auditoria `R-001` ya dio por bueno; el beneficio es de coherencia, no funcional.
- **Costo de no pagarla:** el registro exhibe una excepcion a su propia regla. Mientras este
  escrita aqui es una excepcion conocida; si nadie la anota, en dos sesiones se lee como que la
  regla no existe, y el siguiente nombre en espanol entra sin que nadie lo discuta.
- **Como se paga:** renombrar a `techdebt.md` con `git mv`, actualizar todas sus referencias, y
  comprobar con `git grep -n "debtec" -- .` que no queda ninguna.

🕒 **Estado al 2026-09-01: confirmada y pagada.** El usuario confirmo la deuda y pidio pagarla
en la misma peticion —ordenar el renombrado es confirmar que el atajo era un atajo—, asi que
`Confirmacion` pasa a `Confirmada` y `Estado` a `Implementada` en la misma pasada. El archivo es
ahora `_persistence/techdebt.md` (`git mv`), y se reescribieron las **referencias vivas**: los tres
skills, `session-closer.md`, `CLAUDE.md`, `project.md` y la tabla de estructura de `progress.md`.
**El titulo de esta entrada se deja como esta**, porque nombra el defecto que hubo y no el estado de
hoy. Alcance y verificacion, en `D-021`.

🕒 **Nota anadida el 2026-09-01 (`S-005`), tras el hallazgo `F-009` de `R-004`.** El campo «Como se
paga» de arriba **se deja tal cual se escribio** y pide `git grep -n "debtec" -- .` en cero, sin
acotar ambito. Ese criterio literal **no se cumple y no se pretendio cumplir**: `D-021` acoto el
pago al ambito vivo y dejo lo historico intacto a proposito. Escrito el criterio absoluto y no la
excepcion, quien lo aplique tal cual concluye que la deuda no esta pagada.

**El criterio de cierre realmente aplicado es este:** cero referencias `debtec` en `.claude`,
`CLAUDE.md` y `project.md` —el ambito vivo que fija `D-021`—, con lo historico de `_audit/`,
`decisions.md` y la narrativa de `progress.md` intacto por decision del usuario. Sobre `HEAD`:

```
$ git grep -n "debtec" HEAD -- .claude CLAUDE.md project.md ; echo "exit=$?"
exit=1

$ git ls-tree --name-only HEAD _persistence/ | grep -i debt
_persistence/techdebt.md
```

⚠️ Con ese criterio, `DT-001` esta pagada. Con el literal de «Como se paga», no lo estaria nunca
—reescribir `_audit/` es justo lo que `D-021` descarto—. **Manda el de esta nota.**

🕒 **`Confirmacion` revertida a `Propuesta (pendiente del usuario)` el 2026-09-01, tras el
hallazgo `F-003` de `R-002`.** La entrada nacio en el cierre de `S-002` con `Confirmada`, y el Paso 5
de `protocol-close` prohibe expresamente ese valor al `session-closer`: lo que el escribe va
**marcado como propuesta**, para que el usuario la confirme o la tumbe. El propio `S-002` §6 admite
que el valor descansaba en el traspaso de la sesion, no en el diff, y no existe ningun `D-XXX` que
ampare la excepcion. `manager` **tampoco puede confirmarla**: quien confirma esta escrito dentro del
valor, y es el usuario. El campo `Origen: usuario` se deja como esta — dice de quien nacio la deuda,
no que la confirmacion se haya producido.

---

### DT-002 - `_workflow/` nace sin ningun enganche de uso (`L-014`)
| Campo | Valor |
|---|---|
| Estado | No implementada |
| Confirmacion | Propuesta (pendiente del usuario) |
| Importancia | Media |
| Urgencia | No bloqueante |
| Origen | manager |
| Fecha | 2026-09-02 |

- **Deuda:** `_workflow/` nacio en esta sesion (`D-046`) con sus tres enganches de **control** —fila
  en «Carpetas propias» de `project.md`, entrada en la lista de lo copiable tal cual de `CLAUDE.md`,
  ambito del Paso 1b de `protocol-close`—, pero **ningun** enganche de **uso**: nada en `_phases/`
  ni en ningun protocolo manda leer `team.md` o `ai_levels.md` en el momento en que aplican. Lo deja
  registrado `L-014` de `lessons.md`.
- **Por que se tomo:** los tres enganches de control eran los que ya se sabia que hacian falta,
  porque `_templates/` habia pasado por lo mismo. El cuarto —que alguien tenga que abrir la
  carpeta— exige decidir **en que punto de que etapa** se consulta, y esa es una decision de
  `_phases/` que le toca al usuario, no algo que el cierre de sesion pueda resolver.
- **Costo de no pagarla:** ninguno de los tres controles existentes detecta esta deuda —una carpeta
  agnostica, declarada y sin fugas, pero que nadie abre nunca, deja el repositorio «coherente» con
  material muerto dentro—. Sin el cuarto enganche, `_workflow/` corre el riesgo de quedar como
  documentacion que nadie consulta cuando llegue el momento de repartir trabajo o elegir un nivel de
  sistema de IA.
- **Como se paga:** decidir en que archivo de `_phases/` (o en que otro punto del metodo) se cita
  `_workflow/team.md` y `_workflow/ai_levels.md`, y con que `D-XXX`.

📌 **Propuesta del cierre `S-009`**, a partir de `L-014`. `manager` no la escribe como deuda
confirmada porque resolverla implica una decision de diseño —donde exactamente se engancha— que le
corresponde al usuario.

📌 **Nota del 2026-09-02 (`T-034`, hallazgo `F-026`): el cuerpo de esta entrada citaba
`L-013` donde corresponde `L-014`.** Se corrige la cita, que es una remision cruzada dentro del
mismo registro y llevaba a la leccion equivocada. No cambia nada del fondo de la deuda: las
otras tres menciones —titulo, fila del indice y este cierre— ya citaban bien.

```
$ git show 99c3aa3:_persistence/techdebt.md | grep -n 'registrado `L-01[34]` de'
149:  registrado `L-013` de `lessons.md`.

$ grep -n 'registrado `L-01[34]` de' _persistence/techdebt.md
149:  registrado `L-014` de `lessons.md`.
```

---

### DT-003 - Cinco lineas del registro publican ordenes con un caracter de control `\x08` y no se reejecutan (`L-024`)
| Campo | Valor |
|---|---|
| Estado | No implementada |
| Confirmacion | Propuesta (pendiente del usuario) |
| Importancia | Media |
| Urgencia | No bloqueante |
| Origen | report_auditor |
| Fecha | 2026-09-03 |

- **Deuda:** cinco lineas de `_persistence/decisions.md` y `_persistence/tasks.md` publican bloques
  de verificacion cuyas ordenes llevan el caracter de retroceso `0x08` donde el autor escribio `\b`
  (limite de palabra). Son dieciocho apariciones del caracter repartidas en esas cinco lineas. El
  bloque se ve correcto en pantalla y **no se reejecuta tal como esta escrito**: quien copie la
  linea le pasa al interprete un caracter de control y obtiene otro resultado. Lo destapo `L-024`
  en `S-017`; `F-042` (`R-017`) señalo que quedaba sin `T-XXX` ni `DT-XXX`, y esta entrada lo tapa.

```
$ python -c "import io,re; pat=re.compile(u'[\x00-\x08\x0b\x0c\x0e-\x1f]'); [print(f,i,repr(m.group())) for f in ['_persistence/decisions.md','_persistence/tasks.md'] for i,l in enumerate(io.open(f,encoding='utf-8'),1) for m in pat.finditer(l)]" | awk '{print $1, $2}' | uniq -c
      2 _persistence/decisions.md 917
      2 _persistence/decisions.md 1304
      2 _persistence/tasks.md 1212
     10 _persistence/tasks.md 1931
      2 _persistence/tasks.md 1987
```

- **Por que se tomo:** el atajo es **no reescribir las cinco lineas**, y es deliberado. Reescribir un
  bloque antiguo para que exhiba una orden que en su dia no se ejecuto asi convierte «falta
  evidencia» en «hay evidencia falsa», y esta vez sin nadie que lo note — es exactamente lo que
  `CLAUDE.md` prohibe cuando dice que la regla rige hacia adelante y no se aplica hacia atras.
- **Costo de no pagarla:** cinco bloques de verificacion del registro no son reproducibles. Quien los
  reejecute obtiene otra cosa y no sabra si se equivoco el registro o si cambio el repositorio — que
  es el defecto que `L-019` y `L-024` existen para evitar.
- **Como se paga:** anotando cada una de las cinco lineas con una **nota fechada** que diga que la
  orden publicada lleva un caracter corrompido y cual es su forma reejecutable, **sin tocar la linea
  original**. Es la recomendacion de fondo que dio el propio auditor en `F-042`.

📌 **Se registra como `Propuesta (pendiente del usuario)`** porque pagarla implica escribir sobre
entradas antiguas del registro, y el eje que decide —cuanto se toca lo ya auditado— es del usuario.
`manager` la evalua y la propone; no la confirma.

⚠️ **La clasifico como reversible a criterio**, porque anotar una nota fechada junto a una linea
existente se deshace con un commit y no destruye nada de lo ya escrito. Mientras no exista el
inventario de acciones irreversibles del proyecto (`T-037`), esta clasificacion se declara como
criterio y no como lectura de una tabla.

---

### DT-004 - Siete lineas nuevas de `S-019` repiten el defecto de `DT-003`, en `decisions.md` y `tasks.md`
| Campo | Valor |
|---|---|
| Estado | No implementada |
| Confirmacion | Propuesta (pendiente del usuario) |
| Importancia | Media |
| Urgencia | No bloqueante |
| Origen | manager (deteccion: cierre de sesion) |
| Fecha | 2026-09-03 |

- **Deuda:** el cierre de `S-019` encontro, al revisar `decisions.md` y `tasks.md` contra la
  evidencia, **siete lineas nuevas** de esta misma sesion —no las cinco que ya cubre `DT-003`— con el
  mismo caracter de retroceso `0x08` donde el texto pretendia escribir `\b` o backticks vacios. Cinco
  estan en `_persistence/decisions.md` (dentro y alrededor de `D-077`) y dos en
  `_persistence/tasks.md` (dentro de `T-068`). El defecto es identico al que `L-024`/`DT-003` ya
  documentaron, y ocurre **en el mismo commit que escribe `D-077`**, la decision que sustituye un
  patron escrito a mano precisamente para dejar de tener este tipo de punto ciego.

> 📌 **Nota del 2026-09-04 (`T-073`, hallazgo `F-049`, decision `D-081`).** La entrada se deja tal
> cual se escribio, y **su cifra y su ambito son cortos**: no son siete lineas nuevas en dos
> archivos, son **diez en cuatro**. La entrada las conto revisando a mano solo `decisions.md` y
> `tasks.md` —los dos archivos que el Paso 6 del cierre estaba mirando en ese momento—, en vez de
> barrer el arbol. Barrido sobre **todos** los `.md` del commit que la entrada describe:
>
> ```
> $ for f in $(git ls-tree -r --name-only 1b30e16 | grep -E '\.md$'); do n=$(git show 1b30e16:"$f" | grep -c $'\x08'); if [ "$n" -gt 0 ]; then echo "$f: $n"; fi; done
> _audit/S-018.md: 2
> _audit/S-019.md: 1
> _audit/findings.md: 1
> _persistence/decisions.md: 7
> _persistence/tasks.md: 5
> ```
>
> Y contra el commit padre, para separar lo nuevo de esta sesion de lo heredado:
>
> ```
> $ for f in _audit/S-018.md _audit/S-019.md _audit/findings.md _persistence/decisions.md _persistence/tasks.md; do echo "$f parent=$(git show 1b30e16^:$f | grep -c $'\x08') commit=$(git show 1b30e16:$f | grep -c $'\x08')"; done
> _audit/S-018.md parent=0 commit=2
> _audit/S-019.md parent=0 commit=1
> _audit/findings.md parent=1 commit=1
> _persistence/decisions.md parent=2 commit=7
> _persistence/tasks.md parent=3 commit=5
> ```
>
> **Nuevas de `S-019`: 2 + 1 + 0 + 5 + 2 = 10.** Las tres que la entrada no contaba son las dos de
> `_audit/S-018.md` y la de `_audit/S-019.md`, y las tres importan mas que las siete ya contadas:
>
> - Las **dos de `_audit/S-018.md`** caen dentro de la nota fechada que corrige `F-045`, y no son
>   prosa: son la transcripcion de la **salida cruda** de dos ordenes. La salida real lleva el
>   limite de palabra; la publicada lleva el caracter de control. Es decir, la nota que existia
>   para dejar de publicar cifras falsas publica una salida cruda que la orden no devuelve — la
>   misma clase de defecto que venia a corregir.
> - La **de `_audit/S-019.md`** es la linea 189, en prosa: «Restituyendo el `` que el `0x08`
>   reemplazo, si reproducen». El informe pierde el limite de palabra justo en la frase que explica
>   como restituirlo.
>
> **El ambito de esta deuda queda ampliado a esos diez casos en cuatro archivos**, no a los siete en
> dos que dice el enunciado. El titulo de la entrada no se reescribe (`D-019`): se lee con esta nota.
>
> ⚠️ **Y la leccion de la ampliacion no es la cifra: es como se conto.** Enumerar a mano los
> archivos que uno recuerda haber tocado no es un barrido, y produce exactamente este resultado —
> deja fuera los que se editaron al principio de la sesion. Por eso el remedio no es corregir el
> numero, sino que el cierre lo derive de una orden sobre los archivos que el commit toca (`T-074`).
- **Como se detecto:** revisando los cuatro archivos del porque contra la evidencia (Paso 6 del
  cierre), con el mismo patron que usa `DT-003`:

```
$ python -c "
import io
for f,ns in [('_persistence/decisions.md',[3914,4111,4141,4144,4147]),('_persistence/tasks.md',[3046,3064])]:
    lines=io.open(f,encoding='utf-8').readlines()
    for n in ns:
        l=lines[n-1]
        print(f,n,repr(l))
"
_persistence/decisions.md 3914 '> $ grep -rnoE "(^|[^A-Za-z])(${PAT})-[0-9]{2,3}\x08" _templates/020_baseline/ | wc -l\n'
_persistence/decisions.md 4111 '  mas corto para que un prefijo de una letra no tape a uno de dos, el `\x08` inicial se sustituye por\n'
_persistence/decisions.md 4141 '$ grep -rnoE "(^|[^A-Za-z])(${PAT})-[0-9]{2,3}\x08" _templates/020_baseline/ | wc -l\n'
_persistence/decisions.md 4144 '$ grep -rnoE "\x08(N|T|D|A|C|I|F|L|S|R|DT)-[0-9]{3}\x08" _templates/020_baseline/ | wc -l\n'
_persistence/decisions.md 4147 '$ grep -rnoE "\x08(FT|SC|VS|TC|ADR)-[0-9]{3}\x08" _templates/020_baseline/ | wc -l\n'
_persistence/tasks.md 3046 '  a mas corto, con `(^|[^A-Za-z])` en vez de `\x08` y `[0-9]{2,3}` en vez de `[0-9]{3}`. Nota fechada\n'
_persistence/tasks.md 3064 "$ PAT=$( ... ) && grep -rnoE \"(^|[^A-Za-z])(${PAT})-[0-9]{2,3}\x08\" _templates/020_baseline/ | wc -l\n"
```

- **Por que importa mas de lo habitual:** cuatro de los cinco casos de `decisions.md` (4141, 4144,
  4147, y el propio 3914) caen **dentro de bloques de verificacion de `D-077`** — la decision que se
  presenta como la correccion definitiva del punto ciego de patrones escritos a mano. Publicados tal
  cual, esos comandos **no reproducen**: quien los copie le pasa al interprete un caracter de control
  en vez de nada, y el patron que declaran probar deja de coincidir con el que esta escrito en el
  archivo (`(^|[^A-Za-z])(${PAT})-[0-9]{2,3}` sin el `0x08` final).
- **Verificado, no solo inferido: las tres lineas de `decisions.md` 4141, 4144 y 4147, copiadas y
  reejecutadas tal cual estan escritas, devuelven `0`, no las cifras que el texto de `D-077` afirma
  (`25`, `2`, `23`).**

```
$ sed -n '4144p' _persistence/decisions.md | sed 's/^\$ //' | cat -A | head -1
grep -rnoE "^H(N|T|D|A|C|I|F|L|S|R|DT)-[0-9]{3}^H" _templates/020_baseline/ | wc -l$

$ sed -n '4141p' _persistence/decisions.md | sed 's/^\$ //' | bash
0
$ sed -n '4144p' _persistence/decisions.md | sed 's/^\$ //' | bash
0
$ sed -n '4147p' _persistence/decisions.md | sed 's/^\$ //' | bash
0
```

  El `^H` de `cat -A` es el propio `0x08`. La linea 4141 depende ademas de una variable `$PAT` que
  solo existe dentro del bloque original (la orden 4141 sola, sin la 4139-4140 que la preceden,
  tampoco reproduce por eso — dos defectos distintos en la misma linea). Restituyendo el `\b` que el
  caracter de control reemplazo, **si** reproducen las cifras publicadas:

```
$ grep -rnoE "\b(N|T|D|A|C|I|F|L|S|R|DT)-[0-9]{3}\b" _templates/020_baseline/ | wc -l
2
$ grep -rnoE "\b(FT|SC|VS|TC|ADR)-[0-9]{3}\b" _templates/020_baseline/ | wc -l
23
```

  Confirma que el caracter corrompido no es un adorno tipografico: es la diferencia entre `2`/`23` y
  `0`/`0`. Sin restituirlo, quien reejecute el bloque de `D-077` concluye que el patron antiguo no
  encontraba nada, cuando encontraba exactamente lo que el texto dice.
- **No se corrige en este cierre:** el cierre de sesion **no escribe** `decisions.md`, y las
  entradas de `tasks.md` afectadas ya estaban redactadas por `manager` bajo la excepcion que permite
  citar un `F-NNN` de auditoria — no le corresponde al cierre reescribirlas sin evaluacion previa.
  Se deja para que `manager` decida, en la proxima sesion, si aplica el mismo remedio que `DT-003`
  —nota fechada sin tocar la linea original— o si, al no estar todavia commiteadas, corrige la linea
  directamente antes de cerrar (el argumento de `D-019` sobre «no reescribir» protege lo ya
  commiteado y auditado; esto no lo estaba todavia cuando se detecto).
- **Costo de no pagarla:** siete bloques de verificacion adicionales quedan no reproducibles,
  ademas de los cinco que ya arrastraba `DT-003` — y en el caso de `decisions.md` 4141/4144/4147,
  quedan **tres de las tres** ordenes de verificacion de `D-077` afectadas.
- **Como se paga:** igual que `DT-003` — nota fechada junto a cada linea, sin reescribir la original,
  o correccion directa si `manager` decide que al no estar commiteadas no aplica la prohibicion de
  reescritura retroactiva.

📌 **Se registra como `Propuesta (pendiente del usuario)`**, igual que `DT-003`: decidir cuanto se
toca un texto que otra sesion escribio es un eje que le corresponde al usuario, no al cierre.
