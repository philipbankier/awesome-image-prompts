# Prompt Card format

A Prompt Card is a quick, copy-ready starting point for a narrow image task. It is intentionally smaller than a Recipe: it does not define execution profiles, a Production Candidate Rubric, targeted repair, or promotion evidence.

Each Prompt Card uses one Markdown file:

```text
prompt-cards/<category-id>/<card-id>.md
```

All Prompt Card metadata lives in `catalog.json`. Do not add frontmatter, a per-Card JSON record, or an evidence manifest. The Markdown file owns only the human-readable task guidance and prompt content.

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

For the current release, `rights` is `project-authored`, `sample_status` is `placeholder`, and no Prompt Card has an evidence manifest. An `original` card uses `source_record: null`. Other source postures require a linked Source Entry.

## Required Markdown structure

The H1 must match the catalog title. Every Prompt Card then uses these headings exactly and in this order:

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

## Placeholder Preview

Sample status: Placeholder Preview.

Describe the intended result and state that no recorded generation run supports it.

## Rights and provenance

State the input rights basis, project-authored rights, source posture, and any Source Entry link.
````

The `Prompt` section must contain a fenced `text` block. Every variable in that block must be explained under `Variables`. Every user-supplied creative or safety constraint and every declared non-text input mode must reach the prompt through a variable or an explicit instruction. Keep the prompt immediately usable after those variables are supplied.

## Evidence boundary

A `Placeholder Preview` is navigation material, not evidence that the prompt works. A Quick check helps reject an obvious failure but does not establish repeatability, Recipe promotion, Production Candidate status, or publish readiness.

If correctness depends on exact text or layout, rights-cleared reference inputs, identity or geometry preservation, structured inspection and repair, or repeatability evidence, route the user to the linked Recipe or the Recipe index instead.

## Provenance boundary

The Source Archive records provenance for sourced material. It is infrastructure behind the Prompt Atlas, not a third user-facing content layer. Do not copy uncleared prompt text or images into a Prompt Card. Publish a Translation only when item-level redistribution rights permit it and label the derivative relationship accurately.
