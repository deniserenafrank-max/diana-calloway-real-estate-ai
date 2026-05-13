# Case File — [CASE_ID]
*Format: YYYY-NNN-agent-lastname (e.g. 2026-047-marcus-mitchell)*
*Updated by each specialist as the lead/deal moves through the system.*
*This file is the single source of truth for this lead or deal.*

---

## Header

| Field | Value |
|---|---|
| case_id | |
| created | |
| last_updated | |
| status | New / Qualifying / Active / Under Contract / Nurture / Closed / Dead |
| lead_type | Buyer / Seller / Both |
| source | Zillow / Realtor.com / Redfin / Homes.com / Referral / Open house / Walk-in / Phone call / Personal inbox |
| urgency | CRITICAL / HIGH / MEDIUM / STANDARD |
| assigned_agent | |
| referring_agent | (if referral — who sourced it) |
| pipeline_row | (Google Sheet row number for cross-reference) |

---

## Prospect

| Field | Value |
|---|---|
| name | |
| phone | |
| email | |
| preferred_contact | Call / Text / Email |
| notes | |

---

## Intent (Buyer)

| Field | Value |
|---|---|
| lead_type | Buyer |
| pre_approved | Yes / No / In progress |
| lender | |
| approval_amount | |
| budget_ceiling | |
| target_areas | |
| property_type | House / Condo / Townhouse / Land / Investment |
| bedrooms | |
| timeline | ASAP / 1–3 months / 3–6 months / 6–12 months / Exploring |
| motivation | |
| currently | Renting / Owning |
| dealbreakers | |
| qualification_confidence | High / Medium / Low |

---

## Intent (Seller)

| Field | Value |
|---|---|
| lead_type | Seller |
| property_address | |
| listing_timeline | ASAP / 1–3 months / 3–6 months / 12+ months |
| motivation | Upsizing / Downsizing / Relocating / Investment / Estate / Other |
| target_price | |
| mortgage_balance | Owned outright / Has mortgage |
| competing_agents | Yes / No / Unknown |
| recent_cma | Yes / No |
| qualification_confidence | High / Medium / Low |

---

## Qualification notes

*Free text. What did we learn? What's the real story behind the lead?*
*What signals point to a serious buyer/seller vs early explorer?*

```
[Write qualification notes here]
```

---

## Interaction log

*Append each interaction. Never delete entries. Newest at top.*

| Date | Agent | Channel | Summary |
|---|---|---|---|
| | | | |

---

## Drafts produced

| Date | Specialist | Draft type | Status |
|---|---|---|---|
| | 03_client_communication | First text | Sent / Pending / Revised |
| | 03_client_communication | First email | Sent / Pending / Revised |

---

## Property research

*Filled by 02_property_research when triggered. Link to research brief if separate.*

| Field | Value |
|---|---|
| properties_researched | |
| research_brief | (paste key findings or link to separate research file) |

---

## Transaction (under contract)

*Filled by 04_transaction_coordinator once contract is executed.*

| Field | Value |
|---|---|
| contract_date | |
| option_period_end | |
| financing_contingency_end | |
| close_date | |
| title_company | |
| earnest_money | |
| option_fee | |
| purchase_price | |
| key_contacts | Inspector: / Lender: / Title officer: |

---

## Handoff history

*Record every time this case moves between specialists.*

| Date | From | To | Reason | Confidence |
|---|---|---|---|---|
| | orchestrator | lead_qualifier | New lead — routed on source | — |
