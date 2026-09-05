# PhysioSentinel Gait · Versión 31

## Sincronización biplanar frontal + lateral

- Nuevo modo de dos cámaras orientado a grabación simultánea frontal/posterior + lateral.
- No exige que las cámaras comiencen a grabar en el mismo instante ni que ambas vean al paciente durante todo el recorrido.
- Detecta automáticamente el intervalo principal de visibilidad del paciente en cada cámara.
- Estima el desfase temporal buscando correspondencia del movimiento corporal entre ambas grabaciones.
- Restringe el análisis biplanar a la ventana temporal realmente compartida.
- Empareja ciclos del mismo lado mediante IC (Initial Contact / Contacto Inicial) sincronizado.
- Publica número de ciclos biplanares coincidentes y MAE (Mean Absolute Error / Error Absoluto Medio) temporal entre contactos iniciales.
- Clasifica la calidad de correspondencia de ciclos como Alta, Moderada, Baja o No calculable.
- Una correspondencia insuficiente queda advertida explícitamente y no debe utilizarse como base de cinética estimada sin revisión.
- Se conserva el análisis frontal completo y el análisis lateral complementario; no se ejecuta todavía dinámica inversa ni cinética.
- Se mantiene la preparación para futura reconstrucción 3D (Three-Dimensional / Tridimensional) cuando exista calibración adecuada.

## Corrección de empaquetado
- Se incorpora `requirements.txt` al paquete distribuible.
- Se añade `opencv-python-headless>=4.10,<5`, requerido por `import cv2` para el módulo biplanar.
- Se reincorporan `Dockerfile` y `packages.txt` para despliegue reproducible.
