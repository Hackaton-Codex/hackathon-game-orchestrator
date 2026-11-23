# Compendio: toolkit general y caso Maite

**Actualizado:** 22 de noviembre de 2026

Este documento separa las herramientas que se pueden reutilizar en futuros proyectos de los resultados que pertenecen al caso de prueba **Maite: Rumbo al Salar**. Maite puede retomarse más adelante, pero no define la temática, tecnología ni dirección artística de la hackatón.

## Cómo usar el repositorio

1. Empieza con las reglas generales de [`AGENTS.md`](../AGENTS.md) y la skill [`hackathon-game-orchestrator`](../.agents/skills/hackathon-game-orchestrator/SKILL.md).
2. Confirma el reto, el tiempo disponible, las tecnologías conocidas, cómo se ejecutará la entrega y si se permite trabajo previo.
3. Recorta el alcance a una ruta jugable corta. Añade skills opcionales solo si encajan con el juego elegido.
4. Usa las pruebas de Maite como ejemplos para discutir decisiones; no asumas que su contenido debe pasar al nuevo juego.

El consejo operativo más importante para una hackatón breve es mantener una versión ejecutable desde temprano, revisar riesgos de entrega antes del final y ampliar contenido solo después de completar el núcleo jugable.

## A. Toolkit reutilizable

Estas skills son instrucciones reutilizables. “General” significa que se pueden volver a aplicar; **no** significa que todas deban activarse para cada juego.

| Área | Skill | Cuándo activarla |
| --- | --- | --- |
| Coordinación de hackatón | [`hackathon-game-orchestrator`](../.agents/skills/hackathon-game-orchestrator/SKILL.md) | Como punto de partida para inspeccionar el proyecto, acordar tecnología, recortar alcance e integrar entrega. |
| Prototipo web | [`rpg-web-prototyping`](../.agents/skills/rpg-web-prototyping/SKILL.md) | Solo si el equipo elige un RPG narrativo y tecnologías HTML, CSS y JavaScript. |
| Puzles | [`puzzle-design-reviewer`](../.agents/skills/puzzle-design-reviewer/SKILL.md) | Si el juego incluye puzles; revisa reglas, pistas, solución, feedback y reintentos. |
| Arte top-down | [`cozy-pixelart-design`](../.agents/skills/cozy-pixelart-design/SKILL.md) | Si el proyecto necesita escenarios o sprites originales de pixel art top-down con lectura clara. |
| Escenas con profundidad | [`dimensional-pixel-scenes`](../.agents/skills/dimensional-pixel-scenes/SKILL.md) | Si combina personajes pixelados con entorno 2.5D o una cámara con profundidad. |
| Mapa y cámara | [`spatial-map-camera-flow`](../.agents/skills/spatial-map-camera-flow/SKILL.md) | Si hay exploración, zonas transitables, interiores o cambios de punto de vista. |
| Retratos | [`character-identity-portraits`](../.agents/skills/character-identity-portraits/SKILL.md) | Si hay personajes con retratos o expresiones y se debe mantener su identidad visual. |
| Sprites y movimiento | [`sprite-animation-pipeline`](../.agents/skills/sprite-animation-pipeline/SKILL.md) | Si se requieren ciclos de movimiento con resolución, direcciones y cuadros configurables. |
| Hoja de personaje | [`character-reference-sheet-maintainer`](../.agents/skills/character-reference-sheet-maintainer/SKILL.md) | Si el equipo necesita una referencia que conecte personalidad, diseño, sprites, retratos y procedencia. |

### Perfiles de especialidad para coordinar

Los perfiles de [`AGENTS.md`](../AGENTS.md) describen funciones que se pueden asignar a agentes reales disponibles, si los hay. No son agentes creados por este repositorio ni una promesa de que la delegación estará disponible.

| Perfil | Responsabilidad | Cuándo priorizarlo |
| --- | --- | --- |
| `game-designer` | Bucle principal, objetivo, reglas y alcance mínimo. | Al convertir el reto en una idea jugable. |
| `web-game-engineer` | Implementación web. | Solo tras elegir tecnologías web. |
| `godot-engineer` | Escenas, lógica y exportación en Godot. | Solo tras elegir Godot. |
| `unity-engineer` | Escenas, lógica y build en Unity. | Solo tras elegir Unity. |
| `visual-audio` | Coherencia visual/sonora y procedencia de recursos. | Si arte o audio son parte importante de la experiencia. |
| `playtest-reviewer` | Prueba desde la perspectiva de alguien nuevo. | En cuanto exista un recorrido jugable. |
| `delivery-writer` | Instrucciones, créditos, licencia y README. | Al preparar la reconstrucción y entrega. |
| `live-demo-coach` | Demostración centrada en el juego funcionando. | Cuando se conozca el formato de presentación. |
| `integrator` | Integrar cambios y conservar una versión ejecutable. | Durante todo el desarrollo en equipo. |

No se debe asignar una especialidad de motor antes de elegirlo. Si no hay agentes reales disponibles, una persona puede tomar la función sin presentarla como un agente.

### Perfiles todavía no formalizados

El editor narrativo, el analista de balance y el auditor de recursos se conversaron o probaron como enfoques puntuales. **Todavía no existen como skills o agentes independientes en este repositorio.** Si un futuro proyecto demuestra que los necesita, se pueden convertir en herramientas reutilizables. Los documentos de prueba actuales pertenecen a Maite.

## B. Caso de estudio: Maite: Rumbo al Salar

Maite se usó para probar skills, agentes como enfoques de trabajo y creación de un juego HTML. Es un caso opcional de referencia; no es seguro que continúe. Sus personajes, historia, reglas, arte, cantera y puzles no se trasladan automáticamente a otro juego.

El índice y las pruebas están en [`case-studies/maite-rumbo-al-salar/`](../case-studies/maite-rumbo-al-salar/README.md):

| Prueba de Maite | Skill o enfoque | Resultado observado | Límite |
| --- | --- | --- | --- |
| Cantera chilena en tres cámaras | `cozy-pixelart-design`, `dimensional-pixel-scenes`, `spatial-map-camera-flow` | Comparación top-down, 2.5D y transición mapa/interior. | Conceptos visuales; no prueban colisiones ni navegación real. La referencia a El Way es geográfica, no una reproducción de la operación. |
| Retratos y caminata | `character-identity-portraits`, `sprite-animation-pipeline` | Expresiones coherentes y borrador de ciclos ajustables. | La caminata conserva un halo rojo y no es un asset de producción. |
| Hoja de personaje | `character-reference-sheet-maintainer` | Reunió personalidad, apariencia, estados de assets y procedencia; detectó una discrepancia del largo del cabello. | Hoja de evaluación de Maite; no fija el canon si se retoma. |
| Edición narrativa | Perfil editorial | Redujo carga de lectura conservando decisiones y consecuencias. | Propuesta; no se integró al juego. |
| Balance de decisiones | Perfil analítico | Comparó aritméticamente secuencias de 20 decisiones. | No equivale a playtest integral ni incluye todo efecto de partida. |
| Puzle de turnos | `puzzle-design-reviewer` | Confirmó una solución única y encontró feedback incorrecto para algunas respuestas erróneas. | Revisión estática; falta probar el flujo interactivo en navegador. |

