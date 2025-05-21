---
uni-module: LKO

tags: Algorithmus
---

# MST-Algorithmus von Prim

Dieser Algorithmus verwendet die [[Pfad-Optimalitätsbedingung]].

![[Bildschirmfoto 2022-01-06 um 16.38.33.png]]

### [[Python]] Implementierung

```python

```

Der Algorithmus von Prim funktioniert auf dem gleichen Prinzip wie der [[MST-Algorithmus von Kruskal]] und ist eine Art Variation dieses Algorithmus. Ein Clustering macht mit diesem Algorithmus keinen Sinn, weil es immer einen großen und dann n-1 einzelen Knoten als Cluster gibt.

1. Wähle einen Knoten
2. Wähle die Kante mit minimalem Gewicht, die einen isolierten Knoten mit dem Baum verbindet
3. Wiederhole 2.
