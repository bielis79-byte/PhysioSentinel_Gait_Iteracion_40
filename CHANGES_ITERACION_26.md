# PhysioSentinel Gait · Versión 26

## Cambio conceptual del índice
- Se separa la **capacidad locomotora** del **perfil biomecánico**. Un buen alineamiento de rodilla/pie ya no se presenta como evidencia de buena capacidad funcional.
- Nuevo **ICLM-0.1 experimental (0–100)**: regularidad/consistencia, simetría locomotora, velocidad de marcha medida cuando existe y grado de independencia/apoyo externo.
- Nueva **regla de déficit dominante**: velocidad muy baja, apoyo externo relevante o alteraciones locomotoras marcadas limitan la clasificación y no pueden ser compensadas por dominios segmentarios conservados.
- La discrepancia de recuento de pasos y otros fallos de detección pasan a afectar a **confianza de medición**, no a empeorar artificialmente la función.

## Entradas clínicas nuevas
- Independencia funcional: independiente, supervisión, contacto ocasional con apoyo externo, apoyo externo frecuente o ayuda física.
- Velocidad de marcha medida (m/s), opcional. La app no inventa m/s sin calibración válida.

## Presentación
- Pestaña 10 renombrada a **Capacidad funcional + Perfil biomecánico**.
- Muestra primero capacidad locomotora y después perfil biomecánico cuantitativo.
- Mantiene COM 2D, consistencia paso a paso y anexo completo de la Versión 25.

## Exportación
- Añade `locomotor_capacity_index`, `locomotor_capacity_raw`, `locomotor_measurement_confidence`, `measured_gait_speed_ms` y `functional_support_score`.

## Nota metodológica
ICLM-0.1 e IGPM-0.1 siguen siendo índices internos experimentales y no escalas diagnósticas validadas. La interpretación clínica prevalece y los umbrales deberán calibrarse/validarse con cohortes de referencia.
