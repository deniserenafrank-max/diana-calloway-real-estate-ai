# Case File — 2026-018-denise-richardson
*File name: `_shared/cases/2026-018-denise-richardson.md`. case_id = file name without .md.*

---

## Pipeline summary

```
PIPELINE SUMMARY
case_id:        2026-018-denise-richardson
date:           2026-10-07
source:         HAR.com - Showing Request
prospect_name:  Lisa Richardson
contact:        (601) 513-6825 / virtuous68@yahoo.com
lead_type:      Rental inquiry
assigned_agent: Denise Frank
urgency:        HIGH
status:         Active
next_action:    Call Lisa at (601) 513-6825 this morning about her showing request for 21610 Gannet Peak Way (Katy 77449); confirm showing setup with Progress, get days/times and move-in date. Send the rental template draft. Note: Estefani Ramirez (2026-016) also requested a showing on this same home.
draft_ready:    Yes
notes:          Progress Residential rental listing (HAR To: mls@rentprogress.com, Denise CC'd). MLS 94521936. HAR lead 10057484, generated 10/06 10:06 PM CT (after the weekday routine's last run). No message in HAR lead. 601 area code (Mississippi): may be relocating. Timeline 1 / Budget 1 / Motivation 2 / Responsiveness 2 = 6/12 (Soft). Katy 77449 is outside the core Montgomery County service area. Day 0 template email from plan '1 - Houston Rentals - NEW Lead'. Draft id r3570101114065357742.
```

---

## Header

| Field | Value |
|---|---|
| case_id | 2026-018-denise-richardson |
| created | 2026-10-07 07:10 CT |
| last_updated | 2026-10-07 07:10 CT |
| status | Active |
| lead_type | Rental inquiry |
| source | HAR.com - Showing Request |
| urgency | HIGH |
| assigned_agent | Denise Frank |
| referring_agent | N/A (platform lead) |
| pipeline_row | Google Sheet row 19 |

---

## Prospect

| Field | Value |
|---|---|
| name | Lisa Richardson |
| phone | (601) 513-6825 |
| email | virtuous68@yahoo.com |
| preferred_contact | [TBD] |
| notes | thread 1a113a1d46820d35; HAR lead_id 10057484 (message 1a11453a63ab9b15). Lead generated 10/06/2026 10:06 PM CT. Agent status unknown. Phone has a 601 (Mississippi) area code: may be relocating to Houston. |

---

## Intent (Rental)

| Field | Value |
|---|---|
| lead_type | Rental inquiry |
| pre_approved | N/A (rental) |
| budget_ceiling | [TBD] |
| target_areas | 21610 Gannet Peak Way, Katy TX 77449 (MLS 94521936) |
| property_type | House (rental) |
| bedrooms | [TBD] |
| timeline | [TBD] |
| motivation | [TBD] |
| qualification_confidence | Low |

Properties of interest: 21610 Gannet Peak Way, Katy TX 77449 (MLS 94521936)

Prospect message: none (HAR subject: "Consumer requests more information for 21610 Gannet Peak Way")

---

## Qualification notes

```
Scores: Timeline 1 / Budget 1 / Motivation 2 / Responsiveness 2 = 6/12 (Soft)
Progress Residential rental listing (HAR To: mls@rentprogress.com, Denise CC'd).
Flags: Same home as 2026-016 (Estefani Ramirez), two showing requests in 4 hours. Katy 77449 is outside the core Montgomery County service area. Showing request = active renter signal; HIGH urgency, 30 min SLA.
Next action: Call Lisa at (601) 513-6825 this morning about her showing request for 21610 Gannet Peak Way (Katy 77449); confirm showing setup with Progress, get days/times and move-in date. Send the rental template draft. Note: Estefani Ramirez (2026-016) also requested a showing on this same home.
Do not state Progress Residential's rent, income requirement, fees, pet policy, voucher policy or availability as fact until confirmed from the listing or Progress.
```

---

## Interaction log

| Date | Agent | Channel | Summary |
|---|---|---|---|
| 2026-10-07 | System | HAR | HAR showing request (arrived 10/06 10:06 PM CT, after the last weekday run) received; processed by hourly lead processor. Day 0 rental template draft created in Denise's Drafts. |

---

## Drafts produced

| Date | Specialist | Draft type | Status |
|---|---|---|---|
| 2026-10-07 | action plan rental-new (step 0) | "Your rental home inquiry" template #159 (Gmail draft id r3570101114065357742) | Pending (Denise to review and send) |

To: virtuous68@yahoo.com. Merge field set to "Lisa". Template used word for word.

---

## Action plan

plan: 1 - Houston Rentals - NEW Lead (rental-new). Day 0 email drafted; stage step -> Active. Next plan: 1 - Houston Rentals - Active Lead (waiting for Follow Up Boss export). Lead Book NOT updated this run (ArtifactData write denied by permission check); plan state not recorded there.

---

## Handoff history

| Date | From | To | Reason | Confidence |
|---|---|---|---|---|
| 2026-10-07 | orchestrator | lead_qualifier | New lead: HAR.com - Showing Request, HIGH | high |
| 2026-10-07 | lead_qualifier | client_communication | Rental lead: Day 0 action-plan template | high |
