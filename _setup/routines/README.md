# Scheduled task prompts

These files are the exact prompts the Denise HTR scheduled tasks run. Keep them in sync with the live tasks: a task stores its own copy of the prompt, so editing a file here does NOT change a live task until the task is updated or recreated with the new text.

| Scheduled task | ID | Schedule (America/Chicago) | Prompt file |
|---|---|---|---|
| denise-htr-lead-processor | trig_01X8y2hpMTA8zNENPkZ13fbg | hourly at :01, Mon–Fri 7am–9pm | lead-processor.md |
| denise-htr-lead-processor-weekend | trig_01E1VEHcFdMnNJDzyXsUFcTW | hourly at :02, Sat–Sun 8am–6pm | lead-processor.md (identical) |
| denise-htr-daily-briefing | trig_019NDy2HxLeRYcDVLsEFuHaY | daily 7:56am | daily-briefing.md |

## Status (2026-10-06)

- Created and enabled with the prompt text in this folder, each starting a fresh session per run, with Gmail, Google Drive and Google Sheets attached. They also have every other connector on the account attached; remove the extras on the claude.ai Routines page (only Gmail, Google Drive and Google Sheets are needed).
- Superseded tasks to DELETE on the Routines page (they hold old prompt text and would process every lead twice): diana-lead-processor (trig_0121KPGDonoCPoehq62WnAUc), diana-lead-processor-weekend (trig_01VJALu8DmQyg49sT8Pk3aDa), diana-daily-briefing (trig_01KRKyeyjfh68cDwQhVci3aK), plus the earlier disabled onboarding set (trig_01J9igYYQTfv7Nm3gwVG4Pdy, trig_01KcjNvrvQpjM86xTdFUD5Fs, trig_01AVLy24KpyohtetEnZa45Gx) if they still exist.
- A task stores its own copy of the prompt: editing a file here does not change a live task until the task is updated or recreated.
- Pushing case files back to this repo needs write access from the scheduled task's session. Check the first run summaries to confirm the push works.
