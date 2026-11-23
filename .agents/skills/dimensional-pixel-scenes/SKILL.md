---
name: dimensional-pixel-scenes
description: Plan or review hybrid pixel-character scenes with perspective-rich 2.5D or 3D-like environments, including camera composition, depth, lighting, and sprite integration. Use when a project combines pixel sprites with dimensional scenery.
---

# Dimensional scenes with pixel characters

Help create a coherent hybrid in which pixel-art characters inhabit a deeper environment. Use high-level visual qualities as references; do not recreate a named game's characters, locations, interface, or signature compositions.

## Workflow

1. Inspect the existing project and determine whether the environment is a painted background, layered planes, canvas projection, or actual 3D geometry. Do not assume an engine or propose a migration without a concrete need.
2. Define the camera for the scene: perspective or orthographic, viewing height, direction, and framing. Keep a character's apparent scale and ground contact consistent as the camera changes.
3. Establish depth with foreground, playable ground, midground structures, and distant background. Place interaction points on the playable ground plane, not by visual guess alone.
4. Integrate sprites with stable foot anchors, scale, lighting direction, and occlusion order. Specify when a sprite passes behind or in front of structures.
5. Keep pixel edges crisp at the target resolution. If the environment is detailed or painterly, state that it is a deliberate hybrid and control contrast so sprites remain readable.
6. Review a representative frame at gameplay size and check perspective, sprite scale, silhouettes, occlusion, and light coherence.

## Blockouts and transitions

- Use a simple 3D blockout when it clarifies camera, spatial depth, sight lines, or doorway placement. A blockout is a planning aid and does not by itself require replacing a 2D implementation.
- When a location changes the camera, describe the before and after camera poses and preserve a visual landmark or doorway through the transition.
- Coordinate with a map-flow workflow for walkability, room connections, and environment continuity; do not duplicate its collision validation here.

## Constraints

- Preserve the chosen project's rendering pipeline and art direction.
- Use named titles only to understand broad traits such as pixel sprites against dimensional scenery; produce original designs.
- Track external assets and generated assets according to the project's attribution and licensing requirements.
