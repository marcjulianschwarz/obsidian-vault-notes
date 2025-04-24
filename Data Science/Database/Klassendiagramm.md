---
uni-module: "KonzMod"
---

# Klassendiagramm

## Basisnotation für Klassen

### Namensfeld

Das Namensfeld beinhaltet den Klassennamen, <<Schlüsselwörter>> und eine Eigenschaftsangabe wie {abstract}.

### Attributliste

Hier werden Attribute aufgeschrieben, die die Klasse beschreiben. Dabei wird jeweils vor dem Namen angegeben, wie sichtbar die Attribute sein sollen. Nach einem Doppelpunkt wird dann noch beschrieben welchen Typ das Attribut hat und optional noch ein Default Wert übergeben.
Außerdem können beispielsweise bei mehrwertigen Attributen noch andere Eigenschaften beschrieben werden:
![[Bildschirmfoto 2021-07-20 um 17.40.16.png]]

### Operationsliste

Hier werden Operationen (Methoden) aufgelistet, die auch Parameter haben können. Diese können vorbelegt sein und es kann angegeben werden ob sie in out oder inout sind.

## Aktive Klasse

Kann mit {active} erstellt werden. Das Verhalten dieser Klasse wird durch andere Diagramme (z.B.: [[Zustandsdiagramm]] oder [[Aktivitätsdiagramm]]) modelliert.

## Objekte einer Klasse

sind Instanzen einer Klasse und können mit einem : und einem Namen vor dem Klassennamen benannt werden. Die Objekte können auch mit Links in Beziehungen stehen.

## Assoziationen zwischen Klassen

sind Beziehungen zwischen Klassen. Sie können mit einem Pfeil dargestellt werden. Dieser kann benannt werden, wobei meistens zusätlich die Leserichtung angegeben ist.
Bei ==navigierbaren== Assoziationen kann man noch angeben wie man von Klasse zu Klasse kommt (bzw in welche Richtungen man nicht navigieren kann).

### Multiplizität

Gibt die Anzahl der Links an, die ein Objekt mit dem Objekt einer anderen Klasse eingehen kann.
Notation:

- 0..\* -> beliebig viele
- 1..1 -> genau eins
- 1..\* -> mindestens eins

### Assoziationsklassen

beinhalten Attribute um eine Assoziation noch näher zu beschreiben. Meistens kann diese aber in eine normale Klasse aufgelöst werden.

## Aggregation

Beschreibt eine ==Teil-Ganze== Beziehung (leere Raute statt Pfeil). Dabei kann das Teil auch alleine existieren.

## Komposition

Beschreibt eine stenge ==Teil-Ganze== Beziehung (volle Raute). Hier darf das Teil nur Teil **eines** Ganzen seins.
Aber auch hier kann das Teil alleine existieren.

## Generalisierung

Man kann {Eigenschaften} angeben. Es gibt Mehrfachvererbung. Attribute und Operationen können in den Unterklassen neu definiert werden.

## Metamodellierung

[[Modell]] über ein Modell um dieses zu beschreiben.
[[Unified Modelling Language]] ist eine komplexe Sprache, dessen Architektur durch Metamodellierung verständlicher gemacht werden kann. Dadurch ist die Sprache auch konsistent erweiterbar.

### Ebenen der Metamodellierung

![[Bildschirmfoto 2021-07-20 um 17.55.52.png]]
