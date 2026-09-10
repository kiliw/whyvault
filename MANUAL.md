---
type: system
---

# Manual – das System auf einer Seite

*Die Regeln. Liegt bewusst an der Wurzel, damit sie sich einzeln weitergeben lässt.*

## Wofür das gedacht ist

Für Leute, die vieles gleichzeitig tragen: eine Anstellung, eigene Produkte, Familie. Nicht ein Projekt nach dem anderen, sondern fünf nebeneinander, jedes mit eigenen Beteiligten, eigenen Entscheidungen und eigenem Ablagestand.

Der Engpass dabei ist nicht die Arbeit, sondern der **Wiedereinstieg**: nach zwei Wochen in einer Sache zurückkommen und in fünf Minuten wieder wissen, warum etwas so entschieden wurde. Genau dafür ist dieser Vault die Zentrale. Er ist die Stelle, an der der Kontext liegt, aus dem heraus gearbeitet wird: ein Beitrag, eine Kampagne, eine Entscheidung, eine Übergabe.

Und weil der Kontext geschrieben und geordnet ist, lässt sich ein Teil der Arbeit an eine KI abgeben. Nicht weil das Modell klug ist, sondern weil es den richtigen Ausschnitt bekommt: die Marke, die Stimme, die Grenzen, die letzten Entscheidungen. Schlechter Kontext erzeugt generische Ergebnisse, guter Kontext erzeugt brauchbare.

**Agent-agnostisch.** Alles, was der Assistent über dich wissen muss, liegt als Textdatei im Vault, nicht in den Einstellungen eines Anbieters. Claude, ChatGPT, ein lokales Modell, das nächste Werkzeug: du gibst ihm [[MANUAL]] und die vier Identitätsdateien, und es arbeitet nach denselben Regeln. Der Vault gehört dir, das Modell ist austauschbar.

## Die Grenze des Systems

**Dieser Vault beantwortet „warum". Dein Aufgaben-Tool beantwortet „was als nächstes".**

Testsatz für alles, was du erfassen willst:

- Hat es einen Verantwortlichen und ein Fälligkeitsdatum? → **Aufgaben-Tool**
- Muss man es in sechs Monaten noch verstehen können? → **hier**

Hier gibt es deshalb keine Aufgaben, keine Fristen, keine Fortschritts-Status. Wenn du anfängst, hier Häkchen zu setzen, hast du zwei Wahrheiten und pflegst die schlechtere.

## Drei Arten von Dingen

| | Was | Grenze | Bei Übergabe |
|---|---|---|---|
| **Rooms** (`3_Rooms`) | alles mit eigenen Entscheidungen, Beteiligten und einem Ende | ja – ein Ordner | wird als Paket abgegeben |
| **Knowledge** (`1_Knowledge`) | Personen, Organisationen, Software, Notizen, Quellen, Prinzipien | nein – flach und geteilt | bleibt bei dir |
| **Calendar** (`2_Calendar`) | Tagesnotizen, Rückblicke | dünn, nur Zeitachse | irrelevant |

**Wissen gehört keinem Room. Einen Kontext darf es haben.** Deshalb hat nur `3_Rooms` eine Kontextebene. Eine Person kann privat und geschäftlich auftauchen – die Notiz existiert genau einmal und trägt keinen Kontext. Etwas, das ausdrücklich nur für einen Kontext gilt, ist trotzdem Wissen und bekommt das Feld `context:`. Entscheidend ist nur: keine Wissen-Notiz wohnt in einem Room.

## Room oder Sammlung?

Die häufigste Verwechslung – und die, die Ordner mit leeren Unterordnern erzeugt. Eine Frage entscheidet:

> **Hat die Sache einen Verlauf?** Passieren Dinge, die entschieden werden und die man später verstehen muss?

- **Ja** → **Room.** Es gibt Entscheidungen, Gespräche, eine Chronik, irgendwann einen Abschluss.
- **Nein, es ist ein Bestand, der gepflegt wird** → **Sammlung in `1_Knowledge`**, mit einer Karte in `Maps/` als Eingang. Eine Sammlung wird nie übergeben – sie bleibt.

Sammlungen brauchen keine Meetings, keine Entscheidungen und keine Übergabe. Was an einer Sammlung *Arbeit* ist, passiert in einem Room und landet danach in der Sammlung.

## Die Grenzregel

**Innerhalb eines Rooms darf beliebig verlinkt werden. Nach außen nur auf `1_Knowledge`. Niemals von Room zu Room.**

Kopiert man einen Room-Ordner heraus, zeigt nur eine kurze, bekannte Liste von Links ins Leere – Personen, Organisationen, Software. Die lassen sich beilegen. Wenn zwei Rooms dasselbe brauchen, wird daraus eine Notiz in `1_Knowledge`. Die Regel ist also gleichzeitig der Test, ob etwas projektspezifisch oder allgemein ist.

