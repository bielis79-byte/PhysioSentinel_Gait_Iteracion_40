# PhysioSentinel Gait · Iteración 35

## Correspondencia temporal frontal-lateral robusta
- Mantiene el detector lateral multiseñal de la Iteración 34.
- Añade ajuste fino del desfase temporal a partir de IC (Initial Contact / Contacto Inicial) del mismo lado.
- El desfase global por correlación se conserva como aproximación inicial.
- La corrección fina se limita a ±0,45 s y considera también la duración del ciclo.
- Emparejamiento uno-a-uno por lado, proximidad temporal y duración de ciclo.
- La ventana biplanar se reevalúa con el desfase temporal final.
- Nuevas métricas: desfase global inicial, corrección fina y desfase final.
- Nueva tabla auditable de correspondencia: IC frontal, IC lateral alineado, error temporal y diferencia de duración.
- Si no existe correspondencia válida, se mantienen 0 ciclos biplanares; no se fuerzan emparejamientos.
- No se implementa todavía triangulación 3D ni cinética estimada.
