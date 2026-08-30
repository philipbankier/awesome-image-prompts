# Coverage

Awesome Image Prompts covers all 13 primary categories at two depths: 541 quick-use Prompt Cards and 16 draft Recipes. The Card corpus matches the pinned upstream snapshot in total prompt count and per-category distribution. The content is independently authored, so this is numeric and category parity, not a claim of one-to-one prompts, equal image evidence, or equal workflow coverage.

## Current atlas

| Content or evidence unit      | Current count | What it means                                                              |
| ----------------------------- | ------------: | -------------------------------------------------------------------------- |
| Prompt Cards                  |           541 | Copy-ready, independently authored prompts across all categories           |
| Text-only Prompt Cards        |           430 | Cards that need no image or sketch input                                   |
| Reference-image Prompt Cards  |            46 | Cards that accept a rights-cleared reference image                         |
| Multi-image Prompt Cards      |            33 | Cards that accept a rights-cleared image set with per-source roles         |
| Sketch-guided Prompt Cards    |            33 | Cards that accept a rights-cleared sketch                                  |
| Draft Recipes                 |            16 | Workflows with intake, profiles, inspection, repair, and evidence status   |
| Categories with Prompt Cards  |         13/13 | Every primary category has quick-use coverage                              |
| Categories with a Recipe      |         13/13 | Every primary category has at least one production-oriented workflow       |
| Illustrative Recipe outputs   |            16 | One recorded built-in-tool output per Recipe                               |
| Supporting input assets       |             1 | One project-generated reference used by the product-edit Recipe            |
| Promoted Recipes              |             0 | No Recipe has passed the API promotion gate                                |
| Recorded GPT Image 2 API runs |             0 | Built-in-tool samples do not expose the metadata required for API evidence |

All 541 Prompt Cards have Placeholder Previews. The 16 Rendered Samples belong to their Recipes and do not turn linked Cards into tested prompts.

Input-mode counts are not mutually exclusive: one Card accepts either a reference image or a sketch, and some declared modes are optional. Each Card's Required inputs section is authoritative for its intake logic.

## Category map

| Category                   | Cards | Recipes | Covered output families                                                                            |
| -------------------------- | ----: | ------: | -------------------------------------------------------------------------------------------------- |
| UI & Interfaces            |    73 |       1 | Mobile, tablet, desktop, kiosk, dashboard, booking, review, and control views                      |
| Charts & Infographics      |    53 |       2 | Charts, maps, timelines, processes, comparisons, scales, and explainers                            |
| Posters & Typography       |    90 |       1 | Events, notices, campaigns, specimens, schedules, and typographic studies                          |
| Products & E-commerce      |    42 |       3 | Listing, catalog, packaging, comparison, edit, bundle, and collectible imagery                     |
| Brand & Logos              |    27 |       1 | Marks, identity systems, touchpoints, signage, campaigns, and brand architecture                   |
| Architecture & Spaces      |    12 |       1 | Exterior, interior, adaptive reuse, landscape, modular, and public-space concepts                  |
| Photography & Realism      |    78 |       1 | Editorial, studio, documentary-style, macro, landscape, object, and interior work                  |
| Illustration & Art         |    59 |       1 | Print, paint, collage, diagrammatic, textile, editorial, and narrative media                       |
| Characters & People        |    31 |       1 | Portraits, sheets, ensembles, costumes, actions, expressions, and identity-safe edits              |
| Scenes & Storytelling      |    21 |       1 | Narrative frames, cinematic scenes, suspense, triptychs, comics, and picture-book work             |
| History & Classical Themes |    16 |       1 | Reconstruction, material culture, public-domain interpretation, and museum views                   |
| Documents & Publishing     |    11 |       1 | Covers, spreads, guides, programs, instructions, editorial systems, and layouts                    |
| Other Use Cases            |    28 |       1 | Patterns, craft sheets, game assets, restoration, removal, outpainting, AR, and multi-image boards |

The [Prompt Card index](../prompt-cards/README.md) lists all 541 Cards. The [Recipe index](../skills/image-recipe-library/references/recipe-index.md) routes to all 16 workflows.

## Operation coverage

