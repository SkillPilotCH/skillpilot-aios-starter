# Connections

> Was kann diese KI live erreichen — ohne dass ich Daten reinpaste? MCPs, APIs, Webhooks, lokale Tools.

## Code vs. Desktop — zwei Mechanismen, gleiches Ziel

KI-zu-System-Brücken kommen in zwei Formen, je nach Tool:

- **Claude Code (VS Code)** spricht mit **MCP-Servern**, die du selbst installierst (`claude mcp add ...` oder via natursprachliche Delegation an Claude Code). Das ist explizit, kontrollierbar, beliebig erweiterbar.
- **Claude Desktop** liefert ab Werk **Connectors** mit (z.B. GitHub, Google Drive, Gmail). Da musst du nichts installieren, dafür wählt Anthropic, was es gibt.

Outcome ist meist identisch (Claude liest/schreibt im verbundenen System). Welcher Mechanismus fürs eigene Setup besser passt, hängt davon ab, ob du die Kontrolle willst (Code) oder den schnelleren Einstieg (Desktop).

In dieser Datei trackst du **beides**, damit du den Überblick hast — auch wenn du in der Praxis einen der beiden Wege bevorzugst.

## Verbindungen in Claude Code (MCP)

| System | Zweck | Auth-Typ | Status | Letzte Prüfung |
|--------|-------|----------|--------|----------------|
| (wird durch /onboard befüllt) | | | | |

## Verbindungen in Claude Desktop (Connectors)

| System | Zweck | Status | Letzte Prüfung |
|--------|-------|--------|----------------|
| (optional — nur eintragen, wenn du Desktop ergänzend nutzt) | | | |

## Status-Werte

- `aktiv` — verbunden und funktioniert
- `flaky` — manchmal fällt sie aus, Workarounds nötig
- `paused` — bewusst getrennt
- `geplant` — auf der Wunschliste, noch nicht eingerichtet

## Was hier NICHT reingehört

Tokens, Passwörter, API-Keys, Client Secrets, OAuth-Codes. Auth-Werte gehören in den OS-Keychain, in eine `.env`-Datei (gitignored), oder in den jeweiligen MCP-Server. Hier steht nur, **dass** etwas Auth braucht (z.B. "OAuth via gh CLI"), nicht **was** der Wert ist.
