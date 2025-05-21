---
uni-module: "KonzMod"
---

# Multidimensionale Datenmodellierung

In betrieblichen Informationsprozessen muss man zwischen [[OLTP]] und [[OLAP]] unterscheiden.

Mit unserem bisherigen [[Relationenmodell]] konnte man mit wenigen, einfachen Modellierungskonstrukten anwendungsneutrale Modelle bauen. Diese sind in vielen Bereichen nützliche aber für z.B. Datenanalyse kompliziert in der Anwendung.

Mit einem Multidimensionalem Datenmodell können mit komplexen Modellierungskonstrukte Modelle erstellt werden, die speziell auf Datenanalyse zugeschnitten sind.

Eine wichtige Rolle spielt dabei das [[Data Warehouse]] welches uns erlaubt bereits voraggregierte große Datenmengen zu analysieren.

Es werden Daten in das Data Warehouse geladen. Dabei werden die Daten bereits gesäubert und voraggregiert. Dann liegen die Daten in [[Data Mart|Data Marts]] vor, die durch eine Anfrage an das System abgefragt werden können.

## Wichtige Begriffe MD

- Klassifikationshierarchien
- Spärlich gefüllte Datenräume werden durch viele Null-Werte repräsentiert.
- Stabile Daten werden nie geändert (nur hinzugefügt).
- Materialisierte Sichten = Voraggregierte Daten
- Mikro-Daten = Datenpunkt
- Makro-Daten = Aggregierte Daten
- Meta-Daten = Beschreiben Mikro und Makro Daten sowie deren Entstehung

Ein MDM kann man sich als einer Art [[Hypercube]] vorstellen. Dieser kann auch mit einer speziellen Version des ER Modell als [[mER Diagramm]] modelliert werden.

→ [[Logisches Schema einer Dimension]]
→ [[Aggregationstypen auf MDMs]]
→ [[Multidimensionale Operatoren]]

Die [[Vier Schritte nach Kimball]] erlauben es einem einen Geschäftsprozess multidimensional zu modellieren.

[[ROLAP]]
