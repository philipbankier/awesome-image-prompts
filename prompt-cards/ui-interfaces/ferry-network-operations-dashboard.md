# Ferry Network Operations Dashboard

## Use this when

Use this card for one fictional desktop operations dashboard showing a regional ferry network, vessel status, route disruptions, and dispatch priorities. Use a Recipe for live operational use, safety decisions, or validated information architecture.

## Required inputs

- Fictional network, terminals, routes, and vessels.
- Approved status values, disruptions, schedule window, and priority action.
- Exact labels, map extent, visual system, screen size, and aspect ratio.

## Prompt

```text
SCENE
Create one desktop operations dashboard for {NETWORK_NAME} during {OPERATING_WINDOW}, viewed in a controlled dispatch room.

SUBJECT
Show the network map across {MAP_EXTENT}, with {ROUTE_MANIFEST}, {VESSEL_MANIFEST}, and the priority incident {PRIORITY_INCIDENT} clearly distinguished.

DETAILS
Arrange {NETWORK_SUMMARY}, {ARRIVAL_TABLE}, {ALERT_QUEUE}, and {WEATHER_STATUS} around the map using {VISUAL_SYSTEM}. Render only {EXACT_TEXT_MANIFEST}; use redundant color, shape, and label encoding for every service state.

CONSTRAINTS
Keep route lines, vessel positions, terminal names, timestamps, and status counts internally consistent. No real navigation data, invented safety advice, decorative charts, map-provider branding, tiny pseudo-text, logos, watermarks, or unapproved labels.

OUTPUT INTENT
Return one information-dense 16:9 desktop dashboard at {OUTPUT_SIZE}, with network health, disruptions, and the next dispatch action readable without changing screens.
```

## Variables

- `{NETWORK_NAME}`: fictional ferry operator name.
- `{OPERATING_WINDOW}`: exact date and time range.
- `{MAP_EXTENT}`: fictional coastal geography and terminal bounds.
- `{ROUTE_MANIFEST}`: route names, endpoints, and service states.
- `{VESSEL_MANIFEST}`: vessel names, assigned routes, and status.
- `{PRIORITY_INCIDENT}`: one approved disruption and response state.
- `{NETWORK_SUMMARY}`: closed list of operational totals.
- `{ARRIVAL_TABLE}`: exact rows, columns, and values.
- `{ALERT_QUEUE}`: ordered alerts with severity and timestamp.
- `{WEATHER_STATUS}`: approved conditions without safety interpretation.
- `{VISUAL_SYSTEM}`: project-owned colors, type, icons, and grid.
- `{EXACT_TEXT_MANIFEST}`: complete allowed text list.
- `{OUTPUT_SIZE}`: final pixel dimensions.

## Negative constraints

- No real company, vessel, port, chart, tracking data, or emergency guidance.
- No mismatched route colors, impossible vessel positions, duplicate terminals, or contradictory times.
- No unlabeled status color, ornamental gauges, unreadable tables, browser chrome, signatures, or watermarks.

## Quick check

Trace each vessel to one route, compare all summary counts with the table, confirm the priority alert is dominant, and verify that service states remain understandable without color alone.

## Placeholder Preview

Sample status: Placeholder Preview. No recorded generation run.

Expected result: a credible fictional dispatch view with one central network map, aligned status panels, and a clearly prioritized disruption.

## Rights and provenance

Use only fictional network geography, schedules, vessel names, and operational data. This Prompt Card is independently authored, has source posture `original`, and includes no third-party prompt, map, interface, or image.
