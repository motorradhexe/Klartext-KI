---
title: "Erklären: Beispiele"
description: Drei Erklärungssituationen mit je einem schwachen und einem starken Prompt.
layout: default
parent: Mit KI erklären
grand_parent: Mit KI arbeiten
nav_order: 2
---

# Beispiele: Vorher / Nachher für verschiedene Erklärungssituationen

Drei häufige Situationen, in denen KI beim Formulieren von Erklärungen hilft – von der technischen Erklärung für Nicht-Techniker bis zum Übergabedokument.

---

## Beispiel 1: Ein technisches Konzept für Entscheider erklären

**Schwacher Prompt:**

```
Erkläre, was eine API ist.
```

Das Modell liefert eine technisch korrekte, aber generische Definition. Für jemanden ohne Technikstudium enthält sie Begriffe, die wieder erklärt werden müssten. Für eine Präsentation vor der Geschäftsführung ist sie weder anschaulich noch auf das Wesentliche fokussiert.

---

**Starker Prompt:**

```
Erkläre einer Projektleiterin ohne technisches Hintergrundwissen, was eine API ist und warum es für ihr Projekt wichtig ist, dass zwei Softwaresysteme eine gut dokumentierte API haben. Sie entscheidet nächste Woche, ob das Projekt genehmigt wird. Benutze eine Alltagsanalogie. Kein Fachjargon – der Begriff ‚API' selbst darf vorkommen und soll einmal kurz erklärt werden. Länge: max. vier Absätze.
```

**Was diese Eingabe besser macht:**
- Person: Projektleiterin, kein technisches Wissen
- Entscheidungsaufgabe: Projektgenehmigung nächste Woche
- Format: Alltagsanalogie, kein Jargon
- Ausnahme: „API" darf vorkommen, einmal erklären
- Umfang: max. vier Absätze

**Wie der Dialog weitergeführt werden kann:**
- „Die Steckdosen-Analogie funktioniert, aber ich brauche noch einen Satz, der erklärt, warum schlechte Dokumentation konkrete Kosten verursacht."
- „Formuliere das als Folie: Überschrift, drei Stichpunkte, eine Abschlussaussage."

---

## Beispiel 2: Ein Übergabedokument erstellen

**Schwacher Prompt:**

```
Erkläre mir, was eine Übergabe enthält.
```

Das Modell liefert eine allgemeine Antwort mit typischen Übergabeelementen. Nützlich als Erinnerungshilfe – aber nicht als fertiges Dokument für eine konkrete Situation.

---

**Starker Prompt:**

```
Ich übergebe in zwei Wochen eine laufende Kundenbeziehung an eine Kollegin. Der Kunde ist ein mittelständisches Produktionsunternehmen, das seit drei Jahren Kunde ist. Meine Kollegin kennt die Branche, aber nicht diesen Kunden. Sie übernimmt alle operativen Aufgaben.

Erstelle ein Übergabedokument mit diesen Informationen, die ich dir jetzt gebe:
– Hauptansprechpartner beim Kunden: Thomas Berger, Einkaufsleiter, kommuniziert bevorzugt per E-Mail, reagiert langsam auf Anrufe
– Aktuelles Projekt: Liefervertragsanpassung, läuft seit Oktober, nächster Meilenstein 15. April
– Besonderheit: Der Kunde hat eine schlechte Erfahrung mit einem früheren Dienstleister gemacht und ist sensibel bei Themen rund um Qualitätssicherung
– Offener Punkt: Rechnungsdiskrepanz aus Q4 noch ungeklärt, ich kümmere mich bis zu meinem letzten Tag darum

Format: klares, lesbares Dokument, max. eine Seite. Meine Kollegin soll nach der Lektüre in der Lage sein, das erste Gespräch mit dem Kunden vorzubereiten.
```

**Was diese Eingabe besser macht:**
- Beziehungskontext: Dauer, Branche, Art der Übergabe
- Empfängerin: kennt Branche, nicht den Kunden, übernimmt operativ
- Konkretes Material: vier Punkte mit echten Details
- Ziel des Dokuments: Vorbereitung auf erstes Gespräch
- Format: max. eine Seite

Das Modell kann jetzt ein Dokument erstellen, das über diesen Kunden spricht – nicht über einen imaginären.

**Wie der Dialog weitergeführt werden kann:**
- „Ergänze einen kurzen Abschnitt ‚Kommunikationshinweise', der erklärt, wie man mit Thomas Berger am besten kommuniziert."
- „Die Rechnungsdiskrepanz klingt zu problematisch formuliert. Schreib das neutraler, ohne es herunterzuspielen."

---

## Beispiel 3: Eine Entscheidung für das eigene Team erklären

**Schwacher Prompt:**

```
Erkläre meinem Team, warum wir zu einem neuen Tool wechseln.
```

Das Modell schreibt etwas Allgemeines über Toolwechsel – freundlich, halbherzig, ohne Substanz. Das eigene Team wird das durchschauen.

---

**Starker Prompt:**

```
Ich muss meinem Team erklären, warum wir von Trello auf Jira wechseln. Das Team arbeitet seit drei Jahren mit Trello und ist damit zufrieden. Der Wechsel kommt von der Geschäftsführung.

Gründe für den Wechsel: bessere Integration mit unserem bestehenden Confluence-Wiki, einheitliche Plattform für alle Teams im Unternehmen, leistungsfähigere Berichte für das Management.

Formuliere eine kurze, direkte Erklärung für mein Team (acht Personen, technisch versiert, skeptisch gegenüber Wechseln). Benenne die Gründe ehrlich – auch dass ein Teil des Drucks von oben kommt. Kein Spin, kein Enthusiasmus, den ich nicht halten kann. Max. 150 Wörter.
```

**Was diese Eingabe besser macht:**
- Situation: zufriedenes Team, externer Druck
- Gründe: drei konkrete Punkte
- Zielgruppe: technisch versiert, wechselskeptisch
- Tonvorgabe: ehrlich, kein Spin, kein erzwungener Enthusiasmus
- Umfang: max. 150 Wörter

Ein Team, das seit drei Jahren ein Tool nutzt, erkennt aufgesetzte Begeisterung sofort. Wer das dem Modell sagt, bekommt eine Formulierung, die das nicht tut.

**Wie der Dialog weitergeführt werden kann:**
- „Der letzte Satz klingt zu versöhnlich. Lass ihn weg und ende mit dem konkreten Zeitplan."
- „Formuliere eine kurze FAQ-Antwort für die wahrscheinlichste Gegenfrage: ‚Warum nicht Asana?'"

---

## Übung

Denk an etwas, das Du regelmäßig erklären musst – einem Kollegen, einem Kunden, einer Führungskraft. Etwas, bei dem die Erklärungen oft nicht ankommen oder länger dauern als nötig.

Beschreibe KI: Wer ist die Person? Was weiß sie schon? Was soll sie am Ende verstehen oder entscheiden können? Wie viel Zeit oder Raum hast Du?

Lies das Ergebnis kritisch: Würde diese Person das wirklich verstehen – oder klingt es gut, ohne zu landen?
