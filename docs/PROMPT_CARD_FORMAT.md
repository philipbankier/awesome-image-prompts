# Prompt Card format

A Prompt Card is a quick, copy-ready starting point for a narrow image task. It is intentionally smaller than a Recipe: it does not define execution profiles, a Production Candidate Rubric, targeted repair, or promotion evidence.

Each Prompt Card uses one canonical Markdown file:

```text
prompt-cards/<category-id>/<card-id>.md
```

All Prompt Card routing metadata lives in `catalog.json`. The Markdown file owns the human-readable task guidance, prompt content, and, when present, the public Rendered Sample record. Do not add frontmatter, a per-Card JSON record, or a shared Card evidence manifest.

## Catalog metadata

Each Prompt Card catalog entry contains:

- `id`
- `title`
- `category`
- `task_family`
- `input_modes`, using one or more of `text`, `reference-image`, `multiple-images`, or `sketch`
- `output_type`
- `aspect_ratio`, written as a positive width-to-height ratio such as `3:2`
- `text_density`, using `none`, `low`, `medium`, or `high`
- `tags`, with at least two unique lowercase hyphenated values
- `path`
- `source_posture`
- `source_record`
- `rights`
- `sample_status`
- `linked_recipe`, containing a Recipe ID or `null`

`input_modes` lists the input types a Card supports. It does not encode whether a mode is required, optional, or one of several alternatives; the Card's Required inputs section owns that logic.

For the current release, `rights` is `project-authored` and `sample_status` is either `placeholder` or `rendered`. An `original` card uses `source_record: null`. Other source postures require a linked Source Entry.

## Required Markdown structure

The H1 must match the catalog title. Every Prompt Card uses the common headings below in this order. The sample heading must agree with `sample_status`: a placeholder Card uses `## Placeholder Preview`, while a recorded Card uses `## Rendered Sample`.

````markdown
# <Card title>

## Use this when

State the narrow task fit and the cases that should use a Recipe instead.

## Required inputs

List the minimum facts, assets, and authority the user must provide.

## Prompt

```text
Write the copy-ready prompt here.
```

## Variables

Define every variable used by the prompt and no others.

## Negative constraints

List the failures or unwanted elements the generation should avoid.

## Quick check

Give a short visual check for obvious failures. This is not a Production Candidate Rubric.

## <Placeholder Preview or Rendered Sample>

Use the matching sample record described below.

## Rights and provenance

State the input rights basis, project-authored rights, source posture, and any Source Entry link.
````

The `Prompt` section must contain a fenced `text` block. Every variable in that block must be explained under `Variables`. Every user-supplied creative or safety constraint and every declared non-text input mode must reach the prompt through a variable or an explicit instruction. Keep the prompt immediately usable after those variables are supplied.

## Placeholder Preview record

A Card with `sample_status: placeholder` uses:

```markdown
## Placeholder Preview

Sample status: Placeholder Preview.

Describe the intended result and state that no recorded generation run supports it.
```

It has no public sample directory. A placeholder remains valid while the rest of the Card satisfies this format.

## Rendered Sample record

A Card with `sample_status: rendered` keeps its public evidence in the Card Markdown and stores only deterministic public derivatives beside the Card:

```text
prompt-cards/<category-id>/samples/<card-id>/
|-- <card-id>.webp
|-- <card-id>.prompt.txt
`-- input-NN-<role>.webp        Optional public supporting derivatives
```

The accepted final public derivative is `<card-id>.webp`. The exact instantiated prompt submitted for that output is `<card-id>.prompt.txt`; it must be non-empty UTF-8 text with no unresolved `{VARIABLE}` tokens. Supporting derivatives use a unique two-digit identifier from `01` through `99` and a lowercase hyphenated role, such as `input-01-reference.webp`. Lossless masters, private source assets, rejected attempts, and provider exports do not belong in this public folder.

Use this required field layout. Free-text values must be specific and non-empty.

```markdown
## Rendered Sample

![Rendered sample for <Card title>](samples/<card-id>/<card-id>.webp)

- Sample status: Rendered Sample.
- Generation surface: <surface used>
- Generated at: `YYYY-MM-DDTHH:MM:SSZ`
- Model: `not_exposed`
- Model version: `not_exposed`
- Seed: `not_exposed`
- Request parameters: `not_exposed`
- Request ID: `not_exposed`
- Exact prompt: [<card-id>.prompt.txt](samples/<card-id>/<card-id>.prompt.txt)
- Output dimensions: `<width> x <height>`
- Output SHA-256: `<64 lowercase hexadecimal characters>`
- Profile ID: `null`
- Promotion evidence: `false`
- Human inspection: <what was checked in the accepted derivative>
- Known misses: <remaining misses, or an explicit statement that none were observed>
- Rights and provenance: <input authority, project authorship, derivative history, and public reuse basis>
```

When public supporting derivatives are present, add a supporting-input list after the required fields and link each file using its exact deterministic path:

```markdown
- Supporting inputs:
  - [input-01-reference.webp](samples/<card-id>/input-01-reference.webp): <role and public rights basis>
```

The validator checks the final image and every linked supporting derivative for WebP identity and readable positive dimensions. It also checks the recorded final dimensions and SHA-256 against `<card-id>.webp`.

This record is illustrative evidence for this exact instantiated prompt and derivative only. Hidden model and request fields stay `not_exposed`; `profile_id` stays `null`; and `promotion_evidence` stays `false`. A Rendered Sample does not become Recipe evidence, repeatability proof, a Production Candidate, or a Publish-Ready Asset.

## Evidence boundary

A `Placeholder Preview` is navigation material, not evidence that the prompt works. A Rendered Sample is inspectable evidence for one exact run, with the limits recorded in the Card. A Quick check helps reject an obvious failure but does not establish repeatability, Recipe promotion, Production Candidate status, or publish readiness.

If correctness depends on exact text or layout, rights-cleared reference inputs, identity or geometry preservation, structured inspection and repair, or repeatability evidence, route the user to the linked Recipe or the Recipe index instead.

## Provenance boundary

The Source Archive records provenance for sourced material. It is infrastructure behind the Prompt Atlas, not a third user-facing content layer. Do not copy uncleared prompt text or images into a Prompt Card. Publish a Translation only when item-level redistribution rights permit it and label the derivative relationship accurately.
