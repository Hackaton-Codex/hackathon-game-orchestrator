---
name: sprite-animation-pipeline
description: Create, adapt, and review game-character sprite sheets and movement cycles with configurable resolution, directions, frame counts, anchors, and export settings.
---

# Sprite animation pipeline

Turn an approved character design into usable, consistent game sprites. Adapt the sheet contract to the project's renderer and camera; do not impose a fixed engine, cell size, direction count, or frame count.

## Workflow

1. Inspect the character reference, active sprite sheet, game camera, movement code, and animation loader. Identify the expected directions, cell layout, transparency, pivot/foot anchor, and timing behavior before editing.
2. Agree on configurable asset parameters: source resolution, export resolution, cell width and height, rows and columns, directions, frames per animation, display size, and file format. Treat the current 144 × 272 cells and 4-frame walk sheet as project-specific examples, not defaults for every task.
3. Preserve identity across views and poses: same proportions, outfit, equipment, color placement, and silhouette. Match apparent height across directions and keep the feet aligned to a stable baseline or declared pivot.
4. For a walk cycle, define readable key poses and spacing for each required direction. Ensure weight shifts between legs, arms counter-swing, torso movement is subtle, and equipment or hair follows movement without changing shape. Add idle, start/stop, or other states only when the game uses them.
5. Keep frame order and timing explicit. Set a loop that returns smoothly to its first pose; synchronize playback speed with character movement so sliding feet and exaggerated motion are avoided.
6. Export with clean alpha transparency, consistent cell bounds, padding as required by the renderer, and no stray pixels or background fringe. For pixel art, preserve the chosen pixel grid and use integer nearest-neighbor scaling where appropriate.
7. Preview the full sheet, each direction, the loop, and the character at actual in-game size against both light and dark backgrounds. Check foot anchoring, cut-off limbs, silhouette, frame rhythm, transparency halos, and consistency with the portrait/reference.
8. Provide or update a sheet manifest describing dimensions, cell coordinates, directions, frame order, anchors, and timing so the game can consume a higher-resolution sheet without relying on hard-coded legacy dimensions.

## Resolution changes

- Higher resolution is supported by changing source size and cell dimensions while retaining relative character proportions, pivot placement, and frame layout.
- If enlarging existing pixel art, use integer nearest-neighbor scaling to preserve pixels. If the user wants more detail, redraw or regenerate at a higher native pixel density; do not blur or interpolate the old grid.
- Update loader metadata and cropping values whenever cell size or atlas layout changes. Never silently assume the current 144 × 272 grid.
- Keep displayed character size a separate runtime setting so larger source art can improve detail without unexpectedly enlarging the on-screen character.

## Constraints

- Do not invent extra directions or animation states unless needed by the camera, game code, or user request.
- Mirroring a side view is acceptable only when asymmetrical clothing, handedness, lighting, or props will not become incorrect.
- Preserve the approved character identity; report any unavoidable compromise between source art and runtime animation clearly.
