# Examples — 05_nurture_coordinator

All clients and details below are fictional. Any market figures referenced in a touch must come from 02_property_research or Denise at the time the touch is drafted — market context for Houston-north / Montgomery County: TO BE FILLED IN BY DENISE.

---

## Example 1 — Soft buyer on 90-day touch plan (Kevin Tran, score 4)

**Input (from 01_lead_qualifier):**
```
Routing to: 05_nurture_coordinator
Client: Kevin Tran | Buyer (tentative) | Score: 4/12
Case: 2026-005-denise-tran
Context: Market-curious, no timeline, no budget, no pre-approval. Homes.com cold inquiry.
         Mentioned Spring as an area he's "looked at a little."
First response (brief market email) already sent by Denise.
Assigned agent: Denise Frank
```

**Nurture coordinator output:**

```
NURTURE PLAN — Kevin Tran
Case: 2026-005-denise-tran
Score: 4/12 | Status: Soft lead
Assigned agent: Denise Frank

--- Touch schedule ---

Touch 1: 2026-06-13 (30 days) | Email | Spring-area buyer's market update — honest summary
  Theme: "Here's what the market is actually doing right now." No ask.
  Data: request current figures from 02_property_research when the touch is due.

Touch 2: 2026-07-13 (60 days) | Email | One Spring listing that fits a first-time buyer profile
  Theme: Show him a real listing from HAR.com and explain plainly why it's worth a look.
  Note: Spring is the only area Kevin named — anchor there until he tells us otherwise.

Touch 3: 2026-08-13 (90 days) | Email | Timing note for first-time buyers
  Theme: What the buying process looks like from first conversation to closing, so he can
  judge his own timing. Seasonal claims only if backed by data from 02_property_research.
  Soft ask: "Worth a quick 10-minute call to talk through it?"

Touch 4: 2026-11-13 (6 months) | Email | Year-end market summary for his area
  Theme: Data-driven 2026 summary (figures from 02_property_research). No ask.

Touch 5: 2027-02-13 (9 months) | Email | Getting ready to buy in 2027
  Theme: Practical first steps — talking to a lender, what pre-approval involves.
  Soft ask: "Are you still thinking about buying this year?"

Touch 6+: Quarterly | Email | Market update, seasonal notes

--- Graduation signals to watch for ---
- Kevin replies to any touch with a question about a specific property or neighborhood
- Kevin mentions a life change (lease ending, job change, relationship change)
- Kevin asks about pre-approval or financing options
- Kevin reaches out unprompted

--- Notes for Denise ---
- Kevin is cold. Do not push. Be the agent who is useful, not the agent who wants the commission.
- His Homes.com email suggests he's a digital-first researcher — email is the right medium.
- If he replies to anything, respond same day and escalate warmth accordingly.
- At 12 months with no engagement, revisit whether to continue or archive.
```

---

## Example 2 — Not-ready seller on 12-month plan (the Garcias)

**Input (from 01_lead_qualifier):**
```
Routing to: 05_nurture_coordinator
Client: The Garcias | Seller | Score: 5/12
Case: 2026-006-denise-garcia
Context: Have a 3/2 in Shenandoah. Not actively listing. Responded to a door hanger, not urgent.
         Denise had an initial call. They're thinking about selling "in the next year or two."
Assigned agent: Denise Frank
```

**Nurture coordinator output:**

```
NURTURE PLAN — The Garcias
Case: 2026-006-denise-garcia
Score: 5/12 | Status: Soft lead — seller, 1–2 year timeline
Assigned agent: Denise Frank

--- Touch schedule ---

Touch 1: 2026-08-13 (3 months) | Email | Mid-year Shenandoah market snapshot
  Theme: Honest market summary for their area. "Here's what comparable homes are
  selling for right now and how the market has shifted since we spoke."
  Data: comps from 02_property_research / HAR.com when the touch is due.
  No ask. Just information.

Touch 2: 2026-11-13 (6 months) | Email | Year-end pricing note
  Theme: What recent sales near them suggest about pricing and timing — only what the
  current data actually shows. No predictions.
  Soft ask: "Would it be useful to do a fresh CMA in early 2027?"

Touch 3: 2027-02-13 (9 months) | Email | Seller prep
  Theme: "If listing is on the radar this year, here's what to do now to be ready."
  Include 2–3 low-cost prep items (paint, decluttering, pre-listing inspection).

Touch 4: 2027-05-13 (12 months) | Call attempt (Denise personally) + email if no answer
  Theme: "A year since we talked. Checking in to see where you're at."
  Direct ask: "Has the timeline moved? I'd love to do a fresh walk-through when you're ready."

Touch 5+: Semi-annual | Email | Market update for Shenandoah sellers

--- Graduation signals to watch for ---
- Garcias ask for a CMA or want to see current pricing
- They mention a specific timeline ("we want to be out by next summer")
- They call or email Denise unprompted
- Denise drives by and notices work being done on the property (exterior update, landscaping)

--- Notes for Denise ---
- This is a long-game relationship. The Garcias are not in a rush and that's fine.
- Keep this one personal — Denise handles it start to finish.
- The door hanger is how they found us. A follow-up that feels personal (not automated) matters.
- If Touch 4 gets no response, one more attempt at 18 months, then archive.
```

---

## Example 3 — Graduation event (Kevin Tran re-engages after Touch 2)

**Triggered by: Kevin Tran replies to the Spring listing email:**
*"Hi Denise, thanks for sending this. Actually I just found out my lease is up in January —
is that enough time to buy something? Also this Spring place looks interesting."*

**Nurture coordinator output:**

```
🟢 GRADUATION SIGNAL — Kevin Tran
Case: 2026-005-denise-tran
Signal: Kevin replied to Touch 2 email. Lease ending January — hard deadline now exists.
        Expressed specific interest in the Spring listing. First engagement since initial contact.

This is a genuine graduation. Kevin has gone from "just browsing" to "lease ending in January."
His score would now be approximately 8–9/12.

Recommended action: Re-qualify immediately via 01_lead_qualifier.
Suggested urgency: HIGH — lease deadline is a real motivator.

Routing: orchestrator → 01_lead_qualifier → 03_client_communication (Denise reply to Kevin)

Note for Denise: Call Kevin if possible. Don't just reply via email. He's gone from cold to
warm in one message and the momentum is fragile. A personal call in the next hour converts
this better than an email. Do not promise him a January move-in — talk through a realistic
timeline for his situation.
```
