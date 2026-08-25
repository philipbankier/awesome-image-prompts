# Reference Product Environment Edit

- Status: Draft
- Record version: 1
- Task family: Reference-based edit
- Source posture: Attributed Rebuild
- Evidence status: Recorded illustrative run, not promotion evidence
- Canonical source record: [case-519](../../sources/case-519.md)
- Default outcome: Production Candidate, subject to final QA

This Recipe turns one authorized perfume-bottle reference into a vertical e-commerce hero image by replacing its environment while holding the product itself fixed. It is not a general product generator.

## Task fit and non-fit

Use this Recipe when:

- One perfume bottle is the sole product subject.
- The operator has permission to edit the supplied reference.
- The bottle, cap, glass, label, and existing label text must remain recognizably identical.
- The requested change is limited to the environment, supporting props, lighting integration, canvas extension, and crop.
- The target is a vertical e-commerce detail-page image.

Do not use this Recipe to:

- Invent a new bottle, label, logo, product claim, or packaging system.
- Repair, translate, restyle, or replace label text.
- Combine several products or references into one composition.
- Change the bottle geometry, glass material, liquid color, cap, closure, or product contents.
- Edit an upstream example image or any reference without item-level authorization.
- Claim that a generated result is publish-ready without channel-specific final QA.

## Required Creative Brief inputs

Provide all of the following before generation:

1. `authorized_reference`: one local product image or attachment, plus a plain-language statement of the operator's authority to edit it.
2. `reference_identity`: product name used internally for review. Do not infer a brand or claim from an unreadable label.
3. `exact_label_text`: a human-transcribed list of every visible character that must remain unchanged.
4. `must_preserve`: bottle silhouette, dimensions and proportions, glass color and transparency, liquid level if visible, cap geometry and material, label placement, label design, exact label text, and distinctive surface details.
5. `may_change`: background, support surface, non-product props, environmental lighting, cast shadows and reflections needed for integration, canvas extension, and crop outside the product boundary.
6. `environment_replacement`: named props, palette, background, surface, lighting direction, depth of field, and exclusions.
7. `composition`: target aspect ratio, output size, bottle position, margins, and required negative space.
8. `delivery_context`: intended e-commerce channel and the reviewer responsible for final QA.

If authority, exact label text, or a clear preservation inventory is missing, stop before generation.

## Input preparation

1. Confirm that the reference is authorized for this edit and is not the linked upstream case image.
2. Use the highest-quality available reference with the full bottle, cap, label, and edges visible. Avoid motion blur, heavy compression, glare over text, or existing occlusion.
3. Record the input filename, dimensions, file format, and checksum for any future evidence run.
4. Transcribe visible label text manually. If a character cannot be read confidently, mark the brief incomplete rather than guessing.
5. Describe each must-preserve feature from the actual reference. Do not import material or geometry assumptions from an example product.
6. Separate product invariants from environmental changes. No added prop may cover the label, closure, or identifying geometry.
7. Keep the unmodified reference available for every rerun. Do not use a generated derivative as the preservation source.

## Conversational Profile

Profile ID: `conversational-v1`

Attach the authorized reference as the only image input, then send the following instruction with the bracketed fields completed:

```text
Edit the attached authorized product reference into one vertical e-commerce hero image.

REFERENCE ROLE
The attached image is the sole source of truth for the perfume bottle. Keep one bottle only.

MUST PRESERVE
[MUST_PRESERVE]
Preserve the exact visible label text: [EXACT_LABEL_TEXT]. Do not redraw, translate, replace, add, or remove label text. Keep the bottle silhouette, proportions, cap, glass, liquid, label design, and distinctive details unchanged.

MAY CHANGE
Change only the environment outside the product boundary: [MAY_CHANGE]. You may extend the canvas and create physically plausible contact shadows and reflections, but these changes must not alter or obscure the bottle.

ENVIRONMENT REPLACEMENT
[ENVIRONMENT_REPLACEMENT]

COMPOSITION
[COMPOSITION]
Keep the entire bottle and cap visible with safe margins. The product is the dominant focal point.

EXCLUSIONS
No extra bottles, duplicate caps, invented packaging, new logos, new claims, altered label text, label occlusion, product deformation, watermark, or unrelated props.

Return one image. Treat every MUST PRESERVE item as a hard constraint. If the requested environment conflicts with a product invariant, preserve the product.
```

The operator must still inspect the result. Conversational generation does not provide reproducible promotion evidence on its own.

## GPT Image 2 API Profile

Profile ID: `gpt-image-2-api-v1`

Use the Image Edit endpoint with one authorized reference image and the same completed prompt body as the Conversational Profile.

| Request field | Value |
| --- | --- |
| Endpoint | `POST /v1/images/edits` |
| Model | `gpt-image-2` |
| Image input | One authorized product reference |
| Prompt | Completed profile prompt below |
| Size | `2048x3072` for the declared 2:3 portrait evaluation target |
| Quality | `high` |
| Output format | `png` |
| Background | `opaque` |
| Moderation | `auto` |
| Mask | Omit for the baseline evaluation |
| Input fidelity | Omit. GPT Image 2 applies high-fidelity image input handling automatically |

