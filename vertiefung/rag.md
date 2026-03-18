---
title: RAG – Retrieval-Augmented Generation
description: Wie KI auf eigene Wissensbestände zugreift, ohne alles in den Kontext laden zu müssen.
layout: default
parent: Vertiefung
nav_order: 2
---

# RAG – Retrieval-Augmented Generation

KI-Modelle wissen viel – aber nicht alles. Sie kennen das nicht, was nach ihrem Trainingsdatum passiert ist. Sie kennen nicht die internen Dokumente eines Unternehmens. Sie kennen nicht die spezifischen Regelungen einer bestimmten Organisation.

Die naheliegende Lösung: alles in den [Kontext](../glossar#kontext) laden. Das funktioniert bis zu einem gewissen Umfang. Aber [Kontextfenster](../glossar#kontextfenster) haben Grenzen, und hunderte Dokumente hineinzuladen ist langsam, teuer und unübersichtlich.

RAG löst dieses Problem: Anstatt alle Dokumente zu laden, sucht das System gezielt nach den relevanten Stellen – und gibt nur diese an das Modell weiter.

---

## Was RAG ist

[RAG](../glossar#rag) steht für Retrieval-Augmented Generation. Auf Deutsch: abrufverstärkte Generierung. Der Begriff beschreibt ein Verfahren, bei dem ein KI-System vor dem Generieren einer Antwort zunächst in einer Wissensdatenbank sucht und die gefundenen Inhalte in den Kontext einbindet.

Der Ablauf in drei Schritten:

1. **Suche:** Eine Frage kommt herein. Das System sucht in einer vorbereiteten Wissensdatenbank nach den Abschnitten, die am ehesten zur Frage passen.
2. **Einbindung:** Die gefundenen Abschnitte werden in den Kontext des Modells geladen – zusammen mit der ursprünglichen Frage.
3. **Antwort:** Das Modell beantwortet die Frage auf Basis der gefundenen Inhalte.

Das Modell selbst bleibt unverändert. Es wird nicht neu trainiert. Es bekommt nur im richtigen Moment die richtigen Informationen.

---

## Eine Analogie

Stellen Sie sich vor, jemand fragt Sie nach einem Detail aus einem Vertrag, den Sie vor drei Jahren abgeschlossen haben. Sie erinnern sich nicht an alles – aber Sie wissen, wo Sie suchen müssen. Sie schlagen nach, lesen den relevanten Abschnitt, und antworten dann.

Genau das macht RAG: Es schlägt nach. Das Modell antwortet nicht aus dem Gedächtnis, sondern aus dem, was es gerade gefunden hat.

---

## Wofür RAG nützlich ist

RAG macht KI dort nützlich, wo spezifisches, aktuelles oder internes Wissen gefragt ist:

- **Unternehmensinterne Wissensdatenbanken:** Ein System, das Handbücher, Richtlinien und Prozessdokumentationen kennt und konkrete Fragen dazu beantworten kann
- **Kundensupport:** Ein System, das auf Produktdokumentation zugreift und Kundenfragen präzise beantwortet – ohne das Modell auf Unternehmensdaten trainieren zu müssen
- **Aktuelle Informationen:** Inhalte, die regelmäßig aktualisiert werden, können in die Wissensdatenbank eingespielt werden, ohne das Modell neu zu trainieren

Der entscheidende Vorteil: Das Modell selbst muss nicht verändert werden. Neue Inhalte kommen in die Datenbank – und das System weiß sie ab sofort.

---

## Was RAG nicht löst

RAG verbessert, was ein Modell weiß. Es verbessert nicht, wie das Modell denkt.

Wenn die Wissensdatenbank falsche oder widersprüchliche Inhalte enthält, bekommt das Modell falsche oder widersprüchliche Grundlagen. Garbage in, garbage out: Das gilt auch hier.

Außerdem: RAG findet, was ähnlich klingt – nicht unbedingt, was gemeint ist. Die Suche basiert auf sprachlicher Ähnlichkeit. Ein Dokument, das die Antwort enthält, aber ganz anders formuliert ist als die Frage, wird möglicherweise nicht gefunden. Wie gut das System sucht, hängt stark von der Qualität der Implementierung ab.

[Halluzinationen](../glossar#halluzination) werden durch RAG reduziert, aber nicht ausgeschlossen. Das Modell kann immer noch auf Basis der gefundenen Abschnitte etwas Falsches schlussfolgern – oder Informationen hinzufügen, die nicht in den Abschnitten standen.

---

## Für wen das heute relevant ist

RAG ist für alle interessant, die KI auf eigene Dokumente, Wissensdatenbanken oder interne Informationen anwenden wollen – ohne ein Modell neu zu trainieren.

Die Umsetzung erfordert technischen Aufwand: Dokumente müssen vorbereitet, indiziert und abrufbar gemacht werden. Es gibt Plattformen und Dienste, die diesen Aufwand vereinfachen, aber es ist kein Ein-Klick-Prozess.

Das Grundprinzip zu verstehen ist trotzdem nützlich – besonders um einschätzen zu können, was ein RAG-System leisten kann und was nicht. Ein System, das „auf Basis Ihrer Dokumente antwortet", ist nicht unfehlbar. Es ist eine Suchmaschine mit angeschlossenem Sprachmodell.

Wie KI selbstständig mit solchen Systemen arbeitet: [KI-Agents](agents). Wie die Verbindung zu externen Werkzeugen technisch funktioniert: [MCP](mcp).
