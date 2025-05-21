---
uni-module: EMD
tags:
  - Algorithmus
aliases:
  - Newton Method
---
# Newton Verfahren

Für Polynome höherer Ordnung als 4 gibt es keine allgemeine Lösungsformel für Nullstellen → wir brauchen ein Verfahren um diese zu berechnen.

Das [[Newton Verfahren]] approximiert Nullstellen einer nichtlinearen Funktion von einem Startpunkt aus. Dabei verwendet man die [[Jacobi Matrix]] um die Funktion an dem Startpunkt zu linearisieren.

Mit dem [[Banach Lemma]] kann bewiesen werden, dass das Verfahren [[Superlineare Konvergenz|superlinear]] und [[Quadratische Konvergenz|quadratisch]] ([[Lokal Lipschitz-stetig]]) konvergiert.

## Iterationsvorschrift

$$x^{(k+1)}=x^{(k)}-J_{f}\left(x^{(k)}\right)^{-1} f\left(x^{(k)}\right)$$
Da die Invertierung der [[Jacobi Matrix]] für große Matrizen auwändig ist (und eventuell numerisch instabil im Computer), kann man eine andere Form verwenden, in der keine Invertierung sondern nur eine Lösung eines [[Lineares Gleichungssystem|LGS]] notwendig ist.

Dieses [[Lineares Gleichungssystem|LGS]] kann dann zum Beispiel effizient mit dem [[Jacobi-Verfahren]] gelöst
werden.

$$J_{f}\left(x^{(k)}\right) \underbrace{\left(x^{(k+1)}-x^{(k)}\right)}_{h^{(k)}}=-f\left(x^{(k)}\right)$$
$$x^{(k+1)}=h^{(k)}+x^{(k)}$$

## Algorithmus

1. Einen zufälligen Punkt (möglichst nahe an der Nullstelle) wählen
2. Tangente an diesem Punkt: $T(x)=f(x_0)+f'(x_0)\cdot (x-x_0)$
3. Nullstelle ist ungefähr die Nullstelle der Tangente $x=x_0-\frac{f(x_0)}{f'(x_0)}$
4. Wiederholen bis man in eine bestimmte Fehlertoleranz kommt

### Aber:

- Das Newton Verfahren [[Konvergenz|konvergiert]] nicht immer, das passiert zum Beispiel wenn der Anfangspunkt zu weit von der Nullstelle entfernt ist
- Auch ein Extremum oder eine kleine Ableitung zwischen Startwert und Nullstelle kann zur Divergenz führen
- Bei doppelten Nullstellen [[Konvergenz|konvergiert]] das Newton Verfahren nur extrem langsam
- Bei mehreren Nullstellen ist es nicht klar gegen welche Nullstelle das Verfahren [[Konvergenz|konvergiert]] (zum Beispiel beim sin) → möglichst nahe an der Nullstelle starten

Um einen guten Startwert zu finden kann man das [[Bisektionsverfahren]] mit dem [[Zwischenwertsatz]] verwenden.

## Konvergenzverhalten

Das [[Banach Lemma]] kann verwendet werden um Aussagen über das Konvergenzverhalten zu beweisen.

Es stellt sich heraus, dass es [[Superlineare Konvergenz|superlinear]] [[Konvergenz|konvergiert]]. Wenn zusätzlich die [[Jacobi Matrix]] [[Lokal Lipschitz-stetig]] ist, dann [[Konvergenz|konvergiert]] es sogar [[Quadratische Konvergenz|quadratisch]].

## Anwendung zum finden der Minima einer Funktion

Wir wenden das [[Newton Verfahren]] auf den [[Gradient|Gradienten]] der Funktion an und können so die Nullstellen davon finden, welche Minima und Maxima und [[Sattelpunkt|Sattelpunkte]] darstellen.

### In R

Mit der Funktion `lmn` kann mit dem Newtonverfahren das Minimum einer einfachen Funktion gefunden werden.
