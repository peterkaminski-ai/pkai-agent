# Troubleshooting

Common problems and how to fix them. If you don't see your issue here, describe it to Claude Code — it can often diagnose and fix problems for you.

## Installation Issues

### The Xcode tools dialogue disappeared (Mac)

It's probably behind another window. Check all your displays and use Cmd+Tab to look for a "Software Update" or "Install" window.

### The Xcode download time estimate is absurd (Mac)

Ignore the initial estimate — it may say 16 hours. The actual download typically takes 10-15 minutes. The progress bar may restart about two-thirds of the way through. This is normal.

### Claude Code says it can't find Git

**Mac:** Make sure the Xcode Command Line Tools have finished installing. Open Terminal and run `git --version` to check.

**Windows:** Install Git for Windows from [git-scm.com](https://git-scm.com/). This includes Git Bash, which Claude Code needs.

### Windows: "bash is not recognized as an internal or external command"

Git for Windows is not installed, or you're using Command Prompt instead of Git Bash. Install Git for Windows from [git-scm.com](https://git-scm.com/) and use **Git Bash** for all terminal commands.

### Node.js installation didn't seem to work

Open a new terminal window (close and reopen Terminal or Git Bash) and try `node --version`. If it still doesn't work, download and install again from [nodejs.org](https://nodejs.org/).

## GitHub Issues

### I get a 404 when visiting a GitHub repository

This usually means one of three things:
1. You haven't created a GitHub account yet
2. You aren't logged in to GitHub
3. The repository is private and you haven't been given access

If someone shared a repo link with you and you're getting a 404, make sure you're logged in and check your GitHub notifications for an invitation. GitHub shows a misleading 404 instead of telling you to log in or accept an invite.

### Git asks for my password and rejects it

GitHub no longer accepts regular passwords for Git operations. You need either:
- The GitHub CLI (`gh auth login`) — see [GitHub Account Setup](GitHub%20Account%20Setup.md)
- A personal access token — see [GitHub Account Setup](GitHub%20Account%20Setup.md), Option B

## Obsidian Issues

### BRAT is installed but I can't find the smiley-face icon

Make sure BRAT is **enabled**, not just installed. Go to Settings, then Community plugins, and check that the toggle next to BRAT is on.

### The Claude sidebar shows an error on first open

Close the panel and reopen it. If the problem persists, try restarting Obsidian entirely (quit and relaunch).

### My settings didn't carry over from another vault

This is expected — Obsidian settings are per-vault. You need to configure each vault separately. See [Configuring Obsidian](Configuring%20Obsidian.md) for the recommended settings.

### Windows: "pip install pywinpty" error in the Claude sidebar

Run `pip install pywinpty` in Command Prompt (not Git Bash), then restart Obsidian. If `pip` isn't recognized, install Python first from [python.org](https://python.org/).

## Git and Sync Issues

### "Merge conflict" when pushing

This happens when two people edited the same part of the same file. Describe the situation to Claude Code and it can help you resolve it. This is rare in solo work.

### "Push rejected"

Someone else pushed changes while you were working. Pull first, then push:

> Pull the latest, then push my changes

Or use the habit of saying "pull and push" together to avoid this.

### "Nothing to commit"

You haven't made any changes since your last commit. This is fine — not an error.

### Files I don't want are being tracked by Git

Ask Claude Code to update your `.gitignore` file:

> Add [filename or pattern] to .gitignore

Common things to exclude: `.DS_Store` (Mac), `Thumbs.db` (Windows), and any files with passwords or API keys.

## General Tips

- **When in doubt, describe the problem to Claude Code.** It can read error messages and usually knows what to do.
- **Restart and retry.** Many first-launch issues resolve by closing and reopening the application.
- **Git rarely loses anything.** Even if things look wrong, your history is intact. Ask Claude Code to help you recover.
