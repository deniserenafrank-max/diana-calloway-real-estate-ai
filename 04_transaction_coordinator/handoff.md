# Handoff — 04_transaction_coordinator

## What transaction coordinator receives

A new contract notification from the orchestrator or assigned agent, containing:
- The case file (with transaction section populated, or the raw contract details)
- Contract execution date
- Key dates: option period, earnest money, closing date
- Assigned agent and lender contact (if available)

Minimum required to open a transaction: contract date, option period expiry, closing date, assigned agent.

If the case file transaction section is empty: request contract details from the assigned agent. Do not begin tracking with incomplete dates.

## What transaction coordinator produces

On contract open:
1. **Deadline log** — all dates entered, status flagged, immediate actions listed
2. **Alert schedule** — option period alerts staged (48h / 24h / day-of)
3. **Checklist status** — initial pass through buyer or seller checklist

On ongoing basis:
4. **Alert messages** — triggered when deadlines approach
5. **Transaction update summaries** — for 03_client_communication to draft from

## Output format for alert messages

```
⚠️ [ALERT TYPE] — [Time window]
Transaction: [Case ID]
Client: [Name]
Property: [Address]
Deadline: [Date and time]
Time remaining: [X hours / days]

--- What needs to happen ---
[Numbered action list for assigned agent]

Routing: [Agent name] | [Diana if applicable]
```

## Routing after transaction events

| Event | Route to |
|---|---|
| Client update needed | 03_client_communication — provide update summary |
| Hard stop condition identified | Diana Calloway directly — flag immediately |
| Legal question raised | Flag to Diana — do not answer |
| Transaction closes | Update case file, mark pipeline row as Closed, notify assigned agent |

## Confidence and trail

On every outgoing envelope, set `confidence` honestly — `high` if all deadlines are confirmed and no risk flags are active; `med` if a deadline is approaching or a flag is amber; `low` if a deadline has been missed or critical data is absent. Append `04_transaction_coordinator` to the `trail` from the incoming envelope.

## Back-handoff

If key transaction data is missing and cannot be obtained:

```
back_to: orchestrator
reason: Transaction opened without [critical field]. Cannot log deadlines accurately.
needed: [Contract execution date / option period dates / closing date / lender info]
action: Assigned agent to provide before transaction tracking begins.
```
