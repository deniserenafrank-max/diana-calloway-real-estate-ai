# Examples — 03_client_communication

---

## Example 1 — Marcus first text to Zillow buyer (Sarah Mitchell, Clawson Rd)

**Request (from 01_lead_qualifier):**
```
Draft request: Marcus first text to Sarah Mitchell re: 4504 Clawson Rd tour availability
Voice: Marcus Webb (_shared/voices/marcus.md)
Context: Zillow tour request, HIGH urgency, 5-min SLA. She asked if it's still available
         and could get in this weekend. Lead score 9/12.
```

**Draft output:**
```
DRAFT — Text
From: Marcus Webb
To: Sarah Mitchell
Re: 4504 Clawson Rd — tour request
---
Hey Sarah — Marcus Webb at Diana Calloway Real Estate. 4504 Clawson is still on the market.
Saturday works — morning or afternoon? I can get you in.

— Marcus | (512) 555-0101
---
NOTES FOR AGENT:
- Send within 5 minutes of receiving this draft — Zillow 5-min SLA
- If no reply in 2 hours, follow up with a single call attempt
- Do not ask qualifying questions in this first text — she asked about the property, answer first
```

---

## Example 2 — Marcus follow-up email to referral buyer (James Rodriguez)

**Request (from 01_lead_qualifier + 02_property_research):**
```
Draft request: Follow-up email from Marcus to James Rodriguez after phone call
Voice: Marcus Webb (_shared/voices/marcus.md)
Context: Relocation buyer, pre-approved $720k, Mueller/Hyde Park, 90-day deadline (Dell).
         Just spoke by phone. 02_property_research brief for Mueller is attached.
         Goal: confirm relationship, send 2-3 Mueller listings, set a showing.
```

**Draft output:**
```
DRAFT — Email
From: Marcus Webb
To: James Rodriguez (james.r@gmail.com)
Re: Mueller listings + next steps
---
Subject: Mueller listings for you — let's get you in this week

James,

Good talking earlier. Here's what I'm sending your way first:

[Pull 2–3 Mueller listings in $660–720k, attach or paste MLS links here before sending]

Mueller makes sense for what you described — walkable, family-oriented, solid HOA community,
and a straight shot to Round Rock. At your approval amount you're competitive there.

I want to get you in front of a couple of these before the week's out. What does your Thursday
or Friday afternoon look like?

Marcus
(512) 555-0101
---
NOTES FOR AGENT:
- Fill in the 3 listing links/addresses before sending — pull from MLS
- If you don't have time to pull comps now, send this without listings and add "I'll follow up
  with specific listings in the next hour" to the second paragraph
- James has a hard deadline — Dell start dates don't move. Keep the energy up.
```

---

## Example 3 — Diana email to a personal referral (seller, estate situation)

**Request (from orchestrator, Path C):**
```
Draft request: Diana first email to a personal referral — Helen Park, seller
Voice: Diana Calloway (_shared/voices/diana.md)
Context: Referred by long-time client Tom Chen. Helen's mother passed 3 months ago.
         Estate property in Tarrytown. Helen lives in Houston, hasn't decided timeline yet.
         Hard stop flagged: estate situation → Diana handles directly.
Goal: warm first contact, offer to help her think through it, no push for listing.
```

**Draft output:**
```
DRAFT — Email
From: Diana Calloway
To: Helen Park
Re: Referral from Tom Chen — your mother's home
---
Subject: Tom Chen mentioned you — I wanted to reach out

Helen,

Tom passed along your number. I'm so sorry about your mother.

There's no rush on my end — estate properties have their own timeline and you're the one
who decides when that is. But when you're ready to start thinking through the house, I'm
happy to be a resource. No pressure to list, no pitch. Just an honest conversation about
what the market looks like and what your options are.

I've handled a few estate situations in Austin over the years. I know how much is on your
plate.

Take your time. I'm here when you're ready.

Diana
(512) 555-0100
---
NOTES FOR AGENT:
- Diana sends this personally — not via the team
- Do not CC anyone. This is a quiet, private outreach.
- Hard stop applies: Diana handles all follow-up on this one, no handoff to Marcus or Priya
- If Helen replies and wants to talk, Diana calls within the hour
```

---

## Example 4 — Priya transaction update to buyer clients

**Request (from 04_transaction_coordinator):**
```
Draft request: Transaction update text from Priya to the Okonkwos (buyers, under contract)
Voice: Priya Nair (_shared/voices/priya.md)
Context: Option period expires Friday. Inspection came back with 3 items — minor electrical,
         HVAC filter replacement, a cracked tile in guest bath. Agent and client reviewed.
         Seller agreed to credit $1,200 at closing. Option period releasing Friday.
Goal: update the clients on where things stand, confirm they know the timeline.
```

**Draft output:**
```
DRAFT — Text
From: Priya Nair
To: The Okonkwos
Re: Option period update
---
Good news — seller agreed to the $1,200 credit at closing to cover the inspection items.
Option period releases Friday. We're on track. I'll send a full update email with the
next steps and closing timeline by end of day.

— Priya
---
NOTES FOR AGENT:
- Send the email update by EOD as promised — use 04_transaction_coordinator for checklist content
- Make sure the $1,200 credit is documented in an amendment before option period releases
- If the Okonkwos reply with questions about the inspection items, loop in Marcus for the
  technical conversation
```
