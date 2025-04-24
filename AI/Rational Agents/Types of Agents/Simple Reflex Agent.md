---
uni-module: "AI"
---

# Simple Reflex Agent

An [[Rational Agent|Agent]] that only bases its next [[Action|actions]] on the last [[Percept]] it perceived.

So the [[Agent Function]] simplifies from a history of percepts $\mathcal{P}^*$ to only one percept:
$$f_{a}:\mathcal{P}\to \mathcal{A}$$

An example of an [[Agent Program]] would be the reflex vacuum which cleans when there is dirt in front of it.

Basically a set of if else rules.

## General Agent Program

```
function Simple−Reflex−Agent (percept) returns an action
	persistent: rules /∗ a set of condition−action rules∗/

    state := Interpret−Input(percept)
    rule := Rule−Match(state,rules)
    action := Rule−action[rule]
    return action
```

## Schema

![[Bildschirm­foto 2022-12-07 um 18.21.50.png]]

> [!Warning]+ Cons
> 
> - [[Partially Observable Environment]] (faulty sensors) → infinite loops
> - Cant react to changes of the [[Environment]]
> 

## Further

→ [[Model-based Reflex Agent]]
