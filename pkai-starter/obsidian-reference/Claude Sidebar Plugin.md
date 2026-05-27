# Claude Sidebar Plugin

The Obsidian Claude Sidebar Plugin docks Claude Code into the Obsidian sidebar. It's a JavaScript terminal emulator running Claude Code inside it -- you interact with it like a terminal, not a GUI window.

**Install from:** BRAT (not yet in the community plugin directory)
**GitHub:** [derek-larson14/obsidian-claude-sidebar](https://github.com/derek-larson14/obsidian-claude-sidebar)

## Prerequisites

- Obsidian installed
- Claude Code (the CLI tool) installed and run at least once
- BRAT community plugin installed (see [Installing Community Plugins](Installing%20Community%20Plugins.md))

## Installation

1. Install and enable BRAT (see [Installing Community Plugins](Installing%20Community%20Plugins.md))
2. Go to **Settings > Community plugins > BRAT** (click the gear icon)
3. Click **Add Beta plugin with frozen version**
4. Paste `derek-larson14/obsidian-claude-sidebar` and select **Latest**
5. Click **Install**

The robot icon should appear in the right sidebar. Click it to open Claude Code.

## What it gives you

Claude Code running inside Obsidian means the AI assistant can read and edit notes in your vault directly. It knows the context of your vault (especially if you have a `CLAUDE.md` file describing the vault's purpose and conventions). You can ask it to:

- Create, edit, and organize notes
- Search across your vault and summarize findings
- Run Git commands (commit, push, check status)
- Answer questions about your vault's content
- Execute scripts and shell commands

## Other ways to run Claude Code

The sidebar plugin is convenient, but Claude Code works anywhere a terminal does:

- **VS Code** -- via the official Claude Code extension
- **Terminal / iTerm2 (Mac), PowerShell / Git Bash (Windows)** -- Claude Code is a CLI tool at heart

You can mix and match depending on where your focus is.

## See also

- [Connecting Claude Code to Obsidian](Connecting%20Claude%20Code%20to%20Obsidian.md) -- the full setup workflow
- [Installing Community Plugins](Installing%20Community%20Plugins.md) -- BRAT installation details
- [Recommended Settings](Recommended%20Settings.md) -- the baseline Obsidian configuration
