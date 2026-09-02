# Práctica 2. Seguimiento integral de una iniciativa de trabajo

**Duración:** 20 minutos  
**Herramientas:** Microsoft 365 Copilot Chat, Microsoft Outlook y Microsoft Teams  
**Archivos requeridos:**

- `Jornada_Generacion.xlsx`
- `Hilo_Outlook.md`
- `Conversacion_Teams.md`

---

## Objetivo

Preparar una actualización sobre el comportamiento de la generación eléctrica durante una jornada, recuperando y analizando información distribuida entre datos, comunicaciones y espacios de colaboración para identificar variaciones relevantes, acontecimientos reportados y temas pendientes, y consolidarlos en una visión clara que facilite el seguimiento entre diferentes áreas de la organización.

---

## Escenario

Es el inicio de una nueva jornada de trabajo. Durante el día anterior se registraron datos de generación de distintas instalaciones, se intercambiaron comunicaciones relacionadas con algunos acontecimientos y diferentes integrantes del equipo colaboraron en su seguimiento.

Antes de una reunión interna, necesitamos reconstruir rápidamente qué ocurrió:

- ¿Cómo se comportó la generación?
- ¿Qué variaciones relevantes se registraron?
- ¿Qué información adicional se ha comunicado?
- ¿Qué explicaciones han sido confirmadas y cuáles siguen siendo hipótesis?
- ¿Qué temas permanecen pendientes?
- ¿Qué acciones acordó realizar el equipo?

> **Importante:** Todos los datos, instalaciones, personas, eventos y conversaciones utilizados durante esta práctica son ficticios y fueron creados exclusivamente con fines de capacitación. No representan información operativa real de Generadora Metropolitana.

---

# Parte 1. Analizar los datos de la jornada con Copilot Chat

## Paso 1. Revisar el archivo de generación

Descarga y abre el archivo:

[`Jornada_Generacion.xlsx`](docs/Jornada_Generacion.xlsx)

Accede a la hoja **Jornada generación**.

El archivo contiene registros horarios correspondientes a cuatro instalaciones ficticias con diferentes tecnologías de generación.

Revisa las columnas disponibles:

- Fecha.
- Hora.
- Instalación.
- Tecnología.
- Generación esperada (MWh).
- Generación real (MWh).
- Desviación (MWh).
- Desviación (%).
- Disponibilidad (%).
- Estado.

El archivo contiene información de las 24 horas de la jornada para cada una de las cuatro instalaciones.

No es necesario revisar manualmente todos los registros.

Utilizaremos Copilot para ayudarnos a identificar los patrones y situaciones que merecen nuestra atención.

---

## Paso 2. Analizar la jornada

Accede a **Microsoft 365 Copilot Chat**.

Inicia una conversación nueva y adjunta el archivo:

[`Jornada_Generacion.xlsx`](docs/Jornada_Generacion.xlsx)

Utiliza el siguiente prompt:

~~~text
Analiza el archivo y ayúdame a reconstruir el comportamiento de la generación durante la jornada.

Identifica:

1. Las principales variaciones entre la generación esperada y la generación real.
2. Las horas en las que se produjeron las desviaciones más relevantes.
3. Las instalaciones que presentaron los cambios más importantes durante la jornada.
4. Los patrones que puedan observarse en los datos.
5. Las situaciones que sería conveniente investigar utilizando información adicional.

No atribuyas causas que no puedan demostrarse con los datos disponibles.

Presenta primero un resumen general de la jornada y después los 5 hallazgos que consideres más relevantes.

Para cada hallazgo incluye los datos que sustentan tu observación.
~~~

Espera a que Copilot complete el análisis.

---

## Paso 3. Revisar los principales hallazgos

Revisa los resultados obtenidos.

Presta especial atención a las diferencias encontradas entre las instalaciones.

Comprueba si Copilot identifica situaciones como:

- Un comportamiento relativamente estable durante gran parte de la jornada.
- Una disminución temporal de disponibilidad en una de las instalaciones.
- Diferencias importantes entre generación esperada y real durante determinados bloques horarios.
- Variaciones de generación que no están acompañadas por una disminución equivalente de disponibilidad.
- Un comportamiento diferente de la instalación solar dependiendo de la hora del día.

En este momento conocemos **qué muestran los datos**, pero todavía no necesariamente sabemos **por qué ocurrió cada variación**.

