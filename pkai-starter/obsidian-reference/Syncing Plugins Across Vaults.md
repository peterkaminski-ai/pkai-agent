# Syncing Plugins Across Vaults

Obsidian stores plugins inside each vault's `.obsidian/plugins/` folder. Install a plugin in one vault and it only exists there -- which gets tedious fast when you're running multiple vaults.

Here's how to keep them in sync.

## Option 1: Symlink the plugins folder (recommended)

Create a symbolic link so both vaults share the same plugins directory:

```bash
# 1. Pick one vault as your "source" (the one with plugins already set up)

# 2. In your NEW vault, remove or rename the plugins folder
cd /path/to/new-vault/.obsidian
mv plugins plugins-backup   # keep a backup just in case

# 3. Create a symlink to your source vault's plugins
ln -s /path/to/source-vault/.obsidian/plugins plugins
```

Now both vaults use the same plugins. Install once, available everywhere.

**Caveat:** Plugin *settings* are also shared via this method. If you need different settings per vault (e.g., different template folders), this approach won't work for those plugins.

## Option 2: Community plugin (Plugin Sync)

There's a community plugin called "Plugin Sync" that handles syncing plugins across vaults. Search for it in **Settings > Community Plugins > Browse**.

## Option 3: Manual copy

Copy the `.obsidian/plugins/` folder from one vault to another when needed. Low-tech but works.

## What's per-vault

Everything in `.obsidian/` is per-vault:

| Per-vault | Shared across vaults |
|-----------|---------------------|
| Plugins and plugin settings | Nothing (by default) |
| Theme and appearance | |
| Hotkeys | |
| Core plugin configuration | |

This is why syncing matters if you use multiple vaults. See [Working with Multiple Vaults](Working%20with%20Multiple%20Vaults.md) for more on multi-vault setups.
