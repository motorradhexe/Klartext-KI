---
title: "Agents: Einsatz & Grenzen"
description: Wofür Agents gut geeignet sind, wo sie zuverlässig scheitern und welche Fehler immer wieder auftreten.
layout: default
parent: KI-Agents
grand_parent: Vertiefung
nav_order: 2
---

# Einsatz & Grenzen

## Was Agents können – und was nicht

Agents sind nützlich, wenn eine Aufgabe aus vielen klar beschreibbaren Einzelschritten besteht, die sich wiederholen oder zu aufwändig für manuelle Ausführung wären.

**Gut geeignet:**
- Wiederkehrende, klar definierte Aufgaben mit bekannten Schritten
- Aufgaben, die mehrere Werkzeuge kombinieren (suchen, zusammenfassen, formatieren, speichern)
- Prozesse, bei denen sehr viele Einzelschritte zusammenkommen, die alle für sich trivial sind

**Noch nicht zuverlässig:**
- Aufgaben, bei denen ein Fehler in frühen Schritten alle späteren Schritte vergiftet
- Situationen, die menschliches Urteilsvermögen erfordern – ethische Abwägungen, Ton in Kommunikation, Ausnahmen von Regeln
- Alles, was in der realen Welt schwer rückgängig zu machen ist: eine gesendete E-Mail, eine gelöschte Datei, eine ausgelöste Transaktion

Das größte Risiko bei Agents ist nicht, dass sie zu wenig tun – sondern dass sie zu viel tun, bevor jemand bemerkt, dass etwas falsch läuft.

---

## Typische Fehler – und warum sie passieren

**Der Agent arbeitet in die falsche Richtung.** Das Ziel war zu vage formuliert, und das Modell hat eine Interpretation gewählt, die plausibel klingt, aber nicht gemeint war. Konkrete Ziele, klare Abbruchkriterien und ein Beispiel des gewünschten Ergebnisses helfen.

**Fehler pflanzen sich fort.** Ein Agent, der in Schritt 2 eine falsche Annahme macht, baut in Schritt 3, 4 und 5 darauf auf. Am Ende ist das Ergebnis komplett falsch – und ohne die Zwischenschritte zu lesen, fällt das nicht auf. Wer Agents einsetzt, sollte die Zwischenschritte überprüfen, nicht nur das Endergebnis.

**Der Agent dreht im Kreis.** Manche Implementierungen haben kein robustes Abbruchkriterium. Der Agent startet immer neue Suchen oder Versuche, kommt aber nie zu einem Abschluss. Gute Agent-Systeme haben ein explizites Schritt-Limit – und halten es ein.

**Der Agent tut zu viel.** Wenn ein Agent Schreibzugriff auf ein System hat und einen Fehler macht, kann das Konsequenzen haben, die schwer rückgängig zu machen sind. Lesezugriff ist sicherer als Schreibzugriff. Für kritische Systeme sollte immer ein Mensch den letzten Schritt genehmigen – bevor die Aktion ausgeführt wird, nicht danach.
