---
uni-module: "LNS"

tags: Algorithmus
---

# Feasibility Pump

[[Konstruktionsheuristik]], die zwei Folgen von Punkten konstruiert.

Die eine Folge besteht aus zulässigen Punkten für $P$ ([[Polyeder]]), die aber eventuell nicht ganzzahlig sind.
Die andere Folge besteht aus ganzzahligen Punkten, die aber eventuell nicht zulässig sind.

## Vorgehen

1. Wähle zulässigen Punkt für $P$
2. Runde Punkt zu einem ganzzahligen Punkt
3. Zulässigen Punkt in $P$ bestimmen, der bezüglich der [[Manhattan Distance]] am nächsten an dem gerundeten Punkt liegt
4. Wiederhole bei 2.

![[Bildschirmfoto 2022-07-14 um 15.25.01.png]]

## Arbeitsweise

![[Bildschirmfoto 2022-07-14 um 15.25.42.png]]
