---
uni-module: "StochMod"

alias: ["Cumulative Distribution Function", "CDF"]
---

# Verteilungsfunktion

A function $F$
$$F:\mathbb{R}\rightarrow [0,1]$$
is called **CDF** when
$$\lim _{x \rightarrow-\infty} F(x)=0 \quad \lim _{x \rightarrow+\infty} F(x)=1$$
and $F$ is

- montonocally increasing ([[Proof Monotonic Increase]])
- [[right continuous]] ([[Proof of Right Continuity]])

$$F(x):=P((-\infty,x])$$

> [!TIP]- Properties of CDF
>
> - Left limits exist
> - jump positions are countable
> - If the [[Empirical cumulative distribution functions|ECDF]] converges [[gleichmäßige Konvergenz|uniformly]] to the CDF then all interval frequencies converge and the limit is called interval probability
> - for random numbers from a CDF the ECDF wil converge uniformly [[p-fast sichere Konvergenz|almost surely]] ([[Glivenko-Cantelli]])
> -

> [!TIP]- Relation to PDF
> If $P$ is defined by [[Wahrscheinlichkeitsdichte|PDF]] $f$, one can write
> $$F(x)=\int_{-\infty}^{x} f(y) d y \quad x \in \mathbb{R}$$
>
> Aus dem [[Hauptsatz der Differential- und Integralrechnung]] folgt also wenn $f$ [[Stetigkeit|stetig]] ist, der Zusammenhang:
> $$F' = f$$
> This way we also know that
> $$f(t)=\lim _{h \rightarrow 0} \frac{F(t+h)-F(t)}{h}$$
> which can be used to give a formula for a small interval probability based on $f(t)$ > $$\mathbb{P}((t, t+h]) \approx f(t) h$$
> for small $h$.

## Important Classes of CDF

- piecewise constant CDF
  - for example of uniformly discrete item
  - can be described with [[Zähldichte|PMF]]
- continous CDF
- Mixed types between continous and piecewise constant CDF
- CDF with [[Wahrscheinlichkeitsdichte|PDF]] where the [[Wahrscheinlichkeitsdichte|PDF]] is the slope of the [[Verteilungsfunktion|CDF]] at a given continouity point
  - [[Wahrscheinlichkeitsdichte|PDF]] times $h$ can approximate the interval probability of $(t,t+h]$ for $h$ small
