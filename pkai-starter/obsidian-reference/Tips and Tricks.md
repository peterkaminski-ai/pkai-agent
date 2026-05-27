# Tips and Tricks

Practical tips for working with Obsidian, collected from daily use.

## Navigation

### See the outline of a note
Long notes can be hard to navigate. The **Outline** panel shows all headings as a clickable table of contents. Click the outline icon (bulleted list) in the right sidebar, or Command Palette > **Outline: Show outline**.

### Preview linked notes without navigating
Hold **Ctrl/Cmd** and hover over any `[[wiki-link]]` to see a floating preview. Release to dismiss. Saves constant back-and-forth in notes with many cross-references.

### Bookmark your most-used notes
If you keep going back to the same notes, pin them with Bookmarks. Open a note > three-dot menu > **Bookmark**, or Command Palette > **Bookmarks: Bookmark current file**. Open the bookmarks panel from the left sidebar. Bookmarks are personal -- stored in `.obsidian/`, not synced to the repo.

## Editing

### Insert today's date or time
Instead of typing the date manually, use the Templates core plugin:

1. Set your date format in **Settings > Core Plugins > Templates** (e.g., `YYYY-MM-DD`)
2. Command Palette > **Templates: Insert current date** or **Templates: Insert current time**

Assign hotkeys for even faster access: **Settings > Hotkeys**, search for "Insert current".

### Turn a note into a folder
When a note grows and needs sub-notes, the Folder Notes community plugin does it in one step. Command Palette > **Folder Notes: Create Folder Note**. This creates a folder with the same name and moves the note inside as the index page.

## Discovery

### See what links where
Every note has a Backlinks panel showing linked mentions (explicit `[[wiki-links]]`) and unlinked mentions (plain-text matches). Click the chain-link icon in the right sidebar. Unlinked mentions are especially useful -- click the link button to convert them to proper wiki-links.

### Visualize the graph
The Graph View shows all notes and connections as an interactive graph. The **local graph** (Command Palette > **Graph view: Open local graph**) is usually more useful than the full vault graph -- it shows just the connections for the current note.

### Strange New Worlds
The Strange New Worlds community plugin adds inline counters next to every `[[wiki-link]]` and `#tag`, showing how many other notes reference the same target. Click the badge to see the list. Makes the network visible without opening the graph.

## Vault as a database

### Querying with Bases
Obsidian Bases (1.8+) let you create table views of your notes filtered by folder, tags, or properties -- no code needed. Command Palette > **Create new base**. Embed a Base in any note with `![[MyBase.base#Contents]]`.

### Querying with scripts
Since notes are plain Markdown with YAML frontmatter, any script can query them. A Python script with `pyyaml` can list all notes by a specific author, find notes missing frontmatter, or build timelines. Claude Code can also answer structured questions about your vault directly -- often faster than writing a script for one-off queries.

## Working with frontmatter

- Frontmatter must be the very first thing in the file -- even a blank line before `---` breaks it
- Use ISO 8601 dates (`YYYY-MM-DD`) so they sort correctly
- The `aliases` field lets you create alternative names for a note: `aliases: [JD, Jane]` means `[[JD]]` resolves to the same page
- If unsure what fields to use, look at existing notes in the same folder

## General

- **Command Palette is your friend.** Ctrl/Cmd + P gets you to any command. Use it constantly.
- **Frequently-used commands rise to the top** of the Command Palette. The more you use a command, the easier it becomes to find.
- **Assign hotkeys** to commands you use all the time: Settings > Hotkeys, search for the command name.
- **Don't over-organize upfront.** Start with a flat folder of notes and add subfolders when a category has enough pages to justify one.

## See also

- [Keyboard Shortcuts](Keyboard%20Shortcuts.md) -- the essential shortcuts in one place
- [Core Plugins Overview](Core%20Plugins%20Overview.md) -- what's built in
- [Essential Community Plugins](Essential%20Community%20Plugins.md) -- what's worth adding
