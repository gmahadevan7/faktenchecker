# Faktenchecker — KI-gestützter Faktenprüfer

Ein datenschutzfreundlicher, browserbasierter Faktenprüfer auf Basis von Claude AI. Keine Serverinstallation, keine Datenübertragung außer direkt zur Anthropic-API.

**[🚀 Live Demo](https://danielenki420.github.io/faktenchecker/)** — eigenen Anthropic API-Key mitbringen

![Lizenz: MIT](https://img.shields.io/badge/Lizenz-MIT-blue.svg)

---

> 🇬🇧 [English version below](#english)

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
- UI-Sprache: Deutsch / Englisch
- Analysemodus: Sprache auto-erkennen oder erzwingen
- Zugänglichkeit: vollständige ARIA-Unterstützung
- Kein Backend, kein Tracking, keine Cookies

---

## Schnellstart

### 1. API-Key besorgen

Erstelle einen kostenlosen Account und hole dir einen API-Key unter:
→ [console.anthropic.com](https://console.anthropic.com)

> Neue Accounts erhalten ein kostenloses Startguthaben.

### 2. App öffnen

**Option A — Live:** [danielenki420.github.io/faktenchecker](https://danielenki420.github.io/faktenchecker/)

**Option B — Lokal:** `faktenchecker.html` herunterladen und direkt im Browser öffnen — kein Server nötig.

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
| KI-Modell | `claude-sonnet-4-6` via Anthropic API |
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

---
---

<a name="english"></a>

# Faktenchecker — AI-powered Fact Checker

A privacy-friendly, browser-based fact checker powered by Claude AI. No server required — data is sent directly to the Anthropic API only.

**[🚀 Live Demo](https://danielenki420.github.io/faktenchecker/)** — bring your own Anthropic API key

![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)

---

## What does it do?

Enter a claim — the AI analyses it and returns:

- **Verdict** (True / False / Partially True / Unverifiable / Opinion)
- **Confidence** percentage
- **Reasoning** with source hints
- **Corrected version** of the statement (if needed)

---

## Features

- Streaming analysis with real-time preview
- **Comparison mode**: check two claims side by side
- Analysis history with filter by verdict (stored locally in browser)
- Custom example chips (add & delete)
- Share results via URL (hash-encoded)
- PDF export via Print (`Ctrl/Cmd + P`)
- Dark mode
- UI language: German / English
- Analysis language: auto-detect or force language
- Full ARIA accessibility support
- No backend, no tracking, no cookies

---

## Quick Start

### 1. Get an API Key

Create a free account and get your API key at:
→ [console.anthropic.com](https://console.anthropic.com)

> New accounts receive a free starting credit.

### 2. Open the app

**Option A — Live:** [danielenki420.github.io/faktenchecker](https://danielenki420.github.io/faktenchecker/)

**Option B — Local:** Download `faktenchecker.html` and open it directly in your browser — no server needed.

### 3. Enter your API Key

On first launch, an input field appears for your API key. The key is stored only in your browser's `localStorage` and is never uploaded anywhere.

### 4. Check a claim

Enter text → click "Check now" → read the result.

---

## Privacy & Security

- Your API key only leaves your browser for direct requests to `api.anthropic.com`
- There is no intermediate server
- History and settings stay local in your browser
- Content Security Policy (CSP) blocks unwanted external connections
- User input is wrapped before analysis to prevent prompt injection

---

## Tech Stack

| Area | Details |
|---|---|
| Frontend | Pure HTML/CSS/JavaScript (no frameworks) |
| AI Model | `claude-sonnet-4-6` via Anthropic API |
| Streaming | Server-Sent Events (SSE) |
| Persistence | `localStorage` (local, no server) |
| Styling | CSS Custom Properties, Dark Mode |
| Security | CSP, `esc()` XSS protection, prompt injection wrapper |

---

## Requirements

- Modern browser (Chrome, Firefox, Safari, Edge)
- Active internet connection (for API requests)
- Anthropic API key

---

## Contributing

Pull requests are welcome! Please follow these principles:

- No API key in the code
- No external CDN or framework
- Everything stays in a single HTML file
- Security and accessibility take priority

---

## License

[MIT](LICENSE) — free to use, share, and modify.
