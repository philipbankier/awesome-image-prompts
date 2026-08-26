# Awesome Image Prompts

English-first, evidence-tracked image-generation workflows for product ads, reference edits, and structured infographics.

Each Recipe turns a Creative Brief into a complete generation workflow: prepared inputs, an adaptable prompt, GPT Image 2 conversational and API profiles, pass/fail checks, targeted repair guidance, and an evidence record. This is a working library for Creative Operators and agent-native users, not a dump of prompt snippets.

> Early pilot: all three Recipes are drafts. The images below are real single-run outputs from the Codex built-in image generation tool. They are not GPT Image 2 API results, repeatability evidence, promoted Recipes, or automatically publish-ready assets. The exact model and hidden request settings were not exposed.

> Looking for more? [PromptCache](https://promptcache.live/) is a free prompt discovery tool with image, video, text, flow, and skill prompts, plus practical tips and tricks.

## Recipes and rendered samples

| Product advertisement | Reference product edit | Structured infographic |
| :---: | :---: | :---: |
| [![CITRA SUN sparkling citrus drink advertisement](recipes/summer-citrus-product-ad/samples/citra-sun.png)](recipes/summer-citrus-product-ad/RECIPE.md) | [![FIELD NOTE perfume bottle after an environment edit](recipes/reference-product-environment-edit/samples/field-note-environment-edit.png)](recipes/reference-product-environment-edit/RECIPE.md) | [![Bayes theorem infographic about the flagged group](recipes/structured-concept-infographic/samples/bayes-flagged-group.png)](recipes/structured-concept-infographic/RECIPE.md) |
| Exact display text, product geometry, art direction, inspection, and repair. | Preserve an authorized product while changing only its environment. | Turn approved facts and relationships into one bounded visual explanation. |
| [Open Recipe](recipes/summer-citrus-product-ad/RECIPE.md) · [Run record](recipes/summer-citrus-product-ad/evidence.json) | [Open Recipe](recipes/reference-product-environment-edit/RECIPE.md) · [Run records](recipes/reference-product-environment-edit/evidence.json) | [Open Recipe](recipes/structured-concept-infographic/RECIPE.md) · [Run record](recipes/structured-concept-infographic/evidence.json) |

## Reference edit before and after

| Project-generated reference | Environment edit |
| :---: | :---: |
| ![Fictional FIELD NOTE perfume bottle on a neutral studio background](recipes/reference-product-environment-edit/samples/field-note-reference.png) | ![The same FIELD NOTE bottle on limestone with a cobalt arc and oat stems](recipes/reference-product-environment-edit/samples/field-note-environment-edit.png) |

The reference is fictional and project-generated. The edit preserves one oval amber bottle, its rectangular cap, cream label, and exact `FIELD NOTE / 01` text while replacing the surrounding set. See the [input and edit records](recipes/reference-product-environment-edit/evidence.json).

## What a Recipe contains

Every Recipe defines:

1. Task fit and the cases it should reject.
2. Required Creative Brief fields and rights checks.
3. A portable prompt with no unresolved decisions hidden inside it.
4. Conversational and GPT Image 2 API execution profiles.
5. Critical Invariants that block a candidate when they fail.
6. A Production Candidate Rubric for quality review.
7. Targeted repair steps that preserve failed runs.
8. A final-QA handoff and a linked evidence manifest.

Start with one of the three Recipes above. The [machine-readable catalog](catalog.json) is intended for tools and agents.

## Use with an agent

The canonical [`image-recipe-library` skill](skills/image-recipe-library/SKILL.md) selects the narrowest matching Recipe and loads its guidance progressively. It links to canonical Recipe files instead of duplicating their prompts.

This repository includes discovery links for:

- Codex-style hosts: [`.agents/skills/image-recipe-library`](.agents/skills/image-recipe-library)
- Claude Code-style hosts: [`.claude/skills/image-recipe-library`](.claude/skills/image-recipe-library)

Host discovery and tool behavior still require independent validation. The shared skill layout alone is not a compatibility guarantee.

## Evidence status

| Recipe | Recorded sample | Promotion status |
| --- | --- | --- |
| [Summer Citrus Product Advertisement](recipes/summer-citrus-product-ad/RECIPE.md) | One illustrative built-in-tool run | Draft, not promoted |
| [Reference Product Environment Edit](recipes/reference-product-environment-edit/RECIPE.md) | One supporting-input run and one illustrative edit | Draft, not promoted |
| [Structured Concept Infographic](recipes/structured-concept-infographic/RECIPE.md) | One illustrative built-in-tool run | Draft, not promoted |

`recorded` means an output resolves to an exact prompt, local asset, checksum, dimensions, inspection notes, and rights statement. It does not mean the Recipe passed promotion.

Promotion requires four scored GPT Image 2 API runs across two materially different briefs, all Critical Invariants passing, at least three full-rubric passes, and one additional conversational smoke run. None of the current samples count toward that gate.

See the [Recipe and evidence format](docs/RECIPE_FORMAT.md) for the record contract.

## Repository structure

```text
catalog.json                         Machine-readable Recipe index
recipes/<recipe-id>/RECIPE.md        Canonical workflow and prompt
recipes/<recipe-id>/recipe.json      Small routing record
recipes/<recipe-id>/evidence.json    Run metadata and evidence status
recipes/<recipe-id>/samples/         Recorded prompts and local outputs
sources/                             Pinned provenance records
skills/image-recipe-library/         Canonical agent skill
.agents/skills/                      Codex-style discovery path
.claude/skills/                      Claude Code-style discovery path
LICENSE                              License for project-authored material
THIRD_PARTY_NOTICES.md               Third-party and evidence rights boundary
script/check                         Dependency-free validation
```

## Validate

Run:

```bash
./script/check
```

The command validates the catalog, Recipe metadata, evidence records, sample assets and checksums, local links, skill frontmatter, and runtime discovery links.

## Provenance and license

No upstream application code, prompt bodies, literal translations, or images are bundled. Approved upstream entries remain pinned links, checksums, attribution, and project-authored public summaries under [`sources/`](sources/).

Shoutout to the original [freestylefly/awesome-gpt-image-2](https://github.com/freestylefly/awesome-gpt-image-2), whose collection inspired this independently authored English-first library.

Project-authored code, Recipes, documentation, metadata, validation scripts, skill material, and expressly identified sample rights are covered by the [MIT License](LICENSE). Third-party links and any material without an item-level rights grant remain outside that license. See [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).

See [AGENTS.md](AGENTS.md) for repository-specific agent instructions.
