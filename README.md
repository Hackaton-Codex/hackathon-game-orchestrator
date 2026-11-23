# Agente base para la hackathon

Skill neutral para ayudar al equipo a planificar, coordinar e integrar un juego durante la hackathon. Se adapta al reto, género y tecnología elegidos por el equipo; no incluye un juego ni un motor preseleccionado.

Evento: [Build Games with Codex](https://hackathon.codexparatodos.com/). Revisa el sitio oficial para confirmar cambios en reglas y entrega.

## Contenido

- `AGENTS.md`: instrucciones generales del orquestador.
- `.agents/skills/hackathon-game-orchestrator/SKILL.md`: flujo reutilizable para analizar el proyecto, acordar tecnología, planificar una ruta jugable y preparar la entrega.
- `.agents/skills/hackathon-game-orchestrator/agents/openai.yaml`: nombre y prompt inicial del skill.
- `README-HACKATHON.md`: plantilla de README para el juego del equipo.

## Uso

Abre el repositorio del juego en Codex y activa o menciona `hackathon-game-orchestrator`. Antes de implementar, comparte el reto, las tecnologías que conoce el equipo y las reglas sobre trabajo previo. El agente ayudará a documentar los acuerdos en el README o `PLAN.md` del juego.

El skill está preparado para web, Godot, Unity u otra tecnología que el equipo elija. No inicializa un juego ni instala herramientas antes de confirmar esos acuerdos.

## Biblioteca de skills y evaluaciones

Este repositorio reúne el orquestador neutral y skills opcionales que se pueden elegir según el reto y la tecnología. **Maite: Rumbo al Salar** aparece solo como caso de prueba: no fija el juego, estilo ni stack de la hackathon.

- [Compendio de skills, perfiles y resultados (Markdown)](COMPENDIO_SKILLS_AGENTES.md)
- [Compendio en PDF](output/pdf/compendio-skills-y-agentes.pdf)
- Skills incluidas: [diseño pixel art](.agents/skills/cozy-pixelart-design/SKILL.md), [escenas 2.5D](.agents/skills/dimensional-pixel-scenes/SKILL.md), [mapas y cámara](.agents/skills/spatial-map-camera-flow/SKILL.md), [retratos](.agents/skills/character-identity-portraits/SKILL.md), [animación de sprites](.agents/skills/sprite-animation-pipeline/SKILL.md), [ficha de personaje](.agents/skills/character-reference-sheet-maintainer/SKILL.md), [revisión de puzles](.agents/skills/puzzle-design-reviewer/SKILL.md), [prototipado RPG web](.agents/skills/rpg-web-prototyping/SKILL.md) y [orquestación de hackathon](.agents/skills/hackathon-game-orchestrator/SKILL.md).
- Evidencias: [cantera](skill-evaluations/cantera-chile/README.md), [arte de personaje](skill-evaluations/character-art/README.md), [narrativa y balance](skill-evaluations/narrative-balance/README.md) y [puzles](skill-evaluations/puzzles/referencias-mecanicas.md).

Las imágenes de evaluación son previsualizaciones JPG comprimidas para revisión en GitHub. Los PNG originales del caso de prueba y el código del juego no forman parte de esta biblioteca.
