---
uni-module: ["EMD", "LKO"]

alias: [Netzwerk]
---
# Flussnetzwerk

Ein Flussnetzwerk ist ein gewichteter [[Digraph]] $D=(V,A)$ . Dabei bezeichnen wir die Gewichte einer Kante als die Bogenkapazität $c_a$.
Außerdem wird in einem Flussnetzwerk ein Knoten als Quelle $s$ und einer als Senke $t$ bezeichnet. Wenn man mehrere Quellen und Senken hat verwendet man Superquellen und Supersenken mit unendlicher Kapazität um sie auf jeweils einen Knoten zu reduzieren.
Das Quadrupel $(D,c,s,t)$ bildet das Flussnetzwerk .

Auf einem Flussnetzwerk kann ein [[Fluss]] definiert werden.

- [[Max-Flow Problem]]
- [[Min-Cut Problem]]

Auf einem [[Flussnetzwerk]] kann ein zulässiger [[Fluss]] definiert werden, wenn dieser die [[Kapazitätsbedingung]] und [[Flusserhaltungsbedingung]] erfüllt.

Beim [[Max-Flow Problem]] sucht man einen [[Maximaler Fluss | maximalen Fluss]]. Zum lösen dieses Problems gibt es den primalen [[Ford-Fulkerson Algorithmus]] und den [[Dualität|dualen]] [[Goldberg–Tarjan Algorithmus]].

Der Ford-Fulkerson Algorithmus gibt zusätzlich zum maximalen Fluss noch einen [[Minimaler Schnitt|Min-Cut]] zurück. Dieser gilt nach dem [[Max-Flow-Min-Cut-Theorem]] als ein Zertifikat dafür, dass die Lösung optimal ist.
Der Algorithmus verwendet das Konzept [[Augmentierender Weg | Augmentierender Wege]] um den Fluss auch "nach hinten" zu bewegen.

Der [[Goldberg–Tarjan Algorithmus]] hingegen ist ein [[Push-Relabel Algorithmus]]. Er verwendet einen [[Pseudofluss]] um erstmal so viel wie möglich in das Flussnetzwerk zu stecken.
Dabei entsteht oft ein [[Überschuss]], der unter anderem durch Relabeling entfernt werden muss. Beim Relabeling wird mittels [[Gültige Markierung | gültiger Markierungen]] versucht den Fluss möglichst Richtung Senke fließen zu lassen.

Schlussendlich sagt uns der [[Ganzzahligkeitssatz]], dass jeder maximale Fluss einen ganzzahligen Wert hat, wenn die Kapazitäten in diesem Fluss auch ganzzahlig sind.

## Minimalkosten-Fluss-Problem 

Ein [[Minimalkosten-Fluss-Problem]] basiert auf Kosten und einer [[Bedarfsfunktion]].
Es lässt sich lösen indem man es in ein [[Minimalkosten-Zirkulations-Problem]] umwandelt. Dieses Problem basiert auf einer [[Zirkulation]].
Das neue Problem kann dann relativ einfach mit folgenden Optimalitätsbedingungen gelöst werden:
Das [[Negative-Kreise-Optimalitätsbedingung]] basiert auf dem

Für das nächste braucht man [[Reduzierte Kosten]]

[[Sukzessive-Kürzeste-Wege-Algorithmus]]