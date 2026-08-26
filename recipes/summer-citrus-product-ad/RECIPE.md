# Summer Citrus Product Advertisement

Status: Draft Recipe with one recorded illustrative sample. The sample is not promotion evidence.

Outcome: one Production Candidate for a fictional summer citrus beverage advertisement. Generation alone does not make the result publish-ready.

## Task fit

Use this Recipe when the brief requires:

- one finished product advertisement, not a moodboard or option sheet;
- a fictional or authorized citrus beverage and container;
- a short, closed list of exact English display strings;
- commercial product photography with declared framing and crop;
- inspection and targeted repair before final channel QA.

Do not use it for:

- an existing brand, package, logo, or claim without documented authorization;
- long-form copy, dense comparison tables, or a multi-module detail page;
- medical, nutrition, performance, or environmental claims that lack an approved source;
- a reference-image edit, packaging redesign, or identity-preservation task;
- a request that expects generation alone to produce a publish-ready asset.

## Required Creative Brief

Provide every field before generation:

- `product_name`: fictional or authorized product name.
- `product_category`: for example, sparkling citrus drink or citrus soda.
- `container`: material, shape, closure, and declared volume.
- `liquid_and_flavor`: liquid appearance plus the citrus ingredients shown.
- `exact_text`: an ordered list of one to four strings that must appear verbatim.
- `text_placement`: one location for each exact string.
- `scene`: environment, supporting props, and surface.
- `composition`: camera view, product position, negative space, and crop.
- `palette_and_light`: restrained palette and one coherent lighting direction.
- `output`: aspect ratio, pixel size, background, and file format.
- `must_avoid`: brief-specific exclusions.
- `rights_confirmation`: confirmation that names, packaging, copy, claims, and supplied assets are fictional or authorized.

If any display string, product geometry, output size, or rights confirmation is missing, stop and request it. Do not invent commercial copy, a price, a claim, or a brand mark.

## Input preparation

1. Freeze the exact-text manifest before writing visual direction. Preserve spelling, case, punctuation, spaces, and units.
2. Check that the volume in `exact_text` matches the container description.
3. Assign every string one placement. Do not ask the model to choose which copy is primary.
4. Remove unapproved logos, certification marks, prices, claims, and legal text.
5. Reduce props to elements that support the named flavor and season.
6. Choose one output size whose orientation matches the intended crop.
7. Save the completed brief, prompt, profile version, and rights confirmation with every future run record.

## Portable first-generation prompt

Replace every brace-delimited value with the approved brief. Do not leave unresolved placeholders.

```text
Create one finished commercial product advertisement, not a moodboard, contact sheet, package mockup board, or set of alternatives.

PRODUCT
- Fictional product: {PRODUCT_NAME}, a {PRODUCT_CATEGORY}.
- Container: {CONTAINER_MATERIAL}, {CONTAINER_SHAPE}, {CLOSURE}, declared volume {VOLUME}.
- Liquid and flavor cues: {LIQUID_AND_FLAVOR}.
- The container geometry, closure, liquid level, and declared volume must be physically coherent.

EXACT DISPLAY TEXT
- Render only these strings, each exactly once:
  1. "{TEXT_1}" at {TEXT_1_PLACEMENT}
  2. "{TEXT_2}" at {TEXT_2_PLACEMENT}
  3. "{TEXT_3}" at {TEXT_3_PLACEMENT}
  4. "{TEXT_4}" at {TEXT_4_PLACEMENT}
- Preserve every character, space, punctuation mark, capital letter, and unit exactly as supplied.
- Do not translate, paraphrase, duplicate, truncate, decorate, or add text.
- Add no other letters, numbers, unrequested logos, signatures, watermarks, prices, claims, or fine print.

COMPOSITION
- Scene: {SCENE}.
- Camera and product position: {COMPOSITION}.
- Keep the complete product silhouette, closure, label, and base inside the frame.
- Keep the declared copy-safe area clear and give every text string strong contrast.

ART DIRECTION
- Palette and lighting: {PALETTE_AND_LIGHT}.
- Materials must look physically credible: clean container edges, coherent reflections, realistic condensation, believable liquid, and grounded contact shadows.
- Supporting citrus and props must remain secondary to the product.

OUTPUT CONSTRAINTS
- One finished advertisement at {ASPECT_RATIO}; compose for {PIXEL_SIZE}.
- Background: {BACKGROUND}.
- No unrelated props, extra products, deformed packaging, duplicated fruit, illegible text, clipped copy, clutter, UI chrome, or comparison panels.
- Additional exclusions: {MUST_AVOID}.
```

If a brief has fewer than four strings, delete the unused numbered lines. Never send empty placeholders.

## Conversational Profile: conversational-v1

Use a conversational image-generation surface only when it states that it supports GPT Image 2 generation.

1. Paste the completed Creative Brief and portable prompt.
2. Ask the assistant to identify unresolved fields without generating. Resolve them in one short clarification round.
3. Say: `Generate one image now. Treat the exact-text manifest and Critical Invariants as non-negotiable.`
4. Record the surface, date, any displayed model name, and every observable option. Record hidden model versions or parameters as `not exposed`; do not infer them.
5. Inspect the result against the same invariants and rubric used by the API profile.

