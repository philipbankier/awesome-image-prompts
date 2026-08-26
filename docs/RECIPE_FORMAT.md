# Recipe format

The pilot uses a folder as the smallest complete Recipe record:

```text
recipes/<recipe-id>/
|-- RECIPE.md       Canonical human and agent workflow
|-- recipe.json     Small machine-readable routing metadata
|-- evidence.json   Placeholder or recorded run evidence
`-- samples/        Optional exact prompts and PNG inputs or outputs
```

## RECIPE.md

Each Recipe describes only what the workflow needs:

- Task fit and non-fit
- Required Creative Brief inputs
- Input preparation
- Conversational Profile
- GPT Image 2 API Profile
- Critical Invariants
- Production Candidate Rubric
- Inspection and targeted repair
- Final-QA handoff
- Representative evaluation briefs
- Placeholder Preview or Rendered Samples
- Provenance and rights boundary

Prompt text belongs here. The Packaged Skill links to this file rather than maintaining a copy.

## recipe.json

The metadata record contains:

- `schema_version`
- `id`
- `record_version`
- `status`
- `title`
- `task_family`
- `source_posture`
- `source_record`
- `recipe_markdown`
- `evidence_manifest`
- `profiles`, an object mapping `conversational` and `gpt-image-2-api` to their profile IDs
- `evidence_status`

Version one uses direct integer record versions. It does not implement semantic-version automation or an invalidation graph.

## evidence.json

The evidence record uses `schema_version: 1`, names the `recipe_id`, and binds to the exact `recipe.json` integer through `recipe_record_version`. Its `status` and `runs` must agree:

- `placeholder`: no behavioral claim; `runs` must be empty.
- `recorded`: at least one exact Generation Run is present; `runs` must be non-empty.

Each Generation Run requires:

- `id`, unique within the evidence file
- `kind`, such as `conversational-sample` or `supporting-input-generation`
- `generated_at`
- `surface`
- `model`, `model_version`, and `request_id`, each a non-empty string or the explicit string `not_exposed`
- `seed`, an integer, other non-empty provider value, or `not_exposed`
- `request_parameters`, an object containing the exact parameters or `not_exposed`
- `prompt_file`, a Recipe-folder-relative pointer to a non-empty UTF-8 file containing the exact submitted prompt
- `profile_id`, either a profile ID declared by `recipe.json` or `null` for an illustrative or supporting run that is not promotion evidence
- `inputs`, an array of zero or more input asset records
- `output`, one output asset record
- `inspection`, with a non-empty `status` and a non-empty `notes` array of non-empty strings
- `promotion_evidence`, a boolean
- `featured_in_readme`, a boolean
- `rights`, with non-empty `input_rights`, `creator_or_authorized_licensor`, and `license` strings

Each input and output asset record requires `path`, `sha256`, `width`, `height`, and `format`. Paths resolve from the Recipe folder and must remain inside the repository. `sha256` is the file's 64-character lowercase hexadecimal digest, dimensions are positive integers matching the PNG IHDR, and `format` is `png`. Every input also requires a non-empty `authorization` statement.

The validator checks that prompt and asset files exist, checks asset digests and PNG dimensions, and requires a featured output's repository-root-relative path plus its `evidence.json` path to appear in the root README.

A `supporting-input-generation` run cannot be promotion evidence. Promotion evidence also requires a declared `profile_id` and concrete `model`, `model_version`, `seed`, `request_parameters`, and `request_id` values rather than `not_exposed`.

`recorded` does not mean promoted. It means the repository contains at least one validated run record. A single illustrative or conversational sample may remain unscored and must set `promotion_evidence: false`.

A promoted Recipe eventually requires four API evaluation runs across two materially different briefs and one conversational smoke run. All four API runs must pass Critical Invariants, and at least three must pass the full Production Candidate Rubric.
