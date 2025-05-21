# Modeling Dynamical Systems on Manifolds

If we know that a dynamics stays on a [[Manifold]] we can reduce the dimensions down to that manifold. If we don't know anything about the problem we can use [[Autoencoder|Autoencoders]] to reduce the dimensions automatically.

So we try to learn two transformations $g$ and $g^{-1}$ based on our data and we can learn the dynamical system on the transformed data $g(x)$.

![[Bildschirm­foto 2023-06-08 um 13.15.36.png]]

We can then write 
$$y_t=g^{-1} \circ f \circ g\left(y_{t-1}\right)$$
for the high dimensional flow. 

We can now combine this [[Autoencoder]] approach with [[Error Correction Neural Network|ECNNs]]  or [[Historical Consistent Neural Network|HCNNs]] such that the network will learn the dynamics on a lower dimensional [[Manifold]] and the [[Autoencoder]] will transform the forecast back to the higher dimensional output. 

![[Bildschirm­foto 2023-06-08 um 13.18.39.png]]

