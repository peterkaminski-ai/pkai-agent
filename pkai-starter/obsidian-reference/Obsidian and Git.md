# Obsidian and Git

An Obsidian vault is just a folder of Markdown files. That makes it a natural fit for Git version control. Every note is a text file, diffs are readable, and collaboration works through standard Git workflows.

## Why use Git with Obsidian

- **Version history:** see what changed, when, and why. Recover any previous version of any note.
- **Backup:** push to GitHub (or any remote) for offsite backup.
- **Collaboration:** multiple people work in the same vault by cloning the repo, editing, and pushing changes.
- **Works with Claude Code:** Claude can commit, push, and check status directly from the sidebar.

## Setting up Git in a vault

The easiest way is to ask Claude Code:

> Initialize a git repo here and create a .gitignore for an Obsidian vault.

Claude Code will run `git init` and create a `.gitignore` that excludes workspace files and other things that shouldn't be tracked.

### A typical .gitignore for an Obsidian vault

```
.obsidian/workspace.json
.obsidian/workspace-mobile.json
.DS_Store
```

You may want to add entries for build artifacts, credentials, or large binaries depending on your vault's purpose.

### First commit

```bash
git add -A
git commit -m "Initial commit"
```

Or ask Claude Code: "Commit everything with the message 'Initial commit'"

### Creating a GitHub repo

Ask Claude Code:

> Create a private GitHub repo for this vault and push to it.

Claude Code uses the `gh` CLI to create the repo and push. You choose private (only you and invited collaborators) or public (visible to everyone).

## What to commit

Most things in an Obsidian vault are fine to commit:

| Commit | Don't commit |
|--------|-------------|
| All `.md` files | `.obsidian/workspace.json` (personal UI state) |
| `.obsidian/app.json` (shared settings) | Credentials or secrets |
| `.obsidian/plugins/` (shared plugin setup) | Large binary files |
| `CLAUDE.md` | |
| `.gitignore` | |

The `.obsidian/` folder is usually committed so everyone shares the same plugin setup and core settings. `workspace.json` is personal UI state (which tabs you have open) and generates noisy diffs -- add it to `.gitignore`.

## The .obsidian folder

The `.obsidian/` directory contains all vault configuration:

| File | What it controls |
|------|-----------------|
| `app.json` | Core settings (inline title, line numbers, new-file location) |
| `appearance.json` | Theme and appearance |
| `core-plugins.json` | Which core plugins are enabled/disabled |
| `community-plugins.json` | List of installed community plugin IDs |
| `plugins/` | Community plugin code and settings |
| `workspace.json` | Current UI layout (usually gitignored) |

## Daily workflow

Once Git is set up, the daily workflow is simple:

1. Work in Obsidian as normal
2. Periodically ask Claude Code: "Commit and push my changes"
3. Or use the terminal: `git add -A && git commit -m "session notes" && git push`

For shared vaults, pull before you start working: `git pull` or ask Claude Code to do it.

## See also

- [Connecting Claude Code to Obsidian](Connecting%20Claude%20Code%20to%20Obsidian.md) -- Claude Code can run Git commands from the sidebar
- [Working with Multiple Vaults](Working%20with%20Multiple%20Vaults.md) -- each vault can be its own Git repo
- [Troubleshooting](Troubleshooting.md) -- common Git + Obsidian issues
