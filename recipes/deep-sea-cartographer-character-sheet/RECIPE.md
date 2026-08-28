# Deep-Sea Cartographer Character Sheet

- Status: Draft
- Record version: 1
- Task family: Fictional character turnaround
- Source posture: Original
- Evidence status: Recorded illustrative built-in-tool sample; promotion evidence: no
- Default outcome: Production Candidate, subject to final QA

This Recipe creates one front, side, and back turnaround of the same wholly fictional character. It does not transfer a real identity or extend an existing franchise.

## Task fit and non-fit

Use this Recipe when:

- one fictional character must remain consistent across three orthographic views;
- face, body, clothing, equipment, and handedness anchors are frozen;
- all three complete figures must share scale and alignment;
- only short approved view labels are required;
- the sheet will be inspected before downstream use.

Do not use it for:

- a real person, celebrity, supplied face, or identity transfer;
- an existing character, franchise costume, or real uniform;
- expressive story poses, animation frames, or a crowd;
- a costume exploration board with alternatives;
- an automatic claim of production readiness.

## Required Creative Brief inputs

Provide:

1. `character_description`, including age range, face, hair, body, and skin.
2. `identity_anchors`, with at least three stable recognition details.
3. `body_proportions` and neutral stance.
4. `clothing_layers`, including colors, seams, closures, and wear.
5. `equipment_inventory`, including count, side, attachment, and scale.
6. `view_manifest`, normally front, side, and back.
7. `view_labels`, as exact strings or an explicit no-text choice.
8. `sheet_layout`, alignment, spacing, field, and palette.
9. `output`, including aspect ratio, pixel size, background, and format.
10. `rights_confirmation` that no real identity or protected design is used.

Stop if identity anchors, equipment placement, or rights are unresolved.

## Input preparation

1. Convert the character description into stable visual anchors.
2. List every garment from inner to outer layer.
3. Assign every tool one count, size, side, and attachment point.
4. Freeze handedness and asymmetrical details.
5. Choose one neutral stance and one shared eye and foot line.
6. Remove any real insignia, logo, or franchise shorthand.
7. Save the brief revision and rendered prompt with every future run.

## Portable prompt

Replace all brace-delimited fields before use.

```text
Create one finished three-view character turnaround sheet, not a scene, moodboard, contact sheet, or set of different people.

SCENE
Use {BACKGROUND} in a {ASPECT_RATIO} landscape sheet divided into {VIEW_LAYOUT}. Place {VIEW_LABELS} at {LABEL_POSITION}.

SUBJECT
Show the same wholly fictional deep-sea cartographer in every view: {CHARACTER_DESCRIPTION}.

DETAILS
Preserve {IDENTITY_ANCHORS}, {BODY_PROPORTIONS}, {CLOTHING_LAYERS}, {EQUIPMENT_INVENTORY}, {HANDEDNESS_RULES}, and {PALETTE}. Align all figures using {ALIGNMENT_RULES}.

CONSTRAINTS
Do not change identity, age, body, costume, equipment count or side, handedness, stance, or scale. Add no real insignia, logo, celebrity likeness, franchise cue, weapon, extra limb, signature, watermark, or unapproved text.

OUTPUT INTENT
Return one complete {ASPECT_RATIO} sheet at {PIXEL_SIZE}, with every figure fully visible and consistent.
```

## Conversational Profile

Profile ID: `conversational-v1`

1. Supply the completed brief and rendered prompt.
2. Ask for unresolved identity or equipment details before generation.
3. Resolve those details outside the model.
4. Request one sheet only.
5. Record visible settings and mark hidden metadata `not_exposed`.
6. Compare every view using the same invariants and rubric.

A conversational run cannot replace API promotion evidence.

## GPT Image 2 API Profile

Profile ID: `gpt-image-2-api-v1`

Endpoint: OpenAI Image API, `POST /v1/images/generations`.

```json
{
  "model": "gpt-image-2-2026-04-21",
  "prompt": "<completed portable prompt>",
  "n": 1,
  "size": "1536x1024",
  "quality": "high",
  "background": "opaque",
  "output_format": "png",
  "moderation": "auto"
}
```

