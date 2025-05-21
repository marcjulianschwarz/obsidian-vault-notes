# Optimization of a Linear Model

The model parameters are $\phi = \set{w_0, ..., w_n, \sigma}$. These are all weights and a sigma for the Gaussian distribution.


Then we do a [[Maximum Likelihood Estimation]].

$$\begin{equation}
\boldsymbol{\theta}^{*}=\underset{\boldsymbol{\theta}}{\operatorname{argmax}} p(\mathcal{D} \mid \boldsymbol{\theta})
\end{equation}$$

For this we will use the Likelihood function:
$$p(\mathcal{D} \mid \boldsymbol{\theta})$$
It's the product of all dastapoints where each datapoint is first evaluated with the Gauss Distribution and the weight, error parameters.
We want to maximize this function because values very near to function (high value in the Gaussian distribution) is better than values far away from the function (Low value in the Gaussian distribution).

→ [[Log-Likelihood]]



## Analytical Solution
For the analytical solution we convert the [[Log-Likelihood]] in the way simpler form of the Negative-Log-Likelihood (NLL):
$$\begin{equation}
\operatorname{NLL}(\boldsymbol{\theta})=\frac{1}{\mathbf{2}}(\mathbf{y}-\mathbf{x} \mathbf{w})^{\mathbf{T}}(\mathbf{y}-\mathbf{x} \mathbf{w})
\end{equation}$$

To find the minimum, we calculate the derivative and equate it to zero to get the extrem values (in this case the minimum).
$$x^Txw=x^Ty$$

In practice, this approach is too time consuming, especially with a lot of data.

[[Quality of the fit]]