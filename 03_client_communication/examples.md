# Examples — 03_client_communication

All prospects, addresses and phone numbers below are fictional.

---

## Example 1 — Denise first text to Zillow buyer (Sarah Mitchell, Example Oak Dr)

**Request (from 01_lead_qualifier):**
```
Draft request: Denise first text to Sarah Mitchell re: 1234 Example Oak Dr, Conroe TX tour availability
Voice: Denise Frank (_shared/voices/denise.md)
Case: 2026-001-denise-mitchell
Context: Zillow tour request, HIGH urgency, 5-min SLA. She asked if it's still available
         and could get in this weekend. Lead score 9/12. Phone (936) 555-0187.
```

**Draft output:**
```
DRAFT — Text
From: Denise Frank
To: Sarah Mitchell
Re: 1234 Example Oak Dr, Conroe — tour request
---
Hi Sarah — Denise Frank with Hometown Realtors of Texas. 1234 Example Oak is still on the market.
Saturday works — morning or afternoon? I can get you in.

— Denise | (832) 661-0475
---
NOTES FOR AGENT:
- Send within 5 minutes of receiving this draft — Zillow 5-min SLA
- Confirm the listing is still active on HAR.com before sending
- If no reply in 2 hours, follow up with a single call attempt
- Do not ask qualifying questions in this first text — she asked about the property, answer first
```

---

## Example 2 — Keith follow-up email to a relocation buyer (James Rodriguez, reassigned by Denise)

**Request (from 01_lead_qualifier + 02_property_research):**
```
Draft request: Follow-up email from Keith to James Rodriguez after phone call
Voice: Keith Knowlton (_shared/voices/keith.md)
Case: 2026-002-keith-rodriguez (Denise reassigned to Keith in the case file — overflow)
Context: Relocation buyer for a new job in The Woodlands, pre-approved $450k, interested in
         Magnolia and Montgomery, 90-day deadline tied to his start date.
         Just spoke by phone. 02_property_research brief for Magnolia is attached.
         Goal: confirm relationship, send 2-3 Magnolia listings, set a showing.
```

**Draft output:**
```
DRAFT — Email
From: Keith Knowlton
To: James Rodriguez (james.r@example.com)
Re: Magnolia listings + next steps
---
Subject: Magnolia listings for you — let's get you in this week

James,

Good talking earlier. Here's what I'm sending your way first:

[Pull 2–3 Magnolia listings within his approval amount from HAR.com, paste links here before sending]

You told me you wanted a bit more space and a manageable drive to The Woodlands — these are the
ones in Magnolia that line up with that. Tell me which ones look worth a closer look.

I want to get you in front of a couple of these before the week's out. What does your Thursday
or Friday afternoon look like?

Keith Knowlton
Hometown Realtors of Texas LLC
(832) 661-0475
keith@hometownrealtorsoftexas.com
---
NOTES FOR AGENT:
- Fill in the 2–3 listing links/addresses before sending — pull from HAR.com
- Do not add commute times or school information unless 02_property_research has verified them
- If you don't have time to pull listings now, send this without them and add "I'll follow up
  with specific listings in the next hour" to the second paragraph
- James has a hard deadline tied to his job start date. Keep the energy up.
```

---

## Example 3 — Denise email to a personal referral (seller, estate situation)

**Request (from orchestrator, Path C):**
```
Draft request: Denise first email to a personal referral — Helen Park, seller
Voice: Denise Frank (_shared/voices/denise.md)
Case: 2026-003-denise-park
Context: Referred by past client Tom Chen. Helen's mother passed 3 months ago.
         Estate property in Pinehurst. Helen lives out of town, hasn't decided timeline yet.
         Hard stop flagged: estate situation → Denise handles directly.
Goal: warm first contact, offer to help her think through it, no push for listing.
```

**Draft output:**
```
DRAFT — Email
From: Denise Frank
To: Helen Park
Re: Referral from Tom Chen — your mother's home
---
Subject: Tom Chen mentioned you — about your mother's home in Pinehurst

Helen,

Tom passed along your contact information. I'm so sorry about your mother.

There's no rush on my end — estate properties have their own timeline and you're the one
who decides when that is. But when you're ready to start thinking through the house, I'm
happy to be a resource. No pressure to list, no pitch. Just an honest conversation about
what the market looks like and what your options are.

I know how much is on your plate right now, especially handling this from out of town.

Take your time. I'm here when you're ready.

Denise Frank
Broker, Hometown Realtors of Texas LLC
(832) 661-0475
denise@hometownrealtorsoftexas.com
hometownrealtorsoftexas.com
---
NOTES FOR AGENT:
- Denise sends this personally
- Do not CC anyone. This is a quiet, private outreach.
- Hard stop applies: Denise handles all follow-up on this one — do not reassign to Keith
- If Helen replies and wants to talk, Denise calls within the hour
```

---

## Example 4 — Denise transaction update to buyer clients

**Request (from 04_transaction_coordinator):**
```
Draft request: Transaction update text from Denise to the Okonkwos (buyers, under contract)
Voice: Denise Frank (_shared/voices/denise.md)
Case: 2026-004-denise-okonkwo
Context: Option period expires Friday. Inspection came back with 3 items — minor electrical,
         HVAC filter replacement, a cracked tile in guest bath. Agent and client reviewed.
         Seller agreed to credit $1,200 at closing. Option period ends Friday.
Goal: update the clients on where things stand, confirm they know the timeline.
```

**Draft output:**
```
DRAFT — Text
From: Denise Frank
To: The Okonkwos
Re: Option period update
---
Good news — the seller agreed to the $1,200 credit at closing to cover the inspection items.
Your option period ends Friday. We're on track. I'll send a full update email with the
next steps and closing timeline by end of day.

— Denise | (832) 661-0475
---
NOTES FOR AGENT:
- Send the email update by EOD as promised — use 04_transaction_coordinator for checklist content
- Make sure the $1,200 credit is documented in a signed amendment (TREC Amendment to Contract)
  before the option period ends
- If the Okonkwos reply with questions that need contract interpretation, do not answer in text —
  Denise calls them (or refers to a real estate attorney if it's a legal question)
```
