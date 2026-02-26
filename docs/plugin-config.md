# Plugin Configuration

## Templater
- **Template folder:** `Templates`
- **Trigger:** On file creation (for Periodic Notes) or manual insert
- **Project scaffold:** See QuickAdd "Create Project" macro

## Periodic Notes
- **Daily:** Folder `Journal/Daily`, format `YYYY-MM-DD-ddd`, template `Templates/Daily.md`, create on first open
- **Weekly:** Folder `Journal/Weekly`, format `YYYY-[W]WW-Review`, template `Templates/Weekly-Review.md`, create on **Friday**
- **Monthly:** Folder `Journal/Monthly`, format `YYYY-MM-Monthly`, template `Templates/Monthly.md`, create on **last day of month**

## Rollover Daily Todos
- **Source:** Previous daily note
- **Target:** Current daily note
- **Section:** "Tasks" or "Rolled Over"

## QuickAdd
- **Add to Annoyances:** Capture → Append to `Capture/Annoyances.md`, format `- {{value}}`
- **Add to Ideas:** Capture → Append to `Capture/Ideas.md`, format `- {{value}}`
- **Create Project:** See Task 12

## Longform
- **Projects folder:** `Creative`
- Add novel folders under Creative, then "Add project" in Longform

## QuickAdd Capture Setup (Detailed)

1. Open QuickAdd settings
2. **Add to Annoyances:** New Choice → Capture → Name: "Add to Annoyances" → Capture format: `- {{value}}` → Append to: `Capture/Annoyances.md` → Save
3. **Add to Ideas:** Same, append to `Capture/Ideas.md`
4. Optional: Assign hotkeys (e.g. Cmd+Shift+A, Cmd+Shift+I)
