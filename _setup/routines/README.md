# Scheduled task prompts

These files are the exact prompts the Denise HTR scheduled tasks run. Keep them in sync with the live tasks: a task stores its own copy of the prompt, so editing a file here does NOT change a live task until the task is updated or recreated with the new text.

| Scheduled task | ID | Schedule (America/Chicago) | Prompt file |
|---|---|---|---|
| diana-lead-processor | trig_0121KPGDonoCPoehq62WnAUc | hourly at :02, Mon–Fri 7am–9pm | lead-processor.md |
| diana-lead-processor-weekend | trig_01VJALu8DmQyg49sT8Pk3aDa | hourly at :02, Sat–Sun 8am–6pm | lead-processor.md (identical) |
| diana-daily-briefing | trig_01KRKyeyjfh68cDwQhVci3aK | daily 7:56am | daily-briefing.md |

## Status (2026-10-06)

- Created and enabled, each starting a fresh session per run, with Gmail, Google Drive and Google Sheets attached. They also have every other connector on the account attached; remove the extras on the claude.ai Routines page (only Gmail, Google Drive and Google Sheets are needed).
- The live tasks still hold the ORIGINAL prompt text (branch claude/awesome-gates-gmrzyz, 662 phone number). The prompt files here now point at `main` and use (832) 661-0475. Update the live tasks with this text, or recreate them and delete the old ones.
- An earlier set created during onboarding (trig_01J9igYYQTfv7Nm3gwVG4Pdy, trig_01KcjNvrvQpjM86xTdFUD5Fs, trig_01AVLy24KpyohtetEnZa45Gx) was disabled. Delete those on the Routines page if they still exist.
- Pushing case files back to this repo needs write access from the scheduled task's session. Check the first run summaries to confirm the push works.