Sie gilt in beide Richtungen: eine Notiz in `1_Knowledge` verweist auf einen Room höchstens im Klartext, nie als Wiki-Link. **Eine Ausnahme:** [[Rooms]] ist die Landkarte über die Rooms und muss sie verlinken – das ist Navigation, kein Inhalt.

## Status

Der einzige Status ist die Ordnerposition. Ein Room liegt in `<context>/` oder in `<context>/_Closed/`. Ein Handgriff, wenn etwas endet. Sonst nichts.

An die Stelle von Status tritt die **Chronik** in `00 Overview`: eine Zeile pro Ereignis, das man später verstehen muss.

## Das Skelett: gleiche Namen, nicht gleiche Vollständigkeit

Von Tag 1 existiert genau **eine** Datei:

```
<Room>/
└── 00 Overview – <Room>.md    Zweck, Grenzen, Beteiligte, wer entscheidet was,
                               Systeme, Chronik, offene Fragen
```

Die Übersicht **ist** das Übergabedokument, solange sie reicht. Alles Weitere entsteht, wenn es gebraucht wird – und heißt dann so:

```
01 Decisions/            bei der ersten Entscheidung mit Gewicht
02 Meetings/             beim ersten Gespräch, das man später verstehen muss
03 Knowledge/            beim ersten raumspezifischen Dokument
08 Attachments/          bei der ersten Datei
Documents.md             wenn es mehr als eine Handvoll Dokumente gibt
04 Sub-projects/<X>/     wenn ein Teil eigene Entscheidungen und Meetings ansammelt
99 Handover – <Room>.md  wenn es wirklich etwas zu übergeben gibt (siehe unten)
```

**Die Namen sind fest, die Vollständigkeit nicht.** Ein leerer `01 Decisions/`-Ordner behauptet, es sei nichts entschieden worden, und das ist fast immer falsch. **Das Skelett wird nicht vorbezahlt.** Ausnahme sind die `_Closed/`-Ordner je Kontext: die sind leer, und diese Leere ist eine wahre Aussage.

**Wann sich die Übergabe abspaltet.** Nicht weil es ein Room ist, sondern wenn die Übersicht sonst platzen würde – wenn **Verträge mit Fristen, Zugänge zu Systemen, benannte Risiken mit Folgen und eine Vorgeschichte** zusammenkommen, die jemand anders tatsächlich übernehmen müsste. Und wenn sie sich abspaltet, wird sie **ab dann gepflegt** – nicht am Ende geschrieben.

## Ein Room darf ein Arbeitsverzeichnis sein

Das Skelett garantiert nur, wo das Verstehen liegt. Was ein Room darüber hinaus braucht – Hauptdokumente, Bilder, Skripte, ein Git-Repository – liegt daneben und wird in `00 Overview` erklärt. Obsidian zeigt Nicht-Markdown-Dateien ohnehin nicht an.

## Lebende und Zeitpunkt-Dokumente

| | Beispiel | Was der Vault macht |
|---|---|---|
| **Lebende Dokumente** | ein Konzept, eine Spezifikation, eine Liste, die du pflegst | Wenn du sie selbst pflegst, wohnen sie im Room. Liegen sie in einer geteilten Ablage, wird **verlinkt und verdichtet, nie kopiert** – sonst pflegst du die schlechtere von zwei Fassungen. |
| **Zeitpunkt-Dokumente** | Angebote, unterschriebene Verträge, Protokolle, Bescheide | **Kopie in `08 Attachments/`.** Sie ändern sich nicht mehr und gehören als Beleg zur Entscheidung. |

## Principles: was gilt

`1_Knowledge/Principles/` ist der einzige Ordner mit **normativen** Notizen – nicht was du weißt, sondern was gilt: Prinzipien, Regeln, Leitlinien, Absprachen.

Jede trägt im Kopf, ob und seit wann sie gilt und wer sie verabschiedet hat. Das ist kein Fortschritts-Status, sondern der Inhalt selbst: eine Regel ohne Verabschiedung ist keine Regel.

**Das Verschieben ist die Verabschiedung.** Ein Entwurf entsteht in dem Room, der ihn erarbeitet. Erst wenn er gilt, wandert er nach `Principles/`. So liegt dort nie etwas, das nicht gilt. [[What applies]] ist die Karte darüber.

## Diagramme

**Ein Diagramm als Text im Dokument ist die Quelle. Eine Zeichenfläche ist die Arbeitsfläche.**

Text wird mit der Notiz versioniert, lässt sich vergleichen und überarbeiten. Eine Zeichenfläche ist zum Verschieben und Durchstreichen – allein oder mit anderen. **Was sich auf der Fläche durchsetzt, wird in den Text nachgezogen.** Bei Widerspruch gilt die Notiz. Dieselbe Logik wie Entwurf und Verabschiedung.

