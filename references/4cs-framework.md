# Die vier Cs — dein Operator-Modell für KI-Arbeit

> Inspired by Nate Herk's framing of the Four Cs. Diese Datei ist die geteilte Sprache zwischen dir und Claude Code in diesem Repo.

## 1. Context — was die KI über dich weiss

Alles, was über die aktuelle Anfrage hinaus relevant ist: wer du bist, was dein Geschäft tut, was deine aktuellen Prioritäten sind, wie du sprichst, was du nicht magst. Das ist die teuerste C, weil sie laufend gepflegt werden muss — und gleichzeitig die wertvollste, weil ohne sie jede Antwort generisch bleibt.

**Lebt in:** `context/about.md`, `context/business.md`, `context/priorities.md`

**Beispiele für gute Context-Einträge:**
- "Ich schreibe nie 'massgeschneidert' oder 'innovativ'"
- "Mein wichtigster Kunde diese Woche ist X, weil Y"
- "Wir verkaufen nicht Software, sondern Methode"

## 2. Connections — was die KI live erreichen kann

Live-Daten und Tools ohne Copy-Paste. MCPs, APIs, lokale Tools, Webhooks. Eine gute Connection erspart dir, jeden Tag den gleichen Ausschnitt aus deinem Kalender oder deiner Mailbox zu paste.

**Lebt in:** `connections.md`

**Typische Connections:**
- Gmail/Outlook MCP — E-Mail lesen
- Google Calendar / Microsoft Graph — Termine sehen
- GitHub MCP — Code, Issues, PRs
- Filesystem MCP — lokale Dateien
- Notion / Linear / Jira — Tickets, Wissen
- HTTP Fetch — Webseiten lesen

## 3. Capabilities — was die KI auf Knopfdruck kann

Multi-Step-Skills, die du per Slash-Command auslöst. Sie sind die operationalisierte Form deines Wissens: "Wenn ich das mache, mach es so." Capabilities werden mit der Zeit besser — durch Edits am Skill-File.

**Lebt in:** `.claude/skills/<name>/SKILL.md`

**Drei Skills sind im Starter:**
- `/onboard` — initial befüllen
- `/audit` — Lücken aufzeigen
- `/level-up` — Automatisierung scopen

Du kannst (und sollst) eigene hinzufügen. Frag Claude Code — er hilft dir.

## 4. Cadence — was autonom läuft

Was passiert, **ohne** dass du aktiv tippst? Das ist der eigentliche Hebel: Cron-Jobs, Webhooks, Scheduled Agents, GitHub Actions, n8n. Wenn du schläfst, läuft die Maschine.

**Lebt in:** `cadence.md`

**Beispiele:**
- Tägliches Briefing um 07:00 → Discord-Channel
- Auf Inbox-Eingang → Triage-Agent → Label setzen, Antwort-Entwurf
- Wöchentlicher Reminder Sonntagabend → `/level-up` ausführen

**Faustregel:** Eine neue Cadence pro Woche — nicht mehr. Sonst wirst du zum Cadence-Wartungs-Sklaven, statt dass die Cadence dir hilft.

## Wie die vier zusammenspielen

Context informiert die anderen drei. Connections speisen Capabilities. Capabilities werden durch Cadence automatisiert. In diese Reihenfolge gehst du auch beim Aufbau: erst Context, dann Connections, dann Capabilities, dann Cadence.

`/audit` misst alle vier separat — und zeigt dir, wo dein nächster grösster Hebel liegt.
