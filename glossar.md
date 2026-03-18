---
title: Glossar
description: Alle Fachbegriffe, die im Projekt vorkommen – erklärt ohne Vorwissen.
layout: default
nav_order: 99
---

# Glossar

Hier sind alle Begriffe erklärt, die im Projekt vorkommen. Wer einen Begriff zum ersten Mal sieht, landet hier. Wer alles verstanden hat, braucht diese Seite nie zu lesen.

---

<div class="glossar-eintrag" id="prompt">

## Prompt

Ein Prompt ist die Eingabe, die man an ein KI-System schickt. Der Begriff kommt aus dem Englischen und bedeutet so viel wie „Anstoß" oder „Aufforderung". Alles, was man ins Textfeld tippt – eine Frage, ein Auftrag, ein Beispiel – ist ein Prompt.

**Beispiel:** „Erkläre mir, wie eine Suchmaschine funktioniert" ist ein Prompt. Die Antwort der KI darauf nicht.

Der Prompt ist entscheidend für die Qualität der Antwort. Dasselbe Modell liefert auf einen vagen Prompt eine vage Antwort – und auf einen präzisen Prompt eine präzise.

</div>

<div class="glossar-eintrag" id="token">

## Token

Ein Token ist die kleinste Einheit, in der KI-Modelle Text verarbeiten. Das sind keine ganzen Wörter, sondern Teile davon – oder manchmal auch Zeichen und Zeichengruppen. Das Wort „Zusammenhang" kann zum Beispiel in mehrere Token aufgeteilt werden.

**Beispiel:** Das Modell sieht nicht den Satz „Das ist ein Test" als Ganzes, sondern eine Folge von Token: „Das", „ist", „ein", „Test" – wobei die genaue Aufteilung vom Modell abhängt.

Warum ist das relevant? Weil KI-Modelle eine begrenzte Anzahl von Token auf einmal verarbeiten können. Das nennt man das [Kontextfenster](#kontext). Sehr lange Texte oder sehr lange Gespräche können das Limit überschreiten.

</div>

<div class="glossar-eintrag" id="kontext">

## Kontext

Mit Kontext ist gemeint, welche Informationen das KI-Modell bei der Erstellung einer Antwort zur Verfügung hat. Das ist nicht nur die aktuelle Frage, sondern alles: der bisherige Gesprächsverlauf, mitgelieferte Dokumente, Anweisungen am Anfang.

**Beispiel:** Wenn man fragt „Was meinst du damit?", kann das Modell nur antworten, wenn es aus dem Kontext weiß, worauf sich „damit" bezieht. Ohne diesen Kontext rät es – und liegt oft falsch.

Ein häufiger Fehler: Man setzt voraus, dass das Modell Informationen kennt, die man selbst im Kopf hat, aber nicht eingegeben hat. KI kennt nur, was im Kontext steht.

</div>

<div class="glossar-eintrag" id="modell">

## Modell

Ein Modell ist das eigentliche KI-System – der trainierte Kern, der Text verarbeitet und erzeugt. Modelle haben Namen wie GPT-4, Claude oder Gemini. Jedes Modell wurde auf unterschiedlichen Daten trainiert und hat andere Stärken und Schwächen.

**Beispiel:** ChatGPT ist eine Oberfläche. Das Modell dahinter heißt GPT-4 (oder eine andere Version). Zwei verschiedene Produkte können dasselbe Modell verwenden – und zwei verschiedene Modelle können auf derselben Oberfläche angeboten werden.

Für die meisten Anwendungen ist die Modellwahl weniger entscheidend als die Qualität des Prompts. Ein sehr gutes Modell mit einem schlechten Prompt liefert oft schlechtere Ergebnisse als ein einfacheres Modell mit einem klaren Prompt.

</div>

<div class="glossar-eintrag" id="halluzination">

## Halluzination

Halluzination beschreibt das Phänomen, dass KI-Modelle Aussagen machen, die faktisch falsch sind – und das mit derselben Selbstsicherheit, mit der sie richtige Aussagen machen. Das Modell „erfindet" keine Lügen im menschlichen Sinne. Es produziert Text, der plausibel klingt, aber nicht stimmt.

**Beispiel:** Fragt man ein Modell nach einer wissenschaftlichen Studie zu einem Nischenthema, kann es eine Studie nennen, die so nie existiert hat – mit korrektem Titel, Autornamen und Erscheinungsjahr.

Halluzinationen entstehen, weil Modelle keine Fakten abrufen, sondern Wahrscheinlichkeiten berechnen: Welches Wort folgt sinnvoll auf das vorherige? Das führt zu flüssigem, klingendem Text – der manchmal einfach falsch ist. Kritische Informationen immer selbst überprüfen.

</div>

<div class="glossar-eintrag" id="iteration">

## Iteration

Iteration bedeutet: einen Prozess wiederholen und dabei verbessern. In der Arbeit mit KI heißt das, ein erstes Ergebnis nicht sofort zu akzeptieren, sondern es als Ausgangspunkt zu nutzen – und durch gezielte Folgeprompts besser zu machen.

**Beispiel:** Man bekommt einen Textentwurf, der zu förmlich klingt. Statt ihn zu verwerfen, schreibt man: „Schreib das informeller um, wie in einem Brief an einen Kollegen." Das ist Iteration.

Wer erwartet, dass ein erster Prompt das perfekte Ergebnis liefert, wird häufig enttäuscht sein. KI funktioniert besser als Dialog als als Befehlsautomat.

</div>

<div class="glossar-eintrag" id="ausgabe">

## Ausgabe

Die Ausgabe ist das, was das KI-Modell als Antwort auf einen Prompt produziert. Das kann ein Text sein, ein Codeausschnitt, eine Liste, eine Übersetzung oder eine Zusammenfassung – je nachdem, was man angefragt hat.

**Beispiel:** Man gibt den Prompt „Fasse diesen Artikel in drei Sätzen zusammen" ein und bekommt drei Sätze zurück. Diese drei Sätze sind die Ausgabe.

Die Ausgabe hängt vollständig vom Prompt und vom Kontext ab. Keine Ausgabe ist „die richtige" – es gibt immer viele mögliche Antworten auf einen Prompt. Wenn eine Ausgabe nicht passt, liegt das fast immer daran, dass der Prompt zu vage oder zu wenig kontextuell war.

</div>