| Operation                                  | Recipe coverage | Prompt Card coverage and boundary                                                  |
| ------------------------------------------ | --------------- | ---------------------------------------------------------------------------------- |
| Generate from a structured text brief      | 15 Recipes      | 430 text-only Cards, with text briefs also present in every non-text Card          |
| Reference-led generation or editing        | 1 Recipe        | 46 Cards support reference-image mode, preservation scope, and input rights status |
| Sketch-guided generation                   | No Recipe       | 33 Cards support sketch input; the Card defines whether it is required or optional |
| Multi-image composition                    | No Recipe       | 33 Cards support an image set with declared source roles and rights status         |
| General object removal or inpainting       | No Recipe       | One bounded object-removal Card, with no reliability evidence                      |
| Character continuity across several images | No Recipe       | Character sheets and reference sets do not establish multi-run continuity          |
| Exact text and dense layouts               | 8 Recipes       | Many Cards declare exact-copy manifests, but only Recipes define invariant checks  |
| Seamless tiling                            | 1 Recipe        | One Card and Recipe cover a square repeat                                          |

Prompt Card breadth does not imply Recipe-level reliability. Tasks involving real people, real brands, private inputs, factual claims, safety-critical instructions, or exact preservation still require authorization and task-specific review.

## Breadth compared with the upstream collection

The two repositories use different content units. An upstream case is a prompt record paired with an example-image path. A Prompt Card is an independently authored copy-ready prompt with constraints and an explicit evidence state. A Recipe is a deeper workflow. The rows below compare the nearest layers without treating them as equivalent.

Snapshot taken 2026-08-30:

| Layer or facet                     |                        Awesome Image Prompts |     Upstream `awesome-gpt-image-2` |
| ---------------------------------- | -------------------------------------------: | ---------------------------------: |
| Quick prompt records               |                             541 Prompt Cards |                          541 cases |
| Per-category prompt distribution   | Exact numeric match across all 13 categories |       Exact reference distribution |
| Card or case example-image records |                     0 Card-level generations |         541 cases with image paths |
| Deeper workflow layer              |                             16 draft Recipes | 22 packaged-skill template records |
| Primary categories                 |                                        13/13 |                              13/13 |
| Formal style facets                |                      Tags, no fixed taxonomy |                          19 styles |
| Formal scene or context facets     |                      Tags, no fixed taxonomy |                          10 scenes |
| Deeper illustrative outputs        |                      16 Recipe-owned samples |            Not directly comparable |

The upstream snapshot is commit [`c7d2939`](https://github.com/freestylefly/awesome-gpt-image-2/commit/c7d293963b21c60bf338003915438cc5c39dd3ca). Its machine-readable corpus declares 541 cases, 13 categories, 19 styles, and 10 scenes. Its packaged-skill [template index](https://github.com/freestylefly/awesome-gpt-image-2/blob/c7d293963b21c60bf338003915438cc5c39dd3ca/agents/skills/gpt-image-2-style-library/references/style-library.md#template-index) contains 22 records. See the pinned [`cases.json`](https://github.com/freestylefly/awesome-gpt-image-2/blob/c7d293963b21c60bf338003915438cc5c39dd3ca/data/cases.json) for the corpus counts and the separate [template collection](https://github.com/freestylefly/awesome-gpt-image-2/blob/c7d293963b21c60bf338003915438cc5c39dd3ca/docs/templates.md) for its human-facing examples.

This repository now matches the upstream prompt corpus numerically and by category count. It does not yet match the upstream gallery's Card-level visual examples, 22-record packaged-skill template layer, or fixed style and scene facets. Those are separate gaps rather than hidden inside the 541-Card claim.

## Evidence status

Every Recipe declares a conversational profile and a pinned GPT Image 2 API profile. The recorded images came from a built-in image tool whose exact model and request settings were not exposed. Each run stores its exact submitted prompt, local PNG, checksum, dimensions, inspection notes, and rights statement, with `promotion_evidence: false`.

`recorded` means the run is inspectable. It does not mean the Recipe is a full rubric pass, repeatable, API-conformant, promoted, or publish-ready. Several retained samples disclose exact-count, topology, or requested-dimension misses in their run records. Promotion still requires four scored GPT Image 2 API runs across two materially different briefs plus one conversational smoke run.
