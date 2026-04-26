# ANEXO F: Matriz de Asignación de Consecuencia

Las tradicionales matrices RACI (Responsible, Accountable, Consulted, Informed) son literatura corporativa. Describen cómo la organización desearía que se distribuyeran las tareas, pero no modelan la consecuencia. Este anexo reemplaza la ficción del organigrama con la física del riesgo. El sistema no responde a roles; responde a quién no puede evitar la consecuencia. Su objetivo es mapear, auditar y corregir el grado de acoplamiento estructural entre la autoridad que impone una decisión y el nodo que absorbe su consecuencia.

---

### I. AXIOMAS DE ASIGNACIÓN

Para auditar la responsabilidad real dentro de un sistema, el arquitecto debe operar bajo tres leyes innegociables:

1. **La responsabilidad no es el cargo; es la consecuencia que no se puede evitar:** Un rol documentado como "responsable" es nulo si el diseño lo protege del impacto de la falla. La responsabilidad sin consecuencia es ficción administrativa.
2. **La consecuencia siempre colapsa sobre el nodo con menor capacidad de defensa:** En ausencia de un diseño de acoplamiento rígido, la penalización esquivará a quien diseñó la regla y golpeará a quien intentó ejecutarla bajo presión. La consecuencia siempre converge en el nodo sin capacidad de veto.
3. **Decidir sin pagar es condición de colapso:** Cualquier estructura que permita a un nodo jerárquico exigir resultados sin absorber el riesgo de la ejecución está diseñada para el desastre. Si el decisor no puede absorber consecuencia, el sistema absorberá el colapso.

---

### II. MATRIZ DE CONTRASTE FORENSE

Esta herramienta desmantela la narrativa de la rendición de cuentas. Se aplica sobre procesos críticos y decisiones de alto riesgo, contrastando el flujo de la autoridad con el flujo del castigo.

| Variable Estructural | Pregunta de Auditoría Forense | Indicador de Desacople |
| :--- | :--- | :--- |
| **1. Nodo de Autoridad** | ¿Quién define la meta, recorta el presupuesto o impone la restricción de tiempo? | Impone condiciones sin exposición directa a la ejecución ni a la consecuencia. |
| **2. Nodo Táctico** | ¿Quién opera la maquinaria, firma el formulario o atiende al cliente final? | Absorbe ejecución sin capacidad de veto. |
| **3. Consecuencia Formal** | Según el manual, ¿quién debería responder si se vulnera el control? | La responsabilidad se diluye en abstracciones. |
| **4. Consecuencia Efectiva** | Cuando el riesgo se materializa, ¿quién es despedido, sancionado o culpado en la realidad? | Cierre mediante etiquetado de "error humano" para bloquear análisis estructural. |

**Dictamen Estructural:** Si el Nodo de Autoridad (1) impone las condiciones, pero la Consecuencia Efectiva (4) recae exclusivamente sobre el Nodo Táctico (2), el sistema está desacoplado. El sistema sustituyó gestión de riesgo por gestión de culpa.

---

### III. DETECCIÓN DE FUGAS DE RESPONSABILIDAD

La matriz expone de inmediato las tres tipologías clásicas mediante las cuales el sistema evade la consecuencia:

**A. El Escudo Jerárquico**
* *Mecánica:* La gerencia impone una meta de volumen matemáticamente incompatible con los controles de calidad. El operador asume el riesgo de adulterar el control para cumplir la meta y conservar su empleo.
* *El Colapso:* Cuando la falla se hace pública, el operador es despedido por "violación ética". La gerencia mantiene sus bonos por volumen. La consecuencia fue contenida en la base.

**B. La Dilución Colegiada (Capítulo 14)**
* *Mecánica:* Una decisión de alto riesgo requiere la firma cruzada de cinco gerencias distintas en un comité.
* *El Colapso:* La decisión destruye valor. El análisis postmortem demuestra que todos firmaron asumiendo que otro había revisado. Al estar la decisión socializada, no existe punto de aplicación de consecuencia. El riesgo quedó huérfano. Si validar no duele, validar no existe.

**C. La Transferencia de Fricción**
* *Mecánica:* Un departamento de diseño o cumplimiento (Compliance) crea un proceso inoperante y burocrático que bloquea la operación diaria, pero no asume métricas de negocio.
* *El Colapso:* La primera línea no alcanza las metas comerciales por cumplir la burocracia. Operaciones absorbe la penalización; Cumplimiento cumple métricas sin absorber impacto. 

