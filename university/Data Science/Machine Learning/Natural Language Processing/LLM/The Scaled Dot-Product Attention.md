
# The Scaled Dot-Product Attention

A form of [[Attention]] that uses the scaled dot product as [[Similarity]] function. 
$$\operatorname{Attention}(Q, K, V)=\operatorname{softmax}\left(\frac{Q K^T}{\sqrt{d_k}}\right) V$$
The inputs to the attention function are queries $q$, keys $k$ and values $v$. Each query, key and value is just a vector of numbers (e.g. the [[Word Embedding]] coming from the input).
The query and key have the same dimensions
$$q,k\in \mathbb{R}^{d_k}$$
and 
$$v\in \mathbb{R}^{d_v}.$$

**Intuition**
We compare all keys with the current query via some kind of [[Similarity]] function (in this case the scaled dot product). This will produce a mask that we can apply to all values. 

In practice, one puts all queries, key and values in matrices $Q, K$ and $V$ to use efficient matrix multiplication. The calculated mask will be normalized with $\sqrt{d_k}$ to make sure that not too much information is lost with the [[Softmax]] function. In the end we use the mask to attend to values in $V$.



![[Scaled Dot-Product Attention.canvas]]