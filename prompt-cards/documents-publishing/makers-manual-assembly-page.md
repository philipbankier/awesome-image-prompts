# Maker's Manual Assembly Page

## Use this when

Use this card for one illustrated assembly-instruction page based on an approved fictional object, exact parts manifest, and verified step sequence. Use a Recipe for real safety-critical assembly, engineering sign-off, or production evidence.

## Required inputs

- Approved fictional object and exact parts manifest with labels and quantities.
- Verified ordered steps, tool list, warnings, and finished-state view.
- Illustration style, grid, page size, exact text, and aspect ratio.

## Prompt

```text
SCENE
Create one flat instructional page on {PAGE_FIELD}, with no workshop environment, hands, packaging, or manual mockup.

SUBJECT
Explain assembly of {OBJECT_NAME_EXACT} using exactly {PARTS_MANIFEST}, {TOOLS_MANIFEST}, and the ordered sequence {STEP_MANIFEST}.

DETAILS
Arrange {STEP_PANELS}, {PART_LABELS}, {CONNECTOR_ARROWS}, {WARNING_TEXT}, and {FINISHED_STATE} within {INSTRUCTION_GRID}. Use {VISUAL_SYSTEM} and render only {EXACT_TEXT_MANIFEST}; keep each depicted part consistent from one step to the next.

CONSTRAINTS
Do not change part count, orientation, connection, tool, sequence, or warning. No impossible fastener, floating part, skipped step, ambiguous arrow, real product, copied manual style, invented safety claim, pseudo-text, logo, signature, watermark, or unapproved copy.

OUTPUT INTENT
Return one complete 4:5 assembly page at {OUTPUT_SIZE}, with a left-to-right or top-to-bottom sequence that can be audited against the approved instructions.
```

## Variables

- `{PAGE_FIELD}`: plain paper color and texture.
- `{OBJECT_NAME_EXACT}`: exact fictional object name.
- `{PARTS_MANIFEST}`: labels, quantities, and stable visual descriptions.
- `{TOOLS_MANIFEST}`: approved required tools or `none`.
- `{STEP_MANIFEST}`: exact ordered assembly steps.
- `{STEP_PANELS}`: number and placement of panels.
- `{PART_LABELS}`: exact callout labels.
- `{CONNECTOR_ARROWS}`: approved motion and attachment directions.
- `{WARNING_TEXT}`: exact approved warnings or `none`.
- `{FINISHED_STATE}`: final orientation and required visible details.
- `{INSTRUCTION_GRID}`: panel, legend, and margin layout.
- `{VISUAL_SYSTEM}`: project-owned line, fill, number, and highlight rules.
- `{EXACT_TEXT_MANIFEST}`: complete allowed text list.
- `{OUTPUT_SIZE}`: final pixel dimensions.

## Negative constraints

- No omitted, duplicated, substituted, or physically impossible part or connection.
- No reordered step, conflicting arrow, unsupported safety statement, or hidden fastener.
- No real product identity, corporate manual style, pseudo-text, hand, tool not listed, signature, or watermark.

## Quick check

Count every part, walk through the steps in order, trace each arrow, and confirm the finished state can result from the depicted sequence without an undeclared tool or hidden action.

## Placeholder Preview

Sample status: Placeholder Preview. No recorded generation run.

Expected result: a clean instructional page with stable part drawings, exact numbered steps, unambiguous arrows, and a verifiable finished object.

## Rights and provenance

Use only an approved fictional object, verified assembly sequence, and project-owned illustration direction. This Prompt Card is independently authored, has source posture `original`, and includes no third-party prompt, manual, product design, logo, or image.
