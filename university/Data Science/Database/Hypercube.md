---
uni-module: "KonzMod"

alias: "Data Cube"
---

# Hypercube

A hypercube is defined by qualifiying data (dimensions) and quantifying data (facts).

The dimensions as the starting point for data analysis can be modeled using a [[Concept Hierarchy]].

![[IMG - Hypercube.png]]

Hier sieht man gut wie man über die Klassenhierarchien auf die einzelnen Dimensionen des Würfels zugreifen kann um dann die Fakten auszulesen.

## Darstellung

Struktur: `C[G, M]` wobei M die Menge der Fakten ist und G die Granularität.
![[IMG - Datacube Beispiele.png]]

## Implementierung

Man könnte den Datenwürfel direkt als mehrdimensionalen Array speichern. Allerdings wäre dieser dann [[Sparsity|sparse]] und schlecht skalierbar.

Eine weitere Möglichkeit ist Relational. Diese Technologie ist ausgereift und skalierbar allerdings wurden die Datenbanken nicht dafür konzipiert und haben dementsprechend eine schlechte Performanz. Eine Hybride Lösung würde beides vereinen, wäre aber sehr komplex.
