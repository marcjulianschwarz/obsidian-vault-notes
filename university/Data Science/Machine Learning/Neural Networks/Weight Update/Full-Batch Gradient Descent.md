# Full-Batch Gradient Descent

A [[Gradient Descent]] algorithm that uses the entire dataset to calculate one weight update. 
The update is 
$$\Delta w=\eta \cdot(-g)$$
with 
$$g_t=\frac{\partial E_t}{\partial w}, g=\frac{1}{T} \sum_{t=1}^T g_t.$$

As you can see this can become computationally expensive when the size of the data set grows. For each update we would need to calculate all [[Gradient|Gradients]].

Faster methods are [[Mini-Batch Gradient Descent]] or [[Stochastic Gradient Descent]] which both do more frequent weight updates instead.


## Proof 

With [[Taylor-Approximation|Taylor Expansion]] we can show 
$$\begin{aligned}
E(w+\Delta w) & =E(w)+g^T \Delta w+\frac{1}{2} \Delta w^T G \Delta w \\
& =E(w)-\eta g^T g+\frac{\eta^2}{2} g^T G g<E(w) \quad \text { for } \eta \text { small }
\end{aligned}$$
So, the error decreases with every weight update.



