---
uni-module: LKO

tags: Algorithmus
---

# MST-Algorithmus von Kruskal

Dieser Algorithmus verwendet die [[Schnitt-Optimalitätsbedingung]].

![[Bildschirmfoto 2022-01-06 um 16.37.10.png]]

### [[Python]] Implementierung

```python

```

## Zwei Arten der Implementierung:

### 1.

Beim Kruskal [[Algorithmus]] wählt man immer die Kanten mit minimaler Distanz, die zwei disjunkte Teilbäume miteinander verbinden aus.

### 2.

- $T=\emptyset$
- Kanten nach Gewichten sortieren
- Kanten durchlaufen
  - Wenn man die Kante zu $T$ hinzufügen kann ohne, dass ein [[Kreis]] entsteht, dann fügt man diese Kante zu $T$ hinzu.
- $T$ ist [[Minimal-aufspannende-Bäume|Minimaler Spannbaum]]

![[Clustering mit Kruskal]]
