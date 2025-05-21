---
uni-module: MBNN
---
# Neural Network Weight Initialization


To get a good learning network we want to start approximating only in the linear parts of the [[Activation Function]] ([[Hyperbolic Tangent|tanh]]) and then slowly move towards the saturating ends to add nonlinearities into the mix. 

$$w_i \in\left(-\frac{3}{\sqrt{n}},+\frac{3}{\sqrt{n}}\right)$$
where $n$ is the number of weights.
## Proof 

We want to keep the weights relatively small with [[Arithmetic Mean|Mean]] around zero and [[Standardabweichung|Standard Deviation]] of one 
$$\tanh \left(\sigma\left(\sum_{i=1}^n w_i x_i\right) \stackrel{!}{=} 1\right)$$
We can easily calculate the [[Varianz|Variance]] and [[Standardabweichung|Standard Deviation]] of the weights with respect to the overall domain $(-r,+r)$.
$$\sigma^2(w)=\frac{1}{2 r} \int_{-r}^{+r}(w-0)^2 d w=\frac{r^2}{3} \Rightarrow \sigma\left(w_i\right)=\frac{r}{\sqrt{3}} \quad \& \quad \sigma\left(x_i\right)=\frac{1}{\sqrt{3}}$$
We then use the [[Starkes Gesetz der großen Zahlen|Strong Law of Large Numbers]] to calculate $r$ with 
$$\Rightarrow \quad \sigma\left(\sum_{i=1}^n w_i x_i\right) \stackrel{!}{=} \sqrt{n} \sigma\left(w_i x_i\right)=\sqrt{n} \frac{r}{3} \approx 1$$
and 
$$r=\frac{3}{\sqrt{n}}$$
We should thus choose values of $w$ in $(-r,+r)$ to get good learning.


## More Ressources

- [Initializing neural networks - deeplearning.ai](https://www.deeplearning.ai/ai-notes/initialization/index.html)
- [Don’t Trust PyTorch to Initialize Your Variables | Aditya Rana Blog](https://adityassrana.github.io/blog/theory/2020/08/26/Weight-Init.html)

