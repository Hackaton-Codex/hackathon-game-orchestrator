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
