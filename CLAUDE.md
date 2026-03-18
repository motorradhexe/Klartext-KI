# CLAUDE.md – Klartext KI

Dieses Dokument beschreibt Ziel, Struktur und Konventionen des Projekts.
Es gilt als verbindliche Arbeitsgrundlage für alle Aufgaben in diesem Repository.

**Status:** Projekt ist vollständig aufgebaut und live auf GitHub Pages.
Neue Aufgaben betreffen Pflege, Erweiterung und Qualitätsverbesserung bestehender Inhalte.

---

## Projektziel

**Klartext KI** ist ein öffentliches, deutschsprachiges Lernprojekt für Menschen,
die KI bereits ausprobiert haben – aber enttäuscht waren.

Das Ziel: Erklären, warum KI bisher nicht funktioniert hat – und zeigen,
wie man konkret besser damit arbeitet. Für verschiedene Zwecke, mit echten Beispielen,
ohne Hype, ohne Versprechen.

---

## Zielgruppe

Menschen, die:
- KI schon genutzt haben (ChatGPT, Copilot o. ä.)
- mit den Ergebnissen unzufrieden waren
- nicht verstehen, woran es gelegen hat
- lernen wollen, wie man KI wirklich produktiv einsetzt

Technisches Vorwissen: keins vorausgesetzt.
Beruflicher Hintergrund: beliebig.

---

## Ton und Inhaltsprinzipien

- **Direkt.** Keine Füllsätze, keine Einleitungsfloskeln.
- **Ehrlich.** KI-Grenzen werden klar benannt, nicht wegmoderiert.
- **Konkret.** Jede Aussage wird mit einem Beispiel belegt oder ist ohne Beispiel nicht nötig.
- **Ohne Hype.** Keine Superlative, keine Versprechen, keine Buzzword-Dichte.
- **Lehrend, nicht listend.** Jedes Modul erklärt, *wie* man KI einsetzt – nicht nur, wofür.

Sprache: ausschließlich Deutsch.
Fachbegriffe auf Englisch (Prompt, Token, Kontext) werden beim ersten Auftreten
kurz erklärt und im Glossar vollständig dokumentiert.

---

## Techstack

- **Statischer Site-Generator:** Jekyll (nativ von GitHub Pages unterstützt)
- **Inhalte:** Markdown (`.md`)
- **Styling:** Eigenes CSS – kein UI-Framework, kein Tailwind
- **Deployment:** GitHub Pages – kein Build-Schritt, kein Workflow nötig
- **JavaScript:** Nur wo zwingend nötig

### Warum Jekyll?

GitHub Pages baut Jekyll-Projekte automatisch beim Push – ohne GitHub Actions,
ohne lokales Build-Setup, ohne Konfigurationsaufwand.
Ziel ist: Fork, Inhalt anpassen, pushen – fertig.

---

## Projektstruktur

```
klartext-ki/
├── CLAUDE.md                  # Diese Datei
├── README.md                  # Kurze Projektbeschreibung für GitHub
├── _config.yml                # Jekyll-Konfiguration
│
├── index.md                   # Startseite
├── glossar.md                 # Glossar aller Fachbegriffe
├── ressourcen.md              # Weiterführende Lernmaterialien
│
├── kern/                      # Kernmodule (für alle, sequenziell)
│   ├── 01-warum-ki-enttaeuscht.md
│   ├── 02-wie-ki-funktioniert.md
│   └── 03-kontext-ist-alles.md
│
├── arbeiten-mit-ki/           # Lernpfade (modular, unabhängig)
│   ├── schreiben.md
│   ├── verstehen.md
│   ├── strukturieren.md
│   ├── entwickeln.md
│   └── erklaeren.md
│
├── vertiefung/                # Weiterführende Themen (optional)
│   ├── agents.md
│   ├── rag.md
│   └── mcp.md
│
├── _layouts/
│   ├── default.html
│   └── modul.html
│
└── assets/
    └── css/
        └── main.css
```

---

## Inhaltsstruktur

### Kernmodule (3 Module, sequenziell)

Jeder durchläuft sie zuerst. Sie bauen aufeinander auf.

| Modul | Titel | Kernaussage |
|-------|-------|-------------|
| K-01 | Warum KI oft enttäuscht | Das Problem liegt meist nicht an der KI |
| K-02 | Wie KI eigentlich funktioniert | Das Minimum, das den Unterschied macht |
| K-03 | Kontext ist alles | Warum Eingaben entscheidender sind als das Modell |

### Lernpfade: Mit KI arbeiten (modular, unabhängig voneinander)

**Jeder Lernpfad folgt derselben Struktur:**

1. **Wofür eignet sich KI hier – und wofür nicht?**
   Ehrliche Einschätzung, keine Werbung.

