---
uni-module: "StochMod"

alias: ["Normalapproximation", "Central Limit", "Central Limit Theorem"]
---

# Zentraler Grenzwertsatz

We can use normal approximation to create [[Confidence Interval|CIs]] for a [[Zufallsvariable|Random Variable]].

Es seien $X_i$ [[stochastisch unabhängig|stochastisch unabhängige]] identisch [[Wahrscheinlichkeitsmaß|verteilter]] [[Zufallsvariable|Zufallsvariablen]] mit [[Erwartungswert]] $EX_1=\mu$ und [[Varianz]] $\operatorname{Var}{X_1}=\sigma^2>0$ , dann gilt:

$$P\left(\frac{1}{\sqrt{n} \sigma} \sum_{k=1}^{n}\left(X_{k}-\mu\right) \leqslant x\right) \stackrel{n \rightarrow \infty}{\rightarrow} \int_{-\infty}^{x} \frac{1}{\sqrt{2 \pi}} e^{-\frac{1}{2} y^{2}} d y\quad\forall x\in\mathbb{R}$$

Ein klassisches Problem ist zum Beispiel die Berechnung der Konvergenzgeschwindigkeit [[Zentraler Grenzwertsatz|des zentralen Grenzwertsatzes]].
→ [[Satz von Berny-Esseen]]
