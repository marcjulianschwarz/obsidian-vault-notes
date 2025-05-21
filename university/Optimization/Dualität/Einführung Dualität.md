---
uni-module: "LNS"
---

# Einführung Dualität

→ [[Dualität]]

Eine äquivalente Form oder zumindest untere Schranke des nichtlinearen Problems bildet das duale Problem.

Wenn wir das Supremum der [[Lagrange-Funktion]] beobachten können wir folgendes feststellen:

**_Für die Ungleichungsbedingungen:_**
Wenn $x\notin Z$ ist sind die Nebenbedingungen größer als 0. Die $\mu$ sind nach Definition größer als 0 und können entsprechend so gewählt werden, dass wir im Supremum $+\infty$ erhalten.

Wenn $x\in Z$ ist sind die Nebenbedingungen entweder [[Indexmenge der Aktiven Ungleichungsbedingungen|aktiv]] (also $=0$) oder $<0$.
Für aktive Ungleichungen ist $\mu$ unerheblich und das Supremum ist $f(x)$.
Für Ungleichungen $<0$ werden wegen dem Supremum die $\mu$ auf 0 gesetzt womit das Supremum $f(x)$ ist.

**_Für die Gleichungsnebenbedingungen:_**
Wenn $x\notin Z$ ist sind die Nebenbedingungen ungleich 0.
Für Nebenbedingungen $<0$ kann $\lambda$ negativ gewählt werden um im Supremum $+\infty$ zu erhalten. Für Nebenbedingungen $>0$ kann $\lambda$ positiv gewählt werden um im Supremum $+\infty$ zu erhalten.

Wenn $x\in Z$ ist sind die Nebenbedingungen gleich 0. Die $\lambda$ sind also unerheblich und es folgt im Supremum $f(x)$.

Aus dieser Beobachtung folgt also die Form:
$$p(x):=\sup _{\lambda \in \mathbb{R}^{m}, \mu \in \mathbb{R}_{+}^{\ell}} \mathcal{L}(x, \lambda, \mu)= \begin{cases}f(x), & \text { falls } x \in Z, \\ +\infty, & \text { sonst. }\end{cases}$$
Damit ist unser primales Problem definiert als:
$$\inf _{x \in \mathbb{R}^{n}} \sup _{\lambda \in \mathbb{R}^{m}, \mu \in \mathbb{R}_{+}^{\ell}} \mathcal{L}(x, \lambda, \mu) .$$
Außerdem folgt das [[Lagrange-duales Problem|Lagrange-duale Problem]].

Für jedes feste $x$ ist die [[Lagrange-Funktion]] linear weshalb für die duale Zielfunktion als Infimum von linearen Funktionen folgt, dass sie [[Konvexe Menge|konkav]] ist.
Also ist das duale Problem ein Maximierungsproblem einer konkaven Funktion auf einer [[Konvexe Menge|konvexen Menge]], also äquivalent zu einem konvexen Optimierungsproblem.

Aus dem [[Schwacher Dualitätssatz|schwachen Dualitätssatz]] folgt, dass das duale Problem stets eine untere Schranke des primalen optimalen ZFW darstellt.
Die beiden optimalen ZFW sind gleich, wenn die [[Lagrange-Funktion]] einen [[Sattelpunkt]] besitzt.

[[Sattelpunkt der Lagrange-Funktion]] ← → globale Lösung für primales und duales Problem mit gleichem ZFW.
