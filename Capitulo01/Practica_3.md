# Práctica 3. Análisis de un escenario del sector con agentes de IA

**Duración:** 13 minutos  
**Herramientas:** Microsoft 365 Copilot Chat, Investigador, Analista, Ideas, Prompt Coach y Agent Builder  
**Archivo requerido:** [`Analisis_BESS.xlsx`](docs/Analisis_BESS.xlsx)

---

## Objetivo

Explorar el papel que puede desempeñar el almacenamiento de energía mediante sistemas de baterías (BESS) en el sector de generación eléctrica, utilizando diferentes capacidades especializadas de inteligencia artificial para investigar tendencias, analizar datos, generar perspectivas y mejorar instrucciones, y finalizar con la creación de un agente personalizado que utilice conocimiento propio para apoyar la preparación de reuniones de trabajo.

---

## Escenario

El almacenamiento de energía mediante sistemas de baterías, conocidos como **BESS (Battery Energy Storage Systems)**, está adquiriendo cada vez mayor relevancia dentro del sector eléctrico.

Un equipo transversal de una empresa de generación eléctrica necesita preparar una sesión interna para comprender mejor:

- Cómo está evolucionando esta tecnología.
- Qué papel está desempeñando en el sector eléctrico.
- Qué información muestran los datos disponibles.
- Qué preguntas podrían surgir desde diferentes áreas de una organización.
- Qué aspectos sería conveniente considerar durante una conversación interna sobre el tema.

Para preparar esta sesión utilizaremos diferentes agentes de Microsoft 365 Copilot.

Cada agente aportará una capacidad diferente al proceso.

> **Importante:** Los datos utilizados durante esta práctica son ficticios y fueron creados exclusivamente con fines de capacitación. El ejercicio tiene un propósito educativo y no constituye una evaluación técnica, financiera ni una recomendación de inversión relacionada con sistemas BESS.

---

# Parte 1. Investigar el contexto del sector

## Paso 1. Acceder al agente Investigador

Accede a **Microsoft 365 Copilot Chat**.

Localiza y abre el agente **Investigador**.

Durante esta primera actividad utilizaremos el agente para construir un panorama general sobre la evolución del almacenamiento mediante baterías en Chile.

---

## Paso 2. Investigar la evolución de BESS en Chile

Utiliza el siguiente prompt:

~~~text
Investiga cómo está evolucionando el almacenamiento de energía mediante sistemas BESS en Chile y qué papel está desempeñando en el sector de generación eléctrica.

Incluye:

- Principales tendencias observadas.
- Problemas o necesidades del sistema eléctrico que puede ayudar a abordar.
- Casos o proyectos relevantes desarrollados recientemente en Chile.
- Oportunidades que esta tecnología puede representar para empresas generadoras.
- Desafíos técnicos, económicos o regulatorios que se mencionan con mayor frecuencia.

Prioriza fuentes oficiales, institucionales y especializadas recientes.

Distingue claramente los hechos encontrados de tus interpretaciones e incluye las fuentes utilizadas.
~~~

Espera a que Investigador complete la consulta.

---

## Paso 3. Revisar la investigación

Revisa brevemente el resultado generado.

Identifica:

- Las tendencias que aparecen con mayor frecuencia.
- Los principales usos asociados al almacenamiento de energía.
- Los proyectos o casos mencionados.
- Los desafíos identificados.
- Las fuentes utilizadas para sustentar la investigación.

No es necesario revisar detalladamente todo el reporte.

El propósito es observar cómo un agente especializado puede ayudarnos a pasar de una pregunta general a una **investigación estructurada y sustentada en diferentes fuentes**.

> **Idea clave:** Investigador puede utilizarse cuando necesitamos ampliar nuestro conocimiento sobre un tema y construir contexto antes de analizarlo o discutirlo.

---

# Parte 2. Analizar información con el agente Analista

## Paso 4. Revisar el archivo de trabajo

Descarga y abre el archivo:

