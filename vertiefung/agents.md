---
title: KI-Agents
description: Was Agents sind, wie sie funktionieren und wo ihre Grenzen liegen.
layout: modul
nav_order: 30
---

# KI-Agents

Ein einzelner [Prompt](/glossar#prompt) – Frage stellen, Antwort lesen, fertig. So sieht die Grundnutzung von KI aus. Agents gehen einen Schritt weiter: Sie führen Aufgaben eigenständig aus, treffen Zwischenentscheidungen und nutzen Werkzeuge – ohne dass ein Mensch jeden Schritt manuell auslöst.

Das klingt nach Science-Fiction. Es ist es nicht mehr. Aber es ist auch noch kein zuverlässig funktionierendes Werkzeug für alle Aufgaben.

---

## Was ein Agent ist

Ein Agent ist ein KI-System, das nicht nur antwortet, sondern handelt. Es bekommt ein Ziel – und arbeitet dann selbstständig daran, dieses Ziel zu erreichen. Dabei kann es:

- Werkzeuge nutzen (eine Websuche starten, eine Datei lesen, eine E-Mail schicken)
- Zwischenergebnisse bewerten und den nächsten Schritt planen
- Bei Bedarf weitere KI-Modelle oder Dienste aufrufen
- Das Ergebnis prüfen und bei Bedarf einen neuen Versuch starten

Ein klassisches Beispiel: Ein Agent bekommt den Auftrag „Recherchiere die drei günstigsten Anbieter für Serverhosting in Deutschland und erstelle eine Vergleichstabelle." Er sucht selbstständig im Web, liest Seiten, extrahiert Preise, formatiert die Tabelle – und liefert das Ergebnis.

Der Unterschied zur normalen KI-Nutzung: Man gibt nicht jede Zwischenfrage ein. Der Agent entscheidet selbst, welche Schritte nötig sind.

---

## Wie Agents funktionieren

Ein Agent ist im Kern ein [Modell](/glossar#modell), das in einer Schleife arbeitet. Der Ablauf sieht vereinfacht so aus:

1. Das Modell bekommt ein Ziel und eine Beschreibung verfügbarer Werkzeuge.
2. Es entscheidet, welchen nächsten Schritt es unternimmt – und ob es ein Werkzeug braucht.
3. Das Werkzeug wird ausgeführt, das Ergebnis kommt zurück in den [Kontext](/glossar#kontext) des Modells.
4. Das Modell bewertet das Ergebnis und entscheidet, ob das Ziel erreicht ist oder weitere Schritte folgen.

Diese Schleife läuft so lange, bis das Modell entscheidet, dass die Aufgabe erledigt ist – oder bis ein vordefiniertes Limit erreicht wird.

Das Entscheidende: Das Modell plant nicht wie ein Mensch. Es wählt jeweils den nächsten wahrscheinlichen Schritt auf Basis dessen, was im Kontext steht. Das funktioniert gut für strukturierte, gut definierte Aufgaben. Bei vagen Zielen oder unerwarteten Situationen kann es schiefgehen.

---

## Was Agents können – und was nicht

**Gut geeignet:**
- Wiederkehrende, klar definierte Aufgaben mit bekannten Schritten
- Aufgaben, die mehrere Werkzeuge kombinieren (suchen, zusammenfassen, formatieren)
- Prozesse, bei denen viele Einzelschritte zu viel manuelle Arbeit wären

**Noch nicht zuverlässig:**
- Aufgaben, bei denen ein Fehler in Schritt 3 alle weiteren Schritte fehlerhaft macht
- Situationen, die menschliches Urteilsvermögen erfordern (ethische Abwägungen, unklare Anforderungen)
- Alles, was in der realen Welt schwer rückgängig zu machen ist – ein gesendetes E-Mail, eine gelöschte Datei

Das größte Risiko bei Agents ist nicht, dass sie zu wenig tun – sondern dass sie zu viel tun, bevor jemand bemerkt, dass etwas falsch läuft. Wer Agents einsetzt, sollte definieren, was sie dürfen und was nicht.

---

## Was das für die Praxis bedeutet

Agents sind kein Selbstzweck. Sie sind nützlich, wenn eine Aufgabe aus vielen Schritten besteht, die sich klar beschreiben lassen und die wiederholt vorkommen.

Wer heute mit Agents arbeiten will, braucht dafür Programmierkenntnisse oder spezialisierte Plattformen. Die meisten einfachen Anwendungen – ein Dokument schreiben, einen Text überarbeiten, eine Frage beantworten – brauchen keine Agents. Da reicht ein guter Prompt.

Agents werden relevanter, je mehr KI in Arbeitsprozesse eingebettet wird. Das Verständnis, wie sie funktionieren und wo sie scheitern, ist schon jetzt nützlich.

Wie KI mit externen Werkzeugen verbunden wird, erklärt [MCP](/vertiefung/mcp). Wie KI auf eigene Wissensdatenbanken zugreift, erklärt [RAG](/vertiefung/rag).
