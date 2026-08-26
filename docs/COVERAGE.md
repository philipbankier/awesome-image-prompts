# Coverage

Awesome Image Prompts currently favors detailed, inspectable workflows over a large prompt count. This page records what the library contains today and separates Recipe depth from gallery breadth.

## Current workflows

| Mapped upstream category | Task family              | Input mode                                              | Intended passing outcome                                                        |
| ------------------------ | ------------------------ | ------------------------------------------------------- | ------------------------------------------------------------------------------- |
| Products & E-commerce    | `product-advertisement`  | Structured text brief                                   | One fictional or authorized citrus-beverage Production Candidate                |
| Products & E-commerce    | `reference-based-edit`   | One authorized product image plus edit instructions     | One perfume-bottle environment edit that preserves product identity             |
| Charts & Infographics    | `structured-infographic` | Approved facts, labels, relationships, and visual rules  | One bounded educational Production Candidate                                    |

The library currently contains:

- three draft Recipe task families;
- three task families mapped to two upstream primary categories;
- two text-to-image workflows and one single-image edit workflow;
- three illustrative Recipe outputs and one project-generated supporting input;
- zero promoted Recipes and zero recorded GPT Image 2 API runs.

Every Recipe declares a conversational profile and a pinned GPT Image 2 API profile. The current recorded samples came from a built-in image tool whose exact model and request settings were not exposed, so they are illustrative rather than promotion evidence.

## Breadth compared with the upstream collection

The two repositories use different content units. An upstream case is a prompt and example image. A Recipe here is an end-to-end workflow with intake, rights checks, execution profiles, inspection, repair, and evidence. The counts below compare breadth, not quality or completeness of individual entries.

Snapshot taken 2026-08-26:

| Layer or facet                          | Awesome Image Prompts       | Upstream `awesome-gpt-image-2` |
| --------------------------------------- | --------------------------: | -----------------------------: |
| Source or case layer                    |            3 Source Entries |       535 prompt-bearing cases |
| Workflow or template layer              |             3 draft Recipes |        22 structured templates |
| Primary categories with mapped Recipes  |                           2 |                             13 |
| Style facets                            |          No formal taxonomy |                        19 tags |
| Scene or context facets                 |          No formal taxonomy |                        10 tags |

Source Entries, prompt cases, Recipes, and templates are not equivalent units. The paired rows show the nearest layer-level comparison without claiming parity.

The upstream snapshot is commit [`9a7b2e9`](https://github.com/freestylefly/awesome-gpt-image-2/commit/9a7b2e9c39f816d6c699c2a133e11b6d8bfdc464). Its case IDs run through 538, but three numbered images have no prompt record, so the comparable prompt-case count is 535. See its [category overview](https://github.com/freestylefly/awesome-gpt-image-2/blob/9a7b2e9c39f816d6c699c2a133e11b6d8bfdc464/README.md#L76-L233) and [structured template index](https://github.com/freestylefly/awesome-gpt-image-2/blob/9a7b2e9c39f816d6c699c2a133e11b6d8bfdc464/agents/skills/gpt-image-2-style-library/references/style-library.md#L13-L608).

This breadth snapshot follows newer upstream activity. The three Recipe provenance records remain pinned to [`de6a8ad`](https://github.com/freestylefly/awesome-gpt-image-2/commit/de6a8ad89b6308dc49b316fcd9f7a56bf2a73273); the comparison does not update those source pins.

## Category map

The category names below mirror the upstream taxonomy only to make breadth comparable. They are not additional fields in this repository's Recipe schema.

| Upstream category             | Upstream cases | Recipes mapped here                                                    |
| ----------------------------- | -------------: | ---------------------------------------------------------------------- |
| UI & Interfaces               |             73 | No current Recipe                                                      |
| Charts & Infographics         |             52 | One structured-infographic Recipe                                      |
| Posters & Typography          |             88 | No current Recipe                                                      |
| Products & E-commerce         |             41 | One product-advertisement Recipe and one reference-edit Recipe         |
| Brand & Logos                 |             27 | No current Recipe                                                      |
| Architecture & Spaces         |             12 | No current Recipe                                                      |
| Photography & Realism         |             78 | No general-purpose Recipe                                               |
| Illustration & Art            |             58 | No current Recipe                                                      |
| Characters & People           |             31 | No current Recipe                                                      |
| Scenes & Storytelling         |             21 | No current Recipe                                                      |
| History & Classical Themes    |             16 | No current Recipe                                                      |
| Documents & Publishing        |             10 | No current Recipe                                                      |
| Other Use Cases               |             28 | No current Recipe                                                      |

## Operation coverage

| Operation                                   | Recipe status      | Current boundary                                            |
| ------------------------------------------- | ------------------ | ----------------------------------------------------------- |
| Generate from a structured text brief       | Two draft Recipes  | Product advertisement and structured infographic only       |
| Edit one authorized reference image         | One draft Recipe   | Environment-only edit of one perfume bottle                 |
| Multi-image composition                     | No Recipe          | No task-specific evaluation criteria yet                    |
| General inpainting or object removal        | No Recipe          | The reference edit has a narrower preservation contract     |
| Character consistency or identity transfer | No Recipe          | No task-specific evaluation criteria yet                    |
| Reusable style and scene lookup             | No Recipe          | No formal style or scene taxonomy yet                       |

A Source Entry adds Source Archive breadth but not Recipe or operation coverage. Recipe coverage expands only when a task has declared fit, inputs, execution profiles, Critical Invariants, repair guidance, and evidence status.
