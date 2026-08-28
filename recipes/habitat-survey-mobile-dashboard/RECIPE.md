# Habitat Survey Mobile Dashboard

- Record version: 1
- Status: Draft
- Source posture: Original
- Evidence status: Recorded illustrative built-in-tool sample; promotion evidence: no
- Profiles: `conversational-v1`, `gpt-image-2-api-v1`

Outcome: one Production Candidate for a single-screen fictional habitat-survey mobile interface. Generation alone does not make the interface usable, accessible, or publish-ready.

## Task fit

Use this Recipe when the brief requires:

- one portrait mobile home screen, not a flow or multi-screen board;
- assigned survey plots, observation totals, sync state, and one primary field action;
- a closed exact-label manifest and internally consistent fictional data;
- practical mobile hierarchy, safe areas, and touch targets;
- inspection and targeted repair before product or accessibility QA.

Do not use it for:

- a functioning application, research protocol, navigation system, or safety tool;
- real protected-species, location, volunteer, or organization data without authorization;
- a desktop operations dashboard or a complete survey workflow;
- invented ecological conclusions, risk alerts, or field guidance;
- a request that treats a generated image as deployable UI.

## Required Creative Brief inputs

Provide every field before generation:

- `survey_name_exact`: fictional or authorized survey title.
- `habitat_label_exact`: exact habitat label.
- `active_plot_exact`: exact current plot or transect.
- `assignment_progress`: completed and total plot counts.
- `observation_metrics`: closed list of exact labels and values.
- `sync_state_exact`: connectivity and pending-record wording.
- `next_task_exact`: one approved next-task line.
- `primary_action_exact`: one exact button label.
- `navigation_manifest`: exact navigation labels and selected item.
- `map_cue`: fictional extent, marker, and allowed labels.
- `visual_system`: project-owned palette, typography, card, and icon rules.
- `device_and_output`: safe areas, aspect ratio, and pixel size.
- `rights_confirmation`: authority for every supplied name, datum, icon, and map cue.

Stop if counts conflict, exact labels are incomplete, or private coordinates or participant information appear in the brief.

## Input preparation

1. Freeze the exact-text manifest, including capitalization, punctuation, numbers, and separators.
2. Recalculate progress and ensure metric totals do not imply undeclared observations.
3. Define the offline or sync state independently from completion status.
4. Reduce the home screen to one primary action and no more than three compact secondary destinations.
5. Use fictional geography unless a supplied map is explicitly authorized.
6. Declare a minimum touch-target and contrast intention for later product QA.

## Portable prompt

Replace every brace-delimited value with approved brief content. Leave no unresolved placeholder.

```text
Create one polished portrait mobile home screen for a habitat survey application used during {FIELD_CONTEXT}.

SURVEY STATE
- Survey: {SURVEY_NAME_EXACT}
- Habitat: {HABITAT_LABEL_EXACT}
- Active assignment: {ACTIVE_PLOT_EXACT}
- Progress: {ASSIGNMENT_PROGRESS}
- Observation metrics: {OBSERVATION_METRICS}
- Sync state: {SYNC_STATE_EXACT}
- Next task: {NEXT_TASK_EXACT}

INTERACTION
- Make {PRIMARY_ACTION_EXACT} the one dominant action.
- Navigation: {NAVIGATION_MANIFEST}.
- Include only the fictional location cue {MAP_CUE}.

VISUAL SYSTEM
- Apply {VISUAL_SYSTEM} consistently.
- Keep safe areas, spacing, contrast, and touch targets practical for {DEVICE_AND_OUTPUT}.
- Make progress, sync state, and selected navigation distinct without relying on color alone.

TEXT AND DATA BOUNDARY
- Render only {EXACT_TEXT_MANIFEST}.
- Preserve every number, separator, label, and state exactly.
- Add no species, alert, coordinate, claim, logo, map-provider mark, pseudo-text, signature, or watermark.

OUTPUT
- Return one complete mobile interface, not a device mockup, multi-screen board, wireframe sheet, or app-store panel.
```

## Conversational Profile

Profile ID: `conversational-v1`

1. Submit the approved brief and completed Portable prompt.
2. Ask the surface to identify unresolved labels or conflicting states before generation.
3. Generate one image only after those issues are resolved.
4. Record the surface, date, visible settings, and any exposed model information. Mark hidden fields `not_exposed`; do not infer them.
5. Inspect the result against the same invariants and rubric used for API evaluation.

A conversational result is not API promotion evidence.

## GPT Image 2 API Profile

Profile ID: `gpt-image-2-api-v1`

Endpoint: OpenAI Image API, `POST /v1/images/generations`.

```json
{
  "model": "gpt-image-2-2026-04-21",
  "prompt": "<completed Portable prompt>",
  "n": 1,
  "size": "1024x1536",
  "quality": "high",
  "background": "opaque",
  "output_format": "png",
  "moderation": "auto"
}
```

