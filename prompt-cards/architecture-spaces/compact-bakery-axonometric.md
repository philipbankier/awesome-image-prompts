# Compact Bakery Axonometric

## Use this when

Use this card for a cutaway axonometric concept that communicates the layout of a small fictional or authorized bakery. Use a Recipe for code, equipment clearance, food-safety, or construction decisions.

## Required inputs

- Approximate footprint, ceiling height, entries, and service orientation.
- An optional authorized plan sketch, or `none` when the text geometry is complete.
- Exact room zones, equipment, customer capacity, and circulation sequence.
- Material palette, cutaway direction, background, and aspect ratio.

## Prompt

```text
REFERENCE INPUT
Use {OPTIONAL_PLAN_SKETCH} only as an authorized layout guide. If it is `none`, follow the declared footprint and zone manifest without inventing adjacent rooms.

SCENE
Create a clean architectural axonometric on {BACKGROUND}, using {LIGHTING} and a cutaway from {CUTAWAY_DIRECTION}.

SUBJECT
Show one compact {BAKERY_NAME} bakery within a {FOOTPRINT} shell.

DETAILS
Arrange {ZONE_MANIFEST}, exactly {EQUIPMENT_MANIFEST}, {CUSTOMER_FURNITURE}, and a clear route from {ENTRY_SEQUENCE}. Use {MATERIAL_PALETTE} to distinguish public and work areas without labels.

CONSTRAINTS
Keep walls, floors, doors, counters, equipment, and people-scale proportions coherent. No impossible circulation, sealed work zone, duplicated equipment, floating fixtures, roof, neighboring units, brand logos, annotations, dimensions, watermarks, or unapproved text.

OUTPUT INTENT
Return one legible axonometric at {ASPECT_RATIO}, showing the full plan relationship and operational sequence without claiming construction or regulatory validity.
```

## Variables

- `{OPTIONAL_PLAN_SKETCH}`: attached authorized layout sketch, or `none`.
- `{BACKGROUND}`: plain presentation field.
- `{LIGHTING}`: neutral light and shadow treatment.
- `{CUTAWAY_DIRECTION}`: walls removed to reveal the layout.
- `{BAKERY_NAME}`: fictional or authorized project name.
- `{FOOTPRINT}`: approximate length, width, and height.
- `{ZONE_MANIFEST}`: exact public, service, production, storage, and support zones.
- `{EQUIPMENT_MANIFEST}`: exact equipment pieces and count.
- `{CUSTOMER_FURNITURE}`: tables, chairs, display, and queue elements.
- `{ENTRY_SEQUENCE}`: customer and staff circulation paths.
- `{MATERIAL_PALETTE}`: limited floor, wall, counter, and joinery materials.
- `{ASPECT_RATIO}`: final width-to-height ratio.

## Negative constraints

- No code-compliance, food-safety, capacity, or buildability claim.
- No missing entrance, trapped room, intersecting equipment, or unusable aisle.
- No exploded diagram, floor-plan labels, dimensions, arrows, or decorative text.

## Quick check

Trace customer and staff routes separately, count all equipment and furniture, and confirm every requested zone is visible and spatially connected.

## Placeholder Preview

Sample status: Placeholder Preview. No recorded generation run.

Expected result: a compact, easy-to-read cutaway that communicates bakery zoning and flow without pretending to be a technical drawing.

## Rights and provenance

Use fictional or authorized plans, sketches, and independently specified interiors. This Prompt Card is independently authored, has source posture `original`, and bundles no third-party prompt or image.