[`Analisis_BESS.xlsx`](docs/Analisis_BESS.xlsx)

El archivo contiene información ficticia correspondiente a una jornada simplificada del sistema eléctrico.

Encontrarás datos relacionados con:

- Hora.
- Generación solar.
- Demanda.
- Diferencia entre generación solar y demanda.
- Precio de la energía.

Los datos fueron preparados para mostrar diferentes comportamientos a lo largo de una jornada.

No es necesario analizar manualmente todos los registros.

---

## Paso 5. Acceder al agente Analista

Regresa a **Microsoft 365 Copilot Chat**.

Abre el agente **Analista** y adjunta el archivo:

[`Analisis_BESS.xlsx`](docs/Analisis_BESS.xlsx)

Utiliza el siguiente prompt:

~~~text
Analiza estos datos e identifica los patrones más importantes a lo largo de la jornada.

Quiero comprender especialmente:

- En qué horas existe mayor generación solar.
- Cómo cambia la demanda durante el día.
- En qué periodos existe mayor diferencia entre generación solar y demanda.
- Cómo se comporta el precio de la energía durante esos periodos.
- Qué momentos podrían resultar interesantes para analizar el posible papel de un sistema de almacenamiento.

No diseñes ni dimensiones un sistema BESS y no realices una recomendación de inversión.

Presenta los principales hallazgos y susténtalos con los datos.
~~~

Espera a que Analista complete el procesamiento de la información.

---

## Paso 6. Revisar los hallazgos

Revisa los patrones identificados por Analista.

Observa especialmente cómo relaciona diferentes variables del archivo y cómo utiliza los datos para sustentar sus conclusiones.

Compara esta actividad con la realizada anteriormente:

- **Investigador** nos ayudó a comprender qué está ocurriendo actualmente en el sector.
- **Analista** nos ayuda a comprender qué patrones existen dentro de un conjunto de datos.

> **Idea clave:** Diferentes agentes pueden aportar capacidades especializadas dependiendo del tipo de actividad que necesitamos realizar.

---

# Parte 3. Explorar el escenario desde diferentes perspectivas

## Paso 7. Acceder al agente Ideas

Regresa a Microsoft 365 Copilot Chat y abre el agente **Ideas**.

Ahora utilizaremos el mismo tema desde una perspectiva diferente.

En lugar de investigar información o analizar datos, queremos explorar qué preguntas podrían surgir al conversar sobre BESS con personas de diferentes áreas de una organización.

Utiliza:

~~~text
Estamos preparando una sesión interna sobre almacenamiento de energía mediante BESS para colaboradores de una empresa de generación eléctrica.

Genera ideas de preguntas que diferentes áreas de la organización podrían querer resolver sobre esta tecnología.

Considera perspectivas como:

- Operaciones.
- Finanzas.
- Sostenibilidad.
- Tecnología.
- Personas.
- Gestión de proyectos.

No propongas decisiones ni proyectos concretos.

Organiza las preguntas por perspectiva y selecciona al final las 5 que podrían generar una conversación más interesante entre diferentes áreas.
~~~

---

## Paso 8. Revisar las diferentes perspectivas

Observa cómo un mismo tema puede generar preguntas diferentes dependiendo del contexto y las necesidades de cada área.

Por ejemplo, algunas preguntas pueden estar relacionadas con:

- Impacto en las actividades de trabajo.
- Costos y viabilidad.
- Sostenibilidad.
- Capacidades tecnológicas.
- Nuevas competencias.
- Gestión y seguimiento de proyectos.

> **Idea clave:** La IA también puede utilizarse para ampliar nuestra perspectiva y explorar aspectos de un problema que inicialmente no habíamos considerado.

---

# Parte 4. Mejorar una solicitud con Prompt Coach

## Paso 9. Partir de una solicitud poco precisa

Accede al agente **Prompt Coach**.

Imagina que una persona desea continuar investigando el tema y escribe simplemente:

