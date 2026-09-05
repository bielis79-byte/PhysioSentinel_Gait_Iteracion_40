# PhysioSentinel Gait · Versión 27

## Revisión metodológica del perfil biomecánico según plano de cámara

La pestaña 10 deja de aplicar un único conjunto de dominios biomecánicos a cualquier configuración de cámara. Se introduce **IBV-0.2**, un perfil biomecánico dependiente de la vista, separado del Índice de Capacidad Locomotora (ICLM-0.1).

### Cámara frontal/posterior única
- Se elimina del compuesto la penalización por **magnitud absoluta del valgo/varo proyectado**.
- La rodilla solo puede contribuir mediante **discrepancia bilateral D/I**, evitando interpretar una alineación bilateral asociada a morfología, sexo, rotación de cadera o perspectiva como déficit automático.
- **Pie y retropié quedan fuera del índice compuesto** con frontal única. Se mantienen como variables descriptivas para seguimiento si la visibilidad y geometría son adecuadas.
- El componente puntuable se centra en **simetría frontal D/I de rodilla** y **control pélvico bilateral**.
- COM/BOS, tronco y coordinación permanecen descriptivos mientras no exista una dirección normativa universal transferible al proxy 2D.

### Frontal + lateral
- El compuesto prioriza **simetría cinemática sagital bilateral** de rodilla, cadera y tobillo-pie obtenida de la vista lateral.
- Añade **control pélvico bilateral** de la vista frontal.
- Valgo frontal absoluto y pie/retropié frontal siguen siendo descriptivos y no penalizan.
- Las puntuaciones sagitales se basan en diferencias D/I de P95 y ROM, no en comparar un ángulo individual con una supuesta normalidad universal.

### Lateral única
- El compuesto se limita a simetría sagital D/I de cadera, rodilla y tobillo-pie.
- No se puntúan variables exclusivas del plano frontal.

### Otros cambios
- La pestaña 10 muestra explícitamente qué variables son **deliberadamente no penalizadoras** y por qué.
- Se separa la clasificación del perfil biomecánico de la gravedad funcional: el IBV utiliza términos de simetría/discrepancia y no pretende graduar discapacidad.
- Se corrige el cálculo del ICLM para reconocer métricas prefijadas `front_` y `lateral_` en análisis de dos cámaras.
- La exportación añade `biomech_profile_index`, cobertura, confianza y dominios del IBV-0.2, manteniendo alias `gait_index_*` por compatibilidad histórica.
- Si la cobertura de dominios puntuables es <45%, el compuesto biomecánico se suprime para evitar falsa precisión.

## Alcance
IBV-0.2 continúa siendo un índice interno/experimental de síntesis y seguimiento. No equivale a porcentaje de normalidad, diagnóstico ni análisis cinemático 3D instrumentado.
