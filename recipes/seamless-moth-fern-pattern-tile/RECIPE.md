# Seamless Moth and Fern Pattern Tile

- Status: Draft
- Record version: 1
- Task family: Seamless surface pattern
- Source posture: Original
- Evidence status: Recorded illustrative built-in-tool sample; promotion evidence: no
- Default outcome: Production Candidate, subject to final QA

This Recipe creates one original square pattern tile from declared moth and fern motifs. It treats opposite-edge continuity, corner resolution, motif count, spacing, palette, and repeat artifacts as inspection targets rather than assuming that a square image is seamless.

## Task fit and non-fit

Use this Recipe when:

- the motifs and rendering treatment are independently specified or authorized;
- one flat square repeat tile is the required output;
- motif counts, palette, scale hierarchy, density, and repeat logic can be frozen;
- the operator can test the output in a multi-tile grid and repair seams.

Do not use it to:

- imitate a named artist, protected textile, specimen plate, brand pattern, or living designer;
- generate a room mockup, fabric photograph, wallpaper roll, or bordered swatch;
- infer scientific species accuracy or licensing from generic motif names;
- claim repeatability from visual inspection of one isolated tile;
- call a generated tile manufacturing-ready without production QA.

## Required Creative Brief inputs

Provide every field before generation:

1. `motif_authority`: confirmation that motifs and references are original or authorized.
2. `moth_manifest`: exact forms, poses, scale classes, and quantities.
3. `fern_manifest`: exact frond types, orientations, scale classes, and quantities.
4. `repeat_logic`: tossed, half-drop, lattice, or another declared structure.
5. `ground_and_palette`: one ground and a closed motif color list.
6. `rendering_style`: independently described line, paint, paper, or vector treatment.
7. `density_and_spacing`: coverage target, clear-space rule, and scale hierarchy.
8. `output`: square pixel size, format, background, and intended repeat test.
9. `must_avoid`: excluded motifs, symbols, layout artifacts, and style references.

Stop if motif rights, counts, repeat logic, or tile dimensions are unresolved.

## Input preparation

1. Freeze both motif manifests and label primary, secondary, and filler scales.
2. Choose one repeat logic and state which motifs may cross each edge.
3. Close the palette and map colors to motifs or motif parts.
4. Remove any instruction to imitate an artist, textile, brand, or specimen plate.
5. Reserve clear space around motif silhouettes and likely edge crossings.
6. Define the required 3-by-3 repeat inspection before generation.
7. Save the brief, exact prompt, Recipe version, and rights confirmation for any future run.

## Portable prompt

Replace every brace-delimited variable with the approved brief.

```text
Create one flat seamless square pattern tile on {GROUND_COLOR}, with no perspective, vignette, border, mockup, or surrounding margin.

Build an original {REPEAT_LOGIC} repeat from exactly {MOTH_MANIFEST} and {FERN_MANIFEST}. Use {PALETTE}, {RENDERING_STYLE}, {SCALE_HIERARCHY}, and {DENSITY_AND_SPACING}.

Continue every motif crossing the left edge precisely onto the right edge, and every motif crossing the top edge precisely onto the bottom edge. Resolve all four corners as one continuous repeat.

No visible seam, central medallion, stripe, grid, border, cast shadow, fabric fold, wallpaper room, extra species, scientific label, signature, logo, watermark, letter, or number. Avoid motif collisions, trapped gaps, edge crowding, repeated clusters, directional dead zones, and copied styling. Additional exclusions: {MUST_AVOID}.

Return one flat opaque {PIXEL_SIZE} square PNG intended for direct edge-to-edge repetition and a 3-by-3 seam test.
```

## Conversational Profile

Profile ID: `conversational-v1`

1. Submit the completed brief and prompt to a supported conversational image surface.
2. Ask it to identify unresolved motif counts, rights, palette, or repeat logic before generation.
3. Resolve them, then request exactly one flat square tile.
4. Record the surface, time, displayed model, settings, and exact prompt if a run is authorized.
5. Mark hidden metadata `not_exposed`; do not infer it.
6. Test the returned tile in a 3-by-3 grid before applying the rubric.

A single isolated image cannot establish a seamless repeat.

## GPT Image 2 API Profile

Profile ID: `gpt-image-2-api-v1`

Endpoint: OpenAI Image API, `POST /v1/images/generations`.

```json
{
  "model": "gpt-image-2-2026-04-21",
  "prompt": "<completed portable prompt>",
  "n": 1,
  "size": "1024x1024",
  "quality": "high",
  "background": "opaque",
  "output_format": "png",
  "moderation": "auto"
}
```

