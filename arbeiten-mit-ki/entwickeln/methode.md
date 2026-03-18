---
title: "Entwickeln: Methode"
description: Wie man Code-Prompts formuliert, die zu konkretem, einsetzbarem Code führen.
layout: default
parent: Mit KI entwickeln
grand_parent: Mit KI arbeiten
nav_order: 1
---

# Methode: Code-Prompts, die tatsächlich funktionieren

KI kann Code schreiben, erklären und überprüfen – aber nur, wenn man ihr genug Kontext gibt. Unpräzise Prompts liefern Code, der zwar läuft, aber nicht das tut, was man wirklich braucht.

---

## Sprache und Umgebung immer angeben

Das erste, was in jeden Code-[Prompt](../../glossar#prompt) gehört: die Programmiersprache und die Version. Dazu alles, was die Umgebung beschreibt.

Nützliche Angaben:
- **Sprache und Version:** Python 3.11, JavaScript ES2022, TypeScript 5
- **[Framework](../../glossar#framework):** Das ist das Grundgerüst, auf dem die Anwendung aufbaut – z. B. Django oder FastAPI bei Python, React oder Vue bei JavaScript. Ohne diese Angabe trifft das Modell Annahmen, die oft nicht stimmen.
- **Umgebung:** Läuft der Code im Browser, auf einem Server, in einer Datenbank?
- **Vorhandene [Imports](../../glossar#import):** Welche Zusatz-Bausteine sind bereits eingebunden?

Warum das wichtig ist: KI schreibt Code, der zu den Angaben passt. Fehlt die Angabe, schreibt das Modell für einen imaginierten Standardfall – der nicht deiner ist.

---

## Bestehenden Code immer mitgeben

Wenn man eine Funktion erweitern, einen Fehler beheben oder Code umbauen will, gehört der betroffene Code in den [Kontext](../../glossar#kontext). Ohne ihn kann das Modell keine Verbindung zur bestehenden Struktur herstellen.

Das betrifft:
- Die Funktion, die geändert werden soll
- Die Klasse oder das Modul, in das neuer Code eingebettet wird
- Die Fehlermeldung, die erklärt werden soll

Fehlermeldungen sind besonders wertvoll: Sie geben dem Modell genau die Information, die es braucht, um eine präzise Erklärung oder Lösung zu liefern.

---

## Die Aufgabe vollständig beschreiben

Neben Sprache und Kontext braucht das Modell eine klare Aufgabenbeschreibung. Vollständig heißt:

**Was soll die Funktion tun?**
Klar und konkret: Was geht rein, was kommt raus? In welchem Format?

**Welche Randfälle sollen behandelt werden?**
Was passiert, wenn die Eingabe leer ist? Was, wenn eine Zahl durch null dividiert werden würde? Was, wenn der Nutzer etwas eingibt, das das Format nicht erfüllt? Randfälle, die im Prompt nicht vorkommen, kommen in der Lösung meist auch nicht vor.

**Was soll die Funktion ausdrücklich nicht tun?**
Negative Anforderungen helfen, um ungewollte Nebeneffekte zu vermeiden.

---

## Mit Fehlermeldungen arbeiten

Wenn KI-generierter Code nicht funktioniert: Fehlermeldung in den nächsten Prompt kopieren und fragen lassen. Das ist effektiver als eine vage Beschreibung des Problems.

Guter Folgeprompt bei einem Fehler:
```
Hier ist der Code: [Code]
Hier ist die Fehlermeldung: [Fehlermeldung]
Was ist das Problem, und wie wird es behoben?
```

[Iteration](../../glossar#iteration) ist kein Versagen – es ist der normale Weg zu funktionierendem Code. Auch erfahrene Entwicklerinnen und Entwickler arbeiten iterativ.

---

## Code immer lesen und testen

KI-generierter Code sieht professionell aus. Das kann dazu verführen, ihn direkt einzusetzen. Aber:

- **Lesbarkeit ist nicht dasselbe wie Korrektheit.** Code kann syntaktisch einwandfrei sein und trotzdem nicht das tun, was man braucht.
- **Randfälle sind selten automatisch abgedeckt.** Besonders in produktivem Code – also Code, der tatsächlich bei Nutzerinnen und Nutzern läuft – muss man prüfen, was bei unerwarteten Eingaben passiert.
- **Code, den man nicht versteht, kann man nicht prüfen.** Wenn man eine Funktion nicht lesen und erklären kann, kann man nicht sicherstellen, dass sie das richtige tut.

Testen ist kein Misstrauen gegenüber dem Modell. Es ist normaler Teil des Entwicklungsprozesses.

---

## Typische Fehler – und warum sie passieren

**Keine Angabe der Umgebung.**
„Schreib Python-Code" und „Ich benutze Python 3.11 mit FastAPI, hier ist meine bestehende Route" liefern grundlegend verschiedene Ergebnisse. Der zweite Prompt ist nie zu detailliert.

**Randfälle vergessen.**
Was nicht im Prompt steht, wird nicht bedacht. Wer produktiven Code schreibt, muss die Randfälle selbst benennen – oder explizit fragen: „Welche Randfälle hast du nicht behandelt?"

**Code übernehmen ohne Lesen.**
KI-generierter Code sieht professionell aus. Aber Professionalität im Aussehen ist kein Beweis für Korrektheit. Immer lesen, bevor man einsetzt.

**[Docstring](../../glossar#docstring) vergessen.**
Ein Docstring ist ein eingebetteter Kommentar direkt in der Funktion, der erklärt, was sie tut, was sie erwartet und was sie zurückgibt. KI schreibt ihn gern mit – wenn man darum bittet. Für jede Funktion, die andere lesen oder nutzen sollen, lohnt sich die Anfrage.
