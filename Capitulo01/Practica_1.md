# Práctica 1. Obtención de resultados más precisos con IA

**Duración:** 6 minutos  
**Herramientas:** Microsoft 365 Copilot Chat y Microsoft Excel  
**Archivo requerido:** [`Desempeno_Generacion.xlsx`](docs/Desempeno_Generacion.xlsx)

---

## Objetivo

Analizar información ficticia sobre el desempeño mensual de una instalación de generación eléctrica para identificar variaciones y aspectos relevantes, comprobando cómo la incorporación de un objetivo claro, contexto, instrucciones específicas y un resultado esperado permite obtener respuestas más precisas y útiles para el análisis de información.

---

## Escenario

Una empresa del sector de generación de energía eléctrica realiza un seguimiento mensual de algunos de sus indicadores de desempeño.

Para preparar una reunión de revisión, se cuenta con un archivo de Excel que contiene información de los últimos seis meses sobre:

- Generación real.
- Meta de generación.
- Disponibilidad.
- Horas de indisponibilidad.

Durante la práctica se utilizará Microsoft 365 Copilot Chat para analizar esta información y comparar los resultados obtenidos mediante una solicitud general y una solicitud que proporcione mayor contexto e instrucciones.

Finalmente, los hallazgos obtenidos se transformarán en un reporte ejecutivo que pueda utilizarse como entregable para una reunión de seguimiento.

---

## Paso 1. Revisar el archivo de trabajo

1. Descarga y abre el archivo [`Desempeno_Generacion.xlsx`](docs/Desempeno_Generacion.xlsx).
2. Accede a la hoja **Desempeño mensual**.
3. Revisa brevemente la información incluida en el archivo.
4. Identifica las columnas disponibles:
   - Mes.
   - Generación real (MWh).
   - Meta de generación (MWh).
   - Disponibilidad (%).
   - Horas de indisponibilidad.

No realices cálculos adicionales. El archivo se utilizará como fuente de información para las siguientes solicitudes.

---

## Paso 2. Iniciar una conversación en Copilot Chat

1. Accede a **Microsoft 365 Copilot Chat**.
2. Inicia una conversación nueva.
3. Adjunta el archivo [`Desempeno_Generacion.xlsx`](docs/Desempeno_Generacion.xlsx).
4. Verifica que el archivo aparezca como parte del contexto de la conversación.

---

## Paso 3. Realizar una solicitud general

Escribe el siguiente prompt:

~~~text
Analiza este archivo y dime qué observas.
~~~

Espera a que Copilot genere la respuesta.

### Observa el resultado

Antes de continuar, revisa la respuesta e identifica:

- ¿Qué información decidió analizar Copilot?
- ¿Qué datos consideró más importantes?
- ¿Cómo organizó la respuesta?
- ¿Identificó variaciones o patrones?
- ¿El resultado responde necesariamente a lo que necesitarías para una reunión de seguimiento?

La solicitud es válida, pero deja varias decisiones abiertas a Copilot: no establece para qué necesitamos el análisis, qué debe buscar ni cómo queremos recibir el resultado.

---

## Paso 4. Proporcionar un objetivo y mayor contexto

Inicia una **nueva conversación** y vuelve a adjuntar el mismo archivo.

Ahora utiliza un prompt que proporcione a Copilot mayor información sobre la tarea que debe realizar.

~~~text
Objetivo:
Ayúdame a identificar los aspectos más relevantes del desempeño registrado durante los últimos seis meses para preparar una reunión de seguimiento.

Contexto:
Los datos corresponden a una instalación ficticia de una empresa del sector de generación de energía eléctrica.

Instrucciones:
Compara la generación real contra la meta de generación e identifica los meses con las mayores desviaciones.

Analiza también la disponibilidad y las horas de indisponibilidad para determinar si existen patrones o relaciones que deban llamar nuestra atención.

Utiliza únicamente la información disponible en el archivo. No atribuyas causas a las variaciones si los datos no permiten demostrarlas.

Resultado esperado:
Presenta los 3 hallazgos más relevantes.

Para cada hallazgo indica:
- Qué observaste.
- Qué datos sustentan la observación.
- Por qué merece atención.
~~~

Espera a que Copilot complete el análisis.

