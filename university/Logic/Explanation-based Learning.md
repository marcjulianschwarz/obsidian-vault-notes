---
uni-module: AI
aliases:
  - EBL
---
# Explanation-based Learning

$$\begin{aligned}
\text { Hypothesis } \wedge \text { Descriptions } & \models \text { Classifications } \\
\text { Background } & \models \text { Hypothesis }
\end{aligned}$$

**Intuition**
Extracting general rules from individual observations.
Converting first-principles theories into useful, special purpose knowledge. 

We can for example have a [[Knowledge Base (Prolog)]] with some [[First-Order Predicate Logic]] formulas. Then based on observations we can generate proof trees with the rules from the knowledge base. Such a tree can then be generalized by replacing any values with variables instead and creating a [[Konjunktion|Conjunction]] over all leaves. 

So the general process looks like this
- Use background knowledge to construct a proof for the example.
- In parallel, construct a generalized proof tree.  
- New rule is the conjunction of the leaves of the proof tree and the variabilized goal. 
- Drop conditions that are true regardless of the variables in the goal.

#todo complexity stuff 

We use [[Memoization]].