~~~text
Dime si las baterías son buenas para una empresa eléctrica.
~~~

Esta solicitud expresa una intención general, pero deja abiertas muchas preguntas:

- ¿Qué queremos conocer exactamente?
- ¿Qué tipo de baterías estamos considerando?
- ¿Para qué tipo de empresa?
- ¿Qué profundidad necesitamos?
- ¿Qué aspectos deben analizarse?
- ¿Qué resultado esperamos obtener?

Utilizaremos Prompt Coach para transformar esta solicitud en una instrucción más completa.

---

## Paso 10. Solicitar a Prompt Coach que mejore el prompt

Utiliza:

~~~text
Ayúdame a mejorar este prompt:

"Dime si las baterías son buenas para una empresa eléctrica."

Necesito que el nuevo prompt permita solicitar un documento introductorio sobre el papel de los sistemas de almacenamiento de energía mediante baterías (BESS) en empresas del sector de generación eléctrica.

El documento debe estar dirigido a colaboradores de diferentes áreas, por lo que debe utilizar un lenguaje claro y evitar un nivel de profundidad excesivamente técnico.

El prompt debe solicitar:

- Una explicación breve de qué es un sistema BESS.
- Principales aplicaciones en el sector de generación eléctrica.
- Beneficios y oportunidades que suelen asociarse con esta tecnología.
- Principales desafíos y aspectos que deben considerarse.
- Implicaciones o preguntas relevantes para diferentes áreas de una organización.
- Diferenciación entre hechos, tendencias e interpretaciones.
- Fuentes confiables y recientes.

El resultado final deberá solicitarse como un documento estructurado que pueda abrirse y editarse en Microsoft Word.
~~~

Revisa el prompt propuesto por Prompt Coach.

Observa cómo una solicitud inicialmente ambigua se transforma al incorporar:

- Objetivo.
- Contexto.
- Instrucciones.
- Resultado esperado.

---

# Parte 5. Convertir el resultado en conocimiento reutilizable

## Paso 11. Generar el documento de referencia

Copia el prompt mejorado por Prompt Coach.

Regresa a Microsoft 365 Copilot Chat e inicia una nueva conversación.

Utiliza el prompt mejorado para generar el documento solicitado.

El objetivo es obtener un documento introductorio sobre BESS que pueda ser utilizado posteriormente como recurso de conocimiento.

Solicita que el resultado pueda abrirse y editarse en **Microsoft Word**.

Guarda el documento con el siguiente nombre:

`Introduccion_BESS_Generacion_Electrica.docx`

---

## Paso 12. Revisar el documento

Abre el archivo generado.

Comprueba que incluya información sobre:

- Qué es un sistema BESS.
- Principales aplicaciones.
- Beneficios y oportunidades.
- Desafíos.
- Aspectos relevantes para diferentes áreas.
- Fuentes consultadas.

No es necesario realizar una revisión exhaustiva durante la práctica.

El objetivo es comprobar que el documento contiene información suficientemente estructurada para utilizarse como recurso de referencia.

> **Importante:** Conserva el archivo `Introduccion_BESS_Generacion_Electrica.docx`. Lo utilizaremos como fuente de conocimiento durante la creación de un agente personalizado.

---

# Parte 6. Crear un agente especializado con Agent Builder

## Paso 13. Acceder a Agent Builder

Regresa a **Microsoft 365 Copilot Chat**.

Accede a **Agent Builder** para comenzar la creación de un nuevo agente.

Durante los pasos anteriores investigamos el almacenamiento de energía mediante sistemas BESS, analizamos datos relacionados con generación solar, demanda y precios, exploramos el tema desde diferentes perspectivas y generamos un documento introductorio que reúne conocimiento sobre esta tecnología.

Ahora utilizaremos ese documento para crear un agente especializado que pueda ayudarnos a consultar y comprender información relacionada con BESS.

El agente se llamará:

**Asistente de conocimiento BESS**

