# Graphengenerierung

Ein [[Graph]] lässt sich aus einer Menge an Datenpunkten konstruieren. Dafür braucht man erstmal nur eine Funktion, die ein Gewicht zwischen zwei Datenpunkten berechnet (z.B. die euklidische Distanz). Normalerweise würde daraus dann ein [[Graph]] entstehen, bei dem alle Knoten mit allen Knoten verbunden sind. Das würde schnell dazu führen, dass die Anzahl der Kanten sehr groß wird. Um das zu vermeiden möchte man nur einen Teilgraphen generieren. Dafür gibt es verschiedenen Methoden:

- vollständigen Graphen betrachten → [[Minimal-aufspannende-Bäume | Minimal aufspannenden Baum]] konstruieren.
- $\epsilon$-Ball-[[Graph]] → nur Kanten verwenden, die eine kleinere Entfernung als $\epsilon$ haben (könnte man auch verwenden um Cluster zu erkennen)
- k-nearest-neighbor-[[Graph]] → nur Kanten zwischen den k-nächsten Nachbarn verwenden