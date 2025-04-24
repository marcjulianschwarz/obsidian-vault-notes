# Bayesian Classifier

The Bayesian Classifier is a *statistical classifier* which means that it calculates class-membership probabilities based on training data similar to the [[Logistic Regression]].

The whole algorithm is based on the [[Satz von Bayes|Bayes Theorem]] and [[Bayes Formel|Bayes Formula]].


> [!Check] Pros
> - It has equal performance compared to [[Decision Tree|Decision Trees]] and some [[Neural Network]] Classifiers.
> - Each training example can incrementally increase or decrease the probability of class membership. This allows for [[Online Learning]].

> [!Warning]+ Cons
> - requires calculation of many probabilities
> - which can be computationally expensive 

## Algorithm 

There are several important probabilities that the classifier has to calculate to determine a [[Sample|samples]] class.

The [[Posterior Probability]] can be calculated with the [[Prior Probability]], [[Likelihood]] and [[Evidence]].

Now some sample $X$ belongs to class $C_{i}$ if the corresponding [[Posterior Probability]] is the highest amongst all other posterios for all other classes.

To make computations easier one can assume that all attributes are [[stochastisch unabhängig|independent]] which leads to the [[Naive Bayes Classifier]].


- Class Conditional Modeling / Generative Modeling: $P(y)$ and $P(x|y)$ 
- Decision Boundary / Discriminative Modeling: $P(y|x)$

### Optimality 

The loss for two classes:
$$\begin{equation}
I\left(y_{1}, y_{2}\right)= \begin{cases}0 & , \text { if } y_{1}=y_{2} \\ 1 & , \text { otherwise }\end{cases}
\end{equation}$$

Average loss:
$$\begin{equation}
\mathrm{AL}(\boldsymbol{x}, y)=\sum_{y^{\prime}} I\left(y, y^{\prime}\right) p\left(y^{\prime} \mid \boldsymbol{x}\right)
\end{equation}$$

