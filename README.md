# Denise HTR — AI System for Hometown Realtors of Texas
*Hometown Realtors of Texas LLC's AI lead system. Built on Claude. Runs in Claude Code and Claude scheduled tasks.*

---

**Team portal:** `index.html` in this repo is a plain-language portal for entering leads and finding setup and maintenance instructions. Open it in a browser.

---

## What this is

This repo is the brain of Hometown's AI system. It routes every incoming lead, qualifies it, drafts responses in the right agent's voice, tracks transactions, and keeps long-term leads warm, automatically and on demand.

It is not a chatbot. It is a structured set of AI specialists, each with a defined role, rules, and examples. You give it a lead. It gives you a case file, a response draft, and one next action.

**Team:** Denise Frank (Broker, handles all leads by default) and Keith Knowlton (Agent, handles leads Denise reassigns to him). Details live in `_config/team.md`.

---

## Day-one guide (Denise and Keith)

### What runs automatically

- **Hourly lead processor**, a scheduled task, at about :02 past each hour, Mon–Fri 7am–9pm and Sat–Sun 8am–6pm (Central). It reads new mail sent to leads@hometownrealtorsoftexas.com, creates case files, and saves draft replies to Denise's Gmail Drafts. It never sends.
- **Morning briefing**, a scheduled task, at 7:56am daily. It emails Denise and Keith what needs action today: hot leads with no follow-up, nurture touches due, contract deadlines in the next 7 days, and leads processed in the last 24 hours that haven't been reviewed.

### Your three daily tasks

**1. Review the drafts in Gmail.**
Every lead reply lands in Denise's Drafts. Drafts for Keith's leads start with "[For Keith]". No draft goes out without a human check:
- Does it sound like the person it's from?
- Does it end with one specific next step? (If it ends with "let me know if you have questions", it's wrong.)
- Does it promise anything about price, timeline or outcome? (It must not.)

If it passes, send it. If it's wrong, tell Claude what to fix.

**2. Enter walk-ins, calls and open-house sign-ins yourself (Path C).**
Don't wait for the hourly run. Open Claude Code with this repo and type, for example:

> "New lead — just spoke to a buyer named Sarah Mitchell, (281) 555-0142, looking in Magnolia, pre-approved, wants to move by spring."

Claude qualifies the lead, creates a case file, and drafts a first response.

**3. Check leads@ if something seems missed.**

> "Check leads@ and process any new emails."

---

## How a lead flows through the system

```
Lead arrives (leads@ email / walk-in / phone)
        ↓
00_orchestrator — reads it, identifies source and urgency, routes it
        ↓
01_lead_qualifier — scores it, creates the case file, sets the next action
        ↓
        ├→ Score 7+: 03_client_communication — drafts the first response
        ├→ Score 4–6: 03_client_communication (brief draft) + 05_nurture_coordinator (touch plan)
        └→ Score under 4: 05_nurture_coordinator (nurture plan, no immediate draft)

(If research is needed first)
        ↓
02_property_research — area brief, CMA, or showing prep
        ↓
03_client_communication — draft incorporating the research

(If the lead goes under contract)
        ↓
04_transaction_coordinator — deadline tracking, option period alerts, checklist
```

---

## The folder map

```
diana-calloway-real-estate-ai/
├── CLAUDE.md                    ← The system's brain (onboarding mode / operational mode)
├── README.md                    ← This file
├── index.html                   ← Team portal (landing-page/index.html is a copy)
│
├── 00_orchestrator/             ← Front door — routes everything
├── 01_lead_qualifier/           ← Scores leads, creates case files
├── 02_property_research/        ← Area briefs, CMAs, showing prep
├── 03_client_communication/     ← Drafts all client-facing messages
├── 04_transaction_coordinator/  ← Tracks contracts, deadlines, alerts
├── 05_nurture_coordinator/      ← Long-term lead management
│
├── _config/
│   ├── team.md                  ← Names, emails, phone, assignment rules
│   ├── team-standards.md        ← Quality bar (the Denise HTR test), hard stops
│   ├── buyer-checklist.md       ← TREC buyer transaction checklist
│   └── seller-checklist.md      ← TREC seller transaction checklist
│
├── _setup/
│   ├── onboarding-checklist.md  ← One-time setup steps
│   ├── routine-prompt.md        ← Plain-language description of the scheduled tasks
│   └── routines/                ← The exact prompts the scheduled tasks run
│
└── _shared/
    ├── voices/
    │   ├── denise.md            ← Denise's voice profile (starter — replace samples with real emails)
    │   └── keith.md             ← Keith's voice profile (placeholder)
    └── cases/
        ├── CASE_TEMPLATE.md     ← Template for new lead/deal files
        └── YYYY-NNN-agent-lastname.md ← One case file per lead or deal
```

---

## Common things you'll say to Claude

| Situation | What to type |
|---|---|
| New walk-in buyer | "New lead — [name], buyer, [phone], looking in [area], [budget if known]" |
| New seller inquiry | "New lead — [name], seller, [address], thinking about listing [timeline]" |
| Before a showing | "Prep me for a showing at [address]. Buyers are [client name], [profile]." |
| Draft a follow-up | "Draft a follow-up text from Denise to [name] about [property/situation]." |
| Hand a lead to Keith | "Reassign case [case_id] to Keith and draft his intro." |
| Transaction update | "What's the status on the Rodriguez transaction? What's due this week?" |
| Check nurture queue | "Which nurture leads have a touch due this week?" |

---

## What Claude will never do

- Send anything to a client without your review
- Make price commitments or timeline guarantees
- Handle a hard-stop situation without involving Denise directly
- Process a lead without creating a case file

---

## If something looks wrong

If a draft sounds off (wrong voice, wrong length, too pushy, too generic), tell Claude:

> "This doesn't sound like me. Rewrite it — shorter, warmer, more direct."

The system responds to feedback. You don't need to know how it works to fix it.

---

## Privacy note

Case files contain prospects' names, phone numbers and emails. This repo is a public fork, and GitHub does not allow a public fork to be made private. Move the system to a private repo before real leads are saved here.
