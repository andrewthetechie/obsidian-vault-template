# Create Project Command Setup

QuickAdd macro to scaffold new projects. Run from Command Palette (Cmd+P → "Create Project").

## Setup Steps

1. Open QuickAdd settings
2. **Macros** → Add Macro → Name: "Create Project"
3. Add Step 1: **Capture** — Prompt for "Project name (lowercase-kebab-case):" → Saves to `{{VALUE}}`
4. Add Step 2: **Template** — Template: `Templates/Project-Homepage.md` → File path: `Projects/{{VALUE}}/_index.md` → Create folders: Yes
5. Save macro
6. **Choices** → Add Choice → Macro → Select "Create Project" → Name: "Create Project"
7. Optional: Assign hotkey

## Verify

Run command, enter `test-project`, confirm `Projects/test-project/_index.md` exists with correct frontmatter.
