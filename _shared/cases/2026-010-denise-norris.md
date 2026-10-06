# Case File — 2026-010-denise-norris
*File name: `_shared/cases/2026-010-denise-norris.md`. case_id = file name without .md.*

---

## Pipeline summary

```
PIPELINE SUMMARY
case_id:        2026-010-denise-norris
date:           2026-10-06
source:         HAR.com - Showing Request
prospect_name:  Caprice Norris
contact:        (504) 975-2911 / Capricenorris25@gmail.com
lead_type:      Rental inquiry
assigned_agent: Denise Frank
urgency:        HIGH
status:         New
next_action:    Call Caprice at (504) 975-2911 today about the 23331 Bayleaf Dr (Spring) showing; confirm showing setup with Progress, get days/times, move date and household size.
draft_ready:    Yes
notes:          Progress Residential rental listing (HAR To: mls@rentprogress.com, Denise CC'd). Timeline 1 / Budget 1 / Motivation 2 / Responsiveness 2 = 6/12 (Soft). Spring is in the core service area. 504 (New Orleans) area code: possible relocation, unconfirmed. Draft id r-8408819108831947848.
```

---

## Header

| Field | Value |
|---|---|
| case_id | 2026-010-denise-norris |
| created | 2026-10-06 13:10 CT |
| last_updated | 2026-10-06 13:10 CT |
| status | New |
| lead_type | Rental inquiry |
| source | HAR.com - Showing Request |
| urgency | HIGH |
| assigned_agent | Denise Frank |
| referring_agent | N/A (platform lead) |
| pipeline_row | Google Sheet row 11 |

---

## Prospect

| Field | Value |
|---|---|
| name | Caprice Norris |
| phone | (504) 975-2911 |
| email | Capricenorris25@gmail.com |
| preferred_contact | [TBD] |
| notes | thread 1a1122b52f99df6c; HAR lead_id 10056664. Lead generated 10/06/2026 12:02 PM CT. |

---

## Intent (Rental)

| Field | Value |
|---|---|
| lead_type | Rental inquiry |
| pre_approved | N/A (rental) |
| lender | [TBD] |
| approval_amount | [TBD] |
| budget_ceiling | [TBD] |
| target_areas | 23331 Bayleaf Dr, Spring TX 77373 (MLS 39282931) |
| property_type | House (rental) |
| bedrooms | [TBD] |
| timeline | Unknown |
| motivation | [TBD] |
| currently | [TBD] |
| dealbreakers | [TBD] |
| qualification_confidence | Low |

Properties of interest: 23331 Bayleaf Dr, Spring TX 77373 (MLS 39282931)

Prospect message: none (HAR lead carried no lead_message; subject "Consumer requests more information for 23331 Bayleaf Dr").

---

## Qualification notes

```
Scores: Timeline 1 / Budget 1 / Motivation 2 / Responsiveness 2 = 6/12 (Soft)
Progress Residential rental listing (HAR To: mls@rentprogress.com, Denise CC'd).
Flags: Spring is in the core service area. 504 (New Orleans) area code: possible relocation, unconfirmed.
Next action: Call Caprice at (504) 975-2911 today about the 23331 Bayleaf Dr (Spring) showing; confirm showing setup with Progress, get days/times, move date and household size.
Do not state Progress Residential's rent, income requirement, fees or availability as fact until confirmed from the listing or Progress.
```

---

## Interaction log

| Date | Agent | Channel | Summary |
|---|---|---|---|
| 2026-10-06 | System | Email | Lead received and processed by hourly lead processor. First-reply draft created in Denise's Drafts. |

---

## Drafts produced

| Date | Specialist | Draft type | Status |
|---|---|---|---|
| 2026-10-06 | 03_client_communication | First email (Gmail draft id r-8408819108831947848) | Pending (Denise to review and send) |

Draft subject: "Your showing request for 23331 Bayleaf Dr, Spring". To: Capricenorris25@gmail.com. Signed Denise Frank, (832) 662-0475. No price, timeline or outcome promises.

---

## Handoff history

| Date | From | To | Reason | Confidence |
|---|---|---|---|---|
| 2026-10-06 | orchestrator | lead_qualifier | New lead: HAR.com - Showing Request, HIGH | high |
| 2026-10-06 | lead_qualifier | client_communication | First email needed | high |
