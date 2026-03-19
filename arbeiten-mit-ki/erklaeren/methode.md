---
title: "Erklären: Methode"
description: Wie man Erklärungs-Prompts formuliert, die bei der Zielgruppe tatsächlich ankommen.
layout: default
parent: Mit KI erklären
grand_parent: Mit KI arbeiten
nav_order: 1
---

# Methode: Erklärungen, die bei der Zielgruppe ankommen

Eine gute Erklärung ist nicht für jeden. Sie ist für eine bestimmte Person, in einer bestimmten Situation, mit einem bestimmten Ziel. KI kann genau das liefern – aber nur, wenn Du diese drei Punkte mitgibst.

---

## Die drei Angaben, die jeden Erklärungs-Prompt verbessern

**1. Was soll erklärt werden?**
Nicht das Thema allgemein, sondern der konkrete Aspekt. „Was eine API ist" ist weniger präzise als „warum zwei Softwaresysteme eine gut dokumentierte API brauchen und was ohne das schiefgehen kann". Der zweite Prompt hat ein klares Erkenntnisziel – und das Modell schreibt darauf hin.

**2. Wer soll es verstehen?**
Fachkenntnisse, Berufshintergrund, was die Person schon weiß, was sie nicht weiß. „Meine Chefin ist Juristin ohne technischen Hintergrund" ist eine andere Ausgangslage als „mein Team aus Entwicklerinnen und Entwicklern". Je genauer die Beschreibung, desto passender die Sprache.

**3. Was soll danach anders sein?**
Eine Erklärung ist kein Selbstzweck. Soll die Person eine Entscheidung treffen können? Soll sie einem Projekt zustimmen? Soll sie selbst etwas anwenden können? Das Ziel bestimmt, was in die Erklärung gehört und was nicht.

---

## Analogien gezielt einsetzen

Analogien machen abstrakte Konzepte greifbar. KI kann sie auf Anfrage liefern – und Du kannst sie gezielt anfordern.

Praktische Wege:

**Explizit anfragen:**
„Benutze eine Analogie aus dem Alltag" liefert fast immer etwas Verwendbares. Dann prüfst Du: Passt die Analogie zur Zielgruppe? Ist sie treffend genug, ohne zu vereinfachen?

**Den Bereich vorgeben:**
„Erkläre das mit einer Analogie aus dem Gesundheitswesen" oder „...aus dem Bauwesen" oder „...aus dem Schulalltag" – je nach Hintergrund der Zielgruppe liefert eine bereichsspezifische Analogie mehr als eine beliebige.

**Analogien anpassen:**
Das Modell liefert selten eine perfekte Analogie beim ersten Versuch. Folgeprompt: „Die Analogie mit dem Postboten ist zu simpel für das, was ich erklären muss. Versuch es mit einer, die auch zeigt, warum Datensicherheit dabei eine Rolle spielt."

---

## Schritt für Schritt erklären lassen, nicht alles auf einmal

Eine Erklärung, die zu viele Aspekte abdeckt, erklärt am Ende keinen davon richtig. Wenn Du mehrere Punkte erklären musst, ist es besser, das Modell einen nach dem anderen ausarbeiten zu lassen.

Praktisch:
1. Erstes Konzept erklären lassen
2. Prüfen: Ist das klar genug, um darauf aufzubauen?
3. Zweites Konzept erklären lassen, das auf dem ersten aufbaut
4. Zusammenfassung am Ende anfragen: „Fasse in drei Sätzen zusammen, was die Zuhörenden aus dieser Erklärung mitnehmen sollen."

Dieser Ablauf ist langsamer als alles auf einmal – aber das Ergebnis ist erheblich schärfer.

---

## Erklärungen für Präsentationen vorbereiten

KI kann nicht nur Texte, sondern auch Präsentationsstrukturen entwerfen. Nützliche Angaben:

- Wie viel Zeit hast Du?
- Was soll am Ende mit den Zuhörenden passieren? (Entscheidung, Zustimmung, Wissen)
- Was wissen die Zuhörenden schon, was nicht?
- Was sind mögliche Einwände oder Fragen?

Aus diesen Angaben kann das Modell eine Struktur vorschlagen, die auf das Ziel der Präsentation zugeschnitten ist – nicht eine generische Foliengliederung.

---

## Typische Fehler – und warum sie passieren

**Die Zielgruppe nicht beschrieben.**
KI schreibt für ein mittleres Bildungsniveau und mittleres Vorwissen, wenn Du nichts anderes sagst. Das passt selten genau. Für jemanden ohne Fachkenntnisse ist es zu voraussetzungsreich, für Fachleute zu oberflächlich.

**Den eigenen [Kontext](../../glossar#kontext) nicht mitgegeben.**
„Erkläre mir, was eine Übergabe enthält" liefert eine allgemeine Antwort. „Ich übergebe eine laufende Kundenbeziehung an eine Kollegin, die die Branche kennt, aber den Kunden nicht – was gehört in das Übergabedokument?" liefert etwas Konkretes.

**Das Ergebnis ohne inhaltliche Prüfung eingesetzt.**
KI formuliert gut. Aber der Inhalt kann Fehler enthalten. Wer eine Erklärung für andere erstellt, muss sicherstellen, dass die inhaltlichen Aussagen stimmen – besonders wenn sie für eine Entscheidung relevant sind.

---

## Prompt-Vorlage für Erklärungsaufgaben

```
Thema: [Was soll erklärt werden – konkret, nicht allgemein]
Zielgruppe: [Wer ist die Person? Was weiß sie, was nicht?]
Ziel: [Was soll die Person danach tun, entscheiden oder verstehen können?]
Format: [Fließtext, Stichpunkte, Analogie, Präsentation]
Besonderes: [Fachjargon vermeiden / bestimmten Begriff einmal erklären / max. X Sätze]

Aufgabe: Formuliere eine Erklärung auf Basis dieser Angaben.
```

Beispiele, die diese Vorlage in verschiedenen Situationen anwenden, findest Du auf der Seite [Beispiele](beispiele).