Approve the exact request, credential source, spend ceiling, retention policy, evidence path, and stop condition before any API call. Keep failed identity attempts visible.

## Critical Invariants

- `CI-01 Identity`: face, hair, age, skin, scar, and body anchors match across views.
- `CI-02 Costume`: every garment, seam, color, and closure remains consistent.
- `CI-03 Equipment`: count, form, side, and attachment match the manifest.
- `CI-04 Proportion`: height, limb proportion, and scale remain constant.
- `CI-05 Views`: front, side, and back orientations are distinct and correctly labeled.
- `CI-06 Anatomy`: no missing, duplicated, fused, or impossible body parts appear.
- `CI-07 Rights`: no real-person likeness, real insignia, or franchise cue appears.

Any failed invariant blocks the candidate.

## Production Candidate Rubric

Score `pass` or `fail` after all invariants pass:

- `R-01 Recognition`: the person is immediately the same in all three views.
- `R-02 Silhouette`: the role reads from clothing and equipment without a logo.
- `R-03 Construction`: garments and attachments remain physically coherent.
- `R-04 Alignment`: eyes, ground line, scale, and spacing follow the sheet rules.
- `R-05 Legibility`: view labels and small equipment remain readable.
- `R-06 Finish`: no anatomy, edge, texture, or rendering artifact distracts.

All six items must pass. Promotion remains subject to separate multi-run evidence.

## Inspection and targeted repair

1. Compare face, hairline, scar, body, and skin view by view.
2. Trace every garment seam and pocket around the body.
3. Count equipment and verify its side and attachment.
4. Measure eye line, ground line, and figure scale.
5. Inspect hands, feet, and hidden-side transitions.
6. Record every failure before repair.

Repair one anchor class at a time. Restate the full identity when repairing the face, and the full inventory when repairing costume or gear. Preserve all accepted views, alignment, palette, and dimensions. Rescore the entire repaired sheet.

## Final-QA handoff

Include the selected image and checksum, brief revision, prompt, identity anchors, costume and equipment manifests, profile data, invariant and rubric results, repair history, and rights confirmation. Label it `Production Candidate`. Human review still covers representation, downstream consistency, and publication rights.

## Representative fictional brief

- Character: approximately forty, deep brown skin, oval face, broad nose, dark hazel eyes, short tight black curls, silver right-temple streak, compact athletic build, and left-eyebrow crescent scar.
- Clothing: rust knit undershirt, slate waterproof trousers, cream six-pocket vest, dark teal boots, and folded charcoal hood.
- Equipment: brass compass on left vest strap, cream chart case at right hip, slate stylus behind right ear, depth gauge on left wrist, and measuring line at back belt.
- Views: front, side, and back; neutral stance; exact labels `FRONT`, `SIDE`, and `BACK`.
- Layout: warm-gray field, equal regions, aligned eyes and feet, 3:2 landscape, `1536x1024`.
- Rights: character, costume, equipment, and insignia are fictional and project-authored.

The fully resolved illustrative prompt is [saved here](samples/deep-sea-cartographer-character-sheet.prompt.txt).

## Rendered Sample

![Front, side, and back turnaround of a fictional deep-sea cartographer](samples/deep-sea-cartographer-character-sheet.png)

This is one recorded illustrative output from the representative brief with the Codex built-in image generation tool on 2026-08-26. Manual review found a strong three-view identity, exact view labels, aligned figures, and recognizable equipment. Only four clear vest pockets are visible rather than six, and chart-case side consistency is not established across views.

- [Exact submitted prompt](samples/deep-sea-cartographer-character-sheet.prompt.txt)
- [Generation run record](evidence.json)
- Model, model version, seed, request parameters, and request ID: `not_exposed`
- Output: `1536x1024` PNG
- Promotion evidence: no

This sample is one illustrative built-in-tool output. It does not demonstrate repeatability, GPT Image 2 API conformance, Recipe promotion evidence, a full identity-and-equipment invariant pass, downstream character consistency, or publication readiness.

## Rights and provenance boundary

This independently authored Recipe has `original` source posture and no Source Entry. It uses no reference face, celebrity, real uniform, protected character, or upstream prompt. A fictional design still requires final similarity review before publication.
