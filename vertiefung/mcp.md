---
title: MCP – Model Context Protocol
description: Wie KI mit externen Werkzeugen und Datenquellen verbunden wird – und was MCP dabei ist.
layout: default
parent: Vertiefung
nav_order: 3
---

# MCP – Model Context Protocol

KI-Modelle sind gut darin, Text zu verarbeiten und zu erzeugen. Aber sie kennen nur das, was in ihrem [Kontext](../glossar#kontext) steht. Sie können keine Datei auf dem eigenen Computer öffnen, keine Datenbank abfragen, keinen Kalender lesen. Außer, man gibt ihnen die Möglichkeit dazu.

MCP ist ein Protokoll – also eine technische Vereinbarung –, das beschreibt, wie KI-Modelle mit externen Werkzeugen und Datenquellen sprechen können. Es wurde von Anthropic entwickelt und ist inzwischen offen: andere Hersteller und Entwickler können es verwenden.

---

## Was MCP ist

[MCP](../glossar#mcp) steht für Model Context Protocol. Es ist kein KI-Modell, keine Anwendung und kein Dienst. Es ist ein Standard – vergleichbar mit dem Standard, der festlegt, wie Browser und Webserver miteinander kommunizieren.

Der Standard beschreibt:
- Wie ein KI-Modell ein Werkzeug aufrufen kann (eine Datei lesen, eine Suche starten, eine Datenbank abfragen)
- Wie das Werkzeug antwortet
- Welche Informationen dabei ausgetauscht werden

Für Endanwender sieht das so aus: Man nutzt eine KI-Anwendung, und diese Anwendung kann auf Dateien, Kalender, Tickets, Datenbanken oder andere Systeme zugreifen – weil im Hintergrund MCP-Server laufen, die diese Verbindungen herstellen.

---

## Eine Analogie

Stellen Sie sich vor, Sie haben eine sehr fähige Assistentin. Sie kann vieles – aber nur, wenn man ihr Zugang zu den nötigen Informationen gibt. Bisher mussten Sie ihr alle Informationen mündlich mitteilen. Mit MCP ist es so, als hätte sie jetzt Schlüssel: zum Aktenschrank, zur Datenbank, zum Terminkalender.

Sie entscheidet immer noch, was sie damit macht. Aber sie muss nicht mehr fragen: „Können Sie mir die Datei zeigen?" – sie kann sie selbst öffnen.

---

## Warum das relevant ist

Ohne Anbindung an externe Systeme ist KI ein Werkzeug, das man manuell bedient: Text reinkopieren, Antwort rauskopieren, weiterverarbeiten. Das funktioniert, ist aber aufwändig.

Mit MCP können KI-Anwendungen direkt auf Daten zugreifen, die für eine Aufgabe relevant sind – ohne dass jemand sie manuell einfügen muss. Das verändert, was möglich ist:

- Eine KI, die auf das eigene Projektmanagementsystem zugreift und den Status aller offenen Aufgaben kennt
- Eine KI, die Kundendaten direkt aus der Datenbank liest, um eine Anfrage zu beantworten
- Eine KI, die ein Dokument auf dem lokalen Rechner öffnet, bearbeitet und speichert

Das sind keine Zukunftsszenarien. Es gibt MCP-Integrationen für viele gängige Systeme – von Dateisystemen über GitHub bis zu Notion.

---

## Was man dabei beachten muss

MCP erweitert, was KI-Modelle tun können. Damit wächst auch, was schiefgehen kann.

Ein Modell, das Lese- und Schreibzugriff auf ein System hat, kann Fehler machen – und diese Fehler haben Konsequenzen. Wer MCP einsetzt, sollte genau definieren, welche Berechtigungen ein Modell bekommt. Lesezugriff ist weniger riskant als Schreibzugriff. Zugriff auf unkritische Systeme ist weniger riskant als Zugriff auf Produktionsdatenbanken.

Das Prinzip: So wenig Berechtigung wie nötig, so viel wie für die Aufgabe sinnvoll.

---

## Für wen das heute relevant ist

MCP ist in seiner aktuellen Form vor allem für Entwicklerinnen und Entwickler interessant, die KI in eigene Anwendungen einbetten. Für Endanwender wird es zunehmend relevant, wenn Anwendungen wie Claude Desktop oder andere KI-Tools MCP-Integrationen direkt anbieten.

Das Grundprinzip – KI braucht Zugang zu relevanten Daten, um nützlich zu sein – gilt unabhängig von MCP. Die Frage, welche Daten man einem KI-System zugänglich macht und welche nicht, ist keine technische, sondern eine inhaltliche Entscheidung.

Mehr dazu, wie Agents diese Werkzeuge eigenständig einsetzen: [KI-Agents](agents). Wie KI auf große eigene Wissensbestände zugreift, ohne alles in den Kontext laden zu müssen: [RAG](rag). Welche Berechtigungen und Datenschutzfragen dabei relevant werden: [Risiken beim Einsatz von KI](risiken).
