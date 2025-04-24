# Embedding Observations into Higher Dimensional Spaces 

This is kind of the opposite of [[Modeling Dynamical Systems on Manifolds]]. We try to embed the observations into a higher dimensional space sucht that the learning improves by utilizing more output-target comparisons. 

This means we use a randomly chosen and frozen matrix $E$ with [[Gleichverteilung|Uniformly Distributed]] values 
$$E_{i j} \in\left[-\frac{3}{\sqrt{\operatorname{dim}(y)}},+\frac{3}{\sqrt{\operatorname{dim}(y)}}\right]$$
to embed the original values in a high dimensional space and we learn a matrix $F$ to transform back to the original values. 
The values for $E$ should lie in the above interval to be in a reasonable range of the $tanh$ function. 

![[Bildschirm­foto 2023-06-08 um 13.21.59.png]]
