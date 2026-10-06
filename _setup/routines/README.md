# Cloud Routine prompts

These are the exact prompts Claude created the three Cloud Routines with during
onboarding Step 5 (2026-10-06). Keep them in sync with the live routines.

| Routine | Trigger ID | Schedule (America/Chicago) | Prompt file |
|---|---|---|---|
| diana-lead-processor | trig_01J9igYYQTfv7Nm3gwVG4Pdy | hourly, Mon–Fri 7am–9pm | lead-processor.md |
| diana-lead-processor-weekend | trig_01KcjNvrvQpjM86xTdFUD5Fs | hourly, Sat–Sun 8am–6pm | lead-processor.md (identical) |
| diana-daily-briefing | trig_01AVLy24KpyohtetEnZa45Gx | daily 7:56am | daily-briefing.md |

## Status (2026-10-06): created but DISABLED — connectors not attached

Routines created from a Claude Code session cannot carry connectors, so a test
fire of diana-lead-processor ran with no Gmail tools and stopped safely.
To finish Step 5, open https://claude.ai/code/routines (or Routines in the
claude.ai sidebar), edit each routine, attach **Gmail** (lead processors also
**Google Drive**), and switch it to enabled. If editing is not possible,
create new routines there with the schedules above and the matching prompt
file below, then delete the disabled ones.

Each routine needs the **Gmail** connector (lead processor also uses **Google Drive**).
If a routine is recreated from the claude.ai Routines page, paste the matching
prompt file as its instructions and attach those connectors.
