# Diana Calloway Real Estate — AI System
*Your team's AI system. Built on Claude. Runs in Claude Code.*

---

**New to the system? Start here → [Team Portal](https://six8coffee.github.io/diana-calloway-real-estate-ai/)**
The portal is the easiest way to enter leads, check what each specialist does, and find setup and maintenance instructions in plain language.

---

## What this is

This folder is the brain of your team's AI system. It routes every incoming lead, qualifies it, drafts responses in the right agent's voice, tracks transactions, and keeps long-term leads warm — automatically and on demand.

It is not a chatbot. It is a structured team of AI specialists, each with a defined role, rules, and examples. You give it a lead. It gives you a case file, a response draft, and a next-action directive.

---

## Jordan's day-one guide

If you're Jordan reading this on your first day: this is how the system works and how you use it.

### What you have access to

- **Claude Code** (desktop app or web) — where you run the system
- **Cloud Routines** — run automatically in the background on Anthropic's servers, processing leads@ hourly without any action needed from you
- This project folder — open it in Claude Code as your project

### Your morning briefing

Every day at 8am, the system sends an email to the whole team. It tells you: which leads need action today, which nurture touches are due, upcoming contract deadlines in the next 7 days, and any leads that came in overnight and haven't been reviewed. You do not need to set this up — it starts automatically after onboarding.

### Your three daily tasks

**1. Check leads@ inbox**

The hourly routine handles most of this automatically. But if you're in early or the routine missed something, open Claude Code with this project loaded and say:

> "Check leads@ and process any new emails."

Claude will read the inbox, route each lead through the qualifier, and draft a response for the assigned agent. Your job is to review the drafts before they go out.

**2. Handle walk-ins, calls, and open house sign-ins (Path C)**

When someone walks into the office, calls, or signs your open house sheet — don't wait for the routine. Type a description directly in Claude Code:

> "New lead — just spoke to a buyer named Priya Johnson, 512-555-0177, looking in Mueller, pre-approved $680k, wants to move by August."

Claude will qualify the lead, create a case file, and draft a first response within seconds. Review it, confirm it sounds right, and send.

**3. Review drafted responses before they go out**

No draft leaves without a human check. Your job in the review:
- Does it sound like the agent it's from? (Marcus is different from Diana — check the voice)
- Does it have a specific next step? (If it ends with "let me know if you have questions" — it's wrong)
- Are there any promises you can't keep? (No price commitments, no timeline guarantees)

If it passes: send it from the agent's Gmail. If it's wrong: tell Claude what to fix.

---

## How a lead flows through the system

```
Lead arrives (email / walk-in / phone)
        ↓
00_orchestrator — reads it, identifies source and urgency, routes it
        ↓
01_lead_qualifier — scores it, creates case file, sets next action
        ↓
        ├→ Score 7+: 03_client_communication — drafts first response
        ├→ Score 4–6: 03_client_communication (brief draft) + 05_nurture_coordinator (touch plan)
        └→ Score under 4: 05_nurture_coordinator (nurture plan, no immediate draft)
        
(If research is needed first)
        ↓
02_property_research — neighbourhood brief, CMA, or showing prep
        ↓
03_client_communication — draft incorporating research

(If lead converts and goes under contract)
        ↓
04_transaction_coordinator — deadline tracking, option period alerts, checklist
```

---

## The folder map

```
agency-system/
├── CLAUDE.md                    ← The system's brain (two modes: onboarding / operational)
├── README.md                    ← This file
│
├── 00_orchestrator/             ← Front door — routes everything
├── 01_lead_qualifier/           ← Scores leads, creates case files
├── 02_property_research/        ← Neighbourhood briefs, CMAs, showing prep
├── 03_client_communication/     ← Drafts all client-facing messages
├── 04_transaction_coordinator/  ← Tracks contracts, deadlines, alerts
├── 05_nurture_coordinator/      ← Long-term lead management
│
├── _config/
│   ├── team.md                  ← Your team's names, emails, assignments
│   ├── team-standards.md        ← Diana's philosophy, hard stops, quality floor
│   ├── buyer-checklist.md       ← Full TREC buyer transaction checklist
│   └── seller-checklist.md      ← Full TREC seller transaction checklist
│
├── _setup/
│   ├── onboarding-checklist.md  ← Run once to configure Gmail, Drive, and the routine
│   └── routine-prompt.md        ← Documentation for the hourly Cloud Routine
│
└── _shared/
    ├── voices/
    │   ├── diana.md             ← Diana's voice profile
    │   ├── marcus.md            ← Marcus's voice profile
    │   ├── priya.md             ← Priya's voice profile
    │   └── jordan.md            ← Jordan's voice profile
    └── cases/
        ├── CASE_TEMPLATE.md     ← Template for new lead/deal files
        └── [CASE_*.md]          ← Individual case files (one per lead or deal)
```

---

## Common things you'll say to Claude

| Situation | What to type |
|---|---|
| New walk-in buyer | "New lead — [name], buyer, [phone], looking in [area], [budget if known]" |
| New seller inquiry | "New lead — [name], seller, [address], thinking about listing [timeline]" |
| Before a showing | "Prep me for a showing at [address]. Buyers are [client name], [profile]." |
| Draft a follow-up | "Draft a follow-up text from Marcus to [name] about [property/situation]." |
| Transaction update | "What's the status on the Rodriguez transaction? What's due this week?" |
| Check nurture queue | "Which nurture leads have a touch due this week?" |

---

## What Claude will never do

- Send anything without your review
- Make price commitments or timeline guarantees
- Handle a hard-stop situation without involving Diana directly
- Process a lead without creating a case file first

---

## If something looks wrong

If a draft sounds off — wrong voice, wrong length, too pushy, too generic — tell Claude:

> "This doesn't sound like Marcus. Rewrite it — shorter, less formal, more direct."

The system responds to feedback. You do not need to know how it works to fix it.

---

## Questions?

Ask Claude. It knows this system better than any other tool you have.

> "How does the option period alert work?"
> "What's the difference between Path A and Path C?"
> "Which agent should I assign this to?"

If Claude doesn't know, it will tell you what it would need to find out.
