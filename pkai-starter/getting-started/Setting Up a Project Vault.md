# Setting Up a Project Vault

You have a project — maybe it already has some files, maybe you're starting fresh. You want to turn it into a proper workspace: an Obsidian vault with its own Claude Code context and a GitHub repo for backup and collaboration.

This guide assumes you already have Obsidian, Claude Code, and a GitHub account set up. If not, start with the setup pages earlier in this wiki.

## Prerequisites

- Obsidian installed
- Claude Code installed and authenticated
- A GitHub account
- The `gh` CLI (GitHub's command-line tool) — Claude Code can install it for you if you don't have it

## 1. Choose a Location

Your project folder should **not** be inside iCloud, OneDrive, Dropbox, or any other cloud-synced folder. Git and cloud sync don't mix — you'll get conflicts and corrupted files.

A good location is a dedicated folder like `~/Obsidian-GitHub/` or `~/Vaults/` (Mac), or `C:\Users\YourName\Obsidian-GitHub\` (Windows).

If you already have a project folder somewhere else, move it to a safe location first.

## 2. Create or Move Your Project Folder

If you're starting fresh, create a new empty folder in your safe location and name it after your project.

If you have existing files, move them into a folder in your safe location.

## 3. Open the Folder in Obsidian

1. Open Obsidian
2. Click the vault name in the bottom-left corner (or use **File > Open vault**)
3. Choose **Open folder as vault**
4. Navigate to your project folder and select it

Obsidian will create a `.obsidian/` directory inside the folder. That's all a vault is — a folder with `.obsidian/` and your files in it.

## 4. Configure Obsidian Settings

With the new vault open, go to **Settings** (gear icon, lower left):

- **Editor** — Turn on "Show line number"
- **Files and Links** — Turn on "Detect all file extensions." Set "Default location for new notes" to "Same folder as current file"
- **Appearance** — Turn off "Inline title"

See [Configuring Obsidian](Configuring%20Obsidian.md) for details.

## 5. Install the Claude Code Sidebar

Follow the steps from [Connecting Claude Code to Obsidian](Connecting%20Claude%20Code%20to%20Obsidian.md):

1. Enable community plugins
2. Install and enable BRAT
3. Use BRAT to install the Claude Sidebar plugin (`derek-larson14/obsidian-claude-sidebar`)
4. Open the sidebar with the robot icon

## 6. Create a CLAUDE.md

This is an important step. CLAUDE.md tells Claude Code what your vault is about, what conventions to follow, and what matters. Without it, Claude is flying blind.

Ask Claude Code:

> Create a CLAUDE.md for this project. It's about [describe your project in a sentence or two].

Or write one yourself. Even a few lines make a big difference:

```markdown
# CLAUDE.md

This vault is [what it is]. It's for [what you use it for].

## Structure

- [describe your folder layout, if any]

## Conventions

- [any rules you want Claude to follow]
```

## 7. Initialize Git

Open the Claude Code sidebar and say:

> Initialize a git repo here and create a .gitignore for an Obsidian vault.

Claude Code will run `git init` and create a `.gitignore` that excludes Obsidian's workspace files and other things that shouldn't be tracked.

Then make the first commit:

> Commit everything with the message "Initial commit"

## 8. Create a GitHub Repository

Ask Claude Code:

> Create a private GitHub repo for this project and push to it.

Tell Claude whether you want the repo **private** (only you and people you invite can see it) or **public** (visible to everyone). Claude Code will use the `gh` CLI to create the repo and push.

> [!tip]
> If Claude Code says it can't find `gh`, install the GitHub CLI first. Mac: `brew install gh`. Windows: download from [cli.github.com](https://cli.github.com/).

## 9. Verify Everything Works

Test the full loop:

1. Create or edit a note in the vault
2. Ask Claude Code: "Commit and push my changes"
3. Visit your repository on github.com to confirm the files are there

You now have a working project vault with version control and an AI assistant that understands your project.

## What's Next

- **Add structure as you need it.** Don't over-organize upfront. Start with a flat folder of notes and add subfolders when a category has enough pages to justify one.
- **Evolve CLAUDE.md as you go.** As your project develops conventions, add them so Claude stays current.
- **Invite collaborators** on GitHub if others will work in the vault. They clone the repo, open it in Obsidian, and they're in.
