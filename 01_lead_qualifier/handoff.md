# Handoff — 01_lead_qualifier

## What the lead qualifier receives

A structured handoff envelope from 00_orchestrator, containing the raw lead and routing metadata.

**Required fields to proceed:** source, urgency, intake_path, assign_to, raw_message (or equivalent manual description).

If the envelope is incomplete, stop and ask the orchestrator to re-send before qualifying.

## What the lead qualifier produces

Three outputs, always in this order:

---

### Output 1 — Qualification summary

```
QUALIFICATION SUMMARY — [Prospect Name]

Case file: [filename] (created / updated)
Pipeline row: added

--- Scores ---
Timeline:       [1/2/3]  [brief reasoning]
Budget clarity: [1/2/3]  [brief reasoning]
Motivation:     [1/2/3]  [brief reasoning]
Responsiveness: [1/2/3]  [brief reasoning]
TOTAL: [X/12] — [Priority / Qualified / Soft / Not ready]

--- Pre-approval ---
Status: [Yes / In progress / Unknown / N/A — seller]
[Any notes for the agent]

--- Lead type ---
[Buyer / Seller / Unknown] — [confirmed or inferred]

--- Assessment ---
[2–4 sentences. Plain English. What the agent needs to know to act. Market context if relevant.]

--- Next action ---
[One directive. Who does what, by when, and how to lead the conversation.]

[Routing directives — which specialists receive work from here]
```

---

### Output 2 — Case file

Create or update the file in `_shared/cases/` using `CASE_TEMPLATE.md`.

File name format: `CASE_[LAST NAME]_[FIRST INITIAL]_[YYYYMMDD].md`

Populate every field you have data for. Mark `[TBD]` for fields that will fill in over time. Never leave a field blank without marking it.

---

### Output 3 — Pipeline row

Output the structured pipeline row (see rules.md Rule 7) for the Google Sheet.

---

## Routing after qualification

| Outcome | Handoff to | What you send |
|---|---|---|
| Score 7+ | 03_client_communication | Qualification summary + case file reference + draft request |
| Score 4–6 | 03_client_communication + 05_nurture_coordinator | Brief first-response request + nurture flag |
| Score under 4 | 05_nurture_coordinator | Case file + "not ready" flag + suggested touch cadence |
| Research needed before first contact | 02_property_research | Client profile + area/property + research type needed |

## Back-handoff

If qualification reveals the routing was wrong (e.g., a buyer inquiry is actually a seller), return to the orchestrator:

```
back_to: orchestrator
reason: [one-line correction]
recommended_route: [correct specialist]
```
