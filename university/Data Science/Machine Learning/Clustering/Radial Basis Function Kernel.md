---
alias: "RBF"
---
# Radial Basis Function Kernel

Analyses the similarity of data points (more or less [[Clustering]]).

**Pros**
- most popular kernel
- useful when data is arranged in clusters

**Cons**
- only good in low-dimensional spaces 
$$\frac{v_r^n}{v_1^n}=\frac{c \cdot r^n}{c \cdot 1^n}=r^n \underset{r<1}{\rightarrow} 0$$


Roughly, a [[Similarity]] function between a pair of examples, via the minus sign. Uses exponential function to map values between 1 (similar) and 0 ([[Dissimilarity|dissimilar]]).

$$
\kappa\left(x^{(i)}, x^{(j)}\right)=\exp \left(-\frac{\left\|x^{(i)}-x^{(j)}\right\|^2}{2 \sigma^2}\right)
$$

or simplified to 

$$
\kappa\left(x^{(i)}, x^{(j)}\right)=\exp \left(-\gamma\left\|x^{(i)}-x^{(j)}\right\|^2\right).
$$

Here 
$$\gamma=\frac{1}{2\sigma^2}$$ is a free parameter that can be optimized and set in the scikit learn model. You can control the tightness of the fit with this parameter which of course also affects [[Overfitting]] and [[Underfitting]] of the model. 

**Low Gamma Value**

![[gamma_low.png]]


**High Gamma Value**

![[gamma_high.png]]