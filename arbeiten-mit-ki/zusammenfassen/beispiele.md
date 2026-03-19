---
title: "Zusammenfassen: Beispiele"
description: Drei Zusammenfassungsaufgaben mit je einem schwachen und einem starken Prompt.
layout: default
parent: Mit KI zusammenfassen
grand_parent: Mit KI arbeiten
nav_order: 2
---

# Beispiele: Vorher / Nachher für verschiedene Zusammenfassungsaufgaben

Drei häufige Situationen, in denen KI beim Zusammenfassen hilft – mit je einem schwachen und einem starken Prompt und der Erklärung, warum der Unterschied so groß ist.

---

## Beispiel 1: Einen langen Fachartikel zusammenfassen

**Schwacher Prompt:**

```
Fasse diesen Artikel zusammen. [Artikel eingefügt]
```

Das Modell liefert eine Zusammenfassung in mittlerer Länge, die ungefähr die Struktur des Artikels widerspiegelt. Für jemanden, der den Artikel verstehen will, ist das nützlich. Für jemanden, der eine konkrete Entscheidungsgrundlage braucht, meistens nicht.

---

**Starker Prompt:**

```
Ich bin Personalverantwortliche in einem mittelständischen Unternehmen. Ich habe diesen Artikel über hybrides Arbeiten gelesen und muss entscheiden, ob ich unserer Geschäftsführung eine Anpassung unserer Homeoffice-Richtlinie vorschlagen soll.

[Artikel eingefügt]

Fasse den Artikel so zusammen: (1) Was sind die wichtigsten Erkenntnisse für Unternehmen wie meines? (2) Welche Empfehlungen enthält der Artikel konkret? (3) Welche Einschränkungen oder Gegenargumente nennt der Artikel? Maximale Länge: eine halbe Seite.
```

**Was diese Eingabe besser macht:**
- Rolle: Personalverantwortliche, keine Forscherin
- Zweck: Entscheidungsgrundlage für Geschäftsführungs-Empfehlung
- Struktur: drei explizite Inhaltspunkte
- Umfang: max. eine halbe Seite

Die Zusammenfassung hat jetzt eine Funktion – und das Modell weißt, welche.

---

## Beispiel 2: Ein Meetingprotokoll strukturieren

**Schwacher Prompt:**

```
Fasse dieses Meeting zusammen. [Notizen eingefügt]
```

Das Modell liefert eine Zusammenfassung der Diskussion – aber das ist oft nicht das, was nach einem Meeting gebraucht wird. Was fehlt: Wer macht was? Was wurde entschieden? Was bleibt offen?

---

**Starker Prompt:**

```
Hier sind meine Notizen von einem Projektmeeting (45 Minuten, 6 Teilnehmende).

[Notizen eingefügt]

Erstelle daraus ein strukturiertes Protokoll mit diesen Abschnitten:
1. Entscheidungen: Was wurde beschlossen? (max. 5 Punkte)
2. Handlungspunkte: Wer macht was bis wann? (als Tabelle: Aufgabe | Person | Datum)
3. Offene Punkte: Was wurde nicht entschieden, was muss beim nächsten Meeting geklärt werden?

Wenn in meinen Notizen kein Datum oder keine Person für einen Handlungspunkt steht, markiere das mit [offen].
```

**Was diese Eingabe besser macht:**
- Klare Struktur mit drei Abschnitten
- Format für Handlungspunkte: Tabelle, nicht Fließtext
- Explizite Behandlung fehlender Informationen: [offen] statt erfinden

Das letzte Punkt ist wichtig: Wenn das Modell fehlende Informationen nicht markiert, kann es passieren, dass es Verantwortliche oder Daten erfindet – plausibel klingend, aber falsch.

---

## Beispiel 3: Mehrere Dokumente vergleichen

**Schwacher Prompt:**

```
Vergleiche diese zwei Angebote. [Zwei Dokumente eingefügt]
```

Das Modell listet Unterschiede auf – aber oft nicht nach den Kriterien, die für die eigene Entscheidung relevant sind.

---

**Starker Prompt:**

```
Ich vergleiche zwei Angebote für eine neue CRM-Software für unser 12-köpfiges Vertriebsteam. Angebot A kommt von Anbieter X, Angebot B von Anbieter Y.

[Beide Dokumente eingefügt]

Vergleiche die Angebote nach diesen Kriterien, die für uns wichtig sind:
- Preis (monatlich und einmalig)
- Anzahl der enthaltenen Nutzer und Kosten für zusätzliche
- Enthaltener Support (Reaktionszeit, Sprache, Kanal)
- Vertragslaufzeit und Kündigungsfristen
- Was explizit nicht im Angebot enthalten ist (Einrichtung, Schulung, Migration)

Format: Tabelle. Wenn ein Punkt in einem der Angebote nicht erwähnt wird, trage 'nicht angegeben' ein.
```

**Was diese Eingabe besser macht:**
- Kontext: 12-köpfiges Vertriebsteam, konkreter Kaufentscheid
- Kriterien: fünf explizit benannte, entscheidungsrelevante Punkte
- Format: Tabelle
- Behandlung fehlender Infos: „nicht angegeben" statt erfinden

Die Tabelle zeigt auf einen Blick, wo die Angebote verglichen werden können – und wo Informationen fehlen, die man beim Anbieter nachfragen muss.

---

## Übung

Nimm ein Dokument aus deiner Arbeit, das du zuletzt gelesen hast – einen langen E-Mail-Thread, ein Meeting-Protokoll, einen Bericht.

Formuliere einen Prompt mit: Für wen ist die Zusammenfassung? Was soll die Person danach wissen? Welches Format und welcher Umfang sind sinnvoll?

Dann vergleiche das Ergebnis mit dem Original: Was hat das Modell weggelassen, das wichtig gewesen wäre? Was steht drin, das für den Zweck gar nicht relevant ist?