Before any provider call, approve the exact prompt, credential source, spend ceiling, retention policy, output location, and stop condition. Preserve the request body and returned metadata. No API request has been made for this Recipe.

## Critical Invariants

- `CI-01 Single screen`: exactly one portrait home screen appears, with no device mockup or adjacent state.
- `CI-02 Exact text`: every approved string and number is correct, legible, and appears only as declared.
- `CI-03 State consistency`: progress, counts, active plot, sync state, and selected navigation do not conflict.
- `CI-04 Action hierarchy`: the declared primary action is unmistakable and no secondary control competes with it.
- `CI-05 Mobile viability`: content remains inside safe areas with plausible touch targets and readable contrast.
- `CI-06 Data restraint`: no invented species, coordinate, alert, ecological claim, person, logo, or map-provider mark appears.

## Production Candidate Rubric

Score each item `pass` or `fail` after all Critical Invariants pass:

- `R-01 Glanceability`: plot, progress, sync state, and next action are understood in one scan.
- `R-02 Information hierarchy`: title, active assignment, metrics, and navigation have distinct priority.
- `R-03 Interaction clarity`: controls look actionable and states do not depend on color alone.
- `R-04 Field legibility`: key values remain readable at reduced phone size and in the declared palette.
- `R-05 Visual coherence`: cards, icons, spacing, radii, and typography follow one system.
- `R-06 Finish`: no malformed icon, clipped type, alignment drift, pseudo-text, or low-resolution region remains.

A full pass requires all six items. Recipe promotion still requires the separate four-run API gate and conversational smoke run defined by the library contract.

## Inspection and targeted repair

1. Transcribe every visible string and compare it with the manifest.
2. Recalculate progress and compare every summary value with the brief.
3. Inspect safe areas, tap-target scale, selected states, contrast, and offline messaging.
4. Record every failure before repair.

```text
Repair only this defect in the supplied mobile interface: {DEFECT}.
Required correction: {EXACT_CORRECTION}.
Preserve all already-correct labels, values, hierarchy, layout, palette, icons, and dimensions.
Add no new screen, datum, control, text, logo, or map detail.
Return one corrected complete interface.
```

After repair, rescore the whole image because a local edit can disturb text or state consistency elsewhere.

## Final-QA handoff

Include the Recipe ID and version, brief revision, exact prompt, profile and visible settings, output hash and path, invariant results, rubric results, known failures, repair history, rights status, and descriptive alt text. Label the output `Production Candidate` only after it passes. Product, accessibility, privacy, security, and implementation review remain separate.

## Representative evaluation brief

The saved prompt at `samples/habitat-survey-mobile-dashboard.prompt.txt` resolves this fictional brief:

- `survey_name_exact`: `MARSHLIGHT`, subtitle `Habitat Survey`.
- `habitat_label_exact`: `Salt Marsh`.
- `active_plot_exact`: `Plot H-07`.
- `assignment_progress`: `6 of 10 plots`.
- `observation_metrics`: `Birds 12`, `Plants 8`, `Water 2`.
- `sync_state_exact`: `Offline • 3 records pending`.
- `next_task_exact`: `Next: Eastern transect`.
- `primary_action_exact`: `RECORD OBSERVATION`.
- `navigation_manifest`: `Survey`, `Map`, `Notes`; `Survey` selected.
- `device_and_output`: portrait 9:16, `1024x1536`.

## Rendered Sample

![MARSHLIGHT habitat-survey mobile dashboard showing an offline plot assignment and field-observation totals](samples/habitat-survey-mobile-dashboard.png)

This is the accepted output of a recorded two-step built-in-tool sequence from 2026-08-26. The initial call used the representative base prompt and added an undeclared `60%` label. The second call used the exact targeted edit prompt and the recorded initial PNG as an authorized image input. Manual review found the accepted output's required labels and fictional values legible and internally consistent.

- [Initial generation prompt](samples/habitat-survey-mobile-dashboard.prompt.txt)
- [Exact targeted edit prompt](samples/habitat-survey-mobile-dashboard.edit.prompt.txt)
- [Superseded initial PNG](samples/habitat-survey-mobile-dashboard.initial.png)
- [Initial and edit run record](evidence.json)
- Model, model version, seed, request parameters, and request ID: `not_exposed`
- Initial output: `1024x1536` PNG; accepted edit output: `941x1672` PNG
- Promotion evidence: no

The accepted PNG is bound to the edit run, not the base prompt alone. This two-step illustrative sequence does not demonstrate repeatability, GPT Image 2 API conformance, Recipe promotion evidence, a full rubric pass, implementation readiness, or publication readiness.

## Rights and provenance boundary

This Recipe and its saved fictional brief are independently authored with source posture `original` and `source_record: null`. Use only fictional or authorized survey names, data, icons, and geography. No linked Source Entry, third-party interface, map, prompt, or image is included.
