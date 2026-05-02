# Decisions Log

> Append-only. Jede grössere Richtungsentscheidung kommt rein. Claude schlägt Einträge vor, ich bestätige.

## Format

```
## YYYY-MM-DD — <kurzer Titel>
- **Was:** Was wurde entschieden
- **Warum:** Welcher Trigger, welche Optionen waren auf dem Tisch
- **Konsequenz:** Was ändert sich daraus operativ
```

---

<!-- Beispiel-Eintrag — entfernen, sobald du den ersten echten Eintrag hast. -->
## 2026-05-02 — AIOS aufgesetzt

- **Was:** Diesen Workspace mit dem SkillPilot AIOS Starter initialisiert und das Superpowers-Plugin (`superpowers@claude-plugins-official`) aktiviert.
- **Warum:** Strukturierter Kontext + delegierbare Skills statt Copy-Paste-KI. Superpowers liefert die Workflow-Skills (brainstorming, writing-plans, TDD, verification) als Werks-Käse.
- **Konsequenz:** Ab jetzt wird Wissen nicht mehr nur in Köpfen und E-Mails gespeichert, sondern hier — versionierbar, durchsuchbar, von Claude Code lesbar. Neue Vorhaben starten mit `/brainstorm` (statt sofort drauflos).
