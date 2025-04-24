---
uni-module: "KDD"

alias: "C4.5"
---

# Gain Ratio

Extension to [[Information Gain]] which applies [[Normalization]] to it.

$$
\begin{array}{r}
\text { Splitlnfo }_{A}(D)=-\sum_{j=1}^{v} \frac{\left|D_{j}\right|}{|D|} \log _{2}\left(\frac{\left|D_{j}\right|}{|D|}\right) \\
\text { GainRatio }(A)=\frac{\operatorname{Gain}(A)}{\text { Splitlnfo }_{A}(D)}
\end{array}
$$

Select attribute with the highest gain ratio.

## Disadvantages

- becomes unstable when Splitlnfo apporaches zero → use [[Information Gain]] in that case
- tends to prefer unbalanced splits (one is much smaller than the others)
