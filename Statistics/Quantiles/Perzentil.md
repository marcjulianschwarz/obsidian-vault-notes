---
uni-module: EMD

alias: ["Quantile", "Quartile", "Quantil", "Quartil"]
---

# Das $\alpha$ Perzentil

Der Wert, für den gilt, dass $\alpha$ Prozent aller Datenpunkte kleiner sind und $1-\alpha$ Prozent der Werte größer sind.

## Definition

Let $F$ be a [[Verteilungsfunktion|CDF]]. Then $x_p$ is called $p$-Quantile if
$$F\left(x_{p}-\right) \leq p \leq F\left(x_{p}\right)$$

- $F$ has exactly one $p$-quantile when there is at most one $t$ with $F(t)=p$
- Similar definition when working with real probabilities $P((-\infty,x_p])\geq p$ and $P([x_p,\infty))\geq 1-p$

$x_{0.25},x_{0.5},x_{0.75}$ are called quartiles.

We can use quantiles to calculate

- [[Inter Quartile Range|IQR]]
- [[Median]]

We use the [[Quantile Function]] to quickly calculate quantiles of a given [[Verteilungsfunktion|CDF]].

Quantiles of a data sequence can be best [[Data Visualization|visualized]] using a [[Boxplot]].

---

> [!TIP] Empirical Quantiles
>
> $$
> \begin{aligned}
> &Q_{F_{n}(\cdot ; x)}^{-}(p)=\min \left\{t \in \mathbb{R} \mid \sum_{i=1}^{n} 1_{(-\infty, t]}\left(x_{(i)}\right) \geq n p\right\}=x_{(\lceil n p\rceil)} \\
> &Q_{F_{n}(\cdot ; x)}^{+}(p)=\max \left\{t \in \mathbb{R} \mid \sum_{i=1}^{n} 1_{(-\infty, t)}\left(x_{(i)}\right) \leq n p\right\}=x_{(\lfloor n p\rfloor+1)}
> \end{aligned}
> $$

> [!TIP] Smallest p-Quantile
>
> $$Q_{F}^{-}(p):=\min \{t \in \mathbb{R} \mid F(t) \geq p\}$$ > **Proof**
>
> - $F(t)\geq p$ exists since $F$ is bounded by $0$ and $1$ from below and above
> - Hence $t_p=\operatorname{inf}(F(t)\geq p)$
> - Due to [[right continuous|right continuity]] we even have $t_p=\operatorname{min}(F(t)\geq p)$

> [!TIP] Largest p-Quantile
> $$Q_{F}^{+}(p):=\max \{t \in \mathbb{R} \mid F(t-) \leq p\}$$

## Other Definition

$$
\begin{equation}\large
x_{p}:= \begin{cases}\frac{x_{N \cdot p}+x_{N \cdot p+1}}{2} & \text { falls } N \cdot p \text { ganzzahlig } \\ x_{\lfloor N \cdot p+1\rfloor} & \text { falls } N \cdot p \text { nicht ganzzahlig }\end{cases}
\end{equation}
$$
