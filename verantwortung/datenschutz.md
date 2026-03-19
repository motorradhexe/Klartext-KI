---
title: Datenschutz beim KI-Einsatz
description: Was mit Eingaben passiert, wenn man sie an einen KI-Dienst schickt – und welche Konsequenzen das für den Arbeitsalltag hat.
layout: default
parent: Verantwortung
nav_order: 2
---

# Datenschutz beim KI-Einsatz

Wer einen Prompt an einen KI-Dienst schickt, sendet Daten an einen externen Server. Das klingt banal, hat aber Konsequenzen, die viele nicht bewusst reflektieren – besonders dann, wenn es schnell gehen muss und Du einfach einen Text hineinkopierst.

---

## Was passiert mit dem, was Du eingibst?

Bei den großen Anbietern – OpenAI, Google, Anthropic – gelten je nach Produkt und Vertrag unterschiedliche Regeln. Der entscheidende Unterschied liegt zwischen kostenlosen und bezahlten bzw. Enterprise-Accounts.

Bei kostenlosen oder persönlichen Accounts werden Eingaben teils für das [Training](../glossar#training) neuer Modelle verwendet. Das lässt sich in den Einstellungen oft deaktivieren – aber es ist nicht immer die Standardeinstellung. Wer das nicht aktiv überprüft hat, sollte nicht davon ausgehen, dass die eigenen Eingaben nicht verwendet werden.

Bei Business- oder Enterprise-Accounts schließen die Anbieter das Training auf Basis von Kundendaten vertraglich aus. Die Daten werden für den Dienst verarbeitet und vorübergehend gespeichert – typischerweise 30 Tage –, aber nicht für das Training des Basismodells genutzt. Das ist ein realer Unterschied, kein Marketingversprechen.

Das Problem entsteht selten durch bösen Willen des Anbieters. Es entsteht dadurch, dass Du in der Praxis vergisst, was Du eingibst – und dass der Text Deinen Rechner verlässt, sobald Du auf Senden drückst.

---

## Welche Daten sind unkritisch, welche nicht?

Eine einfache Einstufung für den Alltag:

**Unkritisch:** Eigene Textentwürfe, allgemeine Fachfragen, Sprachverbesserungen, Beispielszenarien ohne echte Personendaten oder Betriebsgeheimnisse.

**Vorsicht:** Interne Dokumentation, Projektzusammenfassungen, Code mit betriebsspezifischer Logik, Inhalte aus Meetings oder E-Mails. Nicht verboten, aber: Kennt die eigene Organisation die Nutzung? Ist das durch die Unternehmensrichtlinien abgedeckt?

**Stop ohne weitere Klärung:** Kundendaten, Patientendaten, Personaldaten, Passwörter, API-Keys, Vertragsinhalte mit Vertraulichkeitsklauseln, Informationen aus internen Systemen mit eingeschränktem Zugriff.

Die Faustregel: Alles, was Du nicht an eine fremde, grundsätzlich vertrauenswürdige Person weitergeben würdest, solltest Du auch nicht in einen KI-Dienst eingeben.

---

## Credentials und Secrets im Code

Wer KI beim Programmieren einsetzt, kopiert oft Code direkt als Prompt. Das ist sinnvoll – aber riskant, wenn der Code Zugangsdaten enthält. Typische Beispiele sind API-Keys in Konfigurationsdateien, Datenbankverbindungsstrings mit Benutzername und Passwort, interne Endpunkt-URLs, die Rückschlüsse auf die Systemarchitektur erlauben, und Umgebungsvariablen, die in `.env`-Dateien oder direkt im Code stehen.

Wer solchen Code eingibt, überträgt diese Informationen an den Anbieter. Selbst wenn der Anbieter sie nicht missbräuchlich nutzt: Sie sind übertragen worden, sie liegen auf externen Servern, sie können geloggt sein.

Die Lösung ist einfach: Vor dem Einkopieren von Code die relevanten Stellen durch Platzhalter ersetzen.

```
# Nicht so:
db_password = "mein_echtes_passwort_123"

# So:
db_password = "HIER_PLATZHALTER"
```

Das Modell versteht die Struktur und kann trotzdem helfen. Den echten Wert muss es nicht kennen.

---

## DSGVO: Die Grundregel für personenbezogene Daten

Die Datenschutz-Grundverordnung (DSGVO) gilt für personenbezogene Daten – also Informationen, die sich auf eine identifizierbare natürliche Person beziehen. Das sind nicht nur Namen und Adressen, sondern auch E-Mail-Adressen, Krankengeschichten, Gehaltsangaben, und in vielen Fällen auch berufliche Informationen, die eine Person erkennbar machen.

Wer personenbezogene Daten an einen externen KI-Dienst übermittelt, gibt sie an einen Dritten weiter. Das ist nach DSGVO grundsätzlich eine Datenübermittlung, die entweder einer Rechtsgrundlage bedarf oder durch einen Auftragsverarbeitungsvertrag abgedeckt sein muss.

Was das im Alltag bedeutet: Kundendaten in einen Prompt kopieren, ohne dass die eigene Organisation einen Auftragsverarbeitungsvertrag mit dem KI-Anbieter abgeschlossen hat, ist datenschutzrechtlich problematisch – unabhängig davon, wie vertrauenswürdig der Anbieter ist.

Konkret: Vor dem Einsatz von KI-Diensten mit personenbezogenen Daten klären, ob der Anbieter als Auftragsverarbeiter eingesetzt wird und ob dafür ein entsprechender Vertrag vorliegt. Bei Unsicherheit: keine Personendaten eingeben, bis das geklärt ist.

---

## Unternehmensrichtlinien: Was die eigene Organisation erlaubt

Viele Organisationen haben Sicherheits- oder Datenschutzrichtlinien, die den Einsatz von KI-Tools regulieren oder einschränken – oft ohne dass die Mitarbeitenden davon wissen oder sich darum kümmern.

Das betrifft vor allem Code und interne Dokumentation, die proprietäres Know-how enthält, Kundendaten, für die DSGVO oder vertragliche Vereinbarungen gelten, sowie Verhandlungs- oder Strategiepapiere, deren Inhalte vertraulich sind.

Das Problem ist nicht, dass KI die Daten stiehlt. Das Problem ist, dass das Einkopieren solcher Inhalte in einen externen Dienst eine Datenweitergabe an Dritte darstellt – egal wie vertrauenswürdig der Anbieter ist. Wer das ohne Klärung tut, kann gegen interne Richtlinien oder Gesetze verstoßen.

**Vor dem produktiven Einsatz:** Klären, was die eigene Organisation erlaubt. Wenn das unklar ist, fragen – nicht annehmen.

---

## Der Irrtum: „Gleicher Anbieter, kein Risiko"

In Unternehmensumgebungen gibt es ein verbreitetes Muster: Viele Organisationen nutzen Dienste eines einzigen großen Anbieters – beispielsweise die gesamte IT-Infrastruktur über Microsoft Azure. Wenn dann ein KI-Tool desselben Anbieters eingeführt wird, entsteht das Gefühl: „Das läuft alles bei uns, also ist es sicher."

Dieses Gefühl ist nicht vollständig falsch – aber es ist unvollständig.

Am Beispiel Azure OpenAI: Microsoft garantiert für Enterprise-Verträge, dass Kundendaten nicht für das Training der Basismodelle verwendet werden. Die Daten verlassen den Azure-Tenant des Kunden nicht. Das ist ein realer und relevanter Unterschied zu kostenlosen Diensten.

Was das aber nicht bedeutet: Credentials im Code sind trotzdem riskant – sie werden übertragen und gespeichert, auch wenn der Anbieter vertrauenswürdig ist. Unternehmensrichtlinien gelten weiterhin. Azure OpenAI ist kein internes System – es ist ein Cloud-Dienst, und viele Policies unterscheiden nicht nach Anbieter, sondern nach „intern vs. extern". Compliance und Regulierung fragen nicht nach dem Vendor, sondern nach dem Ort der Verarbeitung und dem Typ der Daten.

Der eigentliche Irrtum ist nicht „Azure ist unsicher". Der Irrtum ist: **„Weil ich dem Anbieter vertraue, muss ich nicht mehr nachdenken, was ich schicke."** Vertrauen in einen Anbieter ersetzt keine Risikoanalyse der eigenen Eingaben.
