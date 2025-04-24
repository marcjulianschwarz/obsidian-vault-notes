---
uni-module: AI
---
# Variable Elimination

A [[Bayesian Network]] Inference [[Algorithmus|algorithm]] that avoids 
- repeated computation 
- irrelevant computation 
	- Hidden variables in the form of leave nodes can be dropped as they will be equal to $1$ via [[Satz von der totalen Wahrscheinlichkeit|Marginalization]].


On [[Polytree|Polytrees]] it can even run in [[Polynomial Time 1]] which is quite a lot faster than the exact [[Inference]]. 
For non-polytrees however it is \#P-hard which is harder than [[Nondeterministic Polynomial Time|NP]]. For these cases one can use various sampling techniques to get approximations that are mostly good enough but way faster.

