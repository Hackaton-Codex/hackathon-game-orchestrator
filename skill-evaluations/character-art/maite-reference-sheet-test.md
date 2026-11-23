# Ficha de referencia de Maite — prueba del skill

**Estado:** hoja de evaluación; no sustituye ni declara canon nuevo.  
**Skill probado:** `character-reference-sheet-maintainer`  
**Revisión:** 22 de noviembre de 2026.

## Identidad

- **Nombre:** Maite.
- **Rol narrativo confirmado:** ingeniera civil en minas.
- **Personalidad confirmada en `PLAN.md`:** resiliente y cercana.
- **Voz:** clara y práctica en la muestra de diálogo revisada; rasgo observado, pendiente de confirmación como regla general.
- **Edad y complexión:** no especificadas.

## Identidad visual

- **Rasgos que aparecen en los assets:** cabello oscuro con reflejos rojizos y trenzas; lentes; casco amarillo con lámpara; chaqueta/chaleco naranja de alta visibilidad; ropa de terreno oscura y botas.
- **Discrepancia abierta:** `PLAN.md` describe el cabello como corto con trenzas laterales; los retratos y sprites activos lo muestran más largo y con dos trenzas visibles. No se escoge una versión como canon en esta prueba.
- **Señales de reconocimiento que conviene preservar:** lentes, casco amarillo, trenzas y equipo naranja reflectante.

## Índice de assets

| Tipo | Asset | Estado | Datos conocidos |
| --- | --- | --- | --- |
| Retratos | `assets/character-portraits.png` (asset local de prueba; no incluido aquí) | Activo | Atlas 4 × 4; Maite aparece en la celda superior izquierda. Resolución de celda por verificar. |
| Sprites de cuerpo completo | `assets/character-sprites-anno-audited-v3.png` (asset local de prueba; no incluido aquí) | Activo en `index.html` | Vistas frontal, lateral y posterior, según el registro del proyecto. Confirmar dimensiones exactas de esta versión. |
| Movimiento | `assets/maite-walk-cycle-directions.png` (asset local de prueba; no incluido aquí) | Activo en `index.html` | Cuatro poses por dirección; frontal, lateral y posterior. El código prepara los cuadros y limpia halo cromático. |
| Retratos de expresiones | [previsualización del atlas](maite-portrait-expressions-preview.jpg) | Borrador de skill | Atlas generado 2 × 2; no está conectado al juego ni aprobado como canon. |
| Caminata alternativa | [previsualización del ciclo](maite-walk-cycle-draft-preview.jpg) | Borrador de skill | Hoja generada 4 × 3; conserva halo rojo, no usar como reemplazo del asset activo. |

## Parámetros de uso

- **Retratos en runtime:** el CSS usa atlas 4 × 4 y `image-rendering: pixelated`.
- **Sprite activo:** `index.html` carga `character-sprites-anno-audited-v3.png`.
- **Ciclo activo:** `index.html` carga `maite-walk-cycle-directions.png`; el render genera cuadros antes de mostrarlos.
- **Tamaño de celda/exportación:** no fijado para nuevos assets. El registro de 144 × 272 px corresponde a una iteración anterior; confirmar antes de reutilizarlo.
- **Tamaño mostrado en juego:** `PLAN.md` registra 54 × 102 px para el canvas de personajes; volver a comprobar si cambia el layout.
- **Pivote y timing exactos:** por verificar en el renderer.

## Referencias y procedencia

- Los assets activos son locales al repositorio y `PLAN.md` los describe como originales/generados para el proyecto. No se encontró una ficha individual de autoría/licencia por cada imagen.
- Los dos resultados de esta prueba se generaron a partir de los assets locales de Maite con `imagegen`; son borradores, no assets activos.

## Revisión del skill

El skill reunió en una sola ficha información narrativa, rutas a assets activos, estados de borrador y discrepancias. También detectó datos técnicos que no conviene inferir de una versión anterior. La discrepancia de largo de cabello requiere decisión del equipo antes de usar esta ficha como referencia canónica.

