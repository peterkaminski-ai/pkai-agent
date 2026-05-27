# Backlinks and Graph View

Two core plugins for discovering how your notes connect to each other. Backlinks show you the textual connections; Graph View shows them visually.

## Backlinks

The Backlinks panel shows which notes link to the current note. It surfaces two types of connections:

- **Linked mentions** -- notes that link to the current note with a `[[wiki-link]]`
- **Unlinked mentions** -- notes that mention the current note's name as plain text (not yet linked)

### How to open it

- Click the chain-link icon in the right sidebar
- Or use the Command Palette > **Backlinks: Show backlinks**

### Why it matters

Backlinks are how you discover connections you didn't know existed. If someone (or you, three months ago) mentioned a topic in a different note, the backlinks panel surfaces it. This is what makes wiki-style linking more powerful than folders alone -- every link is bidirectional, even if you only wrote it in one direction.

**Tip:** Unlinked mentions are especially useful. Obsidian finds every place a note's name appears as plain text. Click the link button next to an unlinked mention to convert it to a proper `[[wiki-link]]`.

## Graph View

Graph View visualizes all the notes in the vault and their connections as an interactive node-and-edge graph.

### Two modes

- **Full graph:** Command Palette > **Graph view: Open graph view** -- shows the entire vault. Can be overwhelming in large vaults, but useful for seeing clusters and orphans.
- **Local graph:** Command Palette > **Graph view: Open local graph** -- shows only the connections for the current note. This is usually what you want.

### Filtering

You can filter the graph by tags, folders, or search terms using the controls at the top of the graph view. This is the way to make the full graph useful in a large vault -- narrow it down to what you're interested in.

### When it's useful

- Exploring a new area of the vault: "what is this note connected to?"
- Finding orphan notes (nodes with no connections)
- Getting a sense of the vault's overall structure and clusters

## See also

- [Search](Search.md) -- finding notes by content rather than connections
- [Essential Community Plugins](Essential%20Community%20Plugins.md) -- Strange New Worlds adds inline link counts
