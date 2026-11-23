# Compendio de skills y perfiles de agente

**Estado:** 22 de noviembre de 2026  
**Propósito:** inventariar las skills locales, perfiles de especialidad considerados y pruebas disponibles para orientar la próxima guía visual.

## Contexto de uso

**Maite: Rumbo al Salar** es un caso de estudio para probar agentes, skills y creación de juegos HTML. No hay certeza de que se retome ni de que su género, arte, historia o tecnología se usen en la hackathon. Las pruebas sirven para detectar buenas prácticas y fallos; no fijan el estilo de un proyecto futuro.

Una skill es una guía de trabajo reutilizable. Los perfiles de agente de este documento son especialidades propuestas en `AGENTS.md`; no se han creado ni delegado subagentes reales.

## Skills del proyecto

| Skill | Uso principal | Prueba o referencia |
| --- | --- | --- |
| `hackathon-game-orchestrator` | Inspeccionar el workspace, acordar reto y tecnología, planificar una muestra jugable e integrar entrega sin asumir género o motor. | Existe en `.agents/skills/`; todavía no tiene una evaluación con resultado propio. |
| `rpg-web-prototyping` | Planificar o implementar RPG narrativo en HTML, CSS y JavaScript cuando el equipo elige ese stack. | Existe en `.agents/skills/`; Maite demuestra el stack web, pero no se ha registrado una prueba aislada de la skill. |
| `cozy-pixelart-design` | Diseñar/revisar escenas y assets originales de pixel art top-down, con legibilidad y escala consistentes. | Probada con la cantera: [resultado top-down](skill-evaluations/cantera-chile/01-pixelart-topdown-preview.jpg). |
| `dimensional-pixel-scenes` | Integrar personajes pixelados con entornos de profundidad 2.5D, cámara, escala y oclusión. | Probada con la cantera: [escena 2.5D](skill-evaluations/cantera-chile/02-escena-2-5d-preview.jpg). |
| `spatial-map-camera-flow` | Revisar rutas transitables, zonas bloqueadas, entradas, cámaras y continuidad entre exterior e interior. | Probada con un mapa conceptual de cantera: [mapa y transición](skill-evaluations/cantera-chile/03-mapa-transiciones-preview.jpg). No valida colisiones reales. |
| `character-identity-portraits` | Mantener identidad entre retratos, expresiones y hoja de referencia del personaje. | Probada con Maite: [atlas 2 x 2](skill-evaluations/character-art/maite-portrait-expressions-preview.jpg). |
| `sprite-animation-pipeline` | Crear/revisar hojas de sprites y ciclos con resolución, celdas, direcciones y anclajes configurables. | Probada con Maite: [ciclo de caminata, borrador](skill-evaluations/character-art/maite-walk-cycle-draft-preview.jpg). Conserva un halo rojo y no está listo para producción. |
| `character-reference-sheet-maintainer` | Mantener una referencia que conecte personalidad, identidad visual, assets, metadatos y procedencia. | Probada con [ficha de Maite](skill-evaluations/character-art/maite-reference-sheet-test.md); detectó una discrepancia de largo de cabello entre el plan y los assets. |
| `puzzle-design-reviewer` | Revisar claridad, solución, pistas, feedback, controles y reintentos de puzles. Elige representación según la mecánica; no exige un estilo visual universal. | Probada mediante revisión estática del [puzle de turnos](skill-evaluations/puzzles/roster-puzzle-review.md). |

### Skills de apoyo usados

- `imagegen` generó las pruebas visuales de cantera y personaje a partir de referencias. Las imágenes generadas son conceptos, no assets aprobados automáticamente.
- `skill-creator` se usó para crear y validar las skills del proyecto.

## Perfiles de agente y especialidades

Los siguientes roles están descritos en `AGENTS.md`. Son áreas de trabajo, no agentes activos asignados.

| Perfil | Para qué sirve | Estado en esta prueba |
| --- | --- | --- |
| `game-designer` | Define bucle principal, reglas, objetivo y alcance mínimo. | Recomendado; sin prueba aislada. |
| `web-game-engineer` | Implementa y mantiene el juego cuando el equipo elige tecnologías web. | Coincide con el stack de Maite; no se delegó a un agente. |
| `godot-engineer` | Implementa escenas, lógica y exportación si el equipo elige Godot. | Especialidad condicional; tecnología futura sin decidir. |
| `unity-engineer` | Implementa escenas, lógica y build si el equipo elige Unity. | Especialidad condicional; tecnología futura sin decidir. |
| `visual-audio` | Mantiene coherencia de arte/sonido y registra recursos externos. | Recomendado; aún no probado como perfil. |
| `playtest-reviewer` | Prueba como persona nueva y reporta fallos reproducibles. | Pendiente de recorrido interactivo; las revisiones recientes fueron estáticas. |
| `delivery-writer` | Prepara instrucciones, créditos, licencia y documentación de entrega. | Útil si existe entrega; no prioridad hasta confirmar el reto. |
| `live-demo-coach` | Organiza una demostración del juego funcionando. | Pendiente de saber si Maite o el stack se retoman. |
| `integrator` | Integra cambios y conserva una versión ejecutable. | Rol previsto; no se delegaron cambios. |

