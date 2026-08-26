# Práctica: El instructor mostrará cómo mejorar los resultados de Microsoft 365 Copilot mediante técnicas de prompting y el uso adecuado del contexto, utilizando ejemplos relacionados con actividades de una empresa del sector de generación de energía eléctrica utilizando Copilot Chat.

## Metadatos

| Campo | Valor |
|---|---|
| Duración | 6 minutos |
| Complejidad | Fácil |
| Nivel de Bloom | Aplicar |

## Descripción general

En esta práctica, el instructor demuestra cómo la calidad de una respuesta de Microsoft 365 Copilot depende de la claridad del prompt, del contexto disponible y de las fuentes de trabajo autorizadas. Se comparará una solicitud ambigua con un prompt estructurado para analizar la situación operativa de la Central Solar Andes de la empresa ficticia Energía Horizonte S.A.

Como resultado, se generará y almacenará en OneDrive for Business el documento `01_Prompts_validados_Energia_Horizonte.docx`. Este archivo se reutilizará en prácticas posteriores, por lo que debe guardarse exclusivamente en la ruta de laboratorio establecida.

## Objetivos de aprendizaje

Al finalizar esta práctica, el participante podrá:

- [ ] Explicar por qué Copilot puede producir respuestas distintas ante solicitudes similares.
- [ ] Aplicar una estructura de prompt con objetivo, contexto, datos de entrada, restricciones, formato y criterio de validación.
- [ ] Usar Copilot Chat con datos de trabajo para analizar el archivo operativo de la Central Solar Andes.
- [ ] Solicitar una tabla priorizada de riesgos operativos fundamentada en una fuente específica.
- [ ] Crear y guardar un documento reutilizable de prompts validados en OneDrive for Business.

## Requisitos previos

### Conocimientos requeridos

- Conocimiento básico de Microsoft 365 Copilot y de la interfaz de Copilot Chat.
- Comprensión de que Copilot genera texto probabilísticamente y que sus resultados requieren revisión humana.
- Capacidad para identificar información que debe verificarse, especialmente cifras, fechas, responsables, compromisos y decisiones operativas.
- Conocimiento básico de OneDrive for Business y Microsoft Word para la Web.

### Accesos requeridos

Antes de iniciar, confirme que dispone de los siguientes accesos:

- Inicio de sesión activo en `https://m365.cloud.microsoft/`.
- Cuenta del tenant de laboratorio **Tenant-EnergiaHorizonte**:
  - Instructor predeterminado: `instructor.copilot@tenant-energiahorizonte.onmicrosoft.com`
  - Cuenta de referencia del alumno: `alumno01.copilot@tenant-energiahorizonte.onmicrosoft.com`
- Permisos de lectura y escritura en OneDrive for Business.
- Acceso a Copilot Chat con capacidad para usar datos de trabajo, cuando esté habilitado por la licencia y configuración del tenant.
- Disponibilidad del archivo de origen:

```text
/CopilotLabs/EnergiaHorizonte/01_Informe_operativo_Central_Solar_Andes.docx
```

## Entorno de laboratorio

### Tenant, ubicación y archivos obligatorios

| Elemento | Valor obligatorio |
|---|---|
| Tenant de laboratorio | `Tenant-EnergiaHorizonte` |
| Ruta de trabajo en OneDrive | `/CopilotLabs/EnergiaHorizonte/` |
| Archivo fuente de esta práctica | `01_Informe_operativo_Central_Solar_Andes.docx` |
| Archivo que se creará | `01_Prompts_validados_Energia_Horizonte.docx` |
| Política de almacenamiento | No guardar archivos del laboratorio fuera de la ruta indicada. |

> **Importante:** No utilice cuentas personales, OneDrive personal ni un tenant distinto. Copilot solo puede fundamentar respuestas en contenido al que la cuenta autenticada tenga permiso de acceso.

### Hardware recomendado

| Componente | Requisito |
|---|---|
| Equipo | Windows 11 Pro de 64 bits |
| Procesador | Intel Core i5 de 11.ª generación o equivalente |
| Memoria | 16 GB de RAM disponibles |
| Almacenamiento | 10 GB de espacio libre |
| Pantalla | Resolución mínima de 1920 × 1080 |
| Red | Mínimo 25 Mbps de descarga y 5 Mbps de carga |
| Audio | Auriculares con micrófono opcionales para dictado o accesibilidad |

### Software y servicios

| Componente | Referencia del laboratorio |
|---|---|
| Sistema operativo | Windows 11 Pro 23H2, compilación 22631.4890 |
| Microsoft 365 Apps | Versión 2502, compilación 16.0.18526.20208 |
| Navegador | Google Chrome 134.0.6998.89 o Microsoft Edge actualizado |
| Copilot Chat | Experiencia web de Microsoft 365 fijada al 2026-08-26 |
| OneDrive for Business | Servicio SaaS fijado al 2026-08-26 |

### Comprobación inicial

1. Abra el navegador e inicie sesión en:

   ```text
   https://m365.cloud.microsoft/
   ```

2. Compruebe que la cuenta mostrada pertenece al tenant `tenant-energiahorizonte.onmicrosoft.com`.

3. Abra **OneDrive** desde el lanzador de aplicaciones de Microsoft 365.

4. Navegue a la siguiente ruta:

   ```text
   /CopilotLabs/EnergiaHorizonte/
   ```

5. Verifique que están disponibles los archivos iniciales:

   ```text
   01_Informe_operativo_Central_Solar_Andes.docx
   02_Datos_generacion_y_disponibilidad.xlsx
   ```

6. Mantenga abierta una pestaña de OneDrive y abra una segunda pestaña para Copilot Chat. Esta disposición permite consultar simultáneamente el documento fuente y la conversación con Copilot.

## Procedimiento paso a paso

### Paso 1. Identificar los factores que afectan la respuesta de Copilot

**Objetivo:** Relacionar la variabilidad de las respuestas con la redacción del prompt, el contexto conversacional, las fuentes disponibles, los permisos y la naturaleza probabilística del modelo.

**Instrucciones:**

1. Abra **Copilot Chat** desde `https://m365.cloud.microsoft/`.

2. Si la interfaz ofrece un selector de modo o contexto, seleccione la opción que permita trabajar con **datos de trabajo** o contenido organizacional autorizado. No seleccione un modo público si el objetivo es fundamentar la respuesta en documentos de OneDrive.

3. Inicie una conversación nueva para evitar que un historial anterior afecte el resultado de la demostración.

4. Introduzca el siguiente prompt ambiguo:

   ```text
   Resume la situación de la planta.
   ```

5. Revise la respuesta sin asumir que corresponde necesariamente a la Central Solar Andes. Identifique si Copilot:
   - Solicita una aclaración.
   - Ofrece una respuesta general.
   - Interpreta una planta o fuente distinta.
   - No cita una fuente concreta.

6. Explique al grupo que una solicitud ambigua deja sin definir aspectos críticos: planta, periodo, indicadores, audiencia, fuente autorizada, formato y objetivo de decisión.

7. Destaque que dos respuestas pueden ser distintas incluso con prompts similares por los siguientes factores:

   - La redacción exacta de la solicitud.
   - El historial de la conversación.
   - El documento adjunto, abierto o recuperado como contexto.
   - Los datos de trabajo que hayan cambiado desde una ejecución anterior.
   - Los permisos del usuario.
   - La aplicación desde la que se realiza la petición.
   - La generación probabilística del modelo.

**Salida esperada:**

Una respuesta general, una solicitud de aclaración o una respuesta con alcance insuficiente para tomar decisiones operativas. La salida no debe considerarse válida para una comunicación de operación sin comprobar fuentes y datos.

**Verificación:**

Confirme que puede explicar, como mínimo, tres motivos por los que la misma pregunta no garantiza una respuesta idéntica:

- El contexto disponible puede ser diferente.
- El modelo puede elegir formulaciones o énfasis alternativos.
- La redacción ambigua permite interpretaciones distintas.

---

### Paso 2. Preparar un prompt estructurado y fundamentado

**Objetivo:** Construir una solicitud que reduzca la ambigüedad mediante objetivo, contexto, datos de entrada, restricciones, formato esperado y criterio de validación.

**Instrucciones:**

1. En OneDrive, localice el archivo:

   ```text
   01_Informe_operativo_Central_Solar_Andes.docx
   ```

2. Revise de forma breve el nombre del archivo y confirme que corresponde a la Central Solar Andes. No es necesario leerlo por completo antes de la demostración.

3. En Copilot Chat, use la función disponible para **adjuntar**, **agregar contenido** o **referenciar un archivo de OneDrive**.

4. Seleccione el documento:

   ```text
   /CopilotLabs/EnergiaHorizonte/01_Informe_operativo_Central_Solar_Andes.docx
   ```

5. Confirme visualmente que el archivo aparece asociado al mensaje antes de enviar el prompt.

6. Copie y pegue el siguiente prompt estructurado:

   ```text
   Objetivo: preparar un resumen operativo para la responsable de Operaciones de Energía Horizonte S.A.

   Contexto: analiza exclusivamente la situación de la Central Solar Andes durante el periodo descrito en el documento adjunto.

   Datos de entrada: utiliza únicamente el archivo 01_Informe_operativo_Central_Solar_Andes.docx adjunto a esta conversación.

   Restricciones:
   - No inventes cifras, fechas, causas, responsables ni acciones.
   - Si un dato no aparece o no puede confirmarse en la fuente, indícalo explícitamente como "No confirmado en la fuente".
   - No uses información de otros proyectos, plantas o conversaciones.
   - Mantén un tono profesional, objetivo y orientado a la operación.

   Formato esperado:
   1. Un resumen de cinco viñetas.
   2. Una tabla con las columnas: indicador o evento, situación reportada, impacto operativo y evidencia en la fuente.
   3. Una sección final titulada "Datos que requieren validación humana".

   Criterio de validación:
   Incluye referencias o citas al documento cuando estén disponibles y separa claramente los hechos documentados de las inferencias.
   ```

7. Envíe el prompt y espere la respuesta.

8. Revise si Copilot muestra citas, referencias, vínculos o indicadores del documento utilizado. La forma exacta de presentación puede variar según la experiencia de Copilot disponible en el tenant.

**Salida esperada:**

Una respuesta organizada en cinco viñetas, una tabla de situación operativa y una sección de validación humana. La respuesta debe indicar que utiliza el archivo adjunto como fuente y no debe presentar datos no sustentados como hechos.

**Verificación:**

Compruebe los siguientes criterios:

| Criterio | Resultado esperado |
|---|---|
| Fuente delimitada | La respuesta se basa en el archivo adjunto. |
| Audiencia definida | El tono es adecuado para Operaciones. |
| Formato solicitado | Incluye viñetas, tabla y sección final. |
| Transparencia | Señala información no confirmada o ausente. |
| Fundamentación | Muestra citas, referencias o evidencia cuando la experiencia lo permita. |

