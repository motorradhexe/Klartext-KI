---
title: "Entwickeln: Beispiele"
description: Drei Entwicklungsszenarien mit je einem schwachen und einem starken Prompt.
layout: default
parent: Mit KI entwickeln
grand_parent: Mit KI arbeiten
nav_order: 2
---

# Beispiele: Vorher / Nachher für verschiedene Entwicklungsaufgaben

Drei häufige Situationen beim Entwickeln mit KI – mit je einem schwachen und einem starken Prompt und der Erklärung, was den Unterschied macht.

---

## Beispiel 1: Eine Funktion schreiben lassen

**Schwacher Prompt:**

> „Schreib mir eine Funktion in Python."

Das Modell fragt entweder zurück oder schreibt ein generisches Beispiel – eine Funktion, die zwei Zahlen addiert oder einen Namen ausgibt. Nicht falsch, aber für niemanden nützlich.

---

**Starker Prompt:**

> „Ich arbeite in Python 3.11. Schreib eine Funktion `sortiere_personen`, die eine Liste von Dictionaries entgegennimmt. Jedes Dictionary hat die Schlüssel `name` (String) und `alter` (Integer). Die Funktion gibt die Liste sortiert nach `alter` zurück, aufsteigend. Wenn zwei Personen dasselbe Alter haben, wird nach `name` alphabetisch sortiert. Füge einen [Docstring](../../glossar#docstring) hinzu, der Eingabe, Ausgabe und das Verhalten bei gleichen Altersangaben beschreibt."

*Erklärung: Ein Dictionary ist eine strukturierte Datensammlung in Python – zum Beispiel `{"name": "Max", "alter": 30}`. String bedeutet Text, Integer bedeutet ganze Zahl. Ein Docstring ist ein eingebetteter Kommentar direkt in der Funktion.*

**Was diese Eingabe besser macht:**
- Sprache und Version: Python 3.11
- Funktionsname: `sortiere_personen`
- Eingabeformat: Liste von Dictionaries, Schlüssel benannt
- Ausgabeformat: sortierte Liste, Sortierprioritäten
- Randfall: gleiche Altersangaben, alphabetisch
- Docstring: explizit angefragt mit Inhaltsvorgabe

**Wie der Dialog weitergeführt werden kann:**
- „Was passiert, wenn die Liste leer ist? Soll die Funktion das explizit behandeln?"
- „Füge einen Test für den Fall hinzu, dass zwei Personen dasselbe Alter haben."

---

## Beispiel 2: Fremden Code verstehen

**Schwacher Prompt:**

> „Was macht dieser Code?" [Code eingefügt]

Das Modell gibt eine Zusammenfassung – aber often ohne die Tiefe, die man braucht, um den Code wirklich zu verstehen oder sicher zu verändern.

---

**Starker Prompt:**

> „Ich habe diesen Python-Code aus einem Projekt geerbt und muss ihn jetzt warten und erweitern. Ich verstehe Python-Grundlagen, aber bin kein erfahrener Entwickler.
>
> [Code eingefügt]
>
> Erkläre mir, was dieser Code tut – Abschnitt für Abschnitt. Geh davon aus, dass ich nicht weiss, warum bestimmte Entscheidungen getroffen wurden. Wenn es Teile gibt, die ungewöhnlich oder potenziell problematisch sind, weise mich darauf hin. Erkläre auch, was passiert, wenn ich Eingabe X übergebe."

**Was diese Eingabe besser macht:**
- Kontext: geerbter Code, Wartungsaufgabe
- Niveau: Grundkenntnisse Python, kein Senior-Level
- Detailtiefe: Abschnitt für Abschnitt
- Zusatzbitte: Ungewöhnliches und Problematisches markieren
- Konkretes Szenario: Verhalten bei einer bestimmten Eingabe

**Wie der Dialog weitergeführt werden kann:**
- „Du hast erwähnt, dass der Fehlerfall nicht behandelt wird. Wie würde ich das ergänzen, ohne den Rest zu verändern?"
- „Was wäre ein einfacherer Weg, dasselbe zu erreichen?"

---

## Beispiel 3: Einen Fehler beheben

**Schwacher Prompt:**

> „Mein Code funktioniert nicht. Was ist falsch?"

Ohne den Code und die Fehlermeldung kann das Modell nichts analysieren. Es fragt zurück oder gibt generische Hinweise, die nicht weiterhelfen.

---

**Starker Prompt:**

> „Ich benutze Python 3.10 und das Framework FastAPI. Hier ist meine Route:
>
> [Code der Route eingefügt]
>
> Wenn ich die Route mit dieser Anfrage aufrufe: `POST /users` mit dem Body `{"name": "Anna", "email": "anna@example.com"}`, bekomme ich diese Fehlermeldung:
>
> `422 Unprocessable Entity: value is not a valid email address`
>
> Das E-Mail-Format stimmt aber. Was ist das Problem, und wie wird es behoben?"

**Was diese Eingabe besser macht:**
- Umgebung: Python 3.10, FastAPI
- Code: vollständig eingefügt
- Aufruf: konkrete Anfrage mit Body
- Fehlermeldung: vollständig und wörtlich kopiert
- Beobachtung: eigene Einschätzung des Problems

Das Modell kann jetzt gezielt analysieren, ob das Problem im Datenmodell, in der Validierung, in der Route oder woanders liegt – statt allgemeine Hinweise zu geben.

**Wie der Dialog weitergeführt werden kann:**
- „Die Lösung hat funktioniert. Kannst du erklären, warum das Problem entstanden ist – damit ich es beim nächsten Mal selbst erkennen kann?"
- „Gibt es eine sauberere Art, E-Mail-Validierung in FastAPI zu implementieren?"

---

## Übung

Nimm einen Code-Ausschnitt aus deiner Arbeit oder aus einem Projekt, das du verstehen willst. Gib ihn in KI ein und schreib dazu:

- Welche Sprache und Version du verwendest
- Was der Code tun soll (soweit du das weißt)
- Was du nicht verstehst oder was unklar ist

Dann lies die Erklärung – und frag nach dem, was noch unklar ist. KI als Lernpartner beim Entwickeln funktioniert nur als Dialog.
