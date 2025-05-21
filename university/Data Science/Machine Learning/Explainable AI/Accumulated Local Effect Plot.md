---
uni-module: "XAI"

alias: "ALE"
---

# Accumulated Local Effect Plot

> [!NOTE]+ Definition
> Describes how features influence the prediction of a [[Machine Learning|ML]] model on average. ALE plots are faster and unbiased alternative to [[Partial Dependence Plot|PDPs]]. ALE plots are more meaningful in the case of correlated features.

The computation of a [[Partial Dependence Plot|PDP]] for a feature that is strongly correlated with other features involves averaging predictions of artificial [[Dataset|data]] instances that are unlikely in reality.

To get rid of unlikely [[Dataset|data]] points we can use a [[Marginal Plot]] where we only look at the conditional distribution (bin around a value). This however still includes the effects of correlated features.
E.g. lets say we have a feature that does not influence the target but it is strongly correlated to a different feature that does influcence it. Now when we create a [[Marginal Plot]] for that feature, we would still see an effect even though it doesn't exist.

So we want to remove the correlation. We do this by only looking at a small interval and calculating the gradients (differences) in this small interval. In the end we integrate over these gradients to get the actual values.

1. Divide features into intervals
2. For each interval
   1. For each datapoint in interval
      1. Calculate prediction difference of lower and upper limit
   2. Average prediction differences
3. Integrate prediction differences
4. Center

![[Bildschirmfoto 2023-07-11 um 09.58.26.png]]

$$
\begin{aligned}
\hat{f}_{S, A L E}\left(x_S\right) & =\int_{z_{0, S}}^{x_S} E_{X_C \mid X_S=x_S}\left[\hat{f}^S\left(X_s, X_c\right) \mid X_S=z_S\right] d z_S-\text { constant } \\
& =\int_{z_{0, S}}^{x_S}\left(\int_{x_C} \hat{f}^S\left(z_s, X_c\right) d \mathbb{P}\left(X_C \mid X_S=z_S\right) d\right) d z_S-\mathrm{constant}
\end{aligned}
$$

We can estimate these values

$$\hat{\tilde{f}}_{j, A L E}(x)=\sum_{k=1}^{k_j(x)} \frac{1}{n_j(k)} \sum_{i: x_j^{(i)} \in N_j(k)}\left[\hat{f}\left(z_{k, j}, x_{-j}^{(i)}\right)-\hat{f}\left(z_{k-1, j}, x_{-j}^{(i)}\right)\right]$$
$$\hat{f}_{j, A L E}(x)=\hat{\tilde{f}}_{j, A L E}(x)-\frac{1}{n} \sum_{i=1}^n \hat{\tilde{f}}_{j, A L E}\left(x_j^{(i)}\right)$$

For [[Feature Interaction]] we can use a [[Heatmap]] again.

![[Bildschirmfoto 2023-07-11 um 11.19.04.png]]

Compare this to the [[Partial Dependence Plot]] which is not able to capture the interactions.

![[Bildschirmfoto 2023-07-11 um 11.19.42.png]]

To get the total effect it makes sense to look at the [[Partial Dependence Plot|PDP]], for ALE you have to calculate the total effect from the interaction and the individual effects.

> [!Check]+ Pros
>
> - unbiased
> - faster to compute
> - clear interpretation
> - centered at zero
> - feature interactions

> [!Warning]+ Cons
>
> - interpretation of effect across intervals is not possible
> - can become shakey (how big should intervals be)
> - not [[Individual Conditional Expectation Curve|ICE]]
> - implementation is complex
> - feature interaction heatmap hard to interpret
> - still not working for strong [[Korrelation|Correlations]]
