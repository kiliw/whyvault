---
type: system
---

# Tool notes

Tool-specific quirks. These explicitly do **not** belong in the [[MANUAL]] – that describes the system, not the programs. This file is the dumping ground for everything that only applies in your setup, and it's allowed to be incomplete.

## Obsidian

- Non-Markdown files aren't shown as long as "Detect all file extensions" is off. That's why a room may also contain scripts or a repository without getting in the way.
- When you move a note, Obsidian brings the links along. That's exactly what the rule "moving it is the approval" is built on.

## Canvases

- **Excalidraw (plugin):** a drawing sits next to the note as `<Name>.excalidraw.md` and is embedded in the text with `![[<Name>.excalidraw]]`. The area below `# Excalidraw Data` is fragile – don't let lint or formatting plugins touch it.
- **Mermaid import** (Excalidraw and Miro use the same library): **breaks on subgraphs.** A diagram with frames turns into a single image. Build canvases like that by hand.
- A shared canvas for several people (Miro, FigJam) beats a local drawing whenever several people genuinely work on it. The rule then: the canvas is for working, the text in the note stays the source.

## Worth it later

- **Dataview** – replaces hand-maintained maps with queries. The frontmatter keys in this template are built with that in mind.
- **Templater** – fills in date and title in the templates automatically.
