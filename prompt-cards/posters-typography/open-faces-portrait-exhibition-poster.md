# Open Faces Portrait Exhibition Poster

## Use this when

Use this card when you need to promote a fictional portrait exhibition using one authorized sitter image. Use a Recipe when exact typography, preservation, structured repair, repeatability, or evidence matters.

## Required inputs

- A fictional or authorized subject brief and intended audience.
- The exact approved copy manifest, including an explicit `none` when no text is allowed.
- Visual motif, palette, type direction, composition rules, output size, and channel crop.
- One attached reference image and confirmation that it is authorized for this use.
- A preservation manifest separating protected features from approved changes.

## Prompt

```text
COMMISSION
Create one 2:3 portrait exhibition poster to promote a fictional portrait exhibition using one authorized sitter image. Use this independently authored concept: a preserved portrait interrupted only by transparent rectangular captions.

REFERENCE INPUT
Use the attached authorized {REFERENCE_IMAGE} only for {REFERENCE_ROLE}. Preserve {PRESERVE_RULES}; change only elements explicitly permitted by the brief. Do not infer unseen geometry, replace an identity, alter protected copy, or import marks from the reference.

CONTENT
Build the subject from {SUBJECT_BRIEF}. Render only the exact approved copy in {COPY_MANIFEST}; if the manifest says `none`, render no text. Do not add names, dates, sponsors, claims, labels, or calls to action outside that manifest.

VISUAL SYSTEM
Use {VISUAL_MOTIF}, {PALETTE}, and {TYPE_DIRECTION}. Organize the page as follows: face remains unobstructed with exhibition title above and details below. Apply {COMPOSITION_RULES} for hierarchy, margins, crop, contrast, and reading order.

CONSTRAINTS
Use only fictional, public-domain, or authorized subject matter. No real brand, copied campaign, celebrity likeness, unsupported claim, unapproved logo, pseudo-writing, signature, or watermark.

OUTPUT INTENT
Return one flat portrait exhibition poster at {OUTPUT_SIZE} in 2:3. Do not place it in a wall, frame, device, or merchandise mockup.
```

## Variables

- `{SUBJECT_BRIEF}`: fictional or authorized subject, audience, purpose, and factual details
- `{COPY_MANIFEST}`: complete allowed text with exact spelling and hierarchy, or `none`
- `{VISUAL_MOTIF}`: one original central motif and its visual role
- `{PALETTE}`: approved color names or values and contrast relationship
- `{TYPE_DIRECTION}`: project-owned typography character, weight, and case direction
- `{COMPOSITION_RULES}`: margins, reading order, focal position, safe zones, and crop behavior
- `{OUTPUT_SIZE}`: final pixel dimensions
- `{REFERENCE_IMAGE}`: attached authorized single reference image
- `{REFERENCE_ROLE}`: the sole role the reference may play in the composition
- `{PRESERVE_RULES}`: features, geometry, identity, copy, or relationships that must remain unchanged

## Negative constraints

- No copied poster, campaign system, trademark, copyrighted character, celebrity likeness, or unlicensed artwork.
- No misspelled, paraphrased, duplicated, invented, clipped, or decorative pseudo-text.
- No unsupported factual or product claim, signature, watermark, mockup scene, or extra design option.

## Quick check

Confirm the result reads as one portrait exhibition poster, verify the exact copy against the manifest, and check the intended arrangement at thumbnail size: face remains unobstructed with exhibition title above and details below. This is only an obvious-failure check.

## Rendered Sample

![Rendered sample for Open Faces Portrait Exhibition Poster](samples/open-faces-portrait-exhibition-poster/open-faces-portrait-exhibition-poster.webp)

- Sample status: Rendered Sample.
- Generation surface: built-in image generation tool
- Generated at: `2026-08-30T23:24:03Z`
- Model: `not_exposed`
- Model version: `not_exposed`
- Seed: `not_exposed`
- Request parameters: `not_exposed`
- Request ID: `not_exposed`
- Exact prompt: [open-faces-portrait-exhibition-poster.prompt.txt](samples/open-faces-portrait-exhibition-poster/open-faces-portrait-exhibition-poster.prompt.txt)
- Output dimensions: `1024 x 1536`
- Output SHA-256: `376cb4515cae078cb2132b893c6ed0b8a73705aaa77bd551cf04d427d440fd94`
- Profile ID: `null`
- Promotion evidence: `false`
- Human inspection: The portrait remains unobstructed, with the title in pale-cyan panels above and three detail bands below.
- Known misses: None observed at the reviewed master resolution.
- Rights and provenance: The concept, exact prompt, accepted image, and public WebP derivative are project-authored. Lossless masters and rejected attempts are retained privately with checksums. The public derivative may be reused under this repository's license; this record is illustrative evidence only.
- Supporting inputs:
  - [input-01-fictional-sitter.webp](samples/open-faces-portrait-exhibition-poster/input-01-fictional-sitter.webp): project-authored fictional fictional sitter input
## Rights and provenance

This Prompt Card is independently authored with `original` source posture. Use only fictional, public-domain, or properly authorized text, subjects, images, and type direction. The attached reference image must be owned or explicitly authorized, and its preservation manifest must be honored.
