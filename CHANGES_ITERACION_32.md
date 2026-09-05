# PhysioSentinel Gait · Versión 32

## Sincronización y cinemática biplanar fiable

- Emparejamiento biplanar estricto: si frontal o lateral tienen 0 ciclos IC→IC validados, Sentinel informa 0 ciclos coincidentes.
- Se elimina el falso positivo observado en Versión 31 (2 ciclos biplanares pese a 0 ciclos válidos por cámara).
- La sincronización mantiene ejes temporales físicos independientes y admite FPS distintos mediante tiempo en segundos/remuestreo.
- Nuevo visor de **Cinemática biplanar sincronizada**: combina variables frontales y laterales sobre un reloj temporal compartido.
- La curva 0–100 % del ciclo solo se habilita conceptualmente cuando existen ciclos IC→IC válidos en ambas cámaras.
- Mensajes y encabezados antiguos de v0.7/v25/v30 actualizados a Versión 32.
- Se aclara explícitamente que la Versión 32 NO realiza todavía triangulación 3D ni cinética estimada.
- Siglas nuevas desarrolladas en interfaz: IC (Initial Contact / Contacto Inicial), 2D (Two-Dimensional / Bidimensional), 3D (Three-Dimensional / Tridimensional), MAE (Mean Absolute Error / Error Absoluto Medio).
