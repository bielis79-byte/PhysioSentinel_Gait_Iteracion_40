# PhysioSentinel Gait · Iteración 38

## Reloj físico maestro independiente de IC/TO
- La sincronización temporal se fija antes de comparar IC (Initial Contact / Contacto Inicial) y TO (Toe Off / Despegue del Pie).
- El reloj maestro combina señales continuas de pelvis, tronco, rodillas y tobillos.
- Parte del desfase global y permite un refinamiento acotado mediante correlación corporal continua.
- Los IC no pueden modificar el reloj para mejorar artificialmente su coincidencia.
- Los eventos frontal y lateral se proyectan después sobre un único tiempo físico.
- Mantiene comparación automática de hipótesis L↔L/R↔R y L↔R/R↔L.
- Mantiene emparejamiento ordenado uno-a-uno, duración IC→IC y control de secuencia.
- Exporta cada IC detectado con tiempo físico exacto como métrica V38, incluyendo frame, tiempo de cámara y offset maestro en notas.
- Mantiene el indicador explícito de si el segundo ciclo lateral posee homólogo frontal.
- No implementa todavía triangulación 3D ni cinética estimada.
