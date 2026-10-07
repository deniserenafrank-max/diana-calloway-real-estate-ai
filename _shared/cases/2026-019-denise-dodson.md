# Case File — 2026-019-denise-dodson
*File name: `_shared/cases/2026-019-denise-dodson.md`. case_id = file name without .md.*

---

## Pipeline summary

```
PIPELINE SUMMARY
case_id:        2026-019-denise-dodson
date:           2026-10-07
source:         HAR.com - Showing Request
prospect_name:  Ann Marie Dodson
contact:        (346) 552-1307 / annmarie_dodson@icloud.com
lead_type:      Rental inquiry
assigned_agent: Denise Frank
urgency:        HIGH
status:         Active
next_action:    Call Ann Marie at (346) 552-1307 this morning about her showing request for 23903 Lestergate Dr (Spring 77373); confirm showing setup with Progress, get days/times and move-in date. Send the rental template draft.
draft_ready:    Yes
notes:          Progress Residential rental listing (HAR To: mls@rentprogress.com, Denise CC'd). MLS 86437010. HAR lead 10057955, generated 10/07 9:10 AM CT. HAR message: "We are interested in this home" ("we": likely more than one applicant). Timeline 1 / Budget 1 / Motivation 2 / Responsiveness 2 = 6/12 (Soft). Spring 77373 is in the core service area. Day 0 template email from plan '1 - Houston Rentals - NEW Lead'. Draft id r5067803419518609079.
```

---

## Header

| Field | Value |
|---|---|
| case_id | 2026-019-denise-dodson |
| created | 2026-10-07 10:10 CT |
| last_updated | 2026-10-07 10:10 CT |
| status | Active |
| lead_type | Rental inquiry |
| source | HAR.com - Showing Request |
| urgency | HIGH |
| assigned_agent | Denise Frank |
| referring_agent | N/A (platform lead) |
| pipeline_row | Google Sheet row 20 |

---

## Prospect

| Field | Value |
|---|---|
| name | Ann Marie Dodson |
| phone | (346) 552-1307 |
| email | annmarie_dodson@icloud.com |
| preferred_contact | [TBD] |
| notes | thread/message 1a116b41f8f6be96; HAR lead_id 10057955. Lead generated 10/07/2026 9:10 AM CT. Agent status unknown. |

---

## Intent (Rental)

| Field | Value |
|---|---|
| lead_type | Rental inquiry |
| pre_approved | N/A (rental) |
| budget_ceiling | [TBD] |
| target_areas | 23903 Lestergate Dr, Spring TX 77373 (MLS 86437010) |
| property_type | House (rental) |
| bedrooms | [TBD] |
| timeline | [TBD] |
| motivation | [TBD] |
| qualification_confidence | Low |

Properties of interest: 23903 Lestergate Dr, Spring TX 77373 (MLS 86437010)

Prospect message: "We are interested in this home"

---

## Qualification notes

```
Scores: Timeline 1 / Budget 1 / Motivation 2 / Responsiveness 2 = 6/12 (Soft)
Progress Residential rental listing (HAR To: mls@rentprogress.com, Denise CC'd).
Showing request = active renter signal; HIGH urgency, 30 min SLA. "We" suggests a household / co-applicant.
Spring 77373 is in the core service area.
Do not state Progress Residential's rent, income requirement, fees, pet policy, voucher policy or availability as fact until confirmed from the listing or Progress.
```

---

## Interaction log

| Date | Agent | Channel | Summary |
|---|---|---|---|
| 2026-10-07 | System | HAR | HAR showing request received 9:11 AM CT; processed by hourly lead processor. Day 0 rental template draft created in Denise's Drafts. |

---

## Drafts produced

| Date | Specialist | Draft type | Status |
|---|---|---|---|
| 2026-10-07 | action plan rental-new (step 0) | "Your rental home inquiry" template #159 (Gmail draft id r5067803419518609079) | Pending (Denise to review and send) |

To: annmarie_dodson@icloud.com. Merge field set to "Ann Marie". Template used word for word.

---

## Action plan

plan: 1 - Houston Rentals - NEW Lead (rental-new). Day 0 email drafted; stage step -> Active. Next plan: 1 - Houston Rentals - Active Lead (waiting for Follow Up Boss export). Lead Book NOT updated this run (ArtifactData write denied by permission check); plan state not recorded there.

---

## Handoff history

| Date | From | To | Reason | Confidence |
|---|---|---|---|---|
| 2026-10-07 | orchestrator | lead_qualifier | New lead: HAR.com - Showing Request, HIGH | high |
| 2026-10-07 | lead_qualifier | client_communication | Rental lead: Day 0 action-plan template | high |
