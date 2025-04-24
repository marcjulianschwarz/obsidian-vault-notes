---
uni-module: "LNS"
---

# Abstiegsrichtung

Ein Vektor $s$ heißt Abstiegsrichtung von $f$ im Punkt $x$ falls gilt:
$$\nabla f(x)^Ts<0$$
→ bedeutet geometrisch in einem Winkel von mindestens 90° zum [[Gradient]].
→ in Richtung entlang derer sich der Funktionswert verringert
→ siehe auch [[Richtungsableitung]]

Die Steigung in diese Richtung ist gegeben durch:
$$\nabla f(x)^T\frac{s}{||s||}$$
Der Vektor $s$ muss also nur normalisiert werden um die Steigung berechnen zu können.

> [!Info] Wichtige Bemerkung
> Für eine Abstiegsrichtung genügt es nicht, dass $f$ entlang $s$ abnimmt. Denn die Abnahme könnte auch allein durch negative Krümmung ([[Hessematrix]]) in diese Richtung hervorgerufen sein.
> besser erklären → siehe Skript seite 49
