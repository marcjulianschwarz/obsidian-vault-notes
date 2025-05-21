---
uni-module: "StochMod"
---

# Erzeugende Funktion

Für eine [[Zähldichte]] $f$ auf den natürlichen Zahlen ist die [[Potenzreihe]]:
$$\hat{f}(z):=\sum_{k=0}^{\infty} f(k) z^{k}$$
die sogenannte erzeugende Funktion.

Sie sind vor allem nützlich zur Berechnung von [[Erwartungswert]] und [[Varianz]].
Für den [[Erwartungswert]] gilt, wenn er existiert:
$$EX=\sum_{k=1}^{\infty} f_{X}(k) k=\left.\frac{d}{d z} \sum_{k=0}^{\infty} f_{X}(k) z^{k}\right|_{z=1}=\hat{f}_{X}^{\prime}(1)$$
Also die Ableitung der erzeugenden Funktion an der Stelle $x=1$.

Für die [[Varianz]] (wenn existent) gilt entsprechendes:
$$\operatorname{Var} X=\hat{f}^{\prime \prime}(1)+\hat{f}^{\prime}(1)-\left(\hat{f}^{\prime}(1)\right)^{2}$$

Für ein $|z|\leq 1$ aus den Komplexe Zahlen gilt außerdem:

$$|\hat{f}(z)| \leq \sum_{k=0}^{\infty}|f(k)||z|^{k} \leq \sum_{k=0}^{\infty} f(k)=1$$

![[Bildschirmfoto 2022-01-22 um 11.37.31.png]]
