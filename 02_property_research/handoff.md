# Handoff — 02_property_research

## What property research receives

A research request from 01_lead_qualifier or 00_orchestrator, containing:
- The type of research needed (neighbourhood brief, CMA, showing prep, listing prep, etc.)
- The client profile (from case file or handoff envelope)
- The property or area in question
- The urgency level (sets depth per rules.md Rule 6)

Minimum required to proceed: research type + area/property + urgency level.

If the client profile is missing, produce a generic brief and flag: "No case file found — research is not client-tailored. Run 01_lead_qualifier first for personalised output."

## What property research produces

A structured brief, labelled by type and formatted for agent use.

Every brief includes:
- A clear header identifying client, property/area, and brief type
- Sections appropriate to the brief type (see rules.md Rule 2)
- `⚠️ MLS CHECK NEEDED` flags wherever live data is required
- Agent talking points — the 3–4 lines the agent will actually say in conversation

## Output format

```
[BRIEF TYPE] — [Area / Property]
For: [Client name] | [Lead type] | [Budget or goal]

--- [Section 1] ---
[Content]

--- [Section 2] ---
[Content]

⚠️ MLS CHECK NEEDED: [What to verify]

--- Agent talking points ---
- "[Exact line the agent can say]"
- "[Exact line the agent can say]"
- "[Exact line the agent can say]"
```

## Routing after research

| After producing | Send to |
|---|---|
| Showing prep brief | 03_client_communication — draft follow-up text/email if requested |
| Listing prep brief | 03_client_communication — draft listing presentation intro if requested |
| CMA | 03_client_communication — no immediate draft needed unless requested |
| Neighbourhood brief (standalone) | Return to requester — no automatic routing |

Research does not automatically trigger communication drafts. The requester specifies whether a draft follows.

## Confidence and trail

On every outgoing envelope, set `confidence` honestly — `high` if the research is complete and findings are solid; `med` if data was limited or some questions remain open; `low` if the brief is too thin to act on and the receiver should ask before using it. Append `02_property_research` to the `trail` from the incoming envelope.

## Back-handoff

If the research request is ambiguous (no area specified, no client context, no brief type), return to the orchestrator:

```
back_to: orchestrator
reason: Research request is missing [field]. Cannot produce targeted brief without it.
```
