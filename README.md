# Awesome Image Prompts

An English-first library of evidence-backed image-generation Recipes for Creative Operators and agent-native users.

This repository starts with a three-Recipe vertical slice:

- Product advertisement with exact text
- Reference-based product edit
- Structured infographic or diagram

Each Recipe connects a Creative Brief to prompting guidance, GPT Image 2 conversational and API profiles, inspection criteria, repair steps, and evidence status. A successful run produces a Production Candidate, not an automatically publish-ready asset.

## Pilot Recipes

- [Summer Citrus Product Advertisement](recipes/summer-citrus-product-ad/RECIPE.md)
- [Reference Product Environment Edit](recipes/reference-product-environment-edit/RECIPE.md)
- [Structured Concept Infographic](recipes/structured-concept-infographic/RECIPE.md)

## Current status

The three pilot Recipes are drafts with Placeholder Previews. Placeholders explain the intended result but do not claim that a prompt was generated or tested. Promotion requires the recorded evaluation gate described in each Recipe.

No upstream application code, prompt bodies, literal translations, or images are included. Approved upstream entries are retained as pinned links, checksums, attribution, and project-authored public summaries.

## Repository map

```text
catalog.json                         Machine-readable Recipe index
recipes/                             Human and machine Recipe records
sources/                             Pinned provenance records
skills/image-recipe-library/         Canonical agent skill
.agents/skills/                      Codex-compatible discovery path
.claude/skills/                      Claude Code-compatible discovery path
LICENSE                              License for project-authored material
THIRD_PARTY_NOTICES.md               Third-party exclusions and rights boundary
script/check                         Dependency-free validation
```

## Use the library

Human users can start with the Recipe list in [catalog.json](catalog.json), then open the corresponding `RECIPE.md`.

Agent-native users can invoke or allow discovery of the packaged `image-recipe-library` skill. The skill routes to the relevant canonical Recipe without copying the prompt corpus.

## Validate

Run:

```bash
./script/check
```

The command validates the catalog, Recipe metadata, evidence labels, source links, skill frontmatter, and runtime discovery links.

## License and third-party material

Project-authored code, Recipes, documentation, metadata, validation scripts, and packaged-skill material are available under the [MIT License](LICENSE).

Content available through third-party links and future evidence without an explicit item-level rights statement are outside that grant. See [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) for the current boundary.

See [AGENTS.md](AGENTS.md) for repository-specific agent instructions.
