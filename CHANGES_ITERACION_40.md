# PhysioSentinel Gait · Iteración 40

## Reconstrucción biplanar por secuencia de pasos y FPS reales
- Mantiene la sincronización periódica V39; no vuelve a ajustar el reloj mediante un IC aislado.
- Usa los FPS (Frames Per Second / Fotogramas por Segundo) reales de cada cámara de forma independiente.
- Calcula duración de frame frontal y lateral, resolución práctica e incertidumbre temporal conservadora por cuantización.
- Las coincidencias no se presentan como precisión sub-frame.
- Empareja primero la secuencia sincronizada de pasos IC y después reconstruye ciclos.
- Un ciclo V40 se define como: IC ipsilateral inicial → IC contralateral → siguiente IC ipsilateral.
- Ya no exige que los detectores frontal y lateral hayan construido previamente el mismo objeto `cycle`.
- La tolerancia temporal se adapta a la cámara más lenta, con límites conservadores anti-coincidencia espuria.
- Evalúa automáticamente hipótesis L/R directa e invertida.
- Exporta pares de pasos, ciclos por triplete, MAE temporal, error de secuencia, FPS, duración de frame, incertidumbre y diferencias expresadas en milisegundos/frames.
- Mantiene el método anterior como diagnóstico de comparación, pero el indicador V40 del segundo homólogo procede de los tripletes sincronizados.
- No implementa todavía triangulación 3D ni cinética estimada.
