---
uni-module: MFDS
---

# Lipschitz-stetig

Eine Abbildung ist lipschitz-stetig wenn sie [[Hölder-stetig]] ist mit $\alpha = 1$.

Also eine Abbildung ist es, wenn ein $L\geq0$ existiert mit
$$d_Y(f(x),f(y))\leq Ld_x(x,y)$$
für alle $x,y$.

Wenn $L>0$ ist, ist die Abbildung auch [[Stetigkeit|stetig]].

_Beweis, dass eine lipschitz-stetige Abbildung auch stetig ist:_
Man wählt $\epsilon >0$ und $\delta=\frac{\epsilon}{L}$ mit $\delta > d_X(x,y)$, dann lässt sich das Kriterium mit $\epsilon$ abschätzen.

Man spricht von einer [[Kontraktion]] wenn $L<1$ ist.

## Beschränktheit der Ableitung

Der [[Mittelwertsatz der Differentialrechnung]] liefert einen systematischen Ansatz zum beweisen der Lipschitz-stetigkeit einer Abbildung.
Wenn man die Beschränktheit der Ableitung zeigen kann, dann ist die Abbildung selbst lipschitz-stetig.
Wenn zusätzlich gilt, dass die Ableitung absolut gesehen immer kleiner als $L$ ist, dann ist sie eine [[Kontraktion]].

Etwas ähnliches kann wohl auch mit dem [[Hauptsatz der Differential- und Integralrechnung]] gezeigt werden.

_Related:_

- [[Fixpunktsatz von Banach]]
- [[Lokal Lipschitz-stetig]]
