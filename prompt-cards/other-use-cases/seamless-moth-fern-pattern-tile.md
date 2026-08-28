# Seamless Moth and Fern Pattern Tile

## Use this when

Use this card for one square, repeat-ready decorative pattern tile made from fictional moths and fern forms. Use the linked [Recipe](../../recipes/seamless-moth-fern-pattern-tile/RECIPE.md) when seam inspection, repair, or evidence matters.

## Required inputs

- Moth species treatment, fern forms, motif count, and scale hierarchy.
- Palette, ground color, rendering style, repeat density, and tile size.
- Any excluded symbols, plants, insects, or text.

## Prompt

```text
SCENE
Create a flat pattern field on {GROUND_COLOR} with no perspective, lighting vignette, border, or presentation surface.

SUBJECT
Build one seamless square repeat from {MOTH_MOTIFS} and {FERN_MOTIFS}, arranged in {LAYOUT_LOGIC}.

DETAILS
Use {PALETTE}, {RENDERING_STYLE}, {MOTIF_SCALE}, and {DENSITY}. Continue every edge-crossing motif precisely onto the opposite edge while keeping interior spacing balanced.

CONSTRAINTS
The left and right edges and the top and bottom edges must join without a visible seam. No cropped motif that lacks its opposite-edge continuation, central badge, frame, mockup, cast shadow, fabric folds, extra species, logos, watermarks, letters, or numbers. Also avoid {MUST_AVOID}.

OUTPUT INTENT
Return one flat {TILE_SIZE} square tile intended for direct edge-to-edge repetition, with no surrounding margin.
```

## Variables

- `{GROUND_COLOR}`: one flat background color.
- `{MOTH_MOTIFS}`: fictional or generic moth forms, counts, and poses.
- `{FERN_MOTIFS}`: frond types, counts, and curl directions.
- `{LAYOUT_LOGIC}`: half-drop, tossed, lattice, or declared repeat logic.
- `{PALETTE}`: closed color list.
- `{RENDERING_STYLE}`: independently described line, gouache, cut-paper, or vector treatment.
- `{MOTIF_SCALE}`: primary and secondary motif sizes.
- `{DENSITY}`: open, moderate, or dense spacing target.
- `{MUST_AVOID}`: excluded symbols, plants, insects, or text.
- `{TILE_SIZE}`: square pixel dimensions.

## Negative constraints

- No visible tile border, corner emphasis, center medallion, or wallpaper mockup.
- No realistic specimen labels, scientific text, signatures, or existing textile imitation.
- No tangencies, awkward motif collisions, incomplete opposite-edge continuation, or directional dead zone.

## Quick check

Repeat the tile in a 3 by 3 grid and inspect every boundary, corner, motif continuation, spacing rhythm, and unintended stripe.

## Placeholder Preview

Sample status: Placeholder Preview. No recorded generation run.

Expected result: one flat square tile whose moth and fern rhythm remains continuous and balanced when repeated in every direction.

## Rights and provenance

Use independently specified motifs and avoid copying an existing artist, textile, or specimen plate. This Prompt Card is independently authored, has source posture `original`, and includes no third-party prompt or image.
