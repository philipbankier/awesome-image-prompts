# Agent instructions

These instructions apply to the Awesome Image Prompts repository.

## Purpose

Build a static Recipe Library and Source Archive for Creative Operators. Keep the repository useful to humans and agent-native users without adding a website, hosted generator, accounts, billing, or duplicated skill content.

## Read order

Before material changes, read:

1. `README.md`
2. `docs/COVERAGE.md`
3. `docs/RECIPE_FORMAT.md`
4. `catalog.json`
5. The target Recipe's `recipe.json`, `RECIPE.md`, and `evidence.json`
6. The linked record under `sources/`

## Content boundaries

- Treat `RECIPE.md` as the canonical workflow and prompt content for one Recipe.
- Keep `recipe.json` as small machine-readable routing metadata. Do not duplicate full prompts there.
- Keep the packaged skill thin. It routes to canonical Recipes and must not copy their prompt text.
- Distinguish Source Entry, Translation, Attributed Rebuild, and Frozen Source accurately.
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

- Keep changes limited to the requested Recipe or shared contract.
- Update `catalog.json` when adding, removing, or renaming a Recipe.
- Update `docs/RECIPE_FORMAT.md` and `script/check` together when the shared record contract changes.
- Update this `AGENTS.md` when a meaningful agent workflow or repository command changes.
- Preserve source attribution and evidence history.
