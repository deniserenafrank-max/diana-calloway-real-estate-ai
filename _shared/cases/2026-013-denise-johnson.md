# Case File — 2026-013-denise-johnson
*File name: `_shared/cases/2026-013-denise-johnson.md`. case_id = file name without .md.*

---

## Pipeline summary

```
PIPELINE SUMMARY
case_id:        2026-013-denise-johnson
date:           2026-10-06
source:         HAR.com - inquiry
prospect_name:  Heather Johnson
contact:        (832) 712-1503 / tennillejohnson@gmail.com
lead_type:      Rental inquiry
assigned_agent: Denise Frank
urgency:        MEDIUM
status:         Active
next_action:    Send the rental template draft, then call Heather at (832) 712-1503 about 4723 Comal River Loop (Spring 77386). Her lease ends 12/31, so ask whether she wants this home or a January move-in search; set a follow-up for early December.
draft_ready:    Yes
notes:          Progress Residential rental listing (HAR To: mls@rentprogress.com, Denise CC'd). Message: interested but current lease isn't up until 12/31. Timeline 1 / Budget 1 / Motivation 2 / Responsiveness 2 = 6/12 (Soft). Spring 77386 is in the core service area. Day 0 template email from plan '1 - Houston Rentals - NEW Lead'. Draft id r-1187221008244011240.
```

---

## Header

| Field | Value |
|---|---|
| case_id | 2026-013-denise-johnson |
| created | 2026-10-06 16:10 CT |
| last_updated | 2026-10-06 16:10 CT |
| status | Active |
| lead_type | Rental inquiry |
| source | HAR.com - inquiry |
| urgency | MEDIUM |
| assigned_agent | Denise Frank |
| referring_agent | N/A (platform lead) |
| pipeline_row | Google Sheet row 14 |

---

## Prospect

| Field | Value |
|---|---|
| name | Heather Johnson |
| phone | (832) 712-1503 |
| email | tennillejohnson@gmail.com |
| preferred_contact | [TBD] |
| notes | thread 1a112ff6155d0483; HAR lead_id 10057004. Lead generated 10/06/2026 03:54 PM CT. Email handle suggests she may also go by Tennille (unconfirmed). |

---

## Intent (Rental)

| Field | Value |
|---|---|
| lead_type | Rental inquiry |
| pre_approved | N/A (rental) |
| budget_ceiling | [TBD] |
| target_areas | 4723 Comal River Loop, Spring TX 77386 (MLS 2316832) |
| property_type | House (rental) |
| bedrooms | [TBD] |
| timeline | Current lease ends 12/31/2026; likely January 2027 move-in |
| motivation | [TBD] |
| qualification_confidence | Low |

Properties of interest: 4723 Comal River Loop, Spring TX 77386 (MLS 2316832)

Prospect message: "Good afternoon, I am interested in this property, but my current lease isn't up until 12/31."

---

## Qualification notes

```
Scores: Timeline 1 / Budget 1 / Motivation 2 / Responsiveness 2 = 6/12 (Soft)
Progress Residential rental listing (HAR To: mls@rentprogress.com, Denise CC'd).
Flags: Spring 77386 is in the core service area. Move-in is ~12 weeks out; landlords usually hold a home only 3-4 weeks, so this specific home is unlikely to still be available. Good candidate for a December follow-up and a January search.
Next action: Send the rental template draft, then call Heather at (832) 712-1503; set a follow-up for early December.
Do not state Progress Residential's rent, income requirement, fees, voucher policy or availability as fact until confirmed from the listing or Progress.
```

---

## Interaction log

| Date | Agent | Channel | Summary |
|---|---|---|---|
| 2026-10-06 | System | HAR | HAR inquiry received; processed by hourly lead processor. Day 0 rental template draft created in Denise's Drafts. |

---

## Drafts produced

| Date | Specialist | Draft type | Status |
|---|---|---|---|
| 2026-10-06 | action plan rental-new (step 0) | "Your rental home inquiry" template #159 (Gmail draft id r-1187221008244011240) | Pending (Denise to review and send) |

To: tennillejohnson@gmail.com. Merge field set to "Heather". Template used word for word.

---

## Action plan

plan: 1 - Houston Rentals - NEW Lead (rental-new). Day 0 email drafted; stage step -> Active. Next plan: 1 - Houston Rentals - Active Lead (waiting for Follow Up Boss export). Lead Book NOT updated this run (ArtifactData write denied); plan state not recorded there.

---

## Handoff history

| Date | From | To | Reason | Confidence |
|---|---|---|---|---|
| 2026-10-06 | orchestrator | lead_qualifier | New lead: HAR.com - inquiry, MEDIUM | high |
| 2026-10-06 | lead_qualifier | client_communication | Rental lead: Day 0 action-plan template | high |
