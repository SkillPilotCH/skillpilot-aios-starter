---
name: onboard
description: Initial-Interview entlang der vier Cs. Befüllt intake.md, context/, connections.md und cadence.md. Idempotent — re-run respektiert vorhandene Antworten.
---

# /onboard — Initial-Interview

Du führst den User durch ein strukturiertes Interview entlang der vier Cs (Context, Connections, Capabilities, Cadence). Ergebnis: ein lebendiges AIOS, in dem die wichtigsten Files nicht mehr Stubs sind.

## Trigger-Verhalten

- **Erstaufruf:** `intake.md` enthält noch das Stub-Markup ("(offen)"). Du beginnst das Interview.
- **Re-run:** `intake.md` hat schon Antworten. Lies sie. Frag nur dort nach, wo noch "(offen)" steht oder wo der User selbst um Update bat. Niemals stillschweigend überschreiben.

## Vorgehen

### Schritt 1: Begrüssung und Erwartungs-Setting

Sag in zwei Sätzen, was passiert: ~10 Fragen, ~15 Minuten, das Ergebnis ist ein befülltes Skelett. Frag, ob der User bereit ist.

### Schritt 2: Context-Block

Stelle die Fragen aus `intake.md` unter `## Context`, **eine nach der anderen** (nicht gebatcht). Nach jeder Antwort: kurz zurück­spiegeln ("Verstanden — du bist X, Hauptpriorität Y."), dann die nächste Frage. Schreib die Antworten direkt in `intake.md`.

Nach dem Block: synthesiere die Context-Antworten in:
- `context/about.md` (Identität, Hintergrund, Sprache & Stil)
- `context/business.md` (Was wir tun, Für wen, Geld, Stand)
- `context/priorities.md` (Top 3, was bewusst nicht prio, Deadlines)

Halte jedes File maximal eine Bildschirmseite lang. Lieber knapp als episch.

Ersetze in `CLAUDE.md` die Platzhalter `{{NAME}}` und `{{PRIORITÄT}}` durch die konkreten Werte aus den Antworten. Falls die Priorität sich ändert, wird `CLAUDE.md` von Hand oder durch ein späteres `/onboard`-Re-run aktualisiert.

### Schritt 3: Connections-Block

Stelle die Connections-Fragen. Für jedes genannte Tool: notiere in `connections.md` einen Eintrag mit Status `geplant` (wenn noch keine MCP-Anbindung steht) oder `aktiv` (wenn der User bestätigt, dass die Verbindung schon läuft).

Schreib **keine** Tokens oder Auth-Werte in das File. Nur das System, den Zweck, den Auth-Typ ("OAuth", "API-Key", "lokal") und den Status.

### Schritt 4: Capabilities-Block

Stelle die Capabilities-Fragen. Du erstellst hier **noch keine** neuen Skills. Du sammelst nur die Antworten in `intake.md` als Roh-Input. Am Ende des Blocks: schlag dem User 1-3 Skill-Ideen vor, die aus seinen Antworten erwachsen, und sag, dass er die später per `/level-up` schärfen kann.

### Schritt 5: Cadence-Block

Stelle die Cadence-Fragen. Aus den Antworten ("was würdest du loswerden") leite **einen** konkreten Cadence-Kandidaten ab und schreib ihn als `proposed`-Eintrag in `cadence.md`. Nicht mehr — eine pro Onboarding reicht.

### Schritt 6: Wrap-up

- Zeig dem User eine kurze Zusammenfassung: was wurde befüllt, was steht in welchem File.
- Schlag vor, ein erstes `decisions/log.md`-Eintrag zu schreiben ("AIOS in Betrieb genommen").
- Schlag vor, jetzt ein erstes Commit zu machen ("Sag mir, wenn ich diesen Stand committen soll — ich kümmere mich.").
- Erinnere an Tag 7: `/audit` aufrufen.

## Was du dabei NIE tust

- Tokens, Passwörter oder API-Keys in irgendein File schreiben.
- Antworten erfinden oder annehmen, wenn der User unsicher ist — bei Unsicherheit: lass die Antwort offen oder schreib die wörtliche Antwort des Users mit `(unsicher)` dazu.
- Mehr als eine Frage gleichzeitig stellen.
- Überspringen, dass `intake.md` die Roh-Antworten sammelt — die synthetischen `context/`-Files sind kuratiert, nicht ersetzt durch das Original.
