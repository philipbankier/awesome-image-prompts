---
name: image-recipe-library
description: Select, adapt, inspect, and repair evidence-backed image-generation Recipes when a user needs a product ad, reference-based edit, or structured infographic.
---

# Image Recipe Library

Use this skill to turn a Creative Brief into a Production Candidate through one canonical Recipe.

## Workflow

1. Read [references/recipe-index.md](references/recipe-index.md) and select the narrowest matching Recipe.
2. Read only that Recipe's `RECIPE.md`.
3. Collect its required Creative Brief fields and confirm any required reference assets are authorized and available.
4. Use the Conversational Profile for supported conversational image tools or the API Profile for explicit GPT Image 2 requests.
5. Inspect the output against every Critical Invariant and the Production Candidate Rubric.
6. If it fails, apply the Recipe's narrow repair guidance and preserve the failed result in recorded evaluation work.
7. Hand the Production Candidate to the stated final-QA checks. Do not call it publish-ready without that separate evidence.

## Evidence boundary

- A Placeholder Preview is navigation material, not proof that a prompt works.
- A Rendered Sample must resolve to a recorded Generation Run.
- Do not infer compatibility with an untested model or host.
- Do not run a provider, incur spend, upload private inputs, or publish an output without authority for that exact action.

## Source boundary

Preserve each Recipe's source posture and attribution. Do not treat a Translation or Attributed Rebuild as independently sourced, and do not reuse linked upstream images as project assets.
