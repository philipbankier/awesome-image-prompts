# Structured Concept Infographic

- Record version: 2
- Status: Draft
- Source posture: External Frozen Source reference with a separately authored Recipe wrapper
- Evidence status: Recorded illustrative run, not promotion evidence
- Profiles: `conversational-v1`, `gpt-image-2-api-v1`

This Recipe turns an approved facts block into one structured educational infographic. The facts block, not the image model, is the authority. A generated output can become a Production Candidate only after it passes every Critical Invariant and the complete rubric below.

## Task fit

Use this Recipe when a bounded set of approved facts should become one visual explanation with exact text and brief-specified diagrams. It is suited to mathematical, technical, scientific, or process concepts whose claims can be supplied before generation.

Do not use it to:

- Research, derive, or fact-check the subject.
- Invent missing explanations, formulas, quantities, labels, citations, or causal links.
- Reproduce the upstream case-341 image or visual composition.
- Fit a dense reference manual, large data table, or many paragraphs onto one canvas.
- Publish regulated, safety-critical, medical, financial, or legal guidance without qualified domain review.
- Claim publication readiness from an attractive image alone.

If the facts are incomplete, contradictory, or too dense for one canvas, stop and return the brief for revision.

## Required Creative Brief inputs

Supply every field below before generation:

```text
BRIEF_ID: Stable identifier and revision.
TOPIC: The concept being explained.
TITLE_EXACT: Exact title to render.
AUDIENCE: Prior knowledge and reading level.
LEARNING_GOAL: What the viewer should understand after one scan.
AUTHORITATIVE_FACTS:
- F1: One atomic, approved fact, definition, formula, or value.
- F2: One atomic, approved fact, definition, formula, or value.
REQUIRED_RELATIONSHIPS:
- R1: Exact relationship between named facts or objects.
EXACT_LABELS:
- L1: Exact text that must appear, including capitalization and notation.
REQUIRED_VISUALS:
- V1: A diagram, graph, sequence, or comparison tied to fact IDs.
LAYOUT_SPEC: Declared regions, reading order, and placement constraints.
VISUAL_SYSTEM: Project-owned palette, typography, geometry, and annotation rules.
ASPECT_AND_SIZE: Target orientation, aspect ratio, and output size.
SUMMARY_EXACT: One approved concluding sentence.
PROHIBITED_CONTENT: Claims, imagery, notation, brands, or interpretations to exclude.
SOURCE_OWNER: Person responsible for factual approval.
SOURCE_REVIEW_DATE: Date the facts were approved.
```

Facts may include source citations for review. Render citations only when the brief explicitly includes them in `EXACT_LABELS`.

## Input preparation

1. Ask the named source owner to approve the complete facts block before prompting.
2. Split compound statements into atomic fact IDs. Preserve exact equations, symbols, units, percentages, and qualifiers.
3. Map every required visual and relationship to one or more fact IDs. Every connector must encode a declared relationship rather than decorate the page.
4. Confirm that `LAYOUT_SPEC`, `VISUAL_SYSTEM`, and `ASPECT_AND_SIZE` are complete and project-owned. Split the brief when the content cannot remain legible at the selected size.
5. Resolve contradictory facts or ambiguous notation outside the image model. Do not ask the model to choose.
6. Remove instructions to research, browse, calculate new values, or fill gaps from general knowledge.

## Canonical Recipe prompt

Replace every bracketed field with the approved Creative Brief. Do not copy text or art direction from the linked external source.

