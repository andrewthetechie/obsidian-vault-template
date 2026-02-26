# Plugin Configuration

## Templater
- **Template folder:** `Templates`
- **Trigger:** On file creation (for Periodic Notes) or manual insert
- **Project scaffold:** See QuickAdd "Create Project" (docs/create-project-setup.md)

## Periodic Notes
- **Daily:** Folder `Journal/Daily`, format `YYYY-MM-DD-ddd`, template `Templates/Daily.md`, create on first open
- **Weekly:** Folder `Journal/Weekly`, format `YYYY-[W]WW-Review`, template `Templates/Weekly-Review.md`, create on **Friday**
- **Monthly:** Folder `Journal/Monthly`, format `YYYY-MM-Monthly`, template `Templates/Monthly.md`, create on **last day of month**

## Rollover Daily Todos
- **Source:** Previous daily note
- **Target:** Current daily note
- **Section:** "Tasks" or "Rolled Over"

## QuickAdd

QuickAdd has four choice types: **Template**, **Capture**, **Macro**, and **Multi**. When you click "Add Choice", you must select the type from the dropdown (Template is often the default—look for Capture and Macro).

- **Template Folder Path** (in QuickAdd settings → Templates & Properties): Set to `Templates` (or `templates`—match your vault's folder name)
- **Add to Annoyances:** Capture choice → appends to `Capture/Annoyances.md`
- **Add to Ideas:** Capture choice → appends to `Capture/Ideas.md`
- **Create Project:** Macro (creates homepage + ToDo + Research) → see docs/create-project-setup.md

## Longform
- **Projects folder:** `Creative`
- Add novel folders under Creative, then "Add project" in Longform

## QuickAdd Capture Setup (Detailed)

Capture choices append your input to a file. Setup:

1. Open QuickAdd settings → **Choices & Packages**
2. Click **Add Choice** → select **Capture** (not Template)
3. **Add to Annoyances:**
   - Name: `Add to Annoyances`
   - **Capture To:** `Capture/Annoyances.md` (file path)
   - **Capture Format:** `- {{VALUE}}` (bullet + your input)
   - Enable **Write to bottom of file**
   - Save
4. **Add to Ideas:** Repeat with `Capture/Ideas.md`
5. Optional: Assign hotkeys (e.g. Cmd+Shift+A, Cmd+Shift+I) via Obsidian Settings → Hotkeys
