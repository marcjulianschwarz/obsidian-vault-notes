---
alias: "MSE"
---
# Mean Squared Error

It computes the difference between our predicted values and the true values. By squaring the difference we remove any signs and give big values more weight than small values. In the end the [[Arithmetic Mean|mean]] of all differences will be calculated.
$$L(\hat{y},y) = \frac{1}{n}\sum_{i=1}^{n}(\hat{y_i} - y_i)^2$$

This can often lead to [[Outlier]] Learning where the model tries to adjust the weights in a way to *please* the outliers. In the generalization set this might lead to higher instability.
Thus one can use the following approximation instead which only rises linearly:

![[CleanShot 2023-12-13 at 17.46.51@2x.png]]