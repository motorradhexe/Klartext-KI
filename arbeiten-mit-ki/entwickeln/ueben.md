---
title: "Entwickeln: Übungen"
description: Aktive Übungen für das Arbeiten mit KI-generiertem Code – lesen, testen, verbessern.
layout: default
parent: Mit KI entwickeln
grand_parent: Mit KI arbeiten
nav_order: 3
---

# Übungen: Entwickeln mit KI

Code schreiben lassen ist der einfache Teil. Diese Übungen trainieren das, was danach kommt: lesen, verstehen, prüfen und iterieren.

---

<div class="uebung" markdown="1">

## Übung 1: Fremden Code lesen und erklären lassen

**Aufgabe:** Nimm einen Codeausschnitt aus einem Projekt, das Du nicht selbst geschrieben hast – aus einer Bibliothek, einem Kollegen-Commit, einem Tutorial.

**Ablauf:**
1. Lies den Code einmal selbst und schreibe auf, was Du nicht verstehst.
2. Gib den Code mit Kontext in KI ein: Sprache, Version, und was Du nicht verstehst.
3. Bitte um eine Erklärung Abschnitt für Abschnitt.
4. Frage dann gezielt nach dem, was Du nach der Erklärung noch nicht verstanden hast.
5. Zum Abschluss: Kannst Du erklären, was der Code tut – ohne die Erklärung vor Dir zu haben?

**Reflexionsfrage:** Was wäre passiert, wenn Du den Code ohne die Erklärung einfach übernommen hättest?

</div>

<div class="uebung" markdown="1">

## Übung 2: Eine Funktion schreiben – und bewusst Schwächen finden

**Aufgabe:** Schreibe einen vollständigen Prompt für eine Funktion in Deiner bevorzugten Sprache. Lass KI die Funktion schreiben. Dann suche bewusst nach Schwächen.

**Ablauf:**
1. Wähle eine einfache Aufgabe: Eingabe validieren, Liste sortieren, Datum formatieren – etwas Überschaubares.
2. Formuliere einen vollständigen Prompt: Sprache, Version, Eingabe, Ausgabe, Randfälle.
3. Lies den Code. Dann frage KI: „Welche Randfälle werden in diesem Code nicht behandelt?"
4. Ergänze die fehlenden Fälle durch Folgeprompts.
5. Vergleiche den ersten und den letzten Code: Was wurde ergänzt?

**Reflexionsfragen:**
- Welche Randfälle hatte KI selbst identifiziert, die Du nicht im Prompt benannt hattest?
- Welche hattest Du im Prompt benannt, aber KI trotzdem nicht korrekt behandelt?

</div>

<div class="uebung" markdown="1">

## Übung 3: Eine Fehlermeldung debuggen

**Aufgabe:** Suche in einem Deiner aktuellen Projekte nach einer Fehlermeldung – oder erzeuge eine bewusst, indem Du etwas Falsches in einfachem Code machst.

**Ablauf:**
1. Gib in KI: den relevanten Codeabschnitt, die vollständige Fehlermeldung und die Sprache/Umgebung.
2. Bitte um eine Erklärung des Fehlers – nicht nur die Lösung.
3. Frage dann: „Was hätte ich tun können, um diesen Fehler beim Schreiben zu vermeiden?"
4. Optional: Bitte um einen Test, der sicherstellt, dass der Fehler nicht erneut auftritt.

**Ziel:** Du verstehst nicht nur, wie der Fehler behoben wird – sondern auch, warum er entstanden ist. Das ist der Lerneffekt.

</div>

---

## Checkliste: Bevor Du KI-generierten Code einsetzt

- [ ] Habe ich den Code gelesen und verstanden, was er tut?
- [ ] Habe ich die Randfälle geprüft (leere Eingaben, unerwartete Werte, Grenzfälle)?
- [ ] Habe ich den Code in meiner Umgebung getestet?
- [ ] Gibt es Teile des Codes, die ich nicht erklären könnte – und die ich deshalb noch nicht einsetzen sollte?
- [ ] Sind sicherheitsrelevante Bereiche (Eingabevalidierung, Authentifizierung, Datenbankzugriffe) separat geprüft?