---

### IV. INDICADORES DE DESACOPLE ESTRUCTURAL

El desacople no se declara; se mide. La siguiente batería permite cuantificar si la organización gestiona riesgo o gestiona culpa:

* % de incidentes donde la consecuencia recae en la primera línea.
* % de decisiones críticas donde el decisor no firma ejecución.
* Ratio autoridad vs. exposición al riesgo (quién decide vs. quién paga).
* Tiempo entre decisión y materialización de consecuencia.
* % de postmortems cerrados con causa "error humano".
* % de validaciones sin impacto posterior en responsabilidad.
* **Gradiente de consecuencia:** Distribución de impacto entre jerarquía y primera línea. 
    * *Regla:* Si el 80%+ del impacto cae en la ejecución, existe desacople estructural.

**Clasificación Operativa:**

* **Acoplamiento estructural:** Decisión y consecuencia convergen en el mismo nodo.
* **Acoplamiento degradado:** Consecuencia parcialmente redistribuida.
* **Desacople estructural:** Decisión y consecuencia operan en capas distintas.

**Regla Crítica:** Si la consecuencia no escala, el sistema no aprende.

---

### V. PRUEBA DE ESTRÉS DE ASIGNACIÓN

Para validar si el sistema realmente está acoplado, se ejecuta el siguiente escenario controlado:

1. **Inyección de restricción:** Introducir una restricción operativa (tiempo, recursos o conflicto de metas).
2. **Presión de decisión:** Forzar una decisión táctica bajo presión.
3. **Observación de flujo:** Documentar quién toma la decisión, quién ejecuta, quién queda expuesto y quién absorbe la consecuencia final.
4. **Intento de desplazamiento de consecuencia:** Documentar si se intentó redirigir la responsabilidad hacia otro nodo.

**Resultado Esperado (Sistema Sano):** Decisión y consecuencia están acopladas. La jerarquía no puede externalizar el riesgo hacia la base.
**Resultado Real (Sistema Defectuoso):** Decisión arriba, ejecución abajo, consecuencia abajo.

**Diagnóstico Automático:** Si el que decide no puede absorber consecuencia, la decisión es estructuralmente inválida. El sistema no falla donde se ejecuta; falla donde nadie paga.

---

### VI. PROTOCOLO DE REACOPLAMIENTO ESTRICTO

Una vez detectado el desacople, la auditoría debe imponer cambios en la arquitectura. La responsabilidad solo vuelve a existir si se aplican estas correcciones:

1. **Acoplamiento de Métricas de Castigo:** Si el operador es despedido por una falla de control inducida por la presión de tiempo, la métrica de desempeño de su jefatura directa debe recibir un impacto proporcional, automático e ineludible. El riesgo se comparte o no se asume.
2. **Erradicación de la Firma Nula:** Todo comité o cadena de validación debe justificarse estructuralmente. Si un nodo exige el derecho a vetar o aprobar (firma), asume automáticamente el porcentaje proporcional y verificable de la consecuencia de esa decisión. Validar sin riesgo queda prohibido.
3. **Inmunidad por Detención de Flujo:** Transferir el poder de detención a la primera línea. Si el nodo táctico detiene la operación citando un riesgo, la consecuencia económica de esa detención se transfiere automáticamente a la jerarquía operativa, no al operador.

---

### VII. SALIDA OPERACIONAL DEL INSTRUMENTO

La ejecución de esta matriz no produce un informe; produce una reconfiguración obligatoria del flujo de poder y riesgo. El producto final es el **Mapa de Acoplamiento de Consecuencia**.

Este mapa evidencia la arquitectura real de la organización, identificando de manera explícita los nodos protegidos y generando un listado de decisiones de alto impacto sin propietario de consecuencia. Permite predecir dónde colapsará el sistema e identificar dónde se está incubando el riesgo.

**Regla Final:** Toda decisión sin consecuencia asociada es deuda estructural. 
Toda deuda estructural se paga como crisis operativa o colapso sistémico.

---

### VIII. VALIDACIÓN DE LA MATRIZ

La matriz es válida solo si permite demostrar:

* Al menos un caso de desacople real.
* Al menos una decisión sin consecuencia asociada.
* Al menos un nodo protegido estructuralmente.

**Regla:** Si la matriz no identifica nodos protegidos, el análisis es superficial o el sistema está ocultando su arquitectura real.