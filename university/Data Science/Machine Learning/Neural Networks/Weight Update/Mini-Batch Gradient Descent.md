# Mini-Batch Gradient Descent

A widely used [[Gradient Descent]] algorithm that is [[Stochastic Gradient Descent|SGD]] on batches. Instead of updating weights for every individual sample we create batches and accumulate all [[Gradient|Gradients]] in a batch before doing the weight update.

This will result in some more speedup and smooths some of the stochasticity that is introduced by SGD.

The update rule is 
$$\Delta w=-\eta\left(\frac{1}{\text { batch }} \sum_{t=1}^{\text {batch }} g_t\right)$$where $1\leq\text{batch}\leq\text{\#data}$ is the batch size. 




