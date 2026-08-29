# Courtyard Micro-Library

- Status: Draft
- Record version: 1
- Task family: Architectural exterior visualization
- Source posture: Original
- Evidence status: Recorded illustrative built-in-tool sample; promotion evidence: no
- Default outcome: Production Candidate, subject to final QA

This Recipe turns a bounded civic brief into one exterior visualization of a compact public library organized around a courtyard. It tests program visibility, accessible circulation, structural plausibility, climate fit, and public character without claiming buildability.

## Task fit and non-fit

Use this Recipe when:

- the project is fictional or the operator is authorized to visualize it;
- one small public library and its courtyard must read in one exterior frame;
- program, entry, circulation, material, planting, and site conditions can be declared;
- the output is a concept visualization for review, not a technical document.

Do not use it to:

- copy a recognizable building or imitate a named living architect;
- replace licensed architectural, structural, civil, accessibility, fire, or landscape design;
- infer dimensions, code compliance, occupancy, drainage capacity, or construction details;
- show several design options in one sheet;
- call an image buildable or publish-ready without qualified review.

## Required Creative Brief inputs

Provide every field before generation:

1. `site_authority`: fictional status or authorization to use the project and references.
2. `site_context`: climate, terrain, street edge, neighboring scale, and orientation.
3. `footprint_and_height`: approximate enclosed area, courtyard size, and story count.
4. `program_manifest`: exact public, staff, storage, and service spaces.
5. `circulation`: step-free route, entry, courtyard access, and exit relationships.
6. `structure_and_materials`: plausible wall, roof, support, glazing, and finish system.
7. `courtyard_and_planting`: surfaces, shade, drainage intent, and climate-appropriate plants.
8. `scene_direction`: time, weather, camera, figures, and surrounding context.
9. `output`: aspect ratio, dimensions, background behavior, and format.
10. `must_avoid`: project-specific exclusions and prohibited claims.

Stop if authority, entry, circulation, program, or site context is unresolved.

## Input preparation

1. Reduce the program to a closed room and outdoor-space manifest.
2. Trace one step-free path from public edge to every required public space.
3. Choose a courtyard geometry that fits the footprint and does not trap circulation.
4. Map roof spans and supports before adding expressive form.
5. Assign a short material palette and climate-appropriate planting list.
6. Choose a camera that shows the street edge, entrance, and courtyard relationship.
7. Save the approved brief, prompt, Recipe version, and rights confirmation for any future run.

## Portable prompt

Replace every brace-delimited variable with the approved brief.

```text
Create one exterior architectural visualization of a compact public micro-library on {SITE_CONTEXT} during {TIME_AND_WEATHER}.

Design a {HEIGHT_AND_FOOTPRINT} building around {COURTYARD}. Include exactly {PROGRAM_MANIFEST}. Show one obvious step-free entrance and this continuous public route: {CIRCULATION}.

Use {STRUCTURE_AND_MATERIALS}, {GLAZING_AND_SHADE}, and {PLANTING}. Keep roof spans, supports, thresholds, drainage, guard conditions, and human scale plausible. Place only {FIGURE_MANIFEST} for scale.

View the project from {CAMERA_VIEW}. Keep the building, entrance, courtyard relationship, and public use legible in one frame.

No second design, copied landmark, named-architect imitation, impossible cantilever, floating roof, blocked door, inaccessible step, sealed courtyard, luxury-resort cues, cars, crowds, brand sign, logo, caption, watermark, or unapproved text. Additional exclusions: {MUST_AVOID}.

Return one opaque PNG at {PIXEL_SIZE} in {ASPECT_RATIO}. Treat it as a concept visualization, not a technical or compliance document.
```

## Conversational Profile

Profile ID: `conversational-v1`

1. Submit the completed brief and prompt to a supported conversational image surface.
2. Ask for unresolved program, circulation, rights, or camera fields before generation.
3. Resolve them, then request exactly one exterior image.
4. Record the surface, time, displayed model, settings, and submitted prompt if a run is authorized.
5. Mark hidden metadata `not_exposed`; do not infer it.
6. Inspect against every invariant before scoring atmosphere or style.

A conversational sample cannot establish code, buildability, accessibility, or Recipe promotion.

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

