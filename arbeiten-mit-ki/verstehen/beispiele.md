---
title: "Verstehen: Beispiele"
description: Drei Lernszenarien mit je einem schwachen und einem starken Prompt – und der Erklärung, wie der Dialog weitergeführt wird.
layout: default
parent: Mit KI verstehen
grand_parent: Mit KI arbeiten
nav_order: 2
---

# Beispiele: Vorher / Nachher für verschiedene Lernszenarien

Drei Situationen, in denen KI beim Verstehen helfen kann – und wie man den [Prompt](../../glossar#prompt) so gestaltet, dass die Erklärung tatsächlich passt.

---

## Beispiel 1: Ein technisches Konzept für Nicht-Techniker

**Schwacher Prompt:**

> „Erkläre mir Quantencomputer."

Das Modell liefert eine korrekte, aber generische Erklärung auf mittlerem Niveau. Für jemanden ohne Physikstudium enthält sie Begriffe, die wieder erklärt werden müssten. Für jemanden mit Informatikstudium ist sie zu oberflächlich. Sie passt auf niemanden genau.

---

**Starker Prompt:**

> „Ich habe Informatik-Grundkenntnisse aus einer Berufsausbildung, aber kein Physikstudium. Erkläre mir in drei Absätzen, was ein Quantencomputer von einem klassischen Computer unterscheidet – ohne Formeln. Benutze eine Analogie aus dem Alltag, um den Kernunterschied zu veranschaulichen. Gehe nicht auf die Hardware-Details ein."

**Was diese Eingabe besser macht:**
- Vorwissen: Informatik-Grundkenntnisse, kein Physikwissen
- Umfang: drei Absätze
- Einschränkung: keine Formeln, keine Hardware-Details
- Methode: Analogie explizit gewünscht

**Wie der Dialog weitergeführt werden kann:**
- „Die Analogie hilft, aber ich verstehe noch nicht, warum das praktisch relevant ist. Welche Probleme kann ein Quantencomputer lösen, die klassische Computer nicht können?"
- „Gibt es etwas, bei dem Quantencomputer schlechter sind als klassische?"
- „Ich habe das so verstanden: [eigene Zusammenfassung]. Stimmt das – und was habe ich vereinfacht?"

---

## Beispiel 2: Einen juristischen Text verstehen

**Schwacher Prompt:**

> „Erkläre mir den DSGVO-Artikel 17."

Das Modell liefert eine Zusammenfassung des Artikels – korrekt im Groben, aber für eine konkrete Entscheidung meist nicht ausreichend präzise. Und: Für Detailfragen in juristischen Texten gilt besondere Vorsicht vor [Halluzinationen](../../glossar#halluzination).

---

**Starker Prompt:**

> „Ich leite eine kleine Marketingagentur. Ein ehemaliger Kunde hat uns gebeten, alle Daten zu löschen, die wir über ihn gespeichert haben. Ich möchte DSGVO-Artikel 17 verstehen, um zu wissen: Haben wir die Pflicht, das zu tun? Gibt es Ausnahmen, die für Agenturen relevant sein könnten?
>
> Ich bin kein Jurist. Erkläre es so, dass ich verstehe, was ich als nächstes prüfen oder tun muss. Weise mich darauf hin, wenn du unsicher bist oder wenn ich unbedingt juristischen Rat einholen sollte."

**Was diese Eingabe besser macht:**
- Kontext: kleine Marketingagentur, konkreter Fall
- Erkenntnisziel: Pflicht ja/nein, relevante Ausnahmen
- Niveau: kein juristisches Vorwissen
- Ehrlichkeitserwartung: explizit nach Unsicherheiten gefragt

**Wichtiger Hinweis:** KI-Erklärungen juristischer Texte ersetzen keine Rechtsberatung. Sie helfen, den Text zu verstehen und die richtigen Fragen zu stellen – aber nicht, eine rechtssichere Entscheidung zu treffen.

**Wie der Dialog weitergeführt werden kann:**
- „Du hast Ausnahmen erwähnt. Welche davon könnten für eine Marketingagentur realistisch relevant sein?"
- „Was bedeutet ‚berechtigte Interessen' konkret – kannst du das an einem Beispiel zeigen?"

---

## Beispiel 3: Eine komplexe Dokumentation durcharbeiten

**Schwacher Prompt:**

> „Erkläre mir diese Dokumentation." [Dokumentation eingefügt]

Das Modell fasst die Dokumentation zusammen – was nützlich ist, aber oft nicht das, was man wirklich braucht. Man bekommt einen Überblick, aber kein Verständnis der Teile, die tatsächlich unklar waren.

---

**Starker Prompt:**

> „Ich lese diese technische API-Dokumentation [Abschnitt eingefügt]. Ich bin Backend-Entwicklerin mit Python-Kenntnissen, aber ohne Erfahrung mit dieser spezifischen API.
>
> Ich verstehe nicht, was der Unterschied zwischen ‚synchronen' und ‚asynchronen' Anfragen in diesem Kontext bedeutet – und warum ich mich in meinem Fall für die eine oder andere entscheiden würde. Erkläre mir das anhand dieser Dokumentation, nicht abstrakt."

**Was diese Eingabe besser macht:**
- Konkreter Abschnitt: eingefügt, nicht nur beschrieben
- Hintergrund: Python, keine Erfahrung mit der API
- Konkrete Frage: nicht „erkläre alles", sondern „erkläre diesen Unterschied"
- Bezug: „anhand dieser Dokumentation" – nicht abstrakt

**Wie der Dialog weitergeführt werden kann:**
- „In meinem Fall habe ich [Beschreibung des Anwendungsfalls]. Was würdest du empfehlen – und warum?"
- „Hier ist ein Stück meines bestehenden Codes. Was müsste ich ändern, um auf asynchrone Anfragen umzustellen?"

---

## Übung

Nimm einen Text, den du schon einmal gelesen und nicht vollständig verstanden hast – einen Fachartikel, eine Dokumentation, ein Gesetz, einen technischen Standard.

Gib einen Abschnitt davon in KI ein. Schreibe dazu: Was weißt du schon? Was verstehst du nicht? Wozu brauchst du das Verständnis? Dann lies die Antwort – und stell mindestens drei Folgefragen. Das Verständnis, das nach fünf Fragen entsteht, ist immer tiefer als das nach einer.
