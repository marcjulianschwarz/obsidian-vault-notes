# Cross Entropy

In a classification task, the end results of a DNN will be a set of a lot of 0s and one 1 which One Hot encodes the class.
To ensure that we have propabilities (ranging from 0 to 1), we apply a softmax transformation.
$$\bar{y_i} = \frac{\exp{\hat{y_i}}}{\sum_{j=1}^{n}\exp{\hat{y_j}}}$$

Now, the values represent a class probability. To avoid very small numbers, we take the negative log of the result.

$$-\log{\bar{y_i}}$$


In a [[Logistic Regression]] task we also use cross entropy. In this case we construct the loss with the [[Log-Likelihood]]. 

$$\begin{equation}
\begin{aligned}
\boldsymbol{\ell}(\boldsymbol{\theta}) &=\sum_{i=1}^{N} \log \left[p\left(\mathrm{y}_{i} \mid \mathbf{x}_{i}, \boldsymbol{\theta}\right)\right] \\
& \stackrel{\star}{=} \sum_{i=1}^{N} \log \left(\mu\left(\mathbf{x}_{i}, \mathbf{w}\right)^{y_{i}}\left(1-\mu\left(\mathbf{x}_{i}, \mathbf{w}\right)\right)^{1-y_{i}}\right)
\end{aligned}
\end{equation}$$

$$\begin{equation}=
\sum_{i=1}^{N} y_{i} \log \left(\mu\left(\mathbf{x}_{i}, \mathbf{w}\right)\right)+\left(1-y_{i}\right) \log \left(1-\mu\left(\mathbf{x}_{i}, \mathbf{w}\right)\right)
\end{equation}$$

Now we have to minimize the negative log-likelihood and we have Cross Entropy.
This has a unique minimum but no analytical solution is possible. That is why we use [[Gradient Descent]] to get to the minimum.