Before any provider call, approve the exact run manifest, credential source, spend ceiling, retention policy, output location, and stop condition. Record blocked and failed requests. No API run has been made for this Recipe.

## Critical Invariants

Every candidate must pass all of these:

1. Exactly one micro-library design appears.
2. The declared footprint, height, courtyard, and program remain mutually plausible.
3. The entrance is visible and a step-free public route can be traced through required public spaces.
4. Courtyard access is clear and planting does not block doors, glazing, or circulation.
5. Roofs, walls, spans, supports, thresholds, and guard conditions are visually plausible.
6. Materials, planting, light, weather, and ground conditions fit the declared climate and site.
7. No unapproved signage, logo, claim, caption, signature, or watermark appears.
8. The output reads as one exterior concept visualization, not a plan, collage, or option board.

## Production Candidate Rubric

Mark each criterion `pass` or `fail`. Any failure blocks the full-rubric pass.

| Criterion | Pass condition |
| --- | --- |
| Civic legibility | Entrance, library use, and courtyard relationship are understandable at first scan. |
| Program fit | Every requested space is represented without invented major program. |
| Circulation | Public route and courtyard access are coherent and unobstructed. |
| Structural plausibility | Supports, spans, roof thickness, openings, and edges form a believable system. |
| Site and climate | Ground, weather, shade, planting, and envelope fit the brief. |
| Human scale | Doors, windows, furniture, figures, and planting agree in scale. |
| Composition | Camera and crop show the required relationships with useful depth. |
| Finish quality | No warped edges, merged materials, repeated figures, or visual artifacts distract. |

## Inspection and targeted repair

1. Trace the route from street edge to entrance, reading room, courtyard, and required services.
2. Locate every program item and compare it with the manifest.
3. Trace roof loads visually to walls or columns and inspect openings and thresholds.
4. Check planting, shade, drainage cues, weather, material scale, and figure scale.
5. Record all failures before repair.

Repair one defect class at a time:

- Missing program: restore only the named space without redesigning accepted areas.
- Circulation failure: reopen or reposition the blocked segment and preserve the program.
- Structural drift: add or correct the necessary support while preserving footprint and camera.
- Climate mismatch: replace only the failed planting, material, or weather element.
- Camera failure: reposition the view to reveal the entrance and courtyard without changing the design.

Rescore the whole candidate after repair. A corrected view does not inherit earlier passes.

## Final-QA handoff

Hand off a passing Production Candidate with the approved brief, Recipe and profile IDs, exact prompt, output checksum, dimensions, invariant and rubric results, failed attempts, repairs, and rights confirmation. Qualified owners must separately review planning, accessibility, life safety, structure, drainage, landscape suitability, public claims, captioning, and distribution rights.

## Representative brief

The saved future prompt describes a fictional 145-square-meter, single-story neighborhood micro-library around a 7-by-9-meter planted courtyard, with reclaimed brick, timber beams, bronze frames, one step-free public route, a bright overcast spring setting, and a pedestrian-height `1536x1024` exterior view. It does not use a real site or architect.

- [Exact submitted prompt](samples/courtyard-micro-library.prompt.txt)

## Rendered Sample

![Fictional low-rise micro-library organized around a planted courtyard on a wet spring day](samples/courtyard-micro-library.png)

This is one illustrative output generated from the representative brief with the Codex built-in image generation tool on 2026-08-26. Manual review found a coherent entrance, courtyard route, glazed reading program, supported roofs, and planted civic scale. Five figures are visible because the rendering added a reception figure beyond the prompt's exact four-figure instruction.

- [Exact submitted prompt](samples/courtyard-micro-library.prompt.txt)
- [Generation Run record](evidence.json)
- Model, model version, seed, request parameters, and request ID: `not_exposed`
- Output: `1536x1024` PNG
- Promotion evidence: no

This sample is one illustrative built-in-tool output. It does not demonstrate repeatability, GPT Image 2 API conformance, Recipe promotion evidence, a full rubric pass, buildability, or publication readiness.

## Rights and provenance boundary

This Recipe is independently authored with source posture `original` and no Source Entry. Use fictional sites or authorized project data and references. Do not imitate a named living architect or reuse protected plans. Original prompt authorship does not establish rights in inputs or future outputs, and no generated image may be described as promotion evidence without a conforming run record.
