# Travel Flask Colorway Grid

## Use this when

Use this card to show one fictional or authorized travel-flask design across a small, declared set of colorways. Use a Recipe when geometry preservation or exact comparative evaluation is required.

## Required inputs

- One authorized reference image showing the flask geometry, lid, and material.
- The approved colorway manifest.
- Grid dimensions and ordering.
- Background, camera view, lighting, and target aspect ratio.

## Prompt

```text
REFERENCE INPUT
Use the attached authorized {REFERENCE_IMAGE} as the sole source for product geometry, lid construction, material, and camera-facing details.

SCENE
Create a controlled studio comparison grid on {BACKGROUND}, lit uniformly with {LIGHTING}.

SUBJECT
Show the same {FLASK_NAME} travel flask exactly {COUNT} times in a {GRID_LAYOUT} grid, one instance for each colorway in {COLORWAY_MANIFEST}.

DETAILS
Every flask must share {FLASK_GEOMETRY}, {LID_DESCRIPTION}, {MATERIAL_FINISH}, the same scale, and the same {CAMERA_VIEW}. Arrange colorways in the declared order.

CONSTRAINTS
Change color only. Do not alter proportions, lid geometry, highlights, camera angle, crop, or spacing between variants. No extra products, missing variants, labels, swatches, logos, watermarks, captions, or unapproved text.

OUTPUT INTENT
Return one precise colorway grid at {ASPECT_RATIO}, with consistent product geometry, equal cells, and all variants fully visible.
```

## Variables

- `{REFERENCE_IMAGE}`: attached authorized flask image to preserve across variants.
- `{BACKGROUND}`: neutral comparison background.
- `{LIGHTING}`: fixed studio-light description.
- `{FLASK_NAME}`: fictional or authorized product name.
- `{COUNT}`: exact number of variants.
- `{GRID_LAYOUT}`: rows by columns.
- `{COLORWAY_MANIFEST}`: ordered color names and finishes.
- `{FLASK_GEOMETRY}`: body shape, proportions, and base.
- `{LID_DESCRIPTION}`: closure form and material.
- `{MATERIAL_FINISH}`: body material and surface response.
- `{CAMERA_VIEW}`: one view shared by all cells.
- `{ASPECT_RATIO}`: final width-to-height ratio.

## Negative constraints

- No geometry drift, variant-specific accessories, or inconsistent camera views.
- No omitted, duplicated, or reordered colorway.
- No comparison labels, text, branding, or UI framing unless explicitly approved.

## Quick check

Count the flasks, compare silhouettes and lids cell by cell, and verify that only the approved color and finish change.

## Placeholder Preview

Sample status: Placeholder Preview. No recorded generation run.

Expected result: a clean grid of truly matching flasks whose color changes are easy to compare without layout noise.

## Rights and provenance

Use only fictional or authorized product geometry, finishes, names, and reference assets. This Prompt Card is independently authored, has source posture `original`, and bundles no third-party prompt or image.