2. **Wie geht man es an?**
   Konkrete Methode: Wie formuliert man die Eingabe, welchen Kontext braucht KI,
   wie iteriert man auf ein brauchbares Ergebnis?

3. **Typische Fehler – und warum sie passieren**
   Was schiefgeht, wenn man es intuitiv versucht.

4. **Beispiel: Vorher / Nachher**
   Ein schlechter Prompt, ein besserer Prompt, Erklärung des Unterschieds.

5. **Zum Ausprobieren**
   Eine konkrete Übung, die man sofort umsetzen kann.

| Lernpfad | Inhalt |
|----------|--------|
| Schreiben | Wie man mit KI Texte, Mails und Dokumentation erarbeitet |
| Verstehen | Wie man KI nutzt, um komplexe Themen zu durchdringen |
| Strukturieren | Wie man mit KI Ideen ordnet und Entscheidungen vorbereitet |
| Entwickeln | Wie man mit KI Code versteht, schreibt und überprüft |
| Erklären | Wie man mit KI Präsentationen und Übergaben vorbereitet |

### Vertiefungsthemen (optional, für Interessierte)

Keine Voraussetzung für die Lernpfade. Für Menschen, die tiefer einsteigen wollen.

| Seite | Inhalt |
|-------|--------|
| agents.md | Was KI-Agents sind, was sie können und wo sie scheitern |
| rag.md | Wie KI mit eigenem Wissen und Dokumenten arbeitet (RAG) |
| mcp.md | Wie KI mit externen Werkzeugen verbunden wird (MCP) |

### Ressourcen

`ressourcen.md` – Weiterführende, kostenfreie Lernmaterialien der großen KI-Anbieter.
Keine Werbung, keine Partnerlinks. Nur geprüfte Einstiegsangebote.

### Glossar

Eine eigene Seite (`glossar.md`) mit allen Fachbegriffen, die im Projekt vorkommen.
Jeder Begriff wird erklärt, ohne Vorwissen vorauszusetzen.
Aus jedem Modul wird beim ersten Auftreten eines Begriffs auf den Glossareintrag verlinkt.

Dokumentierte Begriffe: Prompt, Token, Kontext, Kontextfenster, Sprachmodell, Training, Modell, Halluzination, Iteration, Ausgabe, Agent, RAG, MCP, Framework, Import, Docstring

---

## Dateikonventionen

- Dateinamen: Kleinbuchstaben, Bindestriche statt Leerzeichen
- Keine Umlaute in Dateinamen (ä → ae, ö → oe, ü → ue, ß → ss)
- Frontmatter: Jede Markdown-Datei hat `title`, `description`, `layout`, `nav_order`
- Bilder: Nur wenn sie echten Mehrwert haben

### Frontmatter-Beispiel

```yaml
---
title: Warum KI oft enttäuscht
description: Die häufigsten Gründe, warum KI-Ergebnisse enttäuschen – und was dahintersteckt.
layout: modul
nav_order: 1
---
```

---

## Was Claude Code in diesem Projekt tun soll

- Bestehende Inhalte überarbeiten, präzisieren und qualitativ verbessern
- Neue Lernpfade oder Vertiefungsseiten nach den definierten Strukturvorgaben erstellen
- Glossar pflegen: neue Begriffe ergänzen, Verlinkungen aus Modulen sicherstellen
- CSS anpassen: klar, lesbar, kein Framework-Look
- Navigation und interne Verlinkung konsistent halten
- Ressourcenseite aktuell halten

## Was Claude Code in diesem Projekt nicht tun soll

- Keine Inhalte mit Hype-Sprache
- Keine KI-Fähigkeiten übertreiben oder verharmlosen
- Keinen JavaScript-Framework-Overhead einführen
- Keine externen Abhängigkeiten ohne explizite Freigabe
- Keine englischsprachigen Inhalte
- Keine Aufzählungen, wo Erklärungen gebraucht werden

---

## Qualitätskriterien für Inhalte

Bevor ein Modul als fertig gilt:

- [ ] Das Modul erklärt, *wie* man vorgeht – nicht nur, dass es möglich ist
- [ ] Es gibt mindestens ein konkretes Vorher/Nachher-Beispiel
- [ ] KI-Grenzen werden benannt
- [ ] Kein Fachbegriff ohne Erklärung oder Glossar-Link
- [ ] Der Text funktioniert ohne Vorwissen aus anderen Lernpfaden
- [ ] Kein Satz, der ohne Substanzverlust weggelassen werden könnte

---

## Lizenz

Inhalte: [Creative Commons BY 4.0](https://creativecommons.org/licenses/by/4.0/)
Code: MIT

Ziel ist maximale Nachnutzbarkeit. Beiträge willkommen.
