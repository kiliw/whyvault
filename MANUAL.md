---
type: system
---

# Manual – the system on one page

*The rules. Deliberately kept at the root so it can be handed on by itself.*

## What this is for

For people carrying several things at once: a job, their own products, a family. Not one project after another, but five side by side, each with its own people, its own decisions and its own filing.

The bottleneck there isn't the work, it's **getting back in**: returning to something after two weeks and knowing within five minutes why it was decided that way. That's exactly what this vault is the hub for. It's the place the context lives – the context you work out of: a post, a campaign, a decision, a handover.

And because the context is written down and ordered, part of the work can be handed to an AI. Not because the model is clever, but because it gets the right slice: the brand, the voice, the boundaries, the last decisions. Bad context produces generic results, good context produces usable ones.

**Agent-agnostic.** Everything the assistant needs to know about you sits in the vault as a text file, not in some vendor's settings. Claude, ChatGPT, a local model, whatever comes next: you hand it [[MANUAL]] and the four identity files, and it works by the same rules. The vault is yours, the model is replaceable.

## The boundary of the system

**This vault answers "why". Your task tool answers "what's next".**

The test for anything you want to capture:

- Does it have an owner and a due date? → **task tool**
- Does someone need to still understand it in six months? → **here**

So there are no tasks here, no deadlines, no progress states. The moment you start ticking boxes here, you have two truths and you'll maintain the worse one.

## Three kinds of things

| | What | Boundary | On handover |
|---|---|---|---|
| **Rooms** (`3_Rooms`) | anything with its own decisions, its own people and an end | yes – one folder | handed over as a package |
| **Knowledge** (`1_Knowledge`) | people, organisations, software, notes, sources, principles | no – flat and shared | stays with you |
| **Calendar** (`2_Calendar`) | daily notes, reviews | thin, timeline only | irrelevant |

**Knowledge belongs to no room. It may have a context.** That's why only `3_Rooms` has a context level. A person can show up privately and professionally – the note exists exactly once and carries no context. Something that explicitly applies to one context only is still knowledge and gets the `context:` field. The only thing that matters: no knowledge note lives inside a room.

## Room or collection?

The most common mix-up – and the one that produces folders full of empty subfolders. One question decides it:

> **Does the thing have a history?** Do things happen that get decided and that someone has to understand later?

- **Yes** → **room.** There are decisions, conversations, a timeline, and eventually a close.
- **No, it's a body of material you maintain** → **collection in `1_Knowledge`**, with a map in `Maps/` as its entrance. A collection is never handed over – it stays.

Collections need no meetings, no decisions and no handover. Whatever about a collection is actual *work* happens in a room and lands in the collection afterwards.

## The boundary rule

**Inside a room, link freely. Outward, only to `1_Knowledge`. Never room to room.**

Copy a room folder out and only a short, known list of links points nowhere – people, organisations, software. Those you can include. If two rooms need the same thing, it becomes a note in `1_Knowledge`. So the rule is at the same time the test for whether something is project-specific or general.

It holds in both directions: a note in `1_Knowledge` refers to a room in plain text at most, never as a wiki link. **One exception:** [[Rooms]] is the map over the rooms and has to link them – that's navigation, not content.

## Status

The only status is the folder position. A room sits in `<context>/` or in `<context>/_Closed/`. One move when something ends. Nothing else.

What replaces status is the **timeline** in `00 Overview`: one line per event someone has to understand later.

## The skeleton: same names, not same completeness

From day 1 exactly **one** file exists:

```
<Room>/
└── 00 Overview – <Room>.md    purpose, boundaries, people, who decides what,
                               systems, timeline, open questions
```

The overview **is** the handover document for as long as it suffices. Everything else appears when it's needed – and is then called this:

```
01 Decisions/            at the first decision that carries weight
02 Meetings/             at the first conversation someone has to understand later
03 Knowledge/            at the first room-specific document
08 Attachments/          at the first file
Documents.md             once there are more than a handful of documents
04 Sub-projects/<X>/     when a part accumulates its own decisions and meetings
99 Handover – <Room>.md  when there is genuinely something to hand over (see below)
```

**The names are fixed, the completeness isn't.** An empty `01 Decisions/` folder claims that nothing has been decided, and that's almost always wrong. **The skeleton isn't paid for up front.** The exception is the `_Closed/` folder per context: those are empty, and that emptiness is a true statement.

**When the handover splits off.** Not because it's a room, but when the overview would otherwise burst – when **contracts with deadlines, access to systems, named risks with consequences and a backstory** come together that somebody else would actually have to take over. And once it splits off, it is **maintained from then on** – not written at the end.

## A room may be a working directory

