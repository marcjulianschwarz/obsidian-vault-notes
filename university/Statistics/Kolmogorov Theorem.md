---
uni-module:
  - AI
---

# Kolmogorov Theorem

$$P(\top)=1$$
$$P(a\lor b)=P(a)+P(b)-P(a\land b)$$

## Example 

Assume 
$$P(\bot)=0$$
Derive 
$$P(\neg a)=1-P(a)$$

**Step 1**
$$P(\top)=1$$
$$(a \vee \neg a) \Leftrightarrow \top $$
$$P(a \vee \neg a)=1$$
**Step 2**

$$P(\perp)=0$$
$$(a \wedge \neg a) \Leftrightarrow \perp $$
$$P(a \wedge \neg a)=0 $$
**Step 3**
$$P(a \vee \neg a)=1=P(a)+P(\neg a)-0 .$$

## Belifing in Kolmogorov

1. You’re free to believe whatever you want, but note this [DF31]: If an agent has a belief that violates Kolmogorov’s axioms, then there exists a combination of “bets” on propositions so that the agent always looses money.
2. If your beliefs are contradictory, then you will not be successful in the long run (and even the next minute if your opponent is clever).

