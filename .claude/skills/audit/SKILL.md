---
name: audit
description: 4-Cs-Gap-Report. Scored 0-10 pro Achse, zeigt die Top 3 Lücken. Erste Ausführung Tag 7 nach /onboard, danach wöchentlich.
---

# /audit — 4-Cs-Gap-Report

Du gehst die vier Cs durch und gibst dem User ein ehrliches Bild, wie reif sein AIOS ist und wo der nächste grösste Hebel liegt.

## Trigger-Verhalten

- Wenn weniger als 7 Tage seit dem letzten `/onboard`-Eintrag in `decisions/log.md` (oder kein solcher Eintrag existiert): sag das, frag, ob trotzdem.
- Wenn schon ein Audit in den letzten 5 Tagen lief (suchbar als `## YYYY-MM-DD — Audit` in `decisions/log.md`): sag das, frag, ob trotzdem.

## Vorgehen

### Schritt 1: Lesen

Lies in dieser Reihenfolge:
- `context/about.md`, `context/business.md`, `context/priorities.md`
- `connections.md`
- `.claude/skills/` (welche Skills existieren, wie aktuell sind sie)
- `cadence.md`
- `decisions/log.md` (letzte 5 Einträge)

### Schritt 2: Scoring

Score 0-10 pro C. Begründe jeden Score in maximal zwei Sätzen.

| C | Score (0-10) | Begründung |
|---|--------------|------------|
| Context | ? | |
| Connections | ? | |
| Capabilities | ? | |
| Cadence | ? | |

**Score-Anker:**
- 0-2 — leer oder Stub
- 3-4 — Grundgerüst da, fühlt sich aber generisch an
- 5-6 — funktional, aber mit klaren Lücken
- 7-8 — solide, lebt, wird aktiv genutzt
- 9-10 — Gold-Standard

### Schritt 3: Top 3 Lücken

Nach den Scores: nenne die drei grössten Lücken, **priorisiert nach Hebel** (was bringt am meisten, wenn man's schliesst). Pro Lücke:

- Was fehlt
- Warum das ein Hebel ist
- Konkreter erster Schritt (eine Stunde Aufwand)

### Schritt 4: Vorschlag Decisions-Log-Eintrag

Schlag einen Eintrag für `decisions/log.md` vor in der Form:

```
## YYYY-MM-DD — Audit
- **Was:** Audit-Score: C={n}, Co={n}, Ca={n}, Cd={n}
- **Warum:** Wöchentliche / verlangte Selbstprüfung.
- **Konsequenz:** Top-Lücke "{kurz}", erster Schritt diese Woche.
```

Frag, ob du den Eintrag committen sollst.

## Tonalität

Ehrlich, nicht weichgespült. Wenn der Score 4 ist, sag 4. "Solide" ist nur dann das Wort, wenn es ≥7 ist. Keine Lobhudelei.
