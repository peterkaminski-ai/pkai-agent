# Templates and Templater

Obsidian has two template systems: the built-in **Templates** core plugin and the **Templater** community plugin. For most people, the core plugin is enough. Templater adds scripting for advanced workflows.

## Templates (core plugin)

### Setup

1. Go to **Settings > Core Plugins** and make sure **Templates** is enabled
2. Click the gear icon next to Templates
3. Set the **Template folder location** (e.g., `Templates`)
4. Set your preferred date format (e.g., `YYYY-MM-DD`) and time format (e.g., `HH:mm`)

### Using a template

1. Create a new note
2. Open the Command Palette (Ctrl/Cmd + P)
3. Run **Templates: Insert template**
4. Pick the template you want

The template content gets inserted into your note. You can then edit it as normal.

### Inserting dates and times

You don't need a full template just to insert a date. The Templates plugin provides standalone commands:

- **Templates: Insert current date** -- inserts today's date in your configured format
- **Templates: Insert current time** -- inserts the current time

Assign hotkeys to these for fast access: **Settings > Hotkeys**, search for "Insert current".

### Template variables

| Variable | Inserts |
|----------|---------|
| `{{title}}` | The note's title (filename without extension) |
| `{{date}}` | Today's date (format set in template settings) |
| `{{time}}` | Current time (format set in template settings) |

### Tips

- **Templates are just notes.** Edit them anytime; changes apply to future insertions, not past ones.
- **You can have as many templates as you want.** Meeting notes, project pages, journal entries -- whatever patterns you repeat.
- **Templates + Bases = less maintenance.** A folder note template with an embedded Base gives every new folder an auto-updating index.

## Templater (community plugin)

Templater is a more powerful alternative that adds scripting, conditionals, date arithmetic, and custom functions. Install it from **Settings > Community Plugins > Browse**, search for "Templater".

### What Templater adds over core Templates

| Feature | Example |
|---------|---------|
| Date manipulation | `<% tp.date.now("YYYY-MM-DD", 7) %>` -- date 7 days from now |
| File metadata | `<% tp.file.title %>`, `<% tp.file.creation_date() %>`, `<% tp.file.folder() %>` |
| Conditionals | `<% if (tp.file.folder() === "Projects") { %>` ... `<% } %>` |
| User prompts | `<% tp.system.prompt("What's the topic?") %>` -- asks for input on insertion |
| Auto-templates | Assign a template to a folder so every new note gets it automatically |

### When to use which

- **Templates (core):** simple templates with `{{title}}`, `{{date}}`, `{{time}}`. Good enough for most uses.
- **Templater (community):** when you need date math, conditionals, prompts, or folder-based auto-insertion. Overkill for simple cases, powerful for complex workflows.

## See also

- [Properties and Frontmatter](Properties%20and%20Frontmatter.md) -- include frontmatter in your templates for consistent metadata
- [Core Plugins Overview](Core%20Plugins%20Overview.md) -- where Templates fits in the plugin landscape
