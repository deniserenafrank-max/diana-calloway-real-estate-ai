# Cloud Routines — internal documentation
# NOT a user-facing copy-paste template.
# Claude creates both routines automatically during onboarding step 5 via CronCreate/Routines tool.
# This file documents what each routine does so any team member can read and understand it.

# ─────────────────────────────────────────
# ROUTINE 1: diana-lead-processor
# Schedule: hourly, weekdays 7am–9pm, weekends 8am–6pm (Austin local time)
# Trigger: time-based (future: Redfin webhook for instant CRITICAL alerts)
# What it does:
#   1. Gmail MCP → read all unread emails in leads@[domain]
#   2. For each email: orchestrator identifies lead type + urgency
#   3. Lead Qualifier extracts structured data, creates/updates case file in _shared/cases/
#   4. Assigns agent based on lead type (buyers → Marcus, listings → Priya, VIP/referrals → Diana)
#   5. Client Communication drafts first response in assigned agent's voice
#   6. Gmail MCP → writes draft into assigned agent's Gmail drafts folder
#   7. Gmail MCP → labels original email in leads@ as "Processed — [case_id]"
#   8. Checks open nurture leads for any touches due today and flags them in the daily briefing

# ─────────────────────────────────────────
# ROUTINE 2: diana-daily-briefing
# Schedule: 8am daily, every day (Austin local time)
# Trigger: time-based
# What it does:
#   1. Reads all case files in _shared/cases/
#   2. Identifies:
#      - CRITICAL or HIGH leads with no agent action logged in the past 24 hours
#      - Nurture leads with a scheduled touch due today or overdue
#      - Active deals under contract with deadlines in the next 7 days
#        (option period end, financing contingency, close date)
#      - Any leads processed overnight by diana-lead-processor not yet reviewed
#   3. Formats a concise morning briefing — one section per category, no padding
#   4. Gmail MCP → sends the briefing as an email to the full team
#      (diana@, marcus@, priya@, jordan@ — all at [domain])
#   5. Subject line format: "Team briefing — [Day, Date] — [N] items need action"
