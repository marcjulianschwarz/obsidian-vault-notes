---
uni-module: "KDD"
---

# IF-THEN Rules for Classification

Represents knowledge of data in the form of _IF-THEN_ rules.

These rules are more readable and easier to understand than large [[Decision Tree|Decision Trees]].

## Problems

More than one rule is triggered.

- Size ordering → highest priority for toughest rule
- Class-based ordering →
- Rule-based ordering (decision list) → rules have to be applied in this particular order to avoid conflicts. Order can be established by some measure of quality or by experts

No rule is triggered.

- Fallback rule which will always be evaluated as the last rule
