# Canvas

Canvas is a core plugin that gives you a spatial note-taking surface -- an infinite 2D space where you can arrange notes, images, links, and text cards. Think of it as a whiteboard inside Obsidian.

## How to use it

- Open the Command Palette and run **Canvas: Create new canvas**
- Drag existing notes from the file explorer onto the canvas
- Double-click empty space to create a new card (text, note, or web link)
- Connect cards with arrows by dragging from a card's edge

## When it's useful

- **Planning:** lay out agenda items spatially and connect related topics
- **Brainstorming:** free-form exploration before committing to a linear structure
- **Relationship mapping:** visualize how people, projects, and ideas connect

Canvas files (`.canvas`) are stored in the vault like any other file. They're JSON under the hood, so Git can track changes, but they don't render as HTML on a published wiki.

## Canvas vs. Excalidraw

| | Canvas (core) | Excalidraw (community) |
|---|---|---|
| **Focus** | Arranging existing notes spatially | Drawing and diagramming |
| **Cards** | Notes, text, web links | Shapes, text, images, embedded notes |
| **Drawing** | No freehand drawing | Full drawing tools |
| **Style** | Clean, structured | Hand-drawn by default (switchable) |
| **Best for** | Organizing notes | Creating visuals |

They complement each other. Canvas is for spatial note organization; Excalidraw is for creating visual content. See [Excalidraw](Excalidraw.md) for more.

## See also

- [Backlinks and Graph View](Backlinks%20and%20Graph%20View.md) -- automatic visualization of connections based on links
- [Excalidraw](Excalidraw.md) -- freehand drawing and diagramming
