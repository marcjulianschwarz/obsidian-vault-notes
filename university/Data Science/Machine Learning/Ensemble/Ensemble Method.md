---
uni-module: "KDD"

alias: "Ensemble"
---
# Ensemble Method

Several weak learners which were all trained on their own partition of a dataset to create predictions by **majority voting**.
This will in most cases lead to better results than any of the individual learners could achieve.

Popular methods are:

- [[Bagging]]
- [[Boosting]]
- [[Random Forest]]

Random initializations of overparameterized models lead to non-unique solutions (echo of random initialization). This can be seen when evaluating multiple models on the same data. On the generalisation data we can observe quite diverse predictions.


## Proof of Decreasing Model Uncertainity by Averaging
$$\begin{aligned}
E_{\text {aver }} & =\frac{1}{T} \sum_{t=1}^T\left[\text { out }_{\text {aver }, t}-\text { tar }_t\right]^2 \\
& =\frac{1}{T} \sum_{t=1}^T\left[\left(\frac{1}{m} \sum_{i=1}^m \text { out }_{i, t}\right)-\text { tar }_t\right]^2 \\
& =\frac{1}{T} \sum_{t=1}^T\left[\frac{1}{m} \sum_{i=1}^m\left(\text { out }_{i, t}-\text { tar }_t\right)\right]^2 \\
& \stackrel{!}{=} \frac{1}{m^2} \frac{1}{T} \sum_{t=1}^T \sum_{i=1}^m\left(\text { out }_{i, t}-\text { tar }_t\right)^2 \\
& =\frac{1}{m} \frac{1}{m} \sum_{i=1}^m \frac{1}{T} \sum_{t=1}^T\left(\text { out }_{i, t}-\text { tar }_t\right)^2 \\
& =\frac{1}{m} \operatorname{aver}\left(E_i\right)
\end{aligned}$$

## But

Even in [[Ensemble Method|Ensemble]] models we can not model the stochasticity as it is not a feature of the real world. Instead, we see stochasticity because of the partial observability of the world. If we could fully observe it, we could predict down to zero error. 


