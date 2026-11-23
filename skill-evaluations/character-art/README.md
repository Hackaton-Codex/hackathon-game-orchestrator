# Prueba de skills: arte de Maite

Se probaron dos flujos con la misma protagonista y referencias existentes del proyecto.

## Referencias

- Identidad y retrato de Maite: `assets/character-portraits.png` (asset del proyecto de prueba; no incluido aquí), celda superior izquierda.
- Proporciones, vestuario y vistas de cuerpo completo: `assets/character-sprites-anno-polished.png` (asset del proyecto de prueba; no incluido aquí), celdas de Maite.

## Resultados

- [`maite-portrait-expressions-preview.jpg`](maite-portrait-expressions-preview.jpg), creado con `character-identity-portraits`: atlas 2 × 2 con expresiones de alerta, escucha, esperanza y firmeza. La segunda pasada separó mejor escucha de alerta; los rasgos, vestuario y encuadre se mantienen consistentes.
- [`maite-walk-cycle-draft-preview.jpg`](maite-walk-cycle-draft-preview.jpg), creado con `sprite-animation-pipeline`: hoja 4 × 3 con cuatro poses para cada una de tres direcciones. Las poses y el tamaño de celda son una demostración, no una especificación fija.

Las imágenes publicadas son previsualizaciones JPG comprimidas; los PNG originales permanecen en el workspace de prueba.`r`n`r`n## Revisión

El retrato funciona como estudio visual de expresiones. La hoja de movimiento muestra alternancia de piernas y respeta la identidad, pero conserva un halo rojo alrededor de varios contornos pese a la pasada de limpieza. Se entrega como borrador: antes de incorporarla al juego habría que limpiar esos bordes y comprobar alpha, recortes, anclaje y loop a la resolución objetivo.

Las resoluciones y celdas se pueden adaptar. Para mayor resolución con detalle real, regenerar o redibujar a esa resolución nativa; para conservar el pixel grid, escalar con vecino más cercano en múltiplos enteros.

