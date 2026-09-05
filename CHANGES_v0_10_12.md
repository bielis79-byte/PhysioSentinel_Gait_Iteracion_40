# PhysioSentinel Gait Online v0.10.12

## Corrección definitiva de alineación visual

En las versiones anteriores los dos gráficos eran dos imágenes Matplotlib
independientes. Aunque compartían el mismo valor temporal, el renderizado podía
introducir pequeñas diferencias horizontales.

v0.10.12 cambia el diseño:

- mapa de fases y cinemática se dibujan dentro de UNA SOLA figura;
- ambos ejes comparten exactamente el mismo eje X;
- mismo `left`, `width`, `xlim` y transformación temporal;
- el cursor se dibuja en ambos paneles desde el mismo valor `tcur`;
- el slider maestro se estrecha y desplaza para aproximar su track al área útil
  de los gráficos;
- el vídeo sigue usando el mismo `current_time_s`.

Con esta arquitectura ya no existen dos sistemas de coordenadas gráficos
independientes que puedan desalinearse entre sí.