```text
Create one self-contained educational infographic using only the authoritative content below.

Purpose
- Topic: [TOPIC]
- Exact title: [TITLE_EXACT]
- Audience: [AUDIENCE]
- Learning goal: [LEARNING_GOAL]

Factual boundary
- Treat AUTHORITATIVE_FACTS, REQUIRED_RELATIONSHIPS, EXACT_LABELS, REQUIRED_VISUALS, and SUMMARY_EXACT as the complete factual universe.
- Preserve every supplied equation, number, symbol, unit, qualifier, and exact label.
- Do not add facts, examples, formulas, citations, causal claims, or terminology that are not supplied.
- If content conflicts or cannot fit legibly, do not resolve it by invention.

Content
AUTHORITATIVE_FACTS:
[AUTHORITATIVE_FACTS]

REQUIRED_RELATIONSHIPS:
[REQUIRED_RELATIONSHIPS]

EXACT_LABELS:
[EXACT_LABELS]

REQUIRED_VISUALS:
[REQUIRED_VISUALS]

SUMMARY_EXACT:
[SUMMARY_EXACT]

PROHIBITED_CONTENT:
[PROHIBITED_CONTENT]

LAYOUT_SPEC:
[LAYOUT_SPEC]

VISUAL_SYSTEM:
[VISUAL_SYSTEM]

ASPECT_AND_SIZE:
[ASPECT_AND_SIZE]

Layout and visual constraints
- Follow only the supplied layout and visual-system rules.
- Keep each diagram near the facts it explains and route every connector to its declared endpoint.
- Do not add logos, signatures, watermarks, decorative pseudo-writing, or unreadable filler text.

Text and finish
- Render the exact title, exact labels, formulas, and summary accurately.
- Prefer short supplied phrases over generated prose.
- Keep all text horizontal unless the brief explicitly requires another orientation.
- Keep every required label, diagram, connector, and region fully inside the canvas.
- Before finalizing, compare the image against every supplied fact and relationship. Remove anything unsupported.
```

## Conversational Profile

Profile ID: `conversational-v1`

Use a supported ChatGPT or Codex conversational image-generation surface.

1. Complete and approve the Creative Brief.
2. Render the Canonical Recipe prompt with the approved values and paste it as one request.
3. Ask for one image using the orientation and dimensions declared in `ASPECT_AND_SIZE`.
4. Record the product surface, date, and every visible setting. Record the model, size, quality, output format, and other hidden parameters as `not exposed` when the surface does not show them.
5. Inspect the returned image using the same Critical Invariants and rubric. A conversational smoke run cannot replace API promotion evidence.

Do not imply that the conversational surface used `gpt-image-2` unless the surface explicitly reports it.

## GPT Image 2 API Profile

Profile ID: `gpt-image-2-api-v1`

Endpoint: OpenAI Image API, `POST /v1/images/generations`.

The reproducible generation profile is:

```json
{
  "model": "gpt-image-2-2026-04-21",
  "prompt": "<rendered Canonical Recipe prompt>",
  "n": 1,
  "size": "1024x1536",
  "quality": "high",
  "background": "opaque",
  "output_format": "png",
  "moderation": "auto"
}
```

