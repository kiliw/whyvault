# Second Brain – Template

Ein Obsidian-Vault, der eine einzige Frage konsequent beantwortet: **warum ist das so?** Aufgaben, Termine und Fortschritt bleiben in deinem Task-Tool.

Ordner- und Dateinamen englisch, Text darin deutsch. Entstanden in einem beruflichen Vault und hier auf die Grundstruktur reduziert – ohne Beispiele aus einem bestimmten Beruf oder Lebensbereich.

## Warum

Für Leute, die vieles gleichzeitig tragen: Anstellung, eigene Produkte, Familie. Der Engpass ist dabei nicht die Arbeit, sondern der Wiedereinstieg. Nach zwei Wochen in eine Sache zurückkommen und in fünf Minuten wissen, warum etwas so entschieden wurde.

Der Vault ist die Zentrale, aus der heraus gearbeitet wird, und gleichzeitig der Kontext, den eine KI braucht, um brauchbare statt generischer Ergebnisse zu liefern: Marke, Stimme, Grenzen, letzte Entscheidungen. Ein Teil der Arbeit, Beiträge, Verdichtungen, Meeting-Extrakte, lässt sich damit abgeben.

**Agent-agnostisch:** alles, was ein Assistent über dich wissen muss, liegt als Textdatei im Vault, nicht in den Einstellungen eines Anbieters. Claude, ChatGPT, ein lokales Modell: du gibst ihm `MANUAL.md` und die vier Identitätsdateien, und es arbeitet nach denselben Regeln. Der Vault gehört dir, das Modell ist austauschbar.

## Schnellstart

1. **Repository herunterladen** – „Use this template", `git clone`, oder als ZIP.
2. In Obsidian: **Open folder as vault** und diesen Ordner wählen. Der Ordner *ist* der Vault, es gibt nichts zu kopieren.
3. **`Start here.md`** öffnen und **[[MANUAL]]** einmal ganz lesen – es ist eine Seite.
4. **Identität anlegen:** `9_System/Setup/Interview prompt.md` in deinen KI-Assistenten kopieren und dich befragen lassen. Ergebnis sind `USER.md`, `SOUL.md` und `IDENTITY.md`. Wer schon Chat-Erinnerungen hat, nimmt `From memories prompt.md`.
5. **Kontext benennen:** `3_Rooms/your-context-here/` umbenennen, `CONTEXTS.md` ausfüllen. Einer genügt.
6. **Einen ersten Room anlegen** – mit genau einer Datei, der Übersicht.

## Die fünf Regeln

1. **Der Vault beantwortet „warum", das Aufgaben-Tool „was als nächstes".** Keine Aufgaben, keine Fristen, keine Fortschritts-Status. Sonst hast du zwei Wahrheiten und pflegst die schlechtere.
2. **Room oder Sammlung?** Hat die Sache einen Verlauf – Dinge werden entschieden, es gibt eine Chronik → **Room**. Ist sie ein gepflegter Bestand → **Sammlung** in `1_Knowledge` mit einer Karte als Eingang.
3. **Grenzregel.** Innerhalb eines Rooms beliebig verlinken, nach außen nur auf `1_Knowledge`, niemals Room zu Room. Das macht einen Room als Ordner abgebbar – und ist gleichzeitig der Test, ob etwas projektspezifisch oder allgemein ist.
4. **Das Skelett wird nicht vorbezahlt.** Ein neuer Room hat genau eine Datei. `01 Decisions/`, `02 Meetings/` und der Rest entstehen bei Bedarf. Die Namen sind fest, die Vollständigkeit nicht – ein leerer Entscheidungsordner behauptet, es sei nichts entschieden worden.
5. **Wissen gehört keinem Room. Einen Kontext darf es haben.** Deshalb ist Kontext nur unter `3_Rooms` eine Ordnerebene: eine Person kann in mehreren Welten auftauchen und existiert trotzdem nur einmal.

## Struktur

```
MANUAL.md                     die Regeln, an der Wurzel und einzeln weitergebbar
Start here.md                 Einstieg in Obsidian
0_Inbox/                      alles Unsortierte, wird geleert
1_Knowledge/                  zeitlos, flach, geteilt
  People/  Organisations/  Software/  Notes/  Sources/  Maps/  Principles/
2_Calendar/                   datiert, dünn
  Days/  Reviews/
3_Rooms/                      alles Abgegrenzte, einzige Kontextebene
  your-context-here/          Platzhalter, je Kontext mit _Closed/
8_Attachments/                kontextfreie Dateien
9_System/
  Tool notes.md               werkzeugspezifische Eigenheiten, bewusst getrennt
  Identity/                   USER · SOUL · IDENTITY · CONTEXTS
  Setup/                      Interview- und Memories-Prompt
  Templates/                  13 Vorlagen
```

Room-Skelett: `00 Overview – <Room>.md`, dann bei Bedarf `01 Decisions/`, `02 Meetings/`, `03 Knowledge/`, `08 Attachments/`, `Documents.md`, `04 Sub-projects/`, `99 Handover – <Room>.md`.

## Die vier Identitätsdateien

| Datei | Beantwortet |
|---|---|
| `USER.md` | Wer ich bin und wie ich arbeite |
| `SOUL.md` | Wie es klingen soll, wenn für mich geschrieben wird |
| `IDENTITY.md` | Wer der Assistent für mich sein soll – Mandat, Grenzen, Standardverhalten |
| `CONTEXTS.md` | In welchen Welten ich mich bewege (das sind die Ordner unter `3_Rooms`) |

Sie werden nicht von Hand geschrieben, sondern per Interview oder aus vorhandenen Erinnerungen erzeugt – siehe `9_System/Setup/`.

## Was absichtlich fehlt

Keine Plugins, keine Automatik, keine Beispiel-Rooms, keine vorbelegten Kontexte. **Struktur muss verdient werden:** erst benutzen, dann verfeinern. Dataview und Templater lohnen sich, wenn das Skelett vier Wochen getragen hat – die Frontmatter-Schlüssel sind darauf ausgelegt.

## Wenn du einen Vault in anderer Sprache daneben betreibst

| Englisch | Deutsch |
|---|---|
| `0_Inbox` | `0_Eingang` |
| `1_Knowledge` | `1_Wissen` |
| `People / Organisations / Software / Notes / Sources / Maps / Principles` | `Personen / Organisationen / Software / Notizen / Quellen / Karten / Leitlinien` |
| `2_Calendar` · `Days` · `Reviews` | `2_Kalender` · `Tage` · `Rückblicke` |
| `3_Rooms` · `_Closed` | `3_Räume` · `_Abgeschlossen` |
| `8_Attachments` | `8_Anhänge` |
| `9_System` · `MANUAL` · `Identity` · `Templates` | `9_System` · `Anleitung` · `Identität` · `Vorlagen` |
| `00 Overview` · `01 Decisions` · `02 Meetings` · `03 Knowledge` · `08 Attachments` · `99 Handover` | `00 Übersicht` · `01 Entscheidungen` · `02 Meetings` · `03 Wissen` · `08 Anhänge` · `99 Übergabe` |

Die Frontmatter-Schlüssel sind in beiden Fällen englisch (`type`, `context`, `updated`) – das ist die Naht, an der sich zwei Vaults später zusammenziehen lassen.

## Lizenz

Noch nicht festgelegt – siehe `LICENSE`.