> **Punto de instrucción:** Una respuesta bien redactada no equivale automáticamente a una respuesta correcta. Las cifras, fechas, responsables, eventos de indisponibilidad y acciones operativas deben verificarse en el documento original antes de utilizarlos en una decisión o comunicación formal.

---

### Paso 3. Solicitar y revisar una tabla de riesgos operativos priorizados

**Objetivo:** Aplicar el contexto del documento para generar una tabla de riesgos útil, delimitada y revisable.

**Instrucciones:**

1. Mantenga el archivo adjunto y la conversación actual para conservar el contexto.

2. Envíe el siguiente prompt de seguimiento:

   ```text
   A partir exclusivamente del archivo adjunto, identifica los riesgos operativos mencionados o razonablemente derivados de hechos documentados para la Central Solar Andes.

   Presenta una tabla con estas columnas:
   - Prioridad: Alta, Media o Baja.
   - Riesgo operativo.
   - Evidencia o hecho que lo sustenta.
   - Posible impacto en generación, disponibilidad o seguridad.
   - Acción de seguimiento propuesta.
   - Estado de confirmación: Documentado en la fuente, Inferencia que requiere validación o No confirmado.

   Reglas:
   - Prioriza por impacto potencial y urgencia descrita en el documento.
   - No atribuyas responsables ni fechas si no están indicados en la fuente.
   - No presentes una inferencia como un hecho confirmado.
   - Finaliza con una nota que indique qué elementos debe validar la responsable de Operaciones antes de actuar.
   ```

3. Revise la tabla generada.

4. Compare al menos un riesgo de prioridad alta o media con el contenido del documento de Word. Abra el documento en OneDrive si es necesario.

5. Identifique una de estas condiciones:
   - El riesgo está explícitamente documentado.
   - El riesgo es una inferencia plausible, pero requiere confirmación.
   - La respuesta no dispone de evidencia suficiente y debe corregirse o eliminarse.

6. Si detecta un dato no sustentado, solicite una corrección a Copilot usando este prompt:

   ```text
   Revisa la fila indicada. Conserva únicamente afirmaciones sustentadas por el documento adjunto. Si no existe evidencia suficiente, cambia el estado a "No confirmado" y explica brevemente la limitación.
   ```

**Salida esperada:**

Una tabla de riesgos priorizados que diferencie entre información documentada, inferencias y datos no confirmados. Debe incluir una nota explícita de validación humana.

**Verificación:**

La tabla se considera apta como borrador de trabajo si cumple todas las condiciones siguientes:

- Cada riesgo tiene evidencia o una declaración explícita de limitación.
- Las prioridades no se presentan como hechos absolutos si el documento no establece una prioridad.
- Las acciones propuestas se distinguen de las acciones ya comprometidas en la fuente.
- La salida no contiene cifras, responsables o fechas inventadas.
- Al menos un elemento fue contrastado manualmente con el archivo fuente.

---

### Paso 4. Crear el documento reutilizable de prompts validados

**Objetivo:** Guardar en OneDrive un documento que conserve los prompts estructurados y los criterios de uso para las prácticas posteriores.

**Instrucciones:**

1. Vuelva a OneDrive y confirme que se encuentra en:

   ```text
   /CopilotLabs/EnergiaHorizonte/
   ```

2. Seleccione **Nuevo** > **Documento de Word**.

3. Asigne al documento el siguiente nombre exacto:

   ```text
   01_Prompts_validados_Energia_Horizonte.docx
   ```

4. Abra el documento recién creado e incluya el siguiente contenido. Puede copiarlo y pegarlo en Word para la Web.

   ```text
   PROMPTS VALIDADOS – ENERGÍA HORIZONTE S.A.

   Propósito
   Reutilizar prompts estructurados para analizar información operativa de la Central Solar Andes mediante Microsoft 365 Copilot, manteniendo la trazabilidad hacia las fuentes y la validación humana de información crítica.

   Prompt 1 – Resumen operativo fundamentado

   Objetivo: preparar un resumen operativo para la responsable de Operaciones de Energía Horizonte S.A.

   Contexto: analiza exclusivamente la situación de la Central Solar Andes durante el periodo descrito en el documento adjunto.

   Datos de entrada: utiliza únicamente el archivo 01_Informe_operativo_Central_Solar_Andes.docx adjunto a esta conversación.

   Restricciones:
   - No inventes cifras, fechas, causas, responsables ni acciones.
   - Si un dato no aparece o no puede confirmarse en la fuente, indícalo explícitamente como "No confirmado en la fuente".
   - No uses información de otros proyectos, plantas o conversaciones.
   - Mantén un tono profesional, objetivo y orientado a la operación.

   Formato esperado:
   1. Un resumen de cinco viñetas.
   2. Una tabla con las columnas: indicador o evento, situación reportada, impacto operativo y evidencia en la fuente.
   3. Una sección final titulada "Datos que requieren validación humana".

   Criterio de validación:
   Incluye referencias o citas al documento cuando estén disponibles y separa claramente los hechos documentados de las inferencias.

   Prompt 2 – Riesgos operativos priorizados

   A partir exclusivamente del archivo adjunto, identifica los riesgos operativos mencionados o razonablemente derivados de hechos documentados para la Central Solar Andes.

   Presenta una tabla con estas columnas:
   - Prioridad: Alta, Media o Baja.
   - Riesgo operativo.
   - Evidencia o hecho que lo sustenta.
   - Posible impacto en generación, disponibilidad o seguridad.
   - Acción de seguimiento propuesta.
   - Estado de confirmación: Documentado en la fuente, Inferencia que requiere validación o No confirmado.

   Reglas:
   - Prioriza por impacto potencial y urgencia descrita en el documento.
   - No atribuyas responsables ni fechas si no están indicados en la fuente.
   - No presentes una inferencia como un hecho confirmado.
   - Finaliza con una nota que indique qué elementos debe validar la responsable de Operaciones antes de actuar.

   Lista de verificación antes de usar una respuesta de Copilot
   - Confirmar que la fuente utilizada es la correcta.
   - Verificar cifras, fechas, responsables y compromisos en el documento original.
   - Distinguir hechos documentados de inferencias.
   - Confirmar que el formato y el tono corresponden a la audiencia.
   - No usar el resultado como decisión operativa sin revisión humana.
   ```

5. Compruebe que Word para la Web guarda los cambios automáticamente.

6. Cierre el documento y actualice la vista de OneDrive si es necesario.

**Salida esperada:**

El archivo `01_Prompts_validados_Energia_Horizonte.docx` aparece en la carpeta `/CopilotLabs/EnergiaHorizonte/` y contiene dos prompts estructurados junto con una lista de verificación de validación humana.

**Verificación:**

En OneDrive, confirme lo siguiente:

- El nombre del archivo es exactamente `01_Prompts_validados_Energia_Horizonte.docx`.
- El archivo está ubicado en `/CopilotLabs/EnergiaHorizonte/`.
- El documento contiene los apartados **Prompt 1**, **Prompt 2** y **Lista de verificación antes de usar una respuesta de Copilot**.
- El archivo puede abrirse sin errores con la cuenta del laboratorio.

## Validación y pruebas

Realice la siguiente validación final antes de dar por terminada la práctica.

| Prueba | Método | Resultado aprobado |
|---|---|---|
| Validación de tenant | Revise la cuenta activa en Microsoft 365. | La cuenta pertenece a `Tenant-EnergiaHorizonte`. |
| Validación de fuente | Confirme que el archivo adjunto en Copilot Chat es `01_Informe_operativo_Central_Solar_Andes.docx`. | La respuesta se fundamenta en el archivo operativo correcto. |
| Validación de estructura del prompt | Revise el prompt utilizado. | Incluye objetivo, contexto, datos de entrada, restricciones, formato y criterio de validación. |
| Validación de respuesta | Revise el resumen y la tabla de riesgos. | Distinguen hechos, inferencias y datos no confirmados. |
| Validación humana | Compare al menos un riesgo con el documento fuente. | La evidencia coincide con el contenido original o se marca como no confirmada. |
| Validación de archivo generado | Abra el documento de prompts en OneDrive. | El archivo se guarda con el nombre y ruta obligatorios. |

Use esta pregunta de cierre para el grupo:

> ¿Qué cambiaría en el resultado si se elimina el documento adjunto, se cambia la audiencia o se pide un formato distinto?

La respuesta esperada es que Copilot podría cambiar el alcance, las prioridades, el tono, las fuentes recuperadas y la estructura de la salida. Por ello, el prompt y el contexto deben declararse de forma explícita cuando el resultado vaya a utilizarse en actividades operativas.

## Solución de problemas

### Problema 1: Copilot no permite adjuntar el archivo o responde sin usar datos de trabajo

**Síntomas:** No aparece la opción para adjuntar contenido de OneDrive, el archivo no se puede seleccionar, o Copilot produce una respuesta genérica sin referencias al informe operativo.

**Causa:** Se ha abierto Copilot en un modo sin datos de trabajo, la sesión pertenece a otro tenant, la cuenta no tiene permiso sobre el archivo o la funcionalidad está restringida por la configuración de licencias y directivas del tenant.

**Solución:**

1. Confirme que inició sesión con `instructor.copilot@tenant-energiahorizonte.onmicrosoft.com` o con la cuenta de laboratorio asignada.
2. Abra OneDrive y compruebe que puede abrir directamente `01_Informe_operativo_Central_Solar_Andes.docx`.
3. Inicie una conversación nueva en Copilot Chat y seleccione el modo de datos de trabajo si está disponible.
4. Vuelva a adjuntar el archivo desde la ruta obligatoria.
5. Si el problema persiste, solicite al administrador del tenant que revise la licencia de Copilot, los permisos de OneDrive y las políticas de acceso a datos de trabajo.

### Problema 2: La tabla de riesgos contiene datos sin evidencia, fechas inventadas o responsables no confirmados

**Síntomas:** La respuesta parece convincente, pero incluye información que no se encuentra en el informe o presenta inferencias como hechos confirmados.

**Causa:** El modelo generativo puede completar información plausible cuando el contexto es incompleto, ambiguo o insuficiente. Una salida fluida no garantiza exactitud ni fundamentación.

**Solución:**

1. Compare las filas críticas con el documento original, especialmente riesgos de prioridad alta, cifras, fechas y responsables.
2. Solicite una revisión con un prompt restrictivo, por ejemplo:

   ```text
   Revisa la respuesta exclusivamente contra el documento adjunto. Elimina toda afirmación sin evidencia textual. Marca como "Inferencia que requiere validación" cualquier conclusión no declarada explícitamente en la fuente.
   ```

3. Corrija manualmente el resultado si sigue existiendo información no sustentada.
4. No use la tabla para decisiones, comunicaciones externas o asignación de acciones hasta completar la validación humana.

## Limpieza

