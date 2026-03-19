---
title: Wie KI eigentlich funktioniert
description: Das Minimum, das man verstehen muss, um KI produktiv einzusetzen.
layout: default
parent: Kernmodule
nav_order: 2
---

# Wie KI eigentlich funktioniert

Du musst kein Informatikstudium haben, um KI sinnvoll nutzen zu können. Aber ein Grundverständnis davon, was im Hintergrund passiert, verhindert viele Fehler – und erklärt, warum KI manchmal überraschend gut und manchmal überraschend schlecht ist.

---

## Nicht Wissen, sondern Wahrscheinlichkeit

Das Wichtigste zuerst: KI-[Sprachmodelle](../glossar#sprachmodell) speichern keine Fakten. Sie sind keine Datenbanken, die Du abfragst. Sie sind auch keine Suchmaschinen.

Ein [Sprachmodell](../glossar#sprachmodell) hat während des [Trainings](../glossar#training) sehr viele Texte gelesen – Bücher, Webseiten, Artikel, Gespräche. Daraus hat es gelernt, wie Sprache funktioniert: welche Wörter zusammen vorkommen, wie Sätze gebaut sind, wie Themen zusammenhängen. Was es dabei nicht gelernt hat, ist: was stimmt und was nicht.

Wenn Du dem Modell eine Frage stellst, berechnet es, welche Zeichenfolge als Antwort am wahrscheinlichsten ist – basierend auf allem, was es während des [Trainings](../glossar#training) gesehen hat. Es „denkt" nicht nach, es sagt nicht: „Ich weiß das." Es sagt: „Dieser Text passt statistisch gut auf diese Eingabe."

Das ist der Grund, warum KI-Texte sprachlich oft überzeugend klingen – auch wenn sie sachlich falsch sind. Sprachliche Plausibilität und inhaltliche Richtigkeit sind zwei verschiedene Dinge.

---

## Wie Text verarbeitet wird: Token

Sprachmodelle arbeiten nicht mit ganzen Wörtern oder Sätzen, sondern mit [Token](../glossar#token). Ein Token ist eine kleine Einheit – manchmal ein ganzes Wort, manchmal nur ein Teil davon, manchmal ein Satzzeichen.

Das Wort „Bundesverfassungsgericht" wird beispielsweise in mehrere Token aufgeteilt. Das Modell sieht nicht das Wort als Ganzes, sondern eine Folge von kleineren Einheiten – und verarbeitet sie Schritt für Schritt.

Warum ist das relevant? Weil Modelle nur eine begrenzte Anzahl von Token gleichzeitig verarbeiten können. Das nennt sich [Kontextfenster](../glossar#kontextfenster). Sehr lange Dokumente, sehr lange Gespräche oder viele mitgelieferte Texte können dieses Limit überschreiten – dann „vergisst" das Modell frühere Teile des Gesprächs.

Für die meisten Aufgaben ist das kein Problem. Bei langen Projekten oder komplexen Analysen ist es gut zu wissen, dass das Modell nicht unbegrenzt „zuhört".

---

## Was das Modell weiß – und was nicht

[Modelle](../glossar#modell) wurden auf Daten bis zu einem bestimmten Zeitpunkt trainiert. Was danach passiert ist, ist ihnen unbekannt – es sei denn, Du gibst es ihnen in der Eingabe mit. Wer nach aktuellen Ereignissen, neuen Gesetzen oder dem Stand eines laufenden Projekts fragt, bekommt entweder eine veraltete Antwort oder – schlimmer – eine erfundene, die sich plausibel anhört.

Außerdem: Was im Training stand, war nicht immer korrekt. Das Internet, auf dem viele Modelle trainiert wurden, enthält Fehler, Meinungen, Widersprüche und Halbwahrheiten. Das Modell hat gelernt, wie häufig bestimmte Aussagen im Text vorkommen – nicht, ob sie stimmen.

Das führt zu [Halluzinationen](../glossar#halluzination): Das Modell erfindet Studien, die nicht existieren. Es nennt Namen von Personen, die die beschriebene Position nie hatten. Es gibt Gesetze mit dem falschen Inhalt wieder. Nicht weil es lügt – es hat kein Bewusstsein, das lügen könnte – sondern weil seine Antwort das ist, was nach dem Trainingsmuster am wahrscheinlichsten klingt.

---

## Was Du daraus mitnimmst

Diese drei Punkte sind das Minimum:

KI prüft keine Fakten. Wer Informationen braucht, auf die es ankommt, muss sie selbst verifizieren – unabhängig davon, wie überzeugend der Text klingt.

KI kennt Deine Situation nicht. Was das Modell über das konkrete Projekt, die Absicht oder den Empfänger wissen soll, muss in der Eingabe stehen – es erschließt sich nichts von selbst.

KI ist keine Suchmaschine. Du fragst nicht, um Fakten abzurufen. Du gibst eine Aufgabe – und bekommst eine sprachlich verarbeitete Ausgabe, die Du einordnen und prüfen musst.

Das klingt nach Einschränkungen. Das sind auch Einschränkungen. Aber innerhalb dieser Grenzen ist KI außerordentlich nützlich – wenn Du weißt, wie Du die Eingabe gestaltest. Darum geht es im nächsten Modul.