The `2048x3072` output satisfies GPT Image 2's documented flexible-size constraints but falls within the documentation's experimental 2K range. Record any size rejection or quality instability as a failed run. Use `1024x1536` only for explicitly labeled drafts or repair trials, not as proof of the declared high-resolution target.

```text
TASK
Replace only the environment around the single perfume bottle in Image 1 and produce a vertical e-commerce hero image.

IMAGE 1 ROLE
Image 1 is an authorized reference and the sole source of truth for the product. Keep one bottle only.

MUST PRESERVE
[MUST_PRESERVE]
Preserve the exact visible label text: [EXACT_LABEL_TEXT]. Do not redraw, translate, replace, add, or remove label text. Preserve the bottle silhouette, proportions, cap, glass, liquid, label design, and distinctive surface details.

MAY CHANGE
Only these environmental elements may change: [MAY_CHANGE]. Canvas extension, environmental lighting, contact shadows, and reflections are allowed only when they leave the product unchanged and unobscured.

ENVIRONMENT REPLACEMENT
[ENVIRONMENT_REPLACEMENT]

COMPOSITION
[COMPOSITION]
Keep the complete bottle and cap visible with safe margins and make the bottle the dominant focal point.

DO NOT
Do not create extra bottles, duplicate caps, new packaging, new text, new logos, new claims, label occlusion, product deformation, watermarks, or unrelated props. If an environmental instruction conflicts with product preservation, preserve the product.
```

For a promotion evaluation, record the request date, model identifier, endpoint, full parameter set, input checksum, exact completed prompt, response request ID, latency, output checksum, and inspection result. The current evidence manifest contains one supporting-input run and one illustrative edit run, neither of which is promotion evidence.

## Critical Invariants

A result fails immediately if any invariant is false or cannot be verified:

1. The input reference is authorized for editing and is not the upstream case image.
2. Exactly one perfume bottle appears, and it is the same product as the reference.
3. Bottle silhouette, geometry, proportions, orientation, and closure relationship are unchanged.
4. Glass color, transparency, material response, liquid appearance, and distinctive surface details remain faithful to the reference.
5. Cap shape, scale, material, texture, and placement remain faithful to the reference.
6. Label shape, position, design, and every transcribed character remain unchanged and legible at the intended review size.
7. No generated prop, overlay, reflection, crop, or effect obscures the label, cap, or identifying bottle geometry.
8. No extra product, duplicate component, invented packaging, logo, claim, watermark, or unrelated readable text appears.
9. Changes remain within the declared `may_change` and environment boundary.
10. The whole bottle and cap remain inside the canvas with the brief's safe margins.

## Production Candidate Rubric

Apply this rubric only after every Critical Invariant passes. Mark each row `pass`, `fail`, or `not applicable`, and explain every result that is not `pass`. A run passes the full rubric only when every applicable row passes.

| Criterion | Pass condition |
| --- | --- |
| Environment fidelity | All required props, surface, palette, background, and exclusions match the brief |
| Product hierarchy | The bottle is immediately dominant without excessive empty space or competing props |
| Physical integration | Contact, shadows, reflections, refraction, and light direction are plausible and consistent |
| Material realism | Glass, liquid, cap, environmental props, and surfaces have coherent scale and texture |
| Composition | Aspect ratio, bottle placement, crop, margins, and requested negative space match the brief |
| Art direction | Saturation, contrast, depth of field, lighting softness, and finish form one coherent treatment |
| Technical delivery | Output dimensions and format match the declared profile, with no corruption or unintended transparency |
| Defect review | No warped edges, doubled details, halos, broken shadows, floating props, noise artifacts, or stray text are visible at 100% review |

Passing produces a Production Candidate only. Channel crop, claims, trademarks, color management, accessibility, and publishing approval remain final-QA responsibilities.

## Inspection and targeted repair

Inspect the output against the unmodified reference, not from memory:

1. Confirm the evidence record identifies the exact authorized input, profile, completed prompt, and output.
2. Compare reference and output side by side at full-frame view, then at 100% around the label, cap, bottle edges, liquid line, distinctive marks, and contact area.
3. Check every Critical Invariant before scoring aesthetics. Do not average a product-preservation failure into an otherwise attractive score.
4. Inspect the environment against the Creative Brief, including prop type and count, exclusions, negative space, depth of field, and lighting direction.
5. Confirm output dimensions, format, crop, safe margins, and absence of unintended text or watermarks.
6. Record each failed criterion and choose one repair target. Preserve failed runs in recorded evidence when evaluation is authorized.

Use a targeted repair path:

