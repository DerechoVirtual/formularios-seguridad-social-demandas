---
name: demanda-contra-mutua-cese-actividad-autonomos-fuerza-ss-002
description: "Demanda contra la mutua por cese de actividad de autónomos por fuerza mayor (incendios forestales). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda contra la mutua por cese de actividad de autónomos por fuerza mayor (incendios forestales)

> Formulario **SS-002** del plugin **Seguridad Social: demandas y recursos ante lo social** (`formularios-seguridad-social-demandas`) · Seguridad Social › Demandas y escritos ante la jurisdicción social · normativa revisada el 25-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda contra la mutua por cese de actividad de autónomos por fuerza mayor (incendios forestales)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda contra la mutua por cese de actividad de autónomos por fuerza mayor (incendios forestales)” para mi caso». También puedes invocarla directamente con `/formularios-seguridad-social-demandas:demanda-contra-mutua-cese-actividad-autonomos-fuerza-ss-002`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguridad-social-demandas:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguridad Social: demandas y recursos ante lo social) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (14 veces)
- [ ] IMPORTE (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] PARTE DEMANDADA (2 veces)
- [ ] ACTIVIDAD
- [ ] CORREO ELECTRÓNICO
- [ ] DNI/NIE
- [ ] LUGAR
- [ ] MOTIVO
- [ ] MUNICIPIOS AFECTADOS
- [ ] Nº DE EXPEDIENTE
- [ ] SEDE
- [ ] TELÉFONO
- [ ] ÓRGANO ADMINISTRATIVO

## Normas que cita el formulario

- art. 331.1.b LGSS
- art. 338 LGSS
- art. 6 Real Decreto-ley 20/2026
- art. 1 Ley 36/2011

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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…veinticuatro meses inmediatamente anteriores a la situación de cese de actividad»: Redacción vigente del período mínimo (art. 338.1 LGSS desde 1-1-2023) y de las normas excepcionales (art. 24.3 RDL 6/2024, art. 6.3 RDL 20/2026, art. 39.3 RDL 22/2026). Fuente: art. 338.1 LGSS (red. RDL 13/2022); RDL 6/2024, BOE-A-2024-22928; RDL 20/2026, BOE-A-2026-16543; RDL 22/2026, BOE-A-2026-18429.
- Junto a «…ad Social. FUNDAMENTOS DE DERECHO I.- Es competente el Tribunal al que me dirijo»: Las referencias a los Juzgados de lo Social se entienden hechas a las Secciones de lo Social de los Tribunales de Instancia. Fuente: LO 1/2025 DA 1.ª; LO 1/2025, BOE-A-2025-76.
- Junto a «…40 a 146 del mismo texto legal que regulan la reclamación administrativa previa.»: La reclamación previa es administrativa, no «judicial». En cese de actividad es potestativa (art. 350.1 LGSS) y, si se dirige a una mutua, informa una comisión paritaria (art. 350.2 LGSS). Fuente: art. 71 LRJS; art. 350 LGSS (red. RDL 28/2018); LRJS (Ley 36/2011), BOE-A-2011-15936; LGSS (RDLeg 8/2015), BOE-A-2015-11724.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Los órganos jurisdiccionales del orden social conocerán de las cuestiones litigiosas que se promuevan en materia de prestaciones de Seguridad Social, incluidas la protección por desempleo y la protección por cese de actividad de las personas trabajadoras por cuenta propia o autónomos (art. 2.o) de la LJS).

La protección por cese de actividad se rige por lo dispuesto en los artículos 331 y 332 de la LGSS, y en sus normas de desarrollo, así como, supletoriamente, por las normas que regulan el régimen especial de la Seguridad Social de encuadramiento.

Las personas trabajadoras por cuenta propia o autónomos podrán solicitar la prestación por cese de actividad por fuerza mayor ante su mutua sin necesidad de contar con la cotización mínima exigida para poder acceder a ella y sin necesidad de acreditar, en el momento de la solicitud, la imposibilidad para desarrollar la actividad. Todo como consecuencia de los incendios forestales que den lugar a la adopción de medidas de protección civil que afecten a la población, tales como evacuaciones, restricciones de acceso, confinamientos u otras de naturaleza análoga, hasta que concluya la campaña anual de peligro alto de incendios forestales del año 2026 en virtud del art. 6 del Real Decreto-ley 20/2026, de 29 de julio, por el que se establecen medidas urgentes de protección laboral y social frente a los incendios forestales.


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
