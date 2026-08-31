# Authorized Portrait Background Extension

## Use this when

Use this card for a bounded creative brief that needs the following output: extended portrait composition. Use a Recipe instead when exact preservation, repeatability, or formal production evidence is required.

## Required inputs

- Every attached image or sketch, its intended role, and confirmation that it may be used.
- For identifiable people, documented subject permission or an applicable public-domain or lawful-use basis.
- A fictional, public-domain, or authorized project brief and intended use.
- A closed content manifest with exact counts, order, and approved text where applicable.
- Visual direction, palette, composition, target aspect ratio, and exclusions.

## Prompt

```text
INPUTS
Use only the declared, authorized assets in {AUTHORIZED_INPUTS}. Treat them as content references, not permission to invent identities, brands, or provenance. For identifiable people, use only sources with documented subject permission or an applicable public-domain or lawful-use basis.

SCENE
Create one extended portrait composition for {PROJECT_BRIEF}.

SUBJECT
Extend the authorized portrait beyond its original crop to the declared wider composition while preserving the subject's face, body, clothing, pose, camera, and existing background continuity.

DETAILS
Include exactly {CONTENT_MANIFEST}. Follow {VISUAL_DIRECTION}, {COLOR_PALETTE}, and {COMPOSITION}; keep scale, orientation, spacing, and visual hierarchy internally consistent.

CONSTRAINTS
Do not add undeclared subjects, panels, symbols, copy, logos, signatures, or watermarks. Avoid {MUST_AVOID}. Do not imply factual verification, endorsement, or evidence that is not supplied.

OUTPUT INTENT
Return one finished extended portrait composition at {ASPECT_RATIO}, complete inside the frame and ready for the stated project review.
```

## Variables

- `{AUTHORIZED_INPUTS}`: attached reference, sketch, or image manifest with permission and each asset's role
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

Overlay the original crop mentally and confirm the retained region is unchanged while the new margins continue perspective and lighting.

## Placeholder Preview

Sample status: Placeholder Preview. No recorded generation run.

Expected result: extended portrait composition with the declared content, hierarchy, and visual direction clearly visible.

## Rights and provenance

This Prompt Card is independently authored with `original` source posture. Use only fictional, public-domain, or properly authorized subjects, references, names, data, and brand materials. It bundles no third-party prompt or image.
