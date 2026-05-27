# Connecting Claude Code to Obsidian

You can run Claude Code inside Obsidian's right sidebar, so you can talk to your AI assistant while looking at your notes. This uses a community plugin called the Claude Sidebar, installed through another plugin called BRAT.

## Prerequisites

- Obsidian installed and open
- Claude Code installed and has been run at least once (so it's authenticated)

## Step 1: Enable Community Plugins

1. Open Obsidian and make sure you're in the vault you want to set up
2. Go to **Settings** (gear icon in the lower left)
3. Go to **Community plugins**
4. If community plugins aren't enabled yet, click **Turn on community plugins**

## Step 2: Install BRAT

BRAT is a plugin that lets you install other plugins that haven't been published to the official Obsidian plugin directory yet.

1. In Settings, go to **Community plugins** and click **Browse**
2. Search for **BRAT**
3. Click **Install**, then **Enable**
4. Close the settings

You should now see a small smiley-face icon in the left sidebar — that's the BRAT icon.

> [!tip]
> If you don't see the smiley-face icon, make sure BRAT is enabled (not just installed). Go back to Settings, then Community plugins, and check that the toggle next to BRAT is on.

## Step 3: Install the Claude Sidebar Plugin

1. Click the **smiley-face icon** (BRAT) in the left sidebar
2. Click **"Add Beta plugin with frozen version"** (the top option)
3. In the Repository field, paste:

```
derek-larson14/obsidian-claude-sidebar
```

4. Click the version dropdown and select **Latest**
5. Click **Install**

## Step 4: Open the Claude Code Sidebar

You should now see a small robot icon in the right sidebar area. Click it to open Claude Code inside Obsidian.

> [!warning]
> If you see an error when opening the sidebar, close the panel (right-click the robot icon and close it), then try opening it again. This occasionally happens and usually resolves on the second attempt. If it persists, try restarting Obsidian.

## What You're Looking At

The Claude Code sidebar is actually a terminal emulator with Claude Code running inside it. You interact with it by typing plain-English requests, just like you would in a terminal. It's the same Claude Code you ran during installation — now embedded in Obsidian for convenience.

## You'll Need to Do This for Each Vault

Just like Obsidian settings, plugins are per-vault. If you create a new vault later, you'll need to install BRAT and the Claude Sidebar again for that vault. It only takes a minute once you've done it before.

## Next Step

Move on to [Basic Markdown](Basic%20Markdown.md) to learn the writing basics, or jump to [Your First Vault](Your%20First%20Vault.md) if you're ready to start working.
