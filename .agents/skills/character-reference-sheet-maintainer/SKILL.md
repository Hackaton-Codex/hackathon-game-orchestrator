---
name: character-reference-sheet-maintainer
description: Create and maintain a reviewable source-of-truth character sheet linking personality, visual identity, portraits, sprite sheets, animations, dimensions, and asset provenance. Use when documenting or reconciling a game's character references.
---

# Character reference sheet maintainer

Keep one clear, reviewable reference for each character that connects story facts to the actual portrait, sprite, and animation assets. Preserve the project's current documentation conventions and avoid replacing an existing source of truth without checking it first.

## Workflow

1. Inspect existing character notes, portraits, sprite sheets, animation assets, code references, and prior versions. Distinguish confirmed details from proposed or uncertain ones.
2. Create or update one character sheet using the template in `references/character-sheet-template.md`. Store it alongside the project's character documentation where maintainers can find it; if no convention exists, use `docs/characters/<character-slug>.md`.
3. Record narrative identity and personality, then describe stable visual cues that connect the face, portrait expressions, full-body sprite, directional views, and movement poses.
4. Link the actual asset files with relative paths and identify which version is active. Keep source assets intact; mark superseded versions instead of silently overwriting or deleting them.
5. Record technical metadata for every asset: native resolution, cell dimensions, atlas layout, directions, animation states, frame order, pivot/foot anchor, runtime display size, and scaling/filtering method when known. Leave unknown values marked as unknown; dimensions are configurable, never assumed from a prior sheet.
6. Record references and provenance, including source, author, license, modifications, and whether an image is an original, generated, or external reference. Keep generated drafts distinct from approved canon.
7. Review the sheet as a whole: name-to-asset mapping, identity consistency, readable expressions, outfit/accessory continuity, frame alignment, transparency issues, and unresolved discrepancies. Link a contact sheet or visual board when useful, but keep the written sheet as the index.
8. Summarize what changed, what was checked, and which questions remain open. Do not invent a definitive character trait to resolve contradictory references; document the conflict for review.

## Resolution and asset changes

- Keep design resolution, exported resolution, atlas cell size, and on-screen size as separate fields.
- Higher resolution is allowed. Preserve proportions, cell boundaries, pivots, and pixel density when scaling; redraw at a higher native resolution when more detail is needed.
- When an asset's layout changes, update its metadata and any known loader mapping together. Do not claim compatibility until the actual file and consumer have been checked.
- Use `character-identity-portraits` for portrait-specific generation or review and `sprite-animation-pipeline` for sprite/animation-specific work when those skills are available; this skill remains responsible for connecting their outcomes to the character's canonical sheet.

## Constraints

- Never treat an unreviewed generation as approved character canon.
- Do not make an asset look more consistent by altering the original source silently; create a new version and document the change.
- Do not embed large images as base64 in the sheet. Use relative links or compact previews.
