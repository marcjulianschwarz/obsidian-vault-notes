---
uni-module: "StochMod"
---

# Faltung

Eine Faltung ist eine Operation auf zwei [[Zähldichte | Zähldichten]] $f$ und $g$ mit ihren [[Wahrscheinlichkeitsmaß | W-Maßen]] $P$ und $Q$ .

$$
\begin{aligned}
&f * g: \mathbb{Z} \rightarrow \mathbb{R} \\
&(f * g)(z):=\sum_{x \in \mathbb{Z}} f(x) g(z-x)
\end{aligned}
$$

Die Faltung ist auch eine [[Zähldichte]] auf $\mathbb{Z}$. Das [[Wahrscheinlichkeitsmaß]] zu der neuen [[Zähldichte]] ist $P*Q$.

Die Faltung ist _assoziativ, kommutativ und distributiv._ Damit kann man sie induktiv für mehr als zwei Zähldichten definieren.

## Für den reellen Fall

$$f_{x+y}(z)=\left(f_{x}+f_{y}\right)(z):=\int_{-\infty}^{\infty} f_{x}(x) f_{y}(z-x) d x$$
→ Die sogenannte [[Lebesguie Dichte]]

## Summe von Zufallsvariablen

Für zwei [[stochastisch unabhängig|stochastisch unabhängige]] [[Zufallsvariable|Zufallsvariablen]] mit ihren [[Wahrscheinlichkeitsmaß|Verteilungen]] und [[Zähldichte|Zähldichten]] gilt:
$$f_{X+Y}=f_X*f_Y$$

### Beweis

Den Beweis führt man über eine [[disjunkte Aufteilung]]:
![[Bildschirmfoto 2022-01-22 um 11.22.41.png]]

## Resultate

Die Summe von $n$ [[Normalverteilung|normalverteilten]] Zufallsvariablen ist wieder eine normalverteile [[Zufallsvariable]] mit [[Erwartungswert]] gleich der Summer der Erwartungswerte und [[Varianz]] gleich der Summer der Varianzen.

Die Summe von [[Binomialverteilung|Binomialverteilungen]] ist wieder eine Binomialverteilung mit $Bin_{n+m,p}$. Außerdem ist die Summe von $n$ [[Bernoulli-Verteilung|Bernoulli-Verteilungen]] eine [[Binomialverteilung]].

→ Die Faltung tritt auch bei der Produktbildung von [[Potenzreihe | Potenzreihen]] und Polynomen auf → [[Erzeugende Funktion]]
