# Trailtools Product Comparison Board

## Use this when

Use this card when you need to compare three fictional hand-tool variants using supplied factual specifications. Use a Recipe when exact geometry preservation, claims review, repair, repeated comparison, or evidence matters.

## Required inputs

- A fictional or authorized product brief with exact form, components, and intended channel.
- Material, finish, color, package-content, and accessory manifest.
- Approved copy or explicit `none`, plus camera view, lighting, background, and output size.

## Prompt

```text
COMMISSION
Create one 16:9 product comparison board to compare three fictional hand-tool variants using supplied factual specifications. Use this independently authored concept: three silhouettes share a baseline while differences are isolated in aligned rows.

PRODUCT
Use {PRODUCT_BRIEF} and build only the declared form, components, materials, finishes, and approved accessories in {MATERIAL_MANIFEST}. Do not invent a feature, certification, ingredient, performance result, compatibility statement, or package content.

PRESENTATION
Use {CAMERA_VIEW}, {LIGHTING}, and {BACKGROUND}. Arrange the product as follows: products across the top and a concise approved comparison matrix below. Render only {APPROVED_COPY}; if it says `none`, render no text or logo.

CONSTRAINTS
Use a fictional product or an authorized product brief. Keep declared geometry, part count, scale, color, and materials consistent. No real brand, copied package, unsupported claim, celebrity endorsement, signature, watermark, or unapproved accessory.

OUTPUT INTENT
Return one clean product comparison board at {OUTPUT_SIZE} in 16:9, with the product fully visible and no unrelated props.
```

## Variables

- `{PRODUCT_BRIEF}`: fictional or authorized product identity, geometry, purpose, and channel
- `{MATERIAL_MANIFEST}`: exact components, counts, materials, finishes, colors, and allowed accessories
- `{CAMERA_VIEW}`: camera height, angle, lens character, crop, and scale relationship
- `{LIGHTING}`: declared studio or environmental lighting and shadow behavior
- `{BACKGROUND}`: surface, set, or plain field allowed behind the product
- `{APPROVED_COPY}`: complete allowed product and campaign text, or `none`
- `{OUTPUT_SIZE}`: final pixel dimensions

## Negative constraints

- No real brand, copied packaging, trademark, celebrity likeness, signature, watermark, or unlicensed design feature.
- No invented component, material, accessory, package content, label copy, certification, performance result, or product claim.
- No duplicated product, warped geometry, unreadable approved copy, unrelated prop, decorative pseudo-text, or mock marketplace UI.

## Quick check

Count the declared products and components, compare form and materials with the manifest, and check the intended arrangement: products across the top and a concise approved comparison matrix below. This does not establish preservation reliability or product readiness.

## Rendered Sample

![Rendered sample for Trailtools Product Comparison Board](samples/trailtools-product-comparison-board/trailtools-product-comparison-board.webp)

- Sample status: Rendered Sample.
- Generation surface: built-in image generation tool
- Generated at: `2026-08-30T23:05:35Z`
- Model: `not_exposed`
- Model version: `not_exposed`
- Seed: `not_exposed`
- Request parameters: `not_exposed`
- Request ID: `not_exposed`
- Exact prompt: [trailtools-product-comparison-board.prompt.txt](samples/trailtools-product-comparison-board/trailtools-product-comparison-board.prompt.txt)
- Output dimensions: `1659 x 948`
- Output SHA-256: `e57e79934952e6a0abccccc972cdd589fff51fdc4bbd1861ed493be2c9f83dfc`
- Profile ID: `null`
- Promotion evidence: `false`
- Human inspection: Passed: exactly three trowel variants align on one baseline and every supplied grip, blade, and width value appears in the correct column.
- Known misses: The displayed dimensions are supplied fictional specifications and are not measurements taken from the render.
- Rights and provenance: The concept, exact prompt, accepted image, and public WebP derivative are project-authored. Lossless masters and rejected attempts are retained privately with checksums. The public derivative may be reused under this repository's license; this record is illustrative evidence only.
## Rights and provenance

This Prompt Card is independently authored with `original` source posture. Use only fictional or properly authorized product geometry, packaging, copy, names, and images. It bundles no third-party prompt, product design, package artwork, or image.
