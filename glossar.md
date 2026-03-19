---
title: Glossar
description: Alle Fachbegriffe, die im Projekt vorkommen – erklärt ohne Vorwissen.
layout: default
nav_order: 6
---

# Glossar

Hier sind alle Begriffe erklärt, die im Projekt vorkommen. Wer einen Begriff zum ersten Mal sieht, landet hier. Wer alles verstanden hat, braucht diese Seite nie zu lesen.

---

<div class="glossar-eintrag" id="prompt" markdown="1">

## Prompt

Ein Prompt ist die Eingabe, die Du an ein KI-System schickst. Der Begriff kommt aus dem Englischen und bedeutet so viel wie „Anstoß" oder „Aufforderung". Alles, was Du ins Textfeld tippst – eine Frage, ein Auftrag, ein Beispiel – ist ein Prompt.

**Beispiel:** „Erkläre mir, wie eine Suchmaschine funktioniert" ist ein Prompt. Die Antwort der KI darauf nicht.

Der Prompt ist entscheidend für die Qualität der Antwort. Dasselbe Modell liefert auf einen vagen Prompt eine vage Antwort – und auf einen präzisen Prompt eine präzise.

</div>

<div class="glossar-eintrag" id="token" markdown="1">

## Token

Ein Token ist die kleinste Einheit, in der KI-Modelle Text verarbeiten. Das sind keine ganzen Wörter, sondern Teile davon – oder manchmal auch Zeichen und Zeichengruppen. Das Wort „Zusammenhang" kann zum Beispiel in mehrere Token aufgeteilt werden.

**Beispiel:** Das Modell sieht nicht den Satz „Das ist ein Test" als Ganzes, sondern eine Folge von Token: „Das", „ist", „ein", „Test" – wobei die genaue Aufteilung vom Modell abhängt.