---

## Paso 4. Complementar el análisis con información de Internet

Mantente en la misma conversación.

Uno de los hallazgos debería mostrar diferencias entre la generación esperada y la generación real de la instalación solar durante determinadas horas.

Utilizaremos ahora información externa para comprender qué factores podrían estar relacionados con este tipo de comportamiento.

Utiliza el siguiente prompt:

~~~text
Uno de los hallazgos muestra diferencias entre la generación esperada y la generación real de la instalación solar durante determinadas horas del día.

Investiga en Internet qué factores pueden provocar variaciones en la generación de una planta solar fotovoltaica a lo largo de una jornada.

Utiliza fuentes confiables y recientes.

Después:

1. Resume los factores que encontraste.
2. Indica cuáles podrían ser compatibles con los patrones observados en nuestro archivo.
3. Distingue claramente entre lo que sabemos a partir de los datos y las posibles explicaciones encontradas en Internet.
4. Indica qué información adicional necesitaríamos para comprobar cualquiera de esas hipótesis.

Incluye las fuentes consultadas.
~~~

Revisa los resultados y las fuentes utilizadas por Copilot.

> **Importante:** Que una explicación encontrada en Internet sea compatible con nuestros datos no significa que sea la causa real de lo ocurrido.

En este punto podemos formular **hipótesis**, pero necesitamos otras fuentes de información para comprobarlas.

---

# Parte 2. Recuperar antecedentes desde Outlook

## Paso 5. Abrir el hilo de correos

Accede a **Microsoft Outlook** e identifica el correo llamado "**RE: Seguimiento jornada de generación – revisión de antecedentes**", o abre el archivo:  [`RE_Seguimiento jornada de generación – revisión de antecedentes`](docs/RE_Seguimiento_jornada.txt)

**RE: Seguimiento jornada de generación – revisión de antecedentes**

Este correo muestra un hilo de comunicaciones entre diferentes integrantes de un equipo que ha estado revisando la información de la jornada.

Lee únicamente el mensaje más reciente. No es necesario revisar manualmente toda la conversación.

Utilizaremos Copilot para recuperar los antecedentes relevantes del hilo.

---

## Paso 6. Analizar la conversación con Copilot en Outlook

Utiliza Copilot en Outlook o en M365 Copilot para analizar la conversación.

Solicita:

~~~text
Resume este hilo para preparar la reunión de seguimiento.

Identifica:

1. Los eventos confirmados.
2. Las posibles explicaciones que todavía no han sido comprobadas.
3. Los puntos que permanecen pendientes.
4. Las personas que aportaron información sobre cada situación.
5. Los temas que deberían incluirse en la reunión.

No conviertas hipótesis o posibilidades mencionadas en los correos en hechos confirmados.
~~~

Revisa el resultado.

---

## Paso 7. Contrastar los correos con el análisis de los datos

Compara mentalmente la información recuperada en Outlook con los hallazgos que obtuviste anteriormente a partir del archivo de Excel.

Observa cómo algunos de los datos ahora cuentan con información adicional.

Por ejemplo:

- Una disminución temporal de disponibilidad puede estar relacionada con una actividad previamente comunicada.
- Las desviaciones de la instalación solar coinciden parcialmente con información relacionada con condiciones meteorológicas.
- Existen variaciones para las que todavía no se ha encontrado una explicación.
- Algunos comportamientos requieren continuar siendo investigados.

Presta especial atención a las expresiones utilizadas en los correos:

**“se confirmó”**, **“podría estar relacionado”**, **“coincide temporalmente”**, **“queda pendiente”** o **“todavía no sabemos”** no significan lo mismo.

> **Idea clave:** Los datos pueden mostrarnos una variación, mientras que las comunicaciones pueden proporcionar el contexto necesario para comprenderla. Aun así, debemos distinguir entre información confirmada e hipótesis.

---

# Parte 3. Recuperar acuerdos desde Teams

## Paso 8. Abrir la conversación de seguimiento

Accede a **Microsoft Teams** e identifica la conversación de seguimiento llamada "**Seguimiento jornada de generación**", o abre el archivo: [`Conversacion_Teams.txt`](docs/Conversacion_Teams.txt)

La conversación ocurre después de que el equipo revisó los datos y los antecedentes enviados por correo.

