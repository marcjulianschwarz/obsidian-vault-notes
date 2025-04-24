---
uni-module: ["EMD", "LKO"]
---

# Min-Cut Problem

Der minimale Schnitt (min cut) eines [[Flussnetzwerk]] ist ein [[Schnitt]], dessen Kapazität im Vergleich zu allen anderen Schnitten minimal ist.
Das Min-Cut Problem lässt sich zusammen mit dem [[Max-Flow Problem]] lösen.

## Clustering mit Min-Cut

Man kann den Min-Cut auch als Decision Boundary für ein Clustering verwenden. Dabei wählt man in einem Graphen zufällig zwei Knoten als Quelle und Senke und baut den Graphen in ein Flussnetzwerk um.
Jetzt kann man den Algorithmus für das Max-Flow Problem anwenden und hat am Ende einen [[Schnitt]], der die beiden Cluster von einander trennt. Den Algorithmus kann man auch rekursiv auf die entstandenen Cluster anwenden um noch mehr Cluster zu finden.
Falls die Wahl von Quelle und Senke zu unerwünschten Ergebnissen führen kann man sie entweder nochmal zufällig wählen oder man fügt einen neuen Knoten als Senke hinzu und verbindet alle anderen Knoten mit ihm mit Gewichten Alpha. Man kann dann so lange Alpha verändern bis gute Cluster entstehen.
