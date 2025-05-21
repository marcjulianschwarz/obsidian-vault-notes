---
uni-module: "ISSP"
---

# Quantile Function

Inverse function of [[Verteilungsfunktion|CDF]] by reflecting at the diagonal. Uses minimum [[Perzentil|Quantile]]. We can use this function to directly calculate quantiles of a given [[Verteilungsfunktion|CDF]].

In R, this can for example be done using the `qnorm` commands or the `quantile` function for the empirical case.

![[Bildschirmfoto 2022-06-14 um 16.06.08.png]]

- $Q_F^-$ is left [[Stetigkeit|continous]]
- $Q_F^+$ is right [[Stetigkeit|continous]]
- $F$ [[Stetigkeit|continous]] ←→ $Q_F^-,Q_F^+$ strictly monotonic
- $F$ strictly monotonic ←→ $Q_F^-,Q_F^+$ [[Stetigkeit|continous]]

The [[Inversion Lemma (Quantiles)]] basically proves that the [[Quantile Function]] is indeed the inverse function of the [[Verteilungsfunktion|CDF]].
