---
uni-module: "KonzMod"
---

# ER Mapping

Ist der Prozess ein [[ER-Modell]] in Tabellen (Relationen) umwandeln.

## 1. Reguläre Entity Typen

Für jeden ET eine Relation mit allen einfachen Attributen. Aus den Schlüsselkandidaten wird ein Primärschlüssel ausgewählt. Die anderen Kandidaten müssen unique und not Null sein.

## 2. Schwache Entity Typen

Wird auch als eigene Relation realisiert. Sie enthält alle Attribute und zusätzlich als Fremdschlüssel die Primärschlüssel der Owner-Typen. Der Primärschlüssel ist die Kombination aller Fremdschlüssel zusammen mit dem partiellen Schlüssel.
Die [[Referenzielle Integrität]] muss jeweils auf CASCADE gestellt werden (Bei den Owner-Typen).

## 3. Beziehungen

### M:N Beziehungen

Für eine M:N Beziehung wird eine neue Relation erstellt. Darin befinden sich alle Attribute der Beziehung und die Primärschlüssel der beteiligten ET als Fremdschlüssel.
Der Primärschlüssel dieser Relation besteht dann aus der Kombination aller Fremdschlüssel.
Auch 1:N und 1:1 Beziehungen können so dargestellt werden.

### N:1 Beziehungen

Zuerst sucht man sich die Relation aus, die auf der N-Seite der Beziehung steht. Dieser Relation wird dann der Primärschlüssel der 1 Seite als Fremdschlüssel hinzugefügt. Auch alle Attribute der Beziehungen kommen mit in die Relation auf der N-Seite.
Bei einer totalen Beziehung muss der Fremdschlüssel natürlich noch als NOT NULL deklariert werden.

### 1:1 Beziehungen

Bei einer 1:1 Beziehung wählt man einen der beiden ET aus, die an der Beziehung teilnehmen (am besten denjenigen, der total an der Beziehung teilnimmt). Dann nimmt man wieder den Primärschlüssel als Fremdschlüssel auf und deklariert ihn als UNIQUE, da ja eine Beziehung nicht doppelt vorkommen darf.
Genauso wie zuvor werden die Attribute der Beziehung einfach mit aufgenommen.
Wenn auf beiden Seiten eine totale Partizipation existiert, können beide Relationen theoretisch auch zu einer einzigen verschmelzen.

## 4. Mehrwertige Attribute

Für jedes mehrwertige Attribut wird eine eigene Relation erstellt. Diese enthält einen Fremdschlüssel, der den Primärschlüssel des ET referenziert, der das mehrwertige Attribut erhalten soll.
Dann gibt es als zweites Attribut eben genau das mehrwertige Attribut des ET.
Der Primärschlüssel ist die Kombination aus Fremdschlüssel und Attribut.
Natürlich muss hier auch zur Erhaltung der [[Referenzielle Integrität]]die Option CASCADE verwendet werden.

## 5. Mehrstellige Beziehungen

Für mehrstellige Beziehungen wird eine Relation erstellt, die die Primärschlüssel aller beteiligten ET als Fremdschlüssel enthält. Der Primärschlüssel entspricht dann der Kombination aller Fremdschlüssel.
Allerdings müssen hier auch [[Funktionale Abhängigkeit]] beachtet werden.
Wenn genau eine Kardinalität = 1 ist, dann nimmt dieser Fremdschlüssel nicht mehr am Primärschlüssel teil und wird lediglich auf NOT NULL gesetzt.
Um [[Funktionale Abhängigkeit]]verlustfrei darzustellen, muss man sich bei mehreren 1er Kardinalitäten für eine Primärschlüssel entscheiden und dann die anderen Attribute so restriktieren, dass die Abhängigkeiten erhalten bleiben.

## Übersicht

![[IMG - ER vs Relationenmodell.png]]

## 6. Abbildung Generalisierung / Spezialisierung

Im Allgemeinen gibt es hier 4 verschiedene Möglichkeiten. Allerdings ist die erste (8A) immer möglich und ist somit die einfachste.
![[Bildschirmfoto 2021-07-20 um 14.51.54.png]]

## 7. Kategorien

Für jede Kategorie wird eine eigene Relation erstellt, die einfach nur ein Surrogat als Primärschlüssel besitzt.
Dieses kann dann in den Relationen als Fremdschlüssel eingesetzt werden, die Teil dieser Kategorie sind.
