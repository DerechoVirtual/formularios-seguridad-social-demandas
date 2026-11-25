---
name: solicitud-revision-sentencia-firme-ante-sala-lo-social-ss-036
description: "Solicitud de revisión de sentencia firme ante la Sala de lo Social del Tribunal Supremo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de revisión de sentencia firme ante la Sala de lo Social del Tribunal Supremo

> Formulario **SS-036** del plugin **Seguridad Social: demandas y recursos ante lo social** (`formularios-seguridad-social-demandas`) · Seguridad Social › Demandas y escritos ante la jurisdicción social · normativa revisada el 25-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de revisión de sentencia firme ante la Sala de lo Social del Tribunal Supremo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de revisión de sentencia firme ante la Sala de lo Social del Tribunal Supremo” para mi caso». También puedes invocarla directamente con `/formularios-seguridad-social-demandas:solicitud-revision-sentencia-firme-ante-sala-lo-social-ss-036`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguridad-social-demandas:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguridad Social: demandas y recursos ante lo social) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] FECHA (3 veces)
- [ ] TIPO Y Nº DE PROCEDIMIENTO (3 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE DE LA PARTE (2 veces)
- [ ] Nº DE SENTENCIA (2 veces)
- [ ] ÓRGANO O PERSONA (2 veces)
- [ ] LUGAR
- [ ] MATERIA DEL PROCEDIMIENTO
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] SEDE

## Normas que cita el formulario

- art. 236 LRJS
- art. 17 LRJS
- art. 245.3 LOPJ
- art. 21 LRJS
- art. 509 LEC
- art. 510 LEC
- art. 512 LEC
- art. 516 LEC

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

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

El artículo 9.c) LRJS expresa que la Sala de lo Social del Tribunal Supremo conocerá de la revisión de sentencias firmes dictadas por los órganos jurisdiccionales del orden social y de la revisión de laudos arbitrales firmes sobre materias objeto de conocimiento del orden social.

El artículo 236.1 LRJS añade que contra cualquier sentencia firme dictada por los órganos del orden jurisdiccional social y contra los laudos arbitrales firmes sobre materias objeto de conocimiento del orden social, procederá la revisión prevista en la LEC, por los motivos de su artículo 510 y por el regulado en el art. 86.3 LRJS (sentencia absolutoria por prejudicialidad penal). La revisión se solicitará ante la Sala de lo Social del Tribunal Supremo.

En la revisión no se celebrará vista, salvo que así lo acuerde el Tribunal o cuando deba practicarse prueba. En caso de condena en costas se estará a lo previsto en el art. 235 LRJS y el depósito para recurrir tendrá la cuantía que en dicha norma se señala para los recursos de casación.

La revisión se inadmitirá de no concurrir los requisitos y presupuestos procesales exigibles o de no haberse agotado previamente los recursos jurisdiccionales que la ley prevé para que la sentencia pueda considerarse firme; así como si se formula por los mismos motivos que hubieran podido plantearse, de concurrir los presupuestos para ello, en el incidente de nulidad de actuaciones regulado en el artículo 241 LOPJ o mediante la audiencia al demandado rebelde (art. 185 LRJS), o cuando planteados aquellos los referidos motivos hubieren sido desestimados por resolución firme.

Si la Sala apreciara la concurrencia de cualquiera de tales causas de inadmisión dictará auto, contra el cual no cabe recurso.

Motivos para la revisión de una sentencia firme (art. 510 LEC):

1. Si después de pronunciada, se recobraren u obtuvieren documentos decisivos, de los que no se hubiere podido disponer por fuerza mayor o por obra de la parte en cuyo favor se hubiere dictado.

2. Si hubiere recaído en virtud de documentos que al tiempo de dictarse ignoraba una de las partes haber sido declarados falsos en un proceso penal, o cuya falsedad declarare después penalmente.

3. Si hubiere recaído en virtud de prueba testifical o pericial, y los testigos o los peritos hubieren sido condenados por falso testimonio dado en las declaraciones que sirvieron de fundamento a la sentencia.

4. Si se hubiere ganado injustamente en virtud de cohecho, violencia o maquinación fraudulenta.

5. Asimismo se podrá interponer recurso de revisión contra una resolución judicial firme cuando el Tribunal Europeo de Derechos Humanos haya declarado que dicha resolución ha sido dictada en violación de alguno de los derechos reconocidos en el Convenio Europeo para la Protección de los Derechos Humanos y Libertades Fundamentales y sus Protocolos, siempre que la violación, por su naturaleza y gravedad, entrañe efectos que persistan y no puedan cesar de ningún otro modo que no sea mediante esta revisión, sin que la misma pueda perjudicar los derechos adquiridos de buena fe por terceras personas.


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