This profile is for operator use and one required smoke run. It cannot replace API promotion evidence because conversational surfaces may hide the exact model version and request parameters.

## GPT Image 2 API Profile: gpt-image-2-api-v1

Surface: OpenAI Image API, `POST /v1/images/generations`.

Model: `gpt-image-2-2026-04-21`.

Profile request:

```json
{
  "model": "gpt-image-2-2026-04-21",
  "prompt": "<completed portable first-generation prompt>",
  "n": 1,
  "size": "<exact pixel size from the evaluation brief>",
  "quality": "high",
  "background": "opaque",
  "output_format": "png",
  "moderation": "auto"
}
```

Profile rules:

- Use `1200x1600` for Evaluation Brief A and `1536x1024` for Evaluation Brief B.
- Run two separate requests per brief. Do not use one request with `n: 2` as a substitute for two Generation Run records.
- Preserve the fully assembled prompt and exact request body for each run.
- Decode and store the returned base64 image only inside the approved evidence location for the future run.
- Record the response request ID when exposed, output checksum, dimensions, format, latency, and actual cost when available.
- Before any provider-connected run, approve an exact run manifest, credential source, spend ceiling, retention policy, evidence location, and stop condition.
- A blocked or failed request is a recorded failure. Retry transient errors only within the approved run manifest. Do not silently rewrite a user-correctable prompt or safety failure.

