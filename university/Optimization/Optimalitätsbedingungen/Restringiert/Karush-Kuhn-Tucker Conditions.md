---
alias: "KKT"
uni-module: LNS
---

# Karush-Kuhn-Tucker Conditions

$$
\begin{aligned}
h_{j}(x) &=0 &(j&=1, \ldots, m), \\
g_{i}(x) & \leq 0 & &(i=1, \ldots, \ell), \\
\nabla f(x)+\sum_{j=1}^{m} \lambda_{j} \nabla h_{j}(x)+\sum_{i=1}^{\ell} \mu_{i} \nabla g_{i}(x) &=0, & & \\
\mu_{i} g_{i}(x) &=0 & &(i=1, \ldots, \ell), \\
\mu_{i} & \geq 0 & &(i=1, \ldots, \ell)
\end{aligned}
$$

Die ersten beiden Bedingungen geben an, dass $x$ zulässig ist.

Die dritte Bedingung sagt aus, dass sich der [[Gradient]] von $f$ als [[Linearkombination]] der [[Gradient|Gradienten]] der Nebenbedingungen $h_j$ und als konische Kombination ([[konische Hülle]]) der Nebenbedingungen $g_i$ schreiben lässt.

Hier ein Beispiel für die dritte Bedingung. Der negative [[Gradient]] liegt im Kegel (konische Hülle) der Nebenbedingungen, somit ist die dritte Bedingung mit bestimmten $\mu_i$ erfüllt.

![[Bildschirmfoto 2022-07-13 um 09.03.35.png]]

Die vierte Bedingung heißt Komplementaritätsbedingung.

$\lambda$ und $\mu$ sind [[Lagrange-Multiplikatoren]].

Keine Restriktionen → [[Notwendige Optimalitätsbedingung erster Ordnung unrestringierter Probleme]]

Da die $\lambda_j$ kein Vorzeichen haben kann man für die [[Linearkombination]] auch schreiben:
$$\sum_{j=1}^{m} \lambda_{j} \nabla h_{j}(x) = -\sum_{j=1}^{m} \lambda_{j} \nabla h_{j}(x)$$

Mit der [[Lagrange-Funktion]] lässt sich die dritte Bedinung auch als
$$\nabla_{x} \mathcal{L}(x, \lambda, \mu)=0$$
schreiben.

Wenn alle Funktionen zweimal [[Stetigkeit|stetig]] differenzierbar sind lässt sich die [[Hessematrix]] bestimmen als:
$$\nabla_{x x}^{2} \mathcal{L}(x, \lambda, \mu)=\nabla^{2} f(x)+\sum_{j=1}^{m} \lambda_{j} \nabla^{2} h_{j}(x)+\sum_{i=1}^{l} \mu_{i} \nabla^{2} g_{i}(x)$$

## KKT-Punkte bestimmen

- [[Nichtlineares Optimierungsproblem|NLP]] in die Form bringen mit $f,g_i,h_i$.
- [[Gradient|Gradienten]] aller Funktionen bestimmen
- Alle Fälle der [[Indexmenge der Aktiven Ungleichungsbedingungen]] durchgehen und auf [[Lagrange-Funktion]] testen
  - Jeweils auf die anderen Bedingungen wie $\mu >0$ testen
  - falls **alle** Bedingungen gelten → $x$ bestimmen
- Mit der Information, dass Ungleichung aktiv ist und dem $x$ kann $y$ berechnet werden
- Punkt auf Zulässigkeit testen (andere Bedingungen)
- [[Linear Independence Constraint Qualification|LICQ]] überprüfen
- Für zwei aktive Ungleichungen können diese kombiniert werden um ein $x$ und $y$ zu berechnen. → Andere Bedinungen testen

## ML4ENG

apply for the given problem:

$$
\begin{equation}
\begin{gathered}
\alpha_{i} \geq 0 \\
y_{i}(w \cdot x-b)-1 \leq 0 \\
\alpha_{i}\left[y_{i}(w \cdot x-b)-1\right]=0
\end{gathered}
\end{equation}
$$

Based on the last condition $\alpha _i = 0$ or $y_i(w \cdot x -b) = 1$ for each training point.

When $\alpha _i$ is not zero, we call the training point a support vector since it is right on the margin.

We can now use our previously derived function to calculate $w$ with our newly gained $\alpha _i$:

Depending on the sign of our result, the datapoint is either in class +1 or -1:

$$
\begin{equation}
y=\operatorname{sgn}(\boldsymbol{w} \cdot \boldsymbol{x}-b)=\operatorname{sgn}\left(\sum_{i=1}^{n} \alpha_{i}^{*} y_{i} \boldsymbol{x}_{i} \cdot \boldsymbol{x}\right)
\end{equation}
$$