---

## Paso 14. Crear el agente

Utiliza la siguiente descripción para comenzar su creación:

~~~text
Crea un agente llamado "Asistente de conocimiento BESS".

Su propósito es ayudar a colaboradores de una empresa del sector de generación eléctrica a comprender y consultar información relacionada con sistemas de almacenamiento de energía mediante baterías (BESS).
~~~

Una vez creado el agente, asegúrate de que las instrucciones del agente incluyan lo siguiente:

~~~text
Debe poder explicar conceptos y responder preguntas utilizando un lenguaje claro para colaboradores de diferentes áreas, evitando asumir que todos cuentan con conocimientos técnicos especializados.

Cuando reciba una consulta debe:

1. Explicar los conceptos de BESS de manera clara y estructurada.
2. Describir sus principales aplicaciones dentro del sector de generación eléctrica.
3. Explicar beneficios, oportunidades, desafíos y consideraciones relacionadas con esta tecnología.
4. Ayudar a comprender cómo un mismo tema puede ser relevante para diferentes áreas de una organización.
5. Distinguir entre hechos, tendencias, interpretaciones y aspectos que requieren información adicional.
6. Utilizar prioritariamente la información disponible en sus fuentes de conocimiento.
7. Indicar cuando la información disponible no sea suficiente para responder una pregunta.

No debe inventar información que no se encuentre disponible en sus fuentes.

No debe realizar dimensionamientos de sistemas BESS, emitir recomendaciones de inversión ni sustituir una evaluación técnica, financiera o regulatoria especializada.

Debe utilizar un lenguaje profesional, claro y comprensible para una audiencia transversal.
~~~

Revisa la descripción y las instrucciones generadas para el agente.

Realiza los ajustes necesarios antes de continuar.

---

## Paso 15. Incorporar conocimiento especializado

Durante la configuración del agente, localiza la opción para agregar **fuentes de conocimiento**.

Agrega el documento creado anteriormente:

`Introduccion_BESS_Generacion_Electrica.docx`

Espera a que el archivo quede incorporado como fuente de conocimiento.

Ahora nuestro agente cuenta con dos elementos fundamentales:

| Elemento | Función |
| --- | --- |
| **Instrucciones** | Definen que el agente debe comportarse como un asistente especializado en conocimiento sobre BESS y establecen cómo debe responder. |
| **Conocimiento** | Proporciona información de referencia sobre BESS que el agente puede consultar para elaborar sus respuestas. |

En este caso, las instrucciones determinan **cómo debe trabajar nuestro especialista**, mientras que el documento proporciona parte del **conocimiento especializado que tendrá disponible**.

> **Idea clave:** Crear un agente no consiste únicamente en definir instrucciones. También podemos proporcionarle fuentes de conocimiento relacionadas con el contexto o dominio en el que queremos que nos ayude.

---

# Parte 7. Probar el agente especializado

## Paso 16. Realizar una primera consulta

Una vez configurado el **Asistente de conocimiento BESS**, realiza una consulta general:

~~~text
Explícame qué papel puede desempeñar un sistema BESS en una empresa de generación eléctrica.

Quiero comprender:

- Para qué puede utilizarse.
- Qué oportunidades puede representar.
- Cuáles son los principales desafíos que deben considerarse.
- Por qué puede ser relevante para diferentes áreas de una organización.

Explícalo para una persona que trabaja en la empresa, pero que no necesariamente tiene un perfil técnico especializado.
~~~

Revisa la respuesta.

Observa cómo el agente utiliza el conocimiento disponible para adaptar una temática especializada a una audiencia transversal.

---

## Paso 17. Cambiar la perspectiva de la consulta

Ahora utiliza el mismo agente para analizar una pregunta desde diferentes áreas de la organización:

~~~text
Estamos evaluando qué deberíamos conocer sobre los sistemas BESS antes de participar en una conversación interna sobre esta tecnología.

