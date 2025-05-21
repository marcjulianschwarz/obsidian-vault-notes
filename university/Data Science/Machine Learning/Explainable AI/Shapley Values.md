---
uni-module: "XAI"
---

# Shapley Values

Game-theoretic method assigning contribution of individual players in achieving a certain payout.

> [!NOTE] Definition
> The average marginal contribution of a feature value across all possible [[Coalition|Feature Subsets]].

$$\operatorname{val}x(S) = \int \hat{f}(x_1, \ldots, x_p) , d \mathbb{P}{x \notin S} - E_X(\hat{f}(X))$$

$$
\operatorname{val}x(S) = \int \hat{f}(x_1, \ldots, x_p) , d
\mathbb{P}{x \notin S}
$$

#todo add all math here

[[Shapley Additive Explanations]]

Efficiency

- shapley values add up to prediction difference to average prediction

Symmetry

- equal shapley value ←→ equal contributions in all [[Coalition|coalitions]]

Dummy

- feature that doesnt change prediction must have value of zero

Additivity

- linear operation

## Pseudocode

```
featureA = "temp"
X_local = ... # local datapoint

shapley_value = 0.0
for _ in range(N):
		feature_subset = random_subset_that_contains(featureA)
		for _ in range(1_000):
			X = X_local.copy()
			X[not feature_subset] = random_feature(not feature_subset)
			X_withoutA = X.copy()
			X_withoutA[featureA] = random_feature(featureA)

			shapley_value += prefactor(feature_subset)*(f(X) – f(X_withoutA))
	shapley_value = shapley_value / (N*1_000)

```

> [!Check]+ Pros
>
> - [[Model-Agnostic]]
> - "Fair payout" properties
> - solid theory

> [!Warning]+ Cons
>
> - only approximations feasible
> - not [[Selectivity|selective]], explanations always contain all features
> - access to training data needed
> - unrealistic datapoints if data is correlated because of random marginalization of features

## References

https://www.youtube.com/watch?v=oCIybnawLdg
