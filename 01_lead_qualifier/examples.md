# Examples — 01_lead_qualifier

*All prospects, phone numbers, emails, and addresses below are fictional.*

---

## Example 1 — Zillow tour request (Sarah Mitchell, Score 9)

**Input (handoff envelope from orchestrator):**
```
HANDOFF ENVELOPE
source: Zillow — Schedule Tour
urgency: HIGH
sla: 5 minutes
intake_path: A
prospect_name: Sarah Mitchell
prospect_phone: (936) 555-0143
prospect_email: sarah.m@gmail.com
lead_type: Buyer (inferred)
property_of_interest: 1234 Example Oak Dr, Conroe TX | $585,000
raw_message: "Hi! Interested in this property. Is it still available? Could I get in this weekend?"
assign_to: Denise Frank
confidence: high
trail: [00_orchestrator]
```

**Lead qualifier output:**
```
QUALIFICATION SUMMARY — Sarah Mitchell

Case file: 2026-001-denise-mitchell.md (created)
Pipeline row: added

--- Scores ---
Timeline:       3  (wants to tour this weekend — active buyer)
Budget clarity: 2  (inquiring at $585k — likely in that range, pre-approval unknown)
Motivation:     2  (property-specific inquiry, no hard deadline stated)
Responsiveness: 2  (first contact via Zillow, no history)
TOTAL: 9/12 — Qualified lead. Standard follow-up.

--- Pre-approval ---
Status: Unknown
Flag for first call: Denise should ask if pre-approved, or connect with lender before offer stage.
Note: Do not block the showing — confirm availability, get pre-approval info during tour conversation.

--- Lead type ---
Buyer — confirmed (tour request on active listing).

--- Assessment ---
Warm lead. She's looking at a specific property and wants in this weekend — that's an active buyer,
not an explorer. The pre-approval gap is a first-call item, not a blocker. Confirm the listing is
still active on HAR.com before replying.

--- Next action ---
Text Sarah within 5 minutes. Confirm the weekend showing. Do not front-load with qualifying
questions — she asked about a specific property, give her an answer first.

Routing to: 03_client_communication
Draft request: Denise first text to Sarah Mitchell re: 1234 Example Oak Dr tour availability.
```

---

## Example 2 — Referral phone call (James Rodriguez, Score 12)

**Input (handoff envelope from orchestrator):**
```
HANDOFF ENVELOPE
source: Phone call (Path C — manual entry)
urgency: HIGH
sla: Immediate
intake_path: C
prospect_name: James Rodriguez
prospect_phone: (281) 555-0287
prospect_email: james.r@gmail.com
lead_type: Buyer
pre_approved: Yes
approval_amount: $720,000
target_areas: Magnolia, Spring
timeline: By September (approx 3–4 months)
motivation: Work relocation — new job in The Woodlands
assign_to: Denise Frank
notes: Warm lead — agent just spoke to them. Draft first follow-up immediately.
confidence: high
trail: [00_orchestrator]
```

**Lead qualifier output:**
```
QUALIFICATION SUMMARY — James Rodriguez

Case file: 2026-002-denise-rodriguez.md (created)
Pipeline row: added

--- Scores ---
Timeline:       3  (by September, ~90 days, hard relocation deadline)
Budget clarity: 3  (pre-approved $720k — confirmed)
Motivation:     3  (job relocation — external deadline, not lifestyle preference)
Responsiveness: 3  (just spoke to agent, warm, engaged)
TOTAL: 12/12 — Priority lead. Full investment.

--- Pre-approval ---
Status: Yes | Amount: $720,000
Note: Confirm lender name and expiry date on first written follow-up.

--- Lead type ---
Buyer — confirmed.

--- Assessment ---
Best possible score. Warm referral, hard deadline, pre-approved, clear area preference. Denise just
spoke to him — this is a close-in-progress, not a lead to nurture.

Magnolia is his first-choice area, Spring his second. Area fit at $720k should come from
02_property_research and a live HAR.com search, not from assumptions here.

--- Next action ---
Send James a follow-up email within 20 minutes. Lead with 2–3 current Magnolia listings within his
budget, pulled from HAR.com. Set a showing block for this week — he has a deadline and he knows it.

Requesting: 02_property_research — Magnolia buyer brief for James Rodriguez, $720k budget, relocation.
Routing to: 03_client_communication — draft follow-up email from Denise once research returns.
```

---

## Example 3 — Homes.com inquiry (Kevin Tran, Score 4)

**Input (handoff envelope from orchestrator):**
```
HANDOFF ENVELOPE
source: Homes.com — General Inquiry
urgency: STANDARD
sla: Same day
intake_path: A
prospect_name: Kevin Tran
prospect_phone: unknown
prospect_email: kevin.tran.tx@gmail.com
lead_type: Buyer (inferred)
raw_message: "Hey just browsing around. What's the market like right now? Still a good time to buy?"
assign_to: Denise Frank
confidence: med
trail: [00_orchestrator]
notes: No phone, no area, no budget.
```

**Lead qualifier output:**
```
QUALIFICATION SUMMARY — Kevin Tran

Case file: 2026-003-denise-tran.md (created)
Pipeline row: added

--- Scores ---
Timeline:       1  (no timeline — "just browsing")
Budget clarity: 1  (no budget, no pre-approval, no property mentioned)
Motivation:     1  (market curiosity, no specific driver)
Responsiveness: 1  (cold Homes.com inquiry, first contact)
TOTAL: 4/12 — Soft lead. First response only. Route to nurture.

--- Pre-approval ---
Status: Unknown
Note: Too early to ask. Let this come up naturally in first conversation.

--- Lead type ---
Buyer — tentative. He's asking about buying, not selling.

--- Assessment ---
Not ready. This is a market-curious person, not an active buyer. He may become one. First response
should be short and generous. Answer his market question honestly — use only market facts Denise
has supplied or verified; do not quote statistics the system cannot confirm. Do not pitch a showing.

--- Next action ---
Email Kevin today with a short, honest note on the Houston-north market (Denise to supply or verify
any figures). Offer to keep him posted on trends. Do not push for a call or showing.

Routing to: 03_client_communication — brief first response email from Denise (market update tone, no ask).
Routing to: 05_nurture_coordinator — 90-day soft touch sequence after first contact sent.
```
