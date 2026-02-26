# Personal Vault User Guide

## Vault Goals

- **Searchability** — Tags (`YYYY-MM`), frontmatter types, Dataview queries
- **Low friction** — Auto-created notes, quick capture, minimal clicks
- **LLM use** — Claude, Cursor, OpenClaw can read and navigate via `_index.md` files

## Folder Structure

| Folder | Purpose |
|--------|---------|
| Journal/Daily | Daily notes (auto-created) |
| Journal/Weekly | Friday week-in-review |
| Journal/Monthly | Monthly rollup (last day) |
| Capture | Annoyances, Ideas (quick capture) |
| Projects | Project homepages |
| Creative | Novels (Longform) |
| Learning | Topics being learned |
| Research | OpenClaw research topics |
| Reference | Inventory, misc |
| Archive | Archived projects and learning |

## Daily Workflow

1. Open Obsidian → daily note auto-created
2. Rollover copies yesterday's unchecked tasks
3. Add thoughts, tasks, notes (~2 min)

## Quick Capture (Annoyances / Ideas)

- **Option A:** Bookmark `Capture/Annoyances.md` and `Capture/Ideas.md` → open and add bullets
- **Option B:** QuickAdd "Add to Annoyances" or "Add to Ideas" → modal → appends to file

## New Project

Run QuickAdd → Create Project (or Cmd+P → "QuickAdd" → "Create Project"), enter project name (e.g. `phone-cluster`), press Enter. Creates `_index.md` (homepage), `ToDo.md` (task list), and `Research.md` (links + freeform thoughts). Fill in overview and links on the homepage. See docs/create-project-setup.md for setup.

## Weekly

Friday: weekly review auto-created. Write summary, accomplishments, carry-over. Dataview links to week's daily notes.

## Monthly

Last day of month: monthly auto-created. Write summary. Dataview links to month's weekly reviews.

## Archive

Drag project folder to `Archive/Projects/` or learning topic to `Archive/Learning/`. Optionally set `status: archived` in frontmatter.

## Research (OpenClaw)

Create note in `Research/<topic>/` with links or questions. Tag with `#openclaw` if using watcher. Point OpenClaw at folder/tag manually or automatically.

## Creative (Novels)

Create folder under `Creative/<novel-name>/`. Add as Longform project. Use Longform sidebar for scenes, ordering, export.

## LLM Navigation

Start at `_index.md`. Follow links to section indexes. Use `[[links]]` to navigate.

## Getting Value

- Bookmark Capture files for one-click access
- Set hotkeys for Add to Annoyances (Cmd+Shift+A) and Add to Ideas (Cmd+Shift+I)
- Review weekly on Friday — builds habit
- Graduate items from Capture to Projects when ready
