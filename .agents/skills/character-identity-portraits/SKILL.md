---
name: character-identity-portraits
description: Design and review consistent original character identities across portraits and expression atlases. Use when creating, editing, or checking game dialogue portraits and character reference sheets.
---

# Character identity and portraits

Keep each character recognizable across portraits, expressions, outfits, and existing game assets. Treat the project's established artwork and written character descriptions as the source of truth; do not assume a new visual identity is wanted.

## Workflow

1. Inspect the existing portrait atlas, character sprites, narrative descriptions, and any established visual notes. Record identity cues that must remain stable: face shape, skin tone, hair, age presentation, accessories, clothing, palette, and silhouette.
2. Define the portrait brief before generating or editing: intended use, framing, expression range, background treatment, and required export format. Preserve character-specific cues while allowing expression to change.
3. Choose the design resolution, atlas layout, cell dimensions, and in-game display size for this task. Keep them configurable. The current project's 4 × 4 portrait atlas is a legacy layout reference, not a required output size.
4. Create expression variants that remain readable at dialogue size. Keep camera crop, head scale, lighting direction, and line/pixel density consistent unless the user asks for a deliberate variation.
5. Compare each result against the character's reference cues and neighboring portraits. Check for identity drift, inconsistent age or features, clipped hair/accessories, low-contrast expressions, and mismatched palette.
6. Deliver a clear mapping from character and expression to atlas cell or asset filename. Record external sources, authors, licenses, and modifications when applicable.

## Resolution and scaling

- Separate design resolution, exported asset resolution, atlas cell size, and displayed UI size; do not conflate them.
- Support higher resolutions by increasing the editable source and export dimensions while preserving framing and proportions. Do not stretch an existing low-resolution portrait if the user needs added detail; re-render or redraw at the chosen source resolution.
- For pixel-art portraits, scale by integer multiples with nearest-neighbor filtering when that preserves the selected pixel grid. If the project adopts a higher native pixel density, update the grid consistently instead of mixing scales within an atlas.
- Keep cell dimensions and atlas coordinates in metadata or a short manifest when the project consumes them programmatically.

## Constraints

- Create original characters. Use named works only as broad references, never as a request to copy a protected character or distinctive portrait design.
- Preserve culturally specific details from the approved character brief; do not add or remove them casually for visual variety.
- Do not claim a portrait matches an in-game character without comparing the actual sprite or established reference.
