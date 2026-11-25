---
name: demanda-reclamar-prestaciones-seguridad-social-reintegro-ss-009
description: "Demanda para reclamar prestaciones de la Seguridad Social (reintegro de gastos médicos y otras). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda para reclamar prestaciones de la Seguridad Social (reintegro de gastos médicos y otras)

> Formulario **SS-009** del plugin **Seguridad Social: demandas y recursos ante lo social** (`formularios-seguridad-social-demandas`) · Seguridad Social › Demandas y escritos ante la jurisdicción social · normativa revisada el 25-11-2026.

## Qué es

Demanda ante la Sección de lo Social del Tribunal de Instancia para reclamar el reconocimiento de prestaciones de la Seguridad Social denegadas por la entidad gestora o la mutua (reintegro de gastos médicos, contingencia profesional, grados de incapacidad, jubilación, viudedad y orfandad, ingreso mínimo vital, nacimiento y cuidado del menor, complemento de brecha de género, riesgo durante el embarazo, etc.); es un formulario con bloques alternativos de los que se conserva solo el que corresponda.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda para reclamar prestaciones de la Seguridad Social (reintegro de gastos médicos y otras)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda para reclamar prestaciones de la Seguridad Social (reintegro de gastos médicos y otras)” para mi caso». También puedes invocarla directamente con `/formularios-seguridad-social-demandas:demanda-reclamar-prestaciones-seguridad-social-reintegro-ss-009`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguridad-social-demandas:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguridad Social: demandas y recursos ante lo social) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (110 veces)
- [ ] IMPORTE (50 veces)
- [ ] N.º (19 veces)
- [ ] N.º DE DOCUMENTOS (14 veces)
- [ ] DENOMINACIÓN SOCIAL (11 veces)
- [ ] LOCALIDAD (10 veces)
- [ ] DENOMINACIÓN DE LA MUTUA (8 veces)
- [ ] N.º DE AFILIACIÓN (8 veces)
- [ ] DÍA, MES Y AÑO (6 veces)
- [ ] NOMBRE (6 veces)
- [ ] DOMICILIO (5 veces)
- [ ] AÑO (4 veces)
- [ ] CATEGORÍA (4 veces)
- [ ] EDAD (4 veces)
- [ ] ENFERMEDAD (4 veces)
- [ ] NOMBRE DEL FALLECIDO (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] REQUISITOS (4 veces)
- [ ] RÉGIMEN (4 veces)
- [ ] ACTIVIDAD (3 veces)
- [ ] DESCRIPCIÓN (3 veces)
- [ ] DIAGNÓSTICO (3 veces)
- [ ] FECHA DE EFECTOS DE LA INCAPACIDAD PERMANENTE (3 veces)
- [ ] MOTIVO (3 veces)
- [ ] N.º DE (3 veces)
- [ ] N.º DE DOCUMENTO (3 veces)
- [ ] PORCENTAJE (3 veces)
- [ ] SEGUNDO / TERCER / ETC. (3 veces)
- [ ] ARTÍCULO (2 veces)
- [ ] COMUNIDAD AUTÓNOMA (2 veces)
- [ ] EDADES (2 veces)
- [ ] GRUPO PROFESIONAL (2 veces)
- [ ] LABORES (2 veces)
- [ ] MOTIVOS (2 veces)
- [ ] N.º DE AÑOS (2 veces)
- [ ] N.º DE EXPEDIENTE (2 veces)
- [ ] NOMBRE DEL LETRADO/A (2 veces)
- [ ] PROFESIÓN (2 veces)
- [ ] TEXTO DE LA RESOLUCIÓN (2 veces)
- [ ] CAUSA
- [ ] … y 56 datos más que aparecen una vez en el modelo

## Normas que cita el formulario

- art. 1 Ley 36/2011
- art. 17 Ley 36/2011
- art. 164 LGSS

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

### Avisos de actualización (4) — se aplican en el texto, nunca se copian en el documento

- Junto a «…sa o tácita de la reclamación previa (debe estar agotada la vía administrativa).»: el modelo cita numerosas disposiciones de la LGSS (RDLeg 8/2015) y de reglamentos de desarrollo, algunos históricos (Decreto 3158/1966, Órdenes de 1962, 1967 y 1996, Real Decreto 1300/1995). Antes de presentar, comprobar la redacción vigente y el artículo equivalente de cada precepto, así como las reformas posteriores en materia de incapacidad permanente, pensión de orfandad y prestaciones por nacimiento y cuidado del menor. Verificar también las referencias jurisprudenciales citadas.
- Junto a «…ey General de la Seguridad Social, aprobada por Decreto 2065/1974, de 30 de mayo»: norma derogada; comprobar el artículo equivalente del texto refundido de la Ley General de la Seguridad Social, RDLeg 8/2015
- Junto a «…or el que se aprueba el texto refundido de la Ley General de la Seguridad Social»: en el original los números de artículo aparecían pegados («164158»); comprobar la relación exacta de preceptos
- Junto a «…etroacción de los efectos económicos a los tres meses anteriores a la solicitud.»: comprobar el número completo de recurso o el ECLI de la sentencia.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

NOTAS DE USO (suprimir antes de presentar):

Este formulario de demanda puede ser utilizado para reclamar las siguientes prestaciones:

- Reintegro de gastos médicos.
- Declaración de la contingencia de accidente de trabajo o enfermedad profesional.
- Declaración del grado de incapacidad permanente.
- Reconocimiento de la prestación de incapacidad temporal, incapacidad permanente parcial para la profesión habitual, incapacidad permanente total para la profesión habitual, incapacidad permanente absoluta o gran invalidez.
- Reconocimiento de la pensión de incapacidad permanente no contributiva.
- Reconocimiento de la pensión de jubilación (contributiva o no contributiva).
- Reconocimiento de la pensión de viudedad y de la pensión de orfandad.
- Reconocimiento de la pensión en favor de familiares.
- Reconocimiento del Ingreso Mínimo Vital.
- Reconocimiento de la prestación por nacimiento y cuidado del menor.
- Reconocimiento del complemento de pensión para la reducción de la brecha de género (antiguo complemento de pensión por aportación demográfica a la Seguridad Social).
- Reconocimiento de la prestación por riesgo durante el embarazo.

La demanda para reclamar una prestación de la Seguridad Social debe presentarse en el plazo de 30 días desde la desestimación expresa o tácita de la reclamación previa (debe estar agotada la vía administrativa).


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