The request shape and output options were checked against the [official OpenAI image-generation guide](https://developers.openai.com/api/docs/guides/image-generation) on 2026-08-25. No OpenAI Image API request has been made for this Recipe. Official documentation notes that precise text rendering and layout-sensitive composition can still fail, so both remain explicit evaluation criteria rather than assumed capabilities.

## Critical Invariants

Every generated or repaired candidate must pass all six. A critical failure blocks promotion even if the image is attractive.

- `CI-01 Exact text`: every manifest string appears exactly once with identical characters, capitalization, punctuation, spacing, and units. No other visible text appears.
- `CI-02 Product geometry`: container material, form, closure, count, and volume match the brief. The product is not fused, duplicated, or structurally impossible.
- `CI-03 Crop and safe area`: the complete product, label, closure, base, and every text string remain inside the frame with the declared copy-safe area intact.
- `CI-04 Brief identity`: flavor, liquid, season, scene, orientation, and required product role match the selected evaluation brief without cross-brief leakage.
- `CI-05 Rights and claims`: the output contains no third-party brand marks, unapproved claims, prices, certifications, signatures, or watermarks.
- `CI-06 Deliverable form`: the output is one finished advertisement, not a moodboard, option grid, process sheet, UI frame, or package-design board.

## Production Candidate Rubric

Rubric version: `product-ad-rubric-v1`.

A full-rubric pass requires all Critical Invariants and every quality criterion below to pass. Record each item as `pass` or `fail` with one sentence of evidence. Do not average away a failure.

- `Q-01 Product hierarchy`: the beverage container is the immediate focal point and supporting elements do not compete with it.
- `Q-02 Text legibility`: every exact string is readable at the intended delivery size, with sufficient contrast and no collision with product edges or props.
- `Q-03 Material realism`: container, liquid, condensation, citrus, reflections, refractions, and shadows are mutually coherent and commercially credible.
- `Q-04 Composition`: the declared camera angle, negative space, orientation, and text placements create a balanced advertisement rather than a generic centered packshot.
- `Q-05 Art direction`: palette, lighting direction, season, and energy match the brief as one controlled visual system.
- `Q-06 Flavor communication`: the named citrus flavor is recognizable without excessive, duplicated, or anatomically implausible fruit.
- `Q-07 Finish quality`: no malformed edges, floating objects, accidental tangencies, smeared labels, unexplained artifacts, or low-resolution regions are visible at 100 percent inspection.
- `Q-08 Technical delivery`: decoded file format, pixel dimensions, background treatment, and orientation match the API profile and brief.

Promotion remains blocked until four API runs are recorded across the two evaluation briefs, all four pass every Critical Invariant, at least three pass the full rubric, and one additional conversational smoke run is recorded.

## Inspection and targeted repair

Inspect every output before selecting or repairing it:

1. Open the image at 100 percent and at intended delivery size.
2. Transcribe all visible text from the image, then compare it character by character with the manifest. OCR may assist but is not the authority.
3. Count products, closures, labels, fruit pieces, and every occurrence of each text string.
4. Trace the product silhouette and frame edges for clipping, deformation, or unsafe copy placement.
5. Check reflections, condensation, liquid level, contact shadow, and citrus anatomy for physical coherence.
6. Score every Critical Invariant and rubric criterion. Keep failures visible in the future run record.

Repair one diagnosed failure at a time:

- Text failure: request only the misspelled, duplicated, missing, or extra text correction. Restate the full exact-text manifest and prohibit all other changes.
- Geometry failure: restate container material, form, closure, volume, and count. Ask to preserve accepted composition and copy.
- Crop failure: expand or reposition the existing composition while preserving product scale, text, and art direction.
- Visual artifact: identify the exact object and defect. Do not ask for a general improvement pass.
- Repeated text failure: regenerate once with reduced decoration around the affected text. If exact text still fails, record the API run as failed. A later human-composited version may continue toward publication, but it is not passing Recipe promotion evidence.

Treat every repaired output as a new candidate and rerun the complete inspection. Never erase the failed predecessor from recorded evidence.

## Final-QA handoff

A passing Recipe output is a Production Candidate. Hand off:

- the selected image and checksum;
- Creative Brief and exact-text manifest;
- completed prompt, Recipe record version, profile version, model, request parameters, and run ID;
- full invariant and rubric results, including repairs and unresolved concerns;
- documented rights confirmation for brand, copy, claims, and any supplied assets;
- a note that no upstream image is included or licensed by this Recipe.

Before anyone calls the asset publish-ready, a human owner must separately approve exact copy, brand assets, claims, prices, legal text, channel crop and safe zones, accessibility and alt text, color and export requirements, and final distribution rights.

## Representative evaluation briefs

These briefs are materially different in container, flavor, environment, palette, camera, orientation, and exact copy.

Evaluation Brief A, `daylight-pet-bottle`:

- Product: fictional `CITRA SUN` sparkling lemon and yuzu drink.
- Container: one transparent 500 ml PET bottle, straight cylindrical walls, shallow shoulder, white tamper-evident cap, pale-yellow carbonated liquid, and one cream paper label.
- Exact text, each once: `CITRA SUN`; `LEMON + YUZU`; `SPARKLING CITRUS DRINK`; `500 mL`.
- Placement: brand centered on label; flavor below brand; product descriptor in upper-left negative space; volume at label base.
- Scene: warm ivory stone plinth with a restrained lemon half, one yuzu peel curl, and soft pool-light caustics.
- Composition: eye-level three-quarter bottle view, product centered slightly right, complete silhouette visible, clean upper-left copy area.
- Palette and light: lemon yellow, warm ivory, leaf green, hard summer key light from upper left with soft fill.
- Output: 3:4 portrait, `1200x1600`, opaque PNG.
- Must avoid: extra bottles, extra labels, splashing liquid, tropical fruit, blue caps, prices, nutrition claims, third-party logos, and fine print.
- Rights confirmation: all brand, copy, packaging, and claims are fictional for evaluation.

Evaluation Brief B, `twilight-slim-can`:

- Product: fictional `TIDE LIME` pink-grapefruit and lime citrus sparkler.
- Container: one matte silver 330 ml slim aluminum can, narrow straight body, rolled top rim, standard silver pull tab, and cold condensation.
- Exact text, each once: `TIDE LIME`; `PINK GRAPEFRUIT + LIME`; `CITRUS SPARKLER`; `330 mL`.
- Placement: brand vertical on can; flavor in one horizontal line below brand; product descriptor in right-side negative space; volume near can base.
- Scene: can standing on dark wet stone at coastal twilight, with one grapefruit wedge and one lime wheel behind the product.
- Composition: low three-quarter view, can on left third, complete silhouette visible, broad right-side copy area and distant soft horizon.
- Palette and light: cool slate, silver, grapefruit coral, and acid green with a cyan rim light and warm coral reflection.
- Output: 3:2 landscape, `1536x1024`, opaque PNG.
- Must avoid: bottles, beach-party crowds, neon signage, extra cans, ice buckets, prices, wellness claims, third-party logos, and fine print.
- Rights confirmation: all brand, copy, packaging, and claims are fictional for evaluation.

## Rendered Sample

![CITRA SUN sparkling citrus drink advertisement with a lemon and yuzu bottle on an ivory stone plinth](samples/citra-sun.png)

This is one real output generated from Evaluation Brief A with the Codex built-in image generation tool on 2026-08-25. Manual review found all four exact strings visibly correct and the single bottle coherent.

- [Exact submitted prompt](samples/citra-sun.prompt.txt)
- [Generation Run record](evidence.json)
- Model, model version, seed, request parameters, and request ID: `not_exposed`
- Output: `1086x1448` PNG, not the API profile's `1200x1600` target
- Promotion evidence: no

The sample demonstrates one result, not repeatability, GPT Image 2 API conformance, a full rubric pass, or publication readiness.

## Provenance and rights boundary

This Recipe is an attributed rebuild informed by upstream `case-237`. See the pinned [Source Entry](../../sources/case-237.md). It is not a translation and does not copy the upstream image.

The Recipe's briefs, prompt structure, invariants, rubric, profiles, inspection, and repair guidance are newly authored. The upstream entry and image remain third-party provenance fixtures with unverified item-level reuse rights. New runs must use fictional or authorized names, packaging, copy, claims, and inputs. A passing generation remains a Production Candidate until channel-specific rights and final QA are complete.
