# Brief del cliente — Aplicación de análisis y generación de juegos Baloto / Revancha

> **Transcripción fiel** de `temporal/client_brief.txt`, sin omisiones ni interpretaciones.
> Lo único que se normalizó es la forma: jerarquía de títulos homogénea (el original mezclaba
> niveles), y el cuadro tabulado de la §27 convertido a tabla Markdown. El contenido, los ejemplos
> y la redacción del cliente se conservan literales.
>
> El texto final —desde «Cómo lo hago hoy»— viene sin numerar en el original; se recoge aquí como
> **Anexo**, sin cambiarle una palabra.

---

## Índice

| Sección | Contenido |
|---|---|
| [1. Propósito de la aplicación](#1-propósito-de-la-aplicación) | Qué construye y qué no |
| [2. Reglas del juego](#2-reglas-del-juego) | Días, balotas, superbalota |
| [3. Fuente de información](#3-fuente-de-información) | Carga inicial y actualizaciones |
| [4. Concepto de "día cero"](#4-concepto-de-día-cero) | Referencia de arranque |
| [5. Información inicial al ingresar](#5-información-inicial-al-ingresar) | Qué se muestra al entrar |
| [6. Generación de números](#6-generación-de-números) | Botón «Generar números» |
| [7. Información estadística de cada número](#7-información-estadística-de-cada-número) | Tabla por número |
| [8. Próxima aparición estimada](#8-próxima-aparición-estimada) | Base del cálculo |
| [9. Indicador estadístico](#9-indicador-estadístico) | Esperado / No esperado |
| [10. Registrar Juego](#10-registrar-juego) | Botón «Registrar Juego» |
| [11. Diferencia entre "Generar números" y "Registrar Juego"](#11-diferencia-entre-generar-números-y-registrar-juego) | Separación de conceptos |
| [12. Detección del sorteo realizado](#12-detección-del-sorteo-realizado) | Cuándo ya ocurrió |
| [13. Comparación del juego registrado](#13-comparación-del-juego-registrado) | Comparación independiente |
| [14. Resultado para Baloto](#14-resultado-para-baloto) | Qué se muestra |
| [15. Resultado para Revancha](#15-resultado-para-revancha) | Qué se muestra |
| [16. Nuevo ciclo](#16-nuevo-ciclo) | Preparación del siguiente sorteo |
| [17. Ciclo general de la aplicación](#17-ciclo-general-de-la-aplicación) | Flujo completo |
| [18. Historial de juegos del usuario](#18-historial-de-juegos-del-usuario) | Qué se guarda |
| [19. Principios del cálculo estadístico](#19-principios-del-cálculo-estadístico) | Alcance de los cálculos |
| [20. Alcance inicial del proyecto](#20-alcance-inicial-del-proyecto) | Primera versión |
| [21. Restricción de inteligencia artificial](#21-restricción-de-inteligencia-artificial) | Sin APIs de LLM |
| [22. Objetivo del proyecto de aprendizaje](#22-objetivo-del-proyecto-de-aprendizaje) | Metodología buscada |
| [23. Decisiones pendientes](#23-decisiones-pendientes) | Lo que no se asume todavía |
| [24. Plataforma de despliegue](#24-plataforma-de-despliegue) | Vercel |
| [25. Restricción de números consecutivos](#25-restricción-de-números-consecutivos) | Máximo dos consecutivos |
| [26. Prioridad entre Baloto y Revancha](#26-prioridad-entre-baloto-y-revancha) | Restricción de generación |
| [27. Historial de Juegos vs. Resultados](#27-historial-de-juegos-vs-resultados) | Dos historiales distintos |
| [Anexo — Cómo lo hago hoy](#anexo--cómo-lo-hago-hoy) | Proceso manual actual del usuario |

---

## 1. Propósito de la aplicación

Construir una aplicación sencilla basada en los juegos **Baloto y Revancha de Colombia**.

La aplicación permitirá:

- Consultar y almacenar el histórico de resultados.
- Generar combinaciones de números.
- Mostrar información estadística sobre los números generados.
- Registrar una combinación para el próximo sorteo.
- Comparar posteriormente el juego registrado con los resultados reales.
- Mostrar la cantidad de aciertos obtenidos en Baloto y Revancha.

La aplicación **no utilizará inteligencia artificial generativa** y no realizará llamadas a APIs de ChatGPT, Anthropic u otros modelos LLM.

La aplicación utilizará reglas determinísticas, generación aleatoria, almacenamiento de datos y cálculos estadísticos.

---

## 2. Reglas del juego

Baloto y Revancha se juegan los siguientes días:

- Lunes
- Miércoles
- Sábado

Cada combinación está compuesta por:

### Balotas

- 5 números.
- Los números están entre 1 y 43.
- Los 5 números no pueden repetirse dentro de la misma combinación.

### Superbalota

- 1 número adicional.
- Está entre 1 y 16.

Por lo tanto, una combinación tendrá la siguiente estructura:

`04 - 11 - 18 - 27 - 35 + 12`

Donde:

- `04, 11, 18, 27, 35` son las cinco balotas.
- `12` es la superbalota.

La misma combinación registrada por el usuario será utilizada tanto para **Baloto como para Revancha**.

---

## 3. Fuente de información

La aplicación deberá obtener directamente de la página oficial de Baloto el histórico de resultados de:

- Baloto
- Revancha

### Primera ejecución

La primera vez que se ejecute/utilice la aplicación deberá:

1. Acceder a la página de Baloto.
2. Leer el histórico de resultados disponible.
3. Obtener los resultados históricos de Baloto y Revancha.
4. Guardar toda la información obtenida en la base de datos de la aplicación.

El histórico deberá contener, como mínimo:

- Fecha del sorteo.
- Cinco balotas de Baloto.
- Superbalota de Baloto.
- Cinco balotas de Revancha.
- Superbalota de Revancha.
- Valor del premio/acumulado de Baloto.
- Valor del premio/acumulado de Revancha.

### Actualizaciones posteriores

Después de la primera carga, la aplicación no deberá volver a descargar innecesariamente todo el histórico.

Cada vez que necesite actualizar la información deberá:

1. Consultar nuevamente la página de Baloto.
2. Identificar cuál es la última fecha almacenada.
3. Comparar esa fecha con los resultados disponibles.
4. Identificar los sorteos que todavía no están almacenados.
5. Incorporar únicamente las fechas faltantes.

Por ejemplo:

Si el último sorteo almacenado es:

`17/08/2026`

y la fuente contiene posteriormente:

`19/08/2026`
`22/08/2026`

la aplicación solamente deberá incorporar esos nuevos sorteos.

---

## 4. Concepto de "día cero"

Para definir el funcionamiento inicial se asumirá como referencia un **lunes cualquiera**.

Durante ese lunes, y en cualquier caso antes del sorteo de esa noche, el usuario ingresa a la aplicación.

La aplicación deberá mostrar la información correspondiente al último sorteo disponible y preparar al usuario para el próximo sorteo.

---

## 5. Información inicial al ingresar

Al ingresar a la aplicación, deberá mostrarse:

### Último sorteo

#### Baloto

- Combinación ganadora.
- Fecha del sorteo.
- Próximo valor del premio/acumulado.

#### Revancha

- Combinación ganadora.
- Fecha del sorteo.
- Próximo valor del premio/acumulado.

La aplicación también deberá mostrar una combinación generada para el próximo juego.

---

## 6. Generación de números

La aplicación tendrá un botón:

**Generar números**

Cada vez que el usuario haga clic en este botón, la aplicación deberá generar una nueva combinación válida.

Cada combinación deberá contener:

- 5 números diferentes entre 1 y 43.
- 1 superbalota entre 1 y 16.

Ejemplo:

`04 - 11 - 18 - 27 - 35 + 12`

Cada clic en **Generar números** deberá reemplazar la combinación actualmente mostrada por una nueva combinación.

El usuario podrá generar tantas combinaciones como quiera.

La generación de números será aleatoria y deberá cumplir siempre las reglas del juego.

---

## 7. Información estadística de cada número

Cada vez que se genere una combinación, la aplicación deberá mostrar información estadística asociada a los números generados.

La información deberá presentarse en una tabla.

Para cada número se deberá mostrar:

- Número.
- Última vez que salió.
- Próxima aparición estimada.
- Indicador de si estadísticamente se encuentra en una ventana esperada para el próximo sorteo.

Ejemplo conceptual:

| Número | Última vez que salió | Próxima aparición estimada | Estado |
|---|---|---|---|
| 04 | 10/08/2026 | 24/08/2026 | 🟢 Esperado |
| 11 | 12/08/2026 | 26/08/2026 | ⚪ No esperado |
| 18 | 03/08/2026 | 19/08/2026 | 🟢 Esperado |
| 27 | 14/08/2026 | 28/08/2026 | ⚪ No esperado |
| 35 | 07/08/2026 | 21/08/2026 | 🟢 Esperado |
| 41 | 17/08/2026 | 31/08/2026 | ⚪ No esperado |

La aplicación deberá distinguir estadísticamente entre:

### Balotas

Números del 1 al 43.

### Superbalota

Números del 1 al 16.

No se deberán mezclar los históricos de balotas con los históricos de superbalotas, aunque tengan el mismo valor numérico.

---

## 8. Próxima aparición estimada

La columna **Próxima aparición estimada** no representa una predicción mediante inteligencia artificial.

Será un cálculo estadístico basado exclusivamente en el histórico de resultados almacenado.

El cálculo deberá considerar, como mínimo:

- Frecuencia histórica de aparición del número.
- Última fecha en que apareció.
- Cantidad de sorteos transcurridos desde su última aparición.
- Intervalo histórico promedio entre apariciones.

La metodología exacta para calcular la fecha estimada deberá definirse durante la etapa de diseño técnico.

---

## 9. Indicador estadístico

La aplicación deberá mostrar una señal que permita identificar si, según el cálculo estadístico utilizado, el número se encuentra en una ventana en la que **estadísticamente se esperaría su aparición próxima**.

Este indicador será exclusivamente descriptivo y estadístico.

No deberá presentarse como:

- Predicción.
- Garantía.
- Recomendación de apuesta.
- Probabilidad superior garantizada.
- Predicción mediante inteligencia artificial.

El objetivo es mostrar una comparación entre el comportamiento histórico del número y su intervalo actual.

Conceptualmente:

- **🟢 Esperado:** el número ha alcanzado o está próximo a alcanzar su intervalo histórico promedio.
- **⚪ No esperado:** el número todavía se encuentra por debajo de su intervalo histórico promedio.

La metodología exacta y los umbrales para determinar estos estados deberán definirse posteriormente.

---

## 10. Registrar Juego

La aplicación tendrá un segundo botón:

**Registrar Juego**

Cuando el usuario encuentre una combinación que desea utilizar y haga clic en **Registrar Juego**:

1. La aplicación deberá guardar la combinación.
2. Deberá mostrar claramente cuál es el juego registrado.
3. La combinación deberá quedar asociada al próximo sorteo.
4. La misma combinación será utilizada para Baloto y Revancha.
5. La combinación registrada deberá permanecer almacenada para poder compararla posteriormente con los resultados reales.

Ejemplo:

**Juego registrado**

`04 - 11 - 18 - 27 - 35 + 12`

Este juego será utilizado tanto para:

**Baloto:** `04 - 11 - 18 - 27 - 35 + 12`

como para:

**Revancha:** `04 - 11 - 18 - 27 - 35 + 12`

---

## 11. Diferencia entre "Generar números" y "Registrar Juego"

Estos dos conceptos deberán permanecer claramente separados.

### Generar números

Significa:

> "Quiero obtener otra combinación para analizar."

No registra ningún juego.

### Registrar Juego

Significa:

> "Esta es la combinación que quiero utilizar en el próximo sorteo."

La combinación pasa a formar parte del historial de juegos registrados del usuario.

---

## 12. Detección del sorteo realizado

Después de registrar un juego, la aplicación deberá detectar cuándo ya ocurrió el sorteo al cual estaba asociado.

Por ejemplo:

### Lunes

El usuario registra:

`04 - 11 - 18 - 27 - 35 + 12`

La combinación queda asociada al sorteo del lunes.

### Martes

Cuando el usuario vuelva a ingresar a la aplicación, esta deberá detectar que:

- Ya ocurrió el sorteo.
- Existe un juego registrado asociado a ese sorteo.
- Ya es posible comparar el juego con los resultados reales.

La aplicación deberá utilizar los resultados almacenados/actualizados desde la fuente de Baloto.

---

## 13. Comparación del juego registrado

Una vez detectado que ya ocurrió el sorteo, la aplicación deberá comparar automáticamente la combinación registrada con los resultados reales.

La comparación deberá realizarse de manera independiente para:

- Baloto.
- Revancha.

---

## 14. Resultado para Baloto

La aplicación deberá mostrar:

- Combinación registrada.
- Combinación ganadora de Baloto.
- Cantidad de aciertos.
- Cuáles fueron los números acertados.
- Fecha del sorteo.
- Valor del premio/acumulado de Baloto.

Ejemplo conceptual:

**Baloto**

Juego registrado:

`04 - 11 - 18 - 27 - 35 + 12`

Resultado:

`04 - 09 - 18 - 22 - 35 + 07`

**Aciertos: 3**

Números acertados:

`04 - 18 - 35`

---

## 15. Resultado para Revancha

La aplicación deberá realizar el mismo proceso para Revancha.

Deberá mostrar:

- Combinación registrada.
- Combinación ganadora de Revancha.
- Cantidad de aciertos.
- Cuáles fueron los números acertados.
- Fecha del sorteo.
- Valor del premio/acumulado de Revancha.

Ejemplo conceptual:

**Revancha**

Juego registrado:

`04 - 11 - 18 - 27 - 35 + 12`

Resultado:

`04 - 08 - 18 - 24 - 31 + 05`

**Aciertos: 2**

Números acertados:

`04 - 18`

---

## 16. Nuevo ciclo

Después de mostrar el resultado del sorteo anterior, la aplicación deberá quedar preparada para el siguiente sorteo.

El usuario podrá nuevamente:

1. Consultar la información del último sorteo.
2. Ver el próximo valor del premio/acumulado.
3. Generar números.
4. Analizar estadísticamente los números generados.
5. Generar nuevas combinaciones tantas veces como quiera.
6. Registrar una nueva combinación.
7. Asociarla al próximo sorteo.

De esta manera se inicia nuevamente el ciclo.

---

## 17. Ciclo general de la aplicación

El funcionamiento general será:

**Actualizar histórico**

↓

**Mostrar último sorteo**

↓

**Mostrar premios/acumulados**

↓

**Generar combinación**

↓

**Mostrar estadísticas de los números**

↓

**Generar números nuevamente si el usuario lo desea**

↓

**Registrar Juego**

↓

**Guardar combinación**

↓

**Asociar combinación al próximo sorteo**

↓

**Esperar a que ocurra el sorteo**

↓

**Detectar nuevo resultado**

↓

**Actualizar histórico**

↓

**Comparar juego registrado con Baloto**

↓

**Comparar juego registrado con Revancha**

↓

**Mostrar aciertos**

↓

**Mostrar números ganadores**

↓

**Mostrar premios/acumulados**

↓

**Preparar nuevo juego**

↓

**Comenzar nuevamente el ciclo**

---

## 18. Historial de juegos del usuario

La aplicación deberá guardar los juegos registrados para poder conservar la información de cada participación.

Cada juego registrado deberá estar asociado como mínimo con:

- Fecha en que fue registrado.
- Fecha del sorteo al que corresponde.
- Cinco balotas.
- Superbalota.
- Resultado de Baloto.
- Resultado de Revancha.
- Cantidad de aciertos en Baloto.
- Cantidad de aciertos en Revancha.
- Números acertados en Baloto.
- Números acertados en Revancha.

La implementación de una pantalla específica para consultar este historial podrá definirse posteriormente.

---

## 19. Principios del cálculo estadístico

La aplicación utilizará exclusivamente información histórica para realizar sus cálculos.

No utilizará inteligencia artificial generativa.

Los cálculos podrán incluir:

- Frecuencia de aparición.
- Última aparición.
- Cantidad de sorteos desde la última aparición.
- Intervalo promedio entre apariciones.
- Estimación estadística de próxima aparición.
- Indicador de cercanía al intervalo histórico promedio.

Es importante que la aplicación comunique claramente que estos cálculos **no predicen el resultado de un sorteo**.

Los sorteos son eventos independientes y el comportamiento histórico de un número no garantiza que vaya a aparecer en el siguiente sorteo.

---

## 20. Alcance inicial del proyecto

El objetivo es construir una aplicación **lo más sencilla posible**, manteniendo únicamente las funcionalidades necesarias para cumplir con el flujo definido.

La primera versión deberá concentrarse en:

- Obtener el histórico de Baloto y Revancha.
- Almacenar el histórico.
- Actualizar únicamente las fechas faltantes.
- Generar combinaciones válidas.
- Mostrar estadísticas de los números.
- Mostrar el indicador estadístico.
- Registrar una combinación.
- Asociarla al próximo sorteo.
- Detectar que el sorteo ya ocurrió.
- Comparar la combinación registrada con los resultados.
- Mostrar los aciertos.
- Mostrar los resultados reales.
- Mostrar los premios/acumulados.
- Reiniciar el ciclo para el siguiente sorteo.

No se deberán agregar funcionalidades adicionales que no sean necesarias para este flujo sin definirlas previamente.

---

## 21. Restricción de inteligencia artificial

La aplicación no deberá realizar llamadas a:

- OpenAI / ChatGPT.
- Anthropic / Claude.
- Google Gemini.
- Otros modelos de lenguaje generativo.

La aplicación podrá ser **desarrollada con asistencia de herramientas de inteligencia artificial**, pero el producto final no dependerá de una API de inteligencia artificial para funcionar.

La lógica de generación de números, análisis estadístico, comparación de resultados y demás reglas deberá ejecutarse mediante código convencional y algoritmos determinísticos/aleatorios según corresponda.

---

## 22. Objetivo del proyecto de aprendizaje

Además de ser una aplicación funcional, este proyecto servirá como ejercicio para aprender a desarrollar software utilizando inteligencia artificial como asistente durante el proceso de desarrollo.

La metodología buscada es:

**Idea**

↓

**Definición del producto**

↓

**Especificación**

↓

**Diseño**

↓

**Desarrollo asistido por IA**

↓

**Pruebas**

↓

**Iteración**

La IA será utilizada como herramienta para ayudar a construir el software, pero **no será parte del producto como motor de inteligencia artificial**.

---

## 23. Decisiones pendientes

Las siguientes decisiones deberán definirse posteriormente y no deben asumirse todavía:

1. Tecnología utilizada para construir la aplicación.
2. Tipo de base de datos.
3. Método exacto para obtener los datos de la página de Baloto.
4. Frecuencia con la que se actualizará el histórico.
5. Estructura definitiva de los datos almacenados.
6. Fórmula exacta para calcular el intervalo promedio.
7. Fórmula exacta para calcular la próxima aparición estimada.
8. Regla exacta para determinar cuándo un número se considera "estadísticamente esperado".
9. Diseño visual definitivo.
10. Número y estructura definitiva de las pantallas.
11. Manejo de errores cuando la página de Baloto no esté disponible.
12. Manejo de resultados que todavía no hayan sido publicados.
13. Comportamiento cuando el usuario no ingrese a la aplicación inmediatamente después de un sorteo.

Estas decisiones se definirán en una etapa posterior, después de validar completamente el comportamiento funcional de la aplicación.

---

## 24. Plataforma de despliegue

La aplicación deberá estar diseñada para ser desplegada en Vercel.

Esto implica que, durante la etapa de diseño técnico, se deberán considerar las capacidades y restricciones de Vercel para:

- Frontend de la aplicación.
- Backend/API, si fuera necesario.
- Ejecución de procesos de actualización del histórico.
- Almacenamiento persistente de los resultados.
- Variables de entorno y configuración.
- Tareas programadas, si se decide automatizar la actualización de resultados.
- Conexión con la fuente externa de datos de Baloto.

La arquitectura deberá mantenerse lo más sencilla posible, evitando incorporar infraestructura adicional que no sea necesaria para el funcionamiento del MVP.

---

## 25. Restricción de números consecutivos

Al generar una nueva combinación, la aplicación deberá impedir que existan más de dos números consecutivos dentro de las cinco balotas principales.

Por ejemplo, esta combinación no es válida:

`02 - 20 - 21 - 22 - 33 + 07`

porque contiene tres números consecutivos:

`20 - 21 - 22`

La aplicación deberá descartarla y generar otra combinación.

En cambio, una combinación como:

`02 - 20 - 21 - 33 - 43 + 07`

sí sería válida porque solamente existen dos números consecutivos:

`20 - 21`

Esta regla aplica únicamente a las cinco balotas principales (1–43). La superbalota se considera independientemente.

---

## 26. Prioridad entre Baloto y Revancha

Aunque la aplicación mostrará una única combinación de seis números, el usuario podrá definir cuál de los dos juegos tendrá prioridad para la generación.

Se deberán contemplar dos opciones:

- Prioridad Baloto
- Prioridad Revancha

La prioridad por defecto será:

**Baloto**

### Cuando la prioridad sea Baloto

Al generar una combinación, ninguno de los números generados deberá coincidir con los números que aparecieron en el último sorteo de Baloto.

Esto deberá aplicarse tanto a las cinco balotas como a la superbalota, respetando sus respectivos universos.

### Cuando la prioridad sea Revancha

Al generar una combinación, ninguno de los números generados deberá coincidir con los números que aparecieron en el último sorteo de Revancha.

La lógica será equivalente a la utilizada para Baloto.

### Importante

La prioridad no significa que la combinación solamente pueda jugarse en ese juego.

La combinación generada continúa siendo la misma para:

- Baloto
- Revancha

La prioridad únicamente determina qué resultado histórico se utiliza como restricción para generar la nueva combinación.

---

## 27. Historial de Juegos vs. Resultados

La aplicación deberá conservar un historial de las combinaciones registradas y sus resultados.

El historial deberá estar organizado por:

**Fecha del sorteo + tipo de juego**

Por lo tanto, cada registro deberá identificar claramente si corresponde a:

- Baloto
- Revancha

Por ejemplo:

| Fecha | Juego | Jugado | Resultado | Aciertos |
|---|---|---|---|---|
| 24/08/2026 | Baloto | 04-11-18-27-35 + 12 | 04-09-18-22-35 + 07 | 3 |
| 24/08/2026 | Revancha | 04-11-18-27-35 + 12 | 04-08-18-24-31 + 05 | 2 |

Esto significa que una misma combinación registrada genera dos registros de resultado, uno para Baloto y otro para Revancha.

Cada registro deberá conservar como mínimo:

- Fecha del sorteo.
- Tipo de juego.
- Combinación jugada.
- Combinación ganadora.
- Cantidad de aciertos.
- Números acertados.
- Superbalota jugada.
- Superbalota ganadora.
- Si la superbalota coincidió.
- Valor del premio/acumulado correspondiente al sorteo.

### Una precisión que considero importante

Con esta nueva regla, el historial de resultados y el historial de juegos del usuario son conceptualmente dos cosas diferentes:

**Historial de resultados**

Todos los sorteos de Baloto y Revancha que la aplicación obtiene de la fuente oficial.

**Historial Jugados vs. Resultados**

Las combinaciones que el usuario realmente registró y cómo se comportaron frente a cada sorteo.

Esto nos permitirá mantener una separación limpia entre:

**Datos externos**

Sorteos oficiales

y

**Datos del usuario**

Juegos registrados → Resultados → Aciertos

---

## Anexo — Cómo lo hago hoy

> Este apartado viene sin numerar en el archivo original. Se transcribe literal.

hoy lo hago de la siguiente forma:

1. Ingreso a la pagina web baloto.com. En esa pagina observo si el premio mayor cayó tanto para baloto como para revancha, para eso si baloto esta en 4000 MM COP o revancha esta en 2000 MM COP significa que el premio cayó.
2. Después ingreso a la pagina de resultados https://www.baloto.com/resultados, y comparó el ultimo resultado contra mi apuesta realizada, lo hago mirando los números que acertaron entre el jugado y el resultado obtenido.
3. Después el siguiente paso es determinar cuales son los 6 números que quiero volver a jugar. Teniendo en cuenta que 5 son balotas que van del 1 al 43 y no se repiten, y el sexto numero es la superbalota que va del 1 al 16. En este punto es donde mas me demoro, porque aunque son números aleatorios busco algunas cosas, como por ejemplo: que ningún numero se repita, es decir si un numero cayó en el ultimo sorteo de baloto o de revancha y lo tengo en la nueva combinación, lo excluyo y busco otro. TAmbien busco cosas como no incluir tres números consecutivos, por ejemplo 3, 4, 5, 22, 34, 16, aunque sueñe con ese numero lo excluyo porque se tiene tres números consecutivos, permito hasta dos. A veces me paso horas haciendo análisis que no conducen a nada como por ejemplo buscar combinacioens que sumen cierto numero o combinaciones como dos pares y tres impares o tres pares y dos impares. A veces me recorro el listado de resultados y determinos cuales son los números calientes ( es decir los que mas han caído en los últimos 15 sorteos) o busco los números fríos (aquellos que no han caído e los últimos 10 sorteos).
4. Esa búsqueda hace que pase mucho tiempo frente el computador y realmente siento que termino escogiéndo los mismos números siempre y dejando por fuera algunos otros, cuando esto debería azar puro.

La operación de revisar y seleccionar los números la realizo los mismos días del juego, es decir los lunes, miércoles y sábados por la mañana ya que el sorteo es por la noche, a veces también lo puedo hacer al dia siguiente del sorteo, ósea el martes, jueves o domingo, para saber si acerté.
