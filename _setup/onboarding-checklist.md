# Onboarding Checklist — Diana Calloway Real Estate AI System
*Run this once. Claude guides you through each step interactively.*
*Estimated time: 20–30 minutes.*

---

## Before you start

You need:
- A Google Workspace account for your team (any paid plan)
- A Claude account with Claude Code (Pro, Max, Team, or Enterprise)
- Admin access to your Google Workspace

Open Claude Code (desktop app or web) in this project folder and say: **"start onboarding"**

Claude will walk you through each step below. Do not try to do these manually — let Claude guide you.

---

## Step 1 — Connect Gmail

**What Claude does:**
Guides you to Claude Settings → Integrations → Gmail → Connect.
Requests these scopes: read messages, compose drafts, manage labels.
Tests the connection by searching your inbox.
Marks Step 1 complete in CLAUDE.md.

**What you do:**
Click Connect in Claude Settings. Authorise the Gmail scopes. Confirm to Claude when done.

**How you know it worked:**
Claude says "Gmail connected. I can see your inbox."

---

## Step 2a — Create the shared lead inbox

**What Claude does:**
Provides exact instructions to create a shared inbox in Google Workspace.
This inbox — `leads@[yourdomain]` — is where all lead emails will arrive.
Every email that arrives here is treated as a lead. No filtering needed.

**What you do:**
1. Go to Google Workspace Admin → Directory → Groups (or Users)
2. Create `leads@[yourdomain]` as a group or shared mailbox
3. Add Diana as the owner. Add all team members as members.
4. Tell Claude the full address (e.g. `leads@dianacalloway.com`)

**How you know it worked:**
Send a test email to `leads@[yourdomain]` from your personal email. Confirm it arrived.

---

## Step 2b — Set up personal inbox forwarding

**What Claude does:**
Generates the exact Gmail filter syntax for each team member.
The filter catches emails from unknown senders that contain lead keywords.
Auto-forwards them to `leads@[yourdomain]`.

**What you do (each team member, one time):**
1. In Gmail → Settings → Filters → Create new filter
2. Claude will give you the exact search query to paste
3. Choose: Skip inbox, Apply label "Potential Lead", Forward to `leads@[yourdomain]`
4. Confirm to Claude when each team member's filter is set

**The filter logic Claude generates:**
```
-from:(@dianacalloway.com) (buy OR sell OR property OR listing OR interested 
OR "looking for" OR "home search" OR realtor OR agent OR showing OR offer)
```

**How you know it worked:**
Forward a test email manually to `leads@`. Confirm it routes correctly.

---

## Step 3 — Connect Google Drive

**What Claude does:**
Guides you to Claude Settings → Integrations → Google Drive → Connect.
Creates the team pipeline spreadsheet automatically with correct columns.
Shares the link into CLAUDE.md config block.

**What you do:**
Click Connect in Claude Settings. Authorise Drive access. Confirm to Claude.

**The pipeline sheet Claude creates:**
`Diana's Team Pipeline` — columns:
`case_id | date | source | prospect_name | contact | lead_type | assigned_agent | urgency | status | next_action | draft_ready | notes | closed_date`

**How you know it worked:**
Claude says "Drive connected. Pipeline sheet created at [link]."

---

## Step 4 — Configure the team

**What Claude does:**
Asks you 4 questions. Writes the answers to `_config/team.md`.
No other action required from you.

**The 4 questions:**
1. What is your team's domain? (e.g. `dianacalloway.com`)
2. What are your team members' names and email addresses?
3. Who handles buyer leads primarily? Who handles listing leads?
4. What is Diana's direct mobile number? (used in drafted communications)

**How you know it worked:**
Claude shows you the completed `_config/team.md` for review. You confirm.

---

## Step 5 — Create the Cloud Routine

**What Claude does:**
Creates the hourly lead-processing routine directly via the Routines tool.
No copy-pasting. No settings page. Claude does it in this conversation.

**The routine:**
- Name: `diana-lead-processor`
- Schedule: hourly, weekdays 7am–9pm / weekends 8am–6pm (your local time)
- What it does: reads `leads@`, processes each unread email through the specialist pipeline, writes drafted responses into assigned agent Gmail drafts, labels processed emails, updates the pipeline sheet, sends Diana an 8am daily digest

**What you do:**
Confirm you want Claude to create it. Claude creates it. Done.

**How you know it worked:**
Claude says "Routine created. ID: [routine_id]. Next run: [time]."

---

## Step 6 — Test run

**What Claude does:**
Sends a mock lead email to `leads@[yourdomain]`.
Waits for the routine to process it (up to 5 minutes).
Checks Gmail drafts via MCP for the drafted response.
Checks the pipeline sheet for the new row.
Confirms everything worked. Marks onboarding complete.
Updates CLAUDE.md STATUS block to OPERATIONAL ✅.

**What you do:**
Say "run the test." Wait. Confirm the draft looks right.

**How you know it worked:**
A draft from Marcus (for the mock buyer lead) appears in marcus@[yourdomain] drafts.
A new row appears in the pipeline sheet.
Claude says "Onboarding complete. System is live."

---

## After onboarding

The system is operational. You do not need to run onboarding again.

**To use the system (Path C — walk-ins, calls, open houses):**
Open Claude Code in this folder. Describe the situation in plain English.
"New lead — phone call, buyer, James Rodriguez, 512-555-0198, looking in Hyde Park, $750k, wants to move in 90 days."
Claude routes it, qualifies it, and drafts a response. Done.

**To reset:**
Delete the STATUS block in CLAUDE.md and say "start onboarding."