The parameter names and values follow the official [OpenAI Image API reference](https://developers.openai.com/api/reference/python/resources/images/methods/generate) and [image-generation guide](https://developers.openai.com/api/docs/guides/image-generation). GPT Image models return base64-encoded image data, so `response_format` is intentionally omitted.

Before any provider-connected run, approve an exact run manifest containing the Recipe record version, profile ID, rendered prompt, Creative Brief revision, credential source, spend ceiling, retention policy, output location, and stop condition. Record the request identifier, run date, returned output metadata, output hash, latency, and cost when available. Do not infer missing provider metadata.

## Critical Invariants

Score each invariant pass or fail. One failure blocks the candidate and Recipe promotion.

- `CI-01 Facts`: Every factual statement, formula, number, unit, qualifier, and definition is supported by an identified item in `AUTHORITATIVE_FACTS`.
- `CI-02 Exact text`: `TITLE_EXACT`, every `EXACT_LABELS` item, and `SUMMARY_EXACT` appear without spelling, notation, or value changes.
- `CI-03 Relationships`: Every connector, sequence, comparison, containment, and grouping expresses a declared `REQUIRED_RELATIONSHIPS` item and points to the correct object.
- `CI-04 Required content`: Every required fact and `REQUIRED_VISUALS` item appears once in a recognizable, reviewable form unless the brief explicitly requests repetition.
- `CI-05 Legibility`: Required text and notation are readable at the full output size, without pseudo-writing, merged characters, clipped glyphs, or ambiguous mathematical symbols.
- `CI-06 Factual restraint`: The image contains no invented example, calculation, source, citation, claim, label, or explanatory prose.
- `CI-07 Canvas integrity`: No required region, label, formula, connector, or diagram is cropped, occluded, or outside the canvas.
- `CI-08 Rights and identity`: The image contains no unrequested logo, signature, watermark, real-person likeness, or copied upstream case-341 image element.

## Production Candidate Rubric

Rubric version: `structured-concept-infographic-rubric-v1`

Score each criterion `0`, `1`, or `2` after the Critical Invariants pass:

| ID | Criterion | 0 | 1 | 2 |
| --- | --- | --- | --- | --- |
| `R-01` | Factual mapping | Facts are missing or cannot be mapped to the brief. | Every fact is present but one mapping is hard to locate. | Every fact maps quickly and unambiguously to its fact ID. |
| `R-02` | Reading order | The page conflicts with `LAYOUT_SPEC`. | The declared path works with one minor jump. | The declared path is immediate and uninterrupted. |
| `R-03` | Diagram semantics | Diagrams do not clarify the declared relationships. | Diagrams are correct but one connection is weak. | Required visuals make every declared relationship easier to understand than text alone. |
| `R-04` | Information hierarchy | Required regions and details compete. | Hierarchy works with one locally crowded or weak region. | Every declared region and detail has the intended visual priority. |
| `R-05` | Text quality | Non-critical text has errors or is difficult to read. | Text is readable with one minor spacing or consistency issue. | Text and notation are crisp, consistent, and comfortably readable. |
| `R-06` | Composition | The canvas is unbalanced, crowded, or wasteful. | Composition is usable with one dense or empty region. | Density, whitespace, alignment, and visual weight are balanced. |
| `R-07` | Visual system | Styling conflicts with the supplied system. | The supplied system is coherent with one unnecessary treatment. | Palette, type, geometry, and annotations follow `VISUAL_SYSTEM` and support meaning. |
| `R-08` | Finish and accessibility | Contrast, artifacts, or color-only encoding impede use. | Output is usable with one minor artifact or contrast issue. | Contrast is clear, color has non-color reinforcement, and no visible artifact distracts. |

A full Production Candidate Rubric pass requires:

- All eight Critical Invariants pass.
- No rubric criterion scores `0`.
- The rubric total is at least `14/16`.

Recipe promotion still requires four scored API runs across the two declared briefs, two runs per brief. All four must pass the Critical Invariants, at least three must pass the full rubric, and one additional conversational smoke run must be recorded.

## Inspection and targeted repair

Inspect at full resolution, then at a reduced overview size.

1. Build a fact-audit list from `F1...Fn`, `R1...Rn`, and `L1...Ln`. Locate each item on the image and transcribe it back before marking it present.
2. Trace every connector from origin to endpoint and state the relationship it encodes. Fail any decorative or contradictory connector.
3. Compare equations, decimals, percentages, signs, subscripts, superscripts, and parentheses character by character. OCR may assist, but manual comparison is authoritative.
4. Check the title, sections, summary, reading order, crop, contrast, spacing, and legibility against the rubric.
5. Record every failure before repair. Do not silently replace a failed run in an evidence package.

Use one repair instruction per localized issue class:

```text
Repair only the identified defect in the supplied candidate image.

Defect: [one precise factual, text, connector, crop, or spacing defect]
Required correction: [exact replacement or positional change]
Must preserve: [all already-correct text, facts, diagrams, palette, layout, and dimensions]
Do not add new content or reinterpret the authoritative facts.
Return one corrected complete image.
```

For an API repair, use `gpt-image-2-2026-04-21` through the image-edit endpoint with the candidate image as the authorized input, omit `input_fidelity` because GPT Image 2 always processes image inputs at high fidelity, and otherwise retain the declared size, quality, background, and output format. Record the edit as a new run. If there are multiple semantic failures, a global hierarchy failure, or repeated edit drift, regenerate from the original approved brief instead of stacking repairs.

After any repair, rescore the whole image. A repaired area can disturb previously correct content, so no previous pass carries forward automatically.

## Final-QA handoff

Handoff only a candidate that passes every Critical Invariant and the full rubric. Include:

- Recipe ID and record version.
- Creative Brief ID, revision, source owner, and source review date.
- Profile ID, product surface or endpoint, exact model and parameters that were observable, rendered prompt, request ID, and run date.
- Original and repaired run IDs, if applicable, plus immutable output hashes and artifact paths.
- Critical Invariant results and all rubric scores with reviewer identity and review date.
- Known limitations, failed attempts, and repairs performed.
- Rights status for every supplied input and confirmation that the upstream case-341 image was not reused.
- Proposed channel, crop, caption, and factual source-owner sign-off.
- Descriptive alt text that does not introduce claims absent from the approved facts.

Label the output `Production Candidate`. It is not automatically publish-ready. The channel owner still reviews factual sign-off, accessibility, brand, legal, crop, and delivery requirements.

## Representative evaluation briefs

These briefs are test inputs, not generated evidence. They are materially different: Brief A tests continuous geometric reasoning with equations and linked graphs, while Brief B tests discrete conditional reasoning with counts, branches, and percentages.

### Brief A: Fundamental Theorem of Calculus

```text
BRIEF_ID: eval-ftc-v1
TOPIC: The Fundamental Theorem of Calculus
TITLE_EXACT: The Fundamental Theorem of Calculus
AUDIENCE: AP Calculus students who know derivatives and definite integrals.
LEARNING_GOAL: Connect accumulation, instantaneous rate of change, signed area, and antiderivatives.
LAYOUT_SPEC: Use an asymmetric two-column atlas. The graph occupies the left two-thirds; an equation rail occupies the right third; a narrow bottom band holds the sign comparison and exact conclusion.
VISUAL_SYSTEM: White field, graphite type and rules, violet for accumulation quantities, acid green for derivative markers, square nodes, monospaced equations, and no ornamental containers.
ASPECT_AND_SIZE: Portrait, 2:3, 1024x1536.
AUTHORITATIVE_FACTS:
- F1: Let f be continuous on the closed interval [a, b].
- F2: Define the accumulation function F(x) = ∫_a^x f(t) dt.
- F3: The first part of the theorem states F'(x) = f(x).
- F4: If A is any antiderivative of f, then ∫_a^b f(x) dx = A(b) - A(a).
- F5: Area above the x-axis contributes positively to a definite integral; area below the x-axis contributes negatively.
- F6: Where f(x) > 0, F is increasing. Where f(x) < 0, F is decreasing.
- F7: For a small positive Δx, F(x + Δx) - F(x) is approximately f(x)Δx; dividing by Δx and taking the limit gives F'(x) = f(x).
REQUIRED_RELATIONSHIPS:
- R1: Link a shaded area from a to x under the graph of f to the value F(x).
- R2: Link the sign of f(x) to whether F increases or decreases.
- R3: Present F'(x) = f(x) and ∫_a^b f(x) dx = A(b) - A(a) as the two complementary parts of the theorem.
EXACT_LABELS:
- L1: Accumulation function
- L2: F(x) = ∫_a^x f(t) dt
- L3: F'(x) = f(x)
- L4: ∫_a^b f(x) dx = A(b) - A(a)
- L5: signed area
REQUIRED_VISUALS:
- V1: A coordinate plot of f with the signed area from a to x highlighted.
- V2: A linked sketch of F showing increasing and decreasing regions corresponding to the sign of f.
- V3: A separate micro-diagram of the narrow strip with width Δx and approximate area f(x)Δx.
- V4: A two-row equation rail showing the theorem's complementary statements.
SUMMARY_EXACT: Differentiating accumulation returns the original rate; integrating a rate gives the net change in an antiderivative.
PROHIBITED_CONTENT: Numerical examples, proof claims beyond F7, historical attribution, citations, and formulas not listed above.
SOURCE_OWNER: Evaluation fact owner
SOURCE_REVIEW_DATE: Must be set before a run.
```

### Brief B: Bayes' theorem through a component sensor

```text
BRIEF_ID: eval-bayes-sensor-v1
TOPIC: Bayes' theorem and conditional probability
TITLE_EXACT: Bayes' Theorem: Read the Flagged Group Correctly
AUDIENCE: Introductory statistics learners who understand percentages.
LEARNING_GOAL: See why a positive signal must be interpreted using the base rate and the full flagged group.
LAYOUT_SPEC: Use a top-to-bottom flow. A population matrix occupies the top half; one horizontal flagged band joins the two branches; a calculation strip occupies the bottom quarter.
VISUAL_SYSTEM: Light-gray field, black type, orange for defective components, cyan for good components, square count markers, monospaced numerals, and heavy brackets for group totals.
ASPECT_AND_SIZE: Portrait, 2:3, 1024x1536.
AUTHORITATIVE_FACTS:
- F1: Consider 1,000 components: 100 are defective and 900 are good.
- F2: The sensor flags 90 of the 100 defective components.
- F3: The sensor flags 45 of the 900 good components.
- F4: The flagged group contains 135 components: 90 defective and 45 good.
- F5: P(defective) = 10%.
- F6: P(flagged | defective) = 90%.
- F7: P(flagged | good) = 5%.
- F8: P(flagged) = 135 / 1,000 = 13.5%.
- F9: P(defective | flagged) = 90 / 135 = 2 / 3 ≈ 66.7%.
- F10: Bayes' theorem is P(D | +) = P(+ | D)P(D) / P(+).
REQUIRED_RELATIONSHIPS:
- R1: Split 1,000 components into 100 defective and 900 good.
- R2: From the defective branch, 90 enter the flagged group. From the good branch, 45 enter the flagged group.
- R3: The posterior denominator is the full flagged group of 135, not the 100 defective components.
- R4: Substitute 90%, 10%, and 13.5% into Bayes' theorem to obtain approximately 66.7%.
EXACT_LABELS:
- L1: Base rate: 10%
- L2: Flagged defective: 90
- L3: Flagged good: 45
- L4: Total flagged: 135
- L5: P(defective | flagged) = 90 / 135 ≈ 66.7%
- L6: P(D | +) = P(+ | D)P(D) / P(+)
REQUIRED_VISUALS:
- V1: A two-level count tree beginning with 1,000 components.
- V2: A horizontal flagged band containing 90 defective and 45 good components.
- V3: A three-row equation stack for the Bayes substitution.
- V4: One bracket joining both flagged branches to the denominator 135.
SUMMARY_EXACT: A positive flag changes the comparison group: 90 of the 135 flagged components are defective, so the posterior probability is about 66.7%.
PROHIBITED_CONTENT: Medical framing, additional sensor metrics, claims about real-world equipment, citations, and values not listed above.
SOURCE_OWNER: Evaluation fact owner
SOURCE_REVIEW_DATE: Must be set before a run.
```

## Rendered Sample

![Bayes theorem infographic showing 1,000 components split into defective and good groups, then recombined into 135 flagged components](samples/bayes-flagged-group.png)

This is one real output generated from Evaluation Brief B with the Codex built-in image generation tool on 2026-08-25. Manual review found the population split, flagged counts, denominator, Bayes substitution, and `66.7%` result visibly consistent with the supplied facts.

- [Exact submitted prompt](samples/bayes-flagged-group.prompt.txt)
- [Generation Run record](evidence.json)
- Model, model version, seed, request parameters, and request ID: `not_exposed`
- Output: `1024x1536` PNG
- Promotion evidence: no

The sample demonstrates one result, not repeatability, GPT Image 2 API conformance, a fully scored rubric pass, factual sign-off, or publication readiness.

## Provenance and rights boundary

This workflow is a separately authored Recipe informed by the general task pattern in the pinned [case-341 Source Reference](../../sources/case-341.md). The upstream prompt body is represented only by an external link and checksum. It is not reproduced or presented as project writing.

The upstream image remains a linked provenance reference and is not part of this Recipe. Use only fictional, project-owned, or otherwise authorized Creative Brief inputs for future Rendered Samples, and complete item-level rights review for those inputs before external publication.
