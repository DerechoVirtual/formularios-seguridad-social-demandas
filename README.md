# Seguridad Social: demandas y recursos ante lo social

> Plugin de Claude Code `formularios-seguridad-social-demandas` · **68 formularios** · Seguridad Social · normativa revisada el 25-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Para reclamar prestaciones ante la Sección de lo Social: demandas de incapacidad permanente e incapacidad temporal, altas médicas, desempleo, cese de actividad de autónomos, recargo de prestaciones, responsabilidad empresarial, mejoras voluntarias, recurso de suplicación y escritos de trámite.

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva; el formulario seco, listo para rellenar, está en `assets/formulario.md` dentro de la carpeta de la skill.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 68 está al final):

- **Demandas, peticiones y solicitudes iniciales** (54). Por ejemplo: Demanda contra la mutua por cese de actividad de autónomos por fuerza mayor en Ceuta (julio de 2026); Demanda contra la mutua por cese de actividad de autónomos por fuerza mayor (incendios forestales); Demanda contra el INSS que impugna la devolución de la prestación de cese de actividad (COVID-19).
- **Contestaciones, oposiciones y alegaciones** (2). Por ejemplo: Alegaciones al acta de infracción de Seguridad Social a empresarios, formadores y autónomos; Reconvención ante lo Social por no haberse citado al demandado a la conciliación previa en el SMAC.
- **Recursos** (1). Por ejemplo: Recurso de queja contra el auto que inadmite el anuncio del recurso de suplicación.
- **Comunicaciones, requerimientos y cartas** (2). Por ejemplo: Solicitud de audiencia al demandado rebelde (art. 185 LRJS); Solicitud de revisión de sentencia firme ante la Sala de lo Social del Tribunal Supremo.
- **Escritos de trámite y otros** (9). Por ejemplo: Escrito de formalización del recurso de suplicación; Escrito pidiendo acumular procesos en el mismo tribunal o en otro; Incidente de nulidad de la providencia que confirma el decreto que termina el monitorio.

## Cómo se usa

1. **Pídelo con tus palabras.** Cuéntale a Claude qué documento necesitas y para qué caso; él elige el formulario. Por ejemplo:
   - «Demanda de incapacidad permanente total contra el INSS»
   - «Impugnación de un alta médica»
   - «Demanda contra la mutua por la prestación de cese de actividad»
2. **Si no da con el formulario**, empieza por el índice del plugin: escribe `/formularios-seguridad-social-demandas:indice` y cuéntale lo que necesitas. Te propondrá el formulario que mejor encaja (o dos o tres para que elijas).
3. **Si ya sabes cuál quieres**, llámalo por su nombre de skill, por ejemplo `/formularios-seguridad-social-demandas:demanda-contra-mutua-cese-actividad-autonomos-fuerza-ss-001`. Los nombres están en la lista de formularios de abajo.

## Qué hace Claude cuando usas un formulario

1. Comprueba que Jurisprudenciator está conectado. Si no lo está, se para y te dice cómo conectarlo: no redacta nada sin él. Todos los datos jurídicos del documento (artículos vigentes, sentencias con su ECLI, datos registrales) salen de Jurisprudenciator; nunca de memoria.
2. Te pide en una sola tanda los datos del caso (partes, órgano, fechas, importes…). Lo que no sepas queda como hueco visible.
3. Resuelve contigo las opciones que el formulario deja abiertas y decide qué párrafos opcionales entran según los hechos.
4. Aplica las notas de actualización de la revisión del 25-11-2026 (reformas legales, órganos judiciales de la LO 1/2025, plazos).
5. Comprueba en el BOE, con Jurisprudenciator, cada norma que cita el documento; si alguna ha cambiado, usa la redacción vigente y te lo dice.
6. Te entrega el documento en Word **tal cual es el formulario**: empieza por su primera línea, sin títulos, notas ni explicaciones añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. En el chat te dice lo que queda pendiente y, si es un escrito, el plazo y ante quién se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.

## Antes de empezar

