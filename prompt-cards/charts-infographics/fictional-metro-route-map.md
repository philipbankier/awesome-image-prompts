# Fictional Metro Route Map

## Use this when

Use this card when every line, station, transfer, branch, and label has already been approved. It is for a schematic diagram, not a geographic or journey-planning claim. Use the linked Recipe when topology, exact text, accessibility, or repair needs recorded inspection.

## Required inputs

Provide the fictional network name, ordered station list for each route, transfer pairs, terminal stations, route colors, accessibility encoding, title, legend labels, aspect ratio, and exclusions.

## Prompt

```text
SCENE: Present one clean schematic transit-map canvas on {BACKGROUND}, with {TITLE_EXACT} at {TITLE_POSITION}.
SUBJECT: Diagram the fictional network {NETWORK_NAME} using only the ordered routes in {ROUTE_GRAPH} and transfers in {TRANSFER_LIST}.
DETAILS: Render every station name from {STATION_LABELS} exactly once, preserve route order and branch structure, mark {TERMINALS}, use {ROUTE_COLORS}, reinforce transfers and accessible stations with {NON_COLOR_ENCODING}, and render {LEGEND_LABELS_EXACT} exactly in the compact legend.
CONSTRAINTS: Do not add, remove, rename, reorder, or merge stations. Do not imply geographic scale, travel time, fares, or real-world affiliation. Keep labels horizontal, legible, and clear of lines and nodes. Also avoid {MUST_AVOID}.
OUTPUT INTENT: Return one finished {ASPECT_RATIO} landscape schematic with a compact legend and enough margin for inspection.
```

## Variables

- `{NETWORK_NAME}`: approved fictional network name.
- `{TITLE_EXACT}` and `{TITLE_POSITION}`: exact heading and placement.
- `{ROUTE_GRAPH}`: ordered station sequence for every line and branch.
- `{TRANSFER_LIST}`: exact station-to-station transfer relationships.
- `{STATION_LABELS}` and `{TERMINALS}`: closed text and endpoint manifests.
- `{ROUTE_COLORS}` and `{NON_COLOR_ENCODING}`: accessible line and node system.
- `{LEGEND_LABELS_EXACT}`: exact approved legend strings.
- `{MUST_AVOID}`: additional project-specific exclusions.
- `{BACKGROUND}` and `{ASPECT_RATIO}`: delivery field and crop.

## Negative constraints

No real transit logos, geographic base map, decorative pseudo-stations, duplicated labels, disconnected lines, false transfers, color-only meaning, signatures, or watermarks.

## Quick check

Trace every route terminal to terminal, verify every transfer from both lines, transcribe every station label, and confirm the legend matches the diagram without relying on color alone.

## Placeholder Preview

Sample status: Placeholder Preview. No recorded generation run.

The intended preview is a clean fictional network schematic with legible labels, traceable routes, and redundant non-color encoding.

## Rights and provenance

This card and prompt are independently authored with `original` source posture. Use only fictional route data, project-owned visual rules, and authorized exact text. It does not reproduce an upstream prompt or map.
