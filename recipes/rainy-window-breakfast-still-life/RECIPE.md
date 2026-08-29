# Rainy-Window Breakfast Still Life

- Status: Draft
- Record version: 1
- Task family: Photoreal editorial still life
- Source posture: Original
- Evidence status: Recorded illustrative built-in-tool sample; promotion evidence: no
- Default outcome: Production Candidate, subject to final QA

This Recipe creates one restrained breakfast still life beside a rainy window. It makes object count, food plausibility, material realism, weather, focus, lighting, and crop explicit so the image can be inspected beyond surface mood.

## Task fit and non-fit

Use this Recipe when:

- one fictional or authorized breakfast arrangement is the sole subject;
- the food, drink, vessel, utensil, textile, and prop manifest can be frozen;
- a photoreal editorial image needs believable rain, window light, and material detail;
- the operator can inspect anatomy, count, reflections, shadows, steam, and focus.

Do not use it to:

- reproduce an unauthorized photograph, branded food package, restaurant identity, or distinctive editorial campaign;
- invent nutrition, ingredient, origin, freshness, or health claims;
- show people, food preparation, recipes, or a multi-scene story;
- treat attractive styling as evidence of edible accuracy or publication readiness;
- replace food-safety, advertising, or rights review.

## Required Creative Brief inputs

Provide every field before generation:

1. `scene_identity`: fictional or authorized setting and intended editorial use.
2. `food_and_drink_manifest`: exact items, preparation state, garnishes, and quantities.
3. `tableware_manifest`: exact vessels, utensils, textiles, and counts.
4. `prop_manifest`: closed secondary-object list, or `none`.
5. `window_and_weather`: window form, rain, exterior glimpse, season, and time.
6. `composition`: camera angle, lens character, focal subject, crop, and depth of field.
7. `lighting`: window direction, softness, room fill, and contrast.
8. `output`: aspect ratio, dimensions, background, and format.
9. `must_avoid`: brief-specific exclusions.
10. `rights_confirmation`: authority for references, products, marks, and location.

Stop if any manifest, reference right, or intended text is unresolved.

## Input preparation

1. Convert the breakfast into a closed item and quantity manifest.
2. Separate primary food and drink from tableware, textiles, and props.
3. State preparation details that affect texture, steam, moisture, and color.
4. Choose one window direction and map the expected highlights and shadows.
5. Define one focal plane and keep every review-critical object legible.
6. Remove real brands, packaging, labels, and unapproved text.
7. Save the completed brief, exact prompt, Recipe version, and rights statement for a future run.

## Portable prompt

Replace every brace-delimited variable with the approved brief.

```text
Create one photoreal editorial breakfast still life on {TABLE_SURFACE} beside {WINDOW_DESCRIPTION} during {RAIN_AND_TIME}.

Arrange exactly {FOOD_AND_DRINK_MANIFEST} and {TABLEWARE_MANIFEST}. Add only {PROP_MANIFEST}. Place the focal subject at {FOCAL_PLACEMENT} and view the grouping from {CAMERA_VIEW}.

Use {LIGHTING} and {FOCUS_BEHAVIOR}. Render physically plausible food texture, ceramic and glass surfaces, metal, textile fibers, rain droplets, reflections, refraction, steam, crumbs, and contact shadows only where the brief calls for them.

Keep all objects correctly counted, edible, grounded, and consistent with one light direction. No extra food, dish, utensil, flower, book, phone, package, hand, person, logo, label, signature, watermark, or readable text. Additional exclusions: {MUST_AVOID}.

Return one opaque PNG at {PIXEL_SIZE} in {ASPECT_RATIO}, suitable as an editorial Production Candidate after inspection and final QA.
```

## Conversational Profile

Profile ID: `conversational-v1`

1. Submit the completed brief and prompt to a supported conversational image surface.
2. Ask it to identify unresolved counts, preparation details, rights, or camera choices before generation.
3. Resolve them, then request exactly one image.
4. Record the surface, time, displayed model, observable settings, and exact prompt if a run is authorized.
5. Mark hidden metadata `not_exposed`; do not infer it.
6. Inspect the image at full resolution and intended display size.

A conversational output is illustrative unless a conforming evidence record says otherwise.

## GPT Image 2 API Profile

Profile ID: `gpt-image-2-api-v1`

Endpoint: OpenAI Image API, `POST /v1/images/generations`.

```json
{
  "model": "gpt-image-2-2026-04-21",
  "prompt": "<completed portable prompt>",
  "n": 1,
  "size": "1024x1536",
  "quality": "high",
  "background": "opaque",
  "output_format": "png",
  "moderation": "auto"
}
```

