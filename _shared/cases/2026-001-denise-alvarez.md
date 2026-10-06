# Case File — 2026-001-denise-alvarez
*File name: `_shared/cases/2026-001-denise-alvarez.md`. case_id = file name without .md.*
*Updated by each specialist as the lead/deal moves through the system.*
*This file is the single source of truth for this lead or deal.*

> **ONBOARDING TEST LEAD (Step 6 test fire).** Mock Zillow lead sent by Denise to leads@. Not a real prospect; the draft is not to be sent.

---

## Pipeline summary

```
PIPELINE SUMMARY
case_id:        2026-001-denise-alvarez
date:           2026-10-06
source:         Zillow — Contact Agent
prospect_name:  Maria Alvarez
contact:        (936) 555-0147 | maria.alvarez.testlead@example.com
lead_type:      Buyer
assigned_agent: Denise Frank
urgency:        MEDIUM
status:         New
next_action:    Review and send the Gmail draft to Maria, then call her at (936) 555-0147 Wed or Thu afternoon. Lead with Conroe vs Montgomery at up to ~$450k / 4 BR, and confirm her pre-approval amount.
draft_ready:    Yes
notes:          ONBOARDING TEST LEAD. Score 10/12 (Priority). Relocation from Dallas (husband's job in The Woodlands). Pre-approved with credit union, amount not stated. Wants to be in a house before January school start. Confirm 2412 Lakeview Dr status on HAR.com.
```

---

## Header

| Field | Value |
|---|---|
| case_id | 2026-001-denise-alvarez |
| created | 2026-10-06 11:36 CT |
| last_updated | 2026-10-06 11:36 CT |
| status | New |
| lead_type | Buyer |
| source | Zillow (Contact Agent), Path A via leads@ |
| urgency | MEDIUM (30-min SLA) |
| assigned_agent | Denise Frank |
| referring_agent | N/A (platform lead) |
| pipeline_row | Repo CSV only (`_shared/pipeline.csv`). Sheets connector lacks spreadsheet scope. |

---

## Prospect

| Field | Value |
|---|---|
| name | Maria Alvarez |
| phone | (936) 555-0147 |
| email | maria.alvarez.testlead@example.com |
| preferred_contact | Call (asked to "set up a time to talk") |
| notes | Buying with her husband. Gmail thread 1a11210b1fb6fbc1. |

---

## Intent (Buyer)

| Field | Value |
|---|---|
| lead_type | Buyer |
| pre_approved | Yes (credit union, per prospect) |
| lender | Credit union, name [TBD] |
| approval_amount | [TBD]. Confirm on first call. |
| budget_ceiling | Up to about $450,000 |
| target_areas | Conroe, Montgomery |
| property_type | House |
| bedrooms | 4 if possible |
| timeline | 1–3 months (wants to be in a house before school starts in January) |
| motivation | Relocation from Dallas for husband's job at a hospital in The Woodlands |
| currently | [TBD] |
| dealbreakers | [TBD] |
| qualification_confidence | High |

Property of interest: 2412 Lakeview Dr, Conroe, TX 77304 (Zillow listing she inquired on). Price and status [TBD]; check HAR.com.

---

## Qualification notes

```
Scores
Timeline:       2  (January target is about 3 months out; borderline 3)
Budget clarity: 3  (says pre-approved; budget about $450k. Amount not yet confirmed.)
Motivation:     3  (job relocation, a hard external deadline)
Responsiveness: 2  (first contact, but she asked for a call this week)
TOTAL: 10/12 — Priority lead.

Real buyer, not an explorer: relocation, stated budget, pre-approval, specific towns,
and she asked to talk this week. Gaps for first call: pre-approval amount and lender,
renting or owning in Dallas (contingent sale?), must-haves beyond 4 BR, school district
priorities (do not state school info unless verified).

Next action: Denise reviews and sends the draft, then calls Maria Wed or Thu afternoon.
Routing: 03_client_communication (first email drafted) → 02_property_research
(Conroe / Montgomery buyer brief, ~$450k, 4 BR) after first call.
```

---

## Interaction log

*Append each interaction. Never delete entries. Newest at top.*

| Date | Agent | Channel | Summary |
|---|---|---|---|
| 2026-10-06 | System | Email (leads@) | Zillow Contact Agent inquiry received and processed. First-reply draft created in Denise's Drafts. |

---

## Drafts produced

| Date | Specialist | Draft type | Status |
|---|---|---|---|
| 2026-10-06 | 03_client_communication | First email (Gmail draft id r-3725808623681190965) | Pending (Denise to review and send) |

Draft subject: "2412 Lakeview Dr + your move from Dallas". Asks for a Wed/Thu afternoon call; no price, timeline or outcome promises.

NOTES FOR AGENT:
- Confirm 2412 Lakeview Dr is still active on HAR.com before sending (the draft says you'll check).
- MEDIUM urgency, Zillow Contact Agent, 30-minute SLA.
- Do not add school or commute claims unless verified.

---

## Property research

| Field | Value |
|---|---|
| properties_researched | [TBD] |
| research_brief | [TBD] |

---

## Transaction (under contract)

| Field | Value |
|---|---|
| contract_date | [TBD] |
| option_period_end | [TBD] |
| financing_contingency_end | [TBD] |
| close_date | [TBD] |
| title_company | [TBD] |
| earnest_money | [TBD] |
| option_fee | [TBD] |
| purchase_price | [TBD] |
| key_contacts | Inspector: [TBD] / Lender: [TBD] / Title officer: [TBD] |

---

## Handoff history

| Date | From | To | Reason | Confidence |
|---|---|---|---|---|
| 2026-10-06 | orchestrator | lead_qualifier | New lead: Zillow Contact Agent, MEDIUM | high |
| 2026-10-06 | lead_qualifier | client_communication | Score 10/12, first email needed | high |
