# PhysioSentinel Gait · Iteración 34

## Objetivo
Mejorar específicamente la detección lateral de eventos de marcha antes de volver a intentar el emparejamiento frontal-lateral y, posteriormente, la cinética estimada.

## Cambios principales
- Nuevo detector lateral multiseñal de IC (Initial Contact / Contacto Inicial) y TO (Toe Off / Despegue del Pie).
- Combina posición anteroposterior del pie respecto a pelvis, velocidad horizontal relativa del pie, trayectoria vertical de talón/tobillo y extensión de rodilla cuando está disponible.
- Separa explícitamente eventos candidatos de eventos aceptados.
- Añade coherencia temporal y alternancia izquierda-derecha para reducir falsos contactos.
- Mantiene la detección sobre toda la ventana visible lateral antes del recorte biplanar.
- Añade métricas de auditoría: candidatos IC laterales, IC laterales aceptados y ciclos IC→IC laterales.
- El emparejamiento biplanar sigue siendo conservador: solo se aceptan ciclos del mismo lado temporalmente coherentes dentro de la ventana física común.
- No añade todavía reconstrucción 3D (Three-Dimensional / Tridimensional) ni cinética estimada.

## Alcance
Los eventos siguen siendo estimaciones cinemáticas 2D (Two-Dimensional / Bidimensional). No equivalen a eventos derivados de plataforma de fuerzas.