- Product, cap, glass, or label drift: reject the output and rerun from the unmodified reference. Tighten only the relevant preservation clause. Never repair from the drifted output.
- Persistent label or geometry drift: stop generative repair. Escalate to an authorized deterministic compositing workflow outside this Recipe rather than claiming a Production Candidate.
- Missing or incorrect environmental element: rerun from the original reference and revise only the environment block.
- Product occlusion: remove or reposition the named prop in the environment block and restate the unobscured-product invariant.
- Weak integration: adjust only the environmental light, contact shadow, or reflection instruction. Do not change product material wording.
- Wrong crop or margins: revise only the composition block and retain every product invariant.
- Unintended extra text or objects: add the specific defect to `DO NOT`, then rerun once from the original reference.

After a repair, repeat the entire invariant gate and rubric. A repaired output does not inherit the prior run's score.

## Final-QA handoff

Hand off a Production Candidate with:

- Recipe ID and record version.
- Execution Profile ID and complete request parameters.
- Rights confirmation for the input and intended channel.
- Input filename, dimensions, format, and checksum.
- Exact label-text transcript and must-preserve inventory.
- Exact completed prompt and any repair delta.
- Output filename, dimensions, format, checksum, request ID, and generation date.
- Completed Critical Invariants checklist and Production Candidate Rubric.
- Failed attempts, known limitations, and any unresolved visual ambiguity.
- A visible statement that the asset is a Production Candidate, not publish-ready.

Final QA must independently verify channel dimensions and safe zones, label and claim accuracy, trademark and usage rights, color and contrast, accessibility text, disclosure requirements, and publishing approval.

## Representative evaluation briefs

Brief A, warm editorial still life:

- Authorized reference: a fictional oval amber-glass perfume bottle with a brushed-aluminum rectangular cap and exact label text `FIELD NOTE / 01`.
- Must preserve: the oval silhouette, shoulder curve, amber glass density, visible liquid level, brushed cap finish, cap scale, cream label design, label position, and exact text.
- May change: the neutral studio sweep, support surface, environmental props, environmental light, shadows, reflections, canvas extension, and crop outside the bottle.
- Environment replacement: a ribbed limestone plinth, one cobalt paper arc behind the bottle, two dry oat stems outside the product boundary, warm side light, crisp controlled shadows, and a matte editorial finish.
- Composition: one complete bottle on the lower-right third of a `2048x3072` portrait frame, with clear margins and negative space above-left.

Brief B, materially different nocturnal fragrance:

- Authorized reference: a fictional tall, faceted deep-violet glass perfume bottle with a matte ivory cylindrical cap and exact foil label text `NIGHT GLASS / 30 mL`.
- Must preserve: the rectangular faceted silhouette, violet glass density, liquid level, facet highlights, cap geometry and finish, foil label design, label position, and exact text.
- May change: the original white tabletop, background, environmental props, environmental light, shadows, reflections, canvas extension, and crop outside the bottle.
- Environment replacement: a rain-dark basalt plinth, sparse eucalyptus leaves behind the bottle, cool moonlit rim light, a deep blue-gray background, restrained wet reflections, and crisp product focus.
- Composition: one complete bottle on the lower third of a `2048x3072` portrait frame, with asymmetric negative space above-left and safe margins on every edge.

The briefs differ in bottle geometry, glass behavior, cap material, label treatment, props, surface, palette, light, and composition while testing the same narrow preservation contract. A future promotion evaluation requires two API runs per brief plus one disclosed Conversational Profile smoke run. No promotion evaluation run has been completed.

## Rendered Sample

| Project-generated reference | Environment edit |
| :---: | :---: |
| ![Fictional FIELD NOTE perfume bottle on a neutral studio background](samples/field-note-reference.png) | ![The same FIELD NOTE perfume bottle on limestone with a cobalt arc and oat stems](samples/field-note-environment-edit.png) |

The left image is a project-generated fictional reference. The right image is one real environment edit made with the Codex built-in image generation tool on 2026-08-25. Manual comparison found the oval amber bottle, rectangular cap, cream label, and exact `FIELD NOTE / 01` text preserved.

- [Reference-generation prompt](samples/field-note-reference.prompt.txt)
- [Environment-edit prompt](samples/field-note-environment-edit.prompt.txt)
- [Generation Run records](evidence.json)
- Model, model version, seed, request parameters, and request ID: `not_exposed`
- Reference and output: `1024x1536` PNG, below the API profile's `2048x3072` target
- Promotion evidence: no

The pair demonstrates one edit, not repeatability, GPT Image 2 API conformance, a complete invariant pass, or publication readiness.

## Provenance and rights boundary

This Recipe is an attributed rebuild informed by the reference-edit task family documented in [Source Entry case 519](../../sources/case-519.md). The upstream prompt body and literal translation are not included. The Creative Brief fields, profile prompts, evaluation briefs, invariant gate, rubric, repair workflow, and final-QA handoff are independently authored for this project.

The upstream prompt and image remain linked provenance references only. Do not copy or edit the upstream image as a Recipe input or sample. Use only fictional or separately authorized reference products, preserve the source links, and obtain the relevant rights for any commercial use.
