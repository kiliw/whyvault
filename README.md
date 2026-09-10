# Second Brain – Template

An Obsidian vault that answers one question consistently: **why is this the way it is?** Tasks, dates and progress stay in your task tool.

It grew out of a working vault and was stripped down here to the bare structure – no examples from any particular job or area of life.

## Why

For people carrying several things at once: a job, their own products, a family. The bottleneck isn't the work, it's getting back in. Returning to something after two weeks and knowing within five minutes why it was decided that way.

The vault is the hub you work out of, and at the same time the context an AI needs to produce something usable instead of something generic: the brand, the voice, the boundaries, the last decisions. Part of the work – posts, condensations, meeting extracts – can be handed off that way.

**Agent-agnostic:** everything an assistant needs to know about you sits in the vault as a text file, not in some vendor's settings. Claude, ChatGPT, a local model: you hand it `MANUAL.md` and the four identity files, and it works by the same rules. The vault is yours, the model is replaceable.

## Quick start

1. **Get the repository** – "Use this template", `git clone`, or download the ZIP.
2. In Obsidian: **Open folder as vault** and pick this folder. The folder *is* the vault, there is nothing to copy.
3. Open **`Start here.md`** and read **[[MANUAL]]** once, all the way through – it's one page.
4. **Create your identity:** copy `9_System/Setup/Interview prompt.md` into your AI assistant and let it interview you. The result is `USER.md`, `SOUL.md` and `IDENTITY.md`. If you already have chat memories, use `From memories prompt.md` instead.
5. **Name your context:** rename `3_Rooms/your-context-here/` and fill in `CONTEXTS.md`. One is enough.
6. **Create a first room** – with exactly one file, the overview.

## The five rules

1. **The vault answers "why", the task tool answers "what's next".** No tasks, no deadlines, no progress states. Otherwise you have two truths and you'll maintain the worse one.
2. **Room or collection?** Does the thing have a history – are decisions made, is there a timeline → **room**. Is it a body of material you maintain → **collection** in `1_Knowledge` with a map as its entrance.
3. **The boundary rule.** Link freely inside a room, outward only to `1_Knowledge`, never room to room. That's what makes a room handoverable as a folder – and it's also the test for whether something is project-specific or general.
4. **The skeleton isn't paid for up front.** A new room has exactly one file. `01 Decisions/`, `02 Meetings/` and the rest appear when needed. The names are fixed, the completeness isn't – an empty decisions folder claims that nothing has been decided.
5. **Knowledge belongs to no room. It may have a context.** That's why context is a folder level only under `3_Rooms`: a person can show up in several worlds and still exist only once.

## Structure

```
MANUAL.md                     the rules, at the root and shareable on its own
Start here.md                 the way in, inside Obsidian
0_Inbox/                      everything unsorted, gets emptied
1_Knowledge/                  timeless, flat, shared
  People/  Organisations/  Software/  Notes/  Sources/  Maps/  Principles/
2_Calendar/                   dated, thin
  Days/  Reviews/
3_Rooms/                      everything bounded, the only context level
  your-context-here/          placeholder, one per context with _Closed/
8_Attachments/                context-free files
9_System/
  Tool notes.md               tool-specific quirks, deliberately kept separate
  Identity/                   USER · SOUL · IDENTITY · CONTEXTS
  Setup/                      interview and memories prompt
  Templates/                  13 templates
```

Room skeleton: `00 Overview – <Room>.md`, then as needed `01 Decisions/`, `02 Meetings/`, `03 Knowledge/`, `08 Attachments/`, `Documents.md`, `04 Sub-projects/`, `99 Handover – <Room>.md`.

## The four identity files

| File | Answers |
|---|---|
| `USER.md` | Who I am and how I work |
| `SOUL.md` | How it should sound when something is written for me |
| `IDENTITY.md` | Who the assistant should be to me – mandate, boundaries, default behaviour |
| `CONTEXTS.md` | Which worlds I move in (these are the folders under `3_Rooms`) |

You don't write them by hand – you generate them from an interview or from existing memories. See `9_System/Setup/`.

## What's deliberately missing

No plugins, no automation, no example rooms, no pre-filled contexts. **Structure has to be earned:** use it first, refine it later. Dataview and Templater pay off once the skeleton has carried you for four weeks – the frontmatter keys are built with that in mind.

## If you run a vault in another language alongside this one

Folder and file names here are English. If you keep a second vault in German, this is the mapping that keeps the two comparable:

| English | German |
|---|---|
| `0_Inbox` | `0_Eingang` |
| `1_Knowledge` | `1_Wissen` |
| `People / Organisations / Software / Notes / Sources / Maps / Principles` | `Personen / Organisationen / Software / Notizen / Quellen / Karten / Leitlinien` |
| `2_Calendar` · `Days` · `Reviews` | `2_Kalender` · `Tage` · `Rückblicke` |
| `3_Rooms` · `_Closed` | `3_Räume` · `_Abgeschlossen` |
| `8_Attachments` | `8_Anhänge` |
| `9_System` · `MANUAL` · `Identity` · `Templates` | `9_System` · `Anleitung` · `Identität` · `Vorlagen` |
| `00 Overview` · `01 Decisions` · `02 Meetings` · `03 Knowledge` · `08 Attachments` · `99 Handover` | `00 Übersicht` · `01 Entscheidungen` · `02 Meetings` · `03 Wissen` · `08 Anhänge` · `99 Übergabe` |

The frontmatter keys stay English either way (`type`, `context`, `updated`) – that's the seam along which two vaults can be pulled together later.

## License

MIT, copyright (c) 2026 Kilian Wimmer – see `LICENSE`.
