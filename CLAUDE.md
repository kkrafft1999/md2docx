# CLAUDE.md

Guide for AI assistants working on this repository.

## Project Overview

**md2docx** ist eine interne Webanwendung zur Konvertierung von Markdown in Microsoft Word (.docx) Dokumente. Das Projekt wird als Angular-Anwendung mit TypeScript und einem Backend realisiert.

- **Typ:** Internes Tool (kein öffentliches Produkt)
- **Sprache der UI:** Deutsch
- **Architektur:** Client-Server (Angular Frontend + Backend)

## Anforderungen

### Funktionale Anforderungen

**Markdown-Eingabe:**
- Markdown-Text über einen Editor/Textarea eingeben
- `.md`-Dateien per Datei-Upload hochladen
- Keine Live-Vorschau erforderlich

**Markdown-Unterstützung:**
- Überschriften (H1–H6)
- Fließtext mit Inline-Formatierung (fett, kursiv, durchgestrichen)
- Listen (geordnet und ungeordnet, verschachtelt)
- Code-Blöcke und Inline-Code
- Links
- Bilder (werden ins DOCX eingebettet)
- Tabellen
- Blockzitate

**DOCX-Konvertierung:**
- Serverseitige Konvertierung (im Backend)
- Saubere Formatierung mit Word-Styles
- Bilder aus dem Markdown werden ins DOCX-Dokument eingebettet
- Fertige .docx-Datei zum Download bereitstellen

**Styling-Optionen:**
- Nutzer kann Formatierungsoptionen wählen (z.B. Schriftart, Schriftgröße, Farben, Seitenränder)
- Optional: Vorlagen/Templates für wiederkehrende Dokument-Layouts

### Nicht-funktionale Anforderungen

- Performante Konvertierung auch bei größeren Dokumenten
- Responsive UI für Desktop-Nutzung
- Deutsche Benutzeroberfläche (Labels, Fehlermeldungen, Tooltips)

## Planned Technology Stack

- **Frontend:** Angular mit TypeScript
- **Backend:** Noch zu definieren (z.B. Node.js/Express, NestJS, oder ähnliches)
- **Package Manager:** npm oder yarn (beide Lock-Dateien sind gitignored)
- **Build Output:** `/dist/`

## Repository Status

Dieses Repository ist frisch initialisiert. Es existiert noch kein Quellcode, keine Build-Konfiguration und keine Dependencies.

## Project Structure

```
md2docx/
├── .gitignore          # Angular/Node/TypeScript Ignore-Patterns
├── README.md           # Projektbeschreibung
└── CLAUDE.md           # Diese Datei
```

Geplante Struktur nach Scaffolding:
- `src/` - Frontend-Quellcode (Angular)
- `src/app/` - Angular Components, Services, Modules
- `src/assets/` - Statische Assets
- `server/` oder `backend/` - Backend-Quellcode (noch zu definieren)
- `angular.json` - Angular CLI Konfiguration
- `tsconfig.json` - TypeScript Konfiguration
- `package.json` - Dependencies und Scripts

## Build and Development Commands

Noch kein Build-System konfiguriert. Nach dem Scaffolding:

```bash
npm install          # Dependencies installieren
ng serve             # Dev-Server starten
ng build             # Production Build
ng test              # Unit-Tests ausführen
ng e2e               # End-to-End-Tests ausführen
ng lint              # Linter ausführen
```

## Key Conventions

- **Environment files:** `.env` ist gitignored; keine Secrets committen
- **Lock files:** Sowohl `package-lock.json` als auch `yarn.lock` sind gitignored
- **Build artifacts:** `/dist/`, `/out-tsc/`, `/tmp/` sind gitignored
- **Sprache:** UI und Nutzertexte auf Deutsch, Code und Kommentare auf Englisch

## Git Workflow

- **Main branch:** `main`
- **Remote:** origin
- Feature-Branches von `main` abzweigen
- Klare, beschreibende Commit-Messages

## Setup Instructions

Beim Initialisieren des Angular-Projekts:

1. Angular CLI installieren: `npm install -g @angular/cli`
2. Projekt generieren: `ng new md2docx --directory .` (im bestehenden Repo)
3. Dependencies installieren: `npm install`
4. Markdown-Parsing-Library hinzufügen (z.B. `marked`, `markdown-it`)
5. DOCX-Generierungs-Library hinzufügen (z.B. `docx`, `html-docx-js`)
6. Backend-Framework aufsetzen

## Notes for AI Assistants

- Bestehende Dateien lesen bevor Änderungen gemacht werden
- Tests ausführen nach Änderungen, sofern eine Test-Suite existiert
- Keine `.env`-Dateien oder Secrets committen
- Angular Style Guide und bestehende Projekt-Konventionen einhalten
- Konvertierungslogik (Markdown-Parsing, DOCX-Generierung) in eigene Services auslagern, getrennt von UI-Komponenten
- UI-Texte auf Deutsch, Code und Kommentare auf Englisch
