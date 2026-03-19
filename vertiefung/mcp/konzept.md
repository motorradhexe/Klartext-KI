---
title: "MCP: Konzept & Aufbau"
description: Was MCP ist, wie ein MCP-System aus Client, Server und Modell aufgebaut ist, und warum ein Standard hier einen Unterschied macht.
layout: default
parent: MCP – Model Context Protocol
grand_parent: Vertiefung
nav_order: 1
---

# Konzept & Aufbau

## Was MCP ist

[MCP](../../glossar#mcp) steht für Model Context Protocol. Es ist kein KI-Modell, keine Anwendung und kein Dienst. Es ist ein Standard – vergleichbar mit dem Standard, der festlegt, wie Browser und Webserver miteinander kommunizieren.

Der Standard beschreibt, wie ein KI-Modell ein Werkzeug aufrufen kann, wie das Werkzeug antwortet und welche Informationen dabei ausgetauscht werden. MCP wurde von Anthropic entwickelt und ist offen: Andere Hersteller und Entwickler können es verwenden.

Der entscheidende Punkt: MCP macht diese Verbindungen einheitlich. Wer einen MCP-Server für ein System baut – etwa für GitHub –, kann diesen Server sofort mit jeder Anwendung nutzen, die MCP unterstützt. Du musst nicht für jede KI-Anwendung eine eigene Schnittstelle bauen.

---

## Eine Analogie

Stell Dir vor, Du hast eine sehr fähige Assistentin. Sie kann vieles – aber nur, wenn ihr Zugang zu den nötigen Informationen gegeben wird. Bisher musstest Du ihr alle Informationen mündlich mitteilen. Mit MCP ist es so, als hätte sie jetzt Schlüssel: zum Aktenschrank, zur Datenbank, zum Terminkalender.

Sie entscheidet immer noch, was sie damit macht. Aber sie muss nicht mehr fragen: „Kannst Du mir die Datei zeigen?" – sie kann sie selbst öffnen.

---

## Wie ein MCP-System aufgebaut ist

Ein MCP-System besteht aus drei Teilen:

**Der MCP-Client** ist die KI-Anwendung, die Werkzeuge nutzen will – zum Beispiel Claude Desktop oder eine selbst entwickelte Anwendung. Der Client fragt beim Server nach, welche Werkzeuge verfügbar sind.

**Der MCP-Server** ist ein kleines Programm, das ein bestimmtes System zugänglich macht. Es gibt MCP-Server für das lokale Dateisystem, für GitHub, für Notion, für Datenbanken, für Kalender. Der Server beschreibt gegenüber dem Client, was er kann – und führt Befehle aus, wenn der Client ihn aufruft.

**Das Modell** entscheidet, welches Werkzeug es für eine Aufgabe braucht, ruft den MCP-Server auf und verarbeitet das Ergebnis. Diese Entscheidung trifft es auf Basis des [Kontexts](../../glossar#kontext) – genau wie ein [Agent](../../glossar#agent).

Ein Beispiel: Jemand fragt Claude Desktop: „Zeig mir alle Python-Dateien, die ich in den letzten drei Tagen geändert habe." Das Modell ruft über MCP den Dateisystem-Server auf, dieser sucht nach den Dateien und gibt die Liste zurück. Das Modell fasst sie zusammen oder stellt weitere Fragen.
