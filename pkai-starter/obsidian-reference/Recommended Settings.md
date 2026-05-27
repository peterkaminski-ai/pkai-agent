# Recommended Settings

A good baseline configuration for Obsidian. These are opinionated defaults -- adjust to taste, but they're a solid starting point.

## Editor

| Setting | Value | Why |
|---------|-------|-----|
| **Show line number** | On | Makes it easier to reference specific lines, especially when working with Claude Code or reviewing diffs |

Find it: **Settings > Editor > Show line number**

## Files and Links

| Setting | Value | Why |
|---------|-------|-----|
| **Detect all file extensions** | On | Lets you see non-Markdown files (images, PDFs, JSON, etc.) in the file explorer. Without this, you're flying blind about what's actually in your vault |
| **Default location for new notes** | Same folder as current file | Keeps new notes near related content instead of dumping everything in the vault root |

Find it: **Settings > Files and Links**

## Appearance

| Setting | Value | Why |
|---------|-------|-----|
| **Inline title** | Off | The inline title duplicates the `# Heading` at the top of the note. Turning it off avoids the visual redundancy |

Find it: **Settings > Appearance > Inline title**

## Community Plugins

Enable community plugins so you can install BRAT, which you'll need for the Claude Sidebar Plugin and other beta plugins.

Find it: **Settings > Community plugins > Turn on community plugins**

## After changing settings

These settings are stored per-vault in `.obsidian/app.json` and `.obsidian/appearance.json`. If you create a new vault, you'll need to set them again -- or use symlinks to share the configuration. See [Syncing Plugins Across Vaults](Syncing%20Plugins%20Across%20Vaults.md) for details.

## See also

- [Installing Community Plugins](Installing%20Community%20Plugins.md) -- next step after enabling community plugins
- [Claude Sidebar Plugin](Claude%20Sidebar%20Plugin.md) -- the plugin that puts Claude Code in your sidebar
