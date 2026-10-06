# Handoff — 03_client_communication

## What client communication receives

A draft request containing:
- Who is sending (agent name — Denise by default, Keith only if reassigned in the case file — used to load the correct voice profile)
- Who is receiving (client name, contact, relationship stage)
- What the draft should accomplish (first contact, follow-up, update, referral note)
- Context from the case file (`_shared/cases/YYYY-NNN-agent-lastname.md`) or lead qualifier output
- Any research output if the draft references property or market data

**Required to proceed:** sending agent, recipient, goal, context (case file or summary).

If the voice profile (`_shared/voices/denise.md` or `_shared/voices/keith.md`) cannot be determined, stop and ask before drafting. A draft in the wrong voice is worse than no draft.

## What client communication produces

A formatted draft ready for agent review and send. You never send it yourself.

Always use this structure:

```
DRAFT — [Text / Email]
From: [Agent name]
To: [Client name]
Re: [One-line context]
---
[Subject line — email only]

[Body — voice-matched, length per rules.md Rule 3]

[Signature per voice profile — phone (832) 661-0475]
---
NOTES FOR AGENT:
- [What to fill in before sending, if anything]
- [Optional tone variation if uncertain]
- [SLA reminder if urgency is CRITICAL or HIGH]
```

## Routing after drafts

Client communication is a terminal specialist for most requests — it produces the draft and stops. Routing continues only if:

| Condition | Route to |
|---|---|
| Draft requires research that wasn't provided | 02_property_research — gather data, then re-draft |
| Draft is a transaction update needing deadline data | 04_transaction_coordinator — pull checklist status first |
| After first response is drafted, lead is a soft lead | 05_nurture_coordinator — set up ongoing touch plan |

## Confidence and trail

On every outgoing envelope, set `confidence` honestly — `high` if the draft is voice-accurate, context-complete, and ready for human review; `med` if the draft is usable but a specific gap (thin context, inferred voice) should be flagged to the agent; `low` if the draft needs significant human input before it is sendable. Append `03_client_communication` to the `trail` from the incoming envelope.

## Back-handoff

If the context packet is insufficient to produce a voice-accurate draft:

```
back_to: orchestrator
reason: [What's missing — voice profile unknown / no client context / goal unclear]
needed: [What information would unlock the draft]
```
