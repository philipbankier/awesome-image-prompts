# Observatory Event Checkout

## Use this when

Use this card for one fictional mobile checkout screen for an observatory event, with tickets, price summary, attendee details, and a clear final action. Use a Recipe for a real payment flow, legal copy, accessibility certification, or transaction validation.

## Required inputs

- Fictional event, venue, date, ticket selection, fees, and currency.
- Exact attendee fields, policy summary, button label, and allowed text.
- Visual system, device frame, payment-state treatment, and aspect ratio.

## Prompt

```text
SCENE
Create one portrait mobile checkout screen for {EVENT_NAME} at {VENUE_NAME} on {EVENT_DATE}, presented in {DEVICE_FRAME}.

SUBJECT
Show the selected tickets {TICKET_MANIFEST}, attendee section {ATTENDEE_FIELDS}, and a final total of {TOTAL_EXACT}, with one dominant action labeled {PRIMARY_ACTION}.

DETAILS
Arrange {ORDER_SUMMARY}, {FEE_BREAKDOWN}, {POLICY_SUMMARY}, and {PAYMENT_STATE} in a trustworthy hierarchy using {VISUAL_SYSTEM}. Render only {EXACT_TEXT_MANIFEST} and make every required field state explicit.

CONSTRAINTS
Keep quantities, subtotals, fees, and total mathematically consistent. Use fictional details only; show no real card number, security code, payment-provider mark, dark pattern, preselected donation, tiny pseudo-text, logo, watermark, or unapproved copy.

OUTPUT INTENT
Return one credible 9:16 mobile checkout interface at {OUTPUT_SIZE}, with the purchase summary and final action clear before submission.
```

## Variables

- `{EVENT_NAME}`: fictional event title.
- `{VENUE_NAME}`: fictional observatory or venue.
- `{EVENT_DATE}`: exact approved date and time.
- `{DEVICE_FRAME}`: approved device-frame treatment.
- `{TICKET_MANIFEST}`: ticket types, quantities, and unit prices.
- `{ATTENDEE_FIELDS}`: closed list of field labels and states.
- `{TOTAL_EXACT}`: exact currency total.
- `{PRIMARY_ACTION}`: exact final button label.
- `{ORDER_SUMMARY}`: concise ticket summary.
- `{FEE_BREAKDOWN}`: itemized subtotal and fees.
- `{POLICY_SUMMARY}`: approved cancellation or access sentence.
- `{PAYMENT_STATE}`: fictional payment method state without credentials.
- `{VISUAL_SYSTEM}`: project-owned palette, type, icons, and spacing.
- `{EXACT_TEXT_MANIFEST}`: complete allowed text list.
- `{OUTPUT_SIZE}`: final pixel dimensions.

## Negative constraints

- No real payment data, payment-provider marks, tracking consent, countdown timer, or deceptive urgency.
- No arithmetic mismatch, hidden fee, duplicate ticket, missing required field, or ambiguous final action.
- No star-field clutter behind form text, illegible policy copy, signatures, or watermarks.

## Quick check

Recalculate the total, count the tickets, confirm every required field and fee is visible, and verify the final action cannot be mistaken for a non-transactional navigation button.

## Placeholder Preview

Sample status: Placeholder Preview. No recorded generation run.

Expected result: a trustworthy fictional checkout with a compact event header, auditable price summary, and one clear purchase action.

## Rights and provenance

Use fictional event, venue, attendee, and payment information. This Prompt Card is independently authored, has source posture `original`, and includes no third-party prompt, ticketing interface, logo, or image.
