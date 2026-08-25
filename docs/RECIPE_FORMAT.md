# Recipe format

The pilot uses a folder as the smallest complete Recipe record:

```text
recipes/<recipe-id>/
|-- RECIPE.md       Canonical human and agent workflow
|-- recipe.json     Small machine-readable routing metadata
`-- evidence.json   Placeholder or recorded run evidence
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

Evidence is either:

- `placeholder`: no behavioral claim; `runs` must be empty.
- `recorded`: supported by exact Generation Run records.

A promoted Recipe eventually requires four API evaluation runs across two materially different briefs and one conversational smoke run. All four API runs must pass Critical Invariants, and at least three must pass the full Production Candidate Rubric.
