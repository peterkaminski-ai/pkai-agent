# Troubleshooting

Common issues and how to fix them.

## Plugins

### Community plugins option is missing
You need to enable community plugins first: **Settings > Community plugins > Turn on community plugins**. This only needs to be done once per vault.

### Plugin installed but not working
Check that it's both installed AND enabled. Go to **Settings > Community plugins** and make sure the toggle next to the plugin is on.

### BRAT plugin installed but can't find Claude Sidebar
Make sure you're entering the correct repository path in BRAT: `derek-larson14/obsidian-claude-sidebar`. Use **Add Beta plugin with frozen version**, not just "Add Beta Plugin", and select **Latest**.

### Plugins missing in a new vault
Plugins are per-vault. Installing in one vault doesn't affect another. You need to install plugins again in each new vault, or use symlinks to share the plugins folder. See [Syncing Plugins Across Vaults](Syncing%20Plugins%20Across%20Vaults.md).

## Files and Links

### Wiki-links not resolving
`[[wiki-links]]` only work within a single vault. For cross-vault links, use Obsidian's URI scheme: `obsidian://open?vault=VaultName&file=Note%20Name`. See [Working with Multiple Vaults](Working%20with%20Multiple%20Vaults.md).

### Frontmatter not rendering as properties
Frontmatter must be the very first thing in the file. Even a blank line before the opening `---` will break it. Make sure `---` is on line 1.

### New notes appearing in the vault root
Change the default location: **Settings > Files and Links > Default location for new notes** and set it to "Same folder as current file". See [Recommended Settings](Recommended%20Settings.md).

## Git

### Vault is inside iCloud/OneDrive/Dropbox and Git is acting weird
Git and cloud sync don't mix well -- you'll get conflicts and corrupted files. Move the vault to a location outside cloud-synced folders (e.g., `~/Documents/GitHub/` or a dedicated `~/Vaults/` directory).

### workspace.json keeps showing up in diffs
Add it to `.gitignore`:
```
.obsidian/workspace.json
.obsidian/workspace-mobile.json
```
This file is personal UI state (which tabs you have open) and changes every time you do anything in Obsidian.

### Merge conflicts in .obsidian/ files
These are usually in `workspace.json` (add to `.gitignore`) or plugin settings. For plugin settings conflicts, accept one version and re-apply any settings that were lost. For `community-plugins.json` conflicts, you can usually accept either version and reinstall any missing plugins.

## Claude Code

### Claude Code not working in the sidebar
Make sure Claude Code is installed and works in a regular terminal first. The sidebar plugin is just a terminal emulator -- if Claude Code doesn't work in Terminal/iTerm2, it won't work in the sidebar either.

### Claude Code doesn't know about my vault
Create a `CLAUDE.md` file in your vault root describing what the vault is about, its structure, and any conventions. Without this file, Claude has no context about your vault. See [Connecting Claude Code to Obsidian](Connecting%20Claude%20Code%20to%20Obsidian.md).

## Performance

### Vault is slow to open or search
Large vaults (thousands of notes) can slow down. Options:
- Split into multiple vaults (see [Working with Multiple Vaults](Working%20with%20Multiple%20Vaults.md))
- Disable plugins you're not using
- Disable Graph View's automatic rendering if it's not needed

### Bases not showing in a note
Bases require Obsidian 1.8+. Check your Obsidian version in **Settings > About**. Also, Bases are an Obsidian-only feature -- they won't render if you're viewing notes as static HTML on a published wiki.

## See also

- [Recommended Settings](Recommended%20Settings.md) -- correct configuration prevents many issues
- [Resources](Resources.md) -- official docs and community forums for further help
