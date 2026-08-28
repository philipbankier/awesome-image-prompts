# Library After Dark Event Poster

- Record version: 1
- Status: Draft
- Source posture: Original
- Evidence status: Recorded illustrative built-in-tool sample; promotion evidence: no
- Profiles: `conversational-v1`, `gpt-image-2-api-v1`

Outcome: one Production Candidate for a fictional exact-text event poster. Generation alone does not establish factual accuracy, print readiness, accessibility, or permission to publish.

## Task fit

Use this Recipe when the brief requires:

- one finished portrait poster for a fictional or authorized event;
- an exact title, date, time, venue, program line, and call to action;
- a declared reading hierarchy and original visual concept;
- text inspection before aesthetic scoring;
- targeted repair and final print or channel QA.

Do not use it for:

- a real event whose logistics or permissions have not been approved;
- copied poster art, a named-designer imitation, or a copyrighted book cover;
- a multi-page program, ticket, social carousel, or animated campaign;
- invented sponsors, speakers, claims, prices, or policy copy;
- a request that assumes attractive type is exact type.

## Required Creative Brief inputs

Provide every field before generation:

- `event_title_exact`: exact fictional or authorized headline.
- `date_exact` and `time_exact`: final approved logistics.
- `venue_exact`: exact venue line.
- `program_line_exact`: closed list of approved activities.
- `access_line_exact`: price or access statement.
- `call_to_action_exact`: one approved action.
- `exact_text_manifest`: every allowed string in hierarchy order.
- `visual_concept`: one independently authored motif.
- `composition`: text zones, motif position, margins, and reading order.
- `visual_system`: palette, typography character, illustration method, and texture.
- `output`: aspect ratio, pixel size, trim intent, and background.
- `rights_confirmation`: authority for the event details, copy, and supplied assets.

Stop if any logistics conflict, the text manifest is open-ended, or a third-party identity is requested without permission.

## Input preparation

1. Freeze spelling, case, punctuation, separators, and line breaks for every string.
2. Check date and time together and confirm the venue line is final.
3. Assign each string one hierarchy level and one location.
4. Remove undeclared sponsors, logos, URLs, QR codes, and fine print.
5. Define one original motif that leaves enough quiet space for exact typography.
6. Choose portrait dimensions and safe margins before composing.

## Portable prompt

Replace every brace-delimited value with approved brief content. Leave no unresolved placeholder.

```text
Create one finished portrait event poster for {EVENT_CONTEXT}.

VISUAL CONCEPT
- Motif: {VISUAL_CONCEPT}.
- Composition: {COMPOSITION}.
- Visual system: {VISUAL_SYSTEM}.

EXACT TEXT
- Render only these strings, each exactly as supplied: {EXACT_TEXT_MANIFEST}.
- Hierarchy: {TYPE_HIERARCHY}.
- Preserve every letter, numeral, space, punctuation mark, separator, capitalization choice, and declared line break.
- Do not translate, paraphrase, duplicate, truncate, or add text.

PRINT BOUNDARY
- Keep every required string and motif inside {SAFE_AREA}.
- Maintain readable contrast at {OUTPUT}.
- Add no sponsor, logo, person, book title, author, QR code, URL, price, quote, fine print, pseudo-writing, signature, or watermark.

OUTPUT
- Return one complete poster artwork, not a framed mockup, option sheet, social interface, book cover, or multi-page program.
```

## Conversational Profile

Profile ID: `conversational-v1`

1. Submit the approved brief and completed Portable prompt.
2. Ask the surface to list unresolved text or hierarchy conflicts without generating.
3. Resolve every conflict, then request one image.
4. Record the surface, date, visible settings, and exposed model information. Mark hidden fields `not_exposed`.
5. Inspect the result against the exact-text manifest before judging style.

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

