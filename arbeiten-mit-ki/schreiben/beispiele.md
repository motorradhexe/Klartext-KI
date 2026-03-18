---
title: "Schreiben: Beispiele"
description: Drei Schreibsituationen mit je einem schwachen und einem starken Prompt – und der Erklärung des Unterschieds.
layout: default
parent: Mit KI schreiben
grand_parent: Mit KI arbeiten
nav_order: 2
---

# Beispiele: Vorher / Nachher für verschiedene Schreibsituationen

Drei häufige Schreibsituationen – jede mit einem schwachen Prompt, einem starken Prompt und der Erklärung, warum der Unterschied so groß ist.

---

## Beispiel 1: Entschuldigungsmail nach einem Fehler

**Schwacher Prompt:**

> „Schreib eine Entschuldigungsmail an einen Kunden."

Das Modell schreibt eine freundliche, entschuldigende E-Mail, die gut klingt und für jeden und keinen passt. Sie könnte an jeden Kunden mit jeder Beschwerde gehen. Generisch, austauschbar, ohne Haltung.

---

**Starker Prompt:**

> „Ich bin Kundenbetreuer bei einem Softwareunternehmen. Ein langjähriger Kunde hat sich per E-Mail beschwert, dass ein Feature seit zwei Wochen nicht mehr funktioniert. Er hat dadurch Zeit verloren und klingt genervt, aber nicht aggressiv. Wir haben den Fehler gestern identifiziert und werden ihn voraussichtlich morgen beheben.
>
> Schreib eine knappe E-Mail (max. 5 Sätze), die: (1) den Stand erklärt, (2) sich ohne Übertreibung entschuldigt, (3) einen konkreten Zeitplan nennt. Ton: professionell, direkt, ohne Floskeln."

**Was diese Eingabe besser macht:**
- Rolle der schreibenden Person: Kundenbetreuer
- Kontext der Situation: langjähriger Kunde, Art des Problems, Dauer
- Emotionale Lage: genervt, nicht aggressiv
- Stand der Lösung: gefunden, morgen behoben
- Format: max. 5 Sätze, drei konkrete Inhaltspunkte
- Ton: professionell, direkt, keine Floskeln

Der Unterschied liegt nicht in der Länge des Prompts, sondern im Informationsgehalt. Jede Angabe reduziert den Spielraum für generische Antworten.

---

## Beispiel 2: Interner Bericht nach einem Projektabschluss

**Schwacher Prompt:**

> „Schreib einen Projektabschlussbericht."

Das Modell liefert eine Vorlage mit Standardabschnitten: Ziel, Ergebnis, Learnings. Sprachlich korrekt, inhaltlich leer – weil das Modell nichts über das Projekt weiß.

---

**Starker Prompt:**

> „Wir haben gerade ein dreimonatiges Projekt abgeschlossen: Einführung eines neuen CRM-Systems für unser Vertriebsteam (15 Personen). Das Projekt war insgesamt erfolgreich, aber zwei Wochen im Verzug wegen Datenmigrationsproblemen. Das System läuft jetzt stabil, und das Team hat es gut angenommen.
>
> Schreib einen internen Abschlussbericht (ca. eine Seite) für die Geschäftsführung. Sie kennt das Projekt, interessiert sich aber vor allem für: Was hat funktioniert? Was hat den Verzug verursacht, und wie wurde es gelöst? Was würden wir beim nächsten Mal anders machen? Sachlicher Ton, keine Rechtfertigung, keine Selbstkritik-Performance."

**Was diese Eingabe besser macht:**
- Projektinhalt: CRM-Einführung, 15 Personen, drei Monate
- Ergebnis: erfolgreich, aber zwei Wochen Verzug
- Ursache: Datenmigrationsprobleme – benannt, nicht erklärt
- Zielgruppe: Geschäftsführung, kennt das Projekt
- Erkenntnisinteresse: drei konkrete Punkte
- Ton: sachlich, nicht defensiv

Das Modell kann jetzt etwas schreiben, das tatsächlich über dieses Projekt handelt – nicht über irgendein Projekt.

---

## Beispiel 3: Dokumentation einer technischen Entscheidung

**Schwacher Prompt:**

> „Schreib eine Dokumentation über unsere Datenbanklösung."

Das Modell schreibt entweder etwas Allgemeines über Datenbankkonzepte oder fragt zurück. In jedem Fall hilft es ohne Kontext nicht.

---

**Starker Prompt:**

> „Ich muss dokumentieren, warum wir uns für PostgreSQL und gegen MongoDB entschieden haben. Die Entscheidung fiel vor drei Monaten. Hauptgründe: unsere Daten sind stark relational, das Team hat mehr Erfahrung mit SQL, und wir wollten kein neues Ökosystem einführen. MongoDB war attraktiv wegen der flexiblen Schemas, aber das war für uns kein ausreichender Vorteil.
>
> Schreib eine knappe technische Entscheidungsdokumentation (Architecture Decision Record, ADR) im Stil: Kontext, Entscheidung, Begründung, abgewogene Alternativen, Konsequenzen. Für ein technisches Team, das die Entscheidung später nachvollziehen soll. Max. 300 Wörter."

**Was diese Eingabe besser macht:**
- Klares Thema: PostgreSQL vs. MongoDB
- Hauptgründe: drei Punkte, konkret benannt
- Abgewogene Alternative: benannt, mit dem Argument, das dagegen sprach
- Format: ADR-Struktur mit benannten Abschnitten
- Zielgruppe: technisches Team, retrospektiv
- Umfang: max. 300 Wörter

Ein ADR ist ein Dokument, das erklärt, warum eine technische Entscheidung so getroffen wurde. Wer das dem Modell sagt, bekommt genau das.

---

## Übung

Nimm einen Text, den du in letzter Zeit geschrieben hast – eine E-Mail, einen Bericht, eine kurze Zusammenfassung. Formuliere einen Prompt, der alle wesentlichen Kontextinformationen enthält, und lass KI einen Entwurf schreiben.

Vergleiche das Ergebnis mit deinem eigenen Text. Dann überarbeite: entweder den Prompt, wenn das Ergebnis noch nicht passt – oder das KI-Ergebnis per Folgeprompt, bis es wirklich deinem Standard entspricht.
