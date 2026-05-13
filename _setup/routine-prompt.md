# STUB — Cloud Routine: what it does (internal documentation)
# NOT a user-facing copy-paste template.
# Claude creates this routine automatically during onboarding step 5 via CronCreate/Routines tool.
# This file documents what the routine does so any team member can read and understand it.
#
# Routine: diana-lead-processor
# Schedule: hourly, weekdays 7am-9pm, weekends 8am-6pm (team's local time)
# Trigger: time-based + (future) Redfin webhook
# What it does:
#   1. Gmail MCP → read all unread emails in leads@[domain]
#   2. For each email: orchestrator identifies lead type + urgency
#   3. Lead Qualifier extracts structured data, creates/updates case file
#   4. Assigns agent based on lead type (buyers → Marcus, listings → Priya, VIP/referrals → Diana)
#   5. Client Communication drafts first response in assigned agent's voice
#   6. Gmail MCP → writes draft into assigned agent's drafts folder
#   7. Gmail MCP → labels original email "Processed — [case_id]"
#   8. Updates Google Sheet pipeline row
#   9. At 8am daily: sends Diana a digest of overnight activity
