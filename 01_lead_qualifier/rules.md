# Rules — 01_lead_qualifier

## Rule 1 — Always create or update the case file

Every lead that passes through this specialist gets a case file. No exceptions.

- Check `_shared/cases/` for an existing file matching the prospect name or email.
- If found: update it. If not: create one from `_shared/cases/CASE_TEMPLATE.md`.
- File name format (single standard everywhere): `_shared/cases/YYYY-NNN-agent-lastname.md`
  - `YYYY` = year the case was opened; `NNN` = next sequential case number for that year (zero-padded, check existing files); `agent` = assigned agent's first name, lowercase (`denise` or `keith`); `lastname` = prospect's last name, lowercase.
- Example: `2026-001-denise-mitchell.md`
- `case_id` = the filename without `.md` (e.g. `2026-001-denise-mitchell`).

## Rule 2 — Score the lead

Rate each dimension on a 1–3 scale. Do not skip any.

| Dimension | 1 — Weak | 2 — Moderate | 3 — Strong |
|---|---|---|---|
| **Timeline** | 12+ months or unknown | 3–12 months | Under 3 months |
| **Budget clarity** | No budget given | Range given, no pre-approval | Pre-approved with amount |
| **Motivation** | Just exploring, no reason given | Lifestyle change or preference | Hard deadline (relocation, lease end, divorce, estate) |
| **Responsiveness** | First contact, no reply history | Replied once, low engagement | Actively inquiring, multiple touchpoints |

**Total score interpretation:**
- 10–12: Priority lead. Full investment. Research + draft on first pass.
- 7–9: Qualified lead. Standard follow-up. Qualify gaps on first call.
- 4–6: Soft lead. First response only. Route to nurture after contact.
- Under 4: Not ready. Route directly to nurture. Flag to agent.

## Rule 3 — Flag pre-approval status

Pre-approval is the single most important qualifier for buyers.

- **Pre-approved:** Note the amount and lender if given. Mark as `pre_approved: Yes`.
- **In progress:** Note it. Recommend agent ask for completion date on first call.
- **Not stated:** Do not assume. Mark as `pre_approved: Unknown`. Add to first-call checklist.
- **Seller lead:** Pre-approval field is not applicable — skip it.

## Rule 4 — Determine lead type

Buyer, Seller, or Unknown. Evidence:
- Platform source (Zillow listing inquiry = Buyer; "Thinking about selling" = Seller)
- Keywords in the raw message ("I want to buy", "we're looking", "list my home", "what's my home worth")
- If genuinely ambiguous: mark Unknown. The orchestrator already had a guess — confirm or correct it.

## Rule 5 — Set one clear next action

Every qualification summary ends with a single directive for the agent. Not a list. One thing.

Examples:
- "Call James Rodriguez now. He's pre-approved $720k, relocating for a new job in The Woodlands, ready in 90 days. Lead the call with Magnolia — that's his first-choice area."
- "Text Sarah Mitchell within 5 minutes. She wants to tour 1234 Example Oak Dr in Conroe. Confirm availability for this weekend. Do not ask qualifying questions yet."
- "Email the Garcias this evening. They're 6–12 months out and exploring. Warm intro only — don't pitch the CMA yet."

## Rule 6 — Route after qualification

| Qualification outcome | Route to |
|---|---|
| Score 7+ and first contact needed | 03_client_communication — draft first response |
| Score 4–6 and first contact needed | 03_client_communication — brief first response, then flag to nurture |
| Score under 4 | 05_nurture_coordinator — no full draft needed, nurture plan only |
| Research needed for showing or listing prep | 02_property_research — after first contact drafted |

## Rule 7 — Include a pipeline summary block in your output

After every qualification, print a structured summary block. This makes the lead easy to scan without opening the full case file, and gives Claude the data it needs when Denise or Keith asks for a pipeline view.

```
PIPELINE SUMMARY
case_id:        [YYYY-NNN-agent-lastname]
date:           [today's date]
source:         [platform or intake path]
prospect_name:  [full name]
contact:        [phone and/or email]
lead_type:      [Buyer / Seller / Unknown]
assigned_agent: [from _config/team.md defaults — Denise Frank unless reassigned to Keith Knowlton in the case file]
urgency:        [CRITICAL / HIGH / MEDIUM / STANDARD]
status:         New
next_action:    [the one directive from Rule 5]
draft_ready:    No
notes:          [qualification score + any flags]
```

Also write this block into the case file header section in `_shared/cases/` so it persists.

## Rule 8 — Never qualify without the full handoff envelope

If the orchestrator's handoff envelope is incomplete or missing, stop. Ask the orchestrator to re-send it before proceeding. A qualification based on partial information produces a wrong score.
