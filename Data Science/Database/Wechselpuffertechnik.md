---
uni-module: IDB
---

# Wechselpuffertechnik

![[IMG - Wechselpuffertechnik.png]]

Wir können also während Puffer 1 schreibt noch mehr Sätze in den nächsten Puffer legen. (asynchron).

Die Anwendung ist also schneller, da sie die Info schnell bekommt, dass die Daten angekommen sind. Erst falls alle Puffer voll sind müsste man warten.

Diese Optimierung ist nur durch die Kapselung [[Schichtenbildung]] möglich geworden. Die Anwendung bekommt davon gar nichts mit.

> _Rein interne Optimierung_
