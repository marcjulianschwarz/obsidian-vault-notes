---
uni-module: ["StochMod", "EMD"]

alias: ["Correlation", "Pearson Correlation"]
---

# Korrelation

Mit der [[Kovarianz]] und falls die [[Varianz]] von $X$ und $Y$ jeweils positiv ist, gilt:
$$\rho(X,Y):=\frac{Cov(X,Y)}{\sqrt{VarX}\sqrt{VarY}}$$
Wenn die [[Kovarianz]] und damit auch die [[Korrelation]] Null ist nennt man $X$ und $Y$ unkorreliert. Das gilt auch wenn die beiden [[Zufallsvariable |Zufallsvariblen]] [[stochastisch unabhängig]] sind.

Die Korrelation liegt zwischen $-1$ und $1$.
→ Proof by [[Cauchy-Schwartz]]

## Interpretation der Korrelation

_Positive Korrelation_: große Werte in $X$ → große Werte in $Y$, analog mit kleinen Werten
_Negative Korrelation_: große Werte in $X$ → kleine Werte in $Y$, analog mit kleinen Werten.

> [!WARNING] Important
> [[Korrelation|Correlation]] is not [[Causation]] > [[Correlation is not Causation]]

## Definition nach EMD

$$
\begin{equation}\large
\rho_{x y}=\frac{s_{x y}}{s_{x} \cdot s_{y}} \in[-1,1]
\end{equation}
$$

→ Erklärung zur Formel: Kovarianz geteilt durch das Produkt der beiden Standardabweichungen.

## Sample Correlation

$$\frac{\sum_{i=1}^n\left(a_i-\mu_A\right)\left(b_i-\mu_B\right)}{n \cdot \sigma_A \sigma_B}$$

## Analysis

See [[Correlation Analysis]].
