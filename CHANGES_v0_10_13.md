# PhysioSentinel Gait Iteración 24

## Nueva pestaña 10 · Índice Global y Perfil Funcional de la Marcha

- Añade un Índice Global experimental IGPM-0.1 en escala 0–100.
- Clasificación interna: patrón global conservado/alteración mínima, alteración leve, moderada o marcada.
- Perfil por dominios con ponderación transparente:
  - Ritmo y regularidad: 20%
  - Simetría temporal: 20%
  - Control frontal de rodilla: 20%
  - Control pélvico: 15%
  - Tronco y coordinación: 10% teórico, mostrado como descriptor y no puntuado cuando no existe una dirección normativa universal.
  - Pie, retropié y estabilidad: 15%
- Ranking automático de déficits prioritarios.
- Cobertura y confianza interna del índice.
- Las métricas no calculables/no fiables no reciben 0: se excluyen y el peso disponible se redistribuye.
- El índice se añade a la exportación de métricas.
- Advertencias explícitas: no equivale a porcentaje de normalidad ni a escala diagnóstica/pronóstica validada.

## Compatibilidad

Mantiene todas las funciones de v0.10.12, incluida la pestaña de ciclo de marcha, cursor maestro sincronizado y exportación ZIP.
