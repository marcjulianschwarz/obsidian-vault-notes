---
uni-module: "AI"

alias: ["Logische Folgerung", "Logische Konsequenz"]
---

# Entailment

**Informal:**
Which formulas $B$ are true when $A$ is true?

**Formal:**
For all [[Variable Assignment|Assignments]] $\varphi$ which satisfy $A$, do these assignments also satisfy $B$ ?

$A$ entails/models $B$:
$$A \models B$$

> Entailment is the ideal outcome of reasoning.

[[Deduction]] is the process of an actual computer trying to reason about entailment.

$$A \models B \Longleftrightarrow(A \cup\{\neg B\}) \models \perp .$$

## Examples

[[Modus Ponens]]
