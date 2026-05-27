# System Requirements

Here's what you need before starting the setup process.

## Your Computer

**Mac** — macOS 10.15 (Catalina) or later. Most Macs from 2015 onward will work fine.

**Windows** — Windows 10 or later. You'll use Git Bash (included with Git for Windows) as your terminal.

> [!tip]
> Linux works too, but this guide focuses on Mac and Windows since those are what most people use.

## Accounts You'll Create

- **Claude Pro** — $20/month at [claude.ai](https://claude.ai/). This gives you access to Claude's chatbot and Claude Code.
- **GitHub** — Free at [github.com](https://github.com/). This is where your files get backed up and shared.

You don't need an Obsidian account. Obsidian the app is free and works without signing up for anything.

## Software You'll Install

All free:

- **Obsidian** — from [obsidian.md](https://obsidian.md/)
- **Git** — Mac gets this through Xcode Command Line Tools; Windows gets it through Git for Windows
- **Claude Code** — from [claude.ai/code](https://claude.ai/code)
- **Node.js** — required by Claude Code, from [nodejs.org](https://nodejs.org/) (Mac via Homebrew or direct download; Windows via direct download)

## Internet Connection

You need internet access for the initial setup (downloading tools, creating accounts, authenticating). After that, you can work offline — your files are on your computer. You only need internet when you want to sync with GitHub.

## Time

Budget 30-60 minutes for the full setup. Mac users should allow extra time — the Xcode Command Line Tools download can take 10-15 minutes on its own.

## Important: Cloud Sync Folders

Your vault folders must **not** be inside iCloud, OneDrive, Dropbox, or any other cloud-synced folder. We use Git to sync with GitHub, and having two sync systems on the same folder causes conflicts and data loss.

Good locations for your vaults:

- **Mac:** `~/Obsidian-GitHub/` or `~/Vaults/` (directly in your home folder)
- **Windows:** `C:\Users\YourName\Obsidian-GitHub\` or `C:\Users\YourName\Vaults\`
