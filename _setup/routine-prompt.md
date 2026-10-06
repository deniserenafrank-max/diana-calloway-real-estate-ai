# Scheduled tasks — plain-language description
# NOT the prompt text. The exact prompts are in _setup/routines/.
# This file explains what each scheduled task does so anyone on the team can understand it.

# ─────────────────────────────────────────
# TASK 1: diana-lead-processor (weekdays) and diana-lead-processor-weekend
# Schedule: hourly, weekdays 7am–9pm, weekends 8am–6pm (America/Chicago)
# Trigger: time-based only. Nothing starts when an email arrives; the next hourly run picks it up.
# What it does:
#   1. Gmail MCP → finds unread mail to leads@hometownrealtorsoftexas.com without the "Processed" label
#   2. For each email: orchestrator identifies lead type, source and urgency
#   3. Lead Qualifier extracts structured data, creates/updates the case file in _shared/cases/
#   4. Assigns the agent per _config/team.md (Denise by default; Keith only if reassigned)
#   5. Client Communication drafts the first response in the assigned agent's voice
#   6. Gmail MCP → saves the draft to Denise's Gmail Drafts ("[For Keith]" subject prefix for Keith's cases). Never sends.
#   7. Gmail MCP → labels the original email "Processed"
#   8. Adds a pipeline row (Google Sheet, or _shared/pipeline.csv if Sheets can't be written)
#   9. Lists nurture touches due today in its run summary
#  10. Commits and pushes the case files to main

# ─────────────────────────────────────────
# TASK 2: diana-daily-briefing
# Schedule: 7:56am daily (America/Chicago)
# Trigger: time-based
# What it does:
#   1. Reads all case files in _shared/cases/
#   2. Identifies:
#      - CRITICAL or HIGH leads with no agent action logged in the past 24 hours
#      - Nurture leads with a scheduled touch due today or overdue
#      - Active deals under contract with deadlines in the next 7 days
#        (option period end, financing contingency, close date)
#      - Leads processed in the last 24 hours that are not yet marked reviewed
#   3. Formats a short briefing — one section per category, no padding
#   4. Gmail MCP → emails it to denise@ and keith@hometownrealtorsoftexas.com
#   5. Subject line format: "Team briefing — [Day, Date] — [N] items need action"
