---
title: "RAG: Konzept & Funktionsweise"
description: Was RAG ist, wie die Suche technisch funktioniert und warum das mehr ist als eine Stichwortsuche.
layout: default
parent: RAG – Retrieval-Augmented Generation
grand_parent: Vertiefung
nav_order: 1
---

# Konzept & Funktionsweise

## Was RAG ist

[RAG](../../glossar#rag) steht für Retrieval-Augmented Generation – auf Deutsch: abrufverstärkte Generierung. Der Begriff beschreibt ein Verfahren, bei dem ein KI-System vor dem Generieren einer Antwort zunächst in einer Wissensdatenbank sucht und die gefundenen Inhalte in den [Kontext](../../glossar#kontext) einbindet.

Der Ablauf in drei Schritten:

1. **Suche:** Eine Frage kommt herein. Das System sucht in einer vorbereiteten Wissensdatenbank nach den Abschnitten, die am ehesten zur Frage passen.
2. **Einbindung:** Die gefundenen Abschnitte werden in den Kontext des Modells geladen – zusammen mit der ursprünglichen Frage.
3. **Antwort:** Das Modell beantwortet die Frage auf Basis der gefundenen Inhalte.

Das Modell selbst bleibt unverändert. Es wird nicht neu trainiert. Es bekommt nur im richtigen Moment die richtigen Informationen.

---

## Eine Analogie

Stellen Sie sich vor, jemand fragt Sie nach einem Detail aus einem Vertrag, den Sie vor drei Jahren abgeschlossen haben. Sie erinnern sich nicht an alles – aber Sie wissen, wo Sie suchen müssen. Sie schlagen nach, lesen den relevanten Abschnitt und antworten dann auf Basis dessen, was dort steht.

Genau das macht RAG: Es schlägt nach. Das Modell antwortet nicht aus dem Gedächtnis, sondern aus dem, was es gerade gefunden hat.

---

## Wie RAG technisch funktioniert

Um zu verstehen, was RAG leisten kann und was nicht, hilft ein Blick auf den technischen Aufbau.

**Dokumente werden in Abschnitte aufgeteilt.** Bevor das System suchen kann, müssen die Dokumente aufbereitet werden. Sie werden in kleine Blöcke aufgeteilt – sogenannte Chunks. Ein Chunk ist typischerweise ein Absatz oder ein thematischer Block, nicht das ganze Dokument.

**Jeder Abschnitt bekommt eine numerische Darstellung.** Ein Sprachmodell wandelt jeden Chunk in einen Zahlenvektor um – ein sogenanntes Embedding. Dieser Vektor beschreibt den semantischen Inhalt des Textes: was er bedeutet, nicht nur welche Wörter er enthält. Ähnliche Inhalte liegen im Vektorraum nah beieinander.

**Suche funktioniert über Bedeutungsähnlichkeit.** Wenn eine Frage gestellt wird, bekommt auch die Frage ein Embedding. Das System sucht dann nach den Chunks, deren Vektoren der Frage am ähnlichsten sind. Das ist keine Stichwortsuche – es ist eine Bedeutungssuche. „Wie hoch ist die Karenzzeit?" findet auch Abschnitte, in denen das Wort „Karenzzeit" nicht vorkommt, der Begriff aber umschrieben wird.

**Die Treffer landen im Kontext.** Die ähnlichsten Chunks werden zusammen mit der Frage an das Modell übergeben. Das Modell antwortet auf Basis dieser Abschnitte.
