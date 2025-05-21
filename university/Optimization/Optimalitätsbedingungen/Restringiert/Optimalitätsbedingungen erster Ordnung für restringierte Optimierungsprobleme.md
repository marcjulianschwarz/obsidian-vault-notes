---
uni-module: "LNS"
---

# Optimalitätsbedingungen erster Ordnung für restringierte Optimierungsprobleme

Jetzt mit mindestens einer Gleichungs oder Ungleichungs Nebenbedingung, also:
$m+l>0$
$f,g_i,h_j\in C^1(\mathbb{R}^n, \mathbb{R})$ → [[Stetigkeit|stetig]] diffbar

Alle nicht aktiven Ungleichungen können lokal ignoriert werden. [[Indexmenge der Aktiven Ungleichungsbedingungen]]

Um über ein restringiertes Problem optimieren zu können müssen wir eine Richtung finden, in die man optimieren kann ohne sich aus der zulässigen Menge zu bewegen und in welche sich der Zielfunktionswert verringert.

Alle [[Zulässige Richtung|zulässigen Richtungen]] bilden den [[Tangentialkegel]]. Für eine lokale Lösung muss gelten, dass der [[Tangentialkegel]] in diesem Punkt keine zulässige [[Abstiegsrichtung]] mehr enthält.

Diese Bedingung ist allerdings recht umständlich weswegen man den [[Linearisierungskegel]] im Punkt $x$ bildet um den zulässigen Bereich um $x$ herum zu approximieren.

Im Allgemeinen gilt, dass der [[Linearisierungskegel]] eine Obermenge des [[Tangentialkegel]] ist.

![[Drawing 2022-07-13 11.36.00.excalidraw]]

Die Bedinung, dass beide Kegel gleich sind nennt man [[Abadie Constraint Qualification]].
Wenn die [[Abadie Constraint Qualification|ACQ]] gilt, gilt also nun auch, dass bei einer lokalen Lösung der [[Linearisierungskegel]] keine zulässige [[Abstiegsrichtung]] mehr enthält.
Der [[Linearisierungskegel]] ist leichter zu berechnen.

[[Karush-Kuhn-Tucker Conditions]]

[[Linear Independence Constraint Qualification]]

[[Lagrange-Newton-Verfahren]]

Ist $f$ und $g_i$ [[Konvexe Funktion]] und ist $x^*$ [[Karush-Kuhn-Tucker Conditions|KKT]]-Punkt, dann ist $x^*$ globale Lösung.

_Beweis:_
Seien zusätzlich die linearen Nebenbedingungen in der [[affin-linear|affin-linearen]] Form, dann ist die zulässige Menge konvex. Insbesondere ist $x^*\in Z$.
Mit der Definition von $f$ [[Konvexe Funktion|konvex]] lässt sich abschätzen:
$$f(x)-f\left(x^{*}\right) \geq \nabla f\left(x^{*}\right)^{\top}\left(x-x^{*}\right)$$
Mit der dritten Bedingung der [[Karush-Kuhn-Tucker Conditions|KKT]] Bedingungen lässt sich auf der rechten Seite der [[Gradient]] ersetzen.

Aus den vorherigen Überlegungen folgt die wichtige [[Notwendige Optimalitätsbedingung erster Ordnung restringierter Probleme]].

[[Notwendige Optimalitätsbedingung erster Ordnung für lineare Nebenbedingungen]]

Aus den Überlegungen folgt damit:

> [!NOTE]
> Wenn $f$ [[Konvexe Funktion|konvex]] ist und alle Nebenbedingungen [[affin-linear]] sind, dann ist $x^*$ genau dann eine globale Lösung wenn $x^*$ ein [[Karush-Kuhn-Tucker Conditions|KKT]] Punkt ist.
