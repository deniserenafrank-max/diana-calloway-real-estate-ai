# Case File — 2026-020-denise-galvan
*File name: `_shared/cases/2026-020-denise-galvan.md`. case_id = file name without .md.*

---

## Pipeline summary

```
PIPELINE SUMMARY
case_id:        2026-020-denise-galvan
date:           2026-10-07
source:         HAR.com - Showing Request
prospect_name:  Jasmine Galvan
contact:        (832) 375-9421 / jasleanjayjasmine@yahoo.com
lead_type:      Rental inquiry
assigned_agent: Denise Frank
urgency:        HIGH
status:         Active
next_action:    Call Jasmine at (832) 375-9421 now (she sent a second showing request at 1:20 PM) about her showing request for 19523 Elmtree Estates Dr (Katy 77449); confirm showing setup with Progress, get days/times and move-in date. Send the rental template draft.
draft_ready:    Yes
notes:          Progress Residential rental listing (HAR To: mls@rentprogress.com, Denise CC'd). MLS 36711957. HAR lead 10058098, generated 10/07 10:16 AM CT. No message in HAR lead. Timeline 1 / Budget 1 / Motivation 2 / Responsiveness 2 = 6/12 (Soft). Katy 77449 is outside the core Montgomery County service area. Day 0 template email from plan '1 - Houston Rentals - NEW Lead'. Draft id r626260276462542546.
```

---

## Header

| Field | Value |
|---|---|
| case_id | 2026-020-denise-galvan |
| created | 2026-10-07 11:10 CT |
| last_updated | 2026-10-07 14:10 CT |
| status | Active |
| lead_type | Rental inquiry |
| source | HAR.com - Showing Request |
| urgency | HIGH |
| assigned_agent | Denise Frank |
| referring_agent | N/A (platform lead) |
| pipeline_row | Google Sheet row 21 |

---

## Prospect

| Field | Value |
|---|---|
| name | Jasmine Galvan |
| phone | (832) 375-9421 |
| email | jasleanjayjasmine@yahoo.com |
| preferred_contact | [TBD] |
| notes | thread/message 1a116f009c72ba72; HAR lead_id 10058098. Lead generated 10/07/2026 10:16 AM CT. Agent status unknown. |

---

## Intent (Rental)

| Field | Value |
|---|---|
| lead_type | Rental inquiry |
| pre_approved | N/A (rental) |
| budget_ceiling | [TBD] |
| target_areas | 19523 Elmtree Estates Dr, Katy TX 77449 (MLS 36711957) |
| property_type | House (rental) |
| bedrooms | [TBD] |
| timeline | [TBD] |
| motivation | [TBD] |
| qualification_confidence | Low |

Properties of interest: 19523 Elmtree Estates Dr, Katy TX 77449 (MLS 36711957)

Prospect message: (no message; HAR subject "Consumer requests more information for 19523 Elmtree Estates Dr")

---

## Qualification notes

```
Scores: Timeline 1 / Budget 1 / Motivation 2 / Responsiveness 2 = 6/12 (Soft)
Progress Residential rental listing (HAR To: mls@rentprogress.com, Denise CC'd).
Showing request = active renter signal; HIGH urgency, 30 min SLA.
Katy 77449 is outside the core Montgomery County service area.
Do not state Progress Residential's rent, income requirement, fees, pet policy, voucher policy or availability as fact until confirmed from the listing or Progress.
```

---

## Interaction log

| Date | Agent | Channel | Summary |
|---|---|---|---|
| 2026-10-07 | System | HAR | Repeat HAR showing request for the same property (19523 Elmtree Estates Dr), HAR lead 10058450, generated 1:20 PM CT (message 1a117989c5ddf3eb), no message. Second request in 3 hours = stronger intent. No new draft (Day 0 template draft r626260276462542546 already exists; plan runs once). |
| 2026-10-07 | System | HAR | HAR showing request received 10:16 AM CT; processed by hourly lead processor (11:10 CT run). Day 0 rental template draft created in Denise's Drafts. |

---

## Drafts produced

| Date | Specialist | Draft type | Status |
|---|---|---|---|
| 2026-10-07 | action plan rental-new (step 0) | "Your rental home inquiry" template #159 (Gmail draft id r626260276462542546) | Pending (Denise to review and send) |

To: jasleanjayjasmine@yahoo.com. Merge field set to "Jasmine". Template used word for word.

---

## Action plan

plan: 1 - Houston Rentals - NEW Lead (rental-new). Day 0 email drafted; stage step -> Active. Next plan: 1 - Houston Rentals - Active Lead (waiting for Follow Up Boss export). Lead Book NOT updated this run (ArtifactData write denied by permission check); plan state not recorded there.

---

## Handoff history

| Date | From | To | Reason | Confidence |
|---|---|---|---|---|
| 2026-10-07 | orchestrator | lead_qualifier | New lead: HAR.com - Showing Request, HIGH | high |
| 2026-10-07 | lead_qualifier | client_communication | Rental lead: Day 0 action-plan template | high |
