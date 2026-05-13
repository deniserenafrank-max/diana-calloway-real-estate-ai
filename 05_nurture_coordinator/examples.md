# Examples — 05_nurture_coordinator

---

## Example 1 — Soft buyer on 90-day touch plan (Kevin Tran, score 4)

**Input (from 01_lead_qualifier):**
```
Routing to: 05_nurture_coordinator
Client: Kevin Tran | Buyer (tentative) | Score: 4/12
Context: Market-curious, no timeline, no budget, no pre-approval. Homes.com cold inquiry.
First response (brief market email) already sent by Marcus.
Assigned agent: Marcus Webb
```

**Nurture coordinator output:**

```
NURTURE PLAN — Kevin Tran
Case: CASE_TRAN_K_20260513
Score: 4/12 | Status: Soft lead
Assigned agent: Marcus Webb

--- Touch schedule ---

Touch 1: 2026-06-13 (30 days) | Email | Austin buyer's market update — honest summary
  Theme: "Here's what the market is actually doing right now." No ask.

Touch 2: 2026-07-13 (60 days) | Email | One Mueller listing that fits a first-time buyer profile
  Theme: Show him what $550–620k buys in Austin today. Commentary on why the value is real.
  Note: Kevin mentioned no specific area — Mueller is a good anchor because it's walkable
  and accessible to someone "just browsing."

Touch 3: 2026-08-13 (90 days) | Email | Fall market timing note
  Theme: "Fall is historically when Austin inventory peaks and competition drops. If you're
  thinking about buying in the next 6 months, fall showing season is worth knowing about."
  Soft ask: "Worth a quick 10-minute call to talk through it?"

Touch 4: 2026-11-13 (6 months) | Email | Year-end Austin market summary
  Theme: Data-driven 2026 summary. No ask.

Touch 5: 2027-02-13 (9 months) | Email | Spring listings are about to surge
  Theme: "Spring is Austin's busiest buying season. Here's what's expected."
  Soft ask: "Are you still thinking about buying this year?"

Touch 6+: Quarterly | Email | Market update, seasonal notes

--- Graduation signals to watch for ---
- Kevin replies to any touch with a question about a specific property or neighbourhood
- Kevin mentions a life change (lease ending, job change, relationship change)
- Kevin asks about pre-approval or financing options
- Kevin reaches out unprompted

--- Notes for Marcus ---
- Kevin is cold. Do not push. Be the agent who is useful, not the agent who wants the commission.
- His Homes.com email suggests he's a digital-first researcher — email is the right medium.
- If he replies to anything, respond same day and escalate warmth accordingly.
- At 12 months with no engagement, revisit whether to continue or archive.
```

---

## Example 2 — Not-ready seller on 12-month annual plan (Garcia estate conversation)

**Input (from 01_lead_qualifier):**
```
Routing to: 05_nurture_coordinator
Client: The Garcias | Seller | Score: 5/12
Context: Have a 3/2 in 78745. Not actively listing. Responded to a door hanger, not urgent.
         Diana had an initial call. They're thinking about selling "in the next year or two."
Assigned agent: Diana Calloway
```

**Nurture coordinator output:**

```
NURTURE PLAN — The Garcias
Case: CASE_GARCIA_20260513
Score: 5/12 | Status: Soft lead — seller, 1–2 year timeline
Assigned agent: Diana Calloway

--- Touch schedule ---

Touch 1: 2026-08-13 (3 months) | Email | Mid-year 78745 market snapshot
  Theme: Honest market summary for South Austin sellers. "Here's what comparable homes are
  selling for right now and how the market has shifted since we spoke."
  No ask. Just information.

Touch 2: 2026-11-13 (6 months) | Email | Year-end pricing note
  Theme: "Spring listings in Austin tend to attract more buyers. Sellers who list February–April
  often see stronger offers. Something to consider as you think about timing."
  Soft ask: "Would it be useful to do a fresh CMA in early 2027?"

Touch 3: 2027-02-13 (9 months) | Email | Spring prep for sellers
  Theme: "Spring is 6 weeks away. If listing is on the radar, here's what to do now to
  be ready." Include 2–3 low-cost prep items (paint, staging, inspection).

Touch 4: 2027-05-13 (12 months) | Call attempt (Diana personally) + email if no answer
  Theme: "A year since we talked. Checking in to see where you're at."
  Direct ask: "Has the timeline moved? I'd love to do a fresh walk-through when you're ready."

Touch 5+: Semi-annual | Email | Market update for 78745 sellers

--- Graduation signals to watch for ---
- Garcias ask for a CMA or want to see current pricing
- They mention a specific timeline ("we want to be out by next summer")
- They call or email Diana unprompted
- Diana drives by and notices work being done on the property (exterior update, landscaping)

--- Notes for Diana ---
- This is a long-game relationship. The Garcias are not in a rush and that's fine.
- Diana should keep this one personal — do not hand off to Priya until they're actively listing.
- The door hanger is how they found us. A follow-up that feels personal (not automated) matters.
- If Touch 4 gets no response, one more attempt at 18 months, then archive.
```

---

## Example 3 — Graduation event (Kevin Tran re-engages after Touch 2)

**Triggered by: Kevin Tran replies to Mueller listing email:**
*"Hey Marcus, thanks for sending this. Actually I just found out my lease is up in January —
is that enough time to buy something? Also this Mueller place looks interesting."*

**Nurture coordinator output:**

```
🟢 GRADUATION SIGNAL — Kevin Tran
Case: CASE_TRAN_K_20260513
Signal: Kevin replied to Touch 2 email. Lease ending January — hard deadline now exists.
        Expressed specific interest in a Mueller listing. First engagement since initial contact.

This is a genuine graduation. Kevin has gone from "just browsing" to "lease ending in January."
His score would now be approximately 8–9/12.

Recommended action: Re-qualify immediately via 01_lead_qualifier.
Suggested urgency: HIGH — lease deadline is a real motivator.

Routing: orchestrator → 01_lead_qualifier → 03_client_communication (Marcus reply to Kevin)

Note for Marcus: Call Kevin if possible. Don't just reply via email. He's gone from cold to
warm in one message and the momentum is fragile. A personal call in the next hour converts
this better than an email.
```
