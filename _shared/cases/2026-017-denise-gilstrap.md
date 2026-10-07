# Case File — 2026-017-denise-gilstrap
*File name: `_shared/cases/2026-017-denise-gilstrap.md`. case_id = file name without .md.*

---

## Pipeline summary

```
PIPELINE SUMMARY
case_id:        2026-017-denise-gilstrap
date:           2026-10-06
source:         HAR.com - Showing Request
prospect_name:  Ashley Gilstrap
contact:        (346) 604-5864 / msashleygilstrap@gmail.com (also ashley_gilstrap@yahoo.com)
lead_type:      Rental inquiry
assigned_agent: Denise Frank
urgency:        HIGH
status:         Active
next_action:    Call Ashley at (346) 604-5864 now: she self-toured 8410 Tararin Ln (Richmond 77407) today and wants to apply, 2 applicants. Get the application link from Progress and send it. Review the new personal draft to msashleygilstrap@gmail.com.
draft_ready:    Yes
notes:          Progress Residential rental listing (HAR To: mls@rentprogress.com, Denise CC'd). MLS 67544929. First HAR showing request 10/06 8:26 PM CT (lead 10057387, no message). Repeat HAR inquiry 10/07 3:12 PM CT (lead 10058630) from a new email msashleygilstrap@gmail.com: 'We had a self tour today and would like to complete an application for this home. There will be two applicants.' Timeline 3 / Budget 1 / Motivation 3 / Responsiveness 3 = 10/12 (Hot). Richmond 77407 is outside the core Montgomery County service area. Day 0 template draft r-8026433564159969637 (to yahoo address); application reply draft r122326698091888542 (to gmail address).
```

---

## Header

| Field | Value |
|---|---|
| case_id | 2026-017-denise-gilstrap |
| created | 2026-10-06 21:10 CT |
| last_updated | 2026-10-07 16:05 CT |
| status | Active |
| lead_type | Rental inquiry |
| source | HAR.com - Showing Request |
| urgency | HIGH |
| assigned_agent | Denise Frank |
| referring_agent | N/A (platform lead) |
| pipeline_row | Google Sheet row 18 |

---

## Prospect

| Field | Value |
|---|---|
| name | Ashley Gilstrap |
| phone | (346) 604-5864 |
| email | msashleygilstrap@gmail.com (newest, 10/07); ashley_gilstrap@yahoo.com (10/06) |
| preferred_contact | [TBD] |
| notes | thread 1a113f7cfd49e266; HAR lead_id 10057387. Lead generated 10/06/2026 08:26 PM CT. No message in HAR lead. Repeat HAR inquiry: thread/message 1a117ff05dbbf8ee, HAR lead_id 10058630, generated 10/07/2026 3:12 PM CT. |

---

## Intent (Rental)

| Field | Value |
|---|---|
| lead_type | Rental inquiry |
| pre_approved | N/A (rental) |
| budget_ceiling | [TBD] |
| target_areas | 8410 Tararin Ln, Richmond TX 77407 (MLS 67544929) |
| property_type | House (rental) |
| bedrooms | [TBD] |
| timeline | Ready to apply now (self-toured 10/07) |
| motivation | Wants to apply; 2 applicants |
| qualification_confidence | Medium |

Properties of interest: 8410 Tararin Ln, Richmond TX 77407 (MLS 67544929)

Prospect message (10/06): none (notification subject: Showing Request)
Prospect message (10/07): "Hi, We had a self tour today and would like to complete an application for this home. There will be two applicants."

---

## Qualification notes

```
Scores (updated 10/07): Timeline 3 / Budget 1 / Motivation 3 / Responsiveness 3 = 10/12 (Hot)
Was 6/12 on 10/06. Self-toured 10/07 and wants to apply with 2 applicants.
Progress Residential rental listing (HAR To: mls@rentprogress.com, Denise CC'd).
Flags: Richmond 77407 is outside the core Montgomery County service area. Showing request = active renter signal; HIGH urgency, 30 min SLA.
Next action: Call Ashley at (346) 604-5864 now: she self-toured 8410 Tararin Ln (Richmond 77407) today and wants to apply, 2 applicants. Get the application link from Progress and send it. Review the new personal draft to msashleygilstrap@gmail.com.
Do not state Progress Residential's rent, income requirement, fees, pet policy, voucher policy or availability as fact until confirmed from the listing or Progress.
```

---

## Interaction log

| Date | Agent | Channel | Summary |
|---|---|---|---|
| 2026-10-06 | System | HAR | HAR showing request received; processed by hourly lead processor. Day 0 rental template draft created in Denise's Drafts. |
| 2026-10-07 | System | HAR | Repeat HAR inquiry 3:12 PM CT from msashleygilstrap@gmail.com: self-toured today, wants to apply, 2 applicants. Personal application reply drafted (16:05 CT run). No plan restart. |

---

## Drafts produced

| Date | Specialist | Draft type | Status |
|---|---|---|---|
| 2026-10-06 | action plan rental-new (step 0) | "Your rental home inquiry" template #159 (Gmail draft id r-8026433564159969637) | Pending (Denise to review and send) |

To: ashley_gilstrap@yahoo.com. Merge field set to "Ashley". Template used word for word.

| 2026-10-07 | client_communication | Personal reply: application next steps (Gmail draft id r122326698091888542) | Pending (Denise to review and send) |

To: msashleygilstrap@gmail.com. Subject "8410 Tararin Ln - your application". Asks her to call/text (832) 662-0475; no promises on approval, fees or timing.

---

## Action plan

plan: 1 - Houston Rentals - NEW Lead (rental-new). Day 0 email drafted; stage step -> Active. Next plan: 1 - Houston Rentals - Active Lead (waiting for Follow Up Boss export). Lead Book NOT updated this run (ArtifactData write denied by permission check); plan state not recorded there. 10/07: repeat inquiry, plan not restarted.

---

## Handoff history

| Date | From | To | Reason | Confidence |
|---|---|---|---|---|
| 2026-10-06 | orchestrator | lead_qualifier | New lead: HAR.com - Showing Request, HIGH | high |
| 2026-10-06 | lead_qualifier | client_communication | Rental lead: Day 0 action-plan template | high |
| 2026-10-07 | orchestrator | client_communication | Repeat inquiry: ready to apply, personal reply | high |
