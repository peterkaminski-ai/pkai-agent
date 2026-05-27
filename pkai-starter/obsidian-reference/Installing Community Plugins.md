# Installing Community Plugins

Community plugins extend Obsidian beyond its built-in features. There are hundreds available, covering everything from mind mapping to AI integration to Git-based version control.

## Enabling community plugins

Community plugins are disabled by default. To turn them on:

1. Go to **Settings > Community plugins**
2. Click **Turn on community plugins**
3. Acknowledge the security notice

This only needs to be done once per vault.

## Installing from the directory

1. Go to **Settings > Community plugins > Browse**
2. Search for the plugin by name
3. Click **Install**, then **Enable**

The plugin is now active. Its settings (if any) appear under **Settings > Community plugins** -- click the gear icon next to the plugin name.

## Installing beta plugins with BRAT

Some plugins aren't published in the community directory yet. BRAT (Beta Reviewers Auto-update Tester) lets you install them directly from GitHub.

### Installing BRAT itself

1. Go to **Settings > Community plugins > Browse**
2. Search for **BRAT**
3. Click **Install**, then **Enable**

### Using BRAT to install a beta plugin

1. Go to **Settings > Community plugins > BRAT** (click the gear icon)
2. Click **Add Beta Plugin** (or **Add Beta plugin with frozen version** if you want a specific release)
3. Paste the GitHub repository path (e.g., `derek-larson14/obsidian-claude-sidebar`)
4. BRAT installs the plugin and keeps it updated

BRAT is how you install the [Claude Sidebar Plugin](Claude%20Sidebar%20Plugin.md), which isn't in the community directory yet.

## Where plugins live on disk

Plugins are stored in `.obsidian/plugins/` inside each vault. Each plugin gets its own subfolder containing:

| File | Purpose |
|------|---------|
| `manifest.json` | Plugin metadata -- name, version, author |
| `main.js` | The plugin's compiled JavaScript code |
| `styles.css` | Optional CSS for the plugin's UI |
| `data.json` | The plugin's saved settings (created after first use) |

Since plugins are per-vault, installing in one vault doesn't affect another. See [Syncing Plugins Across Vaults](Syncing%20Plugins%20Across%20Vaults.md) for workarounds.

## See also

- [Essential Community Plugins](Essential%20Community%20Plugins.md) -- which plugins are worth installing
- [Claude Sidebar Plugin](Claude%20Sidebar%20Plugin.md) -- the key beta plugin installed via BRAT
- [Syncing Plugins Across Vaults](Syncing%20Plugins%20Across%20Vaults.md) -- keeping plugins consistent across vaults
