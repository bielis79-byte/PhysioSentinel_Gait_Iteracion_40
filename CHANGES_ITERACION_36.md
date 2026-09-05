# PhysioSentinel Gait · Iteración 36

## Diagnóstico y auto-resolución de correspondencia biplanar
- Conserva la detección multiseñal lateral de V34 y la sincronización global/fina de V35.
- Añade línea temporal diagnóstica de todos los IC (Initial Contact / Contacto Inicial) frontales y laterales alineados.
- Compara automáticamente dos hipótesis anatómicas:
  - directa: L↔L y R↔R;
  - invertida: L↔R y R↔L.
- Selecciona la hipótesis por número de pares válidos, error temporal, coherencia de duración y proximidad al desfase global.
- Añade una segunda referencia temporal independiente de IC basada en fase continua de movimiento distal.
- No fuerza pares si ninguna hipótesis cumple los criterios.
- Mantiene una tabla auditable por ciclo con tiempos y errores.
- No implementa todavía triangulación 3D ni cinética estimada.
