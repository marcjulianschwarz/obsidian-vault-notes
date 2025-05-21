---
uni-module: "LNS"
---

# Hessematrix

Die Hessematrix ist die Verallgemeinerung des [[Gradient|Gradienten]] und sieht entsprechend so aus:

$$
\nabla^{2} f(x)=\left(\begin{array}{cccc}
\frac{d^{2} f}{d x_{1} d x_{1}}(x) & \frac{d^{2} f}{d x_{1} d x_{2}}(x) & \cdots & \frac{d^{2} f}{d x_{1} d x_{n}} \\
\frac{d^{2} f}{d x_{2} d x_{1}}(x) & \frac{d^{2} f}{d x_{2} d x_{2}}(x) & \cdots & \vdots \\
\vdots & \vdots & \ddots & \\
\frac{d^{2} f}{d x_{n} d x_{1}}(x) & \cdots & \cdots & \frac{d^{2} f}{d x_{n} d x_{n}}(x)
\end{array}\right)
$$

Die Hessematrix ist symmetrisch.

$f$ muss entsprechend [[Stetigkeit|stetig]] und zweimal differenzierbar sein.
