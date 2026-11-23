# Prueba de skills: cantera ficticia en Chile

Se recreó el mismo lugar ficticio en tres ejercicios para comparar el alcance de cada skill. El sitio común es una cantera árida del norte de Chile: pozo ovalado con tres terrazas, camino sinuoso que entra por el noroeste, caseta blanca de control en el borde noreste, poza turquesa al sureste y Andes al fondo.

## Referencia geográfica y visual

La geografía árida y las terrazas de extracción toman como referencia general la fotografía del proyecto de ampliación de la mina El Way, en Antofagasta, publicada por Knight Piésold:

[Production Capacity Increase of the El Way Mine — Knight Piésold](https://www.knightpiesold.com/en/projects/production-capacity-increase-of-the-el-way-mine/)

Las imágenes son interpretaciones ficticias generadas para esta prueba; no representan esa operación ni reproducen su fotografía. No son mapas de una faena real.

## Resultados

1. **[01-pixelart-topdown-preview.jpg](01-pixelart-topdown-preview.jpg) — `cozy-pixelart-design`:** comunica la forma general del pozo y el camino desde arriba, con colores cálidos y terreno diferenciable. Sirve como concepto visual; todavía no es un tileset y no valida colisiones.
2. **[02-escena-2-5d-preview.jpg](02-escena-2-5d-preview.jpg) — `dimensional-pixel-scenes`:** conserva el pozo, la caseta, la poza y la cordillera en una cámara oblicua con personaje en primer plano. Expresa profundidad, aunque el sprite requeriría ajuste para integrarse en un juego pixel-perfect.
3. **[03-mapa-transiciones-preview.jpg](03-mapa-transiciones-preview.jpg) — `spatial-map-camera-flow`:** combina vista de mapa, camino verde, zonas de riesgo rayadas, entrada a la caseta y vista interior por ventana. Es útil para discutir recorrido y cambio de punto de vista, pero sus marcas son una maqueta generada y deben verificarse contra geometría y colisiones reales.

Las versiones publicadas en este repositorio son previsualizaciones JPG comprimidas para revisión; los PNG originales permanecen en el workspace de prueba.

## Alcance

Prueba visual de las tres direcciones, no prueba de implementación ni validación técnica de navegación. Las tres imágenes comparten una descripción geográfica fija; cada una prioriza una cámara y una función distintas.



