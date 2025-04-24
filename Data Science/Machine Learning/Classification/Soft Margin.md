# Soft Margin

Used in [[Logistic Regression]] to work with [[Classification]] data that is not linearly seperable (compare to [[Hard Margin]]).

To solve this problem we introduce a slack variable $\xi _i$ which is the distance required to correctly classify a wrongly classified data point.
If a data point is wrongly classified we just move it by:
$$\begin{equation}
\xi_{i}=1-y_{i}\left(\boldsymbol{w} \cdot \boldsymbol{x}_{i}-b\right)
\end{equation}$$

We can now update our optimization problem from before with our slack variable:

$$\begin{equation}
\begin{gathered}
\min _{\boldsymbol{w}, b, \xi} \frac{1}{2}\|\boldsymbol{w}\|^{2}+\lambda \frac{1}{n} \sum_{i=1}^{n} \xi_{i} \\
\text { s.t. } y_{i}\left(\boldsymbol{w} \cdot \boldsymbol{x}_{i}-b\right) \geq 1-\xi_{i}
\end{gathered}
\end{equation}$$