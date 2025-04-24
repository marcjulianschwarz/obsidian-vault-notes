---
uni-module: "StochMod"

alias: "Relative Frequency"
---

# Relative Häufigkeit

Damit die relaitve Häufigkeit funktioniert muss man zuerst die Annahme machen, dass das Zufallsexperiment unter gleichen Bedingungen beliebig oft wiederholbar ist, wobei die Wiederholungen sich nicht gegenseitig beeinflussen dürfen, also [[stochastisch unabhängig | stochastische Unabhängigkeit]] vorliegt.

Die relative Häufigkeit eines [[Ereignis | Ereignises]] $A$ ist nach $n$ Widerholungen berechenbar durch
$$h_n(A):=\frac{1}{n}\cdot |A|$$
, wobei $|A|$ die Anzahl an Auftritten von $A$ ist.

## Relative Frequency for Interval

Uses [[Indikatorfunktion|indicator function]] like this:

$$h_{n}(I)=\frac{1}{n} \sum_{i=1}^{n} 1_{l}\left(x_{i}\right)$$

## True probability using limit of relative frequency

In typischen Fällen nähert sich $h_n(A)$ für große Werte einer Zahl zwischen 0 und 1 an, sodass man $P(A)$ als
$$\lim_{n\rightarrow \infty}h_n(A)$$
definieren kann. Damit ist das [[Wahrscheinlichkeitsmaß]] voll bestimmt.

Schlussendlich gilt für endlich viele Wiederholungen $P(\{1\})=\frac{k}{n}$ wobei $k$ die Anzahl des Ereignises ist und $n$ die Anzahl der Wiederholungen.

## Estimate error

You can estimate the **error** of the relative frequency compared to the true probability like this:
$$|h_n(I)-p(I)|\leq \frac{1}{\sqrt{n}}$$
The formula above is a rough estimate. This [[Confidence Interval]] (95%) is better:

$$p\in\left[ h_n - z_{1-\alpha/2}\frac{\sqrt{h_n(1-h_n)}}{\sqrt{n}}, h_n + z_{1-\alpha/2}\frac{\sqrt{h_n(1-h_n)}}{\sqrt{n}}\right]$$
