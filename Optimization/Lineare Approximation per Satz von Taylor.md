---
uni-module: "LNS"
---

# Lineare Approximation per Satz von Taylor

Gegeben sei eine [[Stetigkeit|stetige]] Funktion $f$, die einmal differenzierbar ist auf einer nichtleeren, offenen und [[Konvexe Menge|konvexen Menge]], dann gilt an der Entwicklungsstelle $x_0$:

$$f(x)=f\left(x_{0}\right)+\nabla f\left(x_{0}\right)^{\top}\left(x-x_{0}\right)+o\left(\left\|x-x_{0}\right\|\right)$$
Das Restglied wächst nur höchstens so schnell wie der Abstand von der Entwicklungsstelle zur approximierten Stelle.

## "Gestaltenwandler"

$$o\left(\left\|x-x_{0}\right\|\right)=\nabla f(\xi)^{\top}\left(x-x_{0}\right)-\nabla f\left(x_{0}\right)^{\top}\left(x-x_{0}\right)$$
wobei:
$$\xi:=(1-\theta) x_{0}+\theta x$$

$$f(x)=f\left(x_{0}\right)+\nabla f(\xi)^{\top}\left(x-x_{0}\right)$$
→ [[Mittelwertsatz der Differentialrechnung]]

Für $x\leftarrow x_0+p$ mit $p$ hinreichen klein
$$f\left(x_{0}\right)+\nabla f\left(x_{0}+\theta p\right)^{\top} p$$

$$f\left(x_{0}+p\right)=f\left(x_{0}\right)+\nabla f\left(x_{0}\right) p+o(\|p\|)$$
