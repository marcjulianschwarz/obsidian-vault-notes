---
uni-module: "AI"

alias: "Reflex Agent with State"
---

# Model-based Reflex Agent

An [[Rational Agent|Agent]] (similar to [[Simple Reflex Agent]]) whose [[Agent Function]] depends on a _world model_ that consists of:

- A [[Belief State]] (this is the different part where we keep track of the state of the world instead of only looking at the last [[Percept]])
- A [[Sensor Model]]
- A [[Transition Model]]
  - maps states to actions
- an [[Agent Function]]
  - maps states to actions iteratively based on the sensor models output

## General Agent Program

```
function Model−Based−Agent (percept) returns an action
		var state /∗ a description of the current state of the world ∗/ persistent rules /∗ a set of condition−action rules ∗/
	var action /∗ the most recent action, initially none ∗/

	state := Update−State(state,action,percept)
	rule := Rule−Match(state,rules)
	action := Rule−action(rule)
	return action
```

## Schema

![[Bildschirm­foto 2022-12-07 um 18.37.38.png]]

## Problems

- does not always determine what to do (in a [[Rational Behavior|Rational]] way)

## Further

→ [[Goal-based Agent]]
