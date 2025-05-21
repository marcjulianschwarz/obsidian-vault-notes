---
uni-module: "LNS"
---

# Alpha-Unterschätzer

Die zulässige Menge muss für den $\alpha$-Unterschätzer ein Quader mit unteren Schranken $\underline{x}_i$ und oberen Schranken $\bar{x}_i$ sein. Für ein $\alpha\in[0,\infty)^n$ heißt die Funktion
$$\hat{f}_{\alpha}(x):=f(x)+\underbrace{\sum_{i=1}^{n} \alpha_{i}\left(\underline{x}_{i}-x_{i}\right)\left(\bar{x}_{i}-x_{i}\right)}_{=: \phi_{\alpha}(x)}$$
Alpha-Unterschätzer von $f$.

Dabei ist $\phi_{\alpha}$ der konvexe Teil der Funktion, da es ein Polynom zweiten Grades mit positiven Koeeffizienten ist. Das heißt, damit wir die Funktion konvex unterschätzen können sollte dieser Teil die Funktion überwiegen. Wir wollen $\alpha$ also groß genug wählen um [[Konvexe Funktion|Konvexität]] zu erreichen.
Gleichzeitig sollte $\alpha$ aber auch so klein wie möglich sein um den enstandenen Fehler (Relaxierungsfaktor) so gering wie möglich zu halten. Eine gutes Maß für die Wahl von $\alpha$ bietet:

$$\lambda_{\min }+2 \min _{i \in\{1, \ldots, n\}} \alpha_{i} \geq 0$$
denn der Unterschätzer ist konvex falls diese Ungleichung gilt, wobei $\lambda_i$ dem kleinsten [[Eigenwert]] der [[Hessematrix]] von $f$ entspricht.

Es lässt sich der kleinste Eigenwert einer symmetrischen Matrix $A$ abschätzen durch:
$$\lambda_{\min }\|x\|^{2} \leq x^{\top} A x \leq \lambda_{\max }\|x\|^{2}$$
_Beweis:_ Übungsaufgabe

![[Bildschirmfoto 2022-07-30 um 11.58.22.png]]
