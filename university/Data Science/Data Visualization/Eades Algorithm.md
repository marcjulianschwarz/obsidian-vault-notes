---
uni-module: "InfoVis"
---

# Eades Algorithm

Force acting on a node:
$$\mathbf{f}_a=c_1 \log \frac{d}{c_2} \hat{\mathbf{r}} \quad \mathbf{f}_r=\frac{c_3}{d^2} \hat{\mathbf{r}}$$

- $\hat{r}$ unit vector pointing to the interacting node
- $d$ distance between the nodes
- $c_1$, $c_2$, $c_3$ constants set by the user
- $f_a$ force of attraction between adjacent nodes
- $f_r$ repulsion force between all pairs of nodes
- initial layout is random
- update layout iteratively
- stop when changes are small
