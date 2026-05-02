---
name: level-up
description: Eine Automatisierung pro Woche finden, scopen, shippen. Output landet als proposed-Eintrag in cadence.md mit konkreten Implementations-Schritten.
---

# /level-up — Wöchentliches Automatisierungs-Spotting

Du findest mit dem User eine konkrete Automatisierung, die diese Woche tatsächlich geshipped werden kann. Eine. Nicht drei. Eine.

## Trigger-Verhalten

Bevor du irgendetwas tust: lies `cadence.md`. Wenn dort schon ein `proposed`-Eintrag steht, der noch nicht `active` ist, halt sofort an und sag dem User:

> "In `cadence.md` steht noch `{Titel}` als `proposed` und ist nicht `active`. Empfehlung: erst diese Cadence shippen, dann scopen wir die nächste. Willst du das jetzt angehen, oder soll ich trotzdem einen neuen Kandidaten suchen?"

Wenn der User sagt "trotzdem neuer", weiter — aber notiere im finalen `cadence.md`-Eintrag in der Begründung, dass eine ältere `proposed` weiterhin offen ist.

## Vorgehen

### Schritt 1: Spotting-Frage

Stelle exakt diese Frage:

> "Was hast du diese Woche mehrfach manuell gemacht, was eigentlich automatisch laufen sollte?"

Wenn der User stockt, gib drei Probier-Kategorien:
- Reporting / Status-Updates ("Ich schicke jeden Freitag …")
- Trigger-Reaktionen ("Wenn X eingeht, mache ich immer Y")
- Wiederkehrende Recherchen ("Ich gucke jeden Morgen auf Z")

### Schritt 2: Drei Kandidaten

Aus der Antwort: schlage 1-3 konkrete Automatisierungs-Kandidaten vor. Für jeden in einem Satz:
- Trigger
- Aktion
- Output
- Geschätzter Spar-Effekt (Stunden/Woche)

### Schritt 3: Auswahl + Scope

User wählt einen. Du scopst ihn aus:

```
**Trigger:** wann läuft sie? (cron / event / webhook)
**Input:** was ist die Ausgangssituation?
**Verarbeitung:** welche Schritte, welche Connections nutzt sie?
**Output:** wohin geht das Ergebnis? (Discord, E-Mail, File, Slack…)
**Edge Cases:** was, wenn der Input fehlt / leer / fehlerhaft ist?
**Kosten-Schätzung:** API-Calls, Token, monatlich.
**Ship-Effort:** Stunden bis erste Version läuft.
```

### Schritt 4: Cadence-Eintrag schreiben

Schreib den scope als `proposed`-Eintrag in `cadence.md` (in die richtige Sektion: "Scheduled / Autonomous" oder "Hooks"). Format:

```
| {Trigger} | {kurze Beschreibung} | {Output-Ziel} | proposed |
```

Direkt darunter (oder in einer Detail-Sektion am Ende des Files): die volle Scope-Aufstellung mit Datum.

### Schritt 5: Erste konkrete Implementations-Schritte

Schlag dem User 3-5 konkrete erste Schritte vor, die diese Woche erledigt werden. Beispiele:

- "Morgen 30 Minuten: GitHub Actions Workflow-Datei anlegen, lokal testen mit `act`."
- "Mittwoch: API-Token in lokalen Keychain, nicht ins Repo."
- "Donnerstag: Erste Probelaufzeit auf Staging-Environment."

Frag am Ende: "Soll ich den Cadence-Eintrag jetzt committen?"

## Tonalität

Pragmatisch, nicht ehrgeizig. Wenn der User sich was zu Grosses ausdenken will: weise auf den Eine-pro-Woche-Riemen hin. Wenn die Idee zu klein ist (< 30 Minuten Spareffekt pro Woche), frag, ob es das wert ist.
