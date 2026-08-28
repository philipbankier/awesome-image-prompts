# Fictional Ceramic Reconstruction Board

## Use this when

Use this card for a museum-style concept board based on project-authored fictional shards. It must state uncertainty and is not archaeological evidence. Use a Recipe when input preservation, exact annotation, or uncertainty review requires evidence.

## Required inputs

Provide one project-owned shard reference sheet as an image or sketch, its authorization, shard inventory, proposed vessel geometry, confidence labels, exact annotations, scale bar, layout, palette, aspect ratio, and prohibited claims.

## Prompt

```text
REFERENCE INPUT: Use the attached authorized {SHARD_REFERENCE_SHEET} as the sole visual source for every observed fragment. Preserve its markings and proportions.
SCENE: Arrange one neutral reconstruction board on {BACKGROUND} using {LAYOUT_SPEC}, with the project-owned fictional shards shown at {SHARD_SCALE}.
SUBJECT: Present {SHARD_INVENTORY} beside the hypothetical vessel form {PROPOSED_GEOMETRY}.
DETAILS: Match each shard to {PLACEMENT_MAP}, render {EXACT_ANNOTATIONS}, {CONFIDENCE_LABELS}, and {SCALE_BAR_EXACT} verbatim, use {PALETTE}, and distinguish observed fragments from hypothetical completion with {UNCERTAINTY_ENCODING}.
CONSTRAINTS: Do not alter shard markings, assert provenance, invent decoration, hide uncertainty, copy a real artifact, add museum branding, signatures, or watermarks. Also avoid {MUST_AVOID}.
OUTPUT INTENT: Return one finished {ASPECT_RATIO} concept board that clearly separates project-owned fictional evidence from hypothetical reconstruction.
```

## Variables

- `{SHARD_REFERENCE_SHEET}`: one attached project-owned image or sketch containing the complete shard set.
- `{BACKGROUND}`, `{LAYOUT_SPEC}`, and `{ASPECT_RATIO}`: page construction.
- `{SHARD_INVENTORY}` and `{SHARD_SCALE}`: exact project-owned inputs.
- `{PROPOSED_GEOMETRY}` and `{PLACEMENT_MAP}`: declared hypothesis.
- `{EXACT_ANNOTATIONS}`, `{CONFIDENCE_LABELS}`, and `{SCALE_BAR_EXACT}`: closed text manifest.
- `{PALETTE}` and `{UNCERTAINTY_ENCODING}`: visual distinction between observed and hypothetical content.
- `{MUST_AVOID}`: additional prohibited claims or motifs.

## Negative constraints

No real artifact copying, altered shard marks, invented provenance, hidden uncertainty, false certainty, pseudo-labels, museum logos, signatures, or watermarks.

## Quick check

Match every shard to its owned input, transcribe every label, inspect the placement map, and confirm hypothetical regions cannot be mistaken for observed material.

## Placeholder Preview

Sample status: Placeholder Preview. No recorded generation run.

The intended preview is a restrained reconstruction board that labels its vessel and fragments as wholly fictional.

## Rights and provenance

This card is independently authored with `original` source posture. All shards, annotations, and vessel hypotheses must be project-authored or otherwise authorized; no real artifact or upstream prompt is included.
