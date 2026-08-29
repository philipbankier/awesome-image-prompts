# Orchard Yield Small Multiples

## Use this when

Use this card for a small, closed dataset that benefits from four panels with the same encoding. It is not for deriving values or deciding the statistical story. Use a Recipe when exact numeric reproduction, repeatability, or repair evidence is required.

## Required inputs

Provide the exact fictional data table, panel order, title, axis ranges, units, series labels, annotations, palette, legend rules, and source-owner approval.

## Prompt

```text
SCENE: Build one restrained four-panel chart page on {BACKGROUND} with {TITLE_EXACT} and a clear left-to-right reading order.
SUBJECT: Compare {ORCHARD_SERIES} across {TIME_PERIODS} using only the values in {APPROVED_DATA_TABLE}.
DETAILS: Use {CHART_TYPE} in every panel, preserve {PANEL_ORDER}, apply the shared {AXIS_RANGE} and {UNITS}, render {SERIES_LABELS} and {ANNOTATIONS} exactly, follow {LEGEND_RULES}, and use {PALETTE} with non-color reinforcement.
CONSTRAINTS: Do not calculate, interpolate, smooth, normalize, or invent values. Keep baselines and scales comparable, show no decorative fruit icons inside plotting areas, and add no source claim not supplied.
OUTPUT INTENT: Return one legible {ASPECT_RATIO} small-multiples graphic suitable for full-size review.
```

## Variables

- `{TITLE_EXACT}` and `{BACKGROUND}`: approved heading and field.
- `{APPROVED_DATA_TABLE}`: complete fictional values.
- `{ORCHARD_SERIES}` and `{TIME_PERIODS}`: exact categories and periods.
- `{CHART_TYPE}`, `{PANEL_ORDER}`, and `{AXIS_RANGE}`: chart construction.
- `{UNITS}`, `{SERIES_LABELS}`, and `{ANNOTATIONS}`: exact text manifest.
- `{LEGEND_RULES}`: approved legend content, order, placement, and encoding.
- `{PALETTE}` and `{ASPECT_RATIO}`: visual and delivery rules.

## Negative constraints

No invented data, inconsistent axes, truncated baselines, missing units, decorative 3D effects, pseudo-text, real farm identities, signatures, or watermarks.

## Quick check

Match every plotted value to the source table, compare axis limits panel by panel, transcribe all labels and units, and confirm no decoration changes perceived magnitude.

## Placeholder Preview

Sample status: Placeholder Preview. No recorded generation run.

The intended preview is a restrained four-panel comparison whose values, axes, labels, and units can be checked directly against the supplied table.

## Rights and provenance

This is an independently authored card with `original` source posture using fictional data. Supply only project-owned facts and labels. No upstream prompt body or third-party chart design is included.
