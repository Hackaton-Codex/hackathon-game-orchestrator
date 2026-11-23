---
name: spatial-map-camera-flow
description: Design and validate traversable game maps, connected interior zones, camera changes, and landscape continuity. Use when a player explores corridors or enters locations whose viewpoint and visible surroundings should change coherently.
---

# Spatial map and camera flow

Make the visible world, movement rules, interaction points, and camera transitions describe the same connected place. Adapt the representation to the project's engine and files rather than requiring a particular map format.

## Workflow

1. Inspect the map, collision data, room assets, entrances, and camera behavior already in the project. Identify gaps before changing the representation.
2. Sketch the world as connected exterior segments and interior zones. Mark entrances, exits, player arrival points, objectives, landmarks, and sight lines through windows or openings.
3. Define a camera pose or framing for each traversal segment and interior. For every transition, record the trigger, outgoing direction, destination point, arrival orientation, and camera change.
4. Mark walkable and blocked regions separately from decorative art. Check that routes connect spawn, required interactions, exits, and objectives; ensure each required point is reachable and no necessary route is blocked.
5. Preserve landscape continuity across thresholds. An interior opening should show the part and direction of the exterior that could be seen from that room's position and orientation, with an appropriate change in scale and viewpoint. Do not reuse a full-map view as a window view unless the camera geometry supports it.
6. Check occlusion and depth order so foreground walls, door frames, characters, and background scenery appear in a consistent order.
7. Validate the proposed routes and transitions with a short playthrough or a map overlay. Report each issue with its location, expected behavior, observed behavior, and a reproducible path.

## Practical prototype path

- For a 2D project, use layered perspective backgrounds, viewport masks for openings, and explicit camera presets before considering a full 3D conversion.
- Use a simple 3D blockout when it helps verify corridor depth, room orientation, door alignment, or window sight lines. Keep it as a design aid unless the user chooses 3D implementation.
- Start with one exterior route, one entrance, and one interior. Confirm that entering and leaving preserves orientation and spatial understanding before scaling the scheme to more locations.

## Constraints

- Never infer walkability from visual appearance alone; compare it with the actual collision or navigation data.
- Keep visual composition and movement/collision data linked but separately inspectable.
- Do not alter existing maps or saved gameplay state just to demonstrate a proposed layout.
- Preserve the project's current technology unless the user asks for a change or a concrete limitation requires one.
