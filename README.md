# SkillPilot AIOS Starter

> Du musst nichts von dem hier auswendig lernen. Öffne dieses Repo in VS Code, starte Claude Code, und sag in eigenen Worten, was du willst. Die Befehle weiter unten sind nur für die Neugierigen.

Ein strukturiertes Skelett für dein persönliches "AI Operating System" — der Startpunkt, ab dem du mit Claude Code dein eigenes Setup ausbaust.

Begleitmaterial zum [SkillPilot Power-User Workshop](https://skillpilot.ch). Standalone funktioniert es, den vollen Wert kriegst du im Kurs.

## Was ist das?

Ein Template-Repo, organisiert entlang der **vier Cs**: Context, Connections, Capabilities, Cadence. Du klonst es, beantwortest ein paar Fragen mit Claude Code, und hast danach eine wachsende Wissens- und Automatisierungs-Basis, die mit dir lernt.

## Voraussetzungen

- Claude Max Account
- Visual Studio Code mit Claude Code Plugin (aktiviert)
- GitHub Account

## Erste 5 Minuten auf Windows

1. Erstelle ein leeres Arbeitsverzeichnis irgendwo auf deinem Rechner (z.B. `C:\Users\DeinName\aios`).
2. Öffne dieses Verzeichnis in VS Code.
3. Starte Claude Code im VS Code Sidebar.
4. Sag Claude Code in eigenen Worten, dass er dieses Repo (`https://github.com/SkillPilotCH/skillpilot-aios-starter`) hierhin klonen und den Git-Remote entfernen soll, weil das hier dein eigenes AIOS wird, kein Fork.
5. Sag dann: *"Bitte installier mir das Plugin `superpowers@claude-plugins-official` und erklär mir kurz, was ich damit mache."* (siehe nächste Sektion — gibt deinem Claude Code zusätzliche Skills für strukturiertes Arbeiten.)
6. Lass Claude Code `/onboard` aufrufen — das Interview befüllt dein Skelett mit deinem Kontext.
7. Wenn das durch ist, sag Claude Code: *"Erstell mir bitte ein privates GitHub-Repo unter meinem Account, push diesen Stand dahin und erklär mir kurz, was passiert ist."*

Das war's. Tastatur-Befehle nicht nötig — du delegierst, Claude Code übersetzt.

## Empfohlene Erweiterung: Superpowers

Das von Anthropic kuratierte Plugin [`superpowers`](https://github.com/obra/superpowers) gibt Claude Code zusätzliche Skills für strukturiertes Arbeiten — `brainstorming` (Design vor Code), `writing-plans` (Implementierungspläne), `test-driven-development`, `verification-before-completion`, `code-reviewer` und mehr.

Installation einfach in eigenen Worten an Claude Code delegieren (siehe Schritt 5 oben). Im Hintergrund läuft `/plugin install superpowers@claude-plugins-official`.

Das `CLAUDE.md` in diesem Repo verweist gezielt auf die wichtigsten Superpowers-Skills, sodass Claude Code sie automatisch nutzt, wenn das Plugin installiert ist.

## Die vier Cs in einem Satz

- **Context** — was die KI über dich weiss (`context/`)
- **Connections** — Live-Daten und Tools, die sie ohne Copy-Paste erreicht (`connections.md`)
- **Capabilities** — was sie auf Knopfdruck kann (`.claude/skills/`)
- **Cadence** — was autonom läuft, ohne dass du tippst (`cadence.md`)

## Die drei Skills

- `/onboard` — Initial-Interview entlang der vier Cs, befüllt das Skelett.
- `/audit` — 4-Cs-Gap-Report. Ab Tag 7, danach wöchentlich.
- `/level-up` — Eine Automatisierung pro Woche finden, scopen, shippen.

## Privatsphäre

**Privates GitHub-Repo heisst nicht vertrauliches Repo.** GitHub kann technisch lesen (Microsoft, US-Cloud). Bevor du sensitive Inhalte einträgst, lies die Sektion *"Was hier NICHT steht"* im `CLAUDE.md`. Faustregel: wenn es deinen Anwalt nervös machen würde, gehört es nicht hier rein.

## Inspiration

Inspired by Nate Herk's AI Operating System concept and the Four Cs framework. This template adapts the structure for German-speaking power users in the SkillPilot Cowork Enabling context.

## Lizenz

MIT.

---

## Anhang: Für Neugierige

Was Claude Code im Hintergrund tippt, wenn du ihn natursprachlich anweist:

```bash
# Schritt 4 (Klonen + Remote entfernen):
git clone https://github.com/SkillPilotCH/skillpilot-aios-starter .
git remote remove origin

# Schritt 6 (Eigenes privates Repo + Push):
gh repo create my-aios --private --source=. --remote=origin
git push -u origin main
```

**Hosting-Alternativen für Compliance-Sensitive:** [Codeberg](https://codeberg.org) (EU, non-profit), self-hosted [Gitea](https://gitea.io), [GitLab self-managed](https://about.gitlab.com/install/).
