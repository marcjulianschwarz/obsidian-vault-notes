---
uni-module: "KDD"
---

# Min-Max Normalization

Scales values to some interval $[max,min]$:

$$a_{\text {new }}=\frac{a-\min _{A}}{\max _{A}-\min _{A}}(\max -\min )+\min$$

This has the advantage that all values lie in a defined interval which might be important for certain tasks. For example Deep Learning Models need the data to be between 0 and 1.
