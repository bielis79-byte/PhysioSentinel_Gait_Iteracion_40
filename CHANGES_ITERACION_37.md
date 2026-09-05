# PhysioSentinel Gait · Iteración 37

## Consolidador de secuencia biplanar y protección anti-coincidencias espurias
- Determina explícitamente si el segundo ciclo lateral tiene un homólogo frontal.
- Optimiza la secuencia completa de ciclos, no un IC aislado.
- Conserva el orden temporal y el emparejamiento uno-a-uno.
- Evalúa hipótesis directa L↔L/R↔R e invertida L↔R/R↔L.
- Combina IC (Initial Contact / Contacto Inicial), duración IC→IC, alternancia anatómica, secuencia temporal y fase continua como evidencia auxiliar.
- Un único par no puede desplazar el desfase global >120 ms; si ocurre, se activa una protección y se recalcula con el desfase global.
- Los offsets alternativos derivados de IC requieren apoyo de al menos dos relaciones temporales.
- Nuevas métricas: pares consolidados, consistencia temporal de secuencia, segundo ciclo lateral con homólogo y activación de la protección anti-espuria.
- Calidad Alta/Moderada exige múltiples pares y coherencia temporal; un único par permanece en calidad Baja.
- No implementa aún triangulación 3D ni cinética estimada.
