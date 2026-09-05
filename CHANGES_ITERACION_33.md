# PhysioSentinel Gait · Iteración 33

## Objetivo
Corregir el cuello de botella observado en la Iteración 32: la sincronización frontal-lateral era coherente, pero la detección de ciclos se realizaba después de recortar a una ventana biplanar demasiado corta y podía dejar 0 ciclos IC→IC válidos.

## Cambios
- Detección de ciclos sobre toda la ventana visible de cada cámara antes de aplicar el recorte biplanar.
- Nuevo detector específico para vista lateral basado en la posición anteroposterior del pie respecto a la pelvis.
- IC (Initial Contact / Contacto Inicial) estimado desde extremos sagitales del pie.
- TO (Toe Off / Despegue del Pie) estimado dentro del ciclo mediante el extremo opuesto de la trayectoria sagital.
- Emparejamiento frontal-lateral posterior a la detección de ciclos y limitado a los ciclos que atraviesan la ventana física común.
- Compatibilidad temporal con FPS (Frames Per Second / Fotogramas por Segundo) diferentes entre cámaras.
- Nuevas métricas de control: ciclos detectados en la ventana visible completa frontal y lateral.
- Un único ciclo completo puede conservarse como evidencia de baja confianza; no se presenta como estimación robusta.
- Se mantienen separados el análisis 2D (Two-Dimensional / Bidimensional), la preparación 3D (Three-Dimensional / Tridimensional) y la futura cinética estimada.
- Corrección de textos antiguos de versión en la interfaz.

## No incluido todavía
- Triangulación 3D real.
- GRF (Ground Reaction Force / Fuerza de Reacción del Suelo).
- CoP (Center of Pressure / Centro de Presión).
- Momentos articulares o potencias articulares estimadas.
