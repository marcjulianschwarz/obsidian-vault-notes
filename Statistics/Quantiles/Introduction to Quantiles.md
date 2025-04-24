# Introduction to Quantiles

We want to find a solution $t$ to the problem:
$$F(t)\geq p$$
to answer questions like "for which income do I belong to the richest 25%?"

> [!TIP] How can we calculate this value?
> Let $F$ be a [[Verteilungsfunktion|CDF]]. From Analysis we know that:
>
> - If $F$ is [[Stetigkeit|continous]] and strictly monotonic then $F(x)=p$ has $F^{-1}(p)$ as solution
> - If $F$ is only [[Stetigkeit|continous]] then the solution is a nonempty [[Kompaktheit|compact]] interval (more than one solution)
> - If $F$ does not attain value $p$ then there is a jump above it

- [[Perzentil|Quantile]]
- [[Quantile Function]]
- [[Inversion Lemma (Quantiles)|Inversion Lemma]]

> [!TIP] Convergence of quantiles and qq plots
> Let $F$ be a [[Verteilungsfunktion|CDF]] which is the limit of a sequence of [[Empirical cumulative distribution functions|ECDFS]].
>
> - If $F$ has exactly one p-quantile then the smallest and largest quantiles of the sequence of ECDFs converge to this p-quantile
> - Every [[Häufungspunkt|Accumulation Point]] of the smallest and largest quantiles of the sequence of CDFs is a p-quantile of $F$

Simple tests for distribution equality:

- [[qq-Plot]]
- [[pp-Plot]]