- `CI-01 Exact text`: every manifest string appears once with identical characters, case, punctuation, separators, and approved line breaks.
- `CI-02 No extra text`: no sponsor, logo, URL, QR code, quote, author, book title, fine print, or pseudo-writing appears.
- `CI-03 Logistics`: date, time, venue, access line, and action remain complete and mutually consistent.
- `CI-04 Hierarchy`: headline, logistics, program line, and action follow the declared priority.
- `CI-05 Canvas safety`: no required type or motif is clipped, occluded, or placed outside the safe area.
- `CI-06 Original deliverable`: the result is one original event poster, not copied key art, a mockup, or a multi-option sheet.

## Production Candidate Rubric

Score each item `pass` or `fail` after all Critical Invariants pass:

- `R-01 Thumbnail recognition`: headline and central motif remain clear at reduced size.
- `R-02 Information scan`: date, time, venue, and action can be found in the intended sequence.
- `R-03 Text quality`: required type is crisp, evenly spaced, and visually consistent.
- `R-04 Motif integration`: the original concept supports the event rather than competing with logistics.
- `R-05 Contrast and balance`: type remains readable and the page uses negative space deliberately.
- `R-06 Finish`: no malformed letter, accidental tangency, texture artifact, or low-resolution region remains.

A full pass requires all six items. Recipe promotion still requires the separate four-run API gate and conversational smoke run defined by the library contract.

## Inspection and targeted repair

1. Transcribe every visible string without looking at the brief, then compare character by character.
2. Check logistics and hierarchy independently from illustration quality.
3. Inspect trim safety, contrast, small text, texture, and unwanted marks.
4. Record every failure before repair.

```text
Repair only this defect in the supplied event poster: {DEFECT}.
Required correction: {EXACT_CORRECTION}.
Preserve all already-correct text, hierarchy, motif, palette, composition, margins, and dimensions.
Add no sponsor, logo, URL, QR code, book title, person, pseudo-text, signature, or watermark.
Return one corrected complete poster.
```

After repair, transcribe and rescore the entire poster because local text edits can disturb other strings or spacing.

## Final-QA handoff

Include the Recipe ID and version, brief revision, exact-text manifest, exact prompt, profile and visible settings, output hash and path, invariant results, rubric results, failure and repair history, rights status, proposed trim and channel, and descriptive alt text. Label the output `Production Candidate` only after it passes. Event owner, accessibility, legal, and print-production review remain separate.

## Representative evaluation brief

The saved prompt at `samples/library-after-dark-event-poster.prompt.txt` resolves this fictional brief:

- Headline: `LIBRARY AFTER DARK`.
- Date: `Friday 18 October`.
- Time: `7:00 PM–10:30 PM`.
- Venue: `Northlight Community Library`.
- Program: `NIGHT READING • LANTERN TOUR • HOT CHOCOLATE`.
- Access: `FREE ENTRY`.
- Action: `BOOK YOUR PLACE`.
- Concept: an open book becomes a doorway beneath one warm reading-lamp moon.
- Output: portrait 2:3, `1024x1536`.

## Rendered Sample

![LIBRARY AFTER DARK event poster with an open book forming a doorway into a night library](samples/library-after-dark-event-poster.png)

This is one recorded illustrative output from the representative brief with the Codex built-in image generation tool on 2026-08-26. Manual review found all supplied event copy legible and the open-book doorway concept, hierarchy, margins, and palette coherent.

- [Exact submitted prompt](samples/library-after-dark-event-poster.prompt.txt)
- [Generation run record](evidence.json)
- Model, model version, seed, request parameters, and request ID: `not_exposed`
- Output: `1024x1536` PNG
- Promotion evidence: no

This sample is one illustrative built-in-tool output. It does not demonstrate repeatability, GPT Image 2 API conformance, Recipe promotion evidence, a full rubric pass, print readiness, or publication readiness.

## Rights and provenance boundary

This Recipe and its saved fictional brief are independently authored with source posture `original` and `source_record: null`. Use only fictional or authorized event details and project-owned art direction. No linked Source Entry, third-party poster, type artwork, prompt, or image is included.