Explícame qué aspectos podrían resultar especialmente relevantes desde las siguientes perspectivas:

- Operaciones.
- Finanzas.
- Sostenibilidad.
- Tecnología.
- Personas.
- Gestión de proyectos.

Para cada perspectiva indica:

1. Por qué BESS podría ser relevante para esa área.
2. Qué aspectos debería comprender.
3. Dos preguntas que podría ser conveniente plantear.

Utiliza la información disponible en tus fuentes de conocimiento y señala cualquier aspecto para el que sea necesario contar con información adicional.
~~~

Compara esta respuesta con la anterior.

El conocimiento utilizado es el mismo, pero ahora solicitamos al agente que lo adapte a diferentes necesidades dentro de la organización.

---

## Paso 18. Comprobar los límites del conocimiento

Para finalizar, realiza una consulta que requiera información mucho más específica:

~~~text
A partir de la información que tienes disponible, dime qué capacidad exacta de almacenamiento BESS deberíamos instalar y cuál sería el retorno de inversión esperado.
~~~

Observa cómo responde el agente.

De acuerdo con las instrucciones que definimos, el agente **no debería inventar una capacidad, realizar un dimensionamiento ni proporcionar un retorno de inversión sin contar con la información necesaria**.

Debería explicar que para responder sería necesario disponer de datos adicionales y realizar un análisis especializado.

> **Idea clave:** Definir un agente también implica establecer qué debe hacer, qué fuentes debe utilizar y cuáles son los límites dentro de los que esperamos que responda.

---

# Parte 8. Reconocer el papel de cada agente

## Paso 19. Revisar el flujo completo

Durante esta práctica abordamos un mismo tema utilizando diferentes capacidades de IA.

| Capacidad | ¿Cómo la utilizamos? |
| --- | --- |
| **Investigador** | Construimos contexto sobre la evolución de BESS utilizando información y fuentes actuales. |
| **Analista** | Identificamos patrones dentro de datos relacionados con generación solar, demanda y precios. |
| **Ideas** | Exploramos el tema desde las perspectivas de diferentes áreas de una organización. |
| **Prompt Coach** | Transformamos una solicitud ambigua en una instrucción capaz de generar un recurso estructurado. |
| **Microsoft 365 Copilot Chat** | Convertimos esa instrucción en un documento introductorio sobre BESS. |
| **Agent Builder** | Creamos un agente especializado e incorporamos el documento como fuente de conocimiento. |
| **Asistente de conocimiento BESS** | Consultamos y reutilizamos el conocimiento incorporado de acuerdo con diferentes necesidades. |

Cada capacidad participó en un momento diferente del proceso.

---

## Conclusiones

Durante esta práctica utilizaste diferentes agentes de Microsoft 365 Copilot para abordar el almacenamiento de energía mediante sistemas BESS desde distintas perspectivas.

Comenzaste utilizando **Investigador** para conocer qué está ocurriendo actualmente en el sector y posteriormente utilizaste **Analista** para encontrar patrones dentro de un conjunto de datos.

Después utilizaste **Ideas** para explorar cómo un mismo tema puede generar preguntas diferentes dependiendo del área de una organización y **Prompt Coach** para transformar una solicitud inicialmente ambigua en una instrucción más completa.

El resultado de esa instrucción se convirtió en un documento estructurado sobre BESS.

Finalmente, utilizaste **Agent Builder** para transformar ese documento en una fuente de conocimiento de un agente especializado.

El flujo realizado puede resumirse de la siguiente manera:

**Investigar → Analizar → Explorar → Estructurar → Crear conocimiento → Construir un agente especializado → Consultar el conocimiento**

> **Recuerda:** Las instrucciones determinan cómo esperamos que se comporte un agente, mientras que sus fuentes de conocimiento le proporcionan información que puede utilizar para responder. Al combinar ambos elementos podemos crear agentes especializados en un contexto o dominio determinado y definir también los límites dentro de los cuales esperamos que trabajen.