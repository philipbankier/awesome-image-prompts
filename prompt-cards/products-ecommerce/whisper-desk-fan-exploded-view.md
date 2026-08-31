# Whisper Desk Fan Exploded View

## Use this when

Use this card when you need to turn an authorized design sketch into a fictional compact fan assembly view. Use a Recipe when exact geometry preservation, claims review, repair, repeated comparison, or evidence matters.

## Required inputs

- A fictional or authorized product brief with exact form, components, and intended channel.
- Material, finish, color, package-content, and accessory manifest.
- Approved copy or explicit `none`, plus camera view, lighting, background, and output size.
- One attached layout or product sketch and confirmation that it is authorized for this use.
- A sketch-flexibility note naming protected zones, landmarks, and details open to interpretation.

## Prompt

```text
COMMISSION
Create one 3:2 exploded product view to turn an authorized design sketch into a fictional compact fan assembly view. Use this independently authored concept: guard, blades, hub, motor shell, stem, and base align on one assembly axis.

SKETCH INPUT
Use the attached authorized {LAYOUT_SKETCH} only as a structural guide. Honor {SKETCH_FLEXIBILITY}, including protected zones, hierarchy, and landmarks. Do not trace distinctive artwork, reproduce sketch text, add a signature, or invent functional details.

PRODUCT
Use {PRODUCT_BRIEF} and build only the declared form, components, materials, finishes, and approved accessories in {MATERIAL_MANIFEST}. Do not invent a feature, certification, ingredient, performance result, compatibility statement, or package content.

PRESENTATION
Use {CAMERA_VIEW}, {LIGHTING}, and {BACKGROUND}. Arrange the product as follows: exploded sequence runs left to right with no invented components. Render only {APPROVED_COPY}; if it says `none`, render no text or logo.

CONSTRAINTS
Use a fictional product or an authorized product brief. Keep declared geometry, part count, scale, color, and materials consistent. No real brand, copied package, unsupported claim, celebrity endorsement, signature, watermark, or unapproved accessory.

OUTPUT INTENT
Return one clean exploded product view at {OUTPUT_SIZE} in 3:2, with the product fully visible and no unrelated props.
```

## Variables

- `{PRODUCT_BRIEF}`: fictional or authorized product identity, geometry, purpose, and channel
- `{MATERIAL_MANIFEST}`: exact components, counts, materials, finishes, colors, and allowed accessories
- `{CAMERA_VIEW}`: camera height, angle, lens character, crop, and scale relationship
- `{LIGHTING}`: declared studio or environmental lighting and shadow behavior
- `{BACKGROUND}`: surface, set, or plain field allowed behind the product
- `{APPROVED_COPY}`: complete allowed product and campaign text, or `none`
- `{OUTPUT_SIZE}`: final pixel dimensions
- `{LAYOUT_SKETCH}`: attached authorized sketch used only as a structural guide
- `{SKETCH_FLEXIBILITY}`: protected landmarks and the degree of allowed refinement

## Negative constraints

- No real brand, copied packaging, trademark, celebrity likeness, signature, watermark, or unlicensed design feature.
- No invented component, material, accessory, package content, label copy, certification, performance result, or product claim.
- No duplicated product, warped geometry, unreadable approved copy, unrelated prop, decorative pseudo-text, or mock marketplace UI.

## Quick check

Count the declared products and components, compare form and materials with the manifest, and check the intended arrangement: exploded sequence runs left to right with no invented components. This does not establish preservation reliability or product readiness.

## Rendered Sample

![Rendered sample for Whisper Desk Fan Exploded View](samples/whisper-desk-fan-exploded-view/whisper-desk-fan-exploded-view.webp)

- Sample status: Rendered Sample.
- Generation surface: built-in image generation tool
- Generated at: `2026-08-30T23:34:32Z`
- Model: `not_exposed`
- Model version: `not_exposed`
- Seed: `not_exposed`
- Request parameters: `not_exposed`
- Request ID: `not_exposed`
- Exact prompt: [whisper-desk-fan-exploded-view.prompt.txt](samples/whisper-desk-fan-exploded-view/whisper-desk-fan-exploded-view.prompt.txt)
- Output dimensions: `1536 x 1024`
- Output SHA-256: `8390b9afd1ea13b7249229e0ce89865caee9be8df609b1a10b014f02caf20d34`
- Profile ID: `null`
- Promotion evidence: `false`
- Human inspection: Passed: exactly six distinct assemblies, including five blades, a detached stem, and a detached base, are countable and aligned in a plausible sequence.
- Known misses: The exploded view explains visible assembly relationships only and omits internal engineering by design.
- Rights and provenance: The concept, exact prompt, accepted image, and public WebP derivative are project-authored. Lossless masters and rejected attempts are retained privately with checksums. The public derivative may be reused under this repository's license; this record is illustrative evidence only.
- Supporting inputs:
  - [input-01-layout-sketch.webp](samples/whisper-desk-fan-exploded-view/input-01-layout-sketch.webp): project-authored fictional layout sketch input
## Rights and provenance

This Prompt Card is independently authored with `original` source posture. Use only fictional or properly authorized product geometry, packaging, copy, names, and images. The sketch must be owned or explicitly authorized and used only within the declared flexibility boundary.
