# Agent instructions

These instructions apply to the Awesome Image Prompts repository.

## Purpose

Build a static Prompt Atlas for Creative Operators with quick, copy-ready Prompt Cards and production-oriented Recipes. Keep the Source Archive as provenance infrastructure rather than a third user-facing content layer. Keep the repository useful to humans and agent-native users without adding a website, hosted generator, accounts, billing, or duplicated skill content.

## Read order

Before material changes, read:

1. `README.md`
2. `docs/COVERAGE.md`
3. `docs/PROMPT_CARD_FORMAT.md`
4. `docs/RECIPE_FORMAT.md`
5. `catalog.json`
6. The target content:
   - for a Prompt Card, its single Markdown file under `prompt-cards/<category-id>/`;
   - for a Recipe, its `recipe.json`, `RECIPE.md`, and `evidence.json`.
7. The linked record under `sources/` when `source_record` is not `null`.

## Content boundaries

- Treat each `prompt-cards/<category-id>/<card-id>.md` file as the canonical copy-ready prompt content for one Prompt Card.
- Keep Prompt Card routing metadata in `catalog.json`. Do not add frontmatter, a per-Card JSON record, or an evidence manifest.
- Give every Prompt Card the mandatory headings defined in `docs/PROMPT_CARD_FORMAT.md`.
- Keep each Prompt Card at `sample_status: placeholder` with a visible `Placeholder Preview` until an accepted public derivative and its exact prompt are recorded in the Card. A recorded Card uses `sample_status: rendered` and a `Rendered Sample` section.
- Keep Card sample evidence in the canonical Card Markdown. Do not add a per-Card JSON record or a shared Card evidence manifest.
- Store public Card sample files only under `prompt-cards/<category-id>/samples/<card-id>/`: `<card-id>.webp`, `<card-id>.prompt.txt`, and optional `input-NN-<role>.webp` supporting derivatives.
- Keep rendered Card samples illustrative and non-promotional when provider metadata is hidden. Record unavailable model and request fields as `not_exposed`, use `profile_id: null`, and set `promotion_evidence: false`.
- Treat `RECIPE.md` as the canonical workflow and prompt content for one Recipe.
- Keep `recipe.json` as small machine-readable routing metadata. Do not duplicate full prompts there.
- Keep the packaged skill thin. It routes quick prompting to canonical Prompt Cards and production work to canonical Recipes without copying their prompt text.
- Treat the Source Archive as provenance infrastructure. Distinguish Original, Source Entry, Translation, Attributed Rebuild, and Frozen Source accurately.
- Link upstream images. Do not copy them into this repository without verified item-level permission.
- Label ungenerated material as `Placeholder Preview`. Never present it as a Rendered Sample or evaluation evidence.
- A Production Candidate still requires channel-specific review before it is publish-ready.

## Provider boundary

- Do not run image-generation APIs from validation or installation commands.
- Before provider-connected evaluation, require an exact run manifest, credential source, spend ceiling, retention policy, and stop condition.
- Record failures as well as successful runs.

## Commands

- `./script/check`: run every configured repository validation.

There is no separate build, linter, typecheck, or test suite yet. Add one only when the repository gains behavior that `script/check` cannot validate clearly.

## Change protocol

- Keep changes limited to the requested Prompt Card, Recipe, or shared contract.
- Update `catalog.json` when adding, removing, renaming, or changing routing metadata for a Prompt Card or Recipe.
- Update `prompt-cards/README.md` when adding, removing, or moving a Prompt Card.
- Update the relevant format document and `script/check` together when the Prompt Card or Recipe contract changes.
- Update this `AGENTS.md` when a meaningful agent workflow or repository command changes.
- Preserve source attribution and evidence history.
