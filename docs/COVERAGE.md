# Coverage

Awesome Image Prompts now covers all 13 primary categories with two deliberately different content depths: 65 quick-use Prompt Cards and 16 draft Recipes. It is broader than the original three-Recipe pilot, but it is still smaller by prompt count than the upstream collection.

## Current atlas

| Content or evidence unit         | Current count | What it means                                                                    |
| -------------------------------- | ------------: | -------------------------------------------------------------------------------- |
| Prompt Cards                     |            65 | Five copy-ready, independently authored prompts in each category                 |
| Draft Recipes                    |            16 | Full workflows with intake, profiles, inspection, repair, and evidence status    |
| Categories with Prompt Cards     |         13/13 | Every primary category has quick-use coverage                                    |
| Categories with a Recipe         |         13/13 | Every primary category has at least one production-oriented workflow             |
| Illustrative Recipe outputs      |            16 | One recorded built-in-tool output per Recipe                                     |
| Supporting input assets          |             1 | One project-generated reference used by the existing product-edit Recipe         |
| Promoted Recipes                 |             0 | No Recipe has passed the API promotion gate                                      |
| Recorded GPT Image 2 API runs    |             0 | Built-in-tool samples do not expose the metadata required for API evidence        |

All 65 Prompt Cards have Placeholder Previews. The 13 new Rendered Samples belong to their Recipes and do not turn linked Cards into tested prompts.

## Category map

| Category                      | Cards | Recipes | Covered output types                                                     |
| ----------------------------- | ----: | ------: | ------------------------------------------------------------------------ |
| UI & Interfaces               |     5 |       1 | Mobile screens, desktop dashboard, tablet controls, checkout              |
| Charts & Infographics         |     5 |       2 | Route map, charts, process diagram, timeline, structured explanation      |
| Posters & Typography          |     5 |       1 | Event, film, festival, poem, and letterform posters                       |
| Products & E-commerce         |     5 |       3 | Listing hero, flat lay, colorway grid, callout, packaging, ad, edit       |
| Brand & Logos                 |     5 |       1 | Symbol lockup, emblem, monogram, cover mark, embroidered badge            |
| Architecture & Spaces         |     5 |       1 | Exterior, interior, pavilion, axonometric, transit concept                |
| Photography & Realism         |     5 |       1 | Editorial, studio, lifestyle, documentary, and overhead photography       |
| Illustration & Art            |     5 |       1 | Paper cut, linocut, gouache, ink wash, geometric quilt                    |
| Characters & People           |     5 |       1 | Turnaround, portrait, full-body design, action pose, ensemble              |
| Scenes & Storytelling         |     5 |       1 | Narrative frames, suspense, storyboard, picture-book spread               |
| History & Classical Themes    |     5 |       1 | Reconstruction, mosaic, workshop, trade-route scene, artifact board       |
| Documents & Publishing        |     5 |       1 | Field guide, book cover, zine, program cover, instruction page            |
| Other Use Cases               |     5 |       1 | Seamless pattern, stickers, game tokens, paper craft, coloring page        |

The [Prompt Card index](../prompt-cards/README.md) lists all 65 Cards. The [Recipe index](../skills/image-recipe-library/references/recipe-index.md) routes to all 16 workflows.

## Operation coverage

| Operation                                  | Recipe coverage | Prompt Card coverage and boundary                                       |
| ------------------------------------------ | --------------- | ----------------------------------------------------------------------- |
| Generate from a structured text brief      | 15 Recipes      | Broad coverage across all categories                                    |
| Edit one authorized reference image        | 1 Recipe        | One product colorway Card also accepts a reference image                |
| Sketch-guided generation                   | No Recipe       | Three Cards accept an authorized sketch, without preservation evidence  |
| Multi-image composition                    | No Recipe       | Not claimed in the first wave                                           |
| General object removal or inpainting       | No Recipe       | Existing product edit is narrower and environment-specific              |
| Character continuity across several images | No Recipe       | Character Card and Recipe cover one sheet, not a multi-run continuity set |
| Exact text and dense layouts               | 8 Recipes       | Several Cards include text, but only Recipes define invariant checks    |
| Seamless tiling                            | 1 Recipe        | One Card and Recipe cover a square repeat                               |

Prompt Card breadth does not imply Recipe-level reliability. Tasks involving real people, real brands, private inputs, factual claims, safety-critical instructions, or exact preservation still require authorization and task-specific review.

## Breadth compared with the upstream collection

The two repositories use different content units. An upstream case is primarily a prompt and example image. A Prompt Card is an independently authored copy-ready prompt with constraints and a visible preview state. A Recipe is a full workflow with evidence boundaries. The rows below compare the nearest layers without treating them as equivalent.

Snapshot taken 2026-08-26:

| Layer or facet                         | Awesome Image Prompts             | Upstream `awesome-gpt-image-2` |
| -------------------------------------- | --------------------------------: | -----------------------------: |
| Source or case layer                   |                  3 Source Entries |       535 prompt-bearing cases |
| Quick prompt layer                     |                 65 Prompt Cards   |       535 prompt-bearing cases |
| Workflow or template layer             |                 16 draft Recipes  |        22 structured templates |
| Primary categories with quick prompts  |                            13/13   |                          13/13 |
| Primary categories with workflows      |                            13/13   |         Not directly comparable |
| Formal style facets                    |           Tags, no fixed taxonomy  |                        19 tags |
| Formal scene or context facets         |           Tags, no fixed taxonomy  |                        10 tags |

The upstream snapshot is commit [`9a7b2e9`](https://github.com/freestylefly/awesome-gpt-image-2/commit/9a7b2e9c39f816d6c699c2a133e11b6d8bfdc464). Its case IDs run through 538, but three numbered images have no prompt record, so the comparable prompt-case count is 535. See its [category overview](https://github.com/freestylefly/awesome-gpt-image-2/blob/9a7b2e9c39f816d6c699c2a133e11b6d8bfdc464/README.md#L76-L233) and [structured template index](https://github.com/freestylefly/awesome-gpt-image-2/blob/9a7b2e9c39f816d6c699c2a133e11b6d8bfdc464/agents/skills/gpt-image-2-style-library/references/style-library.md#L13-L608).

The repository now matches the upstream category breadth, but not its prompt count. The tradeoff is intentional: each Card is newly authored and rights-bounded, while each Recipe adds more workflow depth than a gallery prompt.

## Evidence status

Every Recipe declares a conversational profile and a pinned GPT Image 2 API profile. The recorded images came from a built-in image tool whose exact model and request settings were not exposed. Each run stores its exact submitted prompt, local PNG, checksum, dimensions, inspection notes, and rights statement, with `promotion_evidence: false`.

`recorded` means the run is inspectable. It does not mean the Recipe is a full rubric pass, repeatable, API-conformant, promoted, or publish-ready. Several retained samples disclose exact-count, topology, or requested-dimension misses in their run records. Promotion still requires four scored GPT Image 2 API runs across two materially different briefs plus one conversational smoke run.