1. Confirme que el archivo generado permanece en la ruta obligatoria:

   ```text
   /CopilotLabs/EnergiaHorizonte/01_Prompts_validados_Energia_Horizonte.docx
   ```

2. No elimine los archivos de entrada ni el documento de prompts validados; serán necesarios en las prácticas siguientes.

3. Cierre las pestañas de Copilot Chat y Word para la Web cuando haya confirmado el guardado automático.

4. Cierre sesión únicamente si así lo establece el procedimiento del laboratorio o si utiliza un equipo compartido.

5. No descargue ni copie los archivos a ubicaciones personales fuera de `/CopilotLabs/EnergiaHorizonte/`.

## Resumen

En esta práctica se demostró que Copilot no produce necesariamente la misma respuesta ante prompts similares porque intervienen la redacción, el historial de conversación, los datos disponibles, los permisos, la aplicación utilizada y la naturaleza probabilística del modelo.

También se aplicó una estructura de prompt reutilizable basada en:

1. Objetivo.
2. Contexto.
3. Datos de entrada o fuentes permitidas.
4. Restricciones.
5. Formato esperado.
6. Criterio de validación.

El resultado principal es el documento:

```text
/CopilotLabs/EnergiaHorizonte/01_Prompts_validados_Energia_Horizonte.docx
```

Este documento se utilizará posteriormente para crear un resumen ejecutivo y como fuente de conocimiento controlado para un agente personalizado. Antes de utilizar cualquier salida de Copilot en un contexto operativo, deben verificarse siempre los hechos, cifras, fechas, responsables y compromisos en las fuentes originales.

### Recursos opcionales

