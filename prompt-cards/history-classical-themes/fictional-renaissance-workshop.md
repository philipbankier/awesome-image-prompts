# Fictional Renaissance Workshop

## Use this when

Use this card for a fictional 15th-century workshop interior constrained by an approved regional fact pack. It is not for pastiching a named master or reconstructing a documented studio. Use a Recipe when fact mapping, anachronism review, or repair needs evidence.

## Required inputs

Provide the region and date range, craft activity, architecture, work surfaces, tool inventory, clothing, materials, workers, camera, light, palette, aspect ratio, and excluded anachronisms.

## Prompt

```text
SCENE: Set a fictional {DATE_RANGE} workshop in {REGION}, viewed from {CAMERA_POSITION} under {LIGHT_DESCRIPTION}.
SUBJECT: Show exactly {WORKER_COUNT} fictional craftspeople performing {CRAFT_ACTIVITY} at {WORK_SURFACES}.
DETAILS: Include only {TOOL_INVENTORY}, {MATERIAL_INVENTORY}, {ARCHITECTURAL_FEATURES}, and {CLOTHING_MANIFEST}; use {PALETTE}, plausible scale, soot, wear, and work-in-progress evidence consistent with the approved fact pack.
CONSTRAINTS: Do not add later technologies, electric light, synthetic materials, modern text, copied paintings, named artists, famous faces, logos, signatures, or watermarks. Also avoid {MUST_AVOID}.
OUTPUT INTENT: Return one finished {ASPECT_RATIO} fictional historical interior whose visible details can be checked against the supplied inventory.
```

## Variables

- `{DATE_RANGE}` and `{REGION}`: approved scope.
- `{CAMERA_POSITION}` and `{LIGHT_DESCRIPTION}`: viewpoint and illumination.
- `{WORKER_COUNT}` and `{CRAFT_ACTIVITY}`: exact fictional people and task.
- `{WORK_SURFACES}`, `{TOOL_INVENTORY}`, and `{MATERIAL_INVENTORY}`: production content.
- `{ARCHITECTURAL_FEATURES}` and `{CLOTHING_MANIFEST}`: period boundaries.
- `{PALETTE}` and `{ASPECT_RATIO}`: visual and delivery rules.
- `{MUST_AVOID}`: excluded anachronisms and other prohibited motifs.

## Negative constraints

No modern tools, later machinery, electric light, synthetic materials, named-master imitation, famous faces, copied paintings, logos, signatures, or watermarks.

## Quick check

Map every tool, material, garment, and architectural feature to the fact pack; count workers; reject any later technology or copied artwork.

## Placeholder Preview

Sample status: Placeholder Preview. No recorded generation run.

The intended preview is a plausible but explicitly fictional workshop scene bounded by one region and date range.

## Rights and provenance

This card is independently authored with `original` source posture. It relies on authorized factual research, not a named artist's works, documented studio, or upstream prompt.
