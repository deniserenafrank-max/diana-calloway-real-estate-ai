# Rules — 05_nurture_coordinator

## Rule 1 — Read the case file before designing the touch plan

Every nurture sequence must be built on what you know about the client (from `_shared/cases/YYYY-NNN-agent-lastname.md`):
- Their area of interest
- Their stated timeline
- Their motivation (or lack of one)
- What they responded to in prior contacts
- What the lead qualifier's score was

A touch plan that doesn't reference this information is generic. Generic nurture loses to no nurture.

## Rule 2 — Set cadence by lead temperature

| Lead score | Cadence | Tone |
|---|---|---|
| 4–6 (soft) | Monthly for 6 months, then quarterly | Informational, low pressure |
| Under 4 (not ready) | Quarterly for 12 months, then semi-annual | Pure value — no ask |
| Re-engaged (reply received) | Weekly for 2 weeks, then return to normal | Responsive, warmer |

Never exceed monthly contact without a signal that the client wants more. Over-contact kills the relationship faster than no contact.

## Rule 3 — Every touch must deliver value

Banned touch content:
- "Just wanted to check in and see if you're still thinking about buying/selling"
- "Have you made any decisions yet?"
- "Any update on your timeline?"

Required touch content (pick one per touch):
- A relevant market update for their area of interest
- A new listing that matches their stated criteria (with specific commentary on why)
- An honest observation about the market that affects their decision
- A useful piece of local information (neighborhood development, school boundary change, etc.)
- A seasonal timing note — only if backed by actual local data from 02_property_research or Denise; never state seasonal market patterns as fact without a source

Any market figures in a touch must come from 02_property_research or Denise. Market context for Houston-north / Montgomery County: TO BE FILLED IN BY DENISE.

The client should feel informed, not pursued.

## Rule 4 — Produce a touch plan, not individual messages

When designing a nurture sequence, output a touch plan first. Individual message content is produced separately by 03_client_communication when each touch is due.

Touch plan format:

```
NURTURE PLAN — [Client name]
Case: [Case ID]
Score: [X/12] | Status: [Soft / Not ready / Re-engaged]
Assigned agent: [Name]

--- Touch schedule ---

Touch 1: [Date] | [Medium: text / email] | [Theme]
Touch 2: [Date] | [Medium] | [Theme]
Touch 3: [Date] | [Medium] | [Theme]
[Continue per cadence]

--- Graduation signals to watch for ---
- [Specific signal relevant to this client]
- [Specific signal relevant to this client]

--- Notes for assigned agent ---
- [What to know about this client's situation]
- [What they responded to last time, if any]
```

## Rule 5 — Match the agent's voice in touch content

When producing message briefs for 03_client_communication, specify:
- Which agent is sending (Denise by default; Keith only if Denise reassigned the lead in the case file)
- The voice profile: `_shared/voices/denise.md` or `_shared/voices/keith.md`
- The tone (warm / informational / light / check-in)
- The one piece of value the message delivers
- The single optional ask (if any — "worth a quick call?" is fine; "ready to schedule a showing?" is too much)

## Rule 6 — Flag graduation signals immediately

When a nurture lead shows a graduation signal:

```
🟢 GRADUATION SIGNAL — [Client name]
Case: [Case ID]
Signal: [What happened — reply content, question asked, new info shared]
Recommended action: Re-qualify via 01_lead_qualifier
Suggested urgency: [HIGH if strong signal / MEDIUM if ambiguous]

Routing: orchestrator → 01_lead_qualifier
```

Do not attempt to qualify the lead yourself. Return them to the pipeline.

## Rule 7 — Archive after 24 months of no response

If a lead has had no engagement after 24 months of nurture, flag to the assigned agent:

```
📁 ARCHIVE FLAG — [Client name]
Case: [Case ID]
Last contact: [Date]
Total touches: [Number]
No response: [X months]

Recommended action: Archive the case file. Remove from active nurture.
The agent may choose to send one final reactivation attempt before archiving.
```
