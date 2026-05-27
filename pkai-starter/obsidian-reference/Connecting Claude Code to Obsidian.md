# Connecting Claude Code to Obsidian

Claude Code is a CLI tool that runs in a terminal. The Claude Sidebar Plugin embeds a terminal inside Obsidian so you can use Claude Code without leaving your vault.

## Prerequisites

- **Obsidian** installed from [obsidian.md](https://obsidian.md) (no account needed)
- **Claude Code** (the CLI tool) installed and run at least once
- A working terminal setup (Claude Code needs to work in your terminal before it'll work in Obsidian)

## Setup steps

1. **Enable community plugins** in Obsidian: Settings > Community plugins > Turn on community plugins
2. **Install BRAT:** Settings > Community Plugins > Browse, search for "BRAT", install and enable
3. **Install the Claude Sidebar Plugin via BRAT:**
   - Go to Settings > Community plugins > BRAT (gear icon)
   - Click **Add Beta plugin with frozen version**
   - Paste `derek-larson14/obsidian-claude-sidebar` and select **Latest**
   - Click **Install**
4. **Open Claude Code:** Click the robot icon in the right sidebar

You're now running Claude Code inside Obsidian. It works exactly like the terminal version -- type your questions and instructions, and Claude reads and edits files in your vault.

## Making Claude Code useful: CLAUDE.md

Create a `CLAUDE.md` file in your vault root. This file tells Claude what the vault is about, what conventions to follow, and what matters. Without it, Claude is flying blind.

Even a minimal one helps:

```markdown
# CLAUDE.md

This vault is [what it is]. It's for [what you use it for].

## Structure

- [describe your folder layout, if any]

## Conventions

- [any rules you want Claude to follow]
```

As your vault develops conventions, update CLAUDE.md so Claude stays current.

## Other ways to run Claude Code

The sidebar plugin is convenient, but Claude Code works in any terminal:

- **VS Code** -- via the official Claude Code extension
- **Terminal / iTerm2 (Mac)** -- Claude Code is a CLI tool at heart
- **PowerShell / Git Bash (Windows)** -- works there too

You can mix and match. Some people prefer Claude Code in VS Code for coding projects and in Obsidian for knowledge work.

## See also

- [Claude Sidebar Plugin](Claude%20Sidebar%20Plugin.md) -- plugin details and installation
- [Recommended Settings](Recommended%20Settings.md) -- baseline Obsidian configuration
- [Working with Multiple Vaults](Working%20with%20Multiple%20Vaults.md) -- each vault gets its own CLAUDE.md
