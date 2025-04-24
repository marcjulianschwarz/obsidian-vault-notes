---
tags:
  - MOC
uni-module: StochMod
---

# MOC - Stochastische Modellbildung

> [!Info]
> Eine _kurze_ Zusammenfassung von allem, was in StochMod besprochen wurde.

In [[Ziele und Annahmen StochMod]] wurde festgelegt, dass der Zufall auch regelmäßig sein kann und man ihn daher gut in einem mathematischen [[Modell]] darstellen kann.

## Mathematische Beschreibung

Der [[Grundraum]] bildet die Menge unserer [[Elementarereignis]], also alle [[Ereignis]], die bei einer einfachen Durchführung des Experiments auftreten können.
Will man allerdings auch komplexere Ereignisse darstellen braucht man einen [[Ereignisraum]]. Meistens definiert man sich einen solchen Raum durch eine [[Sigma Algebra]], welche in diskreten Wahrscheinlichkeitsräumen meistens die [[Potenzmenge]] des Grundraums und in reelen Wahrscheinlichkeitsräumen meistens die Menge aller Intervalle ist. Sie besitzt auch viele hilfreiche Eigenschaften wie die [[Sigma-Additivität]].

Der Grundraum, die Sigma-Algebra und das [[Wahrscheinlichkeitsmaß]] bilden zusammen einen [[Wahrscheinlichkeitsraum]] mit dem man ab sofort Wahrscheinlichkeiten von verschiedenen Ereignissen auf diesem Raum berechnen kann.

Ein Beispiel dafür ist der [[Bernoulli-Raum]] mit der [[Bernoulli-Verteilung]].

Eine [[Wahrscheinlichkeitsmaß|Verteilung]] lässt sich manchmal auch durch die [[Relative Häufigkeit]] bestimmen.

Die [[Bedingte Wahrscheinlichkeit]] benutzt man um Wahrscheinlichkeiten darzustellen, die sich ändern, wenn vorher eine Bedingung bekannt ist. Eine solche Wahrscheinlichkeit lässt sich mit der [[Bayes Formel]] berechnen. Oft ist der [[Satz von der totalen Wahrscheinlichkeit]] hier wichtig, da man mit ihm eine unbekannte Wahrscheinlichkeit durch die bedingten Wahrscheinlichkeiten ausrechnen kann. Zusammengefasst wird dann alles im [[Satz von Bayes]].

Zwei Ereignisse sind [[stochastisch unabhängig]], wenn die Wahrscheinlichkeit des gemeinsamen Ereignises gleich dem Produkt der Wahrscheinlichkeit der einzelnen Ereignisse ist.

Möchte man ein Experiment mehr als einmal durchführen nutzt man die [[Zusammenführung mehrerer Wahrscheinlichkeitsräume]] um einen großen Wahrscheinlichkeitsraum aufzustellen.

### Zufallsvariable

[[Zufallsvariable]]

---

## Diskrete Wahrscheinlichkeitsräume

- [[Diskreter Wahrscheinlichkeitsraum]]
- [[Zähldichte]]
- [[Laplace-Experiment]]
- [[Urnenmodell]]

## Verteilungen

Hier eine Liste an wichtigen Verteilungen.

- [[Gleichverteilung]]
- [[Exponentialverteilung]]
- [[Dirac-Verteilung]]
- [[Normalverteilung]]
- [[Hypergeometrische Verteilung]]
- [[Multinomialverteilung]]
- [[Poisson Verteilung]]
- [[Geometrische Verteilung]]
- [[Gedächtnislose Verteilung]]
- [[Negative Binomialverteilung]]
- [[Binomialverteilung]]
- [[Bernoulli-Verteilung]]

## Reele Wahrscheinlichkeitsräume

[[Reelle Wahrscheinlichkeitsräume]]
[[Wahrscheinlichkeitsdichte]]
[[Verteilungsfunktion]]

## Kenngrößen von Verteilungen und Zufallsvariablen

Oft ist man bei Experimenten vor allem an Kenngrößen von Verteilungen und Zufallsvariablen interessiert, da sie angeben welche Ergebnisse typischerweise zu erwarten sind.

Der [[Modalwert]] gibt mehr oder weniger den Wert an, der am meisten vorkommt.

[[Median]]
[[Perzentil]], Quantil

Mit dem [[Erwartungswert]], der den erwarteten Wert einer [[Zufallsvariable]] angibt lässt sich deren Streuung, also die [[Varianz]] und [[Standardabweichung]] berechnen.

Die [[Kovarianz]] lässt sich aus den Erwartungswerten von zwei Zufallsvariablen berechnen. Zusammen mit der Varianz lässt sich dann die [[Korrelation]] bestimmen, welche angibt wie und wie stark sich zwei Zufallsvariablen miteinander verändern.

## Summen unabhängiger Zufallsvariablen und Grenzwertsätze

### Summen von Zufallsvariablen

Die [[Faltung]] und [[Erzeugende Funktion]] kann man verwenden um (zufällige) Summen von Zufallsvariablen zu berechnen.

### Grenzwertsätze

Der Wahrscheinlichkeitstheorie liegt als Basis die [[Relative Häufigkeit]] zugrunde. Sie ist also ziemlich wichtig und es lohnt sich diesen Vorgang mal in der Theorie darzustellen um zu zeigen, dass unsere Intuition stimmt.

Die [[Relative Häufigkeit Theorie]] zeigt, warum die ganze Wahrscheinlichkeitstheorie überhaupt stimmt.

Mit der [[Ungleichung von Chebyshev]] lässt sich die Wahrscheinlichkeit des Fehlers zwischen Wert und [[Erwartungswert]] durch die Varianz abschätzen.

[[Schwaches Gesetz der großen Zahlen]]

[[Gleichung von Bienaymé]]

### Konvergenzarten und ihre Implikationen

[[punktweise Konvergenz]], [[gleichmäßige Konvergenz]] → [[p-fast sichere Konvergenz]] → [[Stochastische Konvergenz]] → [[Schwache Konvergenz]]

[[Starkes Gesetz der großen Zahlen]]

[[Fluktuation]]
[[Reskalierung]]
[[Konvergenzordnung]]
[[Kopplung]]

[[Schwache Konvergenz]]

[[Zentraler Grenzwertsatz]]

Mit einem [[Poisson-Prozess]] kann man die Anzahl an Auftritten eines Ereignisses in einem bestimmten Zeitraum bestimmen und Wahrscheinlichkeiten darauf berechnen.

## Markov-Ketten

Eine [[Markov-Kette]] zusammen mit einem [[Zustandsraum]] einer [[Anfangsverteilung]] und [[Übergangsmatrix]] ist hilfreich um Wahrscheinlichkeiten in einem System mit mehreren Zuständen zu berechnen.

[[Gleichgewichtsverteilung]]