Perfiles adicionales conversados:

- **Editor narrativo:** probado como perfil con una escena de Maite. Resultado antes/después en [editor-narrativo.md](skill-evaluations/narrative-balance/editor-narrativo.md).
- **Analista de balance:** probado como perfil con tres secuencias de 20 decisiones. Alcance y límites en [analisis-balance.md](skill-evaluations/narrative-balance/analisis-balance.md).
- **Auditor de recursos:** recomendado para identificar fuente, autoría, licencia y cambios de assets; todavía sin prueba.
- **Encargado de puzles:** no es un agente real; quedó como skill reutilizable `puzzle-design-reviewer`.

## Resultados de evaluación

### Cantera como comparación de arte y mapa

Se mantuvo una misma cantera ficticia chilena y se compararon una vista top-down, una escena 2.5D y un concepto de mapa/transición. La [nota de prueba](skill-evaluations/cantera-chile/README.md) contiene las imágenes y la referencia fotográfica general a [El Way, Antofagasta, publicada por Knight Piésold](https://www.knightpiesold.com/en/projects/production-capacity-increase-of-the-el-way-mine/). Las imágenes no representan esa operación y el mapa no es una navegación validada.

### Personajes

Las referencias activas de Maite fueron el atlas local de retratos y la hoja de cuerpo completo. La [prueba de personajes](skill-evaluations/character-art/README.md) conserva los resultados y la evaluación. El ciclo generado de caminata queda como borrador por el halo rojo; no se incorporó al juego.

### Narrativa y balance

Se editó una escena real sin cambiar `index.html` y se calculó una comparación aritmética de decisiones usando las reglas actuales. Los resultados no equivalen a una prueba integral de la partida.

### Puzles

La revisión de asignación enumeró las seis permutaciones y encontró que el formulario admite varias respuestas incorrectas pero devuelve siempre la explicación del mismo error. La referencia y el caso reproducible están en `skill-evaluations/puzzles/roster-puzzle-review.md`. No se probó el flujo en navegador ni se modificó el código.

La investigación de mecánicas de juegos está en [referencias-mecanicas.md](skill-evaluations/puzzles/referencias-mecanicas.md). El principio transferible es representar cada puzle de acuerdo con la acción: paneles, mapas o tarjetas cuando se manipulan estados y asignaciones; texto cuando funciona mejor para un acertijo verbal o abstracto.

## Referencias externas

- [Blue Prince - Steam](https://store.steampowered.com/app/1569580/Blue_Prince/): salas variables, decisiones de exploración y pistas conectadas.
- [Professor Layton - guía de Nintendo](https://www.nintendo.com/en-gb/News/2011/The-Beginners-Guide-to-the-Professor-Layton-Games-253601.html) y [manual de Miracle Mask](https://csassets.nintendo.com/noaext/image/private/t_KA_PDF/3DS_Professor_Layton_Miracle_Mask_single_sheet_fr?_a=DATC1RAAZAA0): puzles variados, exploración e ideas de pistas escalonadas.
- [The Witness - Steam](https://store.steampowered.com/app/210970/The_Witness/): exploración y aprendizaje de ideas de puzle.
- [Return of the Obra Dinn - Steam](https://store.steampowered.com/app/653530/Return_of_the_Obra_Dinn/): exploración y deducción lógica.
- [The Case of the Golden Idol - Steam](https://store.steampowered.com/app/1677770/The_Case_of_the_Golden_Idol/): observar escenas y reconstruir hechos mediante deducción.
- [El Way - Knight Piésold](https://www.knightpiesold.com/en/projects/production-capacity-increase-of-the-el-way-mine/): referencia geográfica general para el concepto visual de cantera.

## Límites y próximos pasos

- La futura hackathon todavía no tiene género, estilo visual ni tecnología confirmados; conservar las skills como opciones neutrales.
- No se han delegado tareas a subagentes reales. Las evaluaciones de editor y analista se hicieron como perfiles.
- La guía visual puede consolidar mañana las imágenes, referencias, hallazgos y límites de cada prueba.
- El recorrido interactivo del puzle de turnos sigue pendiente; el skill de revisión se validó estructuralmente, pero aún no se ha probado por medio de una sesión de navegador.

