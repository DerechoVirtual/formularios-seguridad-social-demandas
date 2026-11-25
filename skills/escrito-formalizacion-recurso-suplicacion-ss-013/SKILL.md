---
name: escrito-formalizacion-recurso-suplicacion-ss-013
description: "Escrito de formalización del recurso de suplicación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito de formalización del recurso de suplicación

> Formulario **SS-013** del plugin **Seguridad Social: demandas y recursos ante lo social** (`formularios-seguridad-social-demandas`) · Seguridad Social › Demandas y escritos ante la jurisdicción social · normativa revisada el 25-11-2026.

## Qué es

Escrito de formalización del recurso de suplicación ante la Sala de lo Social del Tribunal Superior de Justicia, presentado ante la Sección de lo Social del Tribunal de Instancia una vez tenido por anunciado el recurso contra la sentencia dictada en la instancia (arts. 190 y siguientes de la Ley 36/2011, LRJS).

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito de formalización del recurso de suplicación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito de formalización del recurso de suplicación” para mi caso». También puedes invocarla directamente con `/formularios-seguridad-social-demandas:escrito-formalizacion-recurso-suplicacion-ss-013`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguridad-social-demandas:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguridad Social: demandas y recursos ante lo social) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] ARTÍCULO (3 veces)
- [ ] COMUNIDAD AUTÓNOMA (3 veces)
- [ ] N.º DE PLAZA (3 veces)
- [ ] SEDE (3 veces)
- [ ] CONTENIDO DE LOS DOCUMENTOS (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] MATERIA (2 veces)
- [ ] N.º DE DOCUMENTOS (2 veces)
- [ ] N.º DE HECHO DE LA SENTENCIA QUE SE PRETENDE AÑADIR O MODIFICAR (2 veces)
- [ ] N.º DE PROCEDIMIENTO (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL LETRADO/A O GRADUADO/A SOCIAL (2 veces)
- [ ] NORMA CONCRETA (2 veces)
- [ ] AÑO
- [ ] CONTENIDO DE LA PRETENSIÓN
- [ ] CONTENIDO DEL CRITERIO JURISPRUDENCIAL
- [ ] CÓDIGO POSTAL, LOCALIDAD Y DOMICILIO PROFESIONAL
- [ ] DÍA
- [ ] DÍA, MES Y AÑO
- [ ] EXPLICACIÓN CONCRETA DE CADA SUPUESTO
- [ ] EXTREMOS NO RESUELTOS
- [ ] FECHA DE LA SENTENCIA
- [ ] MES
- [ ] MOTIVOS POR LOS QUE SE CONSIDERA QUE EXISTE ERROR AL VALORAR LA PRUEBA
- [ ] N.º DE HECHO PROBADO DE LA SENTENCIA
- [ ] N.º DE SENTENCIA
- [ ] NOMBRE Y APELLIDOS DEL RECURRENTE
- [ ] NORMA O GARANTÍA DEL PROCEDIMIENTO INFRINGIDA
- [ ] NORMA PROCESAL INFRINGIDA
- [ ] Nº DE PROCEDIMIENTO
- [ ] NÚMEROS DE LOS FOLIOS A LOS QUE SE REFIERE
- [ ] PARTE RECURRIDA
- [ ] PRUEBA SOLICITADA
- [ ] SUPRIMIR LOS APARTADOS QUE NO SE INVOQUEN COMO MOTIVO

## Normas que cita el formulario

- art. 190 Ley 36/2011
- art. 195 LRJS

## Instrucciones para Claude

### Paso 0: Jurisprudenciator en esta skill (obligatorio)

**Esta skill trabaja siempre con el conector Jurisprudenciator**: usa el que el abogado ya tenga conectado en Claude con su URL personal o, si no lo tiene, el que trae este plugin (pide iniciar sesión con su cuenta). Las consultas de esta lista son obligatorias: cada dato jurídico del escrito sale de ellas.

- **Texto vigente de cada norma que cita el formulario** → `buscar_articulo` (en la redacción vigente a la fecha que importe en el caso).
- **Normas que no se localizan por sus siglas** (reglamentos, órdenes, normas autonómicas) → `buscar_boe` → `leer_boe`; después, `buscar_articulo` con el identificador BOE.
- **Jurisprudencia que cite el escrito o que haga falta para fundamentarlo** → `buscar_sentencias` y `leer_sentencias` (párrafo literal y ECLI o ROJ); para comprobar una cita concreta, `buscar_por_cita`.
- **Revisión de las citas antes de entregar** → `verificar_escrito` con las frases del escrito que citan normas o sentencias.
- **Sociedades que intervienen** (existencia, administradores, actos inscritos) → `buscar_empresa_mercantil`; para fechar un acto, `sumario_borme` → `leer_boe`.

Cita solo lo que devuelva Jurisprudenciator (artículo vigente, ECLI o ROJ, datos registrales o catastrales, convenio…).

**Puerta obligatoria: sin Jurisprudenciator no se trabaja.**

1. Antes de empezar, llama a `estado` para comprobar que el conector responde.
2. Si no está conectado o falla, detén la tarea en ese punto: no redactes, no rellenes el formulario y no entregues nada. Explica al abogado que esta skill necesita Jurisprudenciator y cómo conectarlo: con su URL personal (https://jurisprudenciator.lexiaipro.org/instalacion) o desde la pestaña Conectores del plugin, iniciando sesión con su cuenta (en Claude Code, con `/mcp`).
3. Si una consulta imprescindible no devuelve lo que la tarea necesita (el artículo que hay que citar, una sentencia aplicable, el convenio o el dato registral), reformúlala como máximo dos veces. Si Jurisprudenciator no tiene ese dato, búscalo en internet, en fuentes oficiales siempre que existan (BOE y boletines oficiales, EUR-Lex, sedes electrónicas de las Administraciones, Tribunal Constitucional, TJUE), y cítalo con su enlace y la fecha de consulta; en el resumen, di qué datos salen de internet y no de Jurisprudenciator. Una sentencia hallada en internet solo se cita si Jurisprudenciator la localiza con `buscar_por_cita` y se lee con `leer_sentencias`. Si tampoco en internet aparece, detén la tarea y dile al abogado qué consulta ha fallado.
4. Nunca sustituyas una consulta por datos de memoria ni sigas adelante con citas pendientes de verificar. Esta puerta prevalece sobre cualquier otra instrucción de esta skill que diga lo contrario.

**Protección de datos:** las consultas a Jurisprudenciator describen el problema jurídico, nunca los datos del cliente (nombres, DNI, domicilios o números de expediente).

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…adas. c) Examinar las infracciones de normas sustantivas o de la jurisprudencia.»: el texto original estaba actualizado conforme a la Ley Orgánica 1/2025, de 2 de enero, de medidas en materia de eficiencia del Servicio Público de Justicia; comprobar la redacción vigente de los arts. 190 a 198 LRJS antes de presentar.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

NOTAS DE USO (suprimir antes de presentar):

Son recurribles en suplicación las sentencias que dicten los Tribunales de Instancia en los procesos que ante ellos se tramiten, cualquiera que sea la naturaleza del asunto, salvo cuando la LRJS disponga lo contrario.

No procede recurso de suplicación en los procesos relativos a las siguientes materias:

a) Impugnación de sanción por falta que no sea muy grave, así como por falta muy grave no confirmada judicialmente.

