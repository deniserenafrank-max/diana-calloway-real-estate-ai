# Handoff — 00_orchestrator

## What the orchestrator receives

Any raw input: an email from the leads@ inbox, a plain-English description from a team member, a forwarded message, or a structured form submission.

There is no required format for input. The orchestrator's job is to make sense of whatever arrives.

## What the orchestrator produces

A structured handoff envelope passed to the receiving specialist. Every envelope contains:

```
HANDOFF ENVELOPE
source:           [platform or intake path]
urgency:          [CRITICAL / HIGH / MEDIUM / STANDARD]
sla:              [time window for response]
intake_path:      [A / B / C]
prospect_name:    [full name if known]
prospect_phone:   [if known]
prospect_email:   [if known]
lead_type:        [Buyer / Seller / Unknown]
assign_to:        [agent name — from team-standards.md assignment defaults]
raw_message:      [original text from email or team member, unmodified]
notes:            [anything else the receiving specialist needs to know]
```

**Required fields:** source, urgency, intake_path, assign_to, raw_message
**Optional fields:** all others — mark as "unknown" if not available. Never omit a field entirely.

## Missing field protocol

If urgency cannot be determined from the source: default to MEDIUM.
If assign_to cannot be determined: flag it. Ask the team member to confirm before routing.
If lead_type is genuinely ambiguous: mark as "Unknown" and let 01_lead_qualifier determine it.

## Who receives the handoff

| Handoff to | When |
|---|---|
| 01_lead_qualifier | Every new lead, without exception |
| 02_property_research | Property or neighbourhood research request |
| 03_client_communication | Draft request — always paired with a complete context packet |
| 04_transaction_coordinator | Contract executed — include the full case file |
| 05_nurture_coordinator | Lead qualifier outputs "not ready" flag |

## Back-handoff

If a specialist determines the routing was wrong, it returns the envelope to the orchestrator with a `back_to: orchestrator` flag and a one-line reason. The orchestrator re-routes.
