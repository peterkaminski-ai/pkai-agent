# Why This Stack

You're about to set up three tools that work together as an integrated system for knowledge work. Here's what each one does and why they fit together.

## Obsidian — Where You Read and Write

Obsidian is a free note-taking app that stores everything as plain text files (Markdown) in a folder on your computer. Unlike Google Docs or Notion, your files aren't locked in someone else's cloud — they're just files on your hard drive, and you can open them with any text editor.

Obsidian organizes files into "vaults." A vault is just a folder. Inside it, you create pages, link them together, and build up a personal wiki or knowledge base.

## Git and GitHub — How You Save and Share

Git is a version-control tool used by software teams worldwide. It keeps a complete history of every change you make — like an infinite undo button that remembers every version of every file.

GitHub is a website that stores a copy of your files in the cloud. When you "push" your work to GitHub, it's backed up and visible to anyone you're collaborating with. When you "pull," you download their latest changes.

The key idea: Git gives you full history and the ability to work offline. GitHub gives you backup and collaboration. Together, they replace the auto-save-to-cloud model (like Google Docs) with something more deliberate — you decide when to save and sync.

## Claude Code — Your AI Assistant

Claude Code is an AI tool made by Anthropic. It runs in a terminal (a text-based interface) and can read and write files on your computer. When you connect it to Obsidian, it sits in a sidebar panel where you can talk to it while you work.

What makes Claude Code special for this workflow:

- **It handles Git for you.** You say "pull the latest changes" or "commit and push my work" in plain English. No commands to memorize.
- **It understands your files.** Claude Code can read the pages in your vault, help you write, reorganize, summarize, or create new content.
- **It works locally.** Your files stay on your computer. Claude Code reads them directly — nothing gets uploaded unless you tell it to push to GitHub.

## How They Fit Together

```
You write in Obsidian
        ↓
Claude Code helps you manage files and sync
        ↓
Git tracks every change (locally)
        ↓
GitHub stores your backup in the cloud
```

The daily rhythm is simple:

1. Open your vault in Obsidian
2. Ask Claude Code to "pull the latest" (grab any new changes from GitHub)
3. Do your work — write, edit, organize
4. Ask Claude Code to "commit and push" (save and upload)

You never need to touch Git directly. Claude Code translates your plain-English requests into the right commands.

## Why Not Just Use Google Docs?

Google Docs is great for many things. This stack is better when you want:

- **Full version history** of every file, forever
- **Offline access** — everything is on your computer
- **Plain text files** you truly own and can move anywhere
- **An AI assistant** that can read and work with all your files at once
- **Collaboration** without giving up control of your data
