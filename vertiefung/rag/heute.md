---
title: "RAG: Heute"
description: Wann RAG die richtige Wahl ist, wann nicht – und wie man heute ohne großen Aufwand einsteigt.
layout: default
parent: RAG – Retrieval-Augmented Generation
grand_parent: Vertiefung
nav_order: 3
---

# RAG heute

## Wann RAG – und wann nicht

RAG ist nicht immer die richtige Lösung. Zwei Alternativen sind relevant:

**Langes [Kontextfenster](../../glossar#kontextfenster):** Wenn die gesamte relevante Information in einen einzigen Kontext passt, kannst Du einfach alles einfügen. Für ein einzelnes Handbuch von 50 Seiten braucht es kein RAG – das Dokument passt direkt in den Kontext moderner Modelle. RAG lohnt sich erst, wenn die Datenmenge das Kontextfenster sprengt oder die Auswahl relevanter Abschnitte selbst eine Aufgabe ist.

**[Training](../../glossar#training) des Modells:** Wenn das Modell dauerhaft ein bestimmtes Verhalten, einen Stil oder domänenspezifisches Wissen entwickeln soll, ist das Nachtrainieren des Modells der richtige Weg. RAG liefert Wissen zur Laufzeit; Training verändert das Modell selbst. Für die meisten Wissensanwendungen ist RAG die bessere Wahl, weil es ohne Modell-Training auskommt und sich schnell aktualisieren lässt.

---

## Für wen das heute relevant ist

RAG ist für alle interessant, die KI auf eigene Dokumente, Wissensdatenbanken oder interne Informationen anwenden wollen – ohne ein Modell neu zu trainieren.

Die Umsetzung erfordert technischen Aufwand: Dokumente müssen vorbereitet, indiziert und abrufbar gemacht werden. Es gibt Plattformen und Dienste, die diesen Aufwand vereinfachen. Für einfachere Fälle bieten manche KI-Produkte RAG-ähnliche Funktionen direkt an – Du lädst Dokumente hoch, und das System durchsucht sie bei Bedarf.

Das Grundprinzip zu verstehen ist trotzdem nützlich – besonders um einzuschätzen, was ein RAG-System leisten kann und was nicht. Ein System, das „auf Basis Ihrer Dokumente antwortet", ist nicht unfehlbar. Es ist eine Bedeutungssuche mit angeschlossenem Sprachmodell. Die Qualität des Ergebnisses hängt von der Qualität der Dokumente und der Qualität der Suche ab.

Wie KI selbstständig mit solchen Systemen arbeitet: [KI-Agents](../agents). Wie die Verbindung zu externen Werkzeugen technisch funktioniert: [MCP](../mcp).
