# Examples — 04_transaction_coordinator

---

## Example 1 — New contract executed (buyer, Mueller property)

**Input (from orchestrator):**
```
Transaction opened: James Rodriguez — buyer
Property: 2214 Simond Ave, Austin TX 78723 (Mueller)
Contract date: 2026-05-13
Option period: 7 days (expires 2026-05-20)
Option money: $250 (due to seller within 3 days)
Earnest money: $14,400 (due to Austin Title Company within 3 business days)
Closing date: 2026-06-13
Assigned agent: Marcus Webb
Lender: [TBD — confirm with Marcus]
```

**Transaction coordinator output:**

```
TRANSACTION OPENED — CASE_RODRIGUEZ_J_20260513
Property: 2214 Simond Ave, Austin TX 78723
Buyer: James Rodriguez | Agent: Marcus Webb

--- Deadline log ---

| Deadline | Date | Status | Notes |
|---|---|---|---|
| Option period expires | 2026-05-20 | ⏳ Pending | 7-day unrestricted termination window |
| Option money due | 2026-05-16 | ⏳ Pending | $250 to seller — 3 days from execution |
| Earnest money due | 2026-05-16 | ⏳ Pending | $14,400 to Austin Title — 3 business days |
| Third-party financing deadline | [TBD] | ⚠️ Action needed | Confirm financing contingency window with Marcus |
| Title commitment due | [TBD] | ⚠️ Action needed | Austin Title to confirm delivery date |
| Closing date | 2026-06-13 | ⏳ Pending | Target — confirm with lender |
| Lender contact | [TBD] | ⚠️ Action needed | Marcus to provide before 2026-05-14 |

--- Immediate actions ---

⚠️ ACTION — Marcus Webb: Confirm lender name and contact by tomorrow (2026-05-14).
Without lender info, the financing contingency deadline cannot be logged.

⚠️ ACTION — Marcus Webb: Ensure option money ($250 check to seller) is delivered by 2026-05-16.

--- Option period alert scheduled ---

Alert 1: 2026-05-18 — 48 hours before option period expires → Marcus Webb
Alert 2: 2026-05-19 — 24 hours before option period expires → Marcus Webb + Diana Calloway
Alert 3: 2026-05-20 — Day of expiry → Marcus Webb + Diana + James Rodriguez

--- Checklist status ---
Running full buyer checklist from _config/buyer-checklist.md.
See case file CASE_RODRIGUEZ_J_20260513.md — Transaction section for item-by-item status.
```

---

## Example 2 — Option period expiry alert

**Triggered automatically (48-hour window):**

```
⚠️ OPTION PERIOD ALERT — 48 HOURS
Transaction: CASE_RODRIGUEZ_J_20260513
Client: James Rodriguez
Property: 2214 Simond Ave, Austin TX 78723
Option expires: 2026-05-20 (Wednesday)
Time remaining: ~48 hours

Agent: Marcus Webb

--- What needs to happen before Wednesday ---

1. Inspection results reviewed with James? [Confirm: Yes / No]
2. Any repairs or credits to negotiate? [If yes, amendment needs to be drafted and signed
   before option period expires]
3. James confirmed he's proceeding? [Get explicit verbal or text confirmation]
4. If terminating: TREC Notice of Termination must be delivered before expiry

--- If James is proceeding ---
No action needed from James — the option period simply expires. Marcus should confirm
his intent verbally and note it in the case file.

--- If requesting repairs or credits ---
File a repair amendment now. Do not wait until Tuesday night.
Route to 03_client_communication if a client-facing update is needed.

--- If any doubt ---
Call Diana. This is not a deadline to miss.

Routing: Marcus Webb (primary) | Diana Calloway (cc — 24-hour alert to follow tomorrow)
```

---

## Example 3 — Transaction update summary (for 03_client_communication)

**Request:**
```
Produce transaction update summary for Priya to send to the Okonkwos (buyers).
Status: Inspection complete, seller agreed to $1,200 credit, option period releases Friday.
```

**Transaction coordinator output:**

```
TRANSACTION UPDATE SUMMARY — The Okonkwos
Date: 2026-05-13
Status: On track ✅

✅ Option period: Active until 2026-05-16 (Friday)
✅ Inspection: Complete — 3 items flagged (minor electrical, HVAC filter, cracked tile)
✅ Seller response: $1,200 credit at closing agreed — amendment pending signature
⏳ Earnest money: $18,500 due 2026-05-14 to Austin Title — CONFIRM DELIVERED
⏳ Financing contingency: Expires 2026-05-27 — lender to confirm clear-to-close by then
⏳ Closing date: 2026-06-20 — on track per lender update

Next milestone: Option period release Friday. Amendment for $1,200 credit to be signed
by both parties before then.

Agent action before sending update to Okonkwos:
- Confirm earnest money was received by Austin Title
- Confirm amendment is drafted and ready for seller signature
- Do not send update until amendment is confirmed in process

Route to: 03_client_communication — draft Priya update text + follow-up email for Okonkwos
```