- [Introducción a Microsoft 365 Copilot](https://learn.microsoft.com/es-es/copilot/microsoft-365/microsoft-365-copilot-overview)
- [Datos, privacidad y seguridad para Microsoft 365 Copilot](https://learn.microsoft.com/es-es/copilot/microsoft-365/microsoft-365-copilot-privacy)
- [Prácticas recomendadas para crear prompts en Microsoft 365 Copilot](https://support.microsoft.com/es-es/topic/pr%C3%A1cticas-recomendadas-para-crear-prompts-en-microsoft-365-copilot-3f1c7fbe-3b62-4f8b-9dbf-3b54f7d5d4e8)
- [Uso responsable de la inteligencia artificial de Microsoft](https://www.microsoft.com/es-es/ai/responsible-ai)

---

# Práctica: El instructor mostrará ejemplos del uso de Copilot en https://m365.cloud.microsoft/, Copilot en Outlook, trabajo con archivos de Excel en https://m365.cloud.microsoft/ y Copilot dentro de Teams con el licenciamiento Básico y Premium, aplicados a escenarios propios del sector energético.

## Metadatos

| Elemento | Valor |
|---|---|
| Duración | 20 minutos |
| Complejidad | Media |
| Nivel de Bloom | Aplicar |

## Descripción general

En esta práctica el instructor demuestra cómo seleccionar el punto de entrada de Microsoft 365 Copilot más adecuado según la tarea y el contexto disponible: Copilot Chat, Outlook, Excel y Teams. Los ejemplos usan información operativa de la Central Solar Andes y se apoyan en archivos controlados dentro de OneDrive for Business.

La práctica aplica prompting estructurado: objetivo, fuente, audiencia, formato y criterios de validación. Los resultados generados se revisan antes de guardarse como el documento `02_Resumen_ejecutivo_y_acciones.docx`, que será una fuente controlada para la práctica posterior de creación de agentes personalizados.

## Objetivos de aprendizaje

Al finalizar la práctica, el participante podrá:

- [ ] Distinguir cuándo conviene usar Copilot Chat y cuándo usar Copilot integrado en Outlook, Excel o Teams.
- [ ] Aplicar Copilot Chat para sintetizar un informe operativo y producir un resumen ejecutivo verificable.
- [ ] Usar Copilot en Outlook para preparar un correo profesional para responsables de mantenimiento.
- [ ] Usar Copilot con un archivo de Excel para identificar variaciones de generación, indisponibilidad y datos que requieren contraste.
- [ ] Usar Copilot en Teams para resumir una conversación operativa y extraer responsables, fechas, riesgos y acciones.
- [ ] Comparar de forma demostrativa las capacidades de Copilot Chat Básico y Microsoft 365 Copilot Premium, considerando licencias, permisos, directivas y disponibilidad del tenant.

## Requisitos previos

### Conocimientos requeridos

Antes de iniciar, los participantes deben poder:

- Diferenciar una instrucción ambigua de un prompt estructurado.
- Explicar que Copilot genera respuestas a partir de la instrucción, el contexto disponible, los datos autorizados, la aplicación utilizada y mecanismos de seguridad.
- Reconocer que una respuesta fluida no garantiza que sea correcta.
- Aplicar revisión humana a cifras, fechas, responsables, compromisos y decisiones operativas.
- Identificar que los permisos de Microsoft 365 determinan los archivos, correos, chats y reuniones que Copilot puede usar.

### Acceso y recursos requeridos

Confirme que se cumplen los siguientes requisitos:

- Práctica `01-00-01` completada.
- Acceso al tenant único de laboratorio: `Tenant-EnergiaHorizonte`.
- Acceso de edición a la ruta obligatoria de OneDrive for Business:

  ```text
  /CopilotLabs/EnergiaHorizonte/
  ```

- Documento disponible:

  ```text
  /CopilotLabs/EnergiaHorizonte/01_Prompts_validados_Energia_Horizonte.docx
  ```

- Archivo de Excel disponible y editable:

  ```text
  /CopilotLabs/EnergiaHorizonte/02_Datos_generacion_y_disponibilidad.xlsx
  ```

- Buzón de Outlook habilitado para el usuario de laboratorio.
- Acceso al equipo de Teams `Operaciones Energía Horizonte`.
- Acceso al canal `Central-Andes` y, cuando esté preparado, a la conversación de prueba `Alarma inversores - 14 agosto`.
- Una cuenta con capacidad Copilot Chat Básico y, cuando el tenant lo permita, la cuenta del instructor con capacidad Microsoft 365 Copilot Premium.
- Cuenta de instructor predeterminada:

  ```text
  instructor.copilot@tenant-energiahorizonte.onmicrosoft.com
  ```

- Cuenta de alumno de referencia:

  ```text
  alumno01.copilot@tenant-energiahorizonte.onmicrosoft.com
  ```

> **Importante:** Esta práctica es una demostración guiada por el instructor. No se deben usar archivos personales ni datos fuera de la ruta de OneDrive indicada.

## Entorno de laboratorio

### Hardware recomendado

| Componente | Especificación |
|---|---|
| Equipo | Windows 11 Pro de 64 bits |
| Procesador | Intel Core i5 de 11.ª generación o equivalente |
| Memoria | 16 GB de RAM disponibles |
| Almacenamiento | 10 GB de espacio libre |
| Pantalla | Resolución mínima de 1920 × 1080 |
| Red | Al menos 25 Mbps de descarga y 5 Mbps de carga |
| Audio | Auriculares con micrófono opcionales para dictado, reuniones de Teams y accesibilidad |

### Software y servicios

| Componente | Versión o referencia |
|---|---|
| Windows | Windows 11 Pro 23H2, compilación 22631.4890 |
| Microsoft 365 Apps | Versión 2502, compilación 16.0.18526.20208 |
| Microsoft Teams | Trabajo o escuela 25102.2407.3601.1065 |
| Navegador | Google Chrome 134.0.6998.89 o equivalente compatible |
| Copilot Chat | Experiencia web de Microsoft 365, referencia 2026-08-26 |
| Microsoft 365 Copilot | Servicio SaaS, referencia 2026-08-26 |
| OneDrive for Business | Servicio SaaS, referencia 2026-08-26 |

### Comprobación inicial del entorno

1. Abra Google Chrome e inicie sesión con la cuenta del instructor:

   ```text
   instructor.copilot@tenant-energiahorizonte.onmicrosoft.com
   ```

2. Abra el portal de Microsoft 365:

   ```text
   https://m365.cloud.microsoft/
   ```

3. Compruebe que la identidad activa pertenece a `Tenant-EnergiaHorizonte`.

4. Abra OneDrive desde el iniciador de aplicaciones o desde Microsoft 365.

5. Navegue a la carpeta obligatoria:

   ```text
   /CopilotLabs/EnergiaHorizonte/
   ```

6. Confirme la existencia de los dos archivos de entrada:

   ```text
   01_Informe_operativo_Central_Solar_Andes.docx
   02_Datos_generacion_y_disponibilidad.xlsx
   ```

7. Confirme la existencia del documento creado en la práctica anterior:

   ```text
   01_Prompts_validados_Energia_Horizonte.docx
   ```

> **Nota de demostración:** Las etiquetas comerciales, iconos, botones y funciones concretas de Copilot pueden cambiar. Las opciones visibles dependen de la licencia asignada, las directivas del tenant, la región, el canal de actualización y el despliegue gradual del servicio.

## Procedimiento paso a paso

### Paso 1. Revisar el prompt validado y definir el criterio de selección de la aplicación

**Objetivo:** Recuperar el prompt estructurado de la práctica anterior y relacionar cada tarea con la aplicación que aporta el contexto más útil.

**Instrucciones:**

1. En OneDrive, abra:

   ```text
   /CopilotLabs/EnergiaHorizonte/01_Prompts_validados_Energia_Horizonte.docx
   ```

2. Localice el prompt validado para sintetizar el informe operativo de la Central Solar Andes. Si existe más de una versión, seleccione la que incluya explícitamente:
   - La fuente de información.
   - El propósito del resumen.
   - La audiencia.
   - El formato de salida.
   - La necesidad de señalar datos no confirmados.
   - La petición de verificar cifras, fechas, responsables y decisiones.

3. Explique al grupo la selección del punto de entrada de Copilot mediante esta pauta:

   | Tipo de tarea | Punto de entrada recomendado | Motivo |
   |---|---|---|
   | Sintetizar un documento y elaborar un borrador de análisis | Copilot Chat en Microsoft 365 | Permite trabajar con archivos autorizados y solicitar una estructura concreta. |
   | Redactar una respuesta o correo basado en un hilo | Copilot en Outlook | El mensaje, destinatarios y conversación proporcionan contexto inmediato. |
   | Analizar valores, tendencias y posibles anomalías | Copilot en Excel | El libro, las tablas, las columnas y las fórmulas constituyen el contexto principal. |
   | Extraer acuerdos, responsables y seguimiento de una conversación o reunión | Copilot en Teams | El chat, canal, reunión y, si existe, la transcripción aportan el contexto operativo. |

4. Indique que la aplicación no sustituye la validación. Por ejemplo:
   - Excel puede identificar una tendencia, pero el instructor debe confirmar los valores y el periodo en la hoja.
   - Teams puede resumir una conversación, pero se deben comprobar responsables y fechas contra los mensajes originales.
   - Outlook puede redactar un correo, pero el remitente sigue siendo responsable de la exactitud y el tono.
   - Copilot Chat puede sintetizar archivos, pero debe señalarse cualquier inferencia que no esté explícitamente fundamentada.

**Resultado esperado:**

El instructor dispone de un prompt estructurado y el grupo comprende que la elección de la aplicación depende del contexto de trabajo, no solo de la capacidad de generar texto.

**Verificación:**

- El documento `01_Prompts_validados_Energia_Horizonte.docx` está accesible desde la ruta obligatoria.
- El prompt seleccionado identifica la fuente y el formato de salida.
- Los participantes pueden justificar por qué Excel es preferible para analizar el libro de generación y por qué Teams es preferible para resumir una conversación operativa.

---

### Paso 2. Generar y validar un resumen ejecutivo con Copilot Chat en Microsoft 365

**Objetivo:** Usar Copilot Chat en `https://m365.cloud.microsoft/` para sintetizar el informe operativo de la Central Solar Andes con referencias y criterios de revisión.

**Instrucciones:**

1. En el portal de Microsoft 365, abra Copilot Chat.

2. Confirme visualmente qué experiencia está disponible para la cuenta:
   - Copilot Chat Básico, si se está realizando la comparación con una cuenta sin licencia Microsoft 365 Copilot Premium.
   - Microsoft 365 Copilot Premium, si la cuenta del instructor tiene la licencia y las capacidades habilitadas.

3. Adjunte o seleccione como referencia el archivo siguiente, usando únicamente el selector de archivos autorizado de OneDrive:

   ```text
   /CopilotLabs/EnergiaHorizonte/01_Informe_operativo_Central_Solar_Andes.docx
   ```

4. Utilice el prompt validado de la práctica anterior. Si se necesita una versión de referencia para la demostración, use el siguiente prompt:

   ```text
   Usa exclusivamente el documento "01_Informe_operativo_Central_Solar_Andes.docx" de la carpeta /CopilotLabs/EnergiaHorizonte/.

   Elabora un resumen ejecutivo para la jefatura de Operaciones de Energía Horizonte.

   Formato:
   1. Situación operativa actual.
   2. Hallazgos relevantes.
   3. Riesgos o desviaciones que requieren atención.
   4. Tres acciones prioritarias con responsable sugerido y fecha, solo si están fundamentados en la fuente.
   5. Datos, cifras, fechas, responsables o causas que deban verificarse en el documento original.

   Usa un tono profesional y conciso. No inventes valores, responsables, causas ni compromisos. Indica la fuente utilizada y señala cualquier dato que no puedas confirmar.
   ```

5. Envíe el prompt y espere la respuesta.

6. Revise el resultado usando estas preguntas:
   - **¿Está fundamentado?** ¿La respuesta identifica el informe como fuente y, si la experiencia lo muestra, incluye citas o referencias?
   - **¿Está completo?** ¿Cubre situación, hallazgos, riesgos, acciones y elementos por verificar?
   - **¿Es adecuado para la decisión?** ¿El contenido puede ser usado como borrador ejecutivo sin presentar hipótesis como hechos?

7. Abra el informe operativo en otra pestaña y verifique al menos:
   - Una cifra de generación, disponibilidad o impacto operativo mencionada.
   - Una fecha incluida en el resumen.
   - Un riesgo o una causa potencial.
   - Cualquier responsable propuesto por Copilot.

8. Si la respuesta incluye información no comprobable, reformule con una instrucción correctiva:

   ```text
   Revisa el resumen anterior. Elimina cualquier cifra, fecha, responsable, causa o compromiso que no esté explícitamente respaldado por el informe. Mantén una sección titulada "Pendiente de validación" para los elementos que requieran confirmación humana.
   ```

9. Copie el resultado validado en un documento nuevo de Word.

10. Guarde el documento exclusivamente en la ruta de laboratorio con este nombre:

   ```text
   /CopilotLabs/EnergiaHorizonte/02_Resumen_ejecutivo_y_acciones.docx
   ```

11. Incluya al principio del documento una nota de control como la siguiente:

   ```text
   Borrador generado con Microsoft 365 Copilot a partir de fuentes autorizadas.
   Revisión humana requerida antes de distribuir o tomar decisiones operativas.
   Fuente principal: 01_Informe_operativo_Central_Solar_Andes.docx.
   ```

**Resultado esperado:**

Se crea el archivo `02_Resumen_ejecutivo_y_acciones.docx` con un resumen ejecutivo revisado, tres acciones prioritarias fundamentadas o claramente marcadas como sugeridas, y una sección de elementos pendientes de validación.

**Verificación:**

- El archivo nuevo existe en:

  ```text
  /CopilotLabs/EnergiaHorizonte/02_Resumen_ejecutivo_y_acciones.docx
  ```

- El resumen identifica el informe operativo como fuente.
- El documento no presenta datos no confirmados como hechos.
- Las cifras, fechas y responsables relevantes se han contrastado con el archivo original.

---

### Paso 3. Demostrar la redacción de un correo en Copilot para Outlook

**Objetivo:** Convertir el resumen ejecutivo validado en un correo profesional dirigido a responsables de mantenimiento, aprovechando el contexto de Outlook.

**Instrucciones:**

1. Abra Outlook con la cuenta del instructor.

2. Seleccione **Nuevo correo**.

3. Como destinatario de demostración, use un buzón o grupo de prueba autorizado del tenant. Si no existe un destinatario de laboratorio, deje el campo **Para** vacío durante la demostración y no envíe el mensaje.

4. Abra Copilot en Outlook. Según la experiencia disponible, use una opción como **Borrador con Copilot**, **Redactar con Copilot** o el panel de Copilot.

5. Proporcione como contexto el contenido validado de `02_Resumen_ejecutivo_y_acciones.docx`. Puede copiar el resumen ejecutivo en el borrador o usar una referencia de archivo si la experiencia de Outlook la permite.

6. Introduzca el siguiente prompt:

   ```text
   Redacta un correo dirigido a los responsables de mantenimiento de la Central Solar Andes.

   Usa el resumen ejecutivo proporcionado como fuente. El objetivo es solicitar la coordinación de acciones ante los hallazgos operativos.

   Requisitos:
   - Tono profesional, claro y colaborativo.
   - Incluye exactamente tres acciones prioritarias en una lista numerada.
   - No presentes como hechos las causas que estén pendientes de validación.
   - Incluye una petición explícita de confirmación de responsables y fechas.
   - Propón un asunto de correo.
   - Cierra indicando que las cifras y causas deben contrastarse con el informe operativo original antes de tomar decisiones.

   No inventes destinatarios, compromisos, fechas ni responsables.
   ```

7. Revise el borrador generado. Compruebe específicamente:
   - Que el asunto describe la acción solicitada.
   - Que hay exactamente tres acciones prioritarias.
   - Que la solicitud de confirmación es explícita.
   - Que el correo diferencia hechos documentados de elementos pendientes de validación.
   - Que el tono es apropiado para coordinación operativa.

8. Si el borrador omite la petición de confirmación, use esta mejora:

   ```text
   Ajusta el correo para solicitar confirmación explícita antes de las 16:00 del siguiente día laborable, solo si esta fecha es apropiada como propuesta y queda claramente indicada como propuesta. Si no hay una fecha fundamentada, solicita confirmación de la fecha objetivo sin asignar una.
   ```

9. Muestre cómo Copilot puede ayudar a ajustar el tono sin cambiar los hechos:

   ```text
   Mantén el contenido factual del borrador. Haz el tono más directo y operativo, sin aumentar la urgencia ni crear compromisos nuevos.
   ```

10. Guarde el correo como borrador. No lo envíe durante la práctica salvo que el instructor disponga de destinatarios de prueba autorizados y el envío forme parte del diseño del laboratorio.

11. Si corresponde, agregue al documento `02_Resumen_ejecutivo_y_acciones.docx` una sección titulada **Borrador de comunicación a mantenimiento** y pegue el texto final revisado del correo.

**Resultado esperado:**

Existe un borrador de correo profesional en Outlook que convierte el resumen ejecutivo en una solicitud operativa clara, con tres acciones prioritarias y una petición explícita de confirmación.

**Verificación:**

- El borrador no contiene datos inventados ni compromisos no autorizados.
- El mensaje contiene exactamente tres acciones priorizadas.
- Se solicita confirmación de responsables y fechas.
- El borrador permanece sin enviar, a menos que se utilice un destinatario de prueba aprobado.

---

### Paso 4. Analizar generación e indisponibilidad con Copilot en Excel

**Objetivo:** Usar Copilot con el libro de generación y disponibilidad para identificar tendencias, periodos de indisponibilidad y posibles causas que deben contrastarse con el informe operativo.

**Instrucciones:**

1. Vuelva a Microsoft 365 y abra el archivo desde OneDrive:

   ```text
   /CopilotLabs/EnergiaHorizonte/02_Datos_generacion_y_disponibilidad.xlsx
   ```

2. Verifique que el archivo está abierto en Excel para la Web o en la aplicación de escritorio compatible con la capacidad de Copilot disponible.

3. Revise la estructura del libro antes de solicitar análisis:
   - Identifique la hoja o tabla que contiene fechas.
   - Localice las columnas de generación real, generación planificada o prevista, disponibilidad, indisponibilidad, alarmas, observaciones o variables equivalentes.
   - Compruebe que los encabezados son comprensibles.
   - No modifique datos originales durante la demostración.

4. Abra Copilot en Excel.

5. Solicite un análisis inicial mediante este prompt:

   ```text
   Analiza este libro de Excel para la Central Solar Andes.

   Identifica:
   1. Variaciones relevantes entre generación real y generación planificada o prevista.
   2. Periodos de indisponibilidad o disminución relevante de disponibilidad.
   3. Tendencias o patrones visibles por fecha.
   4. Posibles causas o correlaciones que deban contrastarse con el informe operativo, sin afirmar causalidad si el libro no la demuestra.

   Presenta los resultados en una tabla con las columnas:
   - Periodo o fecha
   - Hallazgo
   - Dato observado
   - Impacto potencial
   - Elemento que debe verificarse en el informe operativo

   Usa únicamente los datos del libro. Indica cualquier limitación, columna ausente o supuesto.
   ```

6. Revise la respuesta y compruebe los valores directamente en la hoja:
   - Seleccione una fecha o periodo mencionado.
   - Compare la generación real con el valor planificado.
   - Revise el valor de disponibilidad o la marca de indisponibilidad.
   - Confirme que la respuesta no confunde porcentajes, unidades o periodos.

7. Explique al grupo que Copilot puede proponer una interpretación de los datos, pero no demuestra por sí solo la causa raíz. Una coincidencia entre indisponibilidad y una alarma no equivale a una relación causal confirmada.

8. Solicite una segunda respuesta centrada en elementos verificables:

   ```text
   Resume solo los hallazgos que puedan comprobarse directamente en las celdas del libro. Separa en dos listas:
   - Hechos observados en los datos.
   - Hipótesis o correlaciones que requieren contraste con 01_Informe_operativo_Central_Solar_Andes.docx.

   No calcules ni inventes datos si las columnas necesarias no están disponibles.
   ```

9. Si Copilot ofrece crear una visualización o resaltar datos, úselo únicamente si la función está disponible y no altera el conjunto de datos original. Por ejemplo, puede solicitar:

   ```text
   Propón un gráfico adecuado para comparar generación real frente a plan y señalar periodos de indisponibilidad. Explica qué columnas utilizarías y por qué.
   ```

10. Copie al documento `02_Resumen_ejecutivo_y_acciones.docx` una sección titulada **Hallazgos de datos de generación y disponibilidad**. Incluya:
    - Los hallazgos verificados.
    - Las hipótesis que requieren contraste.
    - Una nota indicando que los resultados se basan en el libro de Excel y deben validarse contra el informe operativo.

11. Guarde el documento Word actualizado.

**Resultado esperado:**

El instructor obtiene una lista estructurada de variaciones, periodos de indisponibilidad y elementos que requieren contraste, diferenciando hechos observados de hipótesis.

**Verificación:**

- Al menos un hallazgo de Copilot se ha confirmado directamente en las celdas del libro.
- Las posibles causas están redactadas como elementos por contrastar, no como conclusiones definitivas.
- El documento `02_Resumen_ejecutivo_y_acciones.docx` incluye la sección de hallazgos de Excel.
- El libro original no ha sido sobrescrito con análisis no validados.

---

### Paso 5. Resumir una conversación operativa en Copilot para Teams

**Objetivo:** Usar Copilot en Teams para resumir una conversación o canal sobre una alarma de inversores y extraer responsables, fechas, riesgos y seguimiento.

**Instrucciones:**

1. Abra Microsoft Teams con la cuenta del instructor.

2. Acceda al equipo:

   ```text
   Operaciones Energía Horizonte
   ```

3. Abra el canal:

   ```text
   Central-Andes
   ```

4. Localice la conversación preparada sobre la alarma. Según la configuración del entorno, use uno de los siguientes contextos:
   - La conversación o publicación denominada `Alarma inversores - 14 agosto`.
   - El chat o conversación de prueba preparado como `Operaciones-Central-Andes`.
   - Una reunión operativa con transcripción, si el instructor ha preparado una.

5. Verifique que la conversación contiene mensajes suficientes para identificar hechos, acciones o preguntas pendientes.

6. Abra Copilot dentro de Teams o use la función de resumen disponible para el chat, canal o reunión.

7. Introduzca el prompt siguiente:

   ```text
   Resume la conversación sobre la alarma de inversores de la Central Solar Andes.

   Presenta una tabla con:
   - Hecho o decisión mencionada
   - Responsable citado en la conversación
   - Fecha o plazo mencionado
   - Riesgo operativo
   - Acción de seguimiento
   - Estado de confirmación: confirmado en el chat / pendiente de validación

   Usa únicamente la información presente en esta conversación. No inventes responsables, fechas, decisiones ni causas. Si existe una discrepancia entre mensajes, indícala explícitamente.
   ```

8. Revise el resumen comparándolo con los mensajes originales. Valide como mínimo:
   - Un responsable mencionado.
   - Una fecha o plazo.
   - Una acción de seguimiento.
   - Un riesgo operativo.
   - Una posible discrepancia, si la conversación contiene mensajes contradictorios o incompletos.

9. Si el resumen incluye inferencias no sustentadas, use el siguiente prompt:

   ```text
   Revisa el resumen anterior y conserva solo afirmaciones explícitamente presentes en los mensajes. Mueve cualquier inferencia a una sección "Pendiente de validación" e indica qué mensaje o dato sería necesario para confirmarla.
   ```

10. Demuestre que Teams es adecuado para esta tarea porque el chat, canal o transcripción es el contexto central. Aclare que un resumen de Teams puede no incluir información que esté únicamente en un informe de Word o en un libro de Excel, salvo que dichos archivos estén explícitamente disponibles y sean accesibles para el usuario.

11. Copie el resultado revisado en `02_Resumen_ejecutivo_y_acciones.docx`, bajo la sección:

   ```text
   Seguimiento de Teams: alarma de inversores
   ```

12. Guarde el documento actualizado en la ruta obligatoria.

**Resultado esperado:**

Se obtiene un resumen de Teams con responsables, fechas, riesgos y acciones, diferenciado entre información confirmada en la conversación y elementos que requieren validación.

**Verificación:**

- Los responsables y fechas incluidos pueden localizarse en los mensajes del chat o canal.
- El resumen no afirma causas técnicas no confirmadas.
- El documento consolidado incorpora el seguimiento de Teams.
- La conversación original permanece sin modificaciones.

---

### Paso 6. Comparar demostrativamente Copilot Chat Básico y Microsoft 365 Copilot Premium

**Objetivo:** Comparar las capacidades visibles de una experiencia Básica y una experiencia Premium, sin asumir que una función está disponible para todos los usuarios.

**Instrucciones:**

1. Explique que la disponibilidad de Copilot depende de:
   - Licencia asignada.
   - Permisos del usuario sobre contenido de Microsoft 365.
   - Directivas de seguridad y cumplimiento del tenant.
   - Aplicación utilizada.
   - Despliegue gradual, región y versión del servicio.

2. Si dispone de ambas cuentas, abra una sesión de navegador separada o un perfil independiente para la cuenta de referencia:

   ```text
   alumno01.copilot@tenant-energiahorizonte.onmicrosoft.com
   ```

3. Abra Copilot Chat Básico con la cuenta de referencia y Copilot Chat o Microsoft 365 Copilot con la cuenta del instructor, según las licencias efectivamente asignadas.

4. Solicite una tarea general equivalente en ambas experiencias, sin usar datos confidenciales ni asumir acceso a archivos. Por ejemplo:

   ```text
   Redacta una lista de cinco preguntas que un responsable de operaciones debería revisar antes de comunicar una indisponibilidad de generación solar. No inventes datos de una planta concreta.
   ```

5. Compare el resultado de forma cualitativa:
   - Calidad general de redacción.
   - Posibilidad de usar contexto de archivos de trabajo, correos, reuniones o chats autorizados.
   - Integración disponible dentro de Outlook, Excel y Teams.
   - Presencia de referencias, citas, selección de archivos o acciones específicas de la aplicación.
   - Limitaciones visibles en la interfaz.

6. Muestre que el acceso a datos de trabajo no significa acceso universal. Copilot respeta los permisos existentes. Si un usuario no puede abrir un archivo, no debe usarse como fuente autorizada para sus respuestas.

7. Use la siguiente tabla como guía de explicación, sin afirmar características no visibles en el tenant:

   | Aspecto | Copilot Chat Básico | Microsoft 365 Copilot Premium |
   |---|---|---|
   | Conversación general y generación de texto | Puede estar disponible, según el servicio y la cuenta | Disponible según licencia y configuración |
   | Uso de datos de trabajo de Microsoft 365 | Puede ser limitado o no estar habilitado | Puede estar disponible conforme a permisos y directivas |
   | Integración en Outlook, Excel y Teams | Puede no estar disponible o ser limitada | Puede estar disponible con la licencia y aplicaciones compatibles |
   | Contexto de correo, libro, chat o reunión | Depende de la función habilitada | Puede aprovechar el contexto de la aplicación, sujeto a permisos |
   | Citas, referencias y acciones contextuales | Varían por experiencia y despliegue | Varían por aplicación, licencia y despliegue |
   | Resultado y necesidad de revisión humana | Requiere revisión | Requiere revisión |

8. Indique que Premium no elimina los riesgos de respuestas incompletas, datos desactualizados, interpretación incorrecta o alucinaciones. En ambos casos se deben validar cifras, responsables, fechas y decisiones antes de distribuir resultados.

9. Registre en el documento `02_Resumen_ejecutivo_y_acciones.docx` una breve sección titulada **Observación sobre licenciamiento y contexto**, con una nota similar a:

   ```text
   Las capacidades observadas de Copilot Chat, Outlook, Excel y Teams dependen de la licencia, los permisos, las directivas y el despliegue del Tenant-EnergiaHorizonte. La disponibilidad de una función no garantiza el acceso a contenido sin autorización ni sustituye la revisión humana.
   ```

10. Guarde y cierre el documento Word.

**Resultado esperado:**

Los participantes distinguen entre capacidades generales de conversación y capacidades integradas basadas en contexto de Microsoft 365, comprendiendo que su disponibilidad real depende del entorno.

**Verificación:**

- El instructor ha mostrado al menos una diferencia observable o ha documentado que no fue posible comparar por falta de licencia o directiva.
- Se ha explicado que las funciones visibles pueden variar.
- El documento final contiene la nota de licenciamiento, permisos y validación humana.

## Validación y pruebas

Realice las siguientes comprobaciones al finalizar la práctica.

| Prueba | Procedimiento | Resultado esperado |
|---|---|---|
| Ubicación de archivos | Abra OneDrive y navegue a `/CopilotLabs/EnergiaHorizonte/`. | Los archivos del laboratorio permanecen dentro de la ruta obligatoria. |
| Documento de salida | Abra `02_Resumen_ejecutivo_y_acciones.docx`. | El documento existe, se abre correctamente y contiene el resumen ejecutivo, hallazgos de Excel, seguimiento de Teams y nota de licenciamiento. |
| Fundamentación del resumen | Compare dos afirmaciones del resumen con `01_Informe_operativo_Central_Solar_Andes.docx`. | Las afirmaciones relevantes están respaldadas o marcadas como pendientes de validación. |
| Análisis de Excel | Compare al menos una variación o indisponibilidad con las celdas del archivo Excel. | El dato, la fecha y la unidad son correctos. |
| Seguimiento de Teams | Compare un responsable, una acción y una fecha contra la conversación de alarma. | Los elementos aparecen en los mensajes originales o se clasifican como pendientes de validación. |
| Correo de Outlook | Revise el borrador guardado. | Tiene tono profesional, exactamente tres acciones, una solicitud explícita de confirmación y no contiene compromisos inventados. |
| Selección del punto de entrada | Pregunte al participante qué aplicación utilizaría para resumir un chat, analizar una tendencia de datos y responder un hilo de correo. | Responde Teams, Excel y Outlook, respectivamente, justificando el contexto disponible. |
| Uso responsable | Revise la sección de observación sobre licenciamiento. | Reconoce que licencia, permisos, directivas y despliegue afectan las funciones disponibles y que la revisión humana es obligatoria. |

> **Criterio de finalización:** La práctica se considera completada cuando `02_Resumen_ejecutivo_y_acciones.docx` está guardado en OneDrive, contiene resultados revisados de Copilot Chat, Outlook, Excel y Teams, y diferencia explícitamente entre hechos confirmados y elementos pendientes de validación.

## Solución de problemas

### Problema 1: Copilot no muestra opciones para usar archivos de trabajo o no encuentra el informe de la Central Solar Andes

**Síntomas:**

- El selector de archivos no muestra OneDrive o no encuentra `01_Informe_operativo_Central_Solar_Andes.docx`.
- Copilot responde de forma general y no usa el contenido del informe.
- Aparece un mensaje indicando que el archivo no está disponible o que no hay acceso.

**Causa:**

La cuenta puede no tener permisos sobre el archivo, estar conectada al tenant equivocado, usar una experiencia sin acceso a datos de trabajo o tener una directiva que limita la integración de Copilot con contenido organizativo.

**Solución:**

1. Confirme que la sesión pertenece a `Tenant-EnergiaHorizonte`.
2. Abra manualmente el archivo desde OneDrive. Si no se abre, solicite permisos de lectura o edición al propietario o al administrador del laboratorio.
3. Compruebe que el archivo está en:

   ```text
   /CopilotLabs/EnergiaHorizonte/
   ```

4. Cierre sesión y vuelva a iniciar sesión con la cuenta correcta.
5. Si el selector de archivos no está disponible, abra el documento directamente en Word y use la experiencia de Copilot habilitada en esa aplicación, o copie únicamente el contenido autorizado necesario en el prompt.
6. Documente la limitación de licencia o directiva en lugar de simular una capacidad no disponible.

### Problema 2: Copilot en Excel o Teams produce un resumen incompleto, con fechas incorrectas o causas no confirmadas

**Síntomas:**

- Copilot no identifica una indisponibilidad visible en Excel.
- El resumen de Teams asigna un responsable o una fecha que no aparece claramente en los mensajes.
- Se presenta una correlación como causa técnica confirmada.
- La respuesta usa valores, unidades o periodos incorrectos.

**Causa:**

El contexto puede ser incompleto, los encabezados de Excel pueden ser ambiguos, los mensajes pueden contener información contradictoria o el modelo puede haber generado una inferencia plausible pero no fundamentada. La respuesta de Copilot es probabilística y requiere revisión humana.

**Solución:**

1. Reduzca el alcance del prompt e indique la fuente exacta, la hoja, las columnas o la conversación que se deben usar.
2. Solicite separar explícitamente hechos observados de hipótesis:

   ```text
   Separa los datos explícitos de las inferencias. No atribuyas causas ni responsables si no aparecen literalmente en la fuente.
   ```

3. Verifique manualmente cifras, fechas y responsables en las celdas o mensajes originales.
4. Corrija el documento consolidado para que los elementos no confirmados aparezcan bajo **Pendiente de validación**.
5. Si la conversación o el libro no contiene la información necesaria, no fuerce una conclusión; registre la limitación y especifique qué fuente adicional sería necesaria.

## Limpieza

1. Compruebe que el documento final está guardado con el nombre exacto:

   ```text
   /CopilotLabs/EnergiaHorizonte/02_Resumen_ejecutivo_y_acciones.docx
   ```

2. Mantenga los archivos fuente sin cambios:
   - `01_Informe_operativo_Central_Solar_Andes.docx`
   - `02_Datos_generacion_y_disponibilidad.xlsx`
   - `01_Prompts_validados_Energia_Horizonte.docx`

3. Cierre el libro de Excel sin guardar cambios no intencionados.

4. Mantenga el correo de Outlook como borrador o elimínelo si el instructor no necesita conservarlo como evidencia de la demostración. No envíe mensajes a destinatarios reales sin autorización.

5. No elimine `02_Resumen_ejecutivo_y_acciones.docx`, ya que será una fuente de conocimiento para la práctica `01-00-03`.

6. Cierre las sesiones adicionales usadas para comparar licenciamiento, especialmente si se inició sesión con la cuenta de referencia del alumno.

7. Cierre Teams, Outlook y el navegador, o bloquee el equipo conforme a las políticas del laboratorio.

## Resumen

En esta práctica se aplicó Copilot en cuatro contextos de Microsoft 365 para tareas operativas del sector energético:

- **Copilot Chat** se utilizó para transformar un informe controlado en un resumen ejecutivo estructurado.
- **Outlook** se utilizó para convertir el resumen validado en un correo profesional con acciones y confirmación solicitada.
- **Excel** se utilizó para identificar variaciones de generación, periodos de indisponibilidad y elementos que requieren contraste.
- **Teams** se utilizó para sintetizar una conversación operativa y extraer seguimiento, responsables, fechas y riesgos.

La selección de la aplicación determina el contexto disponible para Copilot. Sin embargo, ni la integración ni una licencia Premium garantizan exactitud automática. Las respuestas deben fundamentarse en fuentes autorizadas y verificarse antes de tomar decisiones, comunicar compromisos o distribuir información operativa.

El resultado principal de la práctica es el archivo:

```text
/CopilotLabs/EnergiaHorizonte/02_Resumen_ejecutivo_y_acciones.docx
```

Este documento, junto con `01_Prompts_validados_Energia_Horizonte.docx`, será utilizado como fuente controlada en la práctica `01-00-03` para crear y validar un agente personalizado mediante Agent Builder.

### Recursos opcionales

- [Introducción a Microsoft 365 Copilot](https://learn.microsoft.com/es-es/copilot/microsoft-365/microsoft-365-copilot-overview)
- [Datos, privacidad y seguridad para Microsoft 365 Copilot](https://learn.microsoft.com/es-es/copilot/microsoft-365/microsoft-365-copilot-privacy)
- [Prácticas recomendadas para crear prompts en Microsoft 365 Copilot](https://support.microsoft.com/es-es/topic/pr%C3%A1cticas-recomendadas-para-crear-prompts-en-microsoft-365-copilot-3f1c7fbe-3b62-4f8b-9dbf-3b54f7d5d4e8)
- [Uso responsable de la inteligencia artificial de Microsoft](https://www.microsoft.com/es-es/ai/responsible-ai)

---

# Práctica: El instructor presentará capacidades de los agentes Analista, Investigador, Ideas y Prompt Coach mediante escenarios relacionados con una empresa de generación de energía eléctrica, y realizará una breve demostración de la creación de un agente personalizado con Agent Builder.

## Metadatos

| Elemento | Valor |
|---|---|
| Duración | 13 minutos |
| Complejidad | Media |
| Nivel de Bloom | Aplicar |

## Descripción general

En esta práctica, el instructor demuestra cómo seleccionar y utilizar agentes especializados de Microsoft 365 Copilot según una necesidad empresarial concreta de Energía Horizonte. Se emplearán Analista, Investigador, Ideas y Prompt Coach para analizar datos operativos, investigar prácticas del sector, generar iniciativas de comunicación y mejorar un prompt de riesgos.

Como cierre, se creará y probará un agente personalizado básico con Agent Builder, restringido a fuentes documentales aprobadas del laboratorio. Los resultados se tratarán como borradores sujetos a verificación humana, especialmente cuando incluyan cifras, prioridades operativas, recomendaciones o referencias externas.

## Objetivos de aprendizaje

Al finalizar la práctica, podrá:

- [ ] Identificar cuándo utilizar Analista, Investigador, Ideas y Prompt Coach según el tipo de necesidad empresarial.
- [ ] Demostrar un análisis de desviaciones de producción y disponibilidad mediante el agente Analista.
- [ ] Obtener una síntesis de investigación con fuentes verificables utilizando Investigador.
- [ ] Generar alternativas de comunicación operativa con Ideas y mejorar un prompt con Prompt Coach.
- [ ] Crear y probar un agente personalizado básico con fuentes aprobadas mediante Agent Builder.

## Requisitos previos

### Conocimientos requeridos

- Haber completado las prácticas **01-00-01** y **01-00-02**.
- Comprender que Copilot genera respuestas probabilísticas y que una respuesta fluida no garantiza que sea correcta.
- Saber que el contexto, los permisos, los documentos disponibles y la redacción del prompt afectan al resultado.
- Conocer la necesidad de verificar cifras, fechas, responsables, prioridades y referencias antes de utilizar una respuesta en una decisión operativa.

### Acceso y recursos requeridos

- Acceso al tenant único de laboratorio: **Tenant-EnergiaHorizonte**.
- Cuenta recomendada del instructor: `instructor.copilot@tenant-energiahorizonte.onmicrosoft.com`.
- Acceso a Microsoft 365 Copilot y, si están habilitados por el tenant, a los agentes:
  - Analista
  - Investigador
  - Ideas
  - Prompt Coach
- Permiso para crear agentes con Agent Builder o acceso a un entorno de demostración autorizado.
- Acceso de lectura a los siguientes archivos en OneDrive for Business:

```text
/CopilotLabs/EnergiaHorizonte/01_Informe_operativo_Central_Solar_Andes.docx
/CopilotLabs/EnergiaHorizonte/01_Prompts_validados_Energia_Horizonte.docx
/CopilotLabs/EnergiaHorizonte/02_Datos_generacion_y_disponibilidad.xlsx
/CopilotLabs/EnergiaHorizonte/02_Resumen_ejecutivo_y_acciones.docx
```

> **Importante:** No copie ni guarde archivos del laboratorio fuera de `/CopilotLabs/EnergiaHorizonte/`. No publique ni comparta el agente creado fuera del entorno de laboratorio sin revisión previa de permisos, fuentes y cumplimiento.

## Entorno de laboratorio

### Hardware recomendado

| Componente | Requisito |
|---|---|
| Equipo | Windows 11 Pro de 64 bits, Intel Core i5 de 11.ª generación o equivalente |
| Memoria | 16 GB de RAM disponibles |
| Almacenamiento | 10 GB de espacio libre |
| Pantalla | Resolución mínima de 1920 × 1080 |
| Red | 25 Mbps de descarga y 5 Mbps de carga como mínimo |
| Opcional | Auriculares con micrófono para dictado, Teams y accesibilidad |

### Software y servicios

| Componente | Versión o condición |
|---|---|
| Windows | Windows 11 Pro 23H2, compilación 22631.4890 |
| Microsoft 365 Apps | Versión 2502, compilación 16.0.18526.20208 |
| Teams | Trabajo o escuela, versión 25102.2407.3601.1065 |
| Navegador | Google Chrome 134.0.6998.89 o Microsoft Edge actualizado |
| Copilot Chat y Microsoft 365 Copilot | Servicio SaaS, experiencia web de laboratorio fijada al 2026-08-26 |
| OneDrive for Business | Servicio SaaS, experiencia web de laboratorio fijada al 2026-08-26 |

### Preparación inicial

1. Inicie sesión en Microsoft 365 con la cuenta de instructor del tenant **Tenant-EnergiaHorizonte**.
2. Abra OneDrive para la Empresa y compruebe que los cuatro archivos requeridos están disponibles en:

   ```text
   /CopilotLabs/EnergiaHorizonte/
   ```

3. Abra o mantenga disponible el archivo `02_Datos_generacion_y_disponibilidad.xlsx`.
4. Abra Microsoft 365 Copilot en el navegador.
5. Si se solicita, seleccione el modo de trabajo o el agente especializado correspondiente desde el catálogo de agentes.

> **Nota sobre la interfaz:** Los nombres de botones, la ubicación del catálogo de agentes o el flujo de Agent Builder pueden variar según la versión del servicio y la configuración del tenant. Si la interfaz difiere, localice las opciones equivalentes para seleccionar agentes, crear un agente y agregar conocimiento o fuentes.

## Procedimiento paso a paso

### Paso 1. Identificar el agente adecuado para cada necesidad

**Objetivo:** Relacionar una necesidad de negocio de Energía Horizonte con el agente de Copilot más apropiado.

**Instrucciones:**

1. En Microsoft 365 Copilot, abra el catálogo de agentes disponibles.
2. Explique brevemente la finalidad de cada agente antes de demostrarlo:

   | Agente | Necesidad adecuada | Ejemplo en Energía Horizonte |
   |---|---|---|
   | Analista | Interpretar datos, detectar tendencias, explicar variaciones | Comparar producción esperada frente a producción real y disponibilidad |
   | Investigador | Elaborar una síntesis sobre información externa con referencias | Identificar prácticas públicas de mantenimiento predictivo solar |
   | Ideas | Generar alternativas, campañas, nombres o enfoques de comunicación | Proponer iniciativas internas para reducir indisponibilidad |
   | Prompt Coach | Mejorar claridad, estructura, contexto y criterios de un prompt | Refinar un prompt de análisis de riesgos operativos |
   | Agente personalizado | Responder con un propósito definido y fuentes empresariales aprobadas | Consultar prioridades de mantenimiento de Central Andes |

3. Destaque que la selección del agente no elimina la obligación de revisar el resultado.
4. Indique que un mismo prompt puede producir resultados distintos debido a la variabilidad del modelo, al contexto disponible, a los datos actualizados y a los permisos del usuario.

**Resultado esperado:**

El instructor identifica el agente adecuado para cada necesidad y establece que los resultados deben fundamentarse en fuentes verificables o en documentos autorizados.

**Verificación:**

Confirme que los participantes pueden responder correctamente a esta pregunta:

> ¿Qué agente utilizaría para generar varias propuestas de campaña interna y cuál utilizaría para interpretar una desviación de producción?

Respuesta esperada: **Ideas** para la campaña y **Analista** para la desviación de producción.

---

### Paso 2. Analizar desviaciones de generación y disponibilidad con Analista

**Objetivo:** Utilizar el agente Analista para interpretar datos operativos del archivo Excel y producir preguntas de validación.

**Instrucciones:**

1. Seleccione el agente **Analista** en Microsoft 365 Copilot.
2. Adjunte o indique como fuente el archivo:

   ```text
   /CopilotLabs/EnergiaHorizonte/02_Datos_generacion_y_disponibilidad.xlsx
   ```

3. Envíe el siguiente prompt:

   ```text
   Usa exclusivamente el archivo 02_Datos_generacion_y_disponibilidad.xlsx.

   Analiza las desviaciones de producción y disponibilidad de la Central Solar Andes.
   Entrega:
   1. Un resumen de máximo cinco viñetas con las desviaciones más relevantes.
   2. Una tabla con período, producción esperada, producción real, desviación, disponibilidad y posible factor asociado si está respaldado por los datos.
   3. Cinco preguntas de validación para el equipo de operaciones antes de atribuir causas.
   4. Los datos o supuestos que no puedas confirmar.

   No inventes causas. Distingue claramente entre hechos observados, inferencias y preguntas de validación.
   ```

4. Revise la respuesta con el grupo.
5. Señale que las causas sugeridas por el agente son hipótesis, salvo que estén documentadas explícitamente en el archivo.
6. Verifique manualmente al menos una cifra de producción y una cifra de disponibilidad directamente en Excel.

**Resultado esperado:**

El agente produce un resumen de desviaciones, una tabla basada en los datos disponibles, preguntas de validación para Operaciones y una sección de incertidumbres o limitaciones.

**Verificación:**

Compruebe que la respuesta:

- Menciona el archivo Excel como fuente o cita datos atribuibles a él.
- Separa hechos de inferencias.
- No presenta una hipótesis operativa como causa confirmada.
- Incluye preguntas útiles, por ejemplo, sobre irradiancia, alarmas de inversores, mantenimientos, indisponibilidad o calidad de la medición.

> **Punto de control:** Una tabla bien redactada no sustituye la validación en la hoja de cálculo original. Las cifras críticas deben verificarse antes de elevarse a una decisión de operación o mantenimiento.

---

### Paso 3. Investigar buenas prácticas públicas con Investigador

**Objetivo:** Utilizar Investigador para elaborar una nota breve sobre mantenimiento predictivo en plantas solares, con referencias verificables.

**Instrucciones:**

1. Seleccione el agente **Investigador**.
2. Envíe el siguiente prompt:

   ```text
   Prepara una nota breve sobre buenas prácticas públicas de mantenimiento predictivo en plantas solares fotovoltaicas.

   Requisitos:
   - Usa fuentes públicas y verificables.
   - Incluye de 3 a 5 referencias con título, organización, fecha si está disponible y enlace.
   - Separa las secciones: Hechos respaldados por fuentes, Recomendaciones aplicables y Aspectos que requieren validación local.
   - No afirmes que una práctica reduce indisponibilidad en Central Andes si no hay evidencia local.
   - Prioriza fuentes de organismos técnicos, fabricantes con documentación técnica, entidades regulatorias o publicaciones especializadas reconocidas.
   - Redacta para una audiencia de operaciones y mantenimiento; máximo 300 palabras.
   ```

3. Espere la generación de la nota.
4. Revise que las referencias sean accesibles y correspondan al tema solicitado.
5. Abra, cuando sea posible, una de las referencias para comprobar que respalda la afirmación asociada.
6. Explique que una fuente pública puede ser útil para orientar una iniciativa, pero no reemplaza procedimientos internos, análisis de seguridad, contratos de mantenimiento ni criterios de ingeniería aprobados.

**Resultado esperado:**

El agente genera una síntesis breve y estructurada, diferenciando hechos documentados, recomendaciones y elementos que necesitan validación local.

**Verificación:**

Confirme que:

- La respuesta contiene referencias o enlaces verificables.
- Las recomendaciones no se presentan como políticas existentes de Energía Horizonte.
- Se diferencia entre evidencia externa y decisión operativa local.
- No se incluyen referencias sin relación clara con mantenimiento predictivo fotovoltaico.

---

### Paso 4. Generar alternativas de mejora operativa con Ideas

**Objetivo:** Usar Ideas para producir opciones de campaña interna orientadas a reducir la indisponibilidad no programada.

**Instrucciones:**

1. Seleccione el agente **Ideas**.
2. Envíe el siguiente prompt:

   ```text
   Genera 6 opciones para una campaña interna de reducción de indisponibilidad no programada en la Central Solar Andes.

   Para cada opción, incluye:
   - Nombre de la iniciativa.
   - Mensaje principal de máximo 20 palabras.
   - Público objetivo.
   - Acción operativa concreta que promueve.
   - Indicador sugerido para medir adopción o resultado.
   - Riesgo o precaución de implementación.

   Mantén un tono práctico, no punitivo y orientado a seguridad, calidad de datos y aprendizaje operativo.
   No inventes indicadores históricos ni compromisos de reducción porcentual.
   ```

3. Revise las opciones generadas.
4. Seleccione una propuesta y pida una variación breve si es necesario, por ejemplo:

   ```text
   Reescribe la opción 3 para personal técnico de turno. Usa un tono directo y colaborativo, sin prometer resultados cuantificados.
   ```

5. Destaque que Ideas es adecuado para alternativas iniciales, pero la selección final debe considerar viabilidad, seguridad, presupuesto, responsables y políticas internas.

**Resultado esperado:**

El agente propone seis iniciativas diferenciadas, con mensajes, audiencias, acciones e indicadores sugeridos.

**Verificación:**

Compruebe que las ideas:

- Son alternativas y no una lista de afirmaciones presentadas como hechos.
- Evitan metas numéricas no respaldadas por datos.
- Incluyen una precaución o riesgo práctico de implementación.
- Mantienen un enfoque de mejora continua y no punitivo.

---

### Paso 5. Mejorar un prompt de análisis de riesgos con Prompt Coach

**Objetivo:** Refinar un prompt creado en la práctica 01-00-01 para reducir ambigüedad y pedir resultados verificables.

**Instrucciones:**

1. Abra el documento:

   ```text
   /CopilotLabs/EnergiaHorizonte/01_Prompts_validados_Energia_Horizonte.docx
   ```

2. Localice el prompt de análisis de riesgos elaborado en la práctica anterior. Si se requiere un ejemplo de demostración, use el siguiente texto inicial:

   ```text
   Analiza los riesgos de operación de Central Andes y dime qué debemos hacer.
   ```

3. Seleccione el agente **Prompt Coach**.
4. Envíe el prompt inicial junto con esta solicitud:

   ```text
   Mejora este prompt para que permita analizar riesgos operativos de la Central Solar Andes usando únicamente fuentes autorizadas del laboratorio.

   El prompt mejorado debe:
   - Definir audiencia: responsable de operaciones.
   - Pedir una tabla con riesgo, evidencia disponible, impacto potencial, urgencia, acción recomendada y dato pendiente.
   - Exigir que se distingan hechos, inferencias y elementos no confirmados.
   - Solicitar referencias a las fuentes utilizadas.
   - Prohibir inventar cifras, responsables, fechas o causas.
   - Indicar que el resultado es un borrador para validación humana y no una instrucción operativa definitiva.

   Devuelve primero el prompt mejorado y después explica en cinco viñetas qué ambigüedades se corrigieron.
   ```

5. Revise el prompt mejorado.
6. Compare el prompt inicial con el resultado y señale los elementos añadidos: objetivo, audiencia, fuentes, formato, criterios y límites.

**Resultado esperado:**

Prompt Coach genera una versión estructurada que solicita contexto, limita las fuentes, define el formato y requiere transparencia respecto a incertidumbres.

**Verificación:**

El prompt mejorado debe incluir explícitamente:

- Fuentes autorizadas.
- Formato de salida solicitado.
- Distinción entre hechos e inferencias.
- Referencias o trazabilidad.
- Prohibición de inventar información.
- Validación humana previa a cualquier decisión.

---

### Paso 6. Crear el agente personalizado “Asistente de Operación Central Andes”

**Objetivo:** Crear un agente de demostración en Agent Builder con un propósito limitado y conocimiento empresarial aprobado.

**Instrucciones:**

1. En Microsoft 365 Copilot, abra **Agent Builder** o la opción equivalente para crear un agente.
2. Seleccione **Crear un agente**.
3. Configure los datos básicos:

   | Campo | Valor |
   |---|---|
   | Nombre | `Asistente de Operación Central Andes` |
   | Descripción | Asistente de consulta para resumir prioridades operativas y de mantenimiento de Central Andes usando documentos aprobados del laboratorio. |
   | Estado de publicación | Borrador o uso exclusivo de demostración |

4. En el campo de propósito o instrucciones principales, agregue el siguiente contenido:

   ```text
   Eres el Asistente de Operación Central Andes de Energía Horizonte.

   Tu propósito es ayudar a personal autorizado a comprender prioridades de mantenimiento, riesgos operativos, acciones pendientes y contexto operativo de la Central Solar Andes, usando solamente las fuentes aprobadas configuradas para este agente.

   Reglas de comportamiento:
   - Responde en español, con tono profesional, claro y orientado a operaciones.
   - Fundamenta las respuestas en las fuentes aprobadas y cita o identifica el documento de origen cuando sea posible.
   - Distingue entre hechos documentados, inferencias y datos no confirmados.
   - No inventes cifras, fechas, responsables, causas, estados de equipos ni compromisos.
   - Si la información no está en las fuentes, indica: “No encuentro evidencia suficiente en las fuentes aprobadas”.
   - No emitas instrucciones de seguridad, maniobras, consignaciones ni decisiones operativas definitivas.
   - Para prioridades de mantenimiento, presenta una lista priorizada con evidencia disponible, motivo de prioridad y dato pendiente de validar.
   - Recuerda que la respuesta es un borrador de apoyo y requiere validación humana antes de actuar.
   ```

5. Configure preguntas sugeridas, por ejemplo:

   ```text
   ¿Cuáles son las prioridades de mantenimiento identificadas para Central Andes?
   ```

   ```text
   Resume los riesgos operativos y las acciones pendientes documentadas.
   ```

   ```text
   ¿Qué información falta para confirmar la prioridad de mantenimiento de los inversores?
   ```

6. En la sección de conocimiento, fuentes o archivos, agregue únicamente los siguientes documentos:

   ```text
   /CopilotLabs/EnergiaHorizonte/01_Informe_operativo_Central_Solar_Andes.docx
   /CopilotLabs/EnergiaHorizonte/02_Resumen_ejecutivo_y_acciones.docx
   ```

7. No agregue el archivo Excel ni fuentes externas para esta demostración, ya que el alcance del agente se limita a los dos documentos aprobados.
8. Revise los permisos de las fuentes. Confirme que el agente no amplía el acceso de los usuarios a contenido que no podrían abrir directamente.
9. Guarde el agente como borrador o para uso interno de demostración.

**Resultado esperado:**

Se crea un agente denominado **Asistente de Operación Central Andes**, con instrucciones explícitas, límites de respuesta, preguntas sugeridas y dos fuentes documentales aprobadas.

**Verificación:**

Compruebe que la configuración cumple estos criterios:

- El nombre del agente es correcto.
- Las fuentes son exclusivamente `01_Informe_operativo_Central_Solar_Andes.docx` y `02_Resumen_ejecutivo_y_acciones.docx`.
- Las instrucciones obligan a identificar incertidumbres.
- El agente no se publica para toda la organización.
- El agente no promete decisiones operativas autónomas ni instrucciones de seguridad.

---

### Paso 7. Probar el agente personalizado con una prioridad de mantenimiento

**Objetivo:** Validar que el agente responde dentro de su propósito y se fundamenta en las fuentes configuradas.

**Instrucciones:**

1. Abra la vista de prueba del agente **Asistente de Operación Central Andes**.
2. Envíe la siguiente pregunta:

   ```text
   Con base únicamente en las fuentes aprobadas, ¿cuáles son las prioridades de mantenimiento para la Central Solar Andes?

   Preséntalas en una tabla con:
   - Prioridad.
   - Evidencia documentada.
   - Motivo de prioridad.
   - Acción o seguimiento mencionado.
   - Información que debe validar el equipo de operaciones.

   Identifica las fuentes utilizadas y no inventes datos ausentes.
   ```

3. Revise la respuesta.
4. Compare al menos una prioridad y una acción con los documentos fuente originales.
5. Si el agente indica que no puede confirmar un dato, considere esa respuesta adecuada cuando la información no esté documentada.
6. No publique el agente fuera del laboratorio. Explique que antes de una publicación real se requiere revisar:
   - Permisos de los usuarios.
   - Propiedad y actualización de las fuentes.
   - Datos sensibles.
   - Instrucciones y límites del agente.
   - Cumplimiento, seguridad y gobierno de la información.

**Resultado esperado:**

El agente devuelve una lista o tabla de prioridades basada en los dos documentos aprobados, identifica incertidumbres y no agrega información no respaldada.

**Verificación:**

La prueba es satisfactoria si:

- La respuesta se relaciona con mantenimiento y operación de Central Andes.
- Se identifican fuentes documentales utilizadas.
- No se observan cifras, fechas o responsables inventados.
- Se señalan datos pendientes cuando no existe evidencia suficiente.
- El agente permanece como borrador o limitado al entorno de laboratorio.

## Validación y pruebas

Complete la siguiente lista de validación antes de finalizar la práctica:

| Comprobación | Criterio de aceptación |
|---|---|
| Uso de Analista | Se analizó `02_Datos_generacion_y_disponibilidad.xlsx` y se generaron preguntas de validación. |
| Uso de Investigador | La nota contiene referencias públicas verificables y distingue hechos de recomendaciones. |
| Uso de Ideas | Se generaron alternativas de campaña sin afirmar resultados no demostrados. |
| Uso de Prompt Coach | El prompt mejorado incluye objetivo, audiencia, fuentes, formato, límites y validación humana. |
| Creación del agente | Existe el agente `Asistente de Operación Central Andes` en estado de borrador o demostración. |
| Fuentes del agente | Solo se configuraron `01_Informe_operativo_Central_Solar_Andes.docx` y `02_Resumen_ejecutivo_y_acciones.docx`. |
| Prueba del agente | La respuesta sobre prioridades de mantenimiento se fundamenta en fuentes y explicita incertidumbres. |
| Gobernanza | El agente no se publicó fuera del entorno autorizado. |

### Criterios de calidad de las respuestas

Antes de aceptar una respuesta generada por cualquier agente, aplique estas tres preguntas:

1. **¿Está fundamentada?**  
   Confirme que cita fuentes, archivos o referencias y que estas respaldan el contenido.

2. **¿Está completa?**  
   Revise si faltan períodos, activos, riesgos, responsables, acciones o datos relevantes.

3. **¿Es adecuada para la decisión?**  
   Compruebe que el nivel de detalle, la precisión y las limitaciones declaradas son suficientes para el uso previsto.

## Solución de problemas

### Problema 1: No aparece uno de los agentes especializados o Agent Builder

**Síntomas:**  
No se visualiza Analista, Investigador, Ideas, Prompt Coach o la opción para crear un agente en Agent Builder.

**Causa probable:**  
El agente puede no estar habilitado para el tenant, la licencia asignada puede no incluir la capacidad, o la cuenta actual no dispone de permisos de creación de agentes.

**Solución:**  

1. Confirme que inició sesión con `instructor.copilot@tenant-energiahorizonte.onmicrosoft.com`.
2. Actualice la página de Microsoft 365 Copilot y vuelva a abrir el catálogo de agentes.
3. Compruebe con el administrador del tenant si el agente o Agent Builder está habilitado para el entorno de laboratorio.
4. Si Agent Builder no está disponible, realice la demostración revisando la configuración prevista del agente y use Copilot Chat con los dos documentos aprobados como fuentes, sin publicar ni simular permisos no autorizados.

### Problema 2: El agente personalizado responde sin citar las fuentes o incluye información no confirmada

**Síntomas:**  
La respuesta sobre mantenimiento no identifica los documentos utilizados, presenta fechas o responsables no documentados, o responde con excesiva seguridad ante información ausente.

**Causa probable:**  
Las instrucciones del agente son insuficientemente específicas, las fuentes no se cargaron correctamente, el contenido de los documentos no contiene el dato solicitado o el modelo generó una inferencia no claramente etiquetada.

**Solución:**  

1. Revise que las dos fuentes correctas estén configuradas y accesibles:
   - `01_Informe_operativo_Central_Solar_Andes.docx`
   - `02_Resumen_ejecutivo_y_acciones.docx`
2. Refuerce las instrucciones del agente con esta regla:

   ```text
   Para cada prioridad, identifica el documento fuente. Si no existe evidencia documental, indica que no hay evidencia suficiente y no propongas un dato como confirmado.
   ```

3. Reformule la pregunta para exigir referencias y separar hechos de datos pendientes.
4. Compare la salida con los documentos originales y corrija o descarte cualquier afirmación no respaldada.

## Limpieza

1. Mantenga todos los archivos de prácticas anteriores en:

   ```text
   /CopilotLabs/EnergiaHorizonte/
   ```

2. No elimine los documentos de entrada ni los resultados de las prácticas 01-00-01 y 01-00-02.
3. Deje el agente **Asistente de Operación Central Andes** en estado de borrador, demostración privada o elimínelo si la política del laboratorio exige no conservar agentes de prueba.
4. No comparta el agente con usuarios, grupos, Teams ni toda la organización.
5. Cierre las pestañas de Copilot, OneDrive y los documentos que contengan información operativa del laboratorio.
6. Cierre sesión si el equipo es compartido.

## Resumen

En esta práctica se aplicó la selección de agentes de Microsoft 365 Copilot según una necesidad empresarial: Analista para datos, Investigador para síntesis con fuentes, Ideas para alternativas y Prompt Coach para mejorar instrucciones. También se creó un agente personalizado con un propósito limitado y dos documentos aprobados como base de conocimiento.

Los resultados generados por Copilot deben considerarse borradores revisables. La calidad depende del prompt, del contexto disponible, de los permisos, de la actualidad de las fuentes y de la validación humana de cifras, prioridades, riesgos y recomendaciones.

### Recursos opcionales

- [Introducción a Microsoft 365 Copilot](https://learn.microsoft.com/es-es/copilot/microsoft-365/microsoft-365-copilot-overview)
- [Datos, privacidad y seguridad para Microsoft 365 Copilot](https://learn.microsoft.com/es-es/copilot/microsoft-365/microsoft-365-copilot-privacy)
- [Prácticas recomendadas para crear prompts en Microsoft 365 Copilot](https://support.microsoft.com/es-es/topic/pr%C3%A1cticas-recomendadas-para-crear-prompts-en-microsoft-365-copilot-3f1c7fbe-3b62-4f8b-9dbf-3b54f7d5d4e8)
- [Uso responsable de la inteligencia artificial de Microsoft](https://www.microsoft.com/es-es/ai/responsible-ai)
