---
alias: "SVM"
---
# Support Vector Machine

Can be used both for [[Classification]] and [[Regression]] tasks. 


**Intuition**
Construct a [[Decision Boundary]] ([[Maximum Margin Separator]]) that has the largest possible distance to all of the example points. This property should make it the *best* boundary and thus generalize well. The so called [[Kernel Trick]] can be used to [[Embedding|embed]] the original data into a higher-dimensional space to make it linearly seperable. 

Also SVMs try to prioritize critical examples (near the decision boundary), called [[Support Vector]] which will lead to even better generalization.

In [[Logistic Regression]] we wanted to find a decision boundary that can seperate two classes which worked. But is it actually the **best** boundary?

Decision boundary of a margin 
$$\frac {2} {||w||}$$
$$w\cdot x - b = +1$$
$$w\cdot x - b = -1$$

The margin has to be maximized. → minimize $\frac{1}{2}  ||w||^2$
under the constraint 
$$y_i(w \cdot x_i - b) \geq 1$$
(which mean that all classes are correctly classified).

This looks like a [[Quadratisches Optimierungsproblem|quadratic optimization problem]] with some constraint. Thats why we can use [[Lagrange Multipliers for SVM optimization]].

When working with different bases we can apply the [[Kernel Trick]] to reduce unneccesary computations and therefore make our model more efficient.

→ [[Soft Margin]] 

## Regression 

We can use [[Support Vector Machine|SVMs]] for [[Regression]] tasks too. In a regression problem we want to keep all of our data points in a $\epsilon$-tube around a function.
We achieve this with the following two inequalities where we already added two slack variables for outliers:
$$\begin{equation}
\begin{aligned}
&y_{i} \leq\left(\boldsymbol{w} \cdot \boldsymbol{x}_{i}+b\right)+\epsilon+\xi_{i}^{+} \\
&y_{i} \geq\left(\boldsymbol{w} \cdot \boldsymbol{x}_{i}+b\right)-\epsilon-\xi_{i}^{-}
\end{aligned}
\end{equation}$$
We therefore have a new optimization problem where we want to minimize the following function:
$$\begin{equation}
\min _{w, b} \frac{1}{2}\|w\|^{2}+C \sum_{i=1}^{n}\left(\xi_{i}^{+}+\xi_{i}^{-}\right)
\end{equation}$$
under these constraints:
$$\begin{equation}
\begin{aligned}
&y_{i} \leq\left(\boldsymbol{w} \cdot \boldsymbol{x}_{i}+b\right)+\epsilon+\xi_{i}^{+} \\
&y_{i} \geq\left(\boldsymbol{w} \cdot \boldsymbol{x}_{i}+b\right)-\epsilon-\xi_{i}^{-} \\
&\xi_{i}^{+} \geq 0 \\
&\xi_{i}^{-} \geq 0
\end{aligned}
\end{equation}$$

## Pros and Cons 

> [!Check]+ Pros
> - less suspectible to [[Outlier|Outliers]] when compared to [[Logistic Regression]]
> - elegant to optimize since there is only one local and global optimum
> - efficiently scales to high-dimensional features because of [[Sparsity]] and the [[Kernel Trick]]
> - works with nonlinear problems via [[Soft Margin]]
> 

> [!Warning]+ Cons
> 
> - the parameters $\epsilon$ and $C$ have to be tuned very carefully
> - doesnt scale to large data sets

## Code 

#todo implement this, will probably lead to some better understanding.