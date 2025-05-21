---
uni-module: MBNN
---
# Silva Almeida's Rule 


$$\begin{aligned}
W_{+} & =W+\alpha\left(W-[Y][Z]^T\right) \\
& =W+\alpha\left(W-[W X]\left[W^T[W X]\right]^T\right) \\
& =W+\alpha\left(W-W X X^T W^T W\right) \\
& =W+\alpha\left(I d-W X X^T W^T\right) W \\
& =W+\alpha\left(I d-(W X)(W X)^T\right) W \\
& =W+\alpha\left(I d-Y Y^T\right) W
\end{aligned}$$