### Observa el nuevo resultado

Revisa si ahora es más sencillo identificar:

- Los meses que presentan mayores desviaciones.
- Las diferencias entre generación real y meta.
- Los cambios en disponibilidad.
- Las variaciones en las horas de indisponibilidad.
- Las posibles relaciones entre los indicadores.

---

## Paso 5. Convertir el análisis en un entregable

Una vez obtenidos los hallazgos, continúa trabajando en la **misma conversación**.

Solicita a Copilot que transforme los resultados obtenidos en un documento que pueda utilizarse para compartir la información con otras personas.

Utiliza el siguiente prompt:

~~~text
A partir del análisis anterior, prepara un reporte ejecutivo que pueda utilizarse para presentar los resultados en una reunión de seguimiento.

El reporte debe incluir:

1. Título: Reporte de desempeño mensual.
2. Un breve resumen ejecutivo de máximo 100 palabras.
3. Una sección con los 3 principales hallazgos identificados.
4. Una tabla comparativa con los indicadores más relevantes que sustentan los hallazgos.
5. Una sección denominada "Aspectos que requieren atención".
6. Tres preguntas que sería conveniente discutir durante la reunión.

Utiliza un lenguaje ejecutivo, claro y conciso.

Genera el resultado como un documento que pueda abrirse y editarse en Microsoft Word.
~~~

Espera a que Copilot genere el resultado.

> **Nota:** Dependiendo de las capacidades disponibles en el entorno de Microsoft 365 Copilot, la opción para crear, descargar o abrir el resultado como un archivo puede presentarse de forma diferente. Si la generación directa del documento no está disponible, utiliza el contenido generado por Copilot como base para crear el reporte en Microsoft Word.

---

## Paso 6. Revisar el reporte generado

Abre el documento generado y revisa brevemente su contenido.

Comprueba que el reporte:

- Utiliza los datos proporcionados durante la práctica.
- Conserva los principales hallazgos identificados previamente.
- Presenta la información con una estructura adecuada para compartirla.
- Incluye evidencia que sustente los hallazgos.
- Diferencia los datos observados de posibles interpretaciones.
- No incorpora causas o explicaciones que no puedan sustentarse con la información disponible.

Observa cómo una misma conversación puede avanzar desde el **análisis de información** hasta su transformación en un **entregable que puede utilizarse para continuar trabajando**.

> **Idea clave:** El resultado esperado puede definir no solo cómo queremos visualizar una respuesta, sino también el tipo de entregable que necesitamos obtener a partir de ella.

---

## Paso 7. Identificar los límites del análisis

Finalmente, revisa si Copilot distingue entre una **observación sustentada por los datos** y una **explicación que requeriría información adicional**.

Por ejemplo, a partir del archivo sería posible obtener una observación como:

> Durante abril se observa una disminución de la generación acompañada de una menor disponibilidad y un incremento de las horas de indisponibilidad.

Esta conclusión puede contrastarse directamente con los indicadores disponibles en el archivo.

Sin embargo, una afirmación como la siguiente requeriría información adicional:

> La generación disminuyó en abril debido a una falla de mantenimiento.

El archivo no contiene información sobre las causas de la indisponibilidad. Por lo tanto, Copilot no debería atribuir la variación a mantenimiento, fallas técnicas u otra causa específica basándose únicamente en estos datos.

---

## Conclusiones

Durante esta práctica comprobaste que proporcionar instrucciones más claras permite orientar mejor el análisis realizado por Microsoft 365 Copilot.

Un prompt efectivo no tiene que ser simplemente más largo. Debe proporcionar la información necesaria para que Copilot comprenda:

- **Objetivo:** ¿Para qué necesitas el resultado?
- **Contexto:** ¿Qué necesita saber para comprender la tarea?
- **Instrucciones:** ¿Qué quieres que haga con la información?
- **Resultado esperado:** ¿Cómo necesitas recibir o utilizar la respuesta?

También observaste la importancia de validar los resultados generados por inteligencia artificial y diferenciar entre los hallazgos sustentados por los datos y las interpretaciones que requieren información adicional.

> **Recuerda:** Proporciona a Copilot las instrucciones y el contexto necesarios para obtener el resultado que necesitas.