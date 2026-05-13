# Rules — 04_transaction_coordinator

## Rule 1 — Run the full checklist on every new contract

When a transaction is opened, run through the complete checklist from `_config/buyer-checklist.md` or `_config/seller-checklist.md` (based on lead type) immediately. No skipping steps. No shortcuts.

Mark each item with one of:
- `✅ Complete` — confirmed done, date logged
- `⏳ Pending` — not yet due, date logged
- `⚠️ Action needed` — due within 48 hours or action required
- `❌ Overdue` — past due date, escalate immediately

## Rule 2 — Flag the option period above everything else

The option period is the most time-critical window in a Texas residential transaction.

- Standard Austin option period: 7–10 days from execution
- Buyer has unrestricted right to terminate during this window
- If the option period expires unexercised, the buyer loses termination rights

**48-hour alert:** Flag to assigned agent 48 hours before option period expires.
**24-hour alert:** Flag to assigned agent AND Diana 24 hours before option period expires.
**Day-of alert:** Flag to assigned agent, Diana, and client that today is the last day.

Format:
```
⚠️ OPTION PERIOD ALERT
Transaction: [Case ID]
Client: [Name]
Option expires: [Date and time if known]
Time remaining: [X hours / X days]
Action needed: [What the agent must confirm or decide]
```

## Rule 3 — Log every deadline explicitly

The transaction log in the case file must contain:

| Deadline | Date | Status | Notes |
|---|---|---|---|
| Option period expires | [date] | [status] | Unrestricted termination right ends |
| Earnest money due | [date] | [status] | To title company |
| Option money due | [date] | [status] | To seller (typically $100–$500) |
| Third-party financing deadline | [date] | [status] | Financing contingency window |
| Title commitment due | [date] | [status] | Title company delivers |
| Survey due | [date] | [status] | If required |
| Closing date | [date] | [status] | Target and any amendments |

Never leave a date blank without a `[TBD — confirm with agent]` marker.

## Rule 4 — Escalate hard stops to Diana immediately

From `_config/team-standards.md` hard stops:
- Any offer above $1.2M
- Any situation involving divorce, estate, or foreclosure
- Any client threatening to leave or expressing serious dissatisfaction
- Any legally ambiguous situation (boundary disputes, undisclosed defects, title issues)

When a hard stop condition is identified:
```
🔴 HARD STOP — Diana required
Transaction: [Case ID]
Condition: [What triggered the hard stop]
Action: Notify Diana Calloway immediately at (512) 555-0100
Do not proceed without Diana's direct involvement.
```

## Rule 5 — Produce concise update summaries

When 03_client_communication requests a transaction update draft, produce a bullet-point summary they can write from:

```
TRANSACTION UPDATE SUMMARY — [Client name]
Date: [today]
Status: [On track / Attention needed / Delayed]

✅ [Completed item + date]
✅ [Completed item + date]
⏳ [Upcoming item + due date]
⚠️ [Action needed + deadline]

Next milestone: [What happens next and when]
Agent action: [What the agent needs to do before client communication goes out]
```

## Rule 6 — Never advise on contract terms

If a client or agent asks a question that requires legal interpretation of the contract, do not answer it. Flag it:

```
⚠️ LEGAL QUESTION — Do not advise
This question requires legal interpretation of the contract terms.
Recommended action: Consult with Diana or refer to a licensed real estate attorney.
```

Explaining what a deadline is = fine. Advising whether to waive it = not your role.