Before any provider call, approve the exact run manifest, credential source, spend ceiling, retention policy, output location, and stop condition. Record blocked and failed requests. No API run has been made for this Recipe.

## Critical Invariants

Every candidate must pass all of these:

1. The output is one flat square tile with no border, margin, perspective, or mockup.
2. Moth and fern forms match the declared manifests and counts.
3. Left and right edges join without a visible discontinuity.
4. Top and bottom edges join without a visible discontinuity.
5. All four corners resolve correctly when tiles meet.
6. Palette, rendering style, scale hierarchy, density, and spacing match the brief.
7. No copied motif, real brand, label, signature, logo, watermark, letter, or number appears.
8. A 3-by-3 test shows no unintended stripe, block, cluster, hole, or directional dead zone.

## Production Candidate Rubric

Mark each criterion `pass` or `fail`. Any failure blocks the full-rubric pass.

| Criterion | Pass condition |
| --- | --- |
| Seam continuity | Every horizontal, vertical, and corner join is visually continuous. |
| Motif fidelity | Forms, counts, poses, and scale classes match both manifests. |
| Distribution | Motifs feel balanced without a central badge or repeated clump. |
| Rhythm | Orientation and spacing avoid unintended rows, stripes, and channels. |
| Palette | Ground and motif colors stay within the closed palette and remain legible. |
| Style coherence | Edge, texture, detail, and simplification are consistent across motifs. |
| Defect control | No collision, tangent, clipped continuation, artifact, or tiny trapped gap distracts. |
| Technical delivery | The file is an opaque square PNG at the declared dimensions. |

## Inspection and targeted repair

1. Count all moth and fern motifs in the source tile.
2. Place the tile in a 3-by-3 grid without gaps, scaling, or overlap.
3. Inspect every vertical join, horizontal join, and four-tile corner at 100 percent.
4. Scan the repeated field for stripes, holes, blocks, mirrored pairs, and dominant clusters.
5. Compare palette, scale hierarchy, density, and rendering style with the brief.
6. Record all failures before repair.

Repair one defect class at a time:

- Edge mismatch: correct only the named crossing and its opposite-edge continuation.
- Corner mismatch: rebuild the affected corner continuation while preserving interior motifs.
- Repetition artifact: reposition the smallest number of motifs needed to break the stripe or cluster.
- Motif defect: redraw only the failed moth or fern and preserve its bounding space.
- Palette drift: remap only the unapproved color without changing layout.

Repeat the complete 3-by-3 inspection after any repair. Preserve failed predecessors when evidence work is authorized.

## Final-QA handoff

Hand off a passing Production Candidate with the brief, Recipe and profile IDs, exact prompt, source-tile checksum, dimensions, a 3-by-3 repeat proof image, invariant and rubric results, failed attempts, repairs, and rights confirmation. A human owner must separately approve color profile, scale, bleed, substrate, print method, manufacturing tolerances, accessibility or labeling needs, and distribution rights.

## Representative brief

The saved future prompt specifies a fictional hand-cut-paper pattern on deep ink blue with six moth motifs, twelve fern motifs, a warm ivory, coral, moss, sage, and dusty-gold palette, moderate open spacing, half-drop logic, and a flat `1024x1024` output. It references no existing textile, artist, or specimen plate.

- [Exact submitted prompt](samples/seamless-moth-fern-pattern-tile.prompt.txt)

## Rendered Sample

![Hand-cut-paper moth and fern pattern tile on a deep ink-blue ground](samples/seamless-moth-fern-pattern-tile.png)

This is one illustrative output generated from the representative brief with the Codex built-in image generation tool on 2026-08-26. A temporary 3-by-3 repeat inspection found continuous-looking joins without an obvious hard seam. Exact source-tile motif counting remains ambiguous because six complete interior moths appear alongside cropped edge continuations.

- [Exact submitted prompt](samples/seamless-moth-fern-pattern-tile.prompt.txt)
- [Generation Run record](evidence.json)
- Model, model version, seed, request parameters, and request ID: `not_exposed`
- Output: `1254x1254` PNG, not the prompt's `1024x1024` target
- Promotion evidence: no

This sample is one illustrative built-in-tool output. It does not demonstrate repeatability, GPT Image 2 API conformance, Recipe promotion evidence, a full rubric pass, production seamlessness, or publication readiness.

## Rights and provenance boundary

This Recipe is independently authored with source posture `original` and no Source Entry. Use independently specified or authorized motifs and do not imitate a named artist, protected pattern, or specimen plate. Original prompt authorship does not establish rights in inputs or future outputs. Any sample must be recorded with exact prompt and asset metadata and remains non-promotional until the promotion gate is met.
