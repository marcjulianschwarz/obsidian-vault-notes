---
uni-module: "KRY"

alias: "Affin-lineare Blockchiffrierung der Länge 2"
---

# ALBC-2-Verschlüsselung

Ein Spezialfall der [[ALBC-k-Verschlüsselung]], eine [[Blockchiffre]].

> [!ABSTRACT] Verschlüsselung
>
> - [[Alphabet]]: Großbuchstaben, identifiziert mit den Zahlen $0\dots 25$.
> - [[Schlüssel]]: $K$ ist ein $6$-Tuple $K=(k_{1},k_{2},k_{3},k_{4},k_{5},k_{6})$ mit $k$ aus $0\dots 25$ und die [[ggT-Bedingung]] gilt.
> - Verschlüsselungsfunktion ist für den Block $\begin{pmatrix} x  & y\end{pmatrix}$ gegeben als
>   $$
>   f_{k}(\begin{pmatrix}
>   x \\
>   y \\
>   \end{pmatrix})=\begin{pmatrix}
>   k_{1} & k_{2} \\
>   k_{4} & k_{5}
>   \end{pmatrix}\begin{pmatrix}
>   x \\
>   y \\
>   \end{pmatrix}+\begin{pmatrix}
>   k_{3} \\
>   k_{6}
>   \end{pmatrix}\operatorname{mod}(26)
>   $$
>   **Verfahren:**
>
> 1. Der Klartext wird in $n$ Blöcke der Länge $2$ aufgeteilt. Der Text ist also $x_{1}y_{1},x_{2}y_{2}\dots$
> 2. Der Chiffretext entsteht dann durch $$\widetilde{x}_i=k_1 x_i+k_2 y_i+k_3 \bmod N, \quad \widetilde{y}_i=k_4 x_i+k_5 y_i+k_6 \bmod N$$

> [!CHECK] Entschlüsselung
> **Verfahren:**
>
> 1. Finde ein $d$, sodass die [[ggT-Bedingung]] $d\left(k_1 k_5-k_2 k_4\right) \bmod 26=1$ erfüllt ist
> 2. Berechne den inversen Schlüssel mit $$\begin{aligned}
> \ell_1 &=d k_5 \bmod 26=75 \bmod 26=23 \\
> \ell_2 &=\left(-d k_2\right) \bmod 26=(-40) \bmod 26=12 \\
> \ell_3 &=d\left(k_2 k_6-k_3 k_5\right) \bmod 26=(-715) \bmod 26=13 \\
> \ell_4 &=\left(-d k_4\right) \bmod 26=(-115) \bmod 26=15 \\
> \ell_5 &=d k_1 \bmod 26=25 \bmod 26=25 \\
> \ell_6 &=d\left(k_3 k_4-k_1 k_6\right) \bmod 26=1605 \bmod 26=19
> \end{aligned}$$
> 3. Der Klartext wird in $n$ Blöcke der Länge $2$ aufgeteilt. Der Text ist also $x_{1}y_{1},x_{2}y_{2}\dots$
> 4. Entschlüsselung durch $$x_i=\ell_1 \widetilde{x}_i+\ell_2 \widetilde{y}_i+\ell_3 \bmod 26, \quad y_i=\ell_4 \widetilde{x}_i+\ell_5 \widetilde{y}_i+\ell_6 \bmod 26 .$$

Die Anzahl der möglichen Schlüssel ist $N^6$, nach ausfiltern mit der [[ggT-Bedingung]] sind es nur noch
$$\left\{\left(k_1, k_2, k_3, k_4, k_5, k_6\right): 0 \leq k_i \leq N-1, \operatorname{ggT}\left(N, k_1 k_5-k_2 k_4\right)=1\right\}$$

mit
$$ N^6 \prod\_{p \mid N}\left(1-\frac{1}{p}\right)\left(1-\frac{1}{p^2}\right)=106299648$$

> [!WARNING] ALBC-2 ist unsicher
>
> Wenn Teile des Klartexts erraten werden kann man den inversen Schlüssel durch dieses [[Lineares Gleichungssystem|LGS]] lösen:
>
> $$
> \begin{array}{ll} x_1 \equiv \ell_1 \widetilde{x}_1+\ell_{2}\widetilde{y}_1+\ell_3 \bmod 26, & y_1 \equiv \ell_4 \widetilde{x}_1+\ell_5 \widetilde{y}_1+\ell_6 \bmod 26, \\
> x_2 \equiv \ell_1 \widetilde{x}_2+\ell_2 \widetilde{y}_2+\ell_3 \bmod 26, & y_2 \equiv \ell_4 \widetilde{x}_2+\ell_5 \widetilde{y}_2+\ell_6 \bmod 26, \\
> x_3 \equiv \ell_1 \widetilde{x}_3+\ell_2 \widetilde{y}_3+\ell_3 \bmod 26, & y_3 \equiv \ell_4 \widetilde{x}_3+\ell_5 \widetilde{y}_3+\ell_6 \bmod 26
> \end{array}
> $$
