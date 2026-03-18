---
title: RAG – Retrieval-Augmented Generation
description: Wie KI auf eigene Wissensbestände zugreift, ohne alles in den Kontext laden zu müssen – und wo die Grenzen liegen.
layout: default
parent: Vertiefung
nav_order: 2
---

# RAG – Retrieval-Augmented Generation

KI-Modelle wissen viel – aber nicht alles. Sie kennen nicht das, was nach ihrem Trainingsdatum passiert ist. Sie kennen nicht die internen Dokumente eines Unternehmens. Sie kennen nicht die spezifischen Regelungen einer bestimmten Organisation.

Die naheliegende Lösung: alles in den [Kontext](../glossar#kontext) laden. Das funktioniert bis zu einem gewissen Umfang. Aber [Kontextfenster](../glossar#kontextfenster) haben Grenzen, und hunderte Dokumente hineinzuladen ist langsam, teuer und unübersichtlich.

RAG löst dieses Problem: Anstatt alle Dokumente zu laden, sucht das System gezielt nach den relevanten Stellen – und gibt nur diese an das Modell weiter.

---

## Was RAG ist

[RAG](../glossar#rag) steht für Retrieval-Augmented Generation – auf Deutsch: abrufverstärkte Generierung. Der Begriff beschreibt ein Verfahren, bei dem ein KI-System vor dem Generieren einer Antwort zunächst in einer Wissensdatenbank sucht und die gefundenen Inhalte in den Kontext einbindet.

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

Um zu verstehen, was RAG leisten kann und was nicht, hilft ein Blick auf den technischen Aufbau – ohne in die Tiefe zu gehen.

**Dokumente werden vorbereitet.** Bevor das System suchen kann, müssen die Dokumente aufbereitet werden. Sie werden in kleine Abschnitte aufgeteilt – sogenannte Chunks. Ein Chunk ist typischerweise ein Absatz oder ein thematischer Block, nicht das ganze Dokument.

**Jeder Chunk bekommt eine numerische Darstellung.** Ein Sprachmodell wandelt jeden Chunk in einen Zahlenvektor um – eine sogenannte Embedding. Dieser Vektor beschreibt den semantischen Inhalt des Textes: was er bedeutet, nicht nur welche Wörter er enthält. Ähnliche Inhalte liegen im Vektorraum nah beieinander.

**Suche funktioniert über Ähnlichkeit.** Wenn eine Frage gestellt wird, bekommt auch die Frage ein Embedding. Das System sucht dann nach den Chunks, deren Vektoren der Frage am ähnlichsten sind. Das ist keine Stichwortsuche – es ist eine Bedeutungssuche. „Wie hoch ist die Karenzzeit?" findet auch Abschnitte, in denen das Wort „Karenzzeit" nicht vorkommt, der Begriff aber umschrieben wird.

**Die Treffer landen im Kontext.** Die ähnlichsten Chunks werden zusammen mit der Frage an das Modell übergeben. Das Modell antwortet auf Basis dieser Abschnitte.

---

## Wofür RAG nützlich ist

RAG macht KI dort nützlich, wo spezifisches, aktuelles oder internes Wissen gefragt ist:

**Unternehmensinterne Wissensdatenbanken:** Ein System, das Handbücher, Richtlinien und Prozessdokumentationen kennt und konkrete Fragen dazu beantworten kann. Wer im Urlaubsantrag etwas zum Genehmigungsprozess wissen will, bekommt die Antwort aus dem tatsächlichen HR-Handbuch – nicht aus dem allgemeinen Modellwissen.

**Kundensupport:** Ein System, das auf Produktdokumentation zugreift und Kundenfragen präzise beantwortet – ohne das Modell auf Unternehmensdaten trainieren zu müssen. Die Produktdokumentation ändert sich; das Modell bleibt dasselbe.

**Rechtliche und regulatorische Texte:** Wenn die Frage in einem spezifischen Regelwerk beantwortet werden muss, kann RAG sicherstellen, dass das Modell aus dem richtigen Dokument antwortet – nicht aus seiner allgemeinen Trainingsgrundlage.

**Aktuelle Informationen:** Inhalte, die regelmäßig aktualisiert werden, können in die Wissensdatenbank eingespielt werden, ohne das Modell neu zu trainieren.

---

## Was RAG nicht löst

RAG verbessert, was ein Modell weiß. Es verbessert nicht, wie das Modell denkt.

**Schlechte Quelldokumente liefern schlechte Antworten.** Wenn die Wissensdatenbank veraltete, widersprüchliche oder fehlerhafte Inhalte enthält, bekommt das Modell fehlerhafte Grundlagen. Eine RAG-Antwort ist nur so gut wie die Dokumente dahinter.

**Suche findet nicht immer den richtigen Abschnitt.** Die Ähnlichkeitssuche funktioniert gut, wenn Frage und relevanter Text ähnlich formuliert sind. Wenn das Dokument eine Frage auf eine Art beantwortet, die sprachlich weit von der Frage entfernt ist, findet das System den Abschnitt möglicherweise nicht. Die Antwort basiert dann auf weniger relevanten Treffern – oder fehlt ganz.

**[Halluzinationen](../glossar#halluzination) verschwinden nicht.** Das Modell kann immer noch auf Basis der gefundenen Abschnitte etwas Falsches schlussfolgern – oder Informationen hinzufügen, die nicht in den Abschnitten standen. RAG reduziert Halluzinationen, schließt sie nicht aus.

**Chunking-Fehler verursachen Informationsverlust.** Wenn ein Dokument so aufgeteilt wird, dass zusammengehörende Informationen in verschiedene Chunks landen, fehlt dem Modell der Zusammenhang. Ein Vertrag, bei dem Bedingung und Ausnahme in verschiedenen Chunks stehen, kann falsch interpretiert werden.

---

## Wann RAG – und wann nicht

RAG ist nicht immer die richtige Lösung. Zwei Alternativen sind relevant:

**Langes Kontextfenster:** Wenn die gesamte relevante Information in einen einzigen Kontext passt und die Dokumente klein genug sind, kann man einfach alles einfügen. Für ein einzelnes Handbuch von 50 Seiten braucht es kein RAG – das Dokument passt direkt in den Kontext. RAG lohnt sich erst, wenn die Datenmenge das Kontextfenster sprengt oder die Auswahl relevanter Abschnitte selbst eine Aufgabe ist.

**Fine-tuning:** Wenn das Modell dauerhaft ein bestimmtes Verhalten oder Stil-Kenntnisse entwickeln soll – nicht Faktenwissen –, ist Fine-tuning der richtige Weg. RAG liefert Wissen zur Laufzeit; Fine-tuning verändert das Modell selbst. Für die meisten Wissensanwendungen ist RAG die bessere Wahl, weil es ohne Modell-Training auskommt.

---

## Für wen das heute relevant ist

RAG ist für alle interessant, die KI auf eigene Dokumente, Wissensdatenbanken oder interne Informationen anwenden wollen – ohne ein Modell neu zu trainieren.

Die Umsetzung erfordert technischen Aufwand: Dokumente müssen vorbereitet, indiziert und abrufbar gemacht werden. Es gibt Plattformen und Dienste, die diesen Aufwand vereinfachen. Für einfachere Fälle bieten manche KI-Produkte RAG-ähnliche Funktionen direkt an – man lädt Dokumente hoch, und das System durchsucht sie bei Bedarf.

Das Grundprinzip zu verstehen ist trotzdem nützlich – besonders um einzuschätzen, was ein RAG-System leisten kann und was nicht. Ein System, das „auf Basis Ihrer Dokumente antwortet", ist nicht unfehlbar. Es ist eine Bedeutungssuche mit angeschlossenem Sprachmodell. Die Qualität des Ergebnisses hängt von der Qualität der Dokumente und der Qualität der Suche ab.

Wie KI selbstständig mit solchen Systemen arbeitet: [KI-Agents](agents). Wie die Verbindung zu externen Werkzeugen technisch funktioniert: [MCP](mcp).
