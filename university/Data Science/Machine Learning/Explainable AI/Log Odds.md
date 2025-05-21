---
uni-module: "XAI"

alias: ["Odds Ratio", "Logit"]
---

# Log Odds

The log odds is the logarithm applied to the [[Odds]].
$$f(p)=\operatorname{log}\left(\frac{p}{1-p}\right)$$
In a [[Logistic Regression]] we try to predict these log odds via a linear combination of the features (just like in [[Perceptron]] or [[Linear Regression]] we assume this linear relationship).
$$\log \left(\frac{P(y=1)}{1-P(y=1)}\right)=\log \left(\frac{P(y=1)}{P(y=0)}\right)=\beta_0+\beta_1 x_1+\ldots+\beta_p x_p$$

The [[Logistic Function|Sigmoid Function]] is the inverse function of the logit function, so we can get back the normal probability $p$.
$$\sigma (f(p))=p$$

## Explainability

Increasing a features value $x_j$ by one unit (this is happening in the numerator), the odds ratio changes by a factor of $e^{\beta_j}$.

$$\frac{o d d s_{x_j+1}}{o d d s}=\frac{\exp \left(\beta_0+\beta_1 x_1+\ldots+\beta_j\left(x_j+1\right)+\ldots+\beta_p x_p\right)}{\exp \left(\beta_0+\beta_1 x_1+\ldots+\beta_j x_j+\ldots+\beta_p x_p\right)}=\exp \left(\beta_j\left(x_j+1\right)-\beta_j x_j\right)=\exp \left(\beta_j\right)$$

We can rewrite this to
$$\text{odds}_{x_j+1}=\text{odds}\cdot e^{\beta_j}.$$
Which leads to the conclusion that the odds will increase multiplicative by the exponential of the weight of that feature.