Before any provider call, approve the exact run manifest, credential source, spend ceiling, retention policy, output location, and stop condition. Keep blocked and failed runs visible. No API run has been made for this Recipe.

## Critical Invariants

Every candidate must pass all of these:

1. Every declared food, drink, vessel, utensil, textile, and prop appears in the correct quantity.
2. No undeclared object, package, logo, label, person, hand, or readable text appears.
3. Food structure, preparation, moisture, steam, and garnishes are physically plausible.
4. Tableware, utensils, textiles, and glass have coherent geometry and material response.
5. Rain, window, reflections, exterior blur, and interior light describe one weather condition.
6. Every object is grounded and lit by a consistent window and fill setup.
7. Required objects remain inside the frame and reviewable at the declared focal depth.
8. The output is one editorial still life, not a recipe page, collage, restaurant ad, or option sheet.

## Production Candidate Rubric

Mark each criterion `pass` or `fail`. Any failure blocks the full-rubric pass.

| Criterion | Pass condition |
| --- | --- |
| Subject hierarchy | The intended breakfast grouping is immediate and props remain secondary. |
| Food realism | Ingredients, preparation, moisture, steam, and crumbs look edible and specific. |
| Material realism | Ceramic, glass, metal, linen, wood, and water respond credibly. |
| Lighting | Window light, room fill, reflections, and shadows agree. |
| Weather | Rain detail and exterior atmosphere are believable and restrained. |
| Composition | Camera, crop, focal plane, depth, and negative space match the brief. |
| Defect control | No malformed object, fused edge, repetition, halo, or artificial blur distracts. |
| Technical delivery | Pixel size, format, aspect ratio, and opacity match the profile. |

## Inspection and targeted repair

1. Count every food item, vessel, utensil, textile, and prop against the manifests.
2. Inspect food texture, garnish count, steam direction, liquid surfaces, and glass refraction.
3. Trace the window light through highlights, contact shadows, reflections, and exterior droplets.
4. Review rims, handles, spoon geometry, cloth folds, crop, and focal depth at 100 percent.
5. Record all failures before repair.

Repair one defect class at a time:

- Count failure: restate the complete manifest and remove or restore only the failed object.
- Food defect: correct the named texture, slice, garnish, or preparation detail.
- Material defect: repair only the affected vessel, utensil, textile, or surface.
- Lighting conflict: restate the single window direction and preserve composition.
- Focus or crop failure: adjust camera or focal depth without changing the object manifest.

Rescore the entire image after repair. Preserve failed runs when evidence work is authorized.

## Final-QA handoff

Hand off a passing Production Candidate with the brief, Recipe and profile IDs, exact prompt, output checksum, dimensions, invariant and rubric results, failures, repairs, and rights statement. A human owner must separately approve food claims, styling, crop, color, retouching, accessibility text, channel requirements, and publication rights.

## Representative brief

The saved future prompt uses one fictional breakfast on a worn honey-oak table: oatmeal with five pear slices, black coffee in one blue mug, one water tumbler, one linen napkin, one teaspoon, and three loose oat flakes beside a rain-streaked window. It uses a slightly elevated view, cool autumn light, no branding, and a `1024x1536` portrait output.

- [Exact submitted prompt](samples/rainy-window-breakfast-still-life.prompt.txt)

## Rendered Sample

![Oatmeal with pear, coffee, water, napkin, and spoon beside a rain-streaked window](samples/rainy-window-breakfast-still-life.png)

This is one illustrative output generated from the representative brief with the Codex built-in image generation tool on 2026-08-26. Manual review found the five pear slices, vessels, napkin, spoon, wet window, and restrained editorial lighting coherent. The loose-oat garnish appears to exceed the requested three flakes.

- [Exact submitted prompt](samples/rainy-window-breakfast-still-life.prompt.txt)
- [Generation Run record](evidence.json)
- Model, model version, seed, request parameters, and request ID: `not_exposed`
- Output: `1024x1536` PNG
- Promotion evidence: no

This sample is one illustrative built-in-tool output. It does not demonstrate repeatability, GPT Image 2 API conformance, Recipe promotion evidence, a full rubric pass, or publication readiness.

## Rights and provenance boundary

This Recipe is independently authored with source posture `original` and no Source Entry. Use fictional arrangements and project-owned or authorized references, props, products, and locations. Original prompt authorship does not establish rights in inputs or future outputs. A future sample must carry an exact evidence record and cannot count as promotion without the full promotion gate.
