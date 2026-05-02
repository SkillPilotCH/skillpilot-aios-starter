# Connections

> Was kann diese KI live erreichen — ohne dass ich Daten reinpaste? MCPs, APIs, Webhooks, lokale Tools.

## Aktive Verbindungen

| System | Zweck | Auth-Typ | Status | Letzte Prüfung |
|--------|-------|----------|--------|----------------|
| (wird durch /onboard befüllt) | | | | |

## Status-Werte

- `aktiv` — verbunden und funktioniert
- `flaky` — manchmal fällt sie aus, Workarounds nötig
- `paused` — bewusst getrennt
- `geplant` — auf der Wunschliste, noch nicht eingerichtet

## Was hier NICHT reingehört

Tokens, Passwörter, API-Keys, Client Secrets, OAuth-Codes. Auth-Werte gehören in den OS-Keychain, in eine `.env`-Datei (gitignored), oder in den jeweiligen MCP-Server. Hier steht nur, **dass** etwas Auth braucht (z.B. "OAuth via gh CLI"), nicht **was** der Wert ist.
