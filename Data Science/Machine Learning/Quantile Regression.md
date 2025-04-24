# Quantile Regression 

Can be used to give [[Perzentil|Quantile]] bounds for a [[Regression]] task. For example upper and lower bounds for the predicted value. 

Uses a different [[Loss Function]]:

$$
L=\left\{\begin{array}{l}
\tau(y-X \theta), \text { if } y-X \theta \geq 0 \\
(\tau-1)(y-X \theta), \text { if } y-X \theta<0
\end{array}\right.
$$

The parameter $\tau$ ist the [[Perzentil|Quantile]].

You have to train a model for each quantile that you want to obtain values for.

When the predicted values are smaller than the true values, you get a positive loss which is being penalized by the parameter $\tau$.
When the predicted values are bigger than the true values, you get a negative loss which is being penalized by the inverse quantile.

You can use a [[Custom Loss Function for Linear Regression in Python]] to implement this in [[Python]].


## Example:

![[Bildschirm­foto 2023-03-28 um 20.57.31.png]]

## Ressources 

- For non-linear [[Regression]]
	- http://ethen8181.github.io/machine-learning/ab_tests/quantile_regression/quantile_regression.html 
