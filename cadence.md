# Cadence — was autonom läuft

> Was passiert, ohne dass ich aktiv tippe? Cron-Jobs, Hooks, Scheduled Agents, n8n-Workflows, GitHub Actions.

## Scheduled / Autonomous

| Trigger | Was passiert | Output landet wo | Status |
|---------|--------------|------------------|--------|
| (wird durch /onboard und /level-up gefüllt) | | | |

## Hooks

| Event | Aktion | Status |
|-------|--------|--------|
| (z.B. SessionStart, PreToolUse, PostCommit) | | |

## Status-Konvention

- `proposed` — scoped, noch nicht implementiert
- `active` — läuft
- `paused` — manuell pausiert
- `retired` — ausgeschaltet, Eintrag bleibt für Historie

## Pro Woche maximal eine neue `active`-Cadence

`/level-up` setzt das durch: wenn schon ein `proposed` offen ist, wird es zuerst geshipped, bevor ein neuer Kandidat scopt wird.
