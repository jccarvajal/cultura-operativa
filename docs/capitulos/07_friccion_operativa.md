## Capítulo 7: Normalización del desvío

La normalización del desvío no es un evento; es un proceso. Es la integración progresiva de una práctica originalmente inaceptable en la operación estándar. Es un resultado consistente con controles formales degradados que han perdido su capacidad de imponer consecuencia efectiva.

La normalización del desvío comienza cuando la vulneración de una regla no activa consecuencia. Este fenómeno se inicia cuando una desviación operativa —como eludir una barrera de seguridad o agilizar una validación para cumplir con una métrica— no produce consecuencia negativa y reduce la fricción del entorno. Bajo estas condiciones, el sistema expone que el costo del desvío es nulo. Cuando el desvío no tiene costo, se replica. Sin repetición, no hay normalización; un desvío aislado o fortuito no constituye cultura operativa.

El umbral de aceptación no es fijo; se desplaza con la ausencia de consecuencia. A medida que la elusión de la regla no detona penalizaciones, la desviación deja de operar como una excepción transitoria y pasa a constituir el estándar operativo. Una vez consolidado, el desvío no se corrige; se reemplaza mediante intervención estructural.

La normalización del desvío requiere invisibilidad operativa. ¿Qué arquitectura sostiene este bucle? Aquella diseñada con un flujo de información asimétrico y ciego a la ejecución táctica. El sistema audita el resultado, no la ruta. El mecanismo de supervisión verifica la existencia del output visible en verde, pero no registra ni activa consecuencia sobre el proceso invisible utilizado para alcanzarlo. 

Bajo este diseño, el sistema reduce márgenes de seguridad de forma incremental para sostener el flujo. La consolidación de este fenómeno evidencia que la tolerancia operativa al riesgo en la primera línea difiere radicalmente de la declarada en las matrices formales de la organización. Es la consecuencia natural de controles que dejaron de restringir (Capítulo 6).

Por lo tanto, cuando un desvío sistemático desencadena finalmente una falla catastrófica, penalizar de forma aislada al último operador en la cadena por incumplir el manual es un error de diagnóstico estructural. El operador no introduce el desvío; lo ejecuta. La organización no falla cuando ocurre la desviación; falla cuando la normaliza.