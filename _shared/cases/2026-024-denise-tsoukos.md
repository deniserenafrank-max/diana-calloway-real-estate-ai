# Case File — 2026-024-denise-tsoukos
*File name: `_shared/cases/2026-024-denise-tsoukos.md`. case_id = file name without .md.*

---

## Pipeline summary

```
PIPELINE SUMMARY
case_id:        2026-024-denise-tsoukos
date:           2026-10-07
source:         HAR.com - Showing Request
prospect_name:  John Tsoukos
contact:        (832) 973-0546 / ioaniscuko@gmail.com
lead_type:      Rental inquiry
assigned_agent: Denise Frank
urgency:        HIGH
status:         Active
next_action:    Call John at (832) 973-0546 today about his showing request for 19119 Royal Isle Dr (Tomball 77375); confirm showing setup with Progress, get days/times and move-in date. Send the rental template draft.
draft_ready:    Yes
notes:          Progress Residential rental listing (HAR To: mls@rentprogress.com, Denise CC'd). MLS 81055523. HAR lead 10058401, generated 10/07 12:44 PM CT. No message in HAR lead. Email name (ioaniscuko) differs from lead name: confirm. Timeline 1 / Budget 1 / Motivation 2 / Responsiveness 2 = 6/12 (Soft). Tomball 77375 is next to the core service area. Day 0 template email from plan '1 - Houston Rentals - NEW Lead'. Draft id r3192592102827807012.
```

---

## Header

| Field | Value |
|---|---|
| case_id | 2026-024-denise-tsoukos |
| created | 2026-10-07 13:05 CT |
| last_updated | 2026-10-07 13:05 CT |
| status | Active |
| lead_type | Rental inquiry |
| source | HAR.com - Showing Request |
| urgency | HIGH |
| assigned_agent | Denise Frank |
| referring_agent | N/A (platform lead) |
| pipeline_row | Google Sheet row 25 |

---

## Prospect

| Field | Value |
|---|---|
| name | John Tsoukos |
| phone | (832) 973-0546 |
| email | ioaniscuko@gmail.com |
| preferred_contact | [TBD] |
| notes | thread/message 1a117780226b0a89; HAR lead_id 10058401. Lead generated 10/07/2026 12:44 PM CT. Agent status unknown. |

---

## Intent (Rental)

| Field | Value |
|---|---|
| lead_type | Rental inquiry |
| pre_approved | N/A (rental) |
| budget_ceiling | [TBD] |
| target_areas | Tomball; 19119 Royal Isle Dr, Tomball TX 77375 (MLS 81055523) |
| property_type | House (rental) |
| bedrooms | [TBD] |
| timeline | [TBD] |
| motivation | Showing request |
| qualification_confidence | Low |

Properties of interest: 19119 Royal Isle Dr, Tomball TX 77375 (MLS 81055523)

Prospect message: (none)

---

## Qualification notes

```
Scores: Timeline 1 / Budget 1 / Motivation 2 / Responsiveness 2 = 6/12 (Soft)
Progress Residential rental listing (HAR To: mls@rentprogress.com, Denise CC'd).
Showing request: HIGH urgency, 30-minute SLA.
No message with the request. Email name (ioaniscuko) differs from lead name: confirm who is applying.
Do not state rent, income requirement, fees or availability as fact until confirmed from the listing or Progress.
Tomball 77375 is just west of the core Montgomery County service area (borders Magnolia/Spring).
```

---

## Interaction log

| Date | Agent | Channel | Summary |
|---|---|---|---|
| 2026-10-07 | System | HAR | HAR showing request received 12:44 PM CT; processed by hourly lead processor (13:05 CT run). Day 0 rental template draft created in Denise's Drafts. |

---

## Drafts produced

| Date | Specialist | Draft type | Status |
|---|---|---|---|
| 2026-10-07 | action plan rental-new (step 0) | "Your rental home inquiry" template #159 (Gmail draft id r3192592102827807012) | Pending (Denise to review and send) |

To: ioaniscuko@gmail.com. Merge field set to "John". Template used word for word.

---

## Action plan

plan: 1 - Houston Rentals - NEW Lead (rental-new). Day 0 email drafted; stage step -> Active. Next plan: 1 - Houston Rentals - Active Lead (waiting for Follow Up Boss export). Lead Book NOT updated this run (ArtifactData write denied by permission check); plan state not recorded there.

---

## Handoff history

| Date | From | To | Reason | Confidence |
|---|---|---|---|---|
| 2026-10-07 | orchestrator | lead_qualifier | New lead: HAR.com - Showing Request, HIGH | high |
| 2026-10-07 | lead_qualifier | client_communication | Rental lead: Day 0 action-plan template | high |
