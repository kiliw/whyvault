---
type: system
---

# Tool notes

Werkzeugspezifische Eigenheiten. Gehören ausdrücklich **nicht** in das [[MANUAL]] – die beschreibt das System, nicht die Programme. Diese Datei ist die Halde für alles, was nur in deiner Umgebung gilt, und darf ruhig unvollständig sein.

## Obsidian

- Nicht-Markdown-Dateien werden nicht angezeigt, solange „Detect all file extensions" aus ist. Deshalb darf ein Room auch Skripte oder ein Repository enthalten, ohne dass es stört.
- Beim Verschieben einer Notiz zieht Obsidian die Links mit. Genau darauf baut die Regel „Das Verschieben ist die Verabschiedung“.

## Zeichenflächen

- **Excalidraw (Plugin):** eine Zeichnung liegt als `<Name>.excalidraw.md` neben der Notiz und wird mit `![[<Name>.excalidraw]]` im Text eingebettet. Der Bereich unterhalb von `# Excalidraw Data` ist empfindlich – nicht von Lint- oder Formatier-Plugins anfassen lassen.
- **Mermaid-Import** (Excalidraw und Miro nutzen dieselbe Bibliothek): **scheitert an Subgraphs.** Aus einem Diagramm mit Rahmen wird ein einzelnes Bild. Solche Flächen von Hand bauen.
- Eine gemeinsame Fläche für mehrere Personen (Miro, FigJam) schlägt eine lokale Zeichnung immer dann, wenn wirklich mehrere daran arbeiten. Dann gilt: die Fläche ist zum Arbeiten, der Text in der Notiz bleibt die Quelle.

## Später sinnvoll

- **Dataview** – ersetzt handgepflegte Karten durch Abfragen. Die Frontmatter-Schlüssel in diesem Template sind darauf ausgelegt.
- **Templater** – setzt Datum und Titel in den Vorlagen automatisch.
