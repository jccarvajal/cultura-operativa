# ANEXO C: Protocolo de Postmortem Estructural

Este protocolo no es una herramienta de investigación de recursos humanos; es un instrumento forense de rediseño. Su función es bloquear el reflejo defensivo del sistema frente a la falla. La organización siempre intentará proteger su diseño antes que corregirlo.

Si el postmortem termina en una persona, el diseño quedó intacto.

---

### I. REGLAS DE BLOQUEO (REGLAS ANTI-CULPA)

Para que el análisis sea estrictamente estructural, el auditor debe imponer tres restricciones absolutas desde el minuto cero de la investigación:

1. **El error es el síntoma, no la causa raíz:** Se prohíbe cerrar el análisis en "error humano", "descuido" o "negligencia" como la causa del incidente. El error marca el punto exacto donde el diseño dejó de sostener la operación.
2. **Aislamiento de la racionalidad táctica:** Se asume que la decisión fue la única opción operativamente viable dentro del sistema, dadas las herramientas, los tiempos, los incentivos y las presiones jerárquicas que el diseño le imponía en ese instante exacto.
3. **Prohibición del sesgo retrospectivo:** Se prohíbe analizar el evento con la información que se tiene después del colapso. Se audita únicamente con la telemetría y las señales que la red tenía disponibles un segundo antes de la falla. El sistema no falló con información completa; falló con la información que el diseño permitió.

---

### II. MATRIZ DE INTERROGACIÓN FORENSE

El auditor estructural reemplaza las preguntas de responsabilidad moral por preguntas de arquitectura de sistemas. Toda investigación debe responder el siguiente esquema:

| Pregunta Tradicional (Prohibida) | Pregunta Estructural (Obligatoria) | Objetivo Forense |
| :--- | :--- | :--- |
| ¿Quién cometió el error? | ¿Qué configuración hizo que fallar fuera la única opción operativamente viable? | Detectar la tensión real de incentivos operando sobre la primera línea. |
| ¿Por qué se ignoró el procedimiento? | ¿Cuál era el costo (en tiempo o conflicto) de cumplir el procedimiento? | Identificar fricción excesiva, metas contradictorias y controles degradados. |
| ¿Por qué no se reportó el riesgo a tiempo? | ¿Cuál era el costo de visibilidad para el nodo que poseía el dato? | Auditar la arquitectura de transparencia y evidenciar el silencio estructural. |
| ¿Quién debe asumir la culpa? | ¿Qué nodo impuso la restricción y qué nodo absorbió la consecuencia? | Medir el grado de desacople entre la autoridad de decisión y la consecuencia. |

---

### III. VECTORES DE LEVANTAMIENTO DE EVIDENCIA

La recolección de datos debe diseccionar la tríada operativa que sostenía el comportamiento en el momento de la falla:

**A. Vector de Tolerancia y Precedente (Capítulo 16)**
* Levantar evidencia de cuántas veces antes se había ejecutado la misma desviación de forma exitosa sin detonar alarmas ni recibir castigo.
* Determinar si la jerarquía había enviado señales previas tolerando o premiando esa ruta paralela por su velocidad. La repetición sin consecuencia redefine el estándar operativo.

**B. Vector de Telemetría (Capítulo 18)**
* Rastrear dónde se originó la primera anomalía y en qué nodo se interceptó o detuvo la información.
* Identificar el "peaje informacional": verificar si el sistema penalizaba implícitamente el acto de escalar malas noticias. Todo peaje informacional reduce la visibilidad del sistema.

**C. Vector de Dilución (Capítulo 14)**
* Analizar la cadena de aprobaciones formales previas a la materialización de la falla.
* Auditar el "cumplimiento ritualista": demostrar qué firmas en la cadena de flujo validaron el proceso simulando restricción, sin ejercer escrutinio ni exposición a consecuencia.

---

### IV. MANDATO DE RECONFIGURACIÓN OBLIGATORIA

Un postmortem estructural no produce aprendizaje declarativo, correos de concientización ni actas de compromiso ético. Produce modificaciones de diseño. El resultado de este protocolo debe desencadenar, de forma auditable, una de las siguientes reconfiguraciones:

1. **Eliminación o rediseño de controles:** Si un control formal demostró no restringir el riesgo ni aportar telemetría, debe ser eliminado o rediseñado con consecuencia. Mantenerlo es institucionalizar la simulación.
2. **Reasignación de la consecuencia:** Acoplar el costo de la falla al nodo jerárquico que impuso la presión por velocidad o que diseñó el flujo inoperante, cuando el diseño hizo la falla la opción operativamente viable.
3. **Modificación del incentivo dominante:** Alterar la métrica que estaba siendo protegida y que empujó al sistema a operar consistentemente fuera de sus márgenes de seguridad formales.

---

### V. CRITERIO DE VALIDACIÓN DEL POSTMORTEM

Un postmortem estructural solo es válido si cumple simultáneamente:

* Identifica al menos una tensión de incentivos real.
* Identifica al menos un punto de ceguera en la telemetría.
* Identifica al menos un desacople entre decisión y consecuencia.

**Regla:** Si el análisis no modifica incentivos, flujos de información o asignación de consecuencia, no es un postmortem estructural. Es narrativa.

---

### VI. PRUEBA DE ESTRÉS DEL POSTMORTEM

El protocolo debe validarse bajo condiciones controladas.

**Procedimiento:**
1. Seleccionar un incidente reciente ya cerrado por la organización.
2. Reprocesarlo aplicando este protocolo.
3. Comparar:
   * Causa original declarada.
   * Causa estructural detectada.
   * Distribución de consecuencia.
   * Cambios reales implementados.

**Resultado esperado:**
Desplazamiento desde la culpa individual hacia la configuración sistémica; identificación clara de incentivos, telemetría y consecuencia.

**Diagnóstico:**
Si el resultado no cambia respecto al análisis original, el sistema no está ejecutando un postmortem; está documentando fallas.

---

**CONCLUSIÓN DEL PROTOCOLO**

El éxito de este instrumento se mide bajo una única regla: 

Si no genera resistencia en la jerarquía, no fue estructural; fue descriptivo. 

Si la ejecución del postmortem no altera la física de los procesos, la organización no aprendió; optimizó la evasión de responsabilidad.