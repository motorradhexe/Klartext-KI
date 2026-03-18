---
title: "MCP: Heute"
description: Was man beim Einsatz beachten muss, für wen MCP heute relevant ist und wie man einsteigt.
layout: default
parent: MCP – Model Context Protocol
grand_parent: Vertiefung
nav_order: 3
---

# MCP heute

## Was man dabei beachten muss

MCP erweitert, was KI-Modelle tun können. Damit wächst auch, was schiefgehen kann.

**Berechtigungen sind entscheidend.** Ein Modell, das Lese- und Schreibzugriff auf ein System hat, kann Fehler machen – und diese Fehler haben Konsequenzen. Wer MCP einsetzt, sollte genau definieren, welche Berechtigungen ein Server bekommt. Lesezugriff ist weniger riskant als Schreibzugriff. Zugriff auf Testumgebungen ist weniger riskant als Zugriff auf Produktionssysteme.

Das Prinzip: So wenig Berechtigung wie nötig – so viel, wie für die Aufgabe sinnvoll.

**Vertrauliche Daten können das System verlassen.** Wenn ein MCP-Server Dateien oder Datenbankeinträge liest und deren Inhalt in den [Kontext](../../glossar#kontext) des Modells übergibt, verlassen diese Daten das lokale System und gehen an den KI-Anbieter. Das ist derselbe Mechanismus wie beim manuellen Einkopieren von Text – nur dass er jetzt automatisch passiert, ohne dass man jeden Transfer bewusst wahrnimmt.

**Aktionen lassen sich nicht immer rückgängig machen.** Eine gelöschte Datei, eine gesendete E-Mail, ein überschriebenes Dokument – das sind Konsequenzen, die MCP-Server auslösen können, wenn das Modell einen Fehler macht. Vor allem bei Schreibzugriffen sollte man sich fragen: Was ist der schlimmste Fall, wenn hier etwas schiefgeht?

---

## Für wen das heute relevant ist

MCP ist in seiner aktuellen Form vor allem für Entwicklerinnen und Entwickler interessant, die KI in eigene Anwendungen einbetten – sowie für fortgeschrittene Nutzer, die Claude Desktop mit eigenen Integrationen erweitern.

Für Endanwender wird es zunehmend relevant, wenn Anwendungen MCP-Integrationen direkt als Einstellung anbieten – ohne Konfigurationsaufwand. Mehrere Anbieter arbeiten daran.

Die Frage, welche Daten man einem KI-System zugänglich macht und welche nicht, ist keine technische, sondern eine inhaltliche Entscheidung. MCP macht es leichter, diese Entscheidung umzusetzen. Sie abnehmen kann es nicht.

Mehr dazu, wie Agents diese Werkzeuge eigenständig einsetzen: [KI-Agents](../agents). Wie KI auf große eigene Wissensbestände zugreift: [RAG](../rag).
