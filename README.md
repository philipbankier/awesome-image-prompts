# Awesome Image Prompts

Reusable, evidence-tracked workflows for generating and editing images.

Each Recipe turns a structured Creative Brief into an end-to-end workflow: prepared inputs, an adaptable prompt, conversational and API execution profiles, pass/fail checks, targeted repair guidance, and a linked run record. It is built for people and agents who need more than a one-shot prompt.

> Pilot status: all three Recipes are drafts. The images below are real single-run outputs from the Codex built-in image generation tool. They are not GPT Image 2 API results, repeatability evidence, promoted Recipes, or automatically publish-ready assets. The exact model and hidden request settings were not exposed.

## Start here

1. Choose the narrowest matching Recipe from the Current coverage section.
2. Complete its Required Creative Brief, including any required rights and exact-text fields.
3. Confirm authority for the exact provider action and inputs.
4. Use the conversational profile. Use the API profile only after satisfying the exact [provider boundary](AGENTS.md#provider-boundary) for that run.
5. Check the output against the Critical Invariants and rubric, then repair or reject it before final QA.

## Current coverage

- Generate one fictional or authorized citrus-beverage advertisement from a structured brief.
- Edit one authorized perfume-bottle reference while preserving the product and replacing only its environment.
- Generate one bounded mathematical, technical, scientific, or process infographic from approved facts.

These three detailed draft workflows map to two of the upstream collection's 13 primary categories: Products & E-commerce and Charts & Infographics. The pilot is not yet as broad as the upstream collection. See [Coverage](docs/COVERAGE.md) for the exact input and output modes, current gaps, and a dated comparison.

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

The [machine-readable catalog](catalog.json) routes tools and agents to the same canonical Recipe files.

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

See the [Recipe format](docs/RECIPE_FORMAT.md) for the record and evidence contract.

## Source archive and provenance

Each Recipe links to a pinned Source Entry that records provenance without bundling upstream prompt bodies, literal translations of those bodies, or images. The current Source Archive contains:

- [case 237](sources/case-237.md), design evidence for the product-advertisement Recipe.
- [case 519](sources/case-519.md), design evidence for the reference-edit Recipe.
- [case 341](sources/case-341.md), an external Frozen Source reference for the infographic Recipe.

These records document the origins of the three current Recipes. They do not add more mapped Recipe categories, endorse the linked material, or count as generation evidence.

## Repository structure

```text
catalog.json                         Machine-readable Recipe index
recipes/<recipe-id>/RECIPE.md        Canonical workflow and prompt
recipes/<recipe-id>/recipe.json      Small routing record
recipes/<recipe-id>/evidence.json    Run metadata and evidence status
recipes/<recipe-id>/samples/         Recorded prompts and local outputs
sources/                             Pinned provenance records
docs/                                Coverage and record-format documentation
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

## Related resources

- [PromptCache](https://promptcache.live/) is a free prompt discovery tool with image, video, text, flow, and skill prompts, plus practical tips and tricks.
- This independently authored library was inspired by the original [freestylefly/awesome-gpt-image-2](https://github.com/freestylefly/awesome-gpt-image-2) collection.

## License

Project-authored code, Recipes, documentation, metadata, validation scripts, skill material, and expressly identified sample rights are covered by the [MIT License](LICENSE). Third-party links and any material without an item-level rights grant remain outside that license. See [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).

See [AGENTS.md](AGENTS.md) for repository-specific agent instructions.
