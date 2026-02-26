# Template Customization Guide

## Where Templates Live

All templates are in the `Templates/` folder at the vault root.

## How Templater Uses Them

- **Insert template:** Run Templater → Insert template, or use folder triggers
- **Periodic Notes:** Daily, Weekly, Monthly templates are triggered automatically when notes are created
- **QuickAdd:** Create Project macro uses `Templates/Project-Homepage.md`

## Editing an Existing Template

1. Open the template file in `Templates/`
2. Change frontmatter, sections, or Dataview queries
3. Save — changes apply to newly created notes (existing notes are unchanged)

## Adding a New Template

1. Create `Templates/NewTemplate.md` with your content
2. **If manual use:** Add Templater insert command or QuickAdd choice
3. **If periodic:** Register in Periodic Notes settings (Daily/Weekly/Monthly)
4. **If new note type:** Add to relevant `_index.md` Dataview query (see below)

## Templater Syntax Reference

| Syntax | Purpose |
|--------|---------|
| `tp.date.now("YYYY-MM-DD")` | Current date |
| `tp.date.now("YYYY-MM")` | Current month |
| `tp.date.now("dddd, MMMM D")` | Formatted date |
| `tp.file.folder(true)` | Full folder path (e.g. "Projects/phone-cluster") |
| `tp.file.folder(true).split("/").pop()` | Folder name only |
| `tp.file.title` | Current file title |

## Updating Section Indexes

When adding a new note type (e.g. `type: sprint`):

1. Add the `type` to your template's frontmatter
2. Update the relevant `_index.md` Dataview query to include it
3. Example: `WHERE type = "project" OR type = "sprint"`

## Reference

- [Templater docs](https://silentvoid13.github.io/Templater/)
- [Dataview docs](https://blacksmithgu.github.io/obsidian-dataview/)
