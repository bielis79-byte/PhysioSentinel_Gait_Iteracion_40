# PhysioSentinel Gait · Versión 29

## Revisión del perfil biomecánico frontal (ICBF/ICS-0.4)

- El ICBF frontal deja de depender de simetría de rodilla/pie y se estructura en cuatro dominios: pelvis (30%), tronco (25%), COM/BOS (25%) y hombros-relación hombros/pelvis (20%).
- Rodilla frontal, valgo/varo proyectado, pie y retropié permanecen como descriptores clínicos y no penalizan el ICBF.
- Se añaden métricas para evitar que un ROM pequeño o una buena simetría oculten una postura anómala sostenida:
  - P95 absoluto de oblicuidad pélvica, inclinación lateral del tronco, oblicuidad de hombros y relación hombros-pelvis.
  - Asimetría de excursión lateral de pelvis, tronco, hombros y COM.
  - Consistencia cíclica 0–100 de pelvis, tronco, hombros, hombros-pelvis, COM y COM/BOS.
- Cada dominio frontal integra tres dimensiones cuando existen datos suficientes: magnitud, balance lateral y repetibilidad entre zancadas.
- Nueva agregación frontal no compensatoria: 65% media ponderada + 35% peor dominio, con techos cuando coexisten varios dominios <50/100. La interfaz avisa si se activa esta regla.
- COM/BOS adquiere mayor peso clínico dentro del perfil frontal. Los umbrales son operacionales internos y no se presentan como normalidad diagnóstica.
- En frontal+lateral se mantienen dos perfiles independientes: ICBF frontal y perfil cinemático sagital D/I. El combinado 60/40 se conserva solo para compatibilidad/exportación.
- APP_VERSION actualizado a 29.
