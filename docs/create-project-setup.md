# Create Project Command Setup

QuickAdd **Macro** to scaffold new projects with homepage, ToDo list, and Research doc. Run from Command Palette (Cmd+P → "QuickAdd" → "Create Project").

## Project Structure Created

Each project gets:
- `_index.md` — Project homepage (overview, links, status)
- `ToDo.md` — Task list with header linking to project
- `Research.md` — Links and Freeform Thoughts sections

## Setup Steps

### 1. Create the Three Template Choices

Create these **Template** choices first (they will be nested by the macro). For each, use **Add Choice** → **Template**.

**Choice A: Create Project - Homepage**
- Name: `Create Project - Homepage`
- Template Path: `Project-Homepage.md`
- Create in folder: `Projects/{{VALUE:projectName}}`
- File Name Format: `_index`
- Open: Off (macro will open the homepage at the end)

**Choice B: Create Project - ToDo**
- Name: `Create Project - ToDo`
- Template Path: `Project-ToDo.md`
- Create in folder: `Projects/{{VALUE:projectName}}`
- File Name Format: `ToDo`
- Open: Off

**Choice C: Create Project - Research**
- Name: `Create Project - Research`
- Template Path: `Project-Research.md`
- Create in folder: `Projects/{{VALUE:projectName}}`
- File Name Format: `Research`
- Open: Off

### 2. Create the User Script

The template includes `scripts/quickadd-create-project.js`. If you copied the template folder into your vault, it should already exist. Otherwise create it with:

```javascript
module.exports = async (params) => {
  const { quickAddApi, variables } = params;
  const name = await quickAddApi.inputPrompt("Project name (lowercase-kebab-case):");
  if (!name) return params.abort();
  variables.projectName = name.toLowerCase().replace(/\s+/g, "-");
};
```

### 3. Create the Macro

1. **Add Choice** → **Macro** → Name: `Create Project`
2. Open the macro builder (gear icon)
3. Add commands in order:
   - **User Script** — Select the script from step 2
   - **Nested Choice** — Select "Create Project - Homepage"
   - **Nested Choice** — Select "Create Project - ToDo"
   - **Nested Choice** — Select "Create Project - Research"
4. Optional: Add **Open File** as last command — Path: `Projects/{{VALUE:projectName}}/_index` — to open the new homepage
5. Save

### 4. Template Folder Path

In QuickAdd settings → **Templates & Properties** → **Template Folder Path**, set to `Templates` (or `templates` if your folder is lowercase).

## Verify

1. Run QuickAdd → Create Project
2. Enter project name (e.g. `test-project`)
3. Confirm:
   - `Projects/test-project/_index.md` exists
   - `Projects/test-project/ToDo.md` exists with header and empty todo
   - `Projects/test-project/Research.md` exists with Links and Freeform Thoughts sections
