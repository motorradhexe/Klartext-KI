---
title: Risiken beim Einsatz von KI
description: Welche Risiken beim Einsatz von KI-Tools entstehen – und wie man damit verantwortungsvoll umgeht.
layout: default
parent: Verantwortung
nav_order: 1
---

# Risiken beim Einsatz von KI

KI-Tools können nützlich sein. Sie können auch Probleme verursachen – rechtliche, sicherheitsrelevante, organisatorische. Die meisten dieser Probleme entstehen nicht, weil KI gefährlich ist, sondern weil man beim Einsatz nicht nachdenkt, was man eigentlich eingibt und wohin das geht.

Dieses Modul beschreibt die wichtigsten Risikofelder: nicht um von KI abzuschrecken, sondern um den Einsatz informierter zu machen.

---

## Datenweitergabe: Was passiert mit dem, was man eingibt?

Wer einen Prompt an einen KI-Dienst schickt, sendet Daten an einen externen Server. Das klingt banal, hat aber Konsequenzen, die viele nicht bewusst reflektieren.

Bei den großen Anbietern – OpenAI, Google, Anthropic – gelten je nach Produkt und Vertrag unterschiedliche Regeln:

- Bei kostenlosen oder persönlichen Accounts werden Eingaben teils für das [Training](../glossar#training) neuer Modelle verwendet. Das lässt sich in den Einstellungen oft deaktivieren, ist aber nicht immer der Standard.
- Bei Business- oder Enterprise-Accounts ist das Training auf Basis von Kundendaten vertraglich ausgeschlossen – aber die Daten werden für den Dienst verarbeitet und vorübergehend gespeichert.
- Viele Anbieter speichern Eingaben für einen begrenzten Zeitraum (typisch: 30 Tage), um Missbrauch zu erkennen und den Dienst zu betreiben.

Das Problem entsteht selten durch bösen Willen des Anbieters. Es entsteht dadurch, dass man vergisst, was man eingibt – und dass der Text den eigenen Rechner verlässt.

**Praktische Konsequenz:** Keine Kundendaten, keine Passwörter, keine sensiblen Personendaten, keine internen Systeminformationen einfach hineinkopieren – egal wie bequem es wäre.

---

## Credentials und Secrets im Code

Wer KI beim Programmieren einsetzt, kopiert oft Code direkt als Prompt. Das ist sinnvoll – aber riskant, wenn der Code Zugangsdaten enthält.

Typische Beispiele:

- API-Keys in Konfigurationsdateien oder direkt im Code
- Datenbankverbindungsstrings mit Benutzername und Passwort
- Interne Endpunkt-URLs, die Rückschlüsse auf die Systemarchitektur erlauben
- Umgebungsvariablen, die in `.env`-Dateien oder direkt im Code stehen

Wer solchen Code eingibt, überträgt diese Informationen an den Anbieter. Selbst wenn der Anbieter sie nicht missbräuchlich nutzt: sie sind übertragen worden, sie liegen auf externen Servern, sie können geloggt sein.

Die Lösung ist einfach: Vor dem Einkopieren von Code die relevanten Stellen durch Platzhalter ersetzen.

```
# Nicht so:
db_password = "mein_echtes_passwort_123"

# So:
db_password = "HIER_PLATZHALTER"
```

Das Modell versteht die Struktur und kann trotzdem helfen. Den Wert muss es nicht kennen.

---

## Unternehmensrichtlinien

Viele Organisationen haben Sicherheits- oder Datenschutzrichtlinien, die den Einsatz von KI-Tools regulieren oder verbieten – oft ohne dass die Mitarbeitenden davon wissen oder sich darum kümmern.

Das betrifft vor allem:

- **Code und interne Dokumentation**, die proprietäres Know-how enthält
- **Kundendaten**, für die Datenschutzgesetze (DSGVO) oder vertragliche Vereinbarungen gelten
- **Verhandlungs- oder Strategiepapiere**, deren Inhalte vertraulich sind

Das Problem ist nicht, dass KI die Daten stiehlt. Das Problem ist, dass das Einkopieren solcher Inhalte in einen externen Dienst eine Datenweitergabe an Dritte darstellt – egal wie vertrauenswürdig der Anbieter ist. Wer das ohne Genehmigung tut, verstößt möglicherweise gegen interne Richtlinien oder Gesetze.

**Vor dem produktiven Einsatz:** Klären, was die eigene Organisation erlaubt – und wenn unklar, fragen.

---

## Rechtliche Risiken: Urheberrecht und Compliance

KI-generierte Inhalte haben keine klare rechtliche Stellung. Das ist kein theoretisches Problem, sondern eines, das in der Praxis auftaucht.

**Urheberrecht der Ausgabe:** Wer KI-generierten Text veröffentlicht, sollte wissen, dass in den meisten Ländern kein automatischer Urheberrechtsschutz für KI-Ausgaben entsteht. Die Nutzung ist in vielen Fällen problemlos – aber nicht überall, und nicht für alle Zwecke.

**Trainingsdaten und Ähnlichkeit:** KI-Modelle wurden auf großen Textmengen trainiert, die urheberrechtlich geschütztes Material enthalten können. Ob generierte Texte rechtlich problematisch sind, ist noch nicht abschließend geklärt. Bei sensiblen Anwendungen – Werbetexte, Veröffentlichungen, Produktbeschreibungen – lohnt es sich, die eigene Rechtsabteilung zu fragen.

**Branchenregulierung:** In Bereichen wie Finanzdienstleistungen, Gesundheitswesen oder Verteidigung gelten regulatorische Anforderungen, die die Verwendung von Cloud-KI-Diensten einschränken können – unabhängig davon, wie vertrauenswürdig der Anbieter ist.

---

## Verlässlichkeit: Wenn KI sicher klingt und trotzdem falsch liegt

[Halluzinationen](../glossar#halluzination) sind kein Randproblem. KI-Modelle produzieren regelmäßig falsche Aussagen – formuliert mit derselben Sicherheit wie richtige.

Das wird zum Risiko, wenn man KI-Ausgaben weitergibt, ohne sie zu prüfen:

- Ein Rechtsbegriff, der leicht falsch erklärt wird, aber überzeugend klingt
- Eine Zahl in einer Analyse, die nicht stimmt, aber plausibel aussieht
- Eine technische Anweisung, die unter bestimmten Bedingungen nicht funktioniert

Die Verantwortung für die Richtigkeit liegt immer beim Menschen, nicht beim Modell. KI ist ein Werkzeug zum Entwurf, nicht zum Abschluss. Kritische Ausgaben – Verträge, Diagnosen, Berechnungen, Rechtsauskünfte – müssen von Menschen überprüft werden.

---

## Ein häufiger Irrtum: „Der gleiche Anbieter = kein Risiko"

In Unternehmensumgebungen gibt es ein verbreitetes Muster: Viele Organisationen nutzen Dienste eines einzigen großen Anbieters – beispielsweise die gesamte IT-Infrastruktur über Microsoft Azure. Wenn dann ein KI-Tool desselben Anbieters eingeführt wird, entsteht das Gefühl: „Das läuft alles bei uns, also ist es sicher."

Dieses Gefühl ist nicht vollständig falsch – aber es ist unvollständig.

Am Beispiel Azure OpenAI: Microsoft garantiert für Enterprise-Verträge, dass Kundendaten nicht für das Training der Basismodelle verwendet werden. Die Daten verlassen den Azure-Tenant des Kunden nicht. Das ist ein realer und relevanter Unterschied zu kostenlosen Diensten.

Was das aber nicht bedeutet:

- **Credentials im Code** sind trotzdem riskant – sie werden übertragen und gespeichert, auch wenn der Anbieter vertrauenswürdig ist.
- **Unternehmensrichtlinien** gelten weiterhin. Azure OpenAI ist kein internes System – es ist ein Cloud-Dienst, und viele Policies unterscheiden nicht nach Anbieter, sondern nach „intern vs. extern".
- **Compliance und Regulierung** fragen nicht nach dem Vendor, sondern nach dem Ort der Verarbeitung und dem Typ der Daten.
- **Logging**: Azure OpenAI speichert Prompts standardmäßig für bis zu 30 Tage für Zwecke der Missbrauchserkennung, sofern das nicht explizit deaktiviert wird.
- **IP-Recht**: Proprietärer Code, der an einen externen Dienst gesendet wird, kann Gegenstand von NDAs oder internen Geheimhaltungsvereinbarungen sein – unabhängig davon, wer der Anbieter ist.

Der eigentliche Irrtum ist nicht „Azure ist unsicher". Der Irrtum ist: **„Weil ich dem Anbieter vertraue, muss ich nicht mehr nachdenken, was ich schicke."** Vertrauen in einen Anbieter ersetzt keine Risikoanalyse der eigenen Eingaben.

---

## Was man konkret tun kann

Es braucht kein Sicherheitskonzept, um verantwortungsvoll mit KI-Tools zu arbeiten. Einige einfache Regeln reichen für den Anfang:

Keine Credentials, Passwörter oder API-Keys in Prompts einkopieren. Immer durch Platzhalter ersetzen.

Keine Kundendaten, Patientendaten oder personenbezogenen Informationen eingeben, wenn man nicht sicher ist, dass der Anbieter das erlaubt und der eigene Vertrag das abdeckt.

Bei vertraulichen Inhalten – Strategiepapiere, M&A-Unterlagen, interne Systemdokumentation – zuerst klären, ob die eigene Organisation den Einsatz von externen KI-Diensten erlaubt.

KI-Ausgaben, die in wichtigen Entscheidungen verwendet werden, müssen überprüft werden. Nicht stichprobenartig. Jedes Mal.

Wer diese vier Punkte einhält, schließt die meisten realen Risiken aus – ohne auf den Nutzen von KI verzichten zu müssen.