- **Dónde funciona:** en Claude Code y en Claude (web, escritorio y Cowork). Se instala desde este repositorio de GitHub o subiendo el ZIP del plugin.
- **Jurisprudenciator es imprescindible:** el plugin trae el conector y cada skill trabaja siempre con él. Sin una cuenta de Jurisprudenciator conectada, las skills se paran y no redactan nada. La primera vez hay que iniciar sesión (en Claude Code, con `/mcp`; o con tu URL personal: https://jurisprudenciator.lexiaipro.org/instalacion). Si ya tienes Jurisprudenciator conectado en Claude, las skills usan ese.
- **Espacio que ocupa:** unos 4.142 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-seguridad-social-demandas@formularios-seguridad-social-demandas`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-seguridad-social-demandas
/plugin install formularios-seguridad-social-demandas@formularios-seguridad-social-demandas
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-seguridad-social-demandas`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-seguridad-social-demandas/releases/latest/download/formularios-seguridad-social-demandas.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (68)

| Código | Formulario | Skill |
|---|---|---|
| SS-001 | Demanda contra la mutua por cese de actividad de autónomos por fuerza mayor en Ceuta (julio de 2026) | `demanda-contra-mutua-cese-actividad-autonomos-fuerza-ss-001` |
| SS-002 | Demanda contra la mutua por cese de actividad de autónomos por fuerza mayor (incendios forestales) | `demanda-contra-mutua-cese-actividad-autonomos-fuerza-ss-002` |
| SS-003 | Demanda contra el INSS que impugna la devolución de la prestación de cese de actividad (COVID-19) | `demanda-contra-inss-impugna-devolucion-prestacion-cese-ss-003` |
| SS-004 | Demanda de reconocimiento de accidente de trabajo por la DANA de octubre y noviembre de 2024 | `demanda-reconocimiento-accidente-trabajo-dana-octubre-ss-004` |
| SS-005 | Demanda contra la mutua por cese de actividad de autónomos por fuerza mayor debido a la DANA de 2024 | `demanda-contra-mutua-cese-actividad-autonomos-fuerza-ss-005` |
| SS-006 | Demanda contra la mutua reclamando la prestación por cese de actividad de autónomos | `demanda-contra-mutua-reclamando-prestacion-cese-ss-006` |
| SS-007 | Demanda de la empresa contra la persona trabajadora para reclamar una cantidad adeudada | `demanda-empresa-contra-persona-trabajadora-reclamar-ss-007` |
| SS-009 | Demanda para reclamar prestaciones de la Seguridad Social (reintegro de gastos médicos y otras) | `demanda-reclamar-prestaciones-seguridad-social-reintegro-ss-009` |
| SS-010 | Demanda de revisión y de declaración de error judicial contra sentencia firme del orden social | `demanda-revision-declaracion-error-judicial-contra-ss-010` |
| SS-011 | Demanda de la empresa contra la responsabilidad de pago de la pensión por contrato de relevo | `demanda-empresa-contra-responsabilidad-pago-pension-ss-011` |
| SS-012 | Alegaciones al acta de infracción de Seguridad Social a empresarios, formadores y autónomos | `alegaciones-acta-infraccion-seguridad-social-empresarios-ss-012` |
| SS-013 | Escrito de formalización del recurso de suplicación | `escrito-formalizacion-recurso-suplicacion-ss-013` |
| SS-014 | Demanda de reclamación de cantidad en el orden social | `demanda-reclamacion-cantidad-orden-social-ss-014` |
| SS-015 | Escrito pidiendo acumular procesos en el mismo tribunal o en otro | `escrito-pidiendo-acumular-procesos-mismo-tribunal-otro-ss-015` |
| SS-016 | Demanda contra la resolución en materia de prestación por desempleo | `demanda-contra-resolucion-materia-prestacion-desempleo-ss-016` |
| SS-017 | Demanda de reclamación de cantidades indebidamente ingresadas a la Seguridad Social | `demanda-reclamacion-cantidades-indebidamente-ingresadas-ss-017` |
| SS-018 | Demanda contra la extinción de la prestación o subsidio de desempleo por traslado al extranjero | `demanda-contra-extincion-prestacion-subsidio-desempleo-ss-018` |
| SS-021 | Demanda de reconocimiento de incapacidad permanente parcial | `demanda-reconocimiento-incapacidad-permanente-parcial-ss-021` |
| SS-022 | Demanda de reconocimiento de la prestación por desempleo | `demanda-reconocimiento-prestacion-desempleo-ss-022` |
| SS-023 | Incidente de nulidad de la providencia que confirma el decreto que termina el monitorio | `incidente-nulidad-providencia-confirma-decreto-termina-ss-023` |
| SS-024 | Demanda por responsabilidad de la empresa en materia de infracotización | `demanda-responsabilidad-empresa-materia-infracotizacion-ss-024` |
| SS-025 | Reconvención ante lo Social por no haberse citado al demandado a la conciliación previa en el SMAC | `reconvencion-ante-lo-social-no-haberse-citado-demandado-ss-025` |
| SS-026 | Escrito que acredita el intento de celebrar la conciliación previa | `escrito-acredita-intento-celebrar-conciliacion-previa-ss-026` |
| SS-027 | Demanda de reclamación de la mejora voluntaria de Seguridad Social pactada en convenio colectivo | `demanda-reclamacion-mejora-voluntaria-seguridad-social-ss-027` |
| SS-028 | Demanda de la empresa principal sobre recargo de prestaciones por falta de medidas de seguridad | `demanda-empresa-principal-sobre-recargo-prestaciones-ss-028` |
| SS-029 | Demanda contra el alta médica | `demanda-contra-alta-medica-ss-029` |
| SS-030 | Escrito de impugnación del recurso de suplicación | `escrito-impugnacion-recurso-suplicacion-ss-030` |
| SS-031 | Solicitud de audiencia al demandado rebelde (art. 185 LRJS) | `solicitud-audiencia-demandado-rebelde-art-185-lrjs-ss-031` |
| SS-032 | Escrito de impugnación del recurso de reposición | `escrito-impugnacion-recurso-reposicion-ss-032` |
| SS-033 | Demanda contra el alta de oficio en el Régimen General de un trabajador autónomo | `demanda-contra-alta-oficio-regimen-general-trabajador-ss-033` |
| SS-034 | Demanda para reclamar el reconocimiento del grado de discapacidad | `demanda-reclamar-reconocimiento-grado-discapacidad-ss-034` |
| SS-035 | Petición de acumulación de recursos de suplicación (art. 234 LRJS) | `peticion-acumulacion-recursos-suplicacion-art-234-lrjs-ss-035` |
| SS-036 | Solicitud de revisión de sentencia firme ante la Sala de lo Social del Tribunal Supremo | `solicitud-revision-sentencia-firme-ante-sala-lo-social-ss-036` |
| SS-037 | Recurso de queja contra el auto que inadmite el anuncio del recurso de suplicación | `recurso-queja-contra-auto-inadmite-anuncio-recurso-ss-037` |
| SS-063 | Demanda del trabajador extranjero contra la declaración de cobro indebido del desempleo | `demanda-trabajador-extranjero-contra-declaracion-cobro-ss-063` |
| SS-064 | Demanda contra la sanción que extingue la prestación o el subsidio por desempleo | `demanda-contra-sancion-extingue-prestacion-subsidio-ss-064` |
| SS-065 | Demanda reclamando el subsidio de desempleo para mayores de 52 años | `demanda-reclamando-subsidio-desempleo-mayores-52-anos-ss-065` |
| SS-066 | Demanda reclamando la prestación por desempleo denegada por supuesto fraude | `demanda-reclamando-prestacion-desempleo-denegada-ss-066` |
| SS-067 | Demanda para que se reanude el cobro de la prestación por desempleo | `demanda-reanude-cobro-prestacion-desempleo-ss-067` |
| SS-068 | Demanda reclamando el subsidio de desempleo por responsabilidades familiares | `demanda-reclamando-subsidio-desempleo-responsabilidades-ss-068` |
| SS-069 | Demanda contra el servicio de empleo que deniega el desempleo por inicio previo de actividad | `demanda-contra-servicio-empleo-deniega-desempleo-inicio-ss-069` |
| SS-070 | Demanda contra el SEPE que deniega las prestaciones por desempleo | `demanda-contra-sepe-deniega-prestaciones-desempleo-ss-070` |
| SS-071 | Escrito del beneficiario que pide poner fin a la suplicación porque no se le abona la prestación | `escrito-beneficiario-pide-poner-fin-suplicacion-porque-ss-071` |
| SS-072 | Demanda de reconocimiento de gran incapacidad derivada de enfermedad común | `demanda-reconocimiento-gran-incapacidad-derivada-ss-072` |
| SS-073 | Demanda para fijar la base reguladora de la pensión de incapacidad permanente absoluta | `demanda-fijar-base-reguladora-pension-incapacidad-ss-073` |
| SS-074 | Demanda contra la resolución que extingue la pensión de invalidez no contributiva | `demanda-contra-resolucion-extingue-pension-invalidez-no-ss-074` |
| SS-076 | Demanda de pensión no contributiva de jubilación | `demanda-pension-no-contributiva-jubilacion-ss-076` |
| SS-077 | Demanda de revisión de la incapacidad permanente total por enfermedad común por error de diagnóstico | `demanda-revision-incapacidad-permanente-total-enfermedad-ss-077` |
| SS-078 | Demanda contra el INSS para obtener el subsidio temporal en favor de familiares | `demanda-contra-inss-obtener-subsidio-temporal-favor-ss-078` |
| SS-079 | Demanda de reconocimiento de las prestaciones en favor de familiares | `demanda-reconocimiento-prestaciones-favor-familiares-ss-079` |
| SS-080 | Demanda de reintegro de los gastos sanitarios ocasionados en otro país de la Unión Europea | `demanda-reintegro-gastos-sanitarios-ocasionados-otro-ss-080` |
| SS-081 | Demanda de reconocimiento de la pensión de jubilación | `demanda-reconocimiento-pension-jubilacion-ss-081` |
| SS-082 | Demanda de reintegro de gastos médicos por una asistencia urgente de carácter vital | `demanda-reintegro-gastos-medicos-asistencia-urgente-ss-082` |
| SS-083 | Demanda de reintegro de los gastos de una prótesis ortopédica | `demanda-reintegro-gastos-protesis-ortopedica-ss-083` |
| SS-084 | Demanda por desempleo denegado por fraude de ley tras dejar un indefinido y firmar un temporal | `demanda-desempleo-denegado-fraude-ley-tras-dejar-ss-084` |
| SS-085 | Demanda del SEPE para que se revoque una prestación por desempleo ya reconocida | `demanda-sepe-revoque-prestacion-desempleo-ya-reconocida-ss-085` |
| SS-086 | Demanda contra la denegación del desempleo por considerar al solicitante socio y no asalariado | `demanda-contra-denegacion-desempleo-considerar-ss-086` |
| SS-087 | Demanda que discute la base reguladora reconocida en la prestación por desempleo | `demanda-discute-base-reguladora-reconocida-prestacion-ss-087` |
| SS-088 | Demanda de prestaciones de muerte y supervivencia por fallecimiento en accidente de trabajo | `demanda-prestaciones-muerte-supervivencia-fallecimiento-ss-088` |
| SS-089 | Demanda de reconocimiento de gran incapacidad derivada de accidente de trabajo | `demanda-reconocimiento-gran-incapacidad-derivada-ss-089` |
| SS-090 | Demanda de incapacidad permanente parcial por accidente de trabajo de un trabajador autónomo | `demanda-incapacidad-permanente-parcial-accidente-trabajo-ss-090` |
| SS-091 | Demanda de la prestación de incapacidad temporal derivada de accidente de trabajo | `demanda-prestacion-incapacidad-temporal-derivada-ss-091` |
| SS-092 | Demanda de revisión del grado de incapacidad permanente por agravación | `demanda-revision-grado-incapacidad-permanente-agravacion-ss-092` |
| SS-093 | Demanda de reconocimiento de la pensión de viudedad | `demanda-reconocimiento-pension-viudedad-ss-093` |
| SS-094 | Demanda de indemnización por lesiones permanentes no incapacitantes de origen profesional | `demanda-indemnizacion-lesiones-permanentes-no-ss-094` |
| SS-095 | Demanda de la prestación por nacimiento y cuidado de menor | `demanda-prestacion-nacimiento-cuidado-menor-ss-095` |
| SS-096 | Demanda de jubilación con responsabilidad de la empresa por falta de cotización o infracotización | `demanda-jubilacion-responsabilidad-empresa-falta-ss-096` |
| SS-097 | Petición de ejecución de la sentencia que condena a un ente público a pagar prestaciones periódicas | `peticion-ejecucion-sentencia-condena-ente-publico-pagar-ss-097` |

## Privacidad

Ver `PRIVACY.md`.
