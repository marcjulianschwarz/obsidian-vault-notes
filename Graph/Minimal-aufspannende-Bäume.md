---
uni-module: EMD, LKO

alias: [Minimaler Spannbaum]
---

# Minimal aufspannende Bäume

- [[Schnitt]] → Partition eines Graphen in zwei Teile
- Eine Kante kreuzt den [[Schnitt]], wenn die beiden Knoten in der jeweils anderen Hälfte des Schnitts liegen
- Ein [[Schnitt]] respektiert eine Menge an Kanten, wenn keine dieser Kanten den [[Schnitt]] kreuzt
- leichte kreuzende Kante → Eine kreuzende Kante mit minimalem Gewicht

Es gibt verschiedene Methoden einen minimal aufspannenden Baum zu finden:

- [[MST-Algorithmus von Kruskal]]
- [[MST-Algorithmus von Prim]]

Beide Algorithmen (Kruskal, Prim) sind sogenannte Greedy Algorithmen. Allerdings funktionieren diese Algorithmen nicht immer optimal (z.B. beim Travelling Salesman Problem).