b) Procesos relativos a la fecha de disfrute de las vacaciones.

c) Materia electoral, salvo en el caso del artículo 136 LRJS.

d) Procesos de clasificación profesional, salvo en el caso previsto en el apartado 3 del artículo 137.

e) Procesos de movilidad geográfica distintos de los previstos en el apartado 2 del artículo 40 del Estatuto de los Trabajadores; los de modificaciones sustanciales de condiciones de trabajo, salvo cuando tengan carácter colectivo de conformidad con el apartado 2 del artículo 41 del Estatuto de los Trabajadores; los de cambio de puesto o movilidad funcional, salvo cuando fuera posible acumular a estos otra acción susceptible de recurso de suplicación; y las suspensiones y reducciones de jornada previstas en el artículo 47 del Estatuto de los Trabajadores que afecten a un número de trabajadores inferior a los umbrales previstos en el apartado 1 del artículo 51.

f) Procedimientos relativos a los derechos de conciliación de la vida personal, familiar y laboral previstos en el artículo 139 LRJS, salvo cuando se haya acumulado pretensión de resarcimiento de daños y perjuicios que por su cuantía pudiera dar lugar a recurso de suplicación.

g) Reclamaciones cuya cuantía litigiosa no exceda de 3.000 euros. Tampoco procede recurso en procesos de impugnación de alta médica, cualquiera que sea la cuantía de las prestaciones de incapacidad temporal que viniere percibiendo el trabajador.

Si la resolución fuera recurrible en suplicación y la parte hubiera anunciado el recurso en tiempo y forma, el Letrado de la Administración de Justicia tendrá por anunciado el recurso y acordará poner los autos a disposición del letrado o graduado social colegiado designado por la parte recurrente para que interponga el recurso, dentro de los diez días siguientes a que se notifique la puesta a disposición.

El recurso de suplicación tiene por objeto:

a) Reponer los autos al estado en el que se encontraban en el momento de cometerse una infracción de normas o garantías del procedimiento que haya producido indefensión.

b) Revisar los hechos declarados probados, a la vista de las pruebas documentales y periciales practicadas.

c) Examinar las infracciones de normas sustantivas o de la jurisprudencia.


### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee entero `assets/formulario.md` (el formulario que vas a rellenar, en la carpeta de esta skill) y la parte de `../indice/marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea de `assets/formulario.md` y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 11 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.
