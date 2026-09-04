# tasks.md

> Registro de las tareas **realizadas** y de las tareas **por realizar**.
> Cada tarea tiene codigo `T-XXX`, estado, importancia y urgencia.

---

## Indice

| Codigo | Tarea | Estado | Importancia | Urgencia | Etapa |
|---|---|---|---|---|---|
| [T-001](#t-001---definir-alcance-y-objetivo-del-proyecto) | Definir alcance y objetivo del proyecto | No implementada | Alta | Bloqueante | `005_discovery` |
| [T-002](#t-002---declarar-las-etapas-posteriores-a-000_preproject) | Declarar las etapas posteriores a `000_preproject` | No implementada | Media | No bloqueante | `005_discovery` |
| [T-003](#t-003---verificar-si-el-historico-de-la-fuente-oficial-es-obtenible-a-003) | Verificar si el historico de la fuente oficial es obtenible (`A-003`) | No implementada | Alta | Bloqueante | `000_preproject` |
| [T-004](#t-004---acotar-el-enunciado-del-bloque-de-verificacion-de-d-016-f-001) | Acotar el enunciado del bloque de verificacion de `D-016` (`F-001`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-005](#t-005---corregir-los-dos-identificadores-auditor-vivos-f-002) | Corregir los dos identificadores `auditor` vivos (`F-002`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-006](#t-006---devolver-dt-001-a-propuesta-pendiente-del-usuario-f-003) | Devolver `DT-001` a `Propuesta (pendiente del usuario)` (`F-003`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-007](#t-007---corregir-la-tabla-de-actores-de-session-closermd-f-004) | Corregir la tabla de actores de `session-closer.md` (`F-004`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-008](#t-008---escribir-en-la-convencion-de-tasksmd-la-excepcion-que-fija-d-020-f-007) | Escribir en la convencion de `tasks.md` la excepcion que fija `D-020` (`F-007`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-009](#t-009---acotar-la-observacion-de-a-001-y-rehacer-su-criterio-de-refutacion-f-005) | Acotar la observacion de `A-001` y rehacer su criterio de refutacion (`F-005`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-010](#t-010---acotar-los-recuentos-de-la-nota-de-d-016-f-006) | Acotar los recuentos de la nota de `D-016` (`F-006`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-011](#t-011---acotar-el-bloque-de-verificacion-de-d-021-f-008) | Acotar el bloque de verificacion de `D-021` (`F-008`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-012](#t-012---escribir-en-dt-001-el-criterio-de-cierre-realmente-aplicado-f-009) | Escribir en `DT-001` el criterio de cierre realmente aplicado (`F-009`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-013](#t-013---acotar-el-alcance-historico-de-d-021-f-010) | Acotar el alcance historico de `D-021` (`F-010`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-014](#t-014---anclar-los-dos-recuentos-sobre-head-de-a-001-y-t-012-f-011) | Anclar los dos recuentos sobre `HEAD` de `A-001` y `T-012` (`F-011`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-015](#t-015---propagar-la-segunda-excepcion-de-d-025-a-los-tres-sitios-de-la-regla-f-012) | Propagar la segunda excepcion de `D-025` a los tres sitios de la regla (`F-012`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-016](#t-016---anotar-en-d-023-que-d-026-ya-amplio-el-ambito-del-paso-1b-f-013) | Anotar en `D-023` que `D-026` ya amplio el ambito del Paso 1b (`F-013`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-017](#t-017---corregir-el-recuento-de-hallazgos-de-progressmd-f-014) | Corregir el recuento de hallazgos de `progress.md` (`F-014`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-018](#t-018---corregir-la-convencion-viva-de-auditfindingsmd-f-010) | Corregir la convencion viva de `_audit/findings.md` (`F-010`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-019](#t-019---dar-mecanismo-a-d-022-en-el-paso-6-de-protocol-close) | Dar mecanismo a `D-022` en el Paso 6 de `protocol-close` | Implementada | Media | No bloqueante | `000_preproject` |
| [T-020](#t-020---escribir-el-archivo-de-etapa-_phases005_discoverymd-f-015) | Escribir el archivo de etapa `_phases/005_discovery.md` (`F-015`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-021](#t-021---reescribir-la-apertura-de-la-convencion-de-tasksmd-f-016) | Reescribir la apertura de la convencion de `tasks.md` (`F-016`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-022](#t-022---escribir-las-plantillas-de-_templates005_discovery) | Escribir las plantillas de `_templates/005_discovery/` | Implementada | Media | No bloqueante | `000_preproject` |
| [T-023](#t-023---registrar-el-bloque-de-verificacion-de-t-020-f-017) | Registrar el bloque de verificacion de `T-020` (`F-017`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-024](#t-024---registrar-el-barrido-de-variantes-de-t-021-con-su-patron-y-su-ambito-f-018) | Registrar el barrido de variantes de `T-021` con su patron y su ambito (`F-018`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-025](#t-025---endurecer-en-protocol-close-la-lista-de-la-seccion-1-del-informe-f-019) | Endurecer en `protocol-close` la lista de la seccion 1 del informe (`F-019`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-026](#t-026---extender-el-paso-1b-de-protocol-close-a-_templates) | Extender el Paso 1b de `protocol-close` a `_templates/` | Implementada | Media | No bloqueante | `000_preproject` |
| [T-027](#t-027---borrar-la-viñeta-residual-de-f-017-en-findingsmd-f-020) | Borrar la viñeta residual de `F-017` en `findings.md` (`F-020`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-028](#t-028---corregir-en-progressmd-el-commit-que-se-atribuye-a-r-007-f-021) | Corregir en `progress.md` el commit que se atribuye a `R-007` (`F-021`) | Cancelada | Baja | No bloqueante | `000_preproject` |
| [T-029](#t-029---anotar-los-tres-bloques-de-verificacion-de-decisionsmd-que-no-se-reproducen-f-022) | Anotar los tres bloques de verificacion de `decisions.md` que no se reproducen (`F-022`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-030](#t-030---registrar-en-decisionsmd-la-desviacion-de-t-026-f-023) | Registrar en `decisions.md` la desviacion de `T-026` (`F-023`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-031](#t-031---mover-a-005_discovery-la-ruta-de-los-artefactos-del-descubrimiento-d-045) | Mover a `005_discovery/` la ruta de los artefactos del descubrimiento (`D-045`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-032](#t-032---dejar-constancia-de-que-f-021-se-resolvio-por-desaparicion-no-por-correccion-f-024) | Dejar constancia de que `F-021` se resolvio por desaparicion, no por correccion (`F-024`) | Implementada | Alta | No bloqueante | `000_preproject` |
| [T-033](#t-033---anotar-los-bloques-de-verificacion-de-d-043-y-d-044-que-no-se-reproducen-f-025) | Anotar los bloques de verificacion de `D-043` y `D-044` que no se reproducen (`F-025`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-034](#t-034---corregir-la-cita-cruzada-l-013-de-dt-002-f-026) | Corregir la cita cruzada `L-013` de `DT-002` (`F-026`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-035](#t-035---anclar-el-bloque-de-verificacion-de-t-032-que-no-se-reproduce-sobre-su-commit-f-027) | Anclar el bloque de verificacion de `T-032`, que no se reproduce sobre su commit (`F-027`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-036](#t-036---completar-en-s-010-la-viñeta-de-decisionsmd-que-omite-dos-ediciones-f-028) | Completar en `S-010` la viñeta de `decisions.md`, que omite dos ediciones (`F-028`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-037](#t-037---escribir-el-inventario-de-acciones-irreversibles-del-proyecto-lg-38) | Escribir el inventario de acciones irreversibles del proyecto (`LG-38`) | No implementada | Alta | No bloqueante | `000_preproject` |
| [T-038](#t-038---igualar-el-barrido-de-fuga-de-protocol-audit-con-el-de-protocol-close) | Igualar el barrido de fuga de `protocol-audit` con el de `protocol-close` | No implementada | Media | No bloqueante | `000_preproject` |
| [T-039](#t-039---normalizar-a-no-implementada-el-estado-pendiente-de-t-037-y-t-038-f-029) | Normalizar a `No implementada` el estado `Pendiente` de `T-037` y `T-038` (`F-029`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-040](#t-040---dar-a-t-038-el-registro-que-la-respalda-f-030) | Dar a `T-038` el registro que la respalda (`F-030`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-041](#t-041---anotar-el-recuento-de-quince-lecciones-que-no-se-reproduce-en-sus-cuatro-sitios-f-031) | Anotar el recuento de «quince lecciones» que no se reproduce, en sus cuatro sitios (`F-031`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-042](#t-042---impedir-en-el-cierre-que-se-publique-un-bloque-de-verificacion-sin-ancla-f-031) | Impedir en el cierre que se publique un bloque de verificacion sin ancla (`F-031`) | Implementada | Alta | No bloqueante | `000_preproject` |
| [T-043](#t-043---adaptar-el-archivo-de-etapa-del-prototipo-a-esta-metodologia) | Adaptar el archivo de etapa del prototipo a esta metodologia | Implementada | Alta | No bloqueante | `000_preproject` |
| [T-044](#t-044---cerrar-los-enganches-de-la-etapa-del-prototipo-agnosticismo-carpeta-y-puntero-de-pi-5) | Cerrar los enganches de la etapa del prototipo: agnosticismo, carpeta y puntero de `PI-5` | Implementada | Alta | No bloqueante | `000_preproject` |
| [T-045](#t-045---anotar-el-recuento-del-bloque-de-t-041-que-su-commit-no-sostiene-f-032) | Anotar el recuento del bloque de `T-041`, que su commit no sostiene (`F-032`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-046](#t-046---exigir-en-el-paso-2d-la-lista-completa-de-ordenes-sin-ancla-f-032) | Exigir en el Paso 2d la lista completa de ordenes sin ancla (`F-032`) | Implementada | Alta | No bloqueante | `000_preproject` |
| [T-047](#t-047---acotar-la-frase-de-cierre-de-d-060-a-lo-que-su-orden-prueba-f-033) | Acotar la frase de cierre de `D-060` a lo que su orden prueba (`F-033`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-048](#t-048---escribir-las-plantillas-de-_templates010_prototype) | Escribir las plantillas de `_templates/010_prototype/` | Implementada | Alta | No bloqueante | `000_preproject` |
| [T-049](#t-049---publicar-la-lista-completa-del-paso-2d-que-s-013-afirmo-y-no-publico-f-034) | Publicar la lista completa del Paso 2d que `S-013` afirmo y no publico (`F-034`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-050](#t-050---dar-sitio-fijo-a-la-evidencia-del-paso-2d-en-el-informe-de-sesion-f-034) | Dar sitio fijo a la evidencia del Paso 2d en el informe de sesion (`F-034`) | Implementada | Alta | No bloqueante | `000_preproject` |
| [T-051](#t-051---escribir-el-reparto-de-trabajo-de-la-etapa-del-prototipo) | Escribir el reparto de trabajo de la etapa del prototipo | Implementada | Alta | No bloqueante | `000_preproject` |
| [T-052](#t-052---montar-el-gate-1-agente-gate1_auditor-y-skill-protocol-gate1) | Montar el Gate 1 (agente `gate1_auditor` y skill `protocol-gate1`) | Implementada | Alta | No bloqueante | `000_preproject` |
| [T-053](#t-053---corregir-la-procedencia-de-la-seccion-7-de-s-014-y-derivarla-del-diff-f-035) | Corregir la procedencia de la seccion 7 de `S-014` y derivarla del diff (`F-035`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-054](#t-054---reescribir-en-forma-generica-la-cita-instanciada-de-_workflow005_discoverymd-f-036) | Reescribir en forma generica la cita instanciada de `_workflow/005_discovery.md` (`F-036`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-055](#t-055---resolver-la-comprobacion-0-del-gate-1-por-orden-del-grafo-no-por-fecha-f-037) | Resolver la Comprobacion 0 del Gate 1 por orden del grafo, no por fecha (`F-037`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-056](#t-056---dar-a-la-comprobacion-0-forma-de-localizar-la-subcarpeta-del-prototipo-y-salida-si-no-existe-f-038) | Dar a la Comprobacion 0 forma de localizar la subcarpeta del prototipo y salida si no existe (`F-038`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-057](#t-057---escribir-el-reparto-y-las-plantillas-de-la-etapa-de-la-baseline) | Escribir el reparto y las plantillas de la etapa de la baseline | Implementada | Media | No bloqueante | `000_preproject` |
| [T-058](#t-058---escribir-el-archivo-de-etapa-de-la-baseline-_phases020_baselinemd) | Escribir el archivo de etapa de la baseline (`_phases/020_baseline.md`) | Implementada | Alta | No bloqueante | `000_preproject` |
| [T-059](#t-059---publicar-en-el-paso-2d-el-recuento-de-lineas-y-la-orden-que-reproduce-contra-el-commit-f-039) | Publicar en el Paso 2d el recuento de lineas y la orden que reproduce contra el commit (`F-039`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-060](#t-060---anotar-en-progressmd-la-afirmacion-absoluta-sobre-la-comprobacion-0-f-037) | Anotar en `progress.md` la afirmacion absoluta sobre la Comprobacion 0 (`F-037`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-061](#t-061---declarar-ft--y-sc--en-la-tabla-codigos-de-projectmd-f-040) | Declarar `FT-` y `SC-` en la tabla «Codigos» de `project.md` (`F-040`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-062](#t-062---acotar-el-alcance-del-control-de-codigos-instanciados-de-d-073-y-t-057-f-041) | Acotar el alcance del control de codigos instanciados de `D-073` y `T-057` (`F-041`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-063](#t-063---dar-deuda-registrada-a-las-cinco-lineas-con-x08-y-corregir-el-reparto-de-l-024-f-042) | Dar deuda registrada a las cinco lineas con `\x08` y corregir el reparto de `L-024` (`F-042`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-064](#t-064---corregir-en-l-024-el-recuento-de-lineas-presentado-como-apariciones-f-043) | Corregir en `L-024` el recuento de lineas presentado como apariciones (`F-043`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-065](#t-065---exigir-en-la-seccion-1-del-informe-las-entradas-existentes-que-el-commit-edita-f-044) | Exigir en la seccion 1 del informe las entradas existentes que el commit edita (`F-044`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-066](#t-066---publicar-el-recuento-real-de-la-seccion-7-de-s-018-y-numerar-la-lista-con-la-orden-f-045) | Publicar el recuento real de la seccion 7 de `S-018` y numerar la lista con la orden (`F-045`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-067](#t-067---corregir-la-atribucion-l-020l-019-en-s-018-y-derivar-del-diff-las-entradas-editadas-f-046) | Corregir la atribucion `L-020`/`L-019` en `S-018` y derivar del diff las entradas editadas (`F-046`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-068](#t-068---derivar-de-las-tablas-el-patron-del-control-de-codigos-instanciados-f-047) | Derivar de las tablas el patron del control de codigos instanciados (`F-047`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-069](#t-069---escribir-el-archivo-de-etapa-del-esqueleto-que-camina-_phases025_wsltmd) | Escribir el archivo de etapa del esqueleto que camina (`_phases/025_wslt.md`) | Implementada | Alta | No bloqueante | `000_preproject` |
| [T-070](#t-070---escribir-la-plantilla-del-acta-del-esqueleto-_templates025_wslt005_skeleton_recordmd) | Escribir la plantilla del acta del esqueleto (`_templates/025_wslt/005_skeleton_record.md`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-071](#t-071---escribir-el-reparto-de-la-etapa-del-esqueleto-_workflow025_wsltmd-d-080) | Escribir el reparto de la etapa del esqueleto (`_workflow/025_wslt.md`, `D-080`) | Implementada | Alta | No bloqueante | `000_preproject` |
| [T-072](#t-072---publicar-en-s-019-la-lista-completa-del-paso-2d-y-las-cifras-reales-f-048) | Publicar en `S-019` la lista completa del Paso 2d y las cifras reales (`F-048`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-073](#t-073---ampliar-el-ambito-y-la-cifra-de-dt-004-con-su-barrido-f-049-d-081) | Ampliar el ambito y la cifra de `DT-004` con su barrido (`F-049`, `D-081`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-074](#t-074---anadir-al-cierre-el-barrido-de-caracteres-de-control-paso-2e-de-protocol-close-f-049) | Anadir al cierre el barrido de caracteres de control (Paso 2e de `protocol-close`, `F-049`) | Implementada | Alta | No bloqueante | `000_preproject` |
| [T-075](#t-075---aclarar-que-025_wslt-es-una-etapa-con-tres-archivos-no-tres-etapas-f-050) | Aclarar que `025_wslt` es una etapa con tres archivos, no tres etapas (`F-050`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-076](#t-076---escribir-el-archivo-de-etapa-del-crecimiento-_phases030_growthmd-d-082) | Escribir el archivo de etapa del crecimiento (`_phases/030_growth.md`, `D-082`) | Implementada | Alta | No bloqueante | `000_preproject` |
| [T-077](#t-077---separar-las-dos-cuentas-de-la-seccion-8-de-s-020-f-051) | Separar las dos cuentas de la seccion 8 de `S-020` (`F-051`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-078](#t-078---escribir-la-nota-de-cierre-de-la-seccion-1-de-s-020-f-052) | Escribir la nota de cierre de la seccion 1 de `S-020` (`F-052`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-079](#t-079---anclar-la-cabecera-de-s-020-al-hash-literal-f-053) | Anclar la cabecera de `S-020` al hash literal (`F-053`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-080](#t-080---corregir-en-progressmd-el-recuento-de-etapas-sin-adoptar-f-054) | Corregir en `progress.md` el recuento de etapas sin adoptar (`F-054`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-081](#t-081---dar-al-cierre-un-paso-de-anclaje-y-al-auditor-el-hash-literal-f-052-f-053) | Dar al cierre un paso de anclaje, y al auditor el hash literal (`F-052`, `F-053`) | Implementada | Alta | No bloqueante | `000_preproject` |
| [T-082](#t-082---que-el-cierre-derive-la-lista-de-etapas-sin-adoptar-f-054) | Que el cierre derive la lista de etapas sin adoptar (`F-054`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-083](#t-083---escribir-las-plantillas-de-_templates030_growth) | Escribir las plantillas de `_templates/030_growth/` | Implementada | Alta | No bloqueante | `000_preproject` |
| [T-084](#t-084---quitar-los-dos-codigos-instanciados-de-_phases030_growthmd-f-055) | Quitar los dos codigos instanciados de `_phases/030_growth.md` (`F-055`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-085](#t-085---dar-al-cierre-el-control-1c-de-codigos-instanciados-f-055) | Dar al cierre el control 1c de codigos instanciados (`F-055`) | Implementada | Alta | No bloqueante | `000_preproject` |
| [T-086](#t-086---corregir-por-nota-la-salida-cruda-de-la-nota-de-_phases030_growthmd-f-056) | Corregir por nota la salida cruda de la nota de `_phases/030_growth.md` (`F-056`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-087](#t-087---publicar-la-salida-del-criterio-de-cierre-de-d-083-y-d-084-f-057) | Publicar la salida del criterio de cierre de `D-083` y `D-084` (`F-057`) | Implementada | Media | No bloqueante | `000_preproject` |
| [T-088](#t-088---anotar-los-huecos-de-plantilla-de-s-021-y-darle-al-cierre-su-control-f-058) | Anotar los huecos de plantilla de `S-021` y darle al cierre su control (`F-058`) | Implementada | Baja | No bloqueante | `000_preproject` |
| [T-089](#t-089---fijar-la-forma-del-bloque-criterio-de-cierre-en-decisionsmd) | Fijar la forma del bloque «Criterio de cierre» en `decisions.md` | Implementada | Media | No bloqueante | `000_preproject` |
| [T-090](#t-090---que-la-fila-de-_auditindexmd-lleve-el-hash-literal-del-informe) | Que la fila de `_audit/index.md` lleve el hash literal del informe | Implementada | Media | No bloqueante | `000_preproject` |
| [T-091](#t-091---escribir-el-reparto-de-la-etapa-del-crecimiento) | Escribir el reparto de la etapa del crecimiento | Implementada | Alta | No bloqueante | `000_preproject` |
| [T-092](#t-092---completar-las-dos-columnas-que-le-faltaban-a-la-fila-de-l-029) | Completar las dos columnas que le faltaban a la fila de `L-029` | Implementada | Media | No bloqueante | `000_preproject` |

---

## Convenciones

| Campo | Valores posibles |
|---|---|
| Codigo | `T-XXX`, correlativo, no se reutiliza |
| Estado | `Implementada` / `No implementada` / `Cancelada` / `Suspendida` |
| Importancia | `Alta` / `Media` / `Baja` |
| Urgencia | `Bloqueante` / `No bloqueante` |
| Origen | `usuario` / `manager` / `report_auditor` |
| Etapa | una de las etapas declaradas en la tabla «Etapas» de `project.md` |

**`Origen` es obligatorio y su valor sale de esta lista.** Que significa cada uno:

| Valor | La tarea nace de… |
|---|---|
| `usuario` | una peticion o una decision del usuario |
| `manager` | iniciativa propia al ejecutar |
| `report_auditor` | un hallazgo `F-NNN` de una auditoria |

🚨 **Anadir un valor nuevo es una decision, no una improvisacion.** El criterio es uno solo:
**nombra un origen de demanda que ninguno de los ya existentes cubre**. Un matiz de un origen
existente —«usuario, pero por escrito», «report_auditor, pero de otra pasada»— no es un
valor nuevo: va en el cuerpo de la tarea. Si el criterio se cumple, el valor entra **en esta
tabla en la misma pasada** en que se escribe la primera tarea que lo usa, con su `D-XXX`.

Regla: una tarea con origen `report_auditor` solo pasa a ejecutarse despues de que `manager` evalue la
recomendacion y la considere correcta.

🚨 **Este archivo no se escribe a mano durante la jornada.** Lo produce el cierre de sesion, junto
con `progress.md`. **Tiene dos excepciones, y las dos estan escritas.** La primera: cuando `manager`
evalua un hallazgo `F-NNN` de una auditoria y lo acepta, escribe **en ese momento** la `T-XXX` con
`Origen: report_auditor`, sin esperar al cierre. Lo fija `D-020`, confirmada por el usuario el
2026-09-01.

🔑 **Por que esa primera excepcion existe.** La fila del hallazgo en `_audit/findings.md` tiene que
citar el codigo de su tarea para ser auditable, y una fila que cita una `T-XXX` inexistente no lo es.
Esperar al cierre dejaria el hallazgo evaluado y sin registro durante toda la jornada — el agujero
que el estado `Aceptado — pendiente` existe justamente para tapar.

**La segunda, escrita el 2026-09-01 (`D-025`):** `manager` tambien escribe aqui
cuando el cambio **nace de una decision ya registrada que el `session-closer` no puede deducir del
`git diff`** — reasignar la etapa de una tarea, o cambiar la estructura del archivo porque lo pidio
el usuario. El agente arranca en frio y solo ve archivos: una orden del usuario no deja rastro en el
diff, y esperar al cierre significa perderla.

⚠️ **Son dos excepciones, no una puerta.** Las dos exigen lo mismo: **un `D-XXX` o un `F-NNN` que
las respalde, citado en la propia tarea**. Sin esa cita, cualquier edicion a mano se vuelve
indistinguible de saltarse la regla — y entonces la regla deja de existir. Lo demas sigue siendo del
`session-closer`.

🚨 **El indice se escribe a mano, sin generador.** Cada fila enlaza por ancla a su tarea.

---

## Tareas

<!--
Plantilla:

### T-XXX - Titulo
| Campo | Valor |
|---|---|
| Estado | No implementada |
| Importancia | |
| Urgencia | |
| Etapa | |
| Origen | |
| Sesion | S-XXX |

- **Que:** que hay que hacer.
- **Por que:** que problema resuelve.
- **Criterio de cierre:** como se sabe que quedo hecha.
-->

### T-001 - Definir alcance y objetivo del proyecto
| Campo | Valor |
|---|---|
| Estado | No implementada |
| Importancia | Alta |
| Urgencia | Bloqueante |
| Etapa | `005_discovery` |
| Origen | manager |
| Sesion | S-001 |

- **Que:** definir el alcance y el objetivo del proyecto, contrastando `_brief/client_brief.md`
  punto por punto (ver `A-002`), y registrar la decision resultante con su `D-XXX`.
- **Por que:** `project.md` declara que hoy solo esta registrada la etapa `000_preproject`; las
  etapas posteriores y el producto mismo dependen de que exista esa definicion. Un encargo del
  cliente no es una decision del proyecto.
- **Criterio de cierre:** existe un `D-XXX` en `decisions.md` que fija alcance y objetivo, y
  `project.md` deja de decir que las etapas posteriores no estan registradas.

🕒 **Nota del 2026-09-01 (`S-005`): esta tarea cambia de etapa.** Nacio en `000_preproject`, pero
`D-023` dejo escrito que esa etapa **no define alcance ni objetivo** — monta el andamio y nada mas—.
Por decision del usuario (`D-024`, `D-025`) pasa a **`005_discovery`**. No cambia nada de su
contenido: cambia cuando se hace.

---

### T-002 - Declarar las etapas posteriores a `000_preproject`
| Campo | Valor |
|---|---|
| Estado | No implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `005_discovery` |
| Origen | manager |
| Sesion | S-001 |

- **Que:** decidir y registrar en `project.md` (tabla «Etapas») que etapas siguen a
  `000_preproject`, tomando como propuesta de partida —no como decision— la secuencia del brief
  (`_brief/client_brief.md`, §22).
- **Por que:** `project.md` dice explicitamente que esto no esta decidido y que un encargo no
  sustituye a una decision registrada.
- **Criterio de cierre:** la tabla «Etapas» de `project.md` lista mas de una etapa, con su `D-XXX`.

🕒 **Nota del 2026-09-01 (`S-005`): cambia de etapa, y su criterio de cierre se queda corto.** Pasa a
**`005_discovery`** por la misma razon que `T-001` (`D-023`, `D-024`, `D-025`). Ademas, `D-024` acaba
de declarar `005_discovery` en la tabla «Etapas», con lo que el criterio escrito arriba —«lista mas
de una etapa»— **ya se cumple literalmente sin que la tarea este hecha**. El criterio original **no
se reescribe**; leelo asi: lo que cierra esta tarea es **la secuencia completa** de etapas
posteriores, decidida y registrada, no haber nombrado la inmediata para que las tareas de alcance
tuvieran donde ir.

---

### T-003 - Verificar si el historico de la fuente oficial es obtenible (`A-003`)
| Campo | Valor |
|---|---|
| Estado | No implementada |
| Importancia | Alta |
| Urgencia | Bloqueante |
| Etapa | `000_preproject` |
| Origen | manager |
| Sesion | S-001 |

- **Que:** comprobar si el historico completo de resultados de la fuente oficial se puede obtener
  de forma repetible desde el entorno de despliegue (`C-002`, Vercel), tal como lo supone `A-003`.
- **Por que:** `A-003` señala que si este supuesto resulta falso, no cae una funcionalidad sino el
  ciclo entero del producto, porque las secciones 5 a 19 del brief dependen todas del historico.
- **Criterio de cierre:** `A-003` pasa a `Confirmado` (y se traslada a `decisions.md` o
  `constraints.md`) o a `Refutado`, segun lo que se encuentre.

---

### T-004 - Acotar el enunciado del bloque de verificacion de `D-016` (`F-001`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-003 |

- **Que:** el bloque de verificacion de `D-016` se titulaba «cero identificadores `auditor` vivos»
  sin acotar ambito, mientras su comando cubria solo `.claude`, `CLAUDE.md` y `project.md`. Se anade
  bajo el bloque —sin tocar el comando ya ejecutado— una nota fechada que declara el ambito real y
  registra el barrido con ambito completo, con su patron y su salida cruda.
- **Por que:** un enunciado mas ancho que su comando da por cerrado lo que nadie miro. En este caso
  concreto tapo una fuga real, que es `F-002`.
- **Criterio de cierre:** `D-016` lleva la nota de ambito con los dos barridos y sus salidas crudas.
  Verificado en el diff de esta sesion.

---

### T-005 - Corregir los dos identificadores `auditor` vivos (`F-002`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-003 |

- **Que:** `_audit/findings.md:3` —cabecera viva de un registro activo— y el ejemplo de
  `_persistence/tasks.md` que nombra el valor del campo `Origen` pasan de `auditor` a
  `report_auditor`. Los dos son identificadores del agente, no el sustantivo comun que `D-016`
  excluye, y ninguno es historico.
- **Por que:** son las dos unicas referencias vivas que el barrido acotado de `D-016` no alcanzo.
- **Criterio de cierre:** el barrido con ambito completo ya no las devuelve; lo que queda en
  `findings.md` es evidencia citada de `F-001` y `F-002`. Registrado en la nota de ambito de `D-016`.

---

### T-006 - Devolver `DT-001` a `Propuesta (pendiente del usuario)` (`F-003`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-003 |

- **Que:** `DT-001` se registro como `Confirmada` en el cierre de `S-002`, valor que el Paso 5 de
  `protocol-close` prohibe al `session-closer`. Vuelve a `Propuesta (pendiente del usuario)` en el
  indice y en el detalle, con nota fechada que explica el cambio.
- **Por que:** `Confirmacion` existe para distinguir lo confirmado de lo supuesto. Escrito por quien
  el protocolo se lo prohibe, el campo deja de significar nada. `manager` tampoco puede confirmarla:
  el dueno de la confirmacion va dentro del valor, y es el usuario.
- **Criterio de cierre:** las dos apariciones dicen `Propuesta (pendiente del usuario)`, y la
  confirmacion queda pedida al usuario. Verificado en el diff de esta sesion.

---

### T-007 - Corregir la tabla de actores de `session-closer.md` (`F-004`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-003 |

- **Que:** la fila de `report_auditor` en la tabla de actores decia «su propio repositorio», resto
  del esquema de dos terminales que `D-012` revoco. Pasa a nombrar lo que escribe de verdad:
  `_audit/R-XXX.md`, `_audit/findings.md` y `_audit/index.md`, en este mismo repositorio.
- **Por que:** contradecia a `project.md`, a `CLAUDE.md` y a las dos lineas siguientes de su propio
  archivo, en una tabla que el `session-closer` lee en cada cierre.
- **Criterio de cierre:** `git grep -n "su propio repositorio" -- .claude` ya no devuelve esa linea.
  Verificado en el diff de esta sesion.

---

### T-008 - Escribir en la convencion de `tasks.md` la excepcion que fija `D-020` (`F-007`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-004 |

- **Que:** la convencion de este archivo prohibia en absoluto escribirlo a mano durante la jornada,
  mientras `D-020` permitia a `manager` hacerlo al registrar un hallazgo aceptado. Se escribe la
  excepcion **dentro de la convencion**, acotada a ese unico caso y con su motivo, y se refleja
  tambien en `protocol-close` y en `session-closer.md` para que el cierre no duplique la tarea.
- **Por que:** quien abriera este archivo sin conocer `D-020` leia una prohibicion que ya no regia,
  con `T-004`..`T-007` incumpliendola a la vista. El defecto no era la lectura de `D-020` sino la
  contradiccion sin registro.
- **Criterio de cierre:** la convencion enuncia la excepcion y cita `D-020`; el usuario confirmo la
  lectura el 2026-09-01, y esa confirmacion quedo anotada en `D-020`. Verificado en el diff de esta
  sesion.

---

### T-009 - Acotar la observacion de `A-001` y rehacer su criterio de refutacion (`F-005`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-005 |

- **Que:** la observacion del 2026-09-01 bajo `A-001` registra `git grep -n "| Pendiente |" --
  _audit/index.md` con `exit=1` y concluye «cero sesiones cerradas sin auditar». Sobre el commit que
  contiene esa afirmacion el comando devuelve una linea. El bloque **no se reescribe** (`D-019`): se
  le anade debajo una nota fechada que declara su ambito real —recuento tomado antes de que el
  cierre escribiera la fila de su propia sesion— y que **rehace la señal 2** para que sea
  comprobable: una sesion cerrada sigue sin auditar cuando su fila continua en `Pendiente` **al
  abrirse la sesion siguiente**, no en el instante del cierre.
- **Por que:** tal como estaba escrita, la señal 2 no podia dispararse nunca. El `session-closer`
  anade la fila de su sesion con `Pendiente` **antes** de commitear, asi que el comando devuelve
  `exit=0` en todo commit de cierre y `exit=1` solo despues de la auditoria. Una señal de refutacion
  que no puede activarse deja `A-001` sin la unica de sus dos señales que no admite otra lectura.
- **Criterio de cierre:** bajo la observacion de `A-001` hay una nota fechada que (a) acota el
  bloque original a lo que probaba y (b) enuncia la señal 2 con su momento de comprobacion. El
  bloque original queda intacto.

---

### T-010 - Acotar los recuentos de la nota de `D-016` (`F-006`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-005 |

- **Que:** la nota del 2026-09-01 bajo el bloque de verificacion de `D-016` afirma que el barrido se
  hizo «ya escrito el registro de esta sesion» y registra `_persistence/progress.md:7` sin
  `_audit/S-003.md`. Sobre `ea0b850`, el commit que la contiene, son `progress.md:8` y
  `_audit/S-003.md:3`. Se anade una segunda nota fechada que declara el momento real del recuento.
- **Por que:** la correccion de `F-001` repite dentro de si misma el defecto que `F-001` describe
  —declarar mas ambito del que el comando tuvo—, y eso le resta valor a `L-006`. Las diferencias son
  lineas escritas despues del barrido y ninguna es una referencia viva: el fondo es correcto, lo que
  falla es la declaracion de alcance temporal.
- **Criterio de cierre:** la nota lleva su recuento sobre `ea0b850` con comando y salida cruda, y
  dice que el recuento anterior se tomo antes de cerrar el registro de la sesion. Los dos bloques
  anteriores quedan intactos.

---

### T-011 - Acotar el bloque de verificacion de `D-021` (`F-008`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-005 |

- **Que:** `D-021` afirma literalmente que su recuento «se tomo con el registro de esta sesion ya
  escrito, que es lo que hace que se reproduzca sobre el commit que lo contiene», y no se reproduce:
  sobre `c70b757` `progress.md` da **6** y no 2, falta la linea `_audit/S-004.md:17`, y de las 13 de
  `decisions.md` solo **9** caen dentro de la entrada (empieza en la linea 573). Se anade una nota
  fechada con el recuento real sobre `c70b757` y sobre `HEAD`.
- **Por que:** el defecto no es la cifra, es la frase. `D-021` es la primera entrada escrita despues
  de `L-006` y reincide, ademas **afirmando una reproducibilidad que no tiene**: un registro que se
  autodeclara reproducible y no lo es desalienta la comprobacion en vez de solo omitirla.
- **Criterio de cierre:** bajo el bloque de `D-021` hay una nota fechada que corrige la frase, da el
  recuento sobre `c70b757` con su comando y su salida cruda, y separa las 9 coincidencias internas
  de las 4 externas. El bloque original queda intacto.

---

### T-012 - Escribir en `DT-001` el criterio de cierre realmente aplicado (`F-009`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-005 |

- **Que:** el campo «Como se paga» de `DT-001` exige `git grep -n "debtec" -- .` en cero, criterio
  absoluto que la entrada no cumple —el comando devuelve 12 archivos en `HEAD`— mientras su estado
  ya es `Implementada`. Se anade a la nota fechada existente el criterio de cierre realmente
  aplicado, sin reescribir el «Como se paga» original.
- **Por que:** es el mismo defecto que `F-007`, cuya leccion `L-007` —«una excepcion se escribe
  donde esta la regla, no donde se decidio»— se escribio en el mismo commit. La informacion correcta
  esta en la entrada (la nota remite a `D-021`), pero quien aplique el criterio literal concluye que
  la deuda no esta pagada.
- **Criterio de cierre:** la nota de `DT-001` enuncia el criterio aplicado —cero en `.claude`,
  `CLAUDE.md` y `project.md`, historico intacto por `D-021`— con su comando y su salida cruda. El
  campo «Como se paga» original queda intacto.

🕒 **Nota anadida el 2026-09-02 (`S-006`), tras el hallazgo `F-011` de `R-005`.** La cifra «12
archivos en `HEAD`» del primer punto se escribio sin decir cual era ese `HEAD`. Era `e61454b`, y
sobre ese hash se reproduce:

```
$ git grep -c "debtec" e61454b -- . | wc -l
12
```

Sobre `510d580` —el commit que contiene esta ficha— son 13, y sobre `a800d6b` son 14: el recuento
crece con cada registro que cita el nombre antiguo, que es exactamente el motivo por el que `D-022`
obliga a anclarlo o fecharlo. **La cifra era correcta; lo que faltaba era el ancla.** El fondo de la
tarea no cambia.

---

### T-013 - Acotar el alcance historico de `D-021` (`F-010`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-005 |

- **Que:** `D-021` clasifico `_audit/` entero como historico, y por eso `_audit/findings.md:56`
  sigue mandando comprobar una entrada en `debtec.md`, archivo que ya no existe — dentro de una
  **convencion vigente**, no de una cita historica. Se anade a `D-021` una nota fechada que acota el
  criterio: `_audit/` es historico **salvo las convenciones de `findings.md` y de `index.md`**, que
  son registro vivo.
- **Por que:** el criterio se aplico por carpeta y no por naturaleza del texto. Los `S-XXX.md` y los
  `R-XXX.md` son documentos entregados y no deben reescribirse; `findings.md` e `index.md` son
  registros vivos cuyas convenciones se siguen aplicando en cada pasada.
- **Que queda fuera de esta tarea:** la correccion del texto de `_audit/findings.md:56`. Ese archivo
  no lo escribe `manager` mas alla de la fila de estado de cada hallazgo; la linea la corrige
  `report_auditor` en una pasada posterior. Lo que esta tarea entrega es el criterio que se lo
  permite.
- **Criterio de cierre:** `D-021` lleva la nota fechada con la excepcion enunciada y su motivo, y la
  fila de `F-010` en `_audit/findings.md` cita esta tarea y deja constancia de que la correccion del
  texto es del auditor.

---

### T-014 - Anclar los dos recuentos sobre `HEAD` de `A-001` y `T-012` (`F-011`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-006 |

- **Que:** la nota de `S-005` bajo `A-001` cerraba la senal 2 rehecha con un `git grep ... HEAD` sin
  decir cual era ese `HEAD`, y la ficha de `T-012` afirmaba «12 archivos en `HEAD`» igual. Se anaden
  dos notas fechadas que las anclan a `e61454b`, el `HEAD` real del momento, sin reescribir los
  bloques originales (`D-019`).
- **Por que:** es el patron de `F-005`, `F-006` y `F-008` reapareciendo **dentro de la correccion de
  `F-005`**, y contra `D-022`, escrita en ese mismo commit. Quien reprodujera el bloque de `A-001`
  sobre `510d580` obtenia `exit=0` y concluia que la senal 2 **si** se disparo — lo contrario de lo
  que la nota afirma, sobre una de las dos senales que pueden refutar `A-001`.
- **Lo que la verificacion demostro:** las dos cifras **eran correctas**; lo que faltaba era el
  ancla. Sobre `e61454b` el comando de `A-001` da `exit=1` y el recuento da 12, tal como se
  registraron. El fondo de las dos entradas no cambia.
- **Criterio de cierre:** las dos notas existen, cada una con su hash y su salida cruda, los bloques
  originales quedan intactos, y la nota de `A-001` anade la comprobacion de hoy sobre `a800d6b`.

---

### T-015 - Propagar la segunda excepcion de `D-025` a los tres sitios de la regla (`F-012`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-006 |

- **Que:** `D-025` generalizo a dos casos la excepcion de escritura de `manager` sobre `tasks.md`,
  pero solo lo escribio en la convencion de `tasks.md`. Los tres sitios que enuncian la regla para
  quien la ejecuta seguian diciendo «es la unica excepcion». Se reescriben los tres.
- **Por que:** es `F-007` otra vez, y `F-007` se cerro en `S-004` arreglando **esos mismos tres
  sitios**. `L-007` —«una excepcion se escribe donde esta la regla, no donde se decidio»— lleva
  escrita desde entonces. El `session-closer` arranca en frio y lee su skill, no `decisions.md`: con
  el texto viejo, una fila legitima editada a mano se le lee como infraccion.
- **Que se hizo, ademas de propagar:** los tres textos pasan a describir la excepcion **por su
  senal, no por su numero** — toda fila editada a mano lleva un `D-XXX` o un `F-NNN` citado en la
  propia tarea. Es el criterio que `R-005` propuso: contar filas invitaria a repartir un mismo
  cambio en dos sesiones para pasar por debajo del umbral. Y se le dice explicitamente al agente que
  **si la cita esta, no lo reporte como desfase**, que era el dano concreto del hallazgo.
- **Criterio de cierre:** el barrido de la regla no devuelve ningun enunciado que siga afirmando que
  la excepcion es unica, y el archivo de la etapa sigue pasando el control de agnosticidad.

🕒 **Nota anadida el 2026-09-02 (`S-007`), tras el hallazgo `F-016` de `R-006`.** El criterio de
arriba **se deja tal cual se escribio** (`D-019`), y hay que leerlo con esta precision: «ningun
enunciado» significaba **ningun enunciado vivo de esta regla**, no ninguna coincidencia del patron.
Tal como quedo redactado, el barrido no puede dar cero nunca: siempre devolvera la regla de los
supuestos `A-XXX` de `protocol-close`, que es otra, y la cita historica que esta tarea hace del texto
viejo cuatro lineas mas arriba. El criterio corregido —enumerando lo que si puede quedar— vive en
`T-021`, que es donde se atendio el hallazgo.

---

### T-016 - Anotar en `D-023` que `D-026` ya amplio el ambito del Paso 1b (`F-013`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-006 |

- **Que:** `D-023` cerraba con una advertencia —«esto todavia no entra en el ambito del Paso 1b...
  queda pendiente de acordarla con el usuario»— que `D-026`, en el mismo commit, ya habia
  desmentido. Se anade una nota fechada que remite a `D-026`, sin reescribir el original (`D-019`).
- **Por que:** una entrada `Vigente` afirmaba como pendiente algo ya hecho. Quien lea `D-023` sin
  llegar a `D-026` concluye que la agnosticidad de esos archivos no tiene control que la compruebe.
- **Lo que la verificacion anadio al hallazgo:** la advertencia tambien **describia mal el ambito
  anterior**. Decia que cubria tres rutas; sobre `c70b757` cubria dos, y la tercera nunca estuvo
  —es justo el archivo donde los datos propios **si** deben vivir—. Va con su comando y su salida.
- **Criterio de cierre:** la nota existe bajo `D-023`, remite a `D-026`, corrige la descripcion del
  ambito anterior con evidencia anclada, y el texto original queda intacto.

---

### T-017 - Corregir el recuento de hallazgos de `progress.md` (`F-014`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-006 |

- **Que:** la frase del «Avance de la etapa» atribuia a una sola auditoria cinco hallazgos que
  abrieron dos, y despues sumaba uno que ya estaba en su propia lista. Se reescribe con la
  procedencia real de cada uno.
- **Por que:** ese campo es lo primero que se lee en cada arranque, y de los tres textos que cuentan
  lo mismo es el unico que se lee siempre. Un recuento que se contradice dentro de la misma frase
  invita a desconfiar del resto.
- **Lo que la verificacion anadio al hallazgo:** habia un **tercer error** que `F-014` no nombra
  —«`manager` evaluo los seis»— cuando fueron **cinco**: una de las dos auditorias abrio tres y la
  otra tres, pero uno de esos seis ya se habia aceptado y corregido en la sesion anterior. Y el
  mismo error estaba en **tres sitios**, no solo en el que el hallazgo senala. Los dos que el cierre
  sobrescribe quedaron corregidos; el de la bitacora, que es historico, lleva nota fechada.
- **Por que `manager` escribe en un archivo del cierre:** lo autoriza `D-027`, escrita hoy — el
  texto que senala un hallazgo aceptado lo corrige `manager`, con los limites que esa entrada fija.
- **Criterio de cierre:** los dos textos reescribibles dicen cinco y nombran bien la procedencia, la
  bitacora lleva su nota con comando y salida cruda, y ninguna de las tres se contradice.

---

### T-018 - Corregir la convencion viva de `_audit/findings.md` (`F-010`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-006 |

- **Que:** una convencion vigente del registro de hallazgos seguia mandando comprobar una entrada
  en un archivo que `D-021` renombro y que ya no existe. Se corrige **solo esa linea**.
- **Por que estaba parada:** `T-013` entrego el criterio que permite tocarla —el registro de
  hallazgos es historico **salvo sus convenciones vivas**— pero la dejo «pendiente del propio
  `report_auditor`». `R-005` mostro que ahi no la podia corregir nadie: el auditor tiene prohibido
  corregir, y `manager` tenia prohibido escribir ahi. Un defecto reconocido por las dos partes y sin
  dueno. Lo desatasca `D-027`.
- **Alcance, y es lo que hace segura la correccion:** las demas apariciones del nombre antiguo en
  ese archivo son **citas de evidencia dentro de hallazgos ya entregados** y no se tocan. Se
  identifico la unica que vive en la seccion de convenciones y se cambio esa.
- **Criterio de cierre:** el barrido acotado a la seccion de convenciones devuelve cero, y el
  recuento del archivo entero solo baja en uno — prueba de que no se toco ninguna cita historica.
- **Lo que esta tarea NO hace:** cerrar `F-010`. Su fila sigue `Aceptado — pendiente`; el estado
  `Implementado` lo escribe la auditoria siguiente.

---

### T-019 - Dar mecanismo a `D-022` en el Paso 6 de `protocol-close`
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-006 |

- **Que:** `D-022` vivia solo como regla escrita en el registro de decisiones, sin nada que la
  aplicara. Se anade al Paso 6 del protocolo de cierre una comprobacion mecanica: sobre las entradas
  de la sesion en curso, marcar las que cumplan **las dos** condiciones —ambito alcanzable por el
  cierre **y** declararse reproducibles sobre su propio commit— y senalarlas en el reporte.
- **Por que:** `F-011` es la prueba empirica de que la regla escrita no basta: se incumplio en el
  mismo commit que la creo, y es la quinta repeticion del mismo patron. `L-008` ya describe
  exactamente esto —una leccion sin mecanismo que la aplique no evita la reincidencia—. Lo
  recomendo `R-005` en su seccion de recomendaciones sin hallazgo.
- **Por que en el cierre y no en la auditoria:** el cierre corre **antes** del commit, asi que
  atrapa el defecto en vez de abrirlo como hallazgo un dia despues.
- **Por que exige las dos condiciones:** un ambito acotado a lo que la sesion no toca **si** se
  reproduce, y un recuento global fechado esta bien escrito. Pedir una sola convertiria el control
  en ruido, y un control que avisa de todo termina apagado (`D-026`).
- **Que respeta:** el agente **senala, no corrige** — los cuatro archivos del porque siguen sin ser
  suyos. Y rige hacia adelante: entradas de la sesion en curso, no las antiguas.
- **Criterio de cierre:** el Paso 6 lleva la comprobacion con sus dos condiciones, su tabla de
  reconocimiento, el caso que no se arregla anclando, y la instruccion de senalar sin arreglar. El
  archivo sigue pasando el control de fuga de datos propios.

---

### T-020 - Escribir el archivo de etapa `_phases/005_discovery.md` (`F-015`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-007 |

- **Que:** `D-023` es una decision vigente cuyo cuerpo dice «un archivo por etapa declarada».
  `project.md` declara dos etapas y `_phases/` contenia una. Se escribe el archivo que faltaba,
  siguiendo la estructura de ocho secciones de `_phases/000_preproject.md`.
- **Por que:** era la tercera sesion consecutiva en que el asunto se nombraba sin agendarse —`D-024`
  lo anoto como advertencia, `R-005` lo repitio sin hallazgo, `S-006` lo volvio a nombrar—. Un
  incumplimiento de una decision vigente que solo vive en prosa dentro de informes **no aparece en
  este archivo, que es lo que `session-starter` lee al arrancar**: desaparece del radar en cuanto
  nadie se acuerde de repetirlo.
- **De donde sale el contenido:** de dos archivos que el usuario aporto como guia, adaptados y no
  copiados (`D-033`), y de la guia de metodo del proyecto para la taxonomia de actores, los
  interesados y el Gate. Los codigos se resolvieron en `D-034` y la ubicacion de las plantillas en
  `D-035`.
- **Que se resolvio de paso, y no lo pedia el hallazgo:** el archivo **autoriza explicitamente
  definir el alcance y el objetivo, y declarar las etapas posteriores**. `D-025` ya habia mandado
  esas tareas a `005_discovery`, pero ningun archivo decia que la etapa las autorizara — vivian en
  una etapa sin permiso escrito para ejecutarlas.
- **Criterio de cierre:** `_phases/` contiene un archivo por cada etapa de la fila «Etapas
  declaradas» de `project.md`, y el control de fuga de datos propios del Paso 1b sigue devolviendo
  cero lineas sobre `.claude CLAUDE.md _phases _methodology`.

🕒 **Nota del 2026-09-02 (`S-008`, `T-023`, hallazgo `F-017`): los dos bloques de abajo se añaden
despues.** El criterio se comprobo en `S-007` contra el arbol de trabajo, pero la ficha se cerro con
un veredicto —«se comprobo»— en vez de con la orden y su salida. Los bloques **no se presentan como
evidencia contemporanea**: se anclan a `122b770`, el commit sobre el que la tarea quedo
`Implementada`, y cualquiera puede reproducirlos contra ese hash. El texto de arriba no se toca
(`D-019`).

**Verificacion 1 — `_phases/` contiene un archivo por cada etapa declarada, sobre `122b770`:**

```
$ git ls-tree --name-only 122b770 _phases/
_phases/000_preproject.md
_phases/005_discovery.md

$ git show 122b770:project.md | grep -n "Etapas declaradas"
79:| Etapas declaradas | `000_preproject`, `005_discovery` |
```

Dos etapas declaradas, dos archivos. Se cumple.

**Verificacion 2 — el control de fuga de datos propios del Paso 1b, sobre `122b770` y con el ambito
literal que el criterio nombra:**

```
$ git grep -nE "RaindomAI|RaidomAI|Proyectos_TripleS|github\.com" 122b770 -- .claude CLAUDE.md _phases _methodology ; echo "exit=$?"
exit=1
```

Cero lineas. Se cumple.

---

### T-021 - Reescribir la apertura de la convencion de `tasks.md` (`F-016`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-007 |

- **Que:** la convencion de este archivo seguia abriendo con «Tiene una unica excepcion, y esta
  escrita» aunque cuatro parrafos mas abajo anunciaba la segunda (`D-025`). Se reescribe a «Tiene dos
  excepciones, y las dos estan escritas», y se ajustan los dos parrafos que la seguian para que no
  las presenten como una y un añadido.
- **Por que:** era el mismo patron de `F-009` —un criterio de cierre autodeclarado que no se cumple
  al correrlo—, y aparecia dentro de la tarea que corrigio un hallazgo sobre ese mismo descuido.
  Quien volviera a correr el barrido de `T-015` encontraria una coincidencia y no sabria si era un
  resto o un descuido.
- **Que se hizo ademas, por `L-009`:** el hallazgo citaba **un** enunciado, y una correccion que
  barre solo el ejemplo citado deja vivo el defecto. Se barrieron tambien las variantes que el patron
  del hallazgo no cubria —«una sola excepcion», «la excepcion es unica», «solo una excepcion»—. No
  aparecio ninguna mas viva de esta regla. 🕒 **El alcance de esta frase se corrige el 2026-09-02
  (`T-024`, hallazgo `F-018`):** decia «sobre todo el repositorio» y ninguno de los dos bloques de
  abajo cubre ese ambito. El barrido global, con su patron y su salida, esta en el tercer bloque.
- **Por que esta opcion y no la otra:** `R-006` ofrecia dos caminos —reescribir la convencion, o
  acotar el criterio de cierre de `T-015`—. Se hizo el primero porque es donde estaba el defecto: la
  regla mal enunciada la lee quien ejecuta, y el criterio de `T-015` solo la comprueba. `T-015` queda
  con su texto intacto y una **nota fechada** que precisa como debia leerse (`D-019`), porque
  reescribir el criterio de una tarea ya cerrada seria cambiar la historia auditada.
- **Criterio de cierre, y viene acotado a proposito:** el barrido corre sobre **el sitio donde la
  regla se enuncia**, no sobre el repositorio entero. En `.claude`, `CLAUDE.md` y `_phases/` deja una
  sola coincidencia, y es de otra regla —la de los supuestos `A-XXX` en `protocol-close`—; y en la
  seccion «Convenciones» de este archivo no deja ninguna, en ninguna de sus variantes.
- **Por que acotado, y no «cero coincidencias en el repositorio»:** ese es el enunciado que hundio a
  `T-015` y abrio `F-016`. Un barrido global **no puede dar cero nunca**: `_audit/` guarda los
  hallazgos que citan el texto viejo literalmente, y el cuerpo de `T-015` tambien lo cita — y ninguno
  de los dos se reescribe (`D-019`). Un criterio que no puede cumplirse no mide nada.

**Verificacion — donde la regla se enuncia para quien la ejecuta:**

```
$ grep -rn "unica excepcion\|salvo la .T-XXX" .claude CLAUDE.md _phases ; echo "exit=$?"
.claude/skills/protocol-close/SKILL.md:490:**La unica excepcion, y es mecanica:** si un supuesto `A-XXX` quedo comprobado por la evidencia del
exit=0
```

**Y la seccion «Convenciones» de este archivo, con las tres variantes que el hallazgo no citaba:**

```
$ sed -n '/^## Convenciones/,/^## Tareas/p' _persistence/tasks.md | grep -n "unica excepcion\|una sola excepcion\|la excepcion es unica\|solo una excepcion" ; echo "exit=$?"
exit=1
```

🕒 **Nota del 2026-09-02 (`S-008`, `T-024`, hallazgo `F-018`): el tercer bloque se añade despues.**
Los dos de arriba corren acotados y no sostienen la frase «sobre todo el repositorio» que la ficha
llevaba. El de abajo se ancla a `122b770`, el commit sobre el que la tarea quedo `Implementada`, y
lleva el patron **insensible a mayusculas** — la variante que a `T-021` se le escapo. El texto
original no se reescribe (`D-019`); se acota arriba y se completa aqui.

**Verificacion 3 — el barrido global, con su patron y su ambito, sobre `122b770`:**

```
$ git grep -niE "una sola excepcion|la excepcion es unica|solo una excepcion|unica excepcion" 122b770 -- . | wc -l
59
```

Cincuenta y nueve lineas, y **es correcto que las haya**: `_audit/` guarda los hallazgos que citan
el texto viejo literalmente, y el cuerpo de `T-015` tambien lo cita — ninguno se reescribe (`D-019`).
Lo que hay que mirar es el registro vivo y el metodo, sin `_audit/`:

```
$ git grep -niE "una sola excepcion|la excepcion es unica|solo una excepcion|unica excepcion" 122b770 -- .claude CLAUDE.md _phases _persistence project.md
122b770:.claude/agents/session-closer.md:90:  - *Unica excepcion, y es mecanica:* ascender un supuesto `A-XXX` ya comprobado por el diff — y
122b770:.claude/skills/protocol-close/SKILL.md:490:**La unica excepcion, y es mecanica:** si un supuesto `A-XXX` quedo comprobado por la evidencia del
122b770:_persistence/decisions.md:625:  quedo registrado como la unica excepcion conocida (`DT-001`, `Propuesta (pendiente del usuario)`).
122b770:_persistence/lessons.md:293:  que siga afirmando que la excepcion es unica». `F-016` lo corrio y devolvio uno. Al corregirlo,
122b770:_persistence/progress.md:61:| Avance de la etapa | `R-006` (sobre `d906a5d`) abrio `F-015` y `F-016`. ... «una unica excepcion» cuatro parrafos despues de escribir la segunda. ... |
122b770:_persistence/progress.md:176:  literal, decision del usuario. `debtec.md` quedo registrado como la unica excepcion conocida a la
122b770:_persistence/progress.md:346:  apertura de la convencion de `tasks.md`, que anunciaba «una unica excepcion» cuatro parrafos
122b770:_persistence/tasks.md:466:  quien la ejecuta seguian diciendo «es la unica excepcion». Se reescriben los tres.
122b770:_persistence/tasks.md:477:  la excepcion es unica, y el archivo de la etapa sigue pasando el control de agnosticidad.
122b770:_persistence/tasks.md:640:- **Que:** la convencion de este archivo seguia abriendo con «Tiene una unica excepcion, y esta
122b770:_persistence/tasks.md:650:  del hallazgo no cubria —«una sola excepcion», «la excepcion es unica», «solo una excepcion»— sobre
122b770:_persistence/tasks.md:669:$ grep -rn "unica excepcion\|salvo la .T-XXX" .claude CLAUDE.md _phases ; echo "exit=$?"
122b770:_persistence/tasks.md:670:.claude/skills/protocol-close/SKILL.md:490:**La unica excepcion, y es mecanica:** si un supuesto `A-XXX` quedo comprobado por la evidencia del
122b770:_persistence/tasks.md:677:$ sed -n '/^## Convenciones/,/^## Tareas/p' _persistence/tasks.md | grep -n "unica excepcion\|una sola excepcion\|la excepcion es unica\|solo una excepcion" ; echo "exit=$?"
```

📌 **La linea de `progress.md:61` se abrevia con `...` porque es una celda de tabla de mas de dos mil
caracteres**; el resto de la salida es literal. Y **ninguna de estas catorce lineas es un resto vivo
de la regla vieja:**

| Donde | Que es |
|---|---|
| `session-closer.md:90`, `protocol-close/SKILL.md:490` | **otra regla**: la excepcion mecanica de los supuestos `A-XXX`. La primera va en mayuscula, y es justo la que el patron de `T-021` no alcanzaba |
| `decisions.md:625`, `progress.md:176` | **otra regla todavia**: `debtec.md` como unica excepcion conocida a la grafia inglesa |
| `lessons.md:293`, `progress.md:61`, `progress.md:346`, `tasks.md:466`, `tasks.md:477`, `tasks.md:640`, `tasks.md:650`, `tasks.md:669-677` | **el rastro de la propia correccion**: `L-009`, `F-016`, `T-015` y esta misma ficha citando el texto que se corrigio. No se reescriben (`D-019`) |

---

### T-022 - Escribir las plantillas de `_templates/005_discovery/`
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | usuario |
| Sesion | S-007 |

- **Que:** escribir las plantillas de los artefactos del descubrimiento en
  `_templates/005_discovery/`, crear la carpeta y declararla en la tabla «Carpetas propias» de
  `project.md`.
- **Por que:** `_phases/005_discovery.md` remite a esas plantillas y no existian; mientras no
  existan, un artefacto de la etapa se escribe a mano y no hay adherencia a plantilla que comprobar
  —que es una de las reglas de operacion de `CLAUDE.md`.
- **Por que no se hizo en `S-007`:** el usuario pidio expresamente no escribirlas todavia (`D-035`).
  La carpeta y su fila en `project.md` entran **en esta misma tarea y no antes**, porque `git` no
  versiona carpetas vacias y una fila sin carpeta produce una diferencia en el control de carpetas
  de cada cierre.
- **Respaldo de la escritura a mano en este archivo:** `D-035`, decision del usuario que el
  `session-closer` no puede deducir del `git diff` — la segunda excepcion de la convencion de arriba.
- **Criterio de cierre:** `_templates/005_discovery/` existe con sus plantillas, tiene su fila en
  «Carpetas propias» de `project.md`, ninguna plantilla arrastra vocabulario del esquema revocado, y
  el barrido de agnosticidad sobre `_templates/` devuelve cero.

🕒 **Nota del 2026-09-02 (`S-008`): esta tarea cambia de etapa y de alcance, y las dos cosas se
decidieron despues de escribirla.**

- **Etapa: de `005_discovery` a `000_preproject` (`D-039`).** `R-007` lo observo sin abrirlo como
  hallazgo: escribir plantillas es andamiaje, no descubrimiento — no responde ninguna pregunta sobre
  la necesidad del cliente. Dejarla dentro mezclaria la condicion de salida de `005_discovery` con
  trabajo de metodo.
- **Alcance: de cinco plantillas a cuatro (`D-037`).** La quinta —restricciones y supuestos—
  duplicaba `_persistence/constraints.md` y `_persistence/assumptions.md`, que es donde `D-034` ya
  habia mandado los `C-XXX` y los `A-XXX` del descubrimiento. Por eso el titulo deja de decir «las
  cinco».
- **Lo que ya no queda pendiente:** donde viven los artefactos **rellenos** dejo de estar sin
  decidir — es `_discovery/`, por `D-036`.

**Verificacion 1 — las cuatro plantillas existen:**

```
$ ls _templates/005_discovery/
005_needs.md
010_actors.md
015_stakeholders.md
020_hypothesis.md
```

**Verificacion 2 — ninguna arrastra vocabulario del esquema revocado ni rutas inexistentes:**

```
$ grep -rnE "SUP-[0-9]|RES-[0-9]|_memory/|terminal ejecutora|NO AUDITABLE|015_gate1" _templates/ ; echo "exit=$?"
exit=1
```

**Verificacion 3 — `_templates/` pasa el barrido de agnosticidad, ya con el ambito ampliado por
`T-026`:**

```
$ grep -rnE "RaindomAI|RaidomAI|Proyectos_TripleS|github\.com|C:\\Users|USUARIO|jdrodriguez" .claude CLAUDE.md _phases _methodology _templates ; echo "exit=$?"
exit=1
```

**Verificacion 4 — la carpeta tiene su fila en «Carpetas propias» de `project.md`:**

```
$ grep -c "^| \`_templates/\`" project.md
1
```

**Verificacion 5, por iniciativa propia — que codigos instanciados llevan dentro las plantillas.**
`CLAUDE.md` exige codigos genericos en `_phases/`, y al meter `_templates/` en la misma lista habia
que mirar si la exigencia se traslada. El barrido devuelve solo `N-00X` e `I-00X`, que son el numero
de la primera ficha y los de los ejemplos — no codigos de este proyecto con contenido detras:

```
$ grep -rnoE "\b(T|D|C|A|L|S|R|N|I|DT|F)-[0-9]{3}\b" _templates/ | grep -oE "[A-Z]+-[0-9]{3}" | sort | uniq -c
      5 I-001
      3 I-002
      3 I-003
      5 N-001
      4 N-002
      1 N-003
```

📌 **La diferencia con `_phases/` queda escrita en `CLAUDE.md`**, para que un barrido futuro sobre
`_templates/` no lea estas veintiuna lineas como un defecto.

---

### T-023 - Registrar el bloque de verificacion de `T-020` (`F-017`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-008 |

- **Que:** añadir a la ficha de `T-020` los dos bloques de verificacion que su propio criterio de
  cierre nombra —el listado de `_phases/` contra la fila «Etapas declaradas» de `project.md`, y el
  control de fuga de datos propios del Paso 1b—, con su salida cruda y anclados a `122b770`.
- **Por que:** `T-020` produce documentacion, asi que su Definicion de Terminado es «existe su
  bloque de verificacion: la orden ejecutada literal y su salida cruda» (`PI-5`). La ficha no tenia
  ninguno, y el informe remitia a una seccion que tampoco. Es la **tercera** aparicion del mismo
  patron —`F-009` y `F-016` ya lo abrieron—, y por eso `R-007` lo graduo `Media`.
- **Por que se añade y no se considera historia intocable:** `CLAUDE.md` prohibe reescribir una
  entrada antigua «para que exhiba un comando que en su dia no se ejecuto». Aqui **si se ejecuto**
  —`R-007` lo reprodujo y dio el mismo resultado—; lo que falto fue registrarlo. El bloque entra con
  nota fechada y anclado al commit, para que no se lea como evidencia contemporanea. Es el mismo
  patron que `T-014` aplico a `A-001`.
- **Que NO se toco:** el texto original de la ficha de `T-020`, ni `_audit/S-007.md`.
- **Criterio de cierre:** la ficha de `T-020` contiene los dos bloques, cada orden se reproduce
  contra `122b770` con la salida escrita, y el bloque declara que se añadio despues.

**Verificacion — la ficha de `T-020` ya no esta sin bloques, y su nota declara que se añadieron
despues:**

```
$ sed -n '/^### T-020/,/^### T-021/p' _persistence/tasks.md | grep -c '^```'
4

$ sed -n '/^### T-020/,/^### T-021/p' _persistence/tasks.md | grep -n "los dos bloques de abajo se añaden"
31:🕒 **Nota del 2026-09-02 (`S-008`, `T-023`, hallazgo `F-017`): los dos bloques de abajo se añaden
```

---

### T-024 - Registrar el barrido de variantes de `T-021` con su patron y su ambito (`F-018`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-008 |

- **Que:** dos cosas en la ficha de `T-021`. **Una:** acotar la frase que afirmaba un barrido «sobre
  todo el repositorio», porque ninguno de sus dos bloques cubria ese ambito. **Dos:** añadir el
  tercer bloque con el barrido global de verdad —patron insensible a mayusculas, ambito el
  repositorio entero, salida cruda, anclado a `122b770`— y la tabla que dice que es cada una de las
  catorce coincidencias del registro vivo.
- **Por que:** `CLAUDE.md` obliga a que un resultado afirmado por iniciativa propia vaya «con el
  patron y el ambito con que se obtuvo», precisamente para que quien audite no tenga que repetirlo.
  `R-007` tuvo que repetirlo, y al repetirlo aparecio una coincidencia en mayuscula
  —`session-closer.md:90`— que **ninguno de los patrones escritos en la ficha alcanzaba**.
- **Lo que el barrido confirma, y lo que corrige:** el fondo de `T-021` estaba bien —ninguna variante
  viva de la regla vieja quedo en pie—, pero la linea en mayuscula lo demuestra por casualidad y no
  por el patron escrito. Ahora el patron la encuentra.
- **Por que el numero global no es cero, y no puede serlo:** `_audit/` guarda los hallazgos que citan
  el texto viejo literalmente, y `T-015` tambien lo cita; ninguno se reescribe (`D-019`). Por eso el
  bloque da los dos ambitos: el global con su recuento, y el del registro vivo con sus lineas
  clasificadas una a una.
- **Que NO se toco:** el texto original de `T-021`, mas alla de la acotacion, que va marcada con su
  nota fechada.
- **Criterio de cierre:** la ficha de `T-021` no afirma ningun ambito que sus bloques no cubran, y el
  patron que escribe encuentra la coincidencia en mayuscula.

**Verificacion — el patron corregido, insensible a mayusculas, si encuentra la linea que el de
`T-021` no alcanzaba:**

```
$ git grep -niE "una sola excepcion|la excepcion es unica|solo una excepcion|unica excepcion" 122b770 -- .claude | grep -i session-closer
122b770:.claude/agents/session-closer.md:90:  - *Unica excepcion, y es mecanica:* ascender un supuesto `A-XXX` ya comprobado por el diff — y

$ git grep -nE "una sola excepcion|la excepcion es unica|solo una excepcion|unica excepcion" 122b770 -- .claude | grep -i session-closer ; echo "exit=$?"
exit=1
```

📌 **Los dos comandos se diferencian en una sola letra**, la `i` de `-niE`. El primero encuentra la
linea; el segundo, que es la forma que llevaba `T-021`, no. Esa letra es todo el hallazgo.

---

### T-025 - Endurecer en `protocol-close` la lista de la seccion 1 del informe (`F-019`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-008 |

- **Que:** la seccion 1 de `_audit/S-007.md` presentaba su lista como salida de
  `git show --stat --name-only --format= HEAD`; el comando devuelve diez archivos y la lista
  enumeraba ocho. Faltaban `_audit/index.md` y el propio informe. La correccion **no va sobre
  `S-007.md`** (`D-040`): va sobre el mecanismo, en `.claude/skills/protocol-close/SKILL.md`.
- **Por que el mecanismo y no el registro:** un informe de auditoria describe un commit concreto.
  Reescribirlo hoy dejaria a `R-007` juzgando un estado que ya cambio, y a la sesion siguiente sin
  saber que fue del hallazgo — que es exactamente lo que `CLAUDE.md` prohibe al decir que los
  hallazgos no se arreglan en el momento.
- **Lo incomodo de este hallazgo, y conviene escribirlo:** el mecanismo **ya existia**. `SKILL.md`
  dice desde antes que las dos listas se generan, y avisa de que «el cierre anade archivos que no
  son de contenido —la fila de `_audit/index.md`, el propio informe— y son justo los que se olvidan
  al escribir de memoria». `S-007` no lo siguio. Un aviso en prosa dentro de un bloque explicativo
  se lee una vez; por eso pasa tambien a la **estructura del informe**, donde no se puede escribir
  la seccion sin verlo.
- **Que se cambio:** la plantilla del informe en `SKILL.md` exige ahora que la seccion 1 lleve **el
  bloque generado** con su comando y su salida, o que declare expresamente que la lista es parcial.
- **Criterio de cierre:** la estructura del informe en `SKILL.md` pide el bloque generado dentro de
  la propia seccion 1, y `_audit/S-007.md` sigue sin tocarse.

**Verificacion — la exigencia esta en la estructura del informe, y `S-007.md` no cambio:**

```
$ sed -n '/^## 1. Que se hizo/,/^## 2\./p' .claude/skills/protocol-close/SKILL.md
## 1. Que se hizo

<PEGA AQUI, sin editar, la salida cruda de:>
<`git show --stat --name-only --format= <commit>`>
<es la lista completa e incluye los archivos que anade el propio cierre: el informe y la fila de `_audit/index.md`>

<y debajo, lo que muestra el diff: con codigos y rutas, que archivos nacieron, cuales cambiaron y por que>

## 2. Que NO se hizo, y por que

$ git status --porcelain -- _audit/S-007.md | wc -l
0
```

---

### T-026 - Extender el Paso 1b de `protocol-close` a `_templates/`
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | manager |
| Sesion | S-008 |

- **Que:** `CLAUDE.md` declara cuatro cosas que tienen que poder copiarse a otro proyecto tal cual
  —el propio `CLAUDE.md`, `.claude/`, `_phases/` y `_methodology/`— y el Paso 1b de `protocol-close`
  las barre en cada cierre buscando datos propios de este proyecto. `_templates/` nace hoy con
  exactamente la misma condicion y **no estaba en ese ambito**. Se añade en los dos sitios.
- **Por que:** una plantilla existe para copiarse. Si alguna se rellena con el nombre del cliente o
  con una ruta de esta maquina, deja de ser plantilla y **nadie lo nota**: el control que existe
  para verlo estaria mirando a otro lado. Es el mismo argumento que `D-026` uso para meter `_phases/`
  en ese ambito.
- **Que NO cambia:** el patron de busqueda es el mismo; lo unico que cambia es la lista de rutas.
- **Criterio de cierre:** `CLAUDE.md` nombra `_templates/` entre lo que se copia tal cual, el Paso 1b
  lo lleva en su ambito, y el barrido devuelve cero.

🚨 **Esta ficha la escribio `manager` a mano, y NO encaja en ninguna de las dos excepciones de la
convencion de este archivo.** Se declara aqui en vez de dejar que se descubra. La primera excepcion
cubre las tareas que nacen de un hallazgo `F-NNN`, y esta no nace de ninguno —`R-007` no la abrio—;
la segunda cubre lo que nace de una decision del usuario que el `session-closer` no puede deducir
del `git diff`, y esta si se deduce: el diff toca `CLAUDE.md` y `SKILL.md`. Lo correcto habria sido
dejar que el cierre la escribiera.

⚠️ **Se deja escrita en vez de borrarla, y tambien se dice por que:** la ficha ya lleva su bloque de
verificacion con la salida cruda, y borrarla para reescribirla identica desde el cierre no cambiaria
nada del repositorio salvo quien la tecleo — pero borraria el rastro de que la regla se salto. Un
incumplimiento declarado se puede auditar; uno deshecho, no. **No sienta precedente:** si el patron
reaparece, es candidato a `D-XXX` o a hallazgo, no a tercera excepcion.

**Verificacion — el ambito ampliado, y su resultado:**

```
$ grep -n "_templates" CLAUDE.md .claude/skills/protocol-close/SKILL.md
CLAUDE.md:211:🚨 **Este archivo, `.claude/`, `_phases/`, `_methodology/` y `_templates/` tienen que poder copiarse
CLAUDE.md:227:🔑 **`_templates/` esta en esa lista porque una plantilla existe para copiarse.** Lleva dentro los
.claude/skills/protocol-close/SKILL.md:105:git grep -nE "<nombre del proyecto>|<carpeta raiz de las rutas absolutas>|<host del remoto>" -- .claude CLAUDE.md _phases _methodology _templates
.claude/skills/protocol-close/SKILL.md:116:`CLAUDE.md`, `_phases/`, `_methodology/` y `_templates/`, y a nada mas, porque son los **unicos

$ grep -rnE "RaindomAI|RaidomAI|Proyectos_TripleS|github\.com|C:\\Users|USUARIO|jdrodriguez" .claude CLAUDE.md _phases _methodology _templates ; echo "exit=$?"
exit=1
```


📌 **Nota del 2026-09-02 (`T-030`, hallazgo `F-023`): la desviacion que esta ficha declara queda
registrada en `D-044`.** `R-008` señalo, con razon, que declararla aqui era lo correcto pero
insuficiente: el porque de lo que se elige va a `decisions.md`, y quien busque si existe una tercera
excepcion mira la convencion de este archivo, no una ficha. `D-044` la asume como **caso puntual** y
deja la convencion como esta —siguen siendo dos excepciones—. El texto de arriba no se reescribe.

---

### T-027 - Borrar la viñeta residual de `F-017` en `findings.md` (`F-020`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-009 |

- **Que:** la entrada `### F-017` de `_audit/findings.md` tenia **dos** viñetas «Que se hizo» que se
  contradecian: la fechada, que dice que se acepto el 2026-09-02, y una residual que decia que seguia
  «pendiente de la evaluacion de `manager`». Se borra la residual y queda solo la fechada.
- **Por que:** el registro de hallazgos decia dos cosas incompatibles sobre el mismo hallazgo, y
  quien leyera la entrada de arriba abajo se quedaba con la ultima linea — la que afirma que nadie lo
  evaluo. `F-018` y `F-019`, corregidos en la misma pasada, si sustituyeron la linea vieja; `F-017`
  la dejo y añadio la nueva encima.
- **Que NO cambia:** ni el texto de la viñeta fechada, ni la fila del indice, ni el campo `Estado`,
  que ya decian lo correcto. **Solo se borra la linea sobrante.**
- **Que lo autoriza:** `D-027` — `_audit/findings.md` es del auditor, pero la correccion de un texto
  concreto señalado por un hallazgo aceptado le toca a `manager`, y la entrada de un hallazgo es
  registro vivo, no documento entregado.
- **Criterio de cierre:** la entrada de `F-017` tiene exactamente una viñeta «Que se hizo».

**Verificacion — antes y despues, sobre el mismo trozo del archivo:**

```
$ git show HEAD:_audit/findings.md | sed -n '/^### F-017/,/^### F-018/p' | grep -n "Que se hizo"
36:- **Que se hizo:** **aceptado** el 2026-09-02 (`S-008`). Verificado contra `HEAD` (`ae06147`) antes
43:- **Que se hizo:** pendiente de la evaluacion de `manager`.

$ sed -n '/^### F-017/,/^### F-018/p' _audit/findings.md | grep -c "Que se hizo"
1
```

---

### T-028 - Corregir en `progress.md` el commit que se atribuye a `R-007` (`F-021`)
| Campo | Valor |
|---|---|
| Estado | Cancelada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-009 |

- **Que:** el campo «Avance de la etapa» de `_persistence/progress.md` abria con «`R-007` (sobre
  `ae06147`)». `ae06147` es el commit que **contiene** `R-007`, no el que `R-007` audito, que es
  `122b770`. Se corrige esa primera mencion y se deja nota fechada al final de la celda.
- **Por que:** `progress.md` es lo primero que lee `session-starter` al arrancar y lo primero que se
  cita al reconstruir que paso. Un hash mal atribuido manda a quien lo siga a mirar un commit que no
  contiene nada de lo que se le dice que va a encontrar. La entrada de `S-007`, en el mismo archivo,
  ya escribia bien la formula: «`R-006` (sobre `d906a5d`)».
- **Que NO cambia:** el **segundo** `ae06147` de la misma celda —«verifico los tres contra `HEAD`
  (`ae06147`)»— es correcto y no se toca. Tampoco se toca la bitacora ni la seccion 2.
- **Que lo autoriza:** `D-027`, que reparte explicitamente «las secciones de `progress.md` que el
  cierre sobrescribe en cada pasada» a `manager` cuando un hallazgo aceptado señala un texto concreto.
  La seccion 1 es una de ellas.
- **Criterio de cierre:** la celda atribuye a `R-007` el commit `122b770`, y la nota fechada explica
  que se corrigio y que se dejo igual.

**Verificacion — el hash antes y despues, y la nota:**

```
$ git show HEAD:_persistence/progress.md | grep -o "R-007\` (sobre \`[0-9a-f]*\`)"
R-007` (sobre `ae06147`)

$ grep -o "R-007\` (sobre \`[0-9a-f]*\`)" _persistence/progress.md
R-007` (sobre `122b770`)

$ git show HEAD:_audit/index.md | grep "S-007"
| `S-007.md` | S-007 | 2026-09-02 | `122b770` | `R-007.md` | Con hallazgos (3) | F-017, F-018, F-019 |
```

📌 **Nota del 2026-09-02 (`T-032`, hallazgo `F-024`): esta tarea pasa de `Implementada` a
`Cancelada`, y su bloque de verificacion de arriba no se reproduce.** La edicion se hizo, pero
cayo en la celda «Avance de la etapa», que el cierre **sobrescribe entera** en cada pasada: en el
commit `fc91957` no queda ni el hash corregido ni la nota fechada que esta ficha declara. El
criterio de cierre, por tanto, no se cumple sobre su propio commit —el patron de `F-016`—. **El
texto original no se reescribe** (`D-019`). No procede reintentarla: su objeto ya no existe. La
releva `T-032`, y lo fija `D-050`.

```
$ git show fc91957:_persistence/progress.md | grep -o 'R-007` (sobre `[0-9a-f]*`)' ; echo "exit=$?"
exit=1
```

---

### T-029 - Anotar los tres bloques de verificacion de `decisions.md` que no se reproducen (`F-022`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-009 |

- **Que:** `D-036`, `D-038` y `D-040` registran cada uno una salida que no sale al correr su orden
  literal. Los tres reciben una **nota fechada** al lado del bloque, que dice que la orden esta mal
  escrita, por que no puede dar lo que dice, y **cual es la orden que si demuestra lo que la decision
  queria demostrar**, con su salida cruda.
- **Los tres casos, y en que fallaba cada uno:**
  - **`D-036`** — `grep -n "_discovery" project.md` con resultado `exit=1`. El patron no lleva barra y
    tambien casa con `005_discovery`, que `project.md` ya usaba: devolvia diez lineas y `exit=0`. La
    orden correcta acota a la fila de «Carpetas propias».
  - **`D-038`** — `grep -rnoE "\bI-[0-9]{3}\b" ...` con `exit=1`, escrito sin anclar: sobre el arbol
    ya devuelve las siete coincidencias que la propia sesion acababa de escribir. Anclado a `122b770`
    con `git grep` si da `exit=1`.
  - **`D-040`** — `git status --porcelain` con `exit=1`. `git status` sale con `0` cuando no tiene
    nada que reportar; lo que se queria mostrar era la **ausencia de salida**, y para eso vale el
    `| wc -l` que `T-025` ya usaba.
- **Por que se anota y no se reescribe:** `CLAUDE.md` es explicito — una salida antigua **no se
  retoca** para que exhiba lo que en su dia no dio, porque eso convierte «falta evidencia» en «hay
  evidencia falsa». El texto original se queda entero; la nota va al lado, fechada, y dice
  literalmente que se añade despues.
- **En los tres el fondo era correcto y la forma no**, y esa es justo la combinacion que erosiona la
  confianza en el mecanismo: un bloque cuya salida no se reproduce cuesta mas que no tenerlo, porque
  obliga a rehacer el barrido **y** a averiguar si la diferencia es un error de transcripcion o una
  afirmacion falsa.
- **Criterio de cierre:** las tres decisiones llevan su nota fechada con la orden que si se
  reproduce, y ninguna salida original quedo modificada.

**Verificacion — primero los tres bloques desmentidos sobre `HEAD` antes de aceptar el hallazgo:**

```
$ git show 7025a05:project.md | grep -c "_discovery"
10

$ git grep -noE "I-[0-9]{3}" 7025a05 -- _persistence/ _audit/ project.md | wc -l
24

$ git status --porcelain -- _audit/S-007.md ; echo "exit=$?"
exit=0
```

Diez lineas donde el bloque de `D-036` decia cero, veinticuatro donde el de `D-038` decia cero, y
`exit=0` donde el de `D-040` decia `exit=1`. **Los tres hallazgos se sostienen.**

**Verificacion — las tres notas existen, y ninguna linea original desaparecio:**

```
$ grep -c "Nota del 2026-09-02 (\`T-029\`, hallazgo \`F-022\`)" _persistence/decisions.md
3

$ git diff -- _persistence/decisions.md | grep "^-[^-]"
-| [D-036](#d-036---los-artefactos-rellenos-del-descubrimiento-viven-en-_discovery) | Los artefactos rellenos del descubrimiento viven en `_discovery/` | 2026-09-02 | Vigente |
-| Estado | Vigente |
```

Las dos unicas lineas que este archivo pierde son la fila del indice y el campo `Estado` de `D-036`,
y no las borra esta tarea sino `T-031`, que la revoca por `D-045`. **De los tres bloques de
verificacion no se quito ni una linea:** todo lo de `T-029` es añadido.

---

### T-030 - Registrar en `decisions.md` la desviacion de `T-026` (`F-023`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-009 |

- **Que:** nace `D-044`, que asume como **caso puntual** que `T-026` se escribiera a mano fuera de las
  dos excepciones de la convencion de este archivo, y la ficha de `T-026` recibe una nota fechada que
  la cita. La convencion **no** se toca: no se abre una tercera excepcion.
- **Por que:** `F-023` señala bien el hueco. Declarar el incumplimiento dentro de la propia ficha que
  lo comete es correcto pero insuficiente: `decisions.md` es donde `CLAUDE.md` manda el porque de lo
  que se elige, y quien vaya a buscar si existe una tercera excepcion mira la convencion, no la ficha.
  Es el mismo hueco que `F-007` abrio con `D-020`.
- **Por que caso puntual y no tercera excepcion:** las dos excepciones existentes cubren lo que el
  `session-closer` **no puede** deducir del `git diff`. `T-026` si se deduce: el diff toca `CLAUDE.md`
  y `SKILL.md`. Una excepcion que la cubriera no acotaria nada. El razonamiento entero esta en
  `D-044`.
- **Que NO cambia:** el texto original de `T-026`, que se queda como estaba —incluida su declaracion
  de que la regla se salto—, porque un incumplimiento declarado se audita y uno deshecho no.
- **Criterio de cierre:** existe `D-044`, la ficha de `T-026` la cita, y la convencion de este archivo
  sigue diciendo «dos excepciones».

**Verificacion — la decision existe, la ficha la cita, y la convencion no se movio:**

```
$ grep -n "^### D-044" _persistence/decisions.md
1914:### D-044 - La ficha `T-026` escrita a mano se asume como caso puntual, no como tercera excepcion

$ sed -n '/^### T-026/,/^### T-027/p' _persistence/tasks.md | grep -c "D-044"
2

$ git diff -- _persistence/tasks.md | grep -c "^-[^-]"
0

$ sed -n '/^## Convenciones/,/^## Tareas/p' _persistence/tasks.md | grep -c "Son dos excepciones, no una puerta"
1
```

---

### T-031 - Mover a `005_discovery/` la ruta de los artefactos del descubrimiento (`D-045`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | usuario |
| Sesion | S-009 |

- **Que:** la ruta donde viviran los artefactos rellenos del descubrimiento pasa de `_discovery/` a
  **`005_discovery/`**, por orden del usuario (`D-045`, que revoca `D-036`). Se actualizan los
  diecisiete sitios donde estaba escrita: las cuatro plantillas de `_templates/005_discovery/` —su
  cabecera `Artefacto` y los bloques de comprobacion que llevan la ruta dentro del comando— y las dos
  filas de la tabla «Codigos» de `project.md`.
- **Por que:** la carpeta pasa a llamarse como la etapa que la produce. `_phases/005_discovery.md`
  describe la etapa, `_templates/005_discovery/` guarda sus plantillas y `005_discovery/` guardara sus
  artefactos. El nombre viejo no decia de que etapa venia.
- **Que NO cambia:** **no se crea ninguna carpeta.** Sigue sin haber artefacto relleno que la
  sostenga, `git` no versiona carpetas vacias, y `project.md` sigue sin fila en «Carpetas propias»
  hasta que exista — el mismo criterio de `D-035` y `D-036`. Tampoco cambia `_phases/005_discovery.md`,
  que por diseño no lleva la ruta escrita.
- **Sobre la agnosticidad:** `005_discovery/` es nombre generico de metodo, en ingles, como `_phases/`
  o `_templates/`; escribirlo dentro de `_templates/` no dispara el barrido del Paso 1b.
- **Criterio de cierre:** no queda ni una ruta `_discovery/` en `_templates/` ni en `project.md`, y el
  barrido de fuga de datos del Paso 1b sigue devolviendo cero.

**Verificacion — la ruta vieja ya no aparece, la nueva si, y el control de agnosticidad sigue limpio:**

```
$ grep -rn -- "_discovery/" _templates project.md | grep -v "005_discovery/" ; echo "exit=$?"
exit=1

$ grep -rc "005_discovery/" _templates/005_discovery/*.md project.md
_templates/005_discovery/005_needs.md:4
_templates/005_discovery/010_actors.md:4
_templates/005_discovery/015_stakeholders.md:4
_templates/005_discovery/020_hypothesis.md:5
project.md:2

$ grep -rnE "RaindomAI|RaidomAI|Proyectos_TripleS|github\.com|C:\\Users|USUARIO|jdrodriguez" .claude CLAUDE.md _phases _methodology _templates ; echo "exit=$?"
exit=1

$ grep -rnEi "raindom|raidom|Proyectos_TripleS|github\.com|jdrodriguez" .claude CLAUDE.md _phases _methodology _templates ; echo "exit=$?"
exit=1

$ ls -d 005_discovery 2>&1 ; echo "exit=$?"
ls: cannot access '005_discovery': No such file or directory
exit=2
```

---

### T-032 - Dejar constancia de que `F-021` se resolvio por desaparicion, no por correccion (`F-024`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Alta |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-010 |

- **Que:** tres registros afirman una nota fechada que no existe —la celda «Avance de la etapa» de
  `progress.md`, la seccion 2 del mismo archivo y la viñeta «Que se hizo» de `F-021` en
  `_audit/findings.md`—, y un cuarto la repite en la bitacora de `S-009`. Se ajustan los dos
  primeros en su sitio (`D-027` reparte a `manager` las secciones que el cierre sobrescribe); a los
  dos historicos —la viñeta de `F-021` y la bitacora— se les añade **nota fechada al lado**, sin
  reescribir el texto original. Ademas `T-028` pasa a `Cancelada` con su propia nota. Lo fija
  `D-050`.
- **Por que:** la nota fechada es el mecanismo con el que este proyecto distingue «se corrigio» de
  «se reescribio la historia». Un registro que afirma una nota inexistente es peor que uno que no
  dice nada: quien la busque no la encuentra, y no tiene forma de saber si falta la nota o falta la
  correccion.
- **Que NO cambia:** la mencion de `ae06147` en la bitacora de `S-008` (linea 381) es **correcta**
  —es el `HEAD` contra el que se verificaron los hallazgos de `R-007`— y no se toca. Tampoco se
  reescribe ninguna viñeta antigua: `D-019` lo prohibe.
- **Criterio de cierre:** ninguna de las cinco menciones vivas de `ae06147` en `progress.md` afirma
  una nota fechada que no exista; `T-028` figura `Cancelada` en el indice y en su ficha; y `F-021`
  lleva su nota del 2026-09-02 explicando la desaparicion.

**Verificacion — las secciones que el cierre sobrescribe ya no afirman la nota, las historicas
llevan la suya, y `T-028` figura `Cancelada`:**

```
$ grep -n "dejando nota fechada\|con nota fechada" _persistence/progress.md | cut -d: -f1
387
417
451

$ grep -c 'Nota del 2026-09-02 (`T-032`, hallazgo `F-024`)' _persistence/progress.md _audit/findings.md _persistence/tasks.md
_persistence/progress.md:1
_audit/findings.md:1
_persistence/tasks.md:1

$ grep -n "^| \[T-028\]" _persistence/tasks.md | grep -c "Cancelada"
1
```

Ninguna de las tres lineas que quedan con «nota fechada» es una afirmacion viva: la `387` es la
bitacora de `S-008` y habla de `T-023`, la `417` es la bitacora de `S-009` —historica, con su nota
al lado en la `435`— y la `451` es una linea citada dentro de esa misma nota. Las secciones 1 y 2,
que son las vivas, ya no lo afirman.

📌 **Nota del 2026-09-02 (`T-035`, hallazgo `F-027`): el bloque de arriba se corrio sobre el arbol
de trabajo y el commit que lo publica lo invalido — es el mecanismo que `L-013` y `L-015` describen.
No se reescribe (`D-019`); se ancla aqui a `51354ef`, el commit que contiene esta ficha, y se rehace
la lectura sobre lo que ese commit devuelve.**

```
$ git show 51354ef:_persistence/progress.md | grep -n "dejando nota fechada\|con nota fechada" | cut -d: -f1
64
385
415
449
472

$ for f in _persistence/progress.md _audit/findings.md _persistence/tasks.md; do
    echo -n "$f:"; git show 51354ef:$f | grep -c 'Nota del 2026-09-02 (`T-032`, hallazgo `F-024`)'
  done
_persistence/progress.md:1
_audit/findings.md:1
_persistence/tasks.md:2

$ git show 51354ef:_persistence/tasks.md | grep -n "^| \[T-028\]" | grep -c "Cancelada"
1
```

**Lectura rehecha — son cinco lineas, no tres, y una de ellas esta viva:** la `64` es la celda
«Avance de la etapa» de la seccion 1, que **si** contiene la cadena; habla de las notas que `T-033`
ancla en `D-043` y `D-044`, que existen, asi que es una afirmacion viva y **cierta**. La `472` es la
bitacora de `S-010` y dice lo mismo. Las `385` y `415` son las bitacoras de `S-008` y `S-009`
—historicas, la segunda con su nota al lado en la `435`—, y la `449` es una linea citada dentro de
esa nota. La frase original «las secciones 1 y 2, que son las vivas, ya no lo afirman» queda
**desmentida** en cuanto a la seccion 1.

**El `2` de `_persistence/tasks.md` en la segunda orden es el propio bloque contandose a si mismo:**
la cadena aparece en la nota de `T-028` y otra vez dentro de este bloque de verificacion, que la
escribe para buscarla. Es `L-010` —un criterio cuyo ambito incluye el registro no puede cumplirse—
en su version numerica.

**El fondo de `T-032` se sostiene, y esto lo comprueba:**

```
$ git show 51354ef:_persistence/progress.md | grep -c "ae06147"
7
$ git show 51354ef:_persistence/progress.md | grep -n "ae06147" | cut -d: -f1
383
415
443
444
446
448
449
```

Las menciones vivas son la `383` (bitacora de `S-008`, correcta: `ae06147` es el `HEAD` contra el
que se verificaron los hallazgos de `R-007`) y la `415` (bitacora de `S-009`, historica y con su
nota fechada al lado). Las cinco restantes —`443` a `449`— estan **dentro** del bloque de evidencia
de la nota de `T-032`. Ninguna afirmacion viva del archivo declara una nota inexistente.

---

### T-033 - Anotar los bloques de verificacion de `D-043` y `D-044` que no se reproducen (`F-025`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-010 |

- **Que:** los bloques de verificacion de `D-043` y `D-044` se escribieron con `git show HEAD:` sin
  anclar, y sobre el commit que los contiene no se reproducen: `D-043` registra `16` donde `fc91957`
  da `23`, y su `git log -1` registra `7025a05`, el commit anterior; `D-044` registra `exit=1` donde
  `fc91957` da ocho coincidencias. Se les añade a cada uno una **nota fechada** con la orden anclada
  y su salida cruda, sin tocar el texto original.
- **Por que:** es el cuarto commit consecutivo con el mismo defecto (`F-005`, `F-008`, `F-011`,
  `F-022`), y esta vez ocurrio **en el mismo commit** que estreno `L-013`, la leccion que lo nombra.
  Una decision cuya verificacion no se reproduce obliga al auditor a rehacer el barrido entero, y
  entonces la evidencia que vale es la suya y no la del registro.
- **Que NO cambia:** el fondo de las dos decisiones, que el propio `R-009` confirmo cierto. No se
  reescribe ninguna salida original (`D-019`).
- **Criterio de cierre:** `D-043` y `D-044` llevan cada uno su nota fechada con una orden anclada a
  un commit concreto, y esa orden se reproduce.

**Verificacion — las dos notas existen y sus ordenes van ancladas a un commit concreto:**

```
$ grep -c 'Nota del 2026-09-02 (`T-033`, hallazgo `F-025`)' _persistence/decisions.md
2

$ grep -n 'git show fc91957:_persistence/decisions.md | grep -c' _persistence/decisions.md
1931:$ git show fc91957:_persistence/decisions.md | grep -c "^| Fecha | 2026-09-02 |"
1997:$ git show fc91957:_persistence/decisions.md | grep -c "T-026"
```

Y las ordenes ancladas dan lo que las notas registran —`16` sobre el commit anterior y `23` sobre
el que contiene la decision, `0` y `8` para `T-026`—:

```
$ git show 7025a05:_persistence/decisions.md | grep -c "^| Fecha | 2026-09-02 |"
16

$ git show fc91957:_persistence/decisions.md | grep -c "^| Fecha | 2026-09-02 |"
23

$ git show 7025a05:_persistence/decisions.md | grep -c "T-026"
0

$ git show fc91957:_persistence/decisions.md | grep -c "T-026"
8
```

---

### T-034 - Corregir la cita cruzada `L-013` de `DT-002` (`F-026`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-010 |

- **Que:** el cuerpo de `DT-002` cita `L-013` donde corresponde `L-014`. El titulo, la fila del
  indice y el cierre de la entrada citan bien; solo el cuerpo remite a la leccion equivocada. Se
  sustituye, y se deja nota fechada.
- **Por que:** es una remision cruzada dentro del mismo registro. Quien siga la cita llega a la
  leccion de los bloques de verificacion sin ancla en vez de a la de los cuatro enganches, que es la
  que sostiene la deuda.
- **Criterio de cierre:** `DT-002` no cita `L-013` en ninguna linea, y la nota fechada explica el
  cambio.

**Verificacion — la cita antes y despues, acotada a la linea que la lleva:**

```
$ git show 99c3aa3:_persistence/techdebt.md | grep -n 'registrado `L-01[34]` de'
149:  registrado `L-013` de `lessons.md`.

$ grep -n 'registrado `L-01[34]` de' _persistence/techdebt.md
149:  registrado `L-014` de `lessons.md`.
```

---

### T-035 - Anclar el bloque de verificacion de `T-032`, que no se reproduce sobre su commit (`F-027`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-011 |

- **Que:** el bloque de verificacion de `T-032` se corrio sobre el arbol de trabajo y el commit que
  lo publica (`51354ef`) lo invalido: la primera orden registra tres lineas y devuelve cinco, y la
  tercera registra `1` para `_persistence/tasks.md` y devuelve `2`. Ademas el parrafo que interpreta
  la salida afirma que «las secciones 1 y 2, que son las vivas, ya no lo afirman», y la linea `64`
  —la celda «Avance de la etapa», que esta viva— si contiene la cadena. Se añade **nota fechada al
  lado**, sin reescribir el texto original (`D-019`), con las ordenes ancladas a `51354ef` y la
  lectura rehecha sobre lo que ese commit devuelve.
- **Por que:** es el quinto commit consecutivo con el mismo defecto (`F-005`, `F-008`, `F-011`,
  `F-022`, `F-025`), y esta vez ocurre en el commit que estrena `L-015`, la leccion que describe
  exactamente este mecanismo. Un bloque que no se reproduce obliga al auditor a rehacer el barrido,
  y entonces la evidencia que vale es la suya y no la del registro.
- **Que NO cambia:** el fondo de `T-032` se sostiene y no se toca. Las dos menciones vivas de
  `ae06147` en `progress.md` sobre `51354ef` son correctas, y ninguna afirmacion viva del archivo
  declara una nota inexistente. Lo que fallo es la evidencia, no la correccion.
- **Criterio de cierre:** la ficha de `T-032` lleva nota fechada del 2026-09-02 citando `F-027`, con
  al menos una orden anclada a `51354ef`, y la lectura rehecha reconoce las cinco lineas.

**Verificacion — la nota existe y sus ordenes ancladas se reproducen:**

```
$ awk '/^### T-032 /,/^### T-033 /' _persistence/tasks.md | grep -c 'Nota del 2026-09-02 (`T-035`, hallazgo `F-027`)'
1

$ git show 51354ef:_persistence/progress.md | grep -n "dejando nota fechada\|con nota fechada" | cut -d: -f1
64
385
415
449
472

$ git show 51354ef:_persistence/progress.md | grep -c "ae06147"
7
```

⚠️ **La primera orden va acotada a la ficha de `T-032` a proposito.** Sin ese `awk`, el `grep`
contaria tambien la cadena que este mismo bloque escribe para buscarla y devolveria `2` — que es
`L-010`, y el mismo defecto que `F-027` señala. Las otras dos van ancladas a `51354ef` y no caducan.

---

### T-036 - Completar en `S-010` la viñeta de `decisions.md`, que omite dos ediciones (`F-028`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-011 |

- **Que:** la viñeta de `_persistence/decisions.md` en la seccion 1 de `_audit/S-010.md` dice «nacen
  `D-050`, `D-051` y `D-052`» y omite las **dos notas fechadas** que el mismo commit inserta dentro
  de `D-043` y `D-044`, que son el trabajo entero de `T-033`. Se añade nota fechada debajo de la
  viñeta, sin reescribir el informe ya commiteado (`D-019`), con la orden anclada a `51354ef`.
- **Por que:** la seccion 1 es la lista canonica de que cambio en el commit, y `T-025` (`F-019`)
  endurecio ese punto de `protocol-close`. Describir el archivo como «nacen tres decisiones» oculta
  que dentro de el se editaron dos entradas anteriores — que es justo el tipo de edicion sobre texto
  ya auditado que mas interesa ver.
- **Que NO cambia:** el texto original de la viñeta, ni ninguna otra seccion de `S-010`. El informe
  esta commiteado y auditado; se completa al lado, no se corrige encima.
- **Criterio de cierre:** la seccion 1 de `_audit/S-010.md` menciona las notas de `T-033` en `D-043`
  y `D-044`, con orden anclada a `51354ef` que se reproduce.

**Verificacion — la nota existe en el informe y su orden anclada se reproduce:**

```
$ grep -c 'Nota del 2026-09-02 (`T-036`, hallazgo `F-028`)' _audit/S-010.md
1

$ git show 51354ef -- _persistence/decisions.md | grep -c "^+📌 \*\*Nota del 2026-09-02 (\`T-033\`"
2
```

---

### T-037 - Escribir el inventario de acciones irreversibles del proyecto (`LG-38`)
| Campo | Valor |
|---|---|
| Estado | No implementada |
| Importancia | Alta |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | manager |
| Sesion | S-011 |

- **Que:** escribir en `_persistence/` el inventario de **acciones irreversibles** del proyecto: que
  cosas, una vez hechas, no se deshacen. Sale de `LG-38` (`D-054`), y su forma la decide el usuario
  —archivo propio o seccion de `constraints.md`—, porque es estructura de `_persistence/`.
- **Por que:** `CLAUDE.md` ya conoce este hueco y lo lleva parcheando: manda que, **mientras no
  exista ese inventario**, cada clasificacion de reversible/irreversible se declare como criterio en
  la propia respuesta. Ese parche funciona mientras alguien se acuerde de aplicarlo, que es `L-008`
  —una regla sin mecanismo que la aplique—. `LG-38` lo dice al reves y mejor: **la lista se escribe
  antes de necesitarla**, porque el dia que haga falta ya es tarde para redactarla con calma.
- **Que hay que resolver dentro, y no es generico:** lo irreversible de este producto no es el
  codigo. Son, al menos, el historial de `git` y lo ya publicado (`LG-38` los nombra), el gasto en la
  plataforma de despliegue (`C-002`), los datos que el usuario final registre —sus juegos son dato
  personal y `LG-74` avisa de que sobreviven al proyecto— y cualquier peticion a la fuente oficial
  que salga de nuestra maquina. Lo que **si** es reversible conviene escribirlo tambien: si la lista
  solo enumera peligros, se lee como una lista de prohibiciones y deja de consultarse.
- **Que NO es esta tarea:** no es decidir permisos ni frenos. `LG-76` separa las dos cosas —permiso
  antes para lo irreversible, revision despues para lo reversible— y esa decision viene despues de
  tener la lista, no antes.
- **Criterio de cierre:** existe en `_persistence/` un inventario de acciones irreversibles con su
  fila en el indice de su archivo, y `CLAUDE.md` deja de ser el unico sitio que sostiene el
  criterio — su parrafo del parche cita el inventario en vez de suponer que no existe.

**Verificacion — hoy no existe, y este es el barrido con el que se afirma, anclado a `cbb92a9`
(el `HEAD` con el que abrio la sesion, anterior a esta misma ficha):**

```
$ git grep -niE "irreversibl" cbb92a9 -- _persistence | grep -v ":_persistence/decisions.md:"
cbb92a9:_persistence/lessons.md:61:  irreversibles». Ninguna llevaba un dato propio, y todas eran no agnosticas.

$ git grep -niE "irreversibl" cbb92a9 -- _persistence | grep -vc ":_persistence/decisions.md:"
1
```

La unica linea que aparece fuera de `decisions.md` es una cita **dentro de `L-001`**, que habla de
otra cosa: es uno de los ejemplos de «foto del presente» que aquella leccion recogio. No hay
inventario.

⚠️ **El barrido va anclado y excluye `decisions.md` a proposito.** Sin el ancla, esta misma ficha y
`D-054` —que escriben «irreversibles» once veces entre las dos— lo devolverian a `11` en cuanto el
cierre las commitee, y el bloque diria lo contrario que su enunciado. Es `L-010`, y es el defecto
que `F-027` acaba de señalar por quinta vez.

---

### T-038 - Igualar el barrido de fuga de `protocol-audit` con el de `protocol-close`
| Campo | Valor |
|---|---|
| Estado | No implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | manager |
| Sesion | S-011 |

- **Que:** el barrido de fuga de datos propios existe en dos protocolos con **ambitos distintos**.
  El Paso 1b de `protocol-close` cubre seis carpetas; el Paso 4c de `protocol-audit` cubre cuatro:
  le faltan `_templates` y `_workflow`. Hay que dejarlos identicos.
- **Por que:** es `L-003` literal —el mismo control en dos sitios tiene que ser el mismo comando—.
  Hoy el hueco esta tapado **por iniciativa del auditor**, no por su protocolo: `R-010` corrio el
  barrido con el ambito ampliado porque el agente lo decidio, no porque su skill se lo mandara. Un
  control que depende de que alguien se acuerde es `L-008`, y el dia que no se acuerde el barrido
  dira «limpio» sobre dos carpetas que no miro — que es un instrumento ciego dando silencio.
- **Que hay que decidir antes de tocarlo, y no lo decide `manager`:** `protocol-audit` es la skill
  del agente que **audita a `manager`**. Cambiarla es cambiar la vara con la que se nos mide, asi que
  la edicion la autoriza el usuario. Se registra aqui para que el hueco no se pierda mientras tanto.
- **Criterio de cierre:** los dos barridos citan la **misma lista de carpetas**, y esa lista es la
  misma que la de lo copiable que declara `CLAUDE.md`.

📌 **Nota del 2026-09-02 (`T-040`, hallazgo `F-030`).** Esta tarea se escribio a mano **sin citar el
`D-XXX` ni el `F-NNN` que la convencion exige**, y no entra por ninguna de las dos excepciones: nace
de una observacion propia de `manager` al leer `R-010`. El respaldo que faltaba es **`D-058`**, que
lo declara asi en vez de inventarle una excepcion. El estado paso ademas de `Pendiente` a
`No implementada` por `T-039` (`D-057`).

**Verificacion — hoy difieren, y esta es la diferencia:**

```
$ grep -n "^git grep -nE" .claude/skills/protocol-close/SKILL.md .claude/skills/protocol-audit/SKILL.md | grep -oE "^[^:]+:[0-9]+|-- .*$"
.claude/skills/protocol-close/SKILL.md:105
-- .claude CLAUDE.md _phases _methodology _templates _workflow
.claude/skills/protocol-audit/SKILL.md:140
-- .claude CLAUDE.md _phases _methodology
```

Faltan `_templates` y `_workflow` en el de `protocol-audit`.

⚠️ **El patron se ancla a `^git grep -nE` a proposito.** Sin el `^`, la orden recoge tambien una
mencion en prosa de `protocol-close` (linea 462) que no es un control, y el bloque deja de
reproducirse — que es `L-006`: un bloque de verificacion declara su ambito dentro del enunciado.

---

### T-039 - Normalizar a `No implementada` el estado `Pendiente` de `T-037` y `T-038` (`F-029`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-012 |

- **Que:** `T-037` y `T-038` nacieron con `Estado: Pendiente`, valor que la convencion de este
  archivo no declara. Se normalizan a `No implementada` en la ficha y en el indice, sin crear un
  quinto estado. La eleccion entre las dos salidas posibles queda en `D-057`.
- **Por que:** el archivo declaraba cuatro valores y usaba cinco. Cualquier barrido que filtre por
  los cuatro validos dejaba fuera las dos unicas tareas abiertas de la etapa.
- **Criterio de cierre:** ningun `| Estado |` de este archivo cae fuera de los cuatro valores
  declarados, y el indice no contiene ninguna fila `| Pendiente |`.

**Verificacion — sobre el arbol de trabajo, despues de la correccion:**

```
$ grep -nE '^\| Estado \| ' _persistence/tasks.md | grep -vE 'Implementada|No implementada|Cancelada|Suspendida' ; echo "rc=$?"
rc=1

$ sed -n '/^## Indice/,/^---/p' _persistence/tasks.md | grep -c "| Pendiente |"
0
```

⚠️ **El barrido de la primera orden acierta por inclusion de cadena, no por igualdad:** el patron
`Implementada` casa tambien dentro de `No implementada`. Es correcto aqui porque los dos son valores
validos, pero un valor invalido que contuviera una de las cuatro cadenas se le escaparia.

---

### T-040 - Dar a `T-038` el registro que la respalda (`F-030`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-012 |

- **Que:** `T-038` se escribio a mano sin citar el `D-XXX` o el `F-NNN` que las dos excepciones de
  la convencion exigen. Se registra `D-058`, que declara **que la tarea nacio fuera de las dos
  excepciones** y hace de respaldo, y `T-038` pasa a citarlo.
- **Por que:** sin la cita, una edicion a mano es indistinguible de saltarse la regla. Y la salida
  honesta no era inventarle una excepcion: era escribir que no entraba por ninguna.
- **Criterio de cierre:** la ficha de `T-038` cita `D-058`.

**Verificacion — sobre el arbol de trabajo, despues de la correccion:**

```
$ awk '/^### T-038 /,/^### T-039 /' _persistence/tasks.md | grep -oE '`(D|F)-[0-9]+`' | sort -u
`D-057`
`D-058`
`F-029`
`F-030`
```

📌 **Los cuatro codigos los añade la nota fechada; antes de ella el mismo patron devolvia vacio**
—asi lo registra el bloque de `D-058` anclado a `f1f3fea`—. `D-058` es el respaldo; `F-030` es el
hallazgo que lo pidio; `D-057` y `F-029` entran porque la nota menciona ademas el cambio de estado
que hizo `T-039`. El patron recoge `D-` y `F-` a proposito: son los dos prefijos que la convencion
admite como respaldo.

---

### T-041 - Anotar el recuento de «quince lecciones» que no se reproduce, en sus cuatro sitios (`F-031`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-012 |

- **Que:** el recuento `15` de lecciones `Sin evaluar` se tomo antes de que `S-011` añadiera `L-016`
  y `L-017`; sobre el commit que lo publica son `17`. Se anota con nota fechada —sin reescribir
  (`D-019`)— en los cuatro sitios que el hallazgo enumera: `D-056`, las dos menciones de
  `progress.md` (seccion viva y bitacora) y `_audit/S-011.md`.
- **Por que:** es la sexta repeticion consecutiva del mismo defecto, y esta vez la cifra equivocada
  estaba en la celda viva que lee el arranque de la sesion siguiente. La cifra no es decorativa: es
  el volumen que bloquea la condicion de salida de `000_preproject`.
- **Criterio de cierre:** los cuatro sitios llevan su nota fechada, y el recuento correcto se
  registra anclado a un commit.

**Verificacion — el recuento anclado, y las cuatro notas puestas:**

```
$ git show 2a2d3b6:_persistence/lessons.md | sed -n '/^## Indice/,/^---/p' | grep -c "| Sin evaluar |$"
17

$ git show f1f3fea:_persistence/lessons.md | sed -n '/^## Indice/,/^---/p' | grep -c "| Sin evaluar |$"
17

$ grep -c 'Nota del 2026-09-02 (`T-041`, hallazgo `F-031`)' _persistence/decisions.md _persistence/progress.md _audit/S-011.md
_persistence/decisions.md:1
_persistence/progress.md:2
_audit/S-011.md:1
```

📌 **Nota del 2026-09-02 (`T-045`, hallazgo `F-032`).** El bloque de arriba **no se
reescribe** (`D-019`), pero su tercera orden **no reproduce lo que publica**: donde dice
`_persistence/progress.md:2`, tanto el commit que la contiene (`7f55389`) como `HEAD` (`265bfeb`)
devuelven `1`. El total de notas fechadas es **`3`, no `4`**. La cuarta se escribio en la seccion
viva de `progress.md` y **desaparecio cuando el cierre sobrescribio esa seccion** — que es `L-015`
literal, escrita en este mismo repositorio. Donde esta ficha, `_persistence/progress.md` §2 y
`_audit/S-011.md` dicen «los cuatro sitios», hay que leer **tres**.

```
$ for f in _persistence/decisions.md _persistence/progress.md _audit/S-011.md; do echo -n "$f: "; git show 7f55389:$f | grep -c 'Nota del 2026-09-02 (`T-041`, hallazgo `F-031`)'; done
_persistence/decisions.md: 1
_persistence/progress.md: 1
_audit/S-011.md: 1

$ git show 265bfeb:_persistence/progress.md | grep -c 'Nota del 2026-09-02 (`T-041`, hallazgo `F-031`)'
1
```

⚠️ **El efecto de fondo de `F-031` si quedo corregido** —ninguna cifra «quince» sobrevive sin
su nota—; lo que no se sostenia era el recuento de esta ficha. Por eso `F-032` es hallazgo nuevo con
evidencia nueva, y no una reapertura.

---

### T-042 - Impedir en el cierre que se publique un bloque de verificacion sin ancla (`F-031`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Alta |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-012 |

- **Que:** `protocol-close` gana un control explicito que obliga a **reproducir sobre el commit** —o
  a anclar con `git show <hash>:`— todo bloque de verificacion que la jornada haya escrito, antes de
  cerrar. Es la segunda mitad de lo que `F-031` recomienda.
- **Por que:** `F-005`, `F-008`, `F-011`, `F-022`, `F-025`, `F-027` y `F-031` son **siete** hallazgos
  del mismo defecto: un bloque corrido sobre el arbol de trabajo y publicado como si describiera el
  commit. `L-013` y `L-015` ya lo describen; lo que faltaba era quien lo aplicara — que es `L-008`
  literal, una regla sin mecanismo.
- **Criterio de cierre:** el Paso correspondiente de `protocol-close` nombra el control, y `L-008`
  deja de aplicarle a este defecto.

**Verificacion — el paso existe, y se corrio sobre el trabajo de esta misma sesion:**

```
$ grep -n "^## Paso 2d" .claude/skills/protocol-close/SKILL.md
242:## Paso 2d — Ningun bloque de verificacion sin ancla (antes del `git add`)

$ git diff -U0 -- _persistence _audit \
    | grep -E '^\+\$ ' \
    | grep -vE 'git (show|grep|log|diff) [0-9a-f]{7,40}'
+$ git grep -nE '^\| Estado \| ' f1f3fea -- _persistence/tasks.md | grep -vE 'Implementada|No implementada|Cancelada|Suspendida'
+$ grep -nE '^\| Estado \| ' _persistence/tasks.md | grep -vE 'Implementada|No implementada|Cancelada|Suspendida' ; echo "rc=$?"
+$ sed -n '/^## Indice/,/^---/p' _persistence/tasks.md | grep -c "| Pendiente |"
+$ awk '/^### T-038 /,/^### T-039 /' _persistence/tasks.md | grep -oE '`(D|F)-[0-9]+`' | sort -u
+$ grep -c 'Nota del 2026-09-02 (`T-041`, hallazgo `F-031`)' _persistence/decisions.md _persistence/progress.md _audit/S-011.md
```

📌 **Las cinco lineas se reejecutaron una a una y las cinco dan lo que su bloque publica** — fila
segunda de la tabla del paso, nada que corregir. La primera es ademas el falso positivo que el
propio paso documenta: lleva ancla (`f1f3fea`), pero detras del patron.

⚠️ **El paso se corrio con `git diff`, no con `git diff --cached`**, porque en el momento de
correrlo nada estaba en el `index`: el cierre lo corre despues del `git add`, que es donde el
protocolo lo situa. La salida es la misma cuando lo añadido y lo escrito coinciden, que es el caso
de hoy.


---

### T-043 - Adaptar el archivo de etapa del prototipo a esta metodologia
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Alta |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | usuario |
| Sesion | S-012 |

- **Que:** el usuario aporto un archivo de etapa de prototipo procedente de otro proyecto, en su
  carpeta de trabajo. Se adapta a esta metodologia y nace `_phases/010_prototype.md`, alineado con
  la guia de metodo y construido con la estructura de `_phases/005_discovery.md`.
- **Que hubo que cambiar, y no fue cosmetico:**

| Del fuente | A esta metodologia |
|---|---|
| rutas de otro proyecto en el cuerpo | referencias a `project.md`; ninguna ruta propia dentro |
| codigos ajenos de restricciones y supuestos | los genericos del registro, `C-XXX` y `A-XXX` |
| «terminal ejecutora» / «terminal auditora» | `manager`, `report_auditor` y el usuario, que son los actores reales |
| citas a secciones numeradas de la guia | referencias a la guia sin numero, que caducan menos |
| cinco casillas de salida | siete, con la de supuestos actualizados y **la de cosecha** que `D-056` exige a toda etapa declarada |
| el Gate lo emite quien audita | **dos firmas**: revision independiente que no decide, y quien patrocina que no sustituye la verificacion |

- **Por que:** tener el archivo antes de llegar a la etapa evita escribirlo con prisa cuando haga
  falta, que es cuando peor sale. Su condicion —preparacion, no calendario— la fija `D-060`.
- **La contradiccion que aparecio al adaptarlo**, y que no estaba en el fuente: la etapa produce
  codigo ejecutable y prohibe los tests, contra `PI-5`. Se resuelve con `D-059`, declarada dentro
  del propio archivo.
- **Criterio de cierre:** el archivo existe en `_phases/`, no lleva ningun dato propio del proyecto
  ni ningun codigo instanciado, y tiene las ocho secciones de un archivo de etapa.

**Verificacion — los cuatro controles sobre el archivo nuevo:**

```
$ grep -rnE "RaindomAI|RaidomAI|Proyectos_TripleS|github.com" .claude CLAUDE.md _phases _methodology _templates _workflow ; echo "exit=$?"
exit=1

$ grep -nE '(N|T|D|A|C)-[0-9]{3}|F-[0-9]{3}|L-[0-9]+|S-[0-9]+|R-[0-9]+' _phases/010_prototype.md ; echo "exit=$?"
exit=1

$ grep -c "^## " _phases/010_prototype.md
8

$ sed -n '/^## 6. Condicion de salida/,/^### /p' _phases/010_prototype.md | grep -c "^- \[ \]"
7
```

📌 **El primer control es el Paso 1b del cierre, corrido sobre las seis carpetas copiables**, no
solo sobre el archivo nuevo: lo que interesa no es que el archivo este limpio, sino que **el
conjunto copiable siga estandolo** despues de anadirle una pieza. El segundo si esta acotado al
archivo nuevo, y busca codigos con numero —los que delatarian una instancia de este proyecto— sin
tocar las formas genericas `N-XXX` / `T-XXX`, que son las correctas.

---

### T-044 - Cerrar los enganches de la etapa del prototipo: agnosticismo, carpeta y puntero de `PI-5`
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Alta |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | usuario |
| Sesion | S-012 |

- **Que:** el usuario pidio revisar que `_phases/010_prototype.md` fuera agnostico del todo, fijo la
  carpeta de entregables, y pidio revisar que mas habia que actualizar. Cuatro cambios:

| Donde | Que se hizo |
|---|---|
| `_phases/010_prototype.md` | **dos fugas de estado de este proyecto** reescritas en condicional: la cabecera afirmaba que el archivo «se escribio por adelantado», y §5 decia «**Hoy** esas plantillas no existen». Las dos serian falsas en otro proyecto |
| `_phases/010_prototype.md` | paralelismo con la etapa anterior: `_templates/010_prototype/` y `_workflow/010_prototype.md` escritos con nombre, no en vago |
| `CLAUDE.md` | **`PI-5` gana el puntero de la excepcion** — ver abajo, es `L-007` |
| `project.md` | la carpeta `010_prototype/` en «Carpetas propias» y en «Rutas», con la convencion de nombres (`D-061`) |

- **`L-007`, incumplida por quien la tenia escrita:** `D-059` abrio una excepcion a `PI-5` y la
  escribio **solo** en el archivo de etapa. `CLAUDE.md` seguia diciendo «No hay una tercera casilla»
  en absoluto — el mismo defecto que `F-007` en su dia. Se corrigio en la misma sesion, y el puntero
  se escribio **en generico** («una etapa cuyo producto es deliberadamente descartable»), sin nombrar
  ninguna etapa, para que `CLAUDE.md` siga siendo copiable.
- **Por que:** un archivo de `_phases/` que afirme el estado de un proyecto deja de servir para el
  siguiente, que es la unica razon de que sea agnostico. Y una carpeta de entregables sin declarar
  convierte «lo dice `project.md`» en una referencia a nada.
- **Criterio de cierre:** el archivo no contiene ningun dato ni estado propio del proyecto; `PI-5`
  cita su excepcion; `project.md` declara la carpeta y el control de carpetas del cierre solo señala
  diferencias con razon escrita.

**Verificacion — los cuatro controles:**

```
$ grep -rnE "RaindomAI|RaidomAI|Proyectos_TripleS|github.com" .claude CLAUDE.md _phases _methodology _templates _workflow ; echo "exit=$?"
exit=1

$ grep -nEi 'hoy|todavia no existen|no ha empezado|aun no' _phases/010_prototype.md ; echo "exit=$?"
exit=1

$ grep -n "Hay una sola excepcion posible" CLAUDE.md
64:⚠️ **Hay una sola excepcion posible, y no se decide aqui: la declara un archivo de etapa.** Una

$ grep -c "_templates/010_prototype/\|_workflow/010_prototype.md" _phases/010_prototype.md
3
```

📌 **Son `3` y no `2` porque `_workflow/010_prototype.md` se nombra dos veces** —en §4, donde se
manda leerlo antes del Paso 1, y en §5, donde se declara condicion de entrada—. El numero se
publico primero como `2` y el Paso 2d del cierre lo corrigio antes de commitear.

⚠️ **El segundo control busca marcas de estado, no las agota.** Un archivo puede afirmar el presente
de un proyecto sin usar ninguna de esas palabras; el barrido atrapa las formas que ya fallaron aqui,
y la relectura sigue siendo lo que decide. La frase «en este proyecto» sobrevive a proposito: ahi
significa *el proyecto que lea este archivo*, y es la misma forma que usa la etapa anterior.

---

### T-045 - Anotar el recuento del bloque de `T-041`, que su commit no sostiene (`F-032`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-013 |

- **Que:** el bloque de verificacion de `T-041` publica `_persistence/progress.md:2` y afirma cuatro
  notas fechadas; sobre su propio commit son `1` y `3`. Se anota con nota fechada al lado —sin
  reescribir el bloque (`D-019`)— con el recuento real anclado a `7f55389` y a `265bfeb`, y con la
  explicacion de por que falta la cuarta.
- **Por que:** es la **octava** repeticion del mismo defecto, y ocurrio en la sesion que creo el
  control para impedirlo, sobre la tarea que corregia el septimo caso. Dejarlo sin anotar seria
  publicar un estado que el commit no sostiene — justo lo que `F-031` señalaba.
- **Lo que NO se hizo, y se dice para que no parezca olvido:** no se tocaron las frases de
  `_persistence/progress.md` §2 ni de `_audit/S-011.md` que tambien dicen «los cuatro sitios». La
  primera vive en una seccion que el cierre reescribe —es `L-015`, y corregirla ahi no seria
  corregirla— y la segunda es un informe de sesion cerrado, que no se reescribe (`D-040`). La nota
  de esta ficha las acota nombrandolas.
- **Criterio de cierre:** el bloque de `T-041` lleva su nota fechada, con el recuento anclado a un
  commit y con el numero real de notas.

**Verificacion — el recuento real, anclado a los dos commits:**

```
$ for f in _persistence/decisions.md _persistence/progress.md _audit/S-011.md; do echo -n "$f: "; git show 7f55389:$f | grep -c 'Nota del 2026-09-02 (`T-041`, hallazgo `F-031`)'; done
_persistence/decisions.md: 1
_persistence/progress.md: 1
_audit/S-011.md: 1

$ git show 265bfeb:_persistence/progress.md | grep -c 'Nota del 2026-09-02 (`T-041`, hallazgo `F-031`)'
1
```

---

### T-046 - Exigir en el Paso 2d la lista completa de ordenes sin ancla (`F-032`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Alta |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-013 |

- **Que:** el Paso 2d de `protocol-close` gana un parrafo que obliga a **publicar la lista completa**
  que devuelve su primera orden, con su recuento, y el resultado de reejecutar cada linea. Lo fija
  `D-063`.
- **Por que:** el Paso 2d se corrio en `S-012` —asi lo dice `T-042`— y aun asi `F-032` paso. La
  evidencia publicada pegaba **cinco** lineas; la misma orden sobre el commit devuelve varias
  decenas, y la que fallaba estaba entre las que no se pegaron. **Un control que se documenta sobre
  una parte de su propia salida no es el control**: es una muestra, y elegida por quien se examina.
- **Lo que esto no arregla:** el paso sigue siendo un cedazo. No ve una orden escrita en prosa ni
  una sin el prefijo `$ `, y su propio archivo ya lo declara. Lo que cambia es que **la parte
  mecanizable deja de depender de que quien la corre elija bien que pegar**.
- **Criterio de cierre:** el Paso 2d exige por escrito la lista completa y el recuento, y nombra el
  caso que lo motivo.

**Verificacion — el texto nuevo existe, y el recuento real de la orden sobre el commit auditado:**

```
$ grep -n "la lista COMPLETA" .claude/skills/protocol-close/SKILL.md
273:🚨 **Y la evidencia de este paso publica la lista COMPLETA de su primera orden, nunca una

$ git show 7f55389 -U0 -- _persistence _audit | grep -E '^\+\$ ' | grep -vE 'git (show|grep|log|diff) [0-9a-f]{7,40}' | wc -l
28
```

⚠️ **La auditoria `R-012` publica `26` para esa misma orden sobre el mismo commit, y aqui sale
`28`.** No se corrige ninguno de los dos numeros: se deja constancia de que **la orden no es estable
entre entornos** —dos de las lineas son `git grep ... <hash> -- <ruta>`, el falso positivo que el
propio Paso 2d ya documenta, y su recuento depende de como se expanda el patron en cada shell—. Es
una razon mas para publicar la lista y no solo la cifra: **una lista se puede comparar linea a
linea; un numero solo se puede creer.**

---

### T-047 - Acotar la frase de cierre de `D-060` a lo que su orden prueba (`F-033`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-013 |

- **Que:** la ultima nota de `D-060` justifica sus dos ordenes diciendo que `project.md` «no nombra
  la etapa nueva en ningun sitio». Es falso sobre el mismo commit: hay tres menciones, todas de la
  carpeta de entregables que declara `D-061`. Se acota con nota fechada al lado, sin reescribir
  (`D-019`).
- **Por que:** la decision es correcta y no cambia; lo que falla es la frase que la respalda. Quien
  lea `D-060` dentro de un mes encontrara tres menciones y no sabra si la decision sigue vigente o
  si alguien la incumplio. Mismo perfil que `F-027`: la orden se sostiene, la lectura en prosa no.
- **Criterio de cierre:** `D-060` lleva su nota fechada, y lo que afirma es lo que su orden prueba
  —que la tabla «Etapas» sigue teniendo dos—, no que el archivo no nombre la carpeta.

**Verificacion — las tres menciones, y la fila que si prueba lo que la decision afirma:**

```
$ git show 265bfeb:project.md | grep -n "010_prototype"
37:| Entregables de `010_prototype` | `010_prototype/` (el codigo descartable, en una subcarpeta suya) |
150:| `010_prototype/` | **Los entregables de la etapa `010_prototype`**: los cinco artefactos de registro en su raiz, y el codigo descartable del prototipo en una subcarpeta suya. Se archiva o se borra al cerrar su Gate — **no se muda a ninguna carpeta de producto** |
170:- **`010_prototype/`** esta **declarada por adelantado y todavia no existe en el arbol**, porque su

$ git show 265bfeb:project.md | grep "| Etapas declaradas |"
| Etapas declaradas | `000_preproject`, `005_discovery` |
```

---

### T-048 - Escribir las plantillas de `_templates/010_prototype/`
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Alta |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | usuario |
| Sesion | S-013 |

- **Que:** el usuario aporto cinco archivos en su carpeta de trabajo, procedentes de otro proyecto,
  como material para las plantillas de la etapa del prototipo. Se adaptan y nacen las cinco
  plantillas de `_templates/010_prototype/`, una por artefacto de `_phases/010_prototype.md` §5.
- **Por que ahora:** las plantillas y el archivo de reparto de `_workflow/` son **condicion de
  entrada** de la etapa, no trabajo de dentro de ella. Sin ellas la etapa no puede abrirse aunque
  sus cinco entradas esten completas — se construiria sin forma acordada para registrar lo que se
  observe. `R-012` lo anoto como recomendacion sin hallazgo: nada en `tasks.md` lo agendaba.
- **Que hubo que cambiar, y no fue cosmetico:** ver `D-064`. Lo mas caro no fueron las rutas: fue
  que el material traia una cifra de participantes que la guia de metodo no respalda, y referencias
  a una etapa de Gate que este proyecto no ha declarado.
- **Lo que esto NO hace:** no adopta la etapa `010_prototype`, que sigue sin fila en la tabla
  «Etapas» de `project.md` (`D-060` vigente). Y **no cierra la condicion de entrada**: falta
  `_workflow/010_prototype.md`, que no se escribio hoy.
- **Criterio de cierre:** las cinco plantillas existen, no llevan ningun dato propio de este
  proyecto ni ningun codigo instanciado, y no queda residuo del proyecto de origen.

**Verificacion — los cinco controles sobre la carpeta nueva:**

```
$ ls _templates/010_prototype/
005_happy_path.md
010_participants.md
015_session_NNN.md
020_observations.md
025_business_validation.md

$ grep -rnE "RaindomAI|RaidomAI|Proyectos_TripleS|github.com" .claude CLAUDE.md _phases _methodology _templates _workflow ; echo "exit=$?"
exit=1

$ grep -rnE "(N|T|D|A|C|I|F|L|S|R|DT)-[0-9]+" _templates/010_prototype/ ; echo "exit=$?"
_templates/010_prototype/005_happy_path.md:107:🔑 **Esa es tambien la forma en que esta etapa cumple `PI-5`.** El archivo de etapa declara la unica
exit=0

$ grep -rniE "(^|[^0-9])_prototype/|_memory/|015_gate1|terminal (ejecutora|auditora)|sponsor|020_baseline|minimo 3|recomendado 5|SUP-|RES-" _templates/010_prototype/ ; echo "exit=$?"
exit=1

$ LC_ALL=C.UTF-8 grep -rnP "[\x{00e1}\x{00e9}\x{00ed}\x{00f3}\x{00fa}\x{00c1}\x{00c9}\x{00cd}\x{00d3}\x{00da}]" _templates/010_prototype/ ; echo "exit=$?"
exit=1
```

📌 **El tercero devuelve una linea y no cero, y es correcta:** `PI-5` es el nombre de un
principio de ingenieria, no un codigo instanciado de este proyecto. El patron busca codigos con
numero —los que delatarian una instancia— y `PI-5` cae dentro por la forma, no por el fondo. Se
publica la linea en vez de afinar el patron para que desaparezca: **un control que se ajusta hasta
no devolver nada deja de ser un control.**

📌 **El cuarto es el barrido de residuos del proyecto de origen**, y su patron esta escrito
para no confundirse con las rutas propias: `_prototype/` solo cuenta cuando **no** va precedido de un
digito, porque `010_prototype/` lo contiene como subcadena. El quinto busca vocales acentuadas, que
la convencion de este repositorio no usa y que el material de origen si traia.

---

### T-049 - Publicar la lista completa del Paso 2d que `S-013` afirmo y no publico (`F-034`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-014 |

- **Que:** nota fechada al lado de la seccion 6 de `_audit/S-013.md` —sin reescribir el parrafo
  original (`D-019`)— que diga que la lista completa **no** se publico en ningun archivo del commit,
  y que publique ahora esa lista entera con su recuento, anclada al rango equivalente a `8eb8666`.
- **Por que:** `F-034`. El informe afirmo haber cumplido `D-063` y remitio a la verificacion de
  `T-046`, donde hay dos ordenes y ninguna es la primera del Paso 2d. Es «se comprobo» sin la prueba
  —lo que `CLAUDE.md` prohibe—, y encima sobre el control que nacio ese dia para impedirlo.
- **Criterio de cierre:** la nota existe al lado del parrafo original, el original no cambio, y la
  lista publicada reproduce sobre el rango anclado.

**Verificacion — la lista reproduce sobre el rango anclado, y el original no se toco:**

```
$ git diff 265bfeb 8eb8666 -U0 -- _persistence _audit | grep -E '^\+\$ ' | grep -vE 'git (show|grep|log|diff) [0-9a-f]{7,40}' | wc -l
13

$ git diff 265bfeb 8eb8666 -U0 -- _persistence _audit | grep -E '^\+\$ ' | grep -vE 'git (show|grep|log|diff) [0-9a-f]{7,40}' | sort -u | wc -l
10

$ git diff --numstat -- _audit/S-013.md
35      0       _audit/S-013.md
```

📌 **El `35 0` es la prueba de que no se reescribio nada:** treinta y cinco lineas insertadas, cero
borradas. La lista entera esta en la nota, no aqui, porque su sitio es el archivo que hizo la
afirmacion.

📌 **`nueve` no se reproduce con ningun criterio:** ni las apariciones (`13`) ni las ordenes
distintas (`10`). `R-013` publico los mismos dos numeros en su entorno, asi que la diferencia no es
del entorno esta vez — la cifra del informe no salio de esta orden.

---

### T-050 - Dar sitio fijo a la evidencia del Paso 2d en el informe de sesion (`F-034`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Alta |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-014 |

- **Que:** dos inserciones en `.claude/skills/protocol-close/SKILL.md`. En el Paso 2d, el parrafo que
  dice **donde** aterriza la lista completa; en la estructura del informe, la seccion 7 nueva con sus
  huecos.
- **Por que:** la mitad de fondo de `F-034`. `D-063` dice que publicar y no donde, y una evidencia
  sin sitio asignado desaparece con la sesion sin que nada chille. Queda decidido en `D-065`.
- **Criterio de cierre:** las dos inserciones existen, el diff de la skill es solo insercion, y
  ningun informe ya escrito cambia.

**Verificacion — las dos inserciones, y el diff sin borrados:**

```
$ grep -n "seccion 7 del informe" .claude/skills/protocol-close/SKILL.md
280:🚨 **Y esa lista tiene un sitio fijo: la seccion 7 del informe de `_audit/S-XXX.md`, y no la

$ grep -n "^## 7. Evidencia del Paso 2d" .claude/skills/protocol-close/SKILL.md
694:## 7. Evidencia del Paso 2d

$ git diff --numstat -- .claude/skills/protocol-close/SKILL.md
15      0       .claude/skills/protocol-close/SKILL.md
```

📌 **`protocol-audit` no se toca, y es deliberado.** Su Control e reejecuta las ordenes sin ancla por
su cuenta; que ahora el cierre publique tambien su propia lista no cambia lo que el auditor tiene que
hacer, y hacerlo depender de la seccion 7 convertiria la verificacion independiente en una lectura de
lo que el auditado eligio pegar.

---

### T-051 - Escribir el reparto de trabajo de la etapa del prototipo
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Alta |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | usuario |
| Sesion | S-014 |

- **Que:** escribir `_workflow/010_prototype.md`, derivado de `_workflow/team.md` y
  `_workflow/ai_levels.md`, con una fila por cada uno de los nueve pasos de
  `_phases/010_prototype.md` §4 y alineado con las cinco plantillas de `_templates/010_prototype/`.
- **Por que:** es **condicion de entrada** de la etapa, junto con las plantillas
  (`_phases/010_prototype.md` §5): sin el, la etapa no se abre aunque las cinco entradas esten
  completas. `R-013` lo dejo como recomendacion sin hallazgo tras escribirse las plantillas en
  `S-013`; el usuario lo pidio hoy. Lo decidido queda en `D-066`.
- **Criterio de cierre:** el archivo existe, tiene una fila por paso, la etapa lo cita, no lleva
  ningun dato propio del proyecto ni ningun codigo instanciado.

**Verificacion — los cuatro controles sobre el archivo nuevo:**

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
```

📌 **El cuarto devuelve cero y el archivo hermano devuelve una linea.** La diferencia esta declarada
en `D-066` con su orden: `_workflow/005_discovery.md` cita `L-014`, un codigo instanciado, y no se
toca por esta tarea (`PI-3`). Se deja escrito para que no se lea como que los dos archivos pasan el
mismo control.

📌 **Lo que esta tarea NO hace:** no adopta la etapa ni reparte nada. `_workflow/team.md` §8 dice que
leer la tabla no reparte; el reparto es el `D-XXX` que se escriba **al abrir la etapa**, con lo que
se adopta y lo que se descarta de estas tablas.

---

### T-052 - Montar el Gate 1 (agente `gate1_auditor` y skill `protocol-gate1`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Alta |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | usuario |
| Sesion | S-015 |

- **Que:** el usuario trajo un borrador (`temporal/015_gate1.md`) para el Gate 1 y pidio construir
  su archivo de etapa. Al contrastarlo con `_methodology/000_method.md` §28-§32 se decidio que el
  Gate 1 no es una etapa (`D-067`) y se monto como agente y skill: nace
  `.claude/agents/gate1_auditor.md`, `.claude/skills/protocol-gate1/SKILL.md` y
  `_templates/015_gate1/005_verdict.md`. El dictamen tecnico y la decision de inversion quedan
  separados (`D-068`); se adopta `NO AUDITABLE` como tercer resultado y `NO COMPROBABLE` como
  tercer valor de criterio, no contemplados por la guia de metodo (`D-069`); los dictamenes son
  correlativos y no se sobrescriben (`D-070`). `project.md` y `_phases/010_prototype.md` quedan
  actualizados: el primero declara el Gate y su reparto de autoridad; el segundo ancla el lanzamiento
  del Gate como ultimo paso obligatorio de la etapa del prototipo. Nace `L-021`, sobre el barrido de
  fuga con `git grep` corrido antes de versionar los archivos nuevos.
- **Por que:** condicion para poder cerrar la etapa `010_prototype` con una revision independiente,
  y para que el limite conocido del auditor lanzado por el auditado —`report_auditor`, `A-001`— no se
  repita sin antidoto en el Gate.
- **Criterio de cierre:** el par agente/skill existe, `_phases/010_prototype.md` lo cita como ultimo
  paso obligatorio, y ninguno de los archivos nuevos filtra datos propios del proyecto.

**Verificacion — el par existe y la fuga es cero (reejecutado en el cierre, `grep -r` por L-021):**

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

$ grep -rnE "RaindomAI|RaidomAI_App|C:\\Users\\USUARIO|github\.com" .claude CLAUDE.md _phases _methodology _templates _workflow ; echo "exit=$?"
exit=1
```

📌 **Los detalles de diseno del Gate —las dos firmas, el tercer resultado, la correlatividad de los
dictamenes— quedan en `D-067` a `D-070`, no repetidos aqui.**

---

### T-053 - Corregir la procedencia de la seccion 7 de `S-014` y derivarla del diff (`F-035`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-016 |

- **Que:** nota fechada al final de la seccion 7 de `_audit/S-014.md` (`D-019`, sin reescribir el
  bloque original) con la procedencia real de las diecinueve apariciones, derivada del diff. Y el
  fondo: la seccion 7 del Paso 2d de `protocol-close` pasa a exigir que esa procedencia **se derive
  del diff con su orden y su salida cruda**, no que se escriba a mano mirando los bloques.
- **Por que:** la seccion 7 nacio para cerrar `F-034`, cuyo defecto era «el informe remite a un
  sitio donde la evidencia no esta». La lista ya no faltaba, pero el puntero de tres de sus lineas
  volvia a apuntar a donde no estaban.
- **Criterio de cierre:** la nota existe en `_audit/S-014.md`, y `protocol-close` publica la orden
  que deriva la procedencia.

**Verificacion — la procedencia real, y el enganche en el protocolo:**

```
$ git diff ca56b93^ ca56b93 -U0 -- _persistence _audit ":(exclude)_audit/S-014.md" | awk '/^\+\+\+ /{f=$2} /^\+\$ /{print f" :: "$0}' | grep -vE 'git (show|grep|log|diff) [0-9a-f]{7,40}' | sed 's|^b/||' | awk -F' :: ' '{print $1}' | sort | uniq -c
      3 _audit/findings.md
      8 _persistence/decisions.md
      8 _persistence/tasks.md

$ grep -c "esa procedencia se deriva del diff" .claude/skills/protocol-close/SKILL.md
1

$ grep -c "Nota del 2026-09-03 (\`T-053\`, hallazgo \`F-035\`)" _audit/S-014.md
1
```

---

### T-054 - Reescribir en forma generica la cita instanciada de `_workflow/005_discovery.md` (`F-036`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-016 |

- **Que:** la unica cita instanciada del archivo —una leccion `L-XXX` nombrada por su codigo— se
  reescribe diciendo lo que la leccion dice, sin el codigo. `_workflow/` vuelve a pasar limpio el
  barrido de codigos instanciados.
- **Por que:** `D-066` declaro el incumplimiento y decidio no tocarlo por `PI-3`, sin dejar `T-XXX`
  ni `DT-XXX`. Aparcado dentro del cuerpo de una decision, no aparecia en ningun indice de trabajo
  pendiente y nada lo traia de vuelta. Se corrige en vez de aplazarse porque el arreglo es una frase
  y no toca ninguna referencia entrante: **aplazarlo costaba mas registro que hacerlo**.
- **Criterio de cierre:** el barrido de codigos instanciados sobre `_workflow/005_discovery.md`
  devuelve `exit=1`.

**Verificacion — cero codigos instanciados en el archivo:**

```
$ grep -nE "(N|T|D|A|C|I|F|L|S|R|DT)-[0-9]+" _workflow/005_discovery.md ; echo "exit=$?"
exit=1

$ grep -nE "(N|T|D|A|C|I|F|L|S|R|DT)-[0-9]+" _workflow/010_prototype.md _workflow/team.md _workflow/ai_levels.md ; echo "exit=$?"
_workflow/team.md:107:validacion» necesita una firma humana que ninguna herramienta puede dar, y `PI-1` —razona antes de
_workflow/team.md:126:contra las carpetas declaradas. Ninguno opina; todos son reproducibles. Es lo que `PI-5` exige
_workflow/team.md:281:donde ya vive todo lo que se elige. Un prefijo mas es coste permanente, y `PI-2` pide lo minimo que
_workflow/team.md:289:`PI-5` no admite una tercera casilla: lo que produce documentacion esta Terminado cuando existe su
_workflow/ai_levels.md:206:🔑 **Esto conecta directamente con `PI-5`.** «Un test escrito para pasar no cuenta» tiene aqui una
_workflow/ai_levels.md:342:4. **El bloque de verificacion** que exige `PI-5`, porque esto es documentacion: la orden ejecutada y
exit=0
```

🚨 **Las seis lineas del segundo barrido son falsos positivos conocidos, y se publican en vez de
filtrarse.** El patron alterna `I` como inicial, y `PI-1`, `PI-2` y `PI-5` la contienen: son los
principios de ingenieria de `CLAUDE.md`, que es un archivo agnostico, no codigos del registro de este
proyecto. **Ninguna es un incumplimiento.** Se dejan a la vista porque un `exit=0` explicado vale mas
que un patron retocado hasta que devuelva cero — el patron retocado tapa el siguiente positivo de
verdad, y nadie lo nota.

---

### T-055 - Resolver la Comprobacion 0 del Gate 1 por orden del grafo, no por fecha (`F-037`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-016 |

- **Que:** el Paso 2 de `protocol-gate1` pasa a resolver las tres lecturas de «antes» con
  `git merge-base --is-ancestor`, y la de «el prototipo no cambio entre sesiones» con un rango
  `$SES1..$SESN`. `%ad` queda declarado como dato informativo. La afirmacion «las fechas del
  historial no se pueden convencer» se sustituye por lo que el mecanismo garantiza de verdad, en el
  skill y en `_templates/015_gate1/005_verdict.md`; en `D-069` va como **nota fechada al lado**, sin
  reescribir la viñeta original. Lo adopta `D-071`.
- **Por que:** `D-069` apoyaba el tercer resultado `NO AUDITABLE` entero en una propiedad que no
  existia: `%ad` se sobrescribe con `GIT_AUTHOR_DATE`, y la Comprobacion 0 habria dado `PASA` sobre
  una hipotesis escrita despues de las sesiones — el caso exacto para el que existe.
- **Criterio de cierre:** ninguna de las lecturas de «antes» decide por `%ad`, y la frase absoluta
  no queda viva en ninguno de los tres sitios.
- **Lo que esta tarea NO toca:** las dos apariciones de la frase en `_persistence/progress.md`
  (lineas 94 y 690-691). Son entradas de la bitacora de sesiones anteriores, escritas por el
  `session-closer`, y registran lo que se creia entonces. Reescribirlas convertiria «faltaba
  evidencia» en «hay evidencia falsa». La correccion vigente vive en `D-071` y en la nota de
  `D-069`; el cierre de esta sesion escribira el estado nuevo en su propia entrada.

**Verificacion — el «antes» ya no se decide por fecha:**

```
$ grep -c "merge-base --is-ancestor" .claude/skills/protocol-gate1/SKILL.md
3

$ grep -rc "imposible de aprobar a posteriori" .claude/skills/protocol-gate1/SKILL.md _templates/015_gate1/005_verdict.md
.claude/skills/protocol-gate1/SKILL.md:0
_templates/015_gate1/005_verdict.md:0
```

---

### T-056 - Dar a la Comprobacion 0 forma de localizar la subcarpeta del prototipo y salida si no existe (`F-038`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-016 |

- **Que:** el Paso 2 de `protocol-gate1` localiza la subcarpeta del prototipo con
  `git ls-tree -d --name-only HEAD <PROTO>/` en vez de esperar un valor que `project.md` no declara,
  y dice que emite si no la encuentra: **`NO AUDITABLE`**, no `NO COMPROBABLE`. El Paso 0 queda
  acotado en el mismo sentido, para que su regla general no contradiga a la Comprobacion 0.
- **Por que:** dos de las siete lecturas dependian de ese valor, y la salida que el Paso 0 daba para
  un valor no declarado —`NO COMPROBABLE`— no es un resultado que la Comprobacion 0 admita.
- **Criterio de cierre:** el skill no usa ningun marcador sin resolver para la subcarpeta, y los dos
  vocabularios quedan separados por escrito.

**Verificacion — el marcador desaparecio y la salida esta escrita:**

```
$ grep -c "subcarpeta del prototipo>" .claude/skills/protocol-gate1/SKILL.md
0

$ grep -n "ls-tree -d --name-only" .claude/skills/protocol-gate1/SKILL.md
136:PROTO_DIR=$(git ls-tree -d --name-only HEAD <PROTO>/)

$ grep -c "Esa salida es para los criterios del Paso 4, no para la Comprobacion 0" .claude/skills/protocol-gate1/SKILL.md
1
```

---

### T-057 - Escribir el reparto y las plantillas de la etapa de la baseline
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | manager |
| Sesion | S-016 |

- **Que:** `_workflow/020_baseline.md` —el reparto Humano/Software/IA de los pasos de la etapa— y la
  subcarpeta `_templates/020_baseline/` con una plantilla por artefacto.
- **Por que:** `_phases/020_baseline.md` (`D-072`) declara los dos como **condicion de entrada** de
  la etapa, igual que `_phases/010_prototype.md` §5 hace con los suyos. Escribir la tarea ahora es lo
  que impide que la condicion se descubra el dia que haya que registrar el primer artefacto y no haya
  donde — que es justo el modo en que esa condicion se salta, porque no la señala nadie.
- **Criterio de cierre:** los dos existen, `_phases/020_baseline.md` los cita, y ninguno filtra datos
  propios del proyecto ni codigos instanciados.
- **Cuando:** antes de abrir la etapa, no antes de adoptarla. Adoptar las etapas posteriores es
  trabajo de `005_discovery` (`T-002`), y mientras esa decision no exista esta tarea no tiene urgencia.
- **En que punto quedo (S-017):** las nueve plantillas de `_templates/020_baseline/` ya existen
  (`D-073`, `D-074`), numeradas por orden de procedimiento y agnosticas — sin datos propios del
  proyecto y sin codigos instanciados del registro mas alla del primero que la convencion de
  `_templates/` permite (`N-001`, ya usado por las otras dos carpetas de plantillas). Sigue faltando
  `_workflow/020_baseline.md`, el reparto Humano/Software/IA de los pasos de la etapa: la tarea
  **no** se marca `Implementada`, porque el criterio de cierre pide los dos.

  > 📌 **Nota del 2026-09-03 (`T-062`, hallazgo `F-041`).** El parrafo de arriba **no se reescribe**,
  > y esta nota lo acota. «Sin codigos instanciados del registro mas alla del primero» descansa en el
  > bloque de verificacion de `D-073`, cuyo patron es **ciego a los prefijos de dos letras**: no
  > reconoce `FT-001` ni `SC-001`. La frase sigue siendo cierta de los codigos del **registro**; no
  > lo es de la carpeta entera, que es como se lee. Con el patron ampliado aparecen `FT-003`,
  > `SC-003` (dos veces), `SC-007` y `FT-004`, y esos no son «el primero»:
  >
  > ```
  > $ grep -rnoE "\b(FT|SC|VS|TC|ADR)-[0-9]{3}\b" _templates/020_baseline/ | grep -vE "(FT|SC)-00[12]"
  > _templates/020_baseline/015_features.md:72:FT-003
  > _templates/020_baseline/020_scenarios.md:72:SC-003
  > _templates/020_baseline/025_specification.md:236:SC-003
  > _templates/020_baseline/045_traceability.md:200:SC-007
  > _templates/020_baseline/045_traceability.md:200:FT-004
  > ```
  >
  > `FT-` y `SC-` quedan declarados en `project.md` por `D-075` (hallazgo `F-040`), asi que dejan de
  > ser codigos sin declarar; lo que esta nota corrige es el **alcance de la afirmacion**, no el
  > contenido de las plantillas.

- **En que punto quedo (S-018):** nace `_workflow/020_baseline.md`, y con el la tarea queda
  `Implementada`: los dos artefactos existen, `_phases/020_baseline.md` los cita como condicion de
  entrada, y ninguno filtra datos propios ni codigos instanciados fuera de lo que la convencion de
  `_templates/` permite. El reparto que el archivo describe **no queda adoptado por existir**: eso
  exige su `D-XXX` el dia que la etapa se abra (`_workflow/team.md` §8).
- **Correccion colateral, y se dice:** `_phases/020_baseline.md` citaba el reparto como «el archivo
  de esta etapa en `_workflow/`», sin nombrarlo — y los dos archivos de etapa hermanos si lo nombran.
  Con la cita generica, la segunda orden del bloque de verificacion de este archivo no habria
  devuelto nada, que es exactamente el enganche que `DT-002` y `L-014` existen para vigilar. Se
  nombra en los dos sitios donde la etapa lo invoca (§4 y §5). Es un cambio de dos lineas sobre un
  archivo ya auditado, dentro del criterio de cierre de esta tarea —«`_phases/020_baseline.md` los
  cita»— y no fuera de el.
- **La eleccion de fondo del archivo va aparte:** por que esta etapa puntua «variabilidad de la
  entrada» en 2 y no en 3, cuando las dos anteriores tuvieron que declarar discrepancia por ese
  mismo eje, esta en `D-076` con sus alternativas descartadas.

**Verificacion — los dos artefactos existen, la etapa los cita por nombre, y el archivo nuevo tiene
una fila por paso sin fugas ni codigos instanciados:**

```
$ ls -1 _workflow/
005_discovery.md
010_prototype.md
020_baseline.md
ai_levels.md
team.md

$ grep -cE "^\| \*\*([1-9]|10) · " _workflow/020_baseline.md
10

$ grep -c "^### Paso " _phases/020_baseline.md
10

$ grep -n "_workflow/020_baseline" _phases/020_baseline.md
138:**`_workflow/020_baseline.md`**, que se lee ahora y no despues. Ese reparto se adopta con su `D-XXX`
316:🚨 **Las plantillas y el reparto de `_workflow/020_baseline.md` son condicion de entrada, no trabajo

$ grep -rnE "RaidomAI|Proyectos_TripleS|TripleS|github.com|USUARIO" _workflow/020_baseline.md ; echo "exit=$?"
exit=1

$ grep -rnoE "\b(N|T|D|A|C|I|F|L|S|R|DT|FT|SC|VS|TC|ADR)-[0-9]{3}\b" _workflow/020_baseline.md ; echo "exit=$?"
exit=1
```

---

### T-058 - Escribir el archivo de etapa de la baseline (`_phases/020_baseline.md`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Alta |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | usuario |
| Sesion | S-016 |

- **Que:** nace `_phases/020_baseline.md`, con la misma forma que los dos archivos de etapa que ya
  existian: ocho secciones, lo que autoriza, lo que prohibe, sus entradas, diez pasos de
  procedimiento, sus artefactos, su condicion de salida, lo que registra `manager` y lo que le
  entrega a la etapa siguiente. Se construyo sobre el borrador que trajo el usuario, contrastado
  contra `_methodology/000_method.md` §33-§39 y §46-§50 y contra `_phases/005_discovery.md` y
  `_phases/010_prototype.md`. Lo registra `D-072`, que enumera que se corrigio del borrador al
  portarlo y que se conservo de el.
- **Por que:** el borrador venia de otro esquema de trabajo y traia dentro rutas, prefijos y un
  lector que aqui no existen. Portarlo tal cual habria roto el agnosticismo que el Paso 1b del cierre
  comprueba sobre `_phases/`, y habria metido dos prefijos —los de feature y escenario— que colisionan
  con el hallazgo de auditoria y con la sesion de trabajo.
- **La decision de metodo que la etapa aporta, y no estaba en el borrador:** un Paso 3 que **declara
  en `project.md` los codigos de producto que la etapa estrena, antes de escribir el primero**. Sin
  el, la etapa entera habria escrito identificadores nuevos contra la regla que `project.md` ya tiene
  —un codigo que aparece en un archivo antes que en la tabla es un desfase—, y esta es la etapa que
  mas codigos estrena del metodo.
- **Criterio de cierre:** el archivo existe, no lleva ningun codigo instanciado ni ningun dato propio
  del proyecto, y la tabla «Etapas» de `project.md` **sigue diciendo dos**: escribir el archivo no
  adopta la etapa.

**Verificacion — existe, es agnostico, y no adopta nada:**

```
$ ls -1 _phases/
000_preproject.md
005_discovery.md
010_prototype.md
020_baseline.md

$ grep -nE "(N|T|D|A|C|I|F|L|S|R|DT)-[0-9]{3}" _phases/020_baseline.md ; echo "exit=$?"
exit=1

$ grep -rnE "RaindomAI|RaidomAI|Proyectos_TripleS|github.com" _phases/020_baseline.md ; echo "exit=$?"
exit=1

$ grep -n "Etapas declaradas" project.md
105:| Etapas declaradas | `000_preproject`, `005_discovery` |
```

📌 **El primer patron pide tres digitos a proposito, y conviene decirlo.** Los codigos del registro
se escriben siempre con tres (`T-053`, `D-072`); con `[0-9]+` el mismo barrido devolveria las
menciones de los principios de ingenieria de `CLAUDE.md` —`PI-1`, `PI-5`—, que contienen la inicial
`I` y **no son codigos de este proyecto**. El archivo cita `PI-5` una vez, y esa cita es correcta:
`CLAUDE.md` es agnostico.

```
$ grep -on "PI-5" _phases/020_baseline.md
102:PI-5
```

📌 **El reparto de `_workflow/` y las plantillas de `_templates/` para esta etapa NO se escriben
aqui**: el propio archivo los declara condicion de entrada, y su tarea es `T-057`.

---

### T-059 - Publicar en el Paso 2d el recuento de lineas y la orden que reproduce contra el commit (`F-039`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-017 |

- **Que:** el Paso 2d de `protocol-close` y la plantilla de la seccion 7 del informe pasan a exigir
  tres cosas que antes no decian: que el recuento publicado sea el de **lineas devueltas** y no el de
  ordenes distintas; que la lista vaya **sin deduplicar**; y que la orden se escriba en la forma que
  reproduce contra el commit —anclada al hash y con el propio informe excluido—, o que se diga al
  lado cual es esa equivalencia. Y `_audit/S-016.md` recibe su **nota fechada**, sin reescribir el
  bloque publicado.
- **Por que:** el primer bloque de la seccion 7 de `S-016` publicaba quince lineas y las llamaba
  «Quince lineas», cuando la orden devuelve veintiuna: seis ordenes estan citadas a la vez en
  `decisions.md` y en `tasks.md`, y el bloque estaba deduplicado a mano. Deduplicar es seleccionar, y
  el propio Paso 2d prohibe publicar una seleccion de su salida. Ademas la orden, tal como estaba
  escrita, no reproduce contra el commit: se corrio sobre el area de staging, antes de que el informe
  formara parte del diff.
- **Criterio de cierre:** el skill nombra las dos cifras por separado y pide la forma anclada; la
  nota fechada esta en `_audit/S-016.md` y sus dos ordenes reproducen.

**Verificacion — las dos cifras, la nota y el skill:**

```
$ git diff -U0 bd8a9ff^ bd8a9ff -- _persistence _audit ":(exclude)_audit/S-016.md" | grep -E '^\+\$ ' | grep -vE 'git (show|grep|log|diff) [0-9a-f]{7,40}' | wc -l
21

$ git diff -U0 bd8a9ff^ bd8a9ff -- _persistence _audit ":(exclude)_audit/S-016.md" | grep -E '^\+\$ ' | grep -vE 'git (show|grep|log|diff) [0-9a-f]{7,40}' | sort | uniq | wc -l
15

$ grep -c "Nota del 2026-09-03 (\`T-059\`, hallazgo \`F-039\`)" _audit/S-016.md
1

$ grep -c "El recuento que se publica es el de lineas que devolvio la orden" .claude/skills/protocol-close/SKILL.md
1

$ grep -c "sin deduplicar" .claude/skills/protocol-close/SKILL.md
1

$ grep -c "la orden se publica en la forma que reproduce contra el commit" .claude/skills/protocol-close/SKILL.md
1
```

---

### T-060 - Anotar en `progress.md` la afirmacion absoluta sobre la Comprobacion 0 (`F-037`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-018 |

- **Que:** anotar con una nota fechada la bitacora de `S-015` en `_persistence/progress.md`, que
  publica como hecho que la Comprobacion 0 del Gate 1 esta «resuelta con fechas del historial de
  `git` — la unica comprobacion del metodo imposible de aprobar a posteriori».
- **Por que:** es el **tercero de los tres sitios** que nombraba `F-037`, y el unico que `R-016`
  encontro sin corregir. `T-055` llevo la correccion al skill, a la plantilla del dictamen y a
  `D-069`, pero no aqui; el hallazgo siguio `Aceptado — pendiente` por eso. La afirmacion es falsa
  tal como estaba implementada: `%ad` se sobrescribe con una variable de entorno, y `D-071` ya
  cambio el mecanismo al orden del grafo.
- **Como se hizo:** con una **nota fechada** debajo del parrafo, sin reescribirlo. Es el mismo
  tratamiento que recibio `D-069` en `T-055`, y por la misma razon: `progress.md` es la bitacora de
  lo que se decidio aquel dia, y reescribirla convertiria «falta evidencia» en «hay evidencia falsa».
- **Criterio de cierre:** la nota existe, cita `F-037` y `D-071`, y su bloque de verificacion
  reproduce sobre el commit auditado.

```
$ git show 6b42d0f:.claude/skills/protocol-gate1/SKILL.md | grep -c "merge-base --is-ancestor"
3

$ grep -c 'Nota del 2026-09-03 (`T-060`, hallazgo `F-037`)' _persistence/progress.md
1
```

---

### T-061 - Declarar `FT-` y `SC-` en la tabla «Codigos» de `project.md` (`F-040`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-018 |

- **Que:** añadir `FT-XXX` (feature) y `SC-XXX` (scenario) a la tabla «Codigos» de `project.md`, y
  reescribir el parrafo que decia que de los codigos de producto solo estaban declarados `N-` e `I-`.
- **Por que:** las plantillas de `_templates/020_baseline/` los escriben desde `S-017`, y
  `project.md` dice que un codigo que aparece en un archivo antes que en esa tabla es un desfase.
  Mismo caso que produjo `D-034` (`N-`) y `D-038` (`I-`), repetido sin su `D-XXX`. Lo levanta
  `F-040`, y el hallazgo es correcto.
- **Alcance:** **solo esos dos**. `VS-`, `TC-` y `ADR-` no se declaran: no aparecen instanciados en
  ningun archivo fuera de `_methodology/`, donde son propuesta, y declararlos le quitaria al Paso 3
  de `_phases/020_baseline.md` el contraste contra el registro que es su razon de existir.
- **Criterio de cierre:** las dos filas estan en la tabla, ninguna colisiona con un codigo del
  registro, y la decision con sus alternativas descartadas esta en `D-075`.

```
$ grep -nE '^\| `(FT|SC)-XXX`' project.md
232:| `FT-XXX` | el artefacto de features de `020_baseline` (ruta por declarar: la etapa no esta adoptada) | feature |
233:| `SC-XXX` | el artefacto de escenarios de `020_baseline` (ruta por declarar: la etapa no esta adoptada) | scenario |

$ grep -oE '^\| `[A-Z]+-[A-Za-z]+`' project.md | sort | uniq -d | wc -l
0
```

---

### T-062 - Acotar el alcance del control de codigos instanciados de `D-073` y `T-057` (`F-041`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-018 |

- **Que:** anotar con una nota fechada el bloque de verificacion de `D-073` y el parrafo «En que
  punto quedo (S-017)» de `T-057`, publicando el patron ampliado y su salida real.
- **Por que:** los dos afirman que las plantillas quedan «sin codigos instanciados del registro mas
  alla del primero», y el patron que lo respalda es **ciego a los prefijos de dos letras**: el limite
  de palabra inicial no casa delante de la `F` de `FT`. La afirmacion es cierta de los codigos del
  registro y se lee como un veredicto de toda la carpeta. Misma familia que `F-018` y `L-021`: un
  resultado publicado con su comando, pero con el ambito del comando mas estrecho que la frase.
- **Como se hizo:** notas fechadas, **sin reescribir** ninguno de los dos bloques originales, y
  declarando que de aqui en adelante el control se corre con el patron ampliado a dos letras.
- **Criterio de cierre:** las dos notas existen, publican el patron ampliado, y su salida reproduce.

```
$ grep -rnoE "\b(FT|SC|VS|TC|ADR)-[0-9]{3}\b" _templates/020_baseline/ | grep -vE "(FT|SC)-00[12]"
_templates/020_baseline/015_features.md:72:FT-003
_templates/020_baseline/020_scenarios.md:72:SC-003
_templates/020_baseline/025_specification.md:236:SC-003
_templates/020_baseline/045_traceability.md:200:SC-007
_templates/020_baseline/045_traceability.md:200:FT-004

$ grep -c 'Nota del 2026-09-03 (`T-062`, hallazgo `F-041`)' _persistence/decisions.md _persistence/tasks.md
_persistence/decisions.md:1
_persistence/tasks.md:2
```

📌 **`tasks.md` devuelve 2 y no 1 porque el cuerpo de esta misma tarea cita la cadena.** Se publica
el numero que devuelve la orden, no el que uno esperaba: una nota puesta y la cita de esa nota.

---

### T-063 - Dar deuda registrada a las cinco lineas con `\x08` y corregir el reparto de `L-024` (`F-042`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-018 |

- **Que:** abrir `DT-003` para las cinco lineas del registro que publican ordenes con el caracter de
  retroceso `0x08`, y quitar de `L-024` la frase que remitia la decision a «una auditoria, no
  `manager`».
- **Por que:** dos defectos distintos en la misma viñeta. (1) Un pendiente sin `T-XXX` ni `DT-XXX`
  **no lo mira nadie**: el arranque de sesion lee tareas y deuda, no el cuerpo de las lecciones, y el
  pendiente sale del radar en cuanto `L-024` deje de ser lo ultimo escrito. (2) `project.md` dice
  que `report_auditor` «no construye, no corrige y no decide» — delegar en el la decision la deja en
  un actor que por definicion no puede tomarla.
- **Que NO se hizo, a proposito:** las cinco lineas **no se reescriben**. El argumento de `L-024` es
  correcto y el propio auditor lo respalda en `F-042`: reescribir un bloque antiguo para que exhiba
  una orden que en su dia no se ejecuto asi convierte «falta evidencia» en «hay evidencia falsa». La
  forma de pagar la deuda es anotar cada linea, y eso queda en `DT-003`.
- **Criterio de cierre:** `DT-003` existe con su fila en el indice, la frase de `L-024` esta
  sustituida por una nota fechada que nombra a `DT-003`, y el barrido de caracteres de control
  reproduce.

```
$ grep -c 'lo decide una auditoria' _persistence/lessons.md
0

$ grep -c 'DT-003' _persistence/lessons.md _persistence/techdebt.md
_persistence/lessons.md:1
_persistence/techdebt.md:2
```

---

### T-064 - Corregir en `L-024` el recuento de lineas presentado como apariciones (`F-043`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-018 |

- **Que:** cambiar «el barrido encontro **seis** apariciones» por «**seis lineas** afectadas» en la
  viñeta «Que ocurrio» de `L-024`, y la misma correccion en «las cinco apariciones anteriores», que
  son cinco lineas.
- **Por que:** son veinte apariciones repartidas en seis lineas, y la propia entrada lo dice tres
  parrafos mas abajo. Es el defecto que `F-039` corrigio en ese mismo commit —un recuento publicado
  con el nombre de otra magnitud— reproducido **dentro de la leccion escrita para evitarlo**.
- **Alcance mayor que el del hallazgo, y se dice:** `F-043` solo señalaba la primera frase. La
  segunda tiene el mismo defecto y la misma causa, asi que se corrigen las dos en la misma pasada;
  corregir una y dejar la otra habria dejado la entrada diciendo las dos cosas.
- **Criterio de cierre:** ninguna de las dos frases presenta un recuento de lineas como apariciones,
  y el recuento por apariciones sigue estando, con su nombre.

```
$ grep -nE 'seis lineas|cinco lineas|veinte apariciones|dieciocho apariciones' _persistence/lessons.md
850:  obtiene otro resultado. El barrido que lo destapo encontro **seis lineas** afectadas en el registro
851:  —una de esta sesion, ya reparada, y **cinco anteriores**, que no se tocan—. Son veinte apariciones
852:  del caracter repartidas en esas seis lineas; el recuento por lineas y el recuento por apariciones
869:como `(x10)`; el total del barrido fue **veinte apariciones en seis lineas**. Se dice aqui para que
873:`_persistence/decisions.md:3869`: devuelve **dieciocho apariciones en cinco lineas**, las cinco
887:- **Lo que queda pendiente, y por que no se hizo hoy:** las **cinco lineas anteriores** no se

$ grep -cE '\*\*seis\*\* apariciones|\*\*cinco apariciones' _persistence/lessons.md
0
```

📌 **Seis lineas devueltas, no cuatro.** La orden se publica entera y sin deduplicar (`L-023`,
`F-039`): las dos frases corregidas son la 850 y la 887, y las otras cuatro son el recuento por
apariciones que ya estaba bien y que se conserva.

---

### T-065 - Exigir en la seccion 1 del informe las entradas existentes que el commit edita (`F-044`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-018 |

- **Que:** endurecer la seccion `## 1. Que se hizo` de la plantilla del informe en
  `.claude/skills/protocol-close/SKILL.md`, para que nombre tambien las **entradas ya existentes**
  que el commit edita, no solo las que nacen.
- **Por que:** `S-017` describio `_persistence/lessons.md` unicamente por «`L-024` (nace)», y el
  commit ademas anadio notas de reincidencia a `L-004` y a `L-019`. Mismo defecto que `F-028`. La
  salida pegada dice que **archivos** se tocaron; no dice que **entradas** de dentro, y un archivo de
  registro se edita casi siempre de las dos formas a la vez.
- **Por que importa mas de lo que parece:** una nota anadida a una entrada antigua suele ser la
  evidencia de que algo ya registrado **volvio a fallar**. Es el dato mas util del commit para
  decidir si el mecanismo de lecciones funciona, y es justo el que se pierde.
- **Como se hizo:** dos huecos nuevos en la plantilla —donde se ven cada vez que se escribe la
  seccion, no en un bloque explicativo que se lee una vez— y un apartado con la tabla de contraste y
  la orden de la que sale la lista.
- **Criterio de cierre:** la plantilla lo pide y el bloque explicativo lo desarrolla.

```
$ grep -c 'entradas YA EXISTENTES que el commit edita' .claude/skills/protocol-close/SKILL.md
1

$ grep -c 'no es todo lo que cambia' .claude/skills/protocol-close/SKILL.md
1
```

---

### T-066 - Publicar el recuento real de la seccion 7 de `S-018` y numerar la lista con la orden (`F-045`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-019 |

- **Que:** dos cosas. (1) Nota fechada en la seccion 7 de `_audit/S-018.md` con las cifras que
  devuelve la orden anclada al commit —26 lineas, 23 ordenes distintas, tres repetidas nombradas— y
  con la salida de la orden de la posicion 15, que el informe dejo sin publicar. (2) Endurecer el
  Paso 2d de `protocol-close`: la lista se numera con `cat -n` y las repetidas salen de
  `sort | uniq -d`, nunca marcadas a ojo.
- **Por que:** el Paso 2d existe para que el recuento sea contrastable, y es la pieza que `F-039` y
  `T-059` acababan de reparar. Una cifra falsa en ese sitio no es un detalle: es el unico numero que
  un lector puede comparar sin rehacer el barrido. Y una orden marcada como duplicada de otra que no
  lo es desaparece de la verificacion sin dejar hueco.
- **El informe no se reescribe** (`D-019`): la cifra vieja se queda con su nota al lado. Reescribirla
  convertiria «falta evidencia» en «hay evidencia falsa».
- **Criterio de cierre:** la nota existe en la seccion 7, publica las tres cifras con su orden, y el
  Paso 2d prescribe `cat -n` y `uniq -d`.

```
$ grep -c 'Nota del 2026-09-03 (`T-066`, hallazgo `F-045`)' _audit/S-018.md
1

$ grep -c 'cat -n' .claude/skills/protocol-close/SKILL.md
2

$ grep -c 'nunca a ojo' .claude/skills/protocol-close/SKILL.md
1
```

---

### T-067 - Corregir la atribucion `L-020`/`L-019` en `S-018` y derivar del diff las entradas editadas (`F-046`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-019 |

- **Que:** dos cosas. (1) Nota fechada en la seccion 1 de `_audit/S-018.md`, viñeta de
  `_persistence/lessons.md`, diciendo que la nota de reincidencia cae en `L-019` y no en `L-020`, con
  las dos ordenes que lo derivan del diff. (2) Añadir esas dos ordenes al Paso 6b de
  `protocol-close`, que hasta ahora decia «derivalo del diff» sin decir con que.
- **Por que:** `S-018` es el commit que escribio esa regla (`T-065`, `F-044`) y el que la incumplio.
  Eso no es un defecto de la regla —el auditor lo dice y tiene razon— sino la prueba de que una
  regla que no trae su orden se aplica de memoria. Una atribucion equivocada es peor que la omision:
  quien la comprueba abre `L-020`, no encuentra nada, y concluye que el informe exagera.
- **Alcance mayor que el del hallazgo, y se dice:** `F-046` solo pedia corregir la atribucion. Se
  añade ademas el aviso sobre el borde de la primera orden —un hunk que añade entradas al final de
  otra sale rotulado con la anterior—, porque publicarla sin ese aviso reproduce el mismo defecto
  con otra cara.
- **Criterio de cierre:** la nota existe en la seccion 1, y el Paso 6b lleva las dos ordenes.

```
$ grep -c 'Nota del 2026-09-03 (`T-067`, hallazgo `F-046`)' _audit/S-018.md
1

$ grep -c 'que entrada contiene cada punto tocado' .claude/skills/protocol-close/SKILL.md
1

$ grep -c 'que entradas NACEN' .claude/skills/protocol-close/SKILL.md
1
```

---

### T-068 - Derivar de las tablas el patron del control de codigos instanciados (`F-047`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-019 |

- **Que:** `D-077` — el patron del control deja de escribirse a mano y se deriva de la tabla
  «Codigos» de `project.md` unida a la de §46 de `_methodology/000_method.md`, ordenada de mas largo
  a mas corto, con `(^|[^A-Za-z])` en vez de `` y `[0-9]{2,3}` en vez de `[0-9]{3}`. Nota fechada
  en el bloque de `D-073` diciendo que «el patron ampliado» tampoco cubria `H-`.
- **Por que:** es el tercer punto ciego de la misma serie —`F-041` abrio el segundo—, y el hallazgo
  ofrecia dos salidas: añadir `H` a mano, o declarar que `H-` queda fuera. Las dos dejan intacta la
  causa. `H-nn` ademas tiene dos digitos, asi que el cuantificador tambien fallaba: el punto ciego
  era doble.
- **Se rechaza la salida barata que el propio hallazgo ofrecia**, y queda escrito en `D-077` con sus
  tres alternativas descartadas.
- **Criterio de cierre:** existe `D-077`, la nota fechada esta en `D-073`, y el patron derivado ve
  las veinticinco lineas que las dos alternancias antiguas solo veian en dos pasadas.

```
$ grep -c 'Nota del 2026-09-03 (`T-068`, hallazgo `F-047`)' _persistence/decisions.md
1

$ grep -cE '^### D-077' _persistence/decisions.md
1

$ PAT=$( { sed -n '/^## Codigos/,/^---/p' project.md | grep -oE '^\| `[A-Z]+-[A-Za-z0-9]+`'; sed -n '/^## 46\. Identificadores/,/^```/p' _methodology/000_method.md | grep -oE '^\| `[A-Z]+-[A-Za-z0-9]+`'; } | tr -d '|` ' | sed 's/-.*//' | sort -u | awk '{print length, $0}' | sort -rn | cut -d' ' -f2 | paste -sd'|' - ) && grep -rnoE "(^|[^A-Za-z])(${PAT})-[0-9]{2,3}" _templates/020_baseline/ | wc -l
25
```


---

### T-069 - Escribir el archivo de etapa del esqueleto que camina (`_phases/025_wslt.md`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Alta |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | usuario |
| Sesion | S-019 |

- **Que:** nace `_phases/025_wslt.md`, la quinta etapa del metodo declarada en `_phases/` -el
  esqueleto que camina-, portada desde un borrador propio del usuario (`temporal/025_wslt.md`, de
  otro proyecto) y adaptada al agnosticismo y a los codigos de este repositorio (`D-078`). Ocho
  secciones: que autoriza, que prohibe, entradas, procedimiento en seis pasos, artefactos que
  produce (cinco, con el acta nueva de `T-070`), condicion de salida, que registra `manager`, y que
  entrega a la siguiente etapa.
- **Por que:** el mismo patron que `_phases/010_prototype.md` y `_phases/020_baseline.md`: el
  archivo describe que se hace **si** se entra a la etapa, no que se vaya a entrar. Adoptar la etapa
  sigue siendo trabajo de `005_discovery` (`T-002`).
- **No adopta la etapa** (`D-078`): `project.md` sigue declarando `000_preproject` y
  `005_discovery`, y nada mas.
- **Criterio de cierre:** el archivo existe, es agnostico, no lleva codigos instanciados del
  registro ni del producto, y la tabla «Etapas declaradas» de `project.md` sigue sin tocar.

```
$ ls -1 _phases/
000_preproject.md
005_discovery.md
010_prototype.md
020_baseline.md
025_wslt.md

$ grep -n "Etapas declaradas" project.md
105:| Etapas declaradas | `000_preproject`, `005_discovery` |

$ grep -rnE "RaindomAI|Proyectos_TripleS|github.com" _phases/025_wslt.md ; echo "exit=$?"
exit=1
```

---

### T-070 - Escribir la plantilla del acta del esqueleto (`_templates/025_wslt/005_skeleton_record.md`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | usuario |
| Sesion | S-019 |

- **Que:** nace la plantilla del quinto artefacto de la etapa -el **acta del esqueleto**-, que el
  usuario zanjo que hacia falta (`D-079`) porque un test en verde no demuestra ni que se le vio
  rojo, ni contra que se comprobo desde fuera, ni que rompio el despliegue. Ocho secciones: la
  regla que gobierna el archivo, el camino recorrido, las capas sin simular, el entorno
  reproducible, el despliegue, las tres preguntas minimas, la comprobacion desde fuera y el
  veredicto sobre la arquitectura.
- **Por que:** `_phases/025_wslt.md` exige la plantilla como condicion de entrada de la etapa, igual
  que `020_baseline` exige las suyas. Sin ella la etapa no tendria plantilla que exigir.
- **Criterio de cierre:** la plantilla existe en la subcarpeta `025_wslt/` de `_templates/`, y
  `_phases/025_wslt.md` la cita como condicion de entrada.

```
$ ls -1 _templates/025_wslt/
005_skeleton_record.md

$ grep -c "Acta del esqueleto" _phases/025_wslt.md
1

$ grep -c "son condicion de entrada, no trabajo de" _phases/025_wslt.md
1
```

---

### T-071 - Escribir el reparto de la etapa del esqueleto (`_workflow/025_wslt.md`, `D-080`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Alta |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | manager |
| Sesion | S-019 |

- **Que:** nace `_workflow/025_wslt.md`, el reparto Humano/Software/IA de los seis pasos del
  procedimiento de la etapa, con la rubrica de `_workflow/ai_levels.md` §6 puntuada. El despliegue
  (Paso 4) y el empuje de historial quedan fuera de lo que la IA puede ejecutar, porque
  `_workflow/team.md` §5.1 clasifica esa clase de accion como irreversible; el eje «Impacto de un
  error» puntua **2** de forma condicional a ese reparto, y no 3 (`D-080`). El Paso 3 -codigo del
  esqueleto- si lo escribe la IA, con revision humana de cada tramo.
- **Por que:** es la misma obligacion que `_workflow/020_baseline.md` y `_workflow/010_prototype.md`
  cumplieron para sus etapas: `_phases/025_wslt.md` §3 exige el reparto como condicion de entrada, y
  esta etapa introduce algo nuevo -acciones con efecto fuera del repositorio- que las anteriores no
  tenian.
- **No adopta el reparto** (misma nota que `D-080`): leer estas tablas no reparte nada; repartir es
  el `D-XXX` que se escriba al abrir la etapa, y la etapa no esta declarada.
- **Deja abierto `A-007`:** que habra un humano disponible para ejecutar cada despliegue es un
  supuesto, no un hecho confirmado - registrado aparte porque `D-080` ya se apoya en el.
- **Criterio de cierre:** el archivo puntua la rubrica, deja el despliegue fuera de la IA, declara
  la condicion del eje, y su numero de filas coincide con el numero de pasos del procedimiento.

```
$ grep -c "Variabilidad de la entrada" _workflow/025_wslt.md
1

$ grep -c "ejecuten el despliegue" _workflow/025_wslt.md
1

$ grep -c "El 2 del primer eje es condicional" _workflow/025_wslt.md
1

$ grep -cE "^\| \*\*[1-6] · " _workflow/025_wslt.md
6

$ grep -c "^### Paso " _phases/025_wslt.md
6
```

### T-072 - Publicar en `S-019` la lista completa del Paso 2d y las cifras reales (`F-048`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-020 |

- **Que:** nota fechada en la seccion 7 de `_audit/S-019.md`. El informe declaraba «42 lineas
  devueltas (31 ordenes distintas; hay 11 repetidas)» debajo de una lista **truncada en la posicion
  42**; la orden anclada devuelve **48 lineas y 37 ordenes distintas**. La nota publica las tres
  cifras tomadas de `wc -l`, `sort -u | wc -l` y `sort | uniq -d | wc -l`, las seis posiciones
  omitidas (43 a 48) y la salida de cada una, que el informe original nunca publico.
- **Por que:** es el mismo defecto que `F-045` —recuento falso en la seccion 7 y ordenes sin salida—
  y aparece **en el commit que corrige `F-045`**. Las seis omitidas no son lineas de continuacion
  (esa justificacion vale solo para la 42): son ordenes propias que el filtro si captura, y estaban
  dentro de `DT-004`, ya escrita cuando el informe se redacto.
- **Lo que el informe original hizo bien y aun asi no basto:** el Paso 2d ya exigia numerar con
  `cat -n` y sacar las repetidas de `uniq -d`, y las dos cosas se hicieron. Lo que no impide ese
  remedio es **truncar la lista al pegarla** — de ahi que la nota tome las tres cifras de las
  ordenes en vez de escribirlas al lado.
- **Criterio de cierre:** la nota existe en la seccion 7, publica las tres cifras con su orden
  anclada a `1b30e16`, y las seis posiciones 43-48 tienen su salida.

```
$ grep -c 'Nota del 2026-09-04 (`T-072`, hallazgo `F-048`)' _audit/S-019.md
1

$ git diff -U0 1b30e16^ 1b30e16 -- _persistence _audit ":(exclude)_audit/S-019.md" | grep -E '^\+\$ ' | grep -vE 'git (show|grep|log|diff) [0-9a-f]{7,40}' | wc -l
48
```

### T-073 - Ampliar el ambito y la cifra de `DT-004` con su barrido (`F-049`, `D-081`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-020 |

- **Que:** nota fechada en `DT-004`. La entrada declaraba **siete** lineas nuevas con `0x08` en
  **dos** archivos; el barrido sobre todos los `.md` del commit devuelve **diez** en **cuatro**. Las
  tres no contadas son dos en `_audit/S-018.md` y una en `_audit/S-019.md`. La nota publica los dos
  barridos —el del commit y el del padre, para separar lo nuevo de lo heredado— con su salida cruda.
- **Por que importa mas que la cifra:** las dos de `_audit/S-018.md` caen dentro de la nota fechada
  que corrige `F-045`, y no son prosa: son la transcripcion de la **salida cruda** de dos ordenes.
  La nota que existia para dejar de publicar cifras falsas publica una salida que la orden no
  devuelve.
- **Como se conto mal:** enumerando a mano los archivos que el Paso 6 del cierre tenia delante
  —`decisions.md` y `tasks.md`— en vez de barrer el arbol. Los tres que faltaban estaban en archivos
  tocados al principio de la sesion, que son los que la memoria deja fuera. El remedio de fondo es
  `T-074`.
- **Quien escribe la nota:** `manager`, por `D-081`. `Estado`, `Confirmacion` y el titulo de la
  entrada no se tocan.
- **Criterio de cierre:** la nota existe en `DT-004`, cita `F-049` y `D-081`, y su barrido reproduce.

```
$ grep -c 'Nota del 2026-09-04 (`T-073`, hallazgo `F-049`, decision `D-081`)' _persistence/techdebt.md
1

$ for f in $(git ls-tree -r --name-only 1b30e16 | grep -E '\.md$'); do n=$(git show 1b30e16:"$f" | grep -c $'\x08'); if [ "$n" -gt 0 ]; then echo "$f: $n"; fi; done
_audit/S-018.md: 2
_audit/S-019.md: 1
_audit/findings.md: 1
_persistence/decisions.md: 7
_persistence/tasks.md: 5
```

### T-074 - Anadir al cierre el barrido de caracteres de control (Paso 2e de `protocol-close`, `F-049`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Alta |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-020 |

- **Que:** nace el **Paso 2e** de `protocol-close`, entre el 2d y la seccion de como se escriben los
  archivos. Barre los caracteres de control —excluyendo tabulador, salto de linea y retorno de
  carro— sobre **los archivos que el commit toca**, derivados de `git diff --cached --name-only`, y
  no sobre una lista escrita a mano. Trae su tabla de tres salidas posibles, la orden que separa lo
  nuevo de lo heredado contra `HEAD`, y la exigencia de `cat -A` para que el `^H` se vea. El informe
  gana una **seccion 8** donde publicar su resultado, tambien cuando sale vacio.
- **Por que:** el `0x08` lleva tres sesiones consecutivas apareciendo —`DT-003`, `DT-004` y las tres
  lineas que documenta `F-049`— y las tres veces se detecto a mano y por casualidad. Es `L-008`
  literal: una regla sin mecanismo es una intencion. Lo que faltaba no era saber que el defecto
  existe, sino una orden que lo busque sin que nadie se acuerde.
- **Por que antes del `git add` y no en la auditoria:** commiteado, el defecto ya no se corrige —se
  anota—. Esa diferencia es la unica razon de que el paso viva en el cierre.
- **Alcance que NO cubre:** el patron ve caracteres de control, no errores de transcripcion en
  general. Un bloque que publica una salida distinta de la que la orden devuelve **sin** caracteres
  raros sigue siendo cosa del Paso 2d.
- **Criterio de cierre:** el paso existe con su orden, la estructura del informe tiene su seccion 8,
  y el propio archivo del protocolo pasa su barrido.

```
$ grep -c '^## Paso 2e' .claude/skills/protocol-close/SKILL.md
1

$ grep -c '^## 8. Evidencia del Paso 2e' .claude/skills/protocol-close/SKILL.md
1

$ grep -c $'[\x01-\x08\x0b\x0c\x0e-\x1f]' .claude/skills/protocol-close/SKILL.md
0
```

### T-075 - Aclarar que `025_wslt` es una etapa con tres archivos, no tres etapas (`F-050`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-020 |

- **Que:** nota fechada en dos sitios —la seccion 2 de `_audit/S-019.md` y la entrada `S-019` de
  `_persistence/progress.md`—. Las dos frases decian «las tres etapas nuevas de `025_wslt`»; lo que
  nace son **tres archivos de una sola etapa**, y la orden que los deriva va en la nota.
- **Por que:** `project.md` lleva la cuenta de las etapas declaradas y `T-002` existe para declarar
  las que faltan. Un registro que dice «tres etapas nuevas» donde hay una deja al arranque siguiente
  buscando dos etapas que no existen.
- **Lo que no se toca:** el mensaje del commit y `D-078` ya lo dicen bien; ninguno de los dos textos
  originales se reescribe (`D-019`).
- **Criterio de cierre:** las dos notas existen y su orden reproduce.

```
$ grep -c 'Nota del 2026-09-04 (`T-075`, hallazgo `F-050`)' _audit/S-019.md _persistence/progress.md
_audit/S-019.md:1
_persistence/progress.md:1

$ git diff --name-only --diff-filter=A 1b30e16^ 1b30e16 | grep 025_wslt
_phases/025_wslt.md
_templates/025_wslt/005_skeleton_record.md
_workflow/025_wslt.md
```

### T-076 - Escribir el archivo de etapa del crecimiento (`_phases/030_growth.md`, `D-082`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Alta |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | usuario |
| Sesion | S-020 |

- **Que:** nace `_phases/030_growth.md`, el sexto archivo de `_phases/`, con las mismas ocho
  secciones que sus hermanos. Cubre la etapa que hace crecer el producto colgando unidades
  incrementales de un esqueleto que ya camina: es la mas larga del metodo y **la unica que se
  repite**, con los pasos 2 a 7 por cada slice y los pasos 1 y 8 por cada iteracion.
- **De donde sale:** de un borrador que el usuario dejo en la carpeta temporal del repositorio,
  reescrito para esta metodologia. Se conserva su estructura y sus dos prohibiciones con recuadro
  —el corte horizontal y tocar el test para que pase—; se descarta todo su vocabulario de rutas,
  carpetas y codigos, que era el de otro proyecto (`D-082`).
- **La desviacion que hay que saber leer:** el archivo **no instancia ningun codigo de producto, ni
  siquiera generico**. La guia de metodo asigna a la tarea de producto el mismo prefijo que
  `project.md` ya tiene tomado por la tarea del registro de jornada, y esta es la etapa donde esa
  colision se cobra. El archivo habla en prosa y remite a la tabla «Codigos»; resolver la colision
  es de la etapa de la baseline. Decidido con el usuario antes de escribir.
- **No adopta la etapa** (misma nota que `D-082`): `project.md` sigue declarando `000_preproject` y
  `005_discovery`, y declarar las posteriores es `T-002`.
- **Deja pendientes dos artefactos, y el archivo lo dice:** ni `_templates/030_growth/` ni
  `_workflow/030_growth.md` existen, y su §5 los declara condicion de entrada — igual que hizo la
  etapa del esqueleto con los suyos.
- **Criterio de cierre:** el archivo tiene sus ocho secciones y sus ocho pasos, no filtra ningun dato
  propio del proyecto, no instancia ningun codigo, no lleva caracteres de control, y sus recuentos
  declarados coinciden con lo que contiene.

```
$ grep -c "^## " _phases/030_growth.md
8

$ grep -c "^### Paso " _phases/030_growth.md
8

$ grep -rnE "RaindomAI|RaidomAI|Proyectos_TripleS|TripleS|github.com|USUARIO" _phases/030_growth.md ; echo "exit=$?"
exit=1

$ grep -c $'[\x01-\x08\x0b\x0c\x0e-\x1f]' _phases/030_growth.md
0

$ ls -1 _phases/ | wc -l
6
```

---

### T-077 - Separar las dos cuentas de la seccion 8 de `S-020` (`F-051`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-021 |

- **Que:** nota fechada al final de la seccion 8 de `_audit/S-020.md` que separa las dos cuentas que
  el informe habia igualado: las **catorce** lineas de control presentes en los archivos que el
  commit toca, y las **diez** nuevas de `S-019` que `DT-004` documenta. La nota enumera las tres
  discrepancias concretas y remite a `D-083` por la linea de `_audit/findings.md`.
- **Por que era un hallazgo y no una errata de suma:** el enunciado afirmaba mas de lo que su orden
  devolvia, en la seccion que nacio (Paso 2e, `F-049`) para impedir exactamente eso. La consecuencia
  practica es que una linea real quedaba declarada como deuda ya documentada sin que ninguna entrada
  la documentara.
- **Lo que NO se hizo:** no se reescribio el parrafo original. Se deja tal cual con su nota al lado,
  que es lo que `D-019` fija para el registro ya auditado.
- **Criterio de cierre:** la nota existe en la seccion 8, cita las dos cuentas, y su barrido
  reproduce catorce.

```
$ grep -c 'T-077' _audit/S-020.md
1

$ git diff --name-only --diff-filter=d f09d1f7^ f09d1f7 | while read f; do grep -c $'[\x01-\x08\x0b\x0c\x0e-\x1f]' "$f"; done | awk '{s+=$1} END {print s}'
14

$ grep -c 'diez casos' _audit/S-020.md
1
```

---

### T-078 - Escribir la nota de cierre de la seccion 1 de `S-020` (`F-052`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-021 |

- **Que:** la seccion 1 de `_audit/S-020.md` prometia dos veces una lista de archivos anclada al
  commit, y esa nota nunca se escribio: la unica del informe estaba en la seccion 7. Se pega ahora,
  con `git show --stat --name-only --format= f09d1f7` y su salida cruda.
- **El contenido ya era correcto; lo que faltaba era poder comprobarlo.** Los once archivos coinciden
  con el diff del commit. Lo que la version publicada describia era el area de staging, que ya no
  existe — no reproducible por nadie, que es el defecto entero.
- **Criterio de cierre:** la nota existe en la seccion 1, con la orden anclada y sus once archivos, y
  el informe pasa a tener dos notas de cierre en vez de una.

```
$ grep -c 'Nota de cierre' _audit/S-020.md
2

$ git show --stat --name-only --format= f09d1f7 | grep -c .
11

$ awk '/^## 1\. Que se hizo/,/^## 2\./' _audit/S-020.md | grep -c 'Nota de cierre de la seccion 1'
1
```

---

### T-079 - Anclar la cabecera de `S-020` al hash literal (`F-053`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-021 |

- **Que:** nota fechada bajo la cabecera de `_audit/S-020.md` que fija el hash literal del commit de
  la sesion —`f09d1f7`— y explica que `3ff670e` es un commit de anclaje sin trabajo dentro. El campo
  original no se reescribe: queda superado por la nota.
- **Por que la definicion original fallaba:** no escribia un hash, escribia la orden que lo deriva, y
  esa orden devuelve el ultimo commit que toca el informe. Con dos commits, devuelve el equivocado —
  uno cuyo `--stat` tiene un archivo frente a los once que la seccion 1 enumera.
- **La correccion de fondo va aparte** (`T-081`, `D-084`): el defecto era del protocolo, no del
  informe.
- **Criterio de cierre:** la nota existe, nombra `f09d1f7` como commit de la sesion, y la asimetria
  de los dos `--stat` queda pegada.

```
$ grep -c 'T-079' _audit/S-020.md
1

$ git show --stat --name-only --format= 3ff670e | grep -c .
1

$ git show --stat --name-only --format= f09d1f7 | grep -c .
11
```

---

### T-080 - Corregir en `progress.md` el recuento de etapas sin adoptar (`F-054`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-021 |

- **Que:** las dos vinetas de `_persistence/progress.md` que enumeran las etapas pendientes de
  adoptar nombraban **tres** y son **cuatro**: faltaba `020_baseline`, que tiene archivo de etapa,
  plantillas y reparto. Las dos reciben la misma nota fechada, con la lista derivada de una orden.
- **Por que importa mas de lo que su gravedad sugiere:** de esa enumeracion saca `T-002` cuales son
  las etapas que faltan por declarar. Una etapa que se cae de la lista no produce ningun error
  visible; produce que nadie recuerde declararla.
- **Es la forma exacta de `L-027`/`L-028`:** una lista derivable con una orden, escrita de memoria.
  Por eso la correccion de fondo (`T-082`) no es el numero, sino que el cierre la derive.
- **Criterio de cierre:** las dos vinetas llevan su nota, la orden derivada devuelve cuatro etapas, y
  las cuatro estan nombradas.

```
$ grep -c 'T-080' _persistence/progress.md
2

$ comm -23 <(git ls-tree --name-only f09d1f7 _phases/ | sed 's|_phases/||; s|\.md$||' | sort) <(git show f09d1f7:project.md | grep 'Etapas declaradas' | grep -oE '`[a-z0-9_]+`' | tr -d '`' | sort)
010_prototype
020_baseline
025_wslt
030_growth
```

---

### T-081 - Dar al cierre un paso de anclaje, y al auditor el hash literal (`F-052`, `F-053`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Alta |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-021 |

- **Que, en `protocol-close`:** nace el **Paso 7c**, que despues del push rellena en un unico commit
  de anclaje los **tres** sitios que el informe no podia tener completos mientras se escribia —la
  cabecera, la nota de cierre de la seccion 1 y la de la seccion 7—. La cabecera de la plantilla pasa
  a pedir un **hash literal**, y el protocolo nombra por escrito cual de los dos commits es «el
  commit de la sesion»: el primero, el que lleva el trabajo.
- **Que, en `protocol-audit`:** el auditor deja de fiarse de la orden que deriva el commit. Lee el
  hash literal de la cabecera; si no coincide con el derivado, audita el literal; si la cabecera no
  lleva hash, lo dice y es un hallazgo. Se le da ademas el control que delata un commit de anclaje:
  su `--stat` tiene un solo archivo.
- **Por que las dos skills y no solo una:** anclar bien en el cierre y seguir derivando mal en la
  auditoria deja el defecto entero. El auditor arranca en frio y solo tiene el historial; si nadie le
  dice cual de los dos commits manda, elige el ultimo.
- **La alternativa que se descarto de plano** era hacer un solo commit con `--amend`. El Paso 7 lo
  prohibe sin excepcion, y reescribir un commit ya subido borra el estado que la auditoria dice haber
  juzgado (`D-084`).
- **Criterio de cierre:** el Paso 7c existe con su seccion de los dos commits, la plantilla pide el
  hash literal, y `protocol-audit` tiene su control del commit equivocado.

```
$ grep -nE '^### 7c|^### Cual de los dos' .claude/skills/protocol-close/SKILL.md
1079:### 7c — Anclar el informe al hash (obligatorio)
1095:### Cual de los dos commits es «el commit de la sesion»

$ grep -c 'HASH LITERAL' .claude/skills/protocol-close/SKILL.md
1

$ grep -c 'Esa orden puede devolver el commit equivocado' .claude/skills/protocol-audit/SKILL.md
1
```

---

### T-082 - Que el cierre derive la lista de etapas sin adoptar (`F-054`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-021 |

- **Que:** el Paso 3 de `protocol-close` gana un recuadro que prohibe escribir de memoria cualquier
  lista que una orden pueda producir, y da la orden concreta de la que se equivoca sola en cada
  cierre: las etapas con archivo en `_phases/` menos las declaradas en `project.md`.
- **Por que va en el Paso 3 y no en el 2d:** el Paso 2d vigila que los bloques de verificacion lleven
  ancla; esto es otra cosa — una lista escrita en prosa, sin bloque, que nadie mira porque no parece
  evidencia. `L-028` ya generalizo el principio; esto le da el mecanismo.
- **Criterio de cierre:** el recuadro existe en el Paso 3 con su orden, y la orden devuelve las
  cuatro etapas.

```
$ grep -n 'Lo que enumeres, derivalo' .claude/skills/protocol-close/SKILL.md

$ sed -n '/^## Paso 3 /,/^## Paso 4 /p' .claude/skills/protocol-close/SKILL.md | grep -c 'Etapas declaradas'
1
```

---

### T-083 - Escribir las plantillas de `_templates/030_growth/`
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Alta |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | usuario |
| Sesion | S-021 |

- **Que:** nacen las tres plantillas que `_phases/030_growth.md` §5 nombra por su nombre —el acta de
  iteracion, el acta de slice y la declaracion de la ventana de observacion—, con la misma forma que
  las de las otras etapas: cabecera con estado y fechas, una seccion 0 con la regla que gobierna el
  archivo, secciones que piden salidas crudas y no conclusiones, una comprobacion final con ordenes
  mecanicas, y una guia de llenado marcada para borrar al cerrar el artefacto.
- **Que separa cada una** (`D-085`): la de iteracion conserva **el orden de las slices y su razon**,
  que es lo que el `git diff` nunca muestra; la de slice conserva **el rojo del test y lo que rompio
  por el camino**; la de la ventana conserva **cuando se fijaron metrica, ventana y umbral**, que es
  lo unico que hace que el Gate pueda dar un «no».
- **Las tres se escribieron sin estrenar ningun codigo de producto**, que es la desviacion respecto a
  las plantillas de la baseline y esta razonada en `D-085`: slice, tarea de producto y caso de prueba
  no estan en la tabla «Codigos» de `project.md`, y un codigo citado antes de declararse es un
  desfase. Donde haria falta uno hay un hueco con su recuadro.
- **Lo que NO se hizo:** `_workflow/030_growth.md` sigue sin existir. El usuario pidio las plantillas;
  el reparto exige decidir quien hace cada paso y no es trabajo de plantilla. **La etapa sigue sin
  poder abrirse**, porque su §5 exige los dos, y la nota fechada del archivo de etapa lo dice.
- **Criterio de cierre:** las tres existen con su estructura, no filtran datos propios, no instancian
  codigos, no llevan caracteres de control, y el archivo de etapa lleva su nota fechada.

```
$ ls -1 _templates/030_growth/
005_iteration_NNN.md
010_slice_NNN.md
015_observation_window.md

$ for f in _templates/030_growth/*.md; do echo "$f -> $(grep -c '^## ' "$f") secciones, $(grep -c 'Guia de llenado' "$f") marcas de guia"; done
_templates/030_growth/005_iteration_NNN.md -> 9 secciones, 3 marcas de guia
_templates/030_growth/010_slice_NNN.md -> 9 secciones, 3 marcas de guia
_templates/030_growth/015_observation_window.md -> 8 secciones, 3 marcas de guia

$ grep -rnE "RaindomAI|RaidomAI|Proyectos_TripleS|TripleS|github.com|USUARIO" _templates/030_growth/ ; echo "exit=$?"
exit=1

$ ls _workflow/030_growth.md 2>&1
ls: cannot access '_workflow/030_growth.md': No such file or directory

$ grep -c 'T-083' _phases/030_growth.md
1
```

> 📌 **Nota del 2026-09-06.** Dos de las ordenes de arriba **ya no devuelven lo publicado**, y las
> dos por trabajo posterior, no por error de entonces:
>
> - `ls _workflow/030_growth.md 2>&1` devolvia «No such file or directory» y ahora devuelve la ruta:
>   el archivo de reparto se escribio (ver la tarea del reparto de la etapa del crecimiento).
> - `grep -c 'T-083' _phases/030_growth.md` devolvia `1` y ahora devuelve `0`: esa ocurrencia era el
>   codigo instanciado que la auditoria abrio como hallazgo, y se quito.
>
> El bloque no se toca, por la regla de correccion por nota fechada de `D-019`. Las dos siguen
> reproduciendo ancladas al commit que las contiene:
>
> ```
> $ git show 76a2cb6:_phases/030_growth.md | grep -c 'T-083'
> 1
> ```

---

### T-084 - Quitar los dos codigos instanciados de `_phases/030_growth.md` (`F-055`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-022 |

- **Que:** la cabecera de la nota fechada del §5 del archivo de etapa citaba una tarea y una decision
  con su numero. Eran las **dos unicas ocurrencias de un codigo instanciado en toda `_phases/`**, y
  `CLAUDE.md` exige ahi codigos genericos porque la carpeta tiene que poder copiarse a otro proyecto
  tal cual. Copiada, la nota citaba dos entradas que en el destino no existen.
- **Como:** se reescribe la cabecera dejando solo la fecha. **El bloque de verificacion de la nota no
  se toca** — la cabecera no es evidencia, y la distincion esta razonada en `D-086`.
- **Criterio de cierre:** cero codigos instanciados en el archivo, y cero en las dos carpetas que
  tienen que estar limpias.

```
$ grep -noE '\b(T|D|F|L|A|C|DT|S)-[0-9]{2,3}\b' _phases/030_growth.md; echo "exit=$?"
exit=1

$ git grep -noE '\b(T|D|F|L|A|C|DT|S)-[0-9]{2,3}\b' -- _phases _workflow; echo "exit=$?"
exit=1
```

---

### T-085 - Dar al cierre el control 1c de codigos instanciados (`F-055`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Alta |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-022 |

- **Que:** `T-084` quita la fuga; esto impide que vuelva. Nace el **Paso 1c** de `protocol-close`,
  hermano del 1b: aquel busca datos propios —nombre, ruta, host—, este busca **codigos del registro
  con su numero** dentro de `_phases/` y `_workflow/`.
- **Por que solo esas dos carpetas:** en `.claude/`, `_methodology/`, `_templates/` y `CLAUDE.md` un
  codigo numerado es legitimo —los protocolos citan sus decisiones, el metodo numera ejemplos, y una
  plantilla escribe el primero de su serie porque esa forma es lo que existe para dar—. Ensancharlo a
  las seis lo apagaria: devolveria decenas de lineas correctas cada sesion. Razonado en `D-087`.
- **Y su linea en el reporte de pantalla**, para que un cierre que lo corrio y uno que no se lean
  distinto.
- **Criterio de cierre:** el paso existe en la skill y su linea esta en el bloque de controles.

```
$ grep -n '^### 1c' .claude/skills/protocol-close/SKILL.md
136:### 1c. El control de codigos instanciados

$ grep -c 'Codigos instanciados en' .claude/skills/protocol-close/SKILL.md
1
```

---

### T-086 - Corregir por nota la salida cruda de la nota de `_phases/030_growth.md` (`F-056`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-022 |

- **Que:** la nota del §5 encabezaba su bloque con `ls _workflow/030_growth.md 2>&1` y pegaba debajo
  una salida con **comillas dobles de mas** dentro de las simples, que esa orden no produce. El hecho
  de fondo era cierto —el archivo no existia—; lo pegado no era reproducible, y la comilla delata que
  lo corrido fue `ls "_workflow/030_growth.md"`.
- **Como:** el bloque original **se deja intacto** y se le anade debajo una nota fechada que dice que
  la salida no era la de la orden, y que republica la orden tal como se corre con la salida tal como
  sale. Es `D-019` literal: reescribir la salida vieja convertiria «falta evidencia» en «hay
  evidencia falsa».
- **Y la nota aprovecha para cerrar la otra mitad:** el archivo de reparto ya existe (`T-091`), asi
  que la segunda afirmacion de la nota original —«el reparto sigue sin existir»— tambien queda
  superada, y las dos condiciones de entrada del §5 pasan a estar cumplidas.
- **Criterio de cierre:** la nota nueva existe y su bloque reproduce.

```
$ grep -c 'Nota del 2026-09-06' _phases/030_growth.md
1

$ ls _workflow/030_growth.md 2>&1
_workflow/030_growth.md
```

---

### T-087 - Publicar la salida del criterio de cierre de `D-083` y `D-084` (`F-057`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-022 |

- **Que:** las dos decisiones publicaban su «Criterio de cierre» con **seis ordenes y ninguna
  salida**. Las dos tienen `Origen: report_auditor`, y para esas `CLAUDE.md` exige «la orden ejecutada
  literal **y** lo que devolvio». Un comando sin salida obliga a rehacer el barrido para
  contrastarlo, que es el coste exacto que la regla existe para evitar.
- **Como:** los bloques originales **se dejan intactos** y cada decision recibe una nota fechada con
  las mismas ordenes **ancladas al commit en que se cerro** y su salida literal. Ancladas, porque una
  de ellas —los numeros de linea de `protocol-close`— ya no reproduce sobre el arbol de trabajo: la
  skill ha crecido desde entonces.
- **Un anadido:** el criterio de `D-083` afirmaba tres cosas y su bloque solo publicaba dos ordenes.
  La tercera —la fila del hallazgo citando su tarea— se anade en la nota, porque el enunciado la
  afirmaba.
- **Criterio de cierre:** las dos notas existen y las seis ordenes ancladas devuelven lo publicado.

```
$ awk '/^### D-083/,/^### D-085/' _persistence/decisions.md | grep -c 'Nota del 2026-09-06'
2

$ git show 76a2cb6:_persistence/techdebt.md | grep -c '^### DT-005'
1

$ git show 76a2cb6:_audit/S-020.md | grep -c 'Nota de cierre'
2
```

---

### T-088 - Anotar los huecos de plantilla de `S-021` y darle al cierre su control (`F-058`)
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Baja |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-022 |

- **Que:** dos lineas del informe de la sesion anterior eran la **instruccion de llenado** de la
  plantilla, dejadas encima del contenido en vez de sustituidas por el. No falta evidencia —el hueco
  esta relleno debajo—; lo que queda es un artefacto que mezcla la orden de rellenar con lo
  rellenado, que es el defecto que `CLAUDE.md` persigue en `_templates/`.
- **Como, en dos mitades:** el informe **no se toca** —esta auditado, y quitarle lineas cambiaria lo
  que la auditoria describio—, y recibe su nota fechada. Y `protocol-close` gana en el Paso 6b el
  control que exige **cero lineas `^<`** en el informe **antes** del `git add`, que es el unico
  momento en que borrarlas todavia es correcto. Razonado en `D-089`.
- **Criterio de cierre:** la nota existe en el informe y el control existe en la skill.

```
$ grep -c 'Nota del 2026-09-06' _audit/S-021.md
1

$ grep -n 'Ninguna linea de la plantilla sobrevive' .claude/skills/protocol-close/SKILL.md
1022:### 🚨 Ninguna linea de la plantilla sobrevive en el informe
```

---

### T-089 - Fijar la forma del bloque «Criterio de cierre» en `decisions.md`
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-022 |

- **Que:** viene de una **recomendacion sin hallazgo** de `R-021`, y es la causa de fondo de `F-057`:
  en la misma sesion y en el mismo archivo, una decision publico su criterio de cierre con salida
  cruda y dos no. No habia forma fijada en ningun sitio, asi que dependia de quien escribiera.
- **Como:** las convenciones de `decisions.md` pasan a exigir tres partes siempre —enunciado, orden
  **anclada al commit**, y salida literal— y a decir que un criterio con la orden y sin la salida no
  es evidencia, y que uno sin anclar deja de reproducir en cuanto el archivo crece.
- **Criterio de cierre:** la convencion esta escrita en el archivo.

```
$ grep -n 'que hasta ahora no tenia forma fijada' _persistence/decisions.md
115:🚨 **Y eso incluye el bloque «Criterio de cierre», que hasta ahora no tenia forma fijada.** El
```

---

### T-090 - Que la fila de `_audit/index.md` lleve el hash literal del informe
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | report_auditor |
| Sesion | S-022 |

- **Que:** la otra **recomendacion sin hallazgo** de `R-021`. La fila de una sesion en el tablero
  apuntaba al **commit de anclaje** —un solo archivo— en vez de al commit de la sesion, porque el
  auditor la derivaba con `git log -1 -- _audit/S-XXX.md`. La fila describia con exactitud lo que esa
  auditoria juzgo de hecho, asi que no era hallazgo; pero el tablero es el primer sitio donde alguien
  busca «que estado se juzgo».
- **Como:** `protocol-audit` pasa a decir que el hash de la fila es **el literal de la cabecera del
  informe**, no el derivado, y por que. **No se reescribe ninguna fila anterior:** describen lo que la
  auditoria de su dia miro, y ese defecto ya quedo registrado en su hallazgo. Razonado en `D-090`.
- **Criterio de cierre:** la regla esta escrita en la skill del auditor.

```
$ grep -n 'el literal de la cabecera del informe' .claude/skills/protocol-audit/SKILL.md
275:🚨 **El `<hash>` de esa fila es el mismo que auditaste: el literal de la cabecera del informe, no el
```

---

### T-091 - Escribir el reparto de la etapa del crecimiento
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Alta |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | usuario |
| Sesion | S-022 |

- **Que:** nace `_workflow/030_growth.md`, el quinto y ultimo archivo de reparto por etapa. Con el,
  **las dos condiciones de entrada** que el §5 del archivo de etapa exige —las tres plantillas y el
  reparto— quedan cumplidas: hasta hoy la etapa no podia abrirse aunque sus seis entradas estuvieran
  completas.
- **Como:** la misma forma que los cuatro anteriores —nueve secciones, una fila por paso del
  procedimiento, las asignaciones no obvias razonadas, lo que no se delega, que cuenta como software,
  las casillas de salida separadas en mecanico y juicio, la rubrica de nivel, que se registra, la
  verificacion y los errores frecuentes—. Ocho filas, porque el procedimiento de esta etapa tiene
  ocho pasos.
- **Lo que lo distingue de los cuatro anteriores**, y esta razonado en `D-091`: es la primera etapa
  que **se repite**, asi que el reparto se ejecuta decenas de veces y lo que se erosiona es lo que se
  repite; y es la primera cuyo trabajo **llega a usuarios reales**, lo que sube el eje «impacto de un
  error» a **3** y con el la lectura de nivel a **5**.
- **Criterio de cierre:** ocho filas, el archivo de etapa lo cita, y no filtra ni datos propios ni
  codigos instanciados.

```
$ grep -cE "^\| \*\*[1-8] · " _workflow/030_growth.md
8

$ grep -n "_workflow/030_growth" _phases/030_growth.md | head -2
201:quien hace cada uno —humano, software, IA, o una combinacion— lo dice **`_workflow/030_growth.md`**,
387:🚨 **Las plantillas de esta etapa y el reparto de `_workflow/030_growth.md` son condicion de entrada,

$ grep -noE '\b(T|D|F|L|A|C|DT|S|N|I|R|H)-[0-9]{2,3}\b' _workflow/030_growth.md; echo "exit=$?"
exit=1
```

---

### T-092 - Completar las dos columnas que le faltaban a la fila de `L-029`
| Campo | Valor |
|---|---|
| Estado | Implementada |
| Importancia | Media |
| Urgencia | No bloqueante |
| Etapa | `000_preproject` |
| Origen | manager |
| Sesion | S-022 |

- **Que:** hallazgo propio, encontrado al ir a escribir la leccion de esta sesion. La fila de `L-029`
  en el indice de `lessons.md` tenia **cinco campos en vez de siete**: le faltaban `Etapa` y
  `Portabilidad`. Ninguna auditoria lo habia visto, y el control del Paso 2b tampoco: ese compara
  **codigos** entre indice y detalle, no el numero de columnas de cada fila.
- **Por que importa mas de lo que parece:** `Portabilidad` **solo vive en el indice**, y la cosecha
  de lecciones se comprueba barriendo esa columna. Una fila sin ella no sale como `Sin evaluar`: no
  sale de ninguna manera, y la casilla de cosecha de una etapa se aprobaria con una leccion que nadie
  miro.
- **Como:** se completa la fila con `000_preproject` y `Sin evaluar`, que es el valor de partida que
  las convenciones del archivo fijan para toda leccion nueva. **No se toca la ficha de detalle**: el
  estado de portabilidad vive en el indice y en ningun sitio mas.
- **Criterio de cierre:** todas las filas del indice tienen siete campos.

```
$ awk 'NR>=12 && /^\| \[L-/' _persistence/lessons.md | awk -F'|' '{if(NF!=7) print "FILA MAL: "$2}'; echo "exit=$?"
exit=0
```
