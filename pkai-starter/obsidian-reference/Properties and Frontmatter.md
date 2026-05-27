# Properties and Frontmatter

Properties (also called frontmatter) let you add structured metadata to notes using YAML at the top of a file. Obsidian renders this as editable fields via the Properties core plugin.

## What it looks like

```yaml
---
date: 2026-03-19
author: Jane Smith
tags: [project, active]
---
```

Everything between the two `---` lines is metadata, not content. It won't appear in the note body (Obsidian displays it as a clean form instead).

## Adding frontmatter

- **Manually:** type `---` at the very first line of the note, add your fields, close with another `---`
- **Via the UI:** in reading mode, click the properties icon (top of the note) to add fields visually
- **Via templates:** include frontmatter in your templates so every new note starts with the right fields

**Important:** Frontmatter must be the very first thing in the file. Even a blank line before `---` will break it.

## Common fields

| Field | Example | Purpose |
|-------|---------|---------|
| `date` | `2026-03-19` | When the note was created or relevant |
| `tags` | `[project, active]` | Categorization (searchable with `tag:` operator) |
| `aliases` | `[JD, Jane]` | Alternative names for the note -- `[[JD]]` and `[[Jane]]` both resolve to the same page |
| `author` | `Jane Smith` | Who wrote it |

## Why it matters

- **Bases queries** can filter and sort notes by frontmatter fields (e.g., show all notes with a `date` in the last week)
- **Search** can target frontmatter with operators like `tag:project`
- **Consistency:** when everyone uses the same fields the same way, the vault becomes queryable as a lightweight database

## Tags

Tags are words prefixed with `#` that you can add anywhere in a note. They work in two places:

- **Inline:** type `#my-tag` anywhere in the note body
- **In frontmatter:** add a `tags` field (see above)

Both are equivalent for search purposes. Frontmatter tags are tidier; inline tags are useful when you want to tag a specific section.

### Tag conventions

- Use lowercase, hyphenated tags: `#folder-readme`, not `#FolderReadme`
- Nested tags work: `#project/active`, `#project/archived`
- Avoid over-tagging -- a few meaningful tags are better than many vague ones

### Tags vs. folders vs. links

| Method | Best for | Example |
|--------|----------|---------|
| **Folders** | Physical grouping, clear hierarchy | `Projects/`, `Reference/` |
| **Tags** | Cross-cutting categories that span folders | `#active` appears in many folders |
| **Links** | Specific connections between notes | `[[Jane Smith]]` in a project page |

Tags complement folders and links. A note lives in one folder but can have many tags.

## Tips

- Use ISO 8601 dates (`YYYY-MM-DD`) so they sort correctly
- The `aliases` field is particularly useful for people -- `aliases: [JD, Jane]` means both short forms resolve to the full note
- If you're unsure what fields to use, look at existing notes in the same folder for examples

## See also

- [Search](Search.md) -- finding notes by tag and other operators
- [Templates and Templater](Templates%20and%20Templater.md) -- include frontmatter in templates for consistency
