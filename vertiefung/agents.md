---
title: KI-Agents
description: Was Agents sind, wie sie funktionieren, wo sie scheitern – und was das für den praktischen Einsatz bedeutet.
layout: default
parent: Vertiefung
nav_order: 1
---

# KI-Agents

Ein einzelner [Prompt](../glossar#prompt) – Frage stellen, Antwort lesen, fertig. So sieht die Grundnutzung von KI aus. Agents gehen einen Schritt weiter: Sie führen Aufgaben eigenständig aus, treffen Zwischenentscheidungen und nutzen Werkzeuge – ohne dass ein Mensch jeden Schritt manuell auslöst.

Das klingt nach Science-Fiction. Es ist es nicht mehr. Aber es ist auch noch kein zuverlässig funktionierendes Werkzeug für alle Aufgaben.

---

## Was ein Agent ist

Ein [Agent](../glossar#agent) ist ein KI-System, das nicht nur antwortet, sondern handelt. Es bekommt ein Ziel – und arbeitet dann selbstständig daran. Dabei kann es Werkzeuge nutzen, Zwischenergebnisse bewerten und weitere Schritte planen, ohne dass ein Mensch jeden Schritt manuell auslöst.

Der Begriff „Agent" kommt daher, dass das System eigenständig agiert – im Unterschied zu einem [Sprachmodell](../glossar#sprachmodell), das passiv auf Eingaben wartet und antwortet. Ein Agent nimmt sich das nächste Werkzeug selbst.

Die Werkzeuge, die ein Agent nutzen kann, werden ihm bei der Einrichtung mitgegeben: eine Websuche, ein Kalender, ein Dateizugriff, eine Datenbank, eine E-Mail-Funktion. Das Modell weiß, welche Werkzeuge verfügbar sind – und entscheidet bei jedem Schritt selbst, ob und welches davon es braucht.

---

## Wie Agents funktionieren

Ein Agent ist im Kern ein [Modell](../glossar#modell), das in einer Schleife arbeitet:

1. Das Modell bekommt ein Ziel und eine Beschreibung der verfügbaren Werkzeuge.
2. Es entscheidet, welchen nächsten Schritt es unternimmt – und ob es ein Werkzeug braucht.
3. Das Werkzeug wird ausgeführt, das Ergebnis kommt zurück in den [Kontext](../glossar#kontext) des Modells.
4. Das Modell bewertet das Ergebnis und entscheidet: erledigt – oder weiter?

Diese Schleife läuft so lange, bis das Modell das Ziel als erreicht bewertet – oder bis ein vordefiniertes Limit greift.

Das Entscheidende: Das Modell plant nicht wie ein Mensch. Es wählt bei jedem Schritt den nächsten wahrscheinlichen Zug auf Basis dessen, was im Kontext steht. Das funktioniert gut für strukturierte, klar definierte Aufgaben. Bei vagen Zielen oder unerwarteten Situationen bricht die Logik ein.

---

## Ein konkretes Beispiel – Schritt für Schritt

Jemand gibt einem Agent den Auftrag: „Recherchiere die drei günstigsten Anbieter für Cloud-Server in Deutschland und erstelle eine Vergleichstabelle mit Preisen und Leistung."

Was der Agent tut:

**Schritt 1:** Er startet eine Websuche: „günstigste Cloud-Server Deutschland".

**Schritt 2:** Die Suche liefert zehn Treffer. Das Modell liest die relevanten Seiten, extrahiert Anbieternamen und Preise.

**Schritt 3:** Es stellt fest, dass einige Preise veraltet wirken – und startet eine zweite Suche mit dem Anbieternamen und aktuellem Jahr.

**Schritt 4:** Es hat jetzt genug Daten für drei Anbieter und erstellt die Tabelle.

**Schritt 5:** Es entscheidet, dass das Ziel erreicht ist, und gibt das Ergebnis aus.

Klingt reibungslos. Läuft oft auch reibungslos. Aber: In Schritt 2 könnte das Modell eine Seite falsch einschätzen und einen Anbieter aufnehmen, der gar kein Cloud-Hosting anbietet. In Schritt 3 könnte es vergessen, dass die Anforderung „Deutschland" war – und einen internationalen Anbieter recherchieren. In Schritt 5 liefert es eine sauber formatierte Tabelle, die auf falschen Daten basiert.

Solche Fehler sind keine Ausnahmen. Sie sind ein strukturelles Merkmal davon, wie Agents heute funktionieren.

---

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

**Fehler pflanzen sich fort.** Ein Agent, der in Schritt 2 eine falsche Annahme macht, baut in Schritt 3, 4 und 5 darauf auf. Am Ende ist das Ergebnis komplett falsch – und ohne die Zwischenschritte zu lesen, sieht man das nicht. Wer Agents einsetzt, sollte die Zwischenschritte überprüfen, nicht nur das Endergebnis.

**Der Agent dreht im Kreis.** Manche Implementierungen haben kein robustes Abbruchkriterium. Der Agent startet immer neue Suchen oder Versuche, kommt aber nie zu einem Abschluss. Gute Agent-Systeme haben ein explizites Schritt-Limit – und halten es ein.

**Der Agent tut zu viel.** Wenn ein Agent Schreibzugriff auf ein System hat und einen Fehler macht, kann das Konsequenzen haben, die schwer rückgängig zu machen sind. Lesezugriff ist sicherer als Schreibzugriff. Für kritische Systeme sollte immer ein Mensch den letzten Schritt genehmigen – bevor die Aktion ausgeführt wird, nicht danach.

---

## Agents heute: Was schon ohne Programmierung möglich ist

Wer heute mit Agents arbeiten will, braucht nicht zwingend Programmierkenntnisse. Mehrere Produkte bieten Agent-Funktionen direkt an:

Claude, ChatGPT und Copilot bieten Modi an, in denen das Modell eigenständig im Web suchen, Dateien lesen oder Code ausführen kann. Diese Funktionen sind als Bestandteil der normalen Oberfläche zugänglich.

Für komplexere Automatisierungen gibt es Plattformen wie n8n oder Make, die KI-Modelle in Workflows einbetten – ohne Programmierkenntnisse, aber mit Konfigurationsaufwand.

Wer eigene, angepasste Agents bauen will, braucht Programmierkenntnisse und arbeitet mit Frameworks wie LangGraph oder dem Claude Agent SDK.

---

## Was das für die Praxis bedeutet

Agents sind kein Selbstzweck. Sie sind nützlich, wenn eine Aufgabe aus vielen Schritten besteht, die sich klar beschreiben lassen und die wiederholt vorkommen. Die meisten einfachen Anwendungen – ein Dokument schreiben, einen Text überarbeiten, eine Frage beantworten – brauchen keine Agents. Da reicht ein guter [Prompt](../glossar#prompt).

Wer Agents einsetzt, sollte drei Dinge sicherstellen: klare Ziele, klare Grenzen dafür, was der Agent tun darf – und einen Menschen, der die Ergebnisse überprüft. Wer das nicht sicherstellt, übergibt Kontrolle, ohne den Überblick zu behalten.

Agents werden relevanter, je mehr KI in Arbeitsprozesse eingebettet wird. Das Verständnis, wie sie funktionieren und wo sie scheitern, ist schon jetzt nützlich.

Wie KI mit externen Werkzeugen verbunden wird, erklärt [MCP](mcp). Wie KI auf eigene Wissensdatenbanken zugreift, erklärt [RAG](rag).
