---
title: "Agents: Konzept & Funktionsweise"
description: Was ein Agent ist, wie die Arbeitsschleife funktioniert und was dabei Schritt für Schritt passiert.
layout: default
parent: KI-Agents
grand_parent: Vertiefung
nav_order: 1
---

# Konzept & Funktionsweise

## Was ein Agent ist

Ein [Agent](../../glossar#agent) ist ein KI-System, das nicht nur antwortet, sondern handelt. Es bekommt ein Ziel – und arbeitet dann selbstständig daran. Dabei kann es Werkzeuge nutzen, Zwischenergebnisse bewerten und weitere Schritte planen, ohne dass ein Mensch jeden Schritt manuell auslöst.

Der Begriff „Agent" kommt daher, dass das System eigenständig agiert – im Unterschied zu einem [Sprachmodell](../../glossar#sprachmodell), das passiv auf Eingaben wartet und antwortet. Ein Agent nimmt sich das nächste Werkzeug selbst.

Die Werkzeuge, die ein Agent nutzen kann, werden ihm bei der Einrichtung mitgegeben: eine Websuche, ein Kalender, ein Dateizugriff, eine Datenbank, eine E-Mail-Funktion. Das Modell weiß, welche Werkzeuge verfügbar sind – und entscheidet bei jedem Schritt selbst, ob und welches davon es braucht.

---

## Wie Agents funktionieren

Ein Agent ist im Kern ein [Modell](../../glossar#modell), das in einer Schleife arbeitet:

1. Das Modell bekommt ein Ziel und eine Beschreibung der verfügbaren Werkzeuge.
2. Es entscheidet, welchen nächsten Schritt es unternimmt – und ob es ein Werkzeug braucht.
3. Das Werkzeug wird ausgeführt, das Ergebnis kommt zurück in den [Kontext](../../glossar#kontext) des Modells.
4. Das Modell bewertet das Ergebnis und entscheidet: erledigt – oder weiter?

Diese Schleife läuft so lange, bis das Modell das Ziel als erreicht bewertet – oder bis ein vordefiniertes Limit greift.

Das Entscheidende: Das Modell plant nicht wie ein Mensch. Es wählt bei jedem Schritt den nächsten wahrscheinlichen Zug auf Basis dessen, was im Kontext steht. Das funktioniert gut für strukturierte, klar definierte Aufgaben. Bei vagen Zielen oder unerwarteten Situationen bricht die Logik ein.

---

## Ein konkretes Beispiel – Schritt für Schritt

Jemand gibt einem Agent den Auftrag: „Recherchiere die drei günstigsten Anbieter für Cloud-Server in Deutschland und erstelle eine Vergleichstabelle mit Preisen und Leistung."

**Schritt 1:** Er startet eine Websuche: „günstigste Cloud-Server Deutschland".

**Schritt 2:** Die Suche liefert zehn Treffer. Das Modell liest die relevanten Seiten, extrahiert Anbieternamen und Preise.

**Schritt 3:** Es stellt fest, dass einige Preise veraltet wirken – und startet eine zweite Suche mit dem Anbieternamen und aktuellem Jahr.

**Schritt 4:** Es hat jetzt genug Daten für drei Anbieter und erstellt die Tabelle.

**Schritt 5:** Es entscheidet, dass das Ziel erreicht ist, und gibt das Ergebnis aus.

Klingt reibungslos. Läuft oft auch reibungslos. Aber: In Schritt 2 könnte das Modell eine Seite falsch einschätzen und einen Anbieter aufnehmen, der gar kein Cloud-Hosting anbietet. In Schritt 3 könnte es vergessen, dass die Anforderung „Deutschland" war. In Schritt 5 liefert es eine sauber formatierte Tabelle – die auf falschen Daten basiert.

Solche Fehler sind keine Ausnahmen. Sie sind ein strukturelles Merkmal davon, wie Agents heute funktionieren. Mehr dazu im nächsten Abschnitt.
