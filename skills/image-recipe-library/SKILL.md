---
name: image-recipe-library
description: Select a copy-ready image Prompt Card for quick prompting or an evidence-tracked Recipe for production workflows that require structured inputs, inspection, and repair.
---

# Image Prompt Atlas

Use this skill to choose the smallest canonical content layer that fits the user's image task.

## Choose a layer

- Use a Prompt Card when the user wants a fast, copy-ready prompt and does not need a repeatable production workflow. Read [the Prompt Card index](../../prompt-cards/README.md), select the narrowest match, then read only that Card.
- Use a Recipe when correctness depends on structured inputs, authorized reference assets, exact text or layout, identity or geometry preservation, inspection and repair, or evidence. Read [references/recipe-index.md](references/recipe-index.md), select the narrowest match, then read only that Recipe's `RECIPE.md`.
- If neither layer fits, explain the mismatch. Do not label an improvised prompt as a catalog Prompt Card or Recipe.

## Prompt Card workflow

1. Collect the Card's Required inputs and confirm any reference assets are authorized and available.
2. Fill every declared variable without changing the Card's task boundary or Negative constraints.
3. Return the adapted copy-ready prompt. If the user also authorized generation, use it with the requested supported surface.
4. Apply the Quick check to reject obvious failures.
5. State that the first-wave Placeholder Preview is not a recorded run or reliability evidence. Do not call the output a Production Candidate solely because it used a Prompt Card.

## Recipe workflow

1. Collect the Recipe's required Creative Brief fields and confirm any required reference assets are authorized and available.
2. Use the Conversational Profile for supported conversational image tools or the API Profile for explicit GPT Image 2 requests.
3. Inspect the output against every Critical Invariant and the Production Candidate Rubric.
4. If it fails, apply the Recipe's narrow repair guidance and preserve the failed result in recorded evaluation work.
5. Hand the Production Candidate to the stated final-QA checks. Do not call it publish-ready without that separate evidence.

## Evidence boundary

- A Placeholder Preview is navigation material, not proof that a prompt works.
- First-wave Prompt Cards have no evidence manifest and do not inherit evidence from a linked Recipe.
- A Rendered Sample must resolve to a recorded Generation Run.
- Do not infer compatibility with an untested model or host.
- Do not run a provider, incur spend, upload private inputs, or publish an output without authority for that exact action.

## Source boundary

Treat the Source Archive as provenance infrastructure rather than a third content route. Preserve each Prompt Card's and Recipe's source posture and attribution. Do not treat a Translation or Attributed Rebuild as independently sourced, and do not reuse linked upstream images as project assets.
