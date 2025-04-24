---
uni-module: "MBNN"
---

# Homotopy for PTF

We can test for different [[Partial Teacher Forcing|PTF]] probabilities by increasing them over time for each learning step. We can see, that the results are getting better but after extended [[Dropout]] it doesnt help anymore.

**Phase 1**:
No [[Dropout]], so full [[Architectural Teacher Forcing]] will learn the history to very small error.

**Phase 2**:
Increase Dropout probabilty by tiny factor and continue lerning.

Maximum dropout should be 30%.
