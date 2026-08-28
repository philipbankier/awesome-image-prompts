# Garden Tool Sticker Sheet

## Use this when

Use this card for one tidy sheet of fictional garden-tool stickers with a closed object list. Use a Recipe when cut-line tolerances, exact label text, or production export matters.

## Required inputs

- Exact tool and accessory manifest with quantities.
- Illustration treatment, outline, border, palette, background, and spacing.
- Sheet dimensions, aspect ratio, and whether text is allowed, including exact approved strings and placements when applicable.

## Prompt

```text
SCENE
Create a flat {SHEET_DIMENSIONS} sticker sheet on {SHEET_BACKGROUND}, viewed perfectly straight-on with no perspective or surface mockup.

SUBJECT
Include exactly {STICKER_MANIFEST}, each as one separate garden-themed sticker.

DETAILS
Render every object in {ILLUSTRATION_STYLE} using {PALETTE}, {OUTLINE_STYLE}, and a consistent {BORDER_DESCRIPTION}. Arrange the stickers with {SPACING_RULE} and clear separation. Follow {TEXT_POLICY}: render no text when it is `none`; otherwise render only its exact approved strings and placements.

CONSTRAINTS
No overlapping stickers, clipped border, duplicate tool, missing item, floating fragment, realistic brand mark, drop-shadow inconsistency, packaging, hands, logos, watermarks, or unapproved text.

OUTPUT INTENT
Return one complete sticker-sheet image at {ASPECT_RATIO}, with all sticker borders fully inside the frame and ready for later manual production setup.
```

## Variables

- `{SHEET_BACKGROUND}`: flat sheet color.
- `{SHEET_DIMENSIONS}`: intended width and height with units.
- `{STICKER_MANIFEST}`: exact objects and quantities.
- `{ILLUSTRATION_STYLE}`: independently described visual treatment.
- `{PALETTE}`: closed color list.
- `{OUTLINE_STYLE}`: line color, weight, and consistency.
- `{BORDER_DESCRIPTION}`: white or colored sticker margin and width.
- `{SPACING_RULE}`: minimum separation and layout rhythm.
- `{TEXT_POLICY}`: `none`, or the exact approved strings and placements.
- `{ASPECT_RATIO}`: final width-to-height ratio.

## Negative constraints

- No real tool brand, seed brand, mascot, or trademarked character.
- No cut path, bleed, or print-readiness claim generated inside the image.
- No merged silhouettes, missing handles, doubled blades, or inconsistent borders.

## Quick check

Count each sticker, verify every silhouette and border closes cleanly, and confirm no two pieces touch or leave the canvas.

## Placeholder Preview

Sample status: Placeholder Preview. No recorded generation run.

Expected result: a clear, playful sheet of distinct garden objects with consistent borders and generous cutting space.

## Rights and provenance

Use generic or independently designed garden objects and no real branding. This Prompt Card is independently authored, has source posture `original`, and includes no third-party prompt or image.
