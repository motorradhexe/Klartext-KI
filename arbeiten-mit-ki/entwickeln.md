---
title: Mit KI entwickeln
description: Wie man mit KI Code versteht, schreibt und überprüft – auch ohne tiefes Programmierwissen.
layout: modul
nav_order: 13
---

# Mit KI entwickeln

KI verändert das Arbeiten mit Code grundlegend – auch für Menschen ohne tiefes Programmierwissen. Aber die Grundregel bleibt: Code, den man nicht versteht, kann man nicht prüfen. Und Code, den man nicht prüfen kann, sollte man nicht einsetzen.

---

## 1. Wofür eignet sich KI hier – und wofür nicht?

KI ist beim Entwickeln für eine Reihe von Aufgaben gut geeignet: Code erklären, Fehler finden, Funktionen schreiben, bestehenden Code umbauen, Boilerplate generieren (also Standardcode, der in fast jedem Projekt ähnlich aussieht), Dokumentation ergänzen. Gerade das Verstehen von fremdem Code – aus einem Projekt, einer Bibliothek, einem System – wird mit KI erheblich schneller.

Was KI nicht kann: die Anforderungen kennen, die man ihr nicht gegeben hat. Wenn man eine Funktion bestellt, ohne zu sagen, welche Randfälle behandelt werden sollen, werden sie nicht behandelt. Wenn man nicht angibt, in welches System der Code eingebettet ist, ignoriert das Modell das System.

Außerdem: KI-generierter Code kann syntaktisch korrekt sein und trotzdem nicht das tun, was man braucht. Das Modell schreibt Code, der auf den [Prompt](/glossar#prompt) passt – nicht auf die eigentliche Absicht, wenn man die nicht präzise beschrieben hat. Wer Code blind übernimmt, ohne ihn zu lesen und zu testen, baut auf einer unsicheren Grundlage.

---

## 2. Wie geht man es an?

**Sprache und Umgebung angeben.** „Schreib eine Funktion" ist kein ausreichender Startpunkt. Welche Sprache? Welche Version? Welches Framework? Läuft der Code in einer bestimmten Umgebung? Das Modell trifft sonst Annahmen – und die stimmen manchmal nicht.

**Bestehenden Code mitgeben.** Wenn man eine Funktion erweitern, einen Fehler beheben oder Code umbauen will, gehört der betroffene Code in den [Kontext](/glossar#kontext). Das Modell kann nicht erraten, wie die Umgebung aussieht. Mit dem Code vor Augen kann es konkret und korrekt antworten.

**Die Aufgabe vollständig beschreiben.** Was soll die Funktion tun? Was bekommt sie rein, was kommt raus? Gibt es Randfälle, die behandelt werden müssen? Gibt es etwas, das die Funktion ausdrücklich nicht tun soll? Je vollständiger die Beschreibung, desto näher kommt das erste Ergebnis an das, was man braucht.

**Ergebnisse immer testen.** KI-Code funktioniert häufig auf Anhieb – aber nicht immer. Testen ist kein Misstrauen gegenüber dem Modell, sondern normaler Teil des Entwicklungsprozesses. Und wenn der Code nicht funktioniert: Fehlermeldung in den nächsten Prompt einfügen und fragen lassen, was das Problem ist.

---

## 3. Typische Fehler – und warum sie passieren

**Code übernehmen ohne Lesen.** KI-generierter Code sieht professionell aus. Das verführt dazu, ihn direkt einzusetzen. Aber Lesbarkeit und Korrektheit sind verschiedene Dinge. Wer Code einsetzt, ohne ihn gelesen zu haben, kann ihn nicht auf seine eigene Situation hin prüfen – und merkt Probleme erst, wenn sie auftreten.

**Fehlende Randfälle.** Ein Prompt wie „Schreib eine Funktion, die eine Zahl durch eine andere teilt" liefert eine Funktion, die das tut – aber vermutlich keine Behandlung für den Fall, dass der Divisor null ist. Was nicht im Prompt steht, wird nicht bedacht. Wer produktiven Code schreibt, muss diese Lücken selbst schließen.

**Keine Angabe der Umgebung.** „Ich benutze Python 3.9 und das Framework FastAPI, hier ist meine bestehende Route" ist ein anderer Ausgangspunkt als „Schreib Python-Code". Das Modell weiß ohne diese Angaben nicht, welche Imports schon existieren, welche Konventionen gelten oder welche Einschränkungen es gibt.

**[Iteration](/glossar#iteration) als Versagen missverstanden.** Wenn das erste Ergebnis nicht passt, ist das kein Fehler. Es bedeutet, dass der Prompt oder die Anforderung nicht vollständig war. Folgeprompts – „Das funktioniert, aber es soll auch den Fall X behandeln" oder „Hier ist die Fehlermeldung, die ich bekomme" – sind der normale Weg zu funktionierendem Code.

---

## 4. Beispiel: Vorher / Nachher

**Eingabe 1:**
„Schreib mir eine Funktion in Python."

Das Modell fragt entweder nach oder schreibt ein generisches Beispiel – eine Funktion, die zwei Zahlen addiert oder einen Namen ausgibt. Nicht falsch, aber für niemanden nützlich.

**Eingabe 2:**
„Ich arbeite in Python 3.11. Schreib eine Funktion `sortiere_personen`, die eine Liste von Dictionaries entgegennimmt. Jedes Dictionary hat die Schlüssel `name` (String) und `alter` (Integer). Die Funktion gibt die Liste sortiert nach `alter` zurück, aufsteigend. Wenn zwei Personen dasselbe Alter haben, soll nach `name` alphabetisch sortiert werden. Füge einen Docstring hinzu."

Diese Eingabe gibt die Sprache, die Funktion, die Eingabestruktur, das Ausgabeformat, den Hauptfall und den Randfall vor. Das Modell kann jetzt genau das schreiben, was gebraucht wird.

---

## 5. Zum Ausprobieren

Nehmen Sie einen Code-Ausschnitt aus Ihrer Arbeit – oder aus einem Projekt, das Sie verstehen wollen. Geben Sie ihn in KI ein und fragen Sie: „Erkläre mir, was dieser Code tut. Geh Zeile für Zeile vor und erkläre, wozu jeder Abschnitt da ist."

Das Ergebnis zeigt, ob Sie den Code verstanden haben – oder ob die Erklärung Fragen aufwirft, die Sie im nächsten Prompt stellen können. So funktioniert KI als Lernpartner beim Entwickeln.
