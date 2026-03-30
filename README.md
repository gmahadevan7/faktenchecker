# Faktenchecker — KI-gestützter Faktenprüfer

Ein datenschutzfreundlicher, browserbasierter Faktenprüfer auf Basis von Claude AI. Keine Serverinstallation, keine Datenübertragung außer direkt zur Anthropic-API.

**[🚀 Live Demo](https://danielenki420.github.io/faktenchecker/)** — eigenen Anthropic API-Key mitbringen

![Lizenz: MIT](https://img.shields.io/badge/Lizenz-MIT-blue.svg)

---

## Was macht die App?

Du gibst eine Behauptung ein — die KI analysiert sie und gibt dir zurück:

- **Wahrheitsgehalt** (Wahr / Falsch / Teilweise wahr / Unbekannt / Meinung)
- **Konfidenz** in Prozent
- **Begründung** mit Quellhinweisen
- **Korrekte Version** der Aussage (wenn nötig)

---

## Features

- Streaming-Analyse mit Echtzeit-Vorschau
- **Vergleichsmodus**: zwei Behauptungen nebeneinander prüfen
- Prüfverlauf mit Filter nach Verdikt (lokal im Browser gespeichert)
- Eigene Beispiel-Chips (hinzufügen & löschen)
- Ergebnis teilen via URL (kodiert im Hash)
- PDF-Export via Drucken (`Strg/Cmd + P`)
- Dark Mode
- Sprachmodus: Auto-Erkennung oder Deutsch erzwingen
- Zugänglichkeit: vollständige ARIA-Unterstützung
- Kein Backend, kein Tracking, keine Cookies

---

## Schnellstart

### 1. API-Key besorgen

Erstelle einen kostenlosen Account und hole dir einen API-Key unter:
→ [console.anthropic.com](https://console.anthropic.com)

> Neue Accounts erhalten ein kostenloses Startguthaben.

### 2. App öffnen

Lade `faktenchecker.html` herunter und öffne die Datei direkt im Browser — ein Doppelklick reicht.

### 3. API-Key eingeben

Beim ersten Start erscheint ein Eingabefeld für den API-Key. Der Key wird nur lokal im Browser (`localStorage`) gespeichert und nirgends hochgeladen.

### 4. Behauptung prüfen

Text eingeben → „Prüfen" klicken → Ergebnis lesen.

---

## Datenschutz & Sicherheit

- Dein API-Key verlässt deinen Browser nur für direkte Anfragen an `api.anthropic.com`
- Es gibt keinen Zwischenserver
- Verlauf und Einstellungen bleiben lokal in deinem Browser
- Content Security Policy (CSP) verhindert unerwünschte externe Verbindungen
- Eingaben werden vor der Analyse gekapselt, um Prompt-Injection zu erschweren

---

## Technologie

| Bereich | Details |
|---|---|
| Frontend | Reines HTML/CSS/JavaScript (keine Frameworks) |
| KI-Modell | `claude-opus-4-5` via Anthropic API |
| Streaming | Server-Sent Events (SSE) |
| Persistenz | `localStorage` (lokal, kein Server) |
| Styling | CSS Custom Properties, Dark Mode |
| Sicherheit | CSP, `esc()` XSS-Schutz, Prompt-Injection-Wrapper |

---

## Systemanforderungen

- Moderner Browser (Chrome, Firefox, Safari, Edge)
- Aktive Internetverbindung (für die API-Anfragen)
- Anthropic API-Key

---

## Mitentwickeln

Pull Requests sind willkommen! Bitte halte dich an folgende Grundsätze:

- Kein API-Key im Code
- Kein externes CDN oder Framework
- Alles bleibt in einer einzigen HTML-Datei
- Sicherheit und Barrierefreiheit haben Vorrang

---

## Lizenz

[MIT](LICENSE) — freie Nutzung, Weitergabe und Modifikation erlaubt.