Ahora el objetivo ya no es únicamente comprender qué ocurrió, sino identificar **qué decidió hacer el equipo a partir de esa información**.

---

## Paso 9. Recuperar acuerdos y próximos pasos

Utiliza Copilot en Teams sobre la conversación.

Solicita:

~~~text
Ayúdame a preparar el seguimiento de esta conversación.

Identifica:

- Los principales acuerdos.
- Los temas que continúan abiertos.
- Los responsables de cada seguimiento.
- Los plazos mencionados.
- Las decisiones tomadas para la reunión.
- Cualquier punto donde el equipo haya indicado que todavía falta información.

Finaliza con una lista de próximos pasos organizada por responsable.
~~~

Revisa la respuesta generada.

Comprueba especialmente si Copilot logra identificar:

- Qué personas tienen actividades pendientes.
- Qué situaciones continúan abiertas.
- Qué información deberá revisarse posteriormente.
- Cómo acordó el equipo presentar los resultados.
- Qué elementos no deben presentarse todavía como conclusiones definitivas.

---

# Parte 4. Integrar la información

## Paso 10. Preparar la actualización para la reunión

Hasta este momento hemos utilizado diferentes fuentes de información:

- Los **datos** permitieron identificar qué ocurrió durante la jornada.
- La **información externa** permitió conocer posibles explicaciones que debían investigarse.
- Los **correos** aportaron antecedentes y contexto adicional.
- La **conversación del equipo** permitió recuperar acuerdos, responsables y próximos pasos.

Regresa a **Microsoft 365 Copilot Chat**.

Utiliza los hallazgos obtenidos durante la práctica para preparar la actualización final.

Puedes proporcionar a Copilot los resultados relevantes recuperados desde Outlook y Teams y solicitar:

~~~text
Ayúdame a preparar una actualización ejecutiva para la reunión de seguimiento de la jornada de generación utilizando la información que hemos revisado.

Organiza el resultado en las siguientes secciones:

1. Panorama general de la jornada.
2. Principales variaciones observadas.
3. Acontecimientos relevantes reportados.
4. Situaciones que cuentan con una explicación confirmada.
5. Situaciones donde existe una posible explicación que todavía debe validarse.
6. Pendientes y responsables.
7. Próximos pasos.

Finaliza con tres preguntas que convendría resolver durante la reunión.

Distingue claramente entre hechos confirmados, hipótesis y aspectos que todavía requieren investigación.

No agregues causas, eventos o conclusiones que no estén sustentados por la información proporcionada.
~~~

Revisa el resultado final.

---

## Paso 11. Identificar dónde se encontraba el contexto

Reflexiona sobre el recorrido realizado durante la práctica.

La información necesaria para completar una actividad de trabajo no siempre se encuentra en un único lugar.

| Necesidad | Contexto utilizado |
| --- | --- |
| Comprender el comportamiento de la jornada | Datos del archivo de Excel |
| Ampliar la comprensión de un fenómeno | Información disponible en Internet |
| Recuperar antecedentes y comunicaciones | Outlook |
| Identificar acuerdos y próximos pasos | Teams |
| Preparar una visión integrada | Microsoft 365 Copilot Chat |

Cada fuente aportó una perspectiva diferente sobre el mismo escenario.

---

## Conclusiones

Durante esta práctica utilizaste Microsoft 365 Copilot en diferentes momentos de una misma actividad de trabajo.

Comenzaste analizando un conjunto amplio de datos para identificar las situaciones que merecían atención. Posteriormente utilizaste información disponible en Internet para ampliar el contexto de uno de los hallazgos y formular posibles explicaciones.

Después recuperaste antecedentes desde las comunicaciones y utilizaste una conversación de colaboración para identificar acuerdos, responsables y próximos pasos.

Finalmente, integraste los principales hallazgos para preparar una actualización de seguimiento.

> **Recuerda:** No siempre necesitamos comenzar copiando toda nuestra información a un chat. Identifica dónde se encuentra el contexto que necesitas y utiliza Copilot para recuperar, analizar y transformar esa información de acuerdo con el resultado que quieres conseguir.

También recuerda que una posible explicación no debe presentarse como un hecho únicamente porque sea compatible con los datos. Utiliza las diferentes fuentes disponibles para contrastar información y validar las conclusiones generadas con ayuda de IA.