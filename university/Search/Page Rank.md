---
uni-module: AI
---
# Page Rank

Googles way of ranking websites based on the amount of important links to it. 

$$\mathrm{PR}(\boldsymbol{A})=1-\boldsymbol{d}+\boldsymbol{d}\left(\frac{\mathrm{PR}\left(S_1\right)}{C\left(S_1\right)}+\cdots+\frac{\mathrm{PR}\left(S_n\right)}{C\left(S_n\right)}\right)$$
where $C(W)$ is the number of links in a page $W$, $S_i$ are pages that link to page $A$ and $d=0.85$.

**Intuition**
$\operatorname{PR}(A)$ is the probability of reaching page $A$ by random browsing.