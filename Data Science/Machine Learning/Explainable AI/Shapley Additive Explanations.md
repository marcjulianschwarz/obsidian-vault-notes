---
uni-module: "XAI"

alias: "SHAP"
---

# Shapley Additive Explanations

A more efficient way to approximate [[Shapley Values]].

- [[KernelSHAP]]
- [[TreeSHAP]]

## Global SHAP

Run SHAP for every instance and obtain a matrix of shapley values.

SHAP Feature Importance, average over all shapley values (for each instance) for a given feature.
$$I_j=\frac{1}{n} \sum_{i=1}^n\left|\phi_j^{(i)}\right|$$
So we get the average contribution on model output of a feature.

> [!Check]+ Pros
>
> - all [[Shapley Values]] properties
> - [[Model-Agnostic]]
> - "Fair payout" properties
> - solid theory
> - faster approximation with [[KernelSHAP]]
> - even faster non [[Model-Agnostic]] version with [[TreeSHAP]]
> - faster computation enables global interpretations

> [!Warning]+ Cons
>
> - all [[Shapley Values]] properties
> - not [[Selectivity|selective]]
> - training data access needed
> - predictions on unrealistic datapoints if data is correlated
> - [[KernelSHAP]] still slow
> - [[KernelSHAP]] ignores dependence between subsets of included and absent features

## References

https://www.youtube.com/watch?v=VB9uV-x0gtg
