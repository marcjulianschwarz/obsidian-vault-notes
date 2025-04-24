---
uni-module: "KDD"
---

# Outlier Detection with Non-Parametric Statistical Method

These methods dont make as many assumptions about the dat as [[Outlier Detection with Parametric Statistical Method]] and thus are applicable in more scenarios.

Use a [[Histogram]] to check if objects are [[Outlier|Outliers]]. A problem with this method is choosing the correct bin size for the histogram. If the bin size is too small some normal objects might be treated as outliers ([[False Positive]]) and if the bin size is too big some outliers might fall in a frequent bin ([[False Negative]]).

Alternative to histogram is the [[Kernel Density Estimation]].