The skeleton only guarantees where the understanding lives. Whatever else a room needs – main documents, images, scripts, a git repository – sits alongside it and is explained in `00 Overview`. Obsidian doesn't show non-Markdown files anyway.

## Living documents and point-in-time documents

| | Example | What the vault does |
|---|---|---|
| **Living documents** | a concept, a specification, a list you maintain | If you maintain it yourself, it lives in the room. If it sits in shared storage, you **link and condense, never copy** – otherwise you're maintaining the worse of two versions. |
| **Point-in-time documents** | quotes, signed contracts, minutes, official notices | **A copy in `08 Attachments/`.** They don't change any more and belong to the decision as evidence. |

## Principles: what applies

`1_Knowledge/Principles/` is the only folder with **normative** notes – not what you know, but what applies: principles, rules, guidelines, agreements.

Each one carries in its header whether it applies, since when, and who approved it. That isn't a progress state, it's the content itself: a rule without approval is not a rule.

**Moving it is the approval.** A draft is written in the room that works it out. Only once it applies does it move to `Principles/`. That way nothing sits there that doesn't apply. [[What applies]] is the map over it.

## Diagrams

**A diagram as text inside the document is the source. A canvas is the working surface.**

Text is versioned along with the note, can be diffed and reworked. A canvas is for moving things around and crossing things out – alone or with others. **Whatever wins on the canvas gets pulled back into the text.** In case of conflict, the note wins. Same logic as draft and approval.

Tool-specific quirks don't belong here, they belong in [[Tool notes]].

## The AI layer

The vault is built so an assistant can work with it without you starting from scratch in every conversation.

**What you give an assistant:**

1. [[MANUAL]] – the rules, what goes where. That's why it sits at the root and can be handed on by itself
2. [[USER]] · [[SOUL]] · [[IDENTITY]] · [[CONTEXTS]] – who you are, how it should sound, what role it has, which worlds you move in
3. The room in question – the overview is usually enough

**What it gives back:** drafts, condensations, meeting extracts, posts that sound like you. What it does **not** do is written in [[IDENTITY]]: create no tasks, maintain no status fields, send nothing in your name.

**Why text files and not an assistant setting:** a file can be versioned, handed on and pasted into any tool. A vendor profile can't. When you switch models, you switch only the model.

The boundary stays the same as above: an AI doesn't create tasks here either.

## Where things go

| What | Where |
|---|---|
| A thought, unclear where it goes | `0_Inbox` – emptied at the weekly review |
| A meeting about a room | `<Room>/02 Meetings/` |
| A conversation without a room | `2_Calendar/Days/`, in the daily note |
| A decision that carries weight | `<Room>/01 Decisions/` |
| A specification, concept, requirement | `<Room>/03 Knowledge/` |
| A contract, quote, official notice (file) | `<Room>/08 Attachments/`, linked from the overview |
| A person you've met | `1_Knowledge/People/` |
| An organisation you deal with | `1_Knowledge/Organisations/` |
| "Which tool for what" | `1_Knowledge/Software/` |
| A book, video, article | `1_Knowledge/Sources/` |
| Your own concept, an insight | `1_Knowledge/Notes/` |
| An overview page about a topic | `1_Knowledge/Maps/` |
| An **approved** rule, principle, agreement | `1_Knowledge/Principles/` |
| A draft of a rule | in the room that works it out |
| A context-free file | `8_Attachments/` |

## File names

- Dated notes start with the date: `2026-09-07 Kickoff.md`
- People and organisations carry their name: `Jane Doe.md`
- Inside rooms, the overview and the handover carry the room name: `00 Overview – <Room>.md`. Otherwise you end up with twenty tabs all called "00 Overview".
- No prefixes, no numbering except for the room subfolders

## Frontmatter

Field names in English, content up to you. Only fill in what you actually maintain.

```yaml
type: room          # room | person | organisation | software | source | map |
                    # meeting | decision | principle | day | review | handover | note
context:            # only for rooms and for context-bound knowledge
participants: []
updated: 2026-09-10
```

For principles, additionally: `valid_since`, `approved_by`, `revision`.

## Weekly, 15 minutes

1. Empty `0_Inbox` – every note goes to its place or gets deleted
2. Extend the timelines of the active rooms with the lines someone has to understand later
3. Write the review in `2_Calendar/Reviews`
4. Move closed rooms to `_Closed/`

## Later, not now

Structure has to be earned. Only once it has carried you for four weeks:

- **Dataview** – generates context overviews automatically instead of you maintaining maps by hand
- **Templater** – templates with the date filled in automatically
- **Extend the AI layer** – meeting extraction and weekly consolidation. The groundwork is described above; in the template only the identity is set up: [[USER]], [[SOUL]], [[IDENTITY]], [[CONTEXTS]]. How to fill them in is in `9_System/Setup/`.
