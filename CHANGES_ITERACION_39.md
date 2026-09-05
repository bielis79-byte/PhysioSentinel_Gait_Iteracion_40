# PhysioSentinel Gait · Iteración 39

## Sincronización biplanar por fase periódica de la marcha
- Mantiene el reloj físico maestro de V38 como ancla temporal independiente.
- Calcula el periodo de paso frontal/posterior y lateral de forma independiente.
- Compara la periodicidad entre cámaras y cuantifica su diferencia porcentual.
- Busca una correspondencia de fase de la secuencia completa, no la coincidencia de un IC aislado.
- Sólo permite refinar el offset temporal si existen al menos dos eventos laterales coherentes y ordenados.
- Evalúa automáticamente hipótesis anatómica directa L↔L/R↔R e invertida L↔R/R↔L.
- Penaliza incoherencias entre intervalos consecutivos y mantiene proximidad al reloj V38 para reducir alias de un periodo.
- Exporta MAE de fase, error de secuencia, número de eventos de apoyo, offset periódico y si el refinamiento fue aplicado.
- La línea temporal diagnóstica incluye también los IC terminales (`next_ic`) para no ocultar el último evento de un ciclo.
- Añade auditoría completa de todos los candidatos IC laterales: lado, frame, tiempo de cámara, tiempo físico, score, estado y motivo de aceptación/rechazo.
- Conserva el indicador explícito “Segundo ciclo lateral con homólogo frontal”.
- No implementa todavía triangulación 3D ni cinética estimada.
