---
uni-module: "XAI"

alias: "ICE"
---

# Individual Conditional Expectation Curve

Just like the [[Partial Dependence Plot]] but without averaging over the entire dataset. This allows you to see _heterogenous_ effects in the data.
It yields a family of [[Local Explanation|local explanations]]. By aligning them vertically at some value we can get somewhat [[Global Explanation|global explanations]].

![[Bildschirmfoto 2023-07-12 um 14.37.46.png]]

Vertical Alignment and Average:
![[Bildschirmfoto 2023-07-27 um 20.20.43.png]]
