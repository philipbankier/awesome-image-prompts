# Tabletop Dungeon Token Sheet

## Use this when

Use this card for a flat, illustration-ready sheet of top-down encounter tokens with scale classes and cut margins. Use the board-game token Card for a component-style set organized around game roles, or a Recipe when exact production dimensions and evidence are required.

## Required inputs

- A fictional, public-domain, or authorized project brief and intended use.
- A closed content manifest with exact counts, order, and approved text where applicable.
- Visual direction, palette, composition, target aspect ratio, and exclusions.

## Prompt

```text
SCENE
Create one tabletop encounter token sheet for {PROJECT_BRIEF}.

SUBJECT
Create top-down original tabletop tokens for the declared fictional encounter, with consistent bases, readable silhouettes, scale classes, and cut margins.

DETAILS
Include exactly {CONTENT_MANIFEST}. Follow {VISUAL_DIRECTION}, {COLOR_PALETTE}, and {COMPOSITION}; keep scale, orientation, spacing, and visual hierarchy internally consistent.

CONSTRAINTS
Do not add undeclared subjects, panels, symbols, copy, logos, signatures, or watermarks. Avoid {MUST_AVOID}. Do not imply factual verification, endorsement, or evidence that is not supplied.

OUTPUT INTENT
Return one finished tabletop encounter token sheet at {ASPECT_RATIO}, complete inside the frame and ready for the stated project review.
```

## Variables

- `{PROJECT_BRIEF}`: purpose, audience, and fictional or authorized subject matter
- `{CONTENT_MANIFEST}`: closed list of required subjects, props, panels, labels, or variants
- `{VISUAL_DIRECTION}`: project-owned visual language, material treatment, lighting, and mood
- `{COLOR_PALETTE}`: approved color system with any contrast requirements
- `{COMPOSITION}`: camera, hierarchy, spacing, and focal-order instructions
- `{ASPECT_RATIO}`: final width-to-height ratio
- `{MUST_AVOID}`: task-specific exclusions and failure modes

## Negative constraints

- No undeclared people, objects, panels, labels, logos, signatures, or watermarks.
- No unauthorized living-person likeness, protected character, real brand identity, or unsupported factual claim.
- No broken anatomy, duplicated subjects, contradictory lighting, illegible required text, or cropped required content.

## Quick check

Count the tokens, compare base sizes to scale classes, and check that every silhouette remains distinct when reduced.

## Placeholder Preview

Sample status: Placeholder Preview. No recorded generation run.

Expected result: tabletop encounter token sheet with the declared content, hierarchy, and visual direction clearly visible.

## Rights and provenance

This Prompt Card is independently authored with `original` source posture. Use only fictional, public-domain, or properly authorized subjects, references, names, data, and brand materials. It bundles no third-party prompt or image.