Warum ist das relevant? Weil KI-Modelle eine begrenzte Anzahl von Token auf einmal verarbeiten können. Das nennt sich [Kontextfenster](#kontextfenster). Sehr lange Texte oder sehr lange Gespräche können das Limit überschreiten.

</div>

<div class="glossar-eintrag" id="kontext" markdown="1">

## Kontext

Mit Kontext ist gemeint, welche Informationen das KI-Modell bei der Erstellung einer Antwort zur Verfügung hat. Das ist nicht nur die aktuelle Frage, sondern alles: der bisherige Gesprächsverlauf, mitgelieferte Dokumente, Anweisungen am Anfang.

**Beispiel:** Wenn Du fragst „Was meinst Du damit?", kann das Modell nur antworten, wenn es aus dem Kontext weiß, worauf sich „damit" bezieht. Ohne diesen Kontext rät es – und liegt oft falsch.

Ein häufiger Fehler: Du setzt voraus, dass das Modell Informationen kennt, die Du selbst im Kopf hast, aber nicht eingegeben hast. Das Modell hat zwar umfangreiches Trainingswissen – aber nichts über Deine eigene Situation, das konkrete Projekt oder die Absicht hinter einer Anfrage. Was situationsspezifisch ist, musst Du mitgeben.

</div>

<div class="glossar-eintrag" id="sprachmodell" markdown="1">

## Sprachmodell

Ein Sprachmodell ist ein KI-System, das darauf trainiert wurde, Text zu verarbeiten und zu erzeugen. Es liest eine Eingabe und berechnet, welcher Text als Fortsetzung oder Antwort am wahrscheinlichsten ist. Ein Sprachmodell speichert keine Fakten und denkt nicht nach – es berechnet.

**Beispiel:** ChatGPT, Claude und Gemini sind Produkte, die auf Sprachmodellen basieren. Das Sprachmodell ist der Kern, der die eigentliche Textverarbeitung übernimmt.

Der Begriff „Sprachmodell" betont, dass diese Systeme auf Sprache spezialisiert sind – im Unterschied zu KI-Systemen, die Bilder erkennen, Musik erzeugen oder Schach spielen.

</div>

<div class="glossar-eintrag" id="training" markdown="1">

## Training

Mit Training ist der Prozess gemeint, durch den ein Sprachmodell lernt. Dabei liest das System sehr große Mengen an Text – Bücher, Webseiten, Artikel – und lernt daraus, welche Wörter und Sätze wie zusammenpassen. Dieser Prozess findet einmalig (oder in Schüben) statt und ist abgeschlossen, bevor Du das Modell nutzt.

**Beispiel:** Ein Modell wurde bis Ende 2024 trainiert. Was danach passiert ist, kennt es nicht – es sei denn, Du gibst es ihm in der Eingabe mit.

Training ist kein Lernen im menschlichen Sinne. Das Modell merkt sich keine Gespräche und verbessert sich nicht durch die eigene Nutzung. Jedes neue Gespräch beginnt ohne Erinnerung an vorherige.

</div>

<div class="glossar-eintrag" id="kontextfenster" markdown="1">

## Kontextfenster

Das Kontextfenster ist die Obergrenze dafür, wie viel Text ein Sprachmodell auf einmal verarbeiten kann. Alles, was außerhalb dieser Grenze liegt – weil es zu weit zurückliegt oder der Text zu lang ist –, sieht das Modell nicht mehr.

**Beispiel:** In einem langen Gespräch kann es passieren, dass das Modell frühe Teile der Unterhaltung nicht mehr berücksichtigt, weil sie das Kontextfenster verlassen haben. Es antwortet dann so, als hättest Du diese Dinge nie gesagt.

Die Größe des Kontextfensters unterscheidet sich je nach Modell. Für die meisten alltäglichen Aufgaben ist das Limit kein Problem – bei sehr langen Dokumenten oder ausgedehnten Gesprächen wird es relevant.

</div>

<div class="glossar-eintrag" id="modell" markdown="1">

## Modell

Ein Modell ist das eigentliche KI-System – der trainierte Kern, der Text verarbeitet und erzeugt. Modelle haben Namen wie GPT-4, Claude oder Gemini. Jedes Modell wurde auf unterschiedlichen Daten trainiert und hat andere Stärken und Schwächen.

**Beispiel:** ChatGPT ist eine Oberfläche. Das Modell dahinter heißt GPT-4 (oder eine andere Version). Zwei verschiedene Produkte können dasselbe Modell verwenden – und zwei verschiedene Modelle können auf derselben Oberfläche angeboten werden.

Für die meisten Anwendungen ist die Modellwahl weniger entscheidend als die Qualität des Prompts. Ein sehr gutes Modell mit einem schlechten Prompt liefert oft schlechtere Ergebnisse als ein einfacheres Modell mit einem klaren Prompt.

</div>

<div class="glossar-eintrag" id="halluzination" markdown="1">

## Halluzination

Halluzination beschreibt das Phänomen, dass KI-Modelle Aussagen machen, die faktisch falsch sind – und das mit derselben Selbstsicherheit, mit der sie richtige Aussagen machen. Das Modell „erfindet" keine Lügen im menschlichen Sinne. Es produziert Text, der plausibel klingt, aber nicht stimmt.

**Beispiel:** Fragst Du ein Modell nach einer wissenschaftlichen Studie zu einem Nischenthema, kann es eine Studie nennen, die so nie existiert hat – mit korrektem Titel, Autornamen und Erscheinungsjahr.

Halluzinationen entstehen, weil Modelle keine Fakten abrufen, sondern Wahrscheinlichkeiten berechnen: Welches Wort folgt sinnvoll auf das vorherige? Das führt zu flüssigem, klingendem Text – der manchmal einfach falsch ist. Kritische Informationen immer selbst überprüfen.

</div>

<div class="glossar-eintrag" id="iteration" markdown="1">

## Iteration

Iteration bedeutet: einen Prozess wiederholen und dabei verbessern. In der Arbeit mit KI heißt das, ein erstes Ergebnis nicht sofort zu akzeptieren, sondern es als Ausgangspunkt zu nutzen – und durch gezielte Folgeprompts besser zu machen.

**Beispiel:** Du bekommst einen Textentwurf, der zu förmlich klingt. Statt ihn zu verwerfen, schreibst Du: „Schreib das informeller um, wie in einem Brief an einen Kollegen." Das ist Iteration.

Wer erwartet, dass ein erster Prompt das perfekte Ergebnis liefert, wird häufig enttäuscht sein. KI funktioniert besser als Dialog als als Befehlsautomat.

</div>

<div class="glossar-eintrag" id="ausgabe" markdown="1">

## Ausgabe

Die Ausgabe ist das, was das KI-Modell als Antwort auf einen Prompt produziert. Das kann ein Text sein, ein Codeausschnitt, eine Liste, eine Übersetzung oder eine Zusammenfassung – je nachdem, was Du angefragt hast.

**Beispiel:** Du gibst den Prompt „Fasse diesen Artikel in drei Sätzen zusammen" ein und bekommst drei Sätze zurück. Diese drei Sätze sind die Ausgabe.

Die Ausgabe hängt vollständig vom Prompt und vom Kontext ab. Keine Ausgabe ist „die richtige" – es gibt immer viele mögliche Antworten auf einen Prompt. Wenn eine Ausgabe nicht passt, liegt das fast immer daran, dass der Prompt zu vage oder zu wenig kontextuell war.

</div>

<div class="glossar-eintrag" id="agent" markdown="1">

## Agent

Ein Agent ist ein KI-System, das nicht nur antwortet, sondern selbstständig handelt. Es bekommt ein Ziel und arbeitet dann eigenständig daran – indem es Werkzeuge nutzt, Zwischenergebnisse bewertet und weitere Schritte plant, ohne dass ein Mensch jeden Schritt manuell auslöst.

**Beispiel:** Ein Agent bekommt den Auftrag, die drei günstigsten Hosting-Anbieter in Deutschland zu recherchieren und eine Vergleichstabelle zu erstellen. Er sucht selbstständig im Web, liest Seiten, extrahiert Preise und liefert das Ergebnis.

Der Unterschied zur normalen KI-Nutzung: Du gibst nicht jede Zwischenfrage ein. Der Agent entscheidet selbst, welche Schritte nötig sind – und kann dabei auch Fehler machen, die sich unbemerkt durch weitere Schritte fortsetzen.

→ Ausführliche Erklärung: [KI-Agents](vertiefung/agents)

</div>

<div class="glossar-eintrag" id="rag" markdown="1">

## RAG

RAG steht für Retrieval-Augmented Generation (auf Deutsch: abrufverstärkte Generierung). Es bezeichnet ein Verfahren, bei dem ein KI-System vor dem Generieren einer Antwort gezielt in einer Wissensdatenbank sucht und nur die gefundenen, relevanten Abschnitte in den Kontext lädt.

**Beispiel:** Statt alle Unternehmenshandbücher in den Kontext zu laden, sucht das System bei jeder Anfrage nur nach den Abschnitten, die zur Frage passen – und gibt diese an das Modell weiter. Das Modell antwortet dann auf Basis dieser Abschnitte.

RAG ermöglicht es, KI auf spezifische, aktuelle oder interne Wissensbestände anzuwenden, ohne das Modell neu zu trainieren. Es reduziert [Halluzinationen](#halluzination), schließt sie aber nicht aus.

→ Ausführliche Erklärung: [RAG](vertiefung/rag)

</div>

<div class="glossar-eintrag" id="mcp" markdown="1">

## MCP

MCP steht für Model Context Protocol. Es ist ein offener Standard, der beschreibt, wie KI-Modelle mit externen Werkzeugen und Datenquellen kommunizieren können – zum Beispiel um Dateien zu lesen, Datenbanken abzufragen oder Kalender einzusehen.

**Beispiel:** Eine KI-Anwendung kann über MCP auf das lokale Dateisystem zugreifen und ein Dokument direkt öffnen, lesen und bearbeiten – ohne dass Du den Inhalt manuell hineinkopieren musst.

MCP wurde von Anthropic entwickelt und ist offen: andere Hersteller und Entwickler können den Standard verwenden. Es ist kein Modell und keine Anwendung, sondern eine Vereinbarung darüber, wie Systeme miteinander sprechen.

→ Ausführliche Erklärung: [MCP](vertiefung/mcp)

</div>

<div class="glossar-eintrag" id="framework" markdown="1">

## Framework

Ein Framework (auf Deutsch: Grundgerüst oder Rahmenwerk) ist eine fertige Sammlung von Code-Bausteinen, die eine bestimmte Art von Anwendung strukturieren. Wer eine Web-Anwendung baut, muss nicht alles von Null anfangen: Ein Framework übernimmt zum Beispiel grundlegende Aufgaben wie das Empfangen von Anfragen, das Weiterleiten zu verschiedenen Seiten oder die Verwaltung von Nutzerdaten.

**Beispiel:** Django und Flask sind bekannte Python-Frameworks für Webanwendungen. Wer Django nutzt, baut auf einem bestimmten Grundgerüst auf – das Modell muss das wissen, damit der Code dazu passt.

Der Unterschied zu einer Bibliothek (auch: Library): Eine Bibliothek stellt einzelne Werkzeuge bereit, die Du bei Bedarf aufrufst. Ein Framework gibt die Struktur vor, in die Du eigenen Code einfügst.

</div>

<div class="glossar-eintrag" id="import" markdown="1">

## Import

Mit einem Import bindest Du in einer Programmdatei Code ein, der woanders definiert ist – zum Beispiel eine fertige Funktionssammlung (Bibliothek) oder ein anderes Modul des eigenen Projekts. Imports stehen meist am Anfang einer Datei und geben an, welche externen Bausteine der Code verwendet.

**Beispiel:** `import datetime` in Python bindet die eingebaute Datumsfunktion ein. Danach kannst Du sie im Code nutzen – ohne sie selbst schreiben zu müssen.

Für KI relevant: Wenn Du Code schreiben lässt, ohne die vorhandenen Imports anzugeben, kann das Modell Funktionen verwenden, die im Projekt gar nicht eingebunden sind – und der Code funktioniert dann nicht.

</div>

<div class="glossar-eintrag" id="docstring" markdown="1">

## Docstring

Ein Docstring (von: Documentation String) ist ein Kommentar in einem festgelegten Format, der direkt in einer Funktion oder einem Modul steht und erklärt, was dieser Code tut, welche Eingaben er erwartet und was er zurückgibt. In Python wird er mit dreifachen Anführungszeichen geschrieben.

**Beispiel:**
```python
def sortiere_personen(personen):
    """Sortiert eine Liste von Personen nach Alter, dann nach Name."""
    ...
```

Docstrings sind für Menschen gedacht, nicht für den Computer – der ignoriert sie beim Ausführen. Sie helfen, Code verständlich zu halten, auch wenn Du ihn Wochen später wieder liest. Viele Werkzeuge lesen Docstrings aus, um automatisch Dokumentation zu erzeugen.

</div>
