# Core Plugins Overview

Core plugins ship with Obsidian and are enabled by default (unless noted). You don't need to install anything -- just know they're there and what they do.

## Navigation and Discovery

### Backlinks
See which notes link to the current note. Shows both explicit `[[wiki-links]]` (linked mentions) and plain-text mentions of the note's name (unlinked mentions). Click the chain-link icon in the right sidebar, or use the Command Palette > **Backlinks: Show backlinks**. See [Backlinks and Graph View](Backlinks%20and%20Graph%20View.md) for details.

### Graph View
Visualize all notes and their connections as an interactive graph. The **local graph** (showing connections for just the current note) is often more useful than the full vault graph. See [Backlinks and Graph View](Backlinks%20and%20Graph%20View.md).

### Search
Full-text search across the vault with operators like `path:`, `file:`, `tag:`, and `line:`. Press **Ctrl/Cmd + Shift + F**. See [Search](Search.md) for the full operator reference.

### Outline
Shows all headings in the current note as a clickable table of contents in the sidebar. Essential for long notes. Click the outline icon (bulleted list) in the right sidebar.

### Page Preview
Hover over a `[[wiki-link]]` while holding **Ctrl/Cmd** to see a floating preview of the linked note without navigating away.

### Bookmarks
Pin notes, headings, searches, and graph views for quick access. Open a note > three-dot menu > **Bookmark**, or use the Command Palette. Bookmarks are personal (stored in `.obsidian/`, not synced to the repo).

## Content Creation

### Templates
Insert pre-written content into notes, including date and time stamps. Set your template folder in **Settings > Core Plugins > Templates**. Supports `{{title}}`, `{{date}}`, and `{{time}}` variables. See [Templates and Templater](Templates%20and%20Templater.md).

### Canvas
A spatial note-taking surface -- arrange notes, images, links, and text cards on an infinite 2D space. See [Canvas](Canvas.md).

### Daily Notes
One note per day for journaling or scratch notes. Disabled by default. Enable in **Settings > Core Plugins**, then configure date format, file location, and template. Click the calendar icon in the left sidebar to open today's note.

### Properties
Structured metadata (frontmatter) for notes using YAML at the top of a file. Obsidian renders it as editable fields. See [Properties and Frontmatter](Properties%20and%20Frontmatter.md).

## Data and Recovery

### Bases
Structured views of vault content: tables, filters, and queries without code. Requires Obsidian 1.8+. A `.base` file is like a smart spreadsheet that reads your notes. Create one from the Command Palette > **Create new base**. Bases are Obsidian-only -- they don't render when notes are published as static HTML.

### File Recovery
Periodic snapshots of your notes for recovering previous versions. Use the Command Palette > **File recovery: Show saved snapshots**. This is a safety net, not a replacement for Git commits. Snapshots are stored locally in `.obsidian/`.

## Always-On

### Command Palette
The quickest way to do almost anything. Press **Ctrl/Cmd + P** and start typing. Searches across all commands from core plugins, community plugins, and Obsidian itself. Frequently-used commands float to the top. See [Keyboard Shortcuts](Keyboard%20Shortcuts.md) for more.
