# Your First Vault

A vault is just a folder that Obsidian knows about. Inside it, you create Markdown files (pages), organize them in subfolders, and link them together. This page walks you through creating a vault and optionally connecting it to GitHub.

## Step 1: Create a Folder

Create a new folder on your computer for your vault. Remember: this folder must **not** be inside iCloud, OneDrive, Dropbox, or any cloud-synced folder.

Good locations:

- **Mac:** `~/Obsidian-GitHub/my-vault/`
- **Windows:** `C:\Users\YourName\Obsidian-GitHub\my-vault\`

Name it whatever makes sense for your project.

## Step 2: Open It in Obsidian

1. Open Obsidian
2. Click the vault name in the bottom-left corner (or go to **File > Open vault**)
3. Choose **Open folder as vault**
4. Navigate to the folder you just created and select it

Obsidian will create a `.obsidian/` directory inside the folder. That's all a vault is — a folder with `.obsidian/` in it.

## Step 3: Configure Settings

With the new vault open, apply the recommended settings from [Configuring Obsidian](Configuring%20Obsidian.md):

- **Editor** — Turn on "Show line number"
- **Files and Links** — Turn on "Detect all file extensions." Set "Default location for new notes" to "Same folder as current file"
- **Appearance** — Turn off "Inline title"

## Step 4: Install the Claude Code Sidebar

Follow the steps from [Connecting Claude Code to Obsidian](Connecting%20Claude%20Code%20to%20Obsidian.md):

1. Enable community plugins
2. Install and enable BRAT
3. Use BRAT to install the Claude Sidebar plugin
4. Open the sidebar with the robot icon

## Step 5: Connect to GitHub (Optional but Recommended)

If you want your vault backed up and shareable, connect it to a GitHub repository. Open the Claude Code sidebar and ask it:

> Initialize a git repo here and create a .gitignore for an Obsidian vault.

Claude Code will run `git init` and create a `.gitignore` file that excludes Obsidian's workspace files and other things that shouldn't be tracked.

Then ask Claude Code to make a first commit:

> Commit everything with the message "Initial commit"

To create a GitHub repository and upload your vault:

> Create a private GitHub repo for this project and push to it.

Claude Code will use the `gh` CLI to create the repository and push your files. Tell it whether you want the repo **private** (only you can see it) or **public** (visible to everyone).

> [!tip]
> If Claude Code says it can't find `gh`, you may need to install the GitHub CLI first. On Mac: `brew install gh`. On Windows: download from [cli.github.com](https://cli.github.com/).

## Step 6: Create a CLAUDE.md

CLAUDE.md is a special file that tells Claude Code about your vault — what it's for, how it's organized, and what conventions to follow. Without it, Claude has no context about your project.

Ask Claude Code:

> Create a CLAUDE.md for this project. It's about [describe your project briefly].

Or write one yourself:

```markdown
# CLAUDE.md

This vault is [what it is]. It's for [what you use it for].

## Structure

- [describe your folder layout, if any]

## Conventions

- [any rules you want Claude to follow]
```

Even a few lines make a big difference in how well Claude Code understands your vault.

## Step 7: Verify Everything Works

Test the full loop:

1. Create a new note in Obsidian (Cmd+N on Mac, Ctrl+N on Windows)
2. Write something — even just "Hello, world!"
3. In the Claude Code sidebar, say: "Commit and push my changes"
4. Claude Code should commit the file and push it to GitHub

If that works, you have a fully functional vault with version control and AI assistance.

## What's Next

- **Start writing.** Don't over-organize upfront. Start with a flat folder of notes and add subfolders when you have enough related pages to justify them.
- **Evolve your CLAUDE.md as you go.** As your project develops conventions, add them so Claude stays current.
- **Invite collaborators** on GitHub if others will work in the vault. They clone the repo, open it in Obsidian, and they're in.
