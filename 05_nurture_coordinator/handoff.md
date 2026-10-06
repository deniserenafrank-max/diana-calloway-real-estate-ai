# Handoff — 05_nurture_coordinator

## What nurture coordinator receives

A "not ready" flag from 01_lead_qualifier, containing:
- The case file (`_shared/cases/YYYY-NNN-agent-lastname.md`, with whatever qualification data was gathered)
- The lead score and reason for nurture routing
- The first-response status (was a first message already sent by 03_client_communication?)
- The assigned agent (Denise by default; Keith if reassigned)

Minimum required to build a touch plan: lead score, area of interest (even if vague), assigned agent, first-contact status.

If the case file has no client profile information at all, build a minimal plan (quarterly, market updates only) and flag to the assigned agent that this lead will need personalization once more data is gathered.

## What nurture coordinator produces

On intake:
1. **Touch plan** — dated schedule, medium, theme, and cadence per rules.md Rule 4
2. **Graduation signal list** — specific indicators for this client that signal readiness
3. **Notes for assigned agent** — what to know about the relationship

On ongoing basis:
4. **Touch briefs** — one per touch, sent to 03_client_communication when the touch date arrives
5. **Graduation alerts** — flagged to orchestrator when a graduation signal is detected

## Touch brief format (for 03_client_communication)

```
TOUCH BRIEF — [Client name] | Touch [number]
Case: [Case ID]
Date: [today]
Assigned agent: [Name]
Medium: [Text / Email]
Tone: [Informational / Warm / Light check-in]

Value to deliver:
[One specific piece of information or content — what the agent is sharing]

Optional soft ask (if any):
[One question, maximum — or none if the touch is pure value]

Voice profile: _shared/voices/denise.md or _shared/voices/keith.md

Context for the drafter:
[What the client said last time, what they care about, what to reference]
```

## Routing after nurture events

| Event | Route to |
|---|---|
| Touch is due | 03_client_communication — provide touch brief |
| Graduation signal detected | orchestrator → 01_lead_qualifier |
| Lead goes 24 months without engagement | Flag to assigned agent — archive or final reactivation |
| Assigned agent changes (e.g. Denise reassigns to Keith, or takes a lead back) | Update case file and touch plan — do not miss scheduled touches during transition |

## Confidence and trail

On every outgoing envelope, set `confidence` honestly — `high` if the touch plan is active and contact details are current; `med` if the lead has gone quiet and the next touch is speculative; `low` if contact details are stale or engagement has dropped to zero and the agent should decide whether to continue. Append `05_nurture_coordinator` to the `trail` from the incoming envelope.

## Back-handoff

Nurture coordinator does not back-handoff — it is a long-running function, not a single-pass workflow. If a fundamental problem is found with the nurture plan (no contact info, case file deleted, assigned agent no longer with the brokerage), flag to the orchestrator with a note:

```
flag_to: orchestrator
case: [Case ID]
issue: [What has changed that affects the nurture plan]
action_needed: [What the team needs to decide]
```
