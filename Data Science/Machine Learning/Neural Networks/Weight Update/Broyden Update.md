---
uni-module: MBNN
---
# Broyden Update

A method to iteratively approximate the inverse of the [[Jacobi Matrix|Jacobian Matrix]] $W$ or linear transformations of the form
$$y=Wx.$$

The update rule is
$$W_{+}=W+\frac{\left(y_t-W x_t\right) x_t^T}{x_t^T x_t}$$

The approach works even if the data are incomplete vectors. However it can not identify unobserved hidden variables.

For linear functions the broyden update is equivalent to the normal [[Backpropagation]] algorithm. We can rewrite the update in the following way 
$$W_{+}=W+\frac{\left(y_t-W x_t\right) x_t^T}{x_t^T x_t}=W-\frac{\left(W x_t-y_t\right) x_t^T}{x_t^T x_t} \approx W+\eta \cdot\left(\text { output }_{\mathrm{t}}-\text { target }_t\right) * x_t^T$$
The right part of the equation is just the [[Gradient]] update calculated with [[Backpropagation]] for the linear transformation.


![[CleanShot 2023-11-18 at 22.52.04@2x.png]]