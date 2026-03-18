---
title: MCP – Model Context Protocol
description: Wie KI mit externen Werkzeugen und Datenquellen verbunden wird – was MCP ist, wie es funktioniert und was es bedeutet.
layout: default
parent: Vertiefung
nav_order: 3
---

# MCP – Model Context Protocol

KI-Modelle sind gut darin, Text zu verarbeiten und zu erzeugen. Aber sie kennen nur das, was in ihrem [Kontext](../glossar#kontext) steht. Sie können keine Datei auf dem eigenen Computer öffnen, keine Datenbank abfragen, keinen Kalender lesen – außer, man gibt ihnen die Möglichkeit dazu.

[MCP](../glossar#mcp) ist ein Protokoll – also eine technische Vereinbarung –, das beschreibt, wie KI-Modelle mit externen Werkzeugen und Datenquellen sprechen können. Es wurde von Anthropic entwickelt und ist offen: Andere Hersteller und Entwickler können es verwenden.

---

## Was MCP ist

MCP steht für Model Context Protocol. Es ist kein KI-Modell, keine Anwendung und kein Dienst. Es ist ein Standard – vergleichbar mit dem Standard, der festlegt, wie Browser und Webserver miteinander kommunizieren.

Der Standard beschreibt:
- Wie ein KI-Modell ein Werkzeug aufrufen kann (eine Datei lesen, eine Suche starten, eine Datenbank abfragen)
- Wie das Werkzeug antwortet
- Welche Informationen dabei ausgetauscht werden

Der entscheidende Punkt: MCP macht diese Verbindungen einheitlich. Wer einen MCP-Server für ein System baut – sagen wir, für GitHub –, kann diesen Server sofort mit jeder Anwendung nutzen, die MCP unterstützt. Man muss nicht für jede KI-Anwendung eine eigene Schnittstelle bauen.

---

## Eine Analogie

Stellen Sie sich vor, Sie haben eine sehr fähige Assistentin. Sie kann vieles – aber nur, wenn man ihr Zugang zu den nötigen Informationen gibt. Bisher mussten Sie ihr alle Informationen mündlich mitteilen. Mit MCP ist es so, als hätte sie jetzt Schlüssel: zum Aktenschrank, zur Datenbank, zum Terminkalender.

Sie entscheidet immer noch, was sie damit macht. Aber sie muss nicht mehr fragen: „Können Sie mir die Datei zeigen?" – sie kann sie selbst öffnen.

---

## Wie ein MCP-System aufgebaut ist

Ein MCP-System besteht aus drei Teilen:

**Der MCP-Client** ist die KI-Anwendung, die Werkzeuge nutzen will – zum Beispiel Claude Desktop oder eine selbst entwickelte Anwendung. Der Client fragt beim Server nach, welche Werkzeuge verfügbar sind.

**Der MCP-Server** ist ein kleines Programm, das ein bestimmtes System zugänglich macht. Es gibt MCP-Server für das lokale Dateisystem, für GitHub, für Notion, für Datenbanken, für Kalender. Der Server beschreibt gegenüber dem Client, was er kann – und führt Befehle aus, wenn der Client ihn aufruft.

**Das Modell** entscheidet, welches Werkzeug es für eine Aufgabe braucht, ruft den MCP-Server auf und verarbeitet das Ergebnis. Diese Entscheidung trifft es auf Basis des Kontexts – genau wie ein [Agent](../glossar#agent).

Ein Beispiel: Jemand fragt Claude Desktop: „Zeig mir alle Python-Dateien, die ich in den letzten drei Tagen geändert habe." Das Modell ruft über MCP den Dateisystem-Server auf, dieser sucht nach den Dateien und gibt die Liste zurück. Das Modell fasst sie zusammen oder stellt weitere Fragen.

---

## Was es heute schon gibt

MCP hat sich seit seiner Einführung Ende 2024 schnell verbreitet. Es gibt MCP-Server für eine Vielzahl von Systemen:

**Entwicklung:** GitHub (Issues, Pull Requests, Code lesen), lokales Dateisystem, Code-Ausführung, Paketmanager

**Produktivität:** Notion, Google Docs, Kalender, E-Mail

**Daten:** SQL-Datenbanken, Tabellenkalkulationen, APIs verschiedener Dienste

**Suche und Web:** Websuche, Browser-Steuerung, Scraping

Wer Claude Desktop installiert hat, kann MCP-Server mit wenig Aufwand konfigurieren. Die Einrichtung erfordert grundlegende technische Kenntnisse – man muss eine Konfigurationsdatei bearbeiten –, aber kein Programmieren.

---

## Warum das relevant ist

Ohne Anbindung an externe Systeme ist KI ein Werkzeug, das man manuell bedient: Text reinkopieren, Antwort rauskopieren, weiterverarbeiten. Das funktioniert, ist aber aufwändig.

Mit MCP können KI-Anwendungen direkt auf Daten zugreifen, die für eine Aufgabe relevant sind – ohne dass jemand sie manuell einfügen muss. Das verändert, was möglich ist:

- Eine KI, die auf das eigene Projektmanagementsystem zugreift und den Status aller offenen Aufgaben kennt
- Eine KI, die Kundendaten direkt aus der Datenbank liest, um eine Anfrage zu beantworten
- Eine KI, die ein Dokument auf dem lokalen Rechner öffnet, bearbeitet und speichert
- Eine KI, die in einer GitHub-Codebasis navigiert und Zusammenhänge erklärt, ohne dass man Dateien manuell einkopiert

Das sind keine Zukunftsszenarien. Es gibt MCP-Integrationen für alle genannten Systeme, und sie werden aktiv genutzt.

---

## Was man dabei beachten muss

MCP erweitert, was KI-Modelle tun können. Damit wächst auch, was schiefgehen kann.

**Berechtigungen sind entscheidend.** Ein Modell, das Lese- und Schreibzugriff auf ein System hat, kann Fehler machen – und diese Fehler haben Konsequenzen. Wer MCP einsetzt, sollte genau definieren, welche Berechtigungen ein Server bekommt. Lesezugriff ist weniger riskant als Schreibzugriff. Zugriff auf Testumgebungen ist weniger riskant als Zugriff auf Produktionssysteme.

Das Prinzip: So wenig Berechtigung wie nötig – so viel, wie für die Aufgabe sinnvoll.

**Vertrauliche Daten können das System verlassen.** Wenn ein MCP-Server Dateien oder Datenbankeinträge liest und deren Inhalt in den Kontext des Modells übergibt, verlassen diese Daten das lokale System und gehen an den KI-Anbieter. Das ist derselbe Mechanismus wie beim manuellen Einkopieren von Text – nur dass er jetzt automatisch passiert, ohne dass man jeden Transfer bewusst wahrnimmt.

**Aktionen lassen sich nicht immer rückgängig machen.** Eine gelöschte Datei, eine gesendete E-Mail, ein überschriebenes Dokument – das sind Konsequenzen, die MCP-Server auslösen können, wenn das Modell einen Fehler macht. Vor allem bei Schreibzugriffen sollte man sich fragen: Was ist der schlimmste Fall, wenn hier etwas schiefgeht?

---

## Für wen das heute relevant ist

MCP ist in seiner aktuellen Form vor allem für Entwicklerinnen und Entwickler interessant, die KI in eigene Anwendungen einbetten – sowie für fortgeschrittene Nutzer, die Claude Desktop mit eigenen Integrationen erweitern.

Für Endanwender wird es zunehmend relevant, wenn Anwendungen MCP-Integrationen direkt als Einstellung anbieten – ohne Konfigurationsaufwand. Mehrere Anbieter arbeiten daran.

Das Grundprinzip – KI braucht Zugang zu relevanten Daten, um nützlich zu sein – gilt unabhängig von MCP. Die Frage, welche Daten man einem KI-System zugänglich macht und welche nicht, ist keine technische, sondern eine inhaltliche Entscheidung. MCP macht es leichter, diese Entscheidung umzusetzen. Sie abnehmen kann es nicht.

Mehr dazu, wie Agents diese Werkzeuge eigenständig einsetzen: [KI-Agents](agents). Wie KI auf große eigene Wissensbestände zugreift, ohne alles in den Kontext laden zu müssen: [RAG](rag).
