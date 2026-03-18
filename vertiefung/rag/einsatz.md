---
title: "RAG: Einsatz & Grenzen"
description: Wo RAG seinen Nutzen entfaltet, wo es an Grenzen stößt und welche Fehler typisch sind.
layout: default
parent: RAG – Retrieval-Augmented Generation
grand_parent: Vertiefung
nav_order: 2
---

# Einsatz & Grenzen

## Wofür RAG nützlich ist

RAG macht KI dort nützlich, wo spezifisches, aktuelles oder internes Wissen gefragt ist:

**Unternehmensinterne Wissensdatenbanken:** Ein System, das Handbücher, Richtlinien und Prozessdokumentationen kennt und konkrete Fragen dazu beantworten kann. Wer etwas zum Genehmigungsprozess wissen will, bekommt die Antwort aus dem tatsächlichen HR-Handbuch – nicht aus dem allgemeinen Modellwissen.

**Kundensupport:** Ein System, das auf Produktdokumentation zugreift und Kundenfragen präzise beantwortet – ohne das Modell auf Unternehmensdaten trainieren zu müssen. Die Produktdokumentation ändert sich; das Modell bleibt dasselbe.

**Rechtliche und regulatorische Texte:** Wenn die Frage in einem spezifischen Regelwerk beantwortet werden muss, kann RAG sicherstellen, dass das Modell aus dem richtigen Dokument antwortet – nicht aus seiner allgemeinen Trainingsgrundlage.

**Aktuelle Informationen:** Inhalte, die regelmäßig aktualisiert werden, können in die Wissensdatenbank eingespielt werden, ohne das Modell neu zu trainieren.

---

## Was RAG nicht löst

RAG verbessert, was ein Modell weiß. Es verbessert nicht, wie das Modell denkt.

**Schlechte Quelldokumente liefern schlechte Antworten.** Wenn die Wissensdatenbank veraltete, widersprüchliche oder fehlerhafte Inhalte enthält, bekommt das Modell fehlerhafte Grundlagen. Eine RAG-Antwort ist nur so gut wie die Dokumente dahinter.

**Suche findet nicht immer den richtigen Abschnitt.** Die Ähnlichkeitssuche funktioniert gut, wenn Frage und relevanter Text ähnlich formuliert sind. Wenn das Dokument eine Frage auf eine Art beantwortet, die sprachlich weit von der Frage entfernt ist, findet das System den Abschnitt möglicherweise nicht.

**[Halluzinationen](../../glossar#halluzination) verschwinden nicht.** Das Modell kann immer noch auf Basis der gefundenen Abschnitte etwas Falsches schlussfolgern – oder Informationen hinzufügen, die nicht in den Abschnitten standen. RAG reduziert Halluzinationen, schließt sie nicht aus.

**Zusammengehöriges kann auseinandergerissen werden.** Wenn ein Dokument so aufgeteilt wird, dass zusammengehörende Informationen in verschiedene Chunks landen, fehlt dem Modell der Zusammenhang. Ein Vertrag, bei dem Bedingung und Ausnahme in verschiedenen Chunks stehen, kann falsch interpretiert werden.