Werkzeugspezifische Eigenheiten gehören nicht hierher, sondern in [[Tool notes]].

## Die KI-Schicht

Der Vault ist so gebaut, dass ein Assistent damit arbeiten kann, ohne dass du in jedem Gespräch von vorn anfängst.

**Was du einem Assistenten gibst:**

1. [[MANUAL]] – die Regeln, wohin was gehört. Deshalb liegt es an der Wurzel und ist einzeln weitergebbar
2. [[USER]] · [[SOUL]] · [[IDENTITY]] · [[CONTEXTS]] – wer du bist, wie es klingen soll, welche Rolle er hat, in welchen Welten du dich bewegst
3. Den Room, um den es geht – die Übersicht reicht meistens

**Was er zurückgibt:** Entwürfe, Verdichtungen, Meeting-Extrakte, Beiträge, die nach dir klingen. Was er **nicht** tut, steht in [[IDENTITY]]: keine Aufgaben anlegen, keine Statusfelder pflegen, nichts in deinem Namen verschicken.

**Warum Textdateien und keine Assistenten-Einstellung:** eine Datei lässt sich versionieren, weitergeben und in jedes Werkzeug kopieren. Ein Anbieter-Profil nicht. Wenn du das Modell wechselst, wechselst du nur das Modell.

Die Grenze bleibt dieselbe wie oben: auch eine KI legt hier keine Aufgaben an.

## Wohin kommt was

| Was | Wohin |
|---|---|
| Gedanke, unklar wohin | `0_Inbox` – wird beim Wochenrückblick geleert |
| Meeting zu einem Room | `<Room>/02 Meetings/` |
| Gespräch ohne Room | `2_Calendar/Days/` in der Tagesnotiz |
| Entscheidung mit Gewicht | `<Room>/01 Decisions/` |
| Spezifikation, Konzept, Anforderung | `<Room>/03 Knowledge/` |
| Vertrag, Angebot, Bescheid (Datei) | `<Room>/08 Attachments/`, aus der Übersicht verlinkt |
| Person, die du getroffen hast | `1_Knowledge/People/` |
| Organisation, mit der du zu tun hast | `1_Knowledge/Organisations/` |
| „Welches Tool für was" | `1_Knowledge/Software/` |
| Buch, Video, Artikel | `1_Knowledge/Sources/` |
| Eigenes Konzept, Erkenntnis | `1_Knowledge/Notes/` |
| Übersichtsseite über ein Thema | `1_Knowledge/Maps/` |
| **Verabschiedete** Regel, Prinzip, Absprache | `1_Knowledge/Principles/` |
| Entwurf einer Regel | im Room, der sie erarbeitet |
| Kontextfreie Datei | `8_Attachments/` |

## Dateinamen

- Datierte Notizen beginnen mit dem Datum: `2026-09-07 Kickoff.md`
- Personen und Organisationen tragen ihren Namen: `Max Mustermann.md`
- In Rooms tragen Übersicht und Übergabe den Room-Namen mit: `00 Overview – <Room>.md`. Sonst hast du zwanzig Tabs, die alle „00 Overview" heißen.
- Keine Umlaut-Vermeidung, keine Präfixe, keine Nummern außer bei den Room-Unterordnern

## Frontmatter

Feldnamen englisch, Inhalt egal. Nur eintragen, was du auch pflegst.

```yaml
type: room          # room | person | organisation | software | source | map |
                    # meeting | decision | principle | day | review | handover | note
context:            # nur bei Rooms und bei kontextgebundenem Wissen
participants: []
updated: 2026-09-10
```

Bei Principles zusätzlich: `valid_since`, `approved_by`, `revision`.

## Wöchentlich, 15 Minuten

1. `0_Inbox` leeren – jede Notiz kommt an ihren Platz oder wird gelöscht
2. Chronik der aktiven Rooms um die Zeilen ergänzen, die man später verstehen muss
3. Rückblick in `2_Calendar/Reviews` schreiben
4. Abgeschlossene Rooms nach `_Closed/` ziehen

## Später, nicht jetzt

Struktur muss verdient werden. Erst wenn sie vier Wochen getragen hat:

- **Dataview** – macht Kontext-Übersichten automatisch, statt Karten manuell zu pflegen
- **Templater** – Vorlagen mit automatischem Datum
- **KI-Schicht ausbauen** – Meeting-Extraktion und wöchentliche Konsolidierung. Die Grundlage dafür ist oben beschrieben; im Template ist nur die Identität angelegt: [[USER]], [[SOUL]], [[IDENTITY]], [[CONTEXTS]]. Wie du sie füllst, steht in `9_System/Setup/`.
