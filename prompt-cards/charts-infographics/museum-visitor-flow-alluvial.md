# Museum Visitor Flow Alluvial

## Use this when

Use this Card for a fast early-stage alluvial diagram that maps supplied fictional visitor transitions across three exhibit stages. It does not establish factual correctness, preservation fidelity, or Recipe-level reliability. Use a Recipe and qualified review when exact content or repeatability matters.

## Required inputs

- A fictional, public-domain, or properly authorized subject brief and intended audience.
- The complete approved content manifest; independently verify any facts before use.
- Panel count, reading order, hierarchy, and placement constraints.
- Project-owned visual direction, palette, exact allowed text, and exclusions.
- An ordered, project-owned, verified public-domain, or properly authorized image set with one role and preserve/change rule per image.

## Prompt

```text
Create one original alluvial diagram for the following narrow task.

TASK: maps supplied fictional visitor transitions across three exhibit stages.
SUBJECT: Use only {SUBJECT_BRIEF} and the supplied content {CONTENT_MANIFEST}.
COMPOSITION: Begin with this independently authored structure: Use three aligned stage columns with labeled blocks and ribbons whose widths follow supplied transition totals. Apply {STRUCTURE_PLAN} without adding undeclared panels or relationships.
VISUAL DIRECTION: Use museum-catalog restraint, ample white space, and subtle ribbon transparency without pictorial exhibit imagery. Express it through {VISUAL_LANGUAGE} and {PALETTE} while keeping the hierarchy legible.
TEXT: Render only {TEXT_MANIFEST}. If it is `none`, include no letters, numerals, legends, captions, seals, or decorative pseudo-writing.
MULTIPLE INPUTS: Use {AUTHORIZED_IMAGE_SET} only after every image's project-owned, verified public-domain, or otherwise authorized status is documented, and only in the declared order and roles. Preserve exactly {PRESERVE_MANIFEST}; keep inputs distinguishable unless combination is explicitly authorized, and never average identities or invent bridging evidence.
BOUNDARY: Do not invent measurements, data, historical claims, scientific conclusions, chronology, or labels. Do not depict a living-person likeness, real brand, propaganda, unsafe instruction, copied artwork, signature, watermark, or {EXCLUSIONS}.
OUTPUT: Return one flat 16:9 composition. This is a quick concept image, not factual validation, preservation proof, or Recipe-level reliability.
```

## Variables

- `{SUBJECT_BRIEF}`: the fictional, public-domain, or authorized subject and intended audience
- `{CONTENT_MANIFEST}`: the complete supplied facts, values, relationships, or story details allowed in the image
- `{STRUCTURE_PLAN}`: panel count, reading order, hierarchy, spacing, and placement constraints
- `{VISUAL_LANGUAGE}`: the project-owned medium, mark-making, geometry, and finish direction
- `{PALETTE}`: the approved colors and contrast relationships
- `{TEXT_MANIFEST}`: the exact allowed labels and copy, or `none` when the image should contain no text
- `{EXCLUSIONS}`: subject-specific content, motifs, claims, and artifacts that must not appear
- `{AUTHORIZED_IMAGE_SET}`: an ordered set of project-owned, verified public-domain, or properly authorized non-living-person images
- `{PRESERVE_MANIFEST}`: the exact approved role and preserved features for every input image

## Negative constraints

- No invented facts, numbers, relationships, labels, chronology, or scientific conclusions beyond the supplied manifest.
- No living-person likeness, real brand, propaganda, unsafe instruction, copied artwork, signature, or watermark.
- No extra panel, duplicate subject, pseudo-text, clipped label, unexplained symbol, or unapproved visual claim.

## Quick check

Confirm the declared panel count and reading order, transcribe any allowed text, and sum every stage block and trace each ribbon between its declared source and destination. This check only rejects obvious failures; it does not validate facts or establish Recipe-level reliability.

## Placeholder Preview

Sample status: Placeholder Preview. No recorded generation run.

The planned preview concept maps supplied fictional visitor transitions across three exhibit stages. Visual direction: Use museum-catalog restraint, ample white space, and subtle ribbon transparency without pictorial exhibit imagery. It is ungenerated planning material, not behavioral evidence or factual validation.

## Rights and provenance

This Prompt Card is independently authored with `original` source posture. Every input image must be project-owned, verified public-domain, or separately authorized, must avoid living-person likenesses, and may be combined only as the preserve manifest permits. Use only fictional, public-domain, or properly authorized subjects, data, copy, and visual materials. It bundles no third-party prompt or image and makes no Card-level reliability claim.
