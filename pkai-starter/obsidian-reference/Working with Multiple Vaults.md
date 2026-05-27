# Working with Multiple Vaults

You started with one vault. Soon you'll want a second one: a personal vault for your own notes, or a project vault for something you're building. This guide covers why, how, and how to link them together.

## Why not just put everything in one vault?

You could. Many people do. But there are practical reasons to separate.

**Each vault gets its own CLAUDE.md.** That file is the agent's entire context: it tells Claude what this space is about, what conventions to follow, and what matters here. When everything lives in one vault, CLAUDE.md has to describe your entire life and Claude gets lost in the noise. With separate vaults, each agent is a specialist:

- Your **personal vault** agent knows your projects, your preferences, your private notes
- Your **team vault** agent knows the team's workflow, who's doing what, and what's pending
- Your **project vault** agent knows just that project's domain and conventions

The CLAUDE.md stays lean. The agent stays sharp. This is the single biggest practical argument for multiple vaults.

**Other reasons:**

- **Privacy boundaries.** What you share with a team doesn't need to sit next to your private journal. Separate vaults mean separate repos, separate sync, separate access control.
- **Separation of concerns.** Different vaults can follow different conventions -- folder structure, naming, commit protocol.
- **Lighter vaults load faster.** As vaults grow into thousands of notes, search and graph view slow down. Smaller, focused vaults stay snappy.

## Creating a second vault

1. Open Obsidian
2. Click the vault icon in the bottom-left corner (or use **Open another vault** from the Command Palette)
3. Choose **Create new vault**
4. Pick a name and location on your filesystem
5. Done. You now have a second vault with its own `.obsidian/` settings folder.

Write a CLAUDE.md in the new vault root immediately. Even a few lines ("This is my personal knowledge base. I use it for X, Y, Z.") will make Claude Code dramatically more useful.

## Switching between vaults

The **vault switcher** (vault icon, bottom-left corner) shows all your vaults. Click one to switch. Obsidian opens it in the same window.

You can also have multiple vaults open simultaneously in separate windows: use **Open another vault** and choose **Open** instead of switching.

## Linking between vaults

Obsidian has a URI scheme for cross-vault links:

```
obsidian://open?vault=VaultName&file=Note%20Name
```

- `vault` is the vault name (as it appears in the vault switcher)
- `file` is the note name only: no path, no `.md` extension
- Spaces become `%20`

**Example:**

```markdown
[Project Notes](obsidian://open?vault=my-project&file=Project%20Overview)
```

Clicking that link opens the note in the other vault. It works across any vaults on your machine.

**Note:** Cross-vault links are regular markdown links, not `[[wiki-links]]`. Wiki-links only work within a single vault.

## What's per-vault (and what isn't)

Everything in `.obsidian/` is per-vault:

| Per-vault | Shared across vaults |
|-----------|---------------------|
| Plugins and plugin settings | Nothing (by default) |
| Theme and appearance | |
| Hotkeys | |
| Core plugin configuration | |
| CLAUDE.md | |

This means installing a plugin in one vault doesn't affect another. See [Syncing Plugins Across Vaults](Syncing%20Plugins%20Across%20Vaults.md) for workarounds.

## A practical example

Say you're working on a personal project alongside a team wiki:

| Vault | Purpose | CLAUDE.md focus |
|-------|---------|----------------|
| `team-wiki` | Shared knowledge base | Wiki conventions, collaboration rules |
| `my-knowledge-base` | Personal notes | Your projects, preferences, private reflections |

Your personal vault links to the team vault when referencing shared content. The team vault doesn't need to know your personal vault exists. Each CLAUDE.md describes only its own world.

As you grow, you might add more: a client vault, a research vault, a course vault. The pattern scales because each vault is self-contained.

## See also

- [Syncing Plugins Across Vaults](Syncing%20Plugins%20Across%20Vaults.md) -- keeping plugins consistent
- [Recommended Settings](Recommended%20Settings.md) -- baseline setup for each new vault
- [Obsidian and Git](Obsidian%20and%20Git.md) -- version control for your vaults
