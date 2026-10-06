# Examples — 00_orchestrator

*All prospects, phone numbers, emails, and addresses below are fictional.*

---

## Example 1 — Zillow tour request (Path A, HIGH urgency)

**Input (email in leads@ inbox):**
```
FROM: Zillow [inquiries@zillow.com]
SUBJECT: New inquiry from Sarah M. about 1234 Example Oak Dr

Prospect: Sarah Mitchell | (936) 555-0143 | sarah.m@gmail.com
Action: Schedule a Tour
Message: "Hi! Interested in this property. Is it still available? Could I get in this weekend?"
Property: 1234 Example Oak Dr, Conroe TX | $585,000 | 3/2 | 1,450sqft
```

**Orchestrator output:**
```
⚠️ HIGH — Zillow tour request. 5-minute SLA.

Routing to: 01_lead_qualifier

HANDOFF ENVELOPE
source: Zillow — Schedule Tour
urgency: HIGH
sla: 5 minutes
intake_path: A
prospect_name: Sarah Mitchell
prospect_phone: (936) 555-0143
prospect_email: sarah.m@gmail.com
lead_type: Buyer (inferred — property inquiry)
property_of_interest: 1234 Example Oak Dr, Conroe TX | $585,000
raw_message: "Hi! Interested in this property. Is it still available? Could I get in this weekend?"
assign_to: Denise Frank
confidence: high
trail: [00_orchestrator]
```

---

## Example 2 — Manual entry, phone call (Path C, HIGH urgency)

**Input (team member types in Claude):**
```
New lead — just got off the phone with James Rodriguez, buyer, preapproved for $720k,
wants Magnolia or Spring, needs to be in by September, relocating from Dallas for a new job in The Woodlands.
His number is 281-555-0287, email james.r@gmail.com
```

**Orchestrator output:**
```
⚠️ HIGH — Referral/phone lead. Warm. Route now.

Routing to: 01_lead_qualifier

HANDOFF ENVELOPE
source: Phone call (Path C — manual entry)
urgency: HIGH
sla: Immediate — agent has context, draft first response before they cool off
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
notes: Warm lead — agent just spoke to them. Qualify and draft first follow-up immediately.
confidence: high
trail: [00_orchestrator]
```

---

## Example 3 — Multi-specialist request

**Input:**
```
I need to prep for a showing tomorrow at 5678 Example Pine Ln, Montgomery TX. Buyers are the Okonkwos —
pre-approved $680k, two kids, care about schools. Can you get me a research brief
and then draft a follow-up text to send after the showing?
```

**Orchestrator output:**
```
Two tasks. Running in sequence.

Step 1 → 02_property_research
Showing prep brief on 5678 Example Pine Ln, Montgomery TX. Client profile: family with two kids, school priority, $680k budget.

Step 2 → 03_client_communication (after research complete)
Draft post-showing follow-up text for Denise to send to the Okonkwos.

Starting Step 1 now.
```
