# Examples — 04_transaction_coordinator

All clients, addresses, dollar amounts and dates below are fictional example values.

---

## Example 1 — New contract executed (buyer, Magnolia property, reassigned to Keith)

**Input (from orchestrator):**
```
Transaction opened: James Rodriguez — buyer
Case: 2026-002-keith-rodriguez
Property: 5678 Example Pine Ln, Magnolia TX
Contract: TREC One to Four Family Residential Contract (Resale) + Third Party Financing Addendum
Contract date: 2026-05-13
Option period: 7 days per contract (expires 2026-05-20)
Option fee: $250 (delivery per contract terms)
Earnest money: $9,000 (due to Example Title Co. within 3 days per contract)
Closing date: 2026-06-13
Assigned agent: Keith Knowlton (reassigned by Denise)
Lender: [TBD — confirm with Keith]
```

**Transaction coordinator output:**

```
TRANSACTION OPENED — 2026-002-keith-rodriguez
Property: 5678 Example Pine Ln, Magnolia TX
Buyer: James Rodriguez | Agent: Keith Knowlton (Denise oversight)

--- Deadline log ---

| Deadline | Date | Status | Notes |
|---|---|---|---|
| Option period expires | 2026-05-20 | ⏳ Pending | 7-day unrestricted termination window (per contract) |
| Option fee due | 2026-05-16 | ⏳ Pending | $250 — delivery per contract terms |
| Earnest money due | 2026-05-16 | ⏳ Pending | $9,000 to Example Title Co. — per contract |
| Third-party financing deadline | [TBD] | ⚠️ Action needed | Confirm from Third Party Financing Addendum with Keith |
| Title commitment due | [TBD] | ⚠️ Action needed | Example Title Co. to confirm delivery date |
| Closing date | 2026-06-13 | ⏳ Pending | Target — confirm with lender |
| Lender contact | [TBD] | ⚠️ Action needed | Keith to provide before 2026-05-14 |

--- Immediate actions ---

⚠️ ACTION — Keith Knowlton: Confirm lender name and contact by tomorrow (2026-05-14).
Without lender info, the financing contingency deadline cannot be logged.

⚠️ ACTION — Keith Knowlton: Ensure the $250 option fee is delivered as the contract requires by 2026-05-16.

--- Option period alert scheduled ---

Alert 1: 2026-05-18 — 48 hours before option period expires → Keith Knowlton
Alert 2: 2026-05-19 — 24 hours before option period expires → Keith Knowlton + Denise Frank
Alert 3: 2026-05-20 — Day of expiry → Keith Knowlton + Denise Frank + James Rodriguez

--- Checklist status ---
Running full buyer checklist from _config/buyer-checklist.md.
See case file _shared/cases/2026-002-keith-rodriguez.md — Transaction section for item-by-item status.
```

---

## Example 2 — Option period expiry alert

**Triggered automatically (48-hour window):**

```
⚠️ OPTION PERIOD ALERT — 48 HOURS
Transaction: 2026-002-keith-rodriguez
Client: James Rodriguez
Property: 5678 Example Pine Ln, Magnolia TX
Option expires: 2026-05-20 (Wednesday)
Time remaining: ~48 hours

Agent: Keith Knowlton

--- What needs to happen before Wednesday ---

1. Inspection results reviewed with James? [Confirm: Yes / No]
2. Any repairs or credits to negotiate? [If yes, a TREC Amendment to Contract needs to be
   drafted and signed before the option period expires]
3. James confirmed he's proceeding? [Get explicit verbal or text confirmation]
4. If terminating: TREC Notice of Buyer's Termination of Contract must be delivered before expiry

--- If James is proceeding ---
No action needed from James — the option period simply expires. Keith should confirm
his intent verbally and note it in the case file.

--- If requesting repairs or credits ---
Get the amendment moving now. Do not wait until Tuesday night.
Route to 03_client_communication if a client-facing update is needed.

--- If any doubt ---
Call Denise. This is not a deadline to miss.

Routing: Keith Knowlton (primary) | Denise Frank (cc — 24-hour alert to follow tomorrow)
```

---

## Example 3 — Transaction update summary (for 03_client_communication)

**Request:**
```
Produce transaction update summary for Denise to send to the Okonkwos (buyers).
Case: 2026-004-denise-okonkwo
Status: Inspection complete, seller agreed to $1,200 credit, option period ends Friday.
```

**Transaction coordinator output:**

```
TRANSACTION UPDATE SUMMARY — The Okonkwos
Date: 2026-05-13
Status: On track ✅

✅ Option period: Active until 2026-05-16 (Friday)
✅ Inspection: Complete — 3 items flagged (minor electrical, HVAC filter, cracked tile)
✅ Seller response: $1,200 credit at closing agreed — amendment pending signature
⏳ Earnest money: $12,000 due 2026-05-14 to Example Title Co. — CONFIRM DELIVERED
⏳ Financing contingency: Expires 2026-05-27 per Third Party Financing Addendum — lender to confirm approval by then
⏳ Closing date: 2026-06-20 — on track per lender update

Next milestone: Option period ends Friday. Amendment for $1,200 credit to be signed
by both parties before then.

Agent action before sending update to Okonkwos:
- Confirm earnest money was received by Example Title Co.
- Confirm amendment is drafted and ready for seller signature
- Do not send update until amendment is confirmed in process

Route to: 03_client_communication — draft Denise update text + follow-up email for Okonkwos
```
