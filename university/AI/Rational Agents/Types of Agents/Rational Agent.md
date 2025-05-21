---
uni-module: "AI"

alias: "Agent"
---

# Rational Agent

An agent is an entity that **perceives** an [[Environment]] via sensors and **acts** on it with actuators (changing the [[Environment]]).
We assume that agents can always perceive their own actions but maybe not the consequences of the actions.

A rational agent is not perfect as it only optimizes the **expectation**. If the agent does not know everything it cant optimize the actual [[Performance Measure]]. A rational agent might not perceive everything, thus **exploration** (learning, autonomy) might be needed in order to find hidden _dangers_. A rational agent might not be **successfull** as action outcomes may not be as expected (very unlikely events can still happen) → still take actions to learn.


> [!NOTE] Summary of why a rational agent is not perfect
>
> - rational is not omiscient
> - rational is not clairvoyant (hellseherisch)
> - rational is not successfull

A rational agent exhibits [[Rational Behavior]] for any given class of [[Environment|environments]] and tasks.
Want to find the optimal/best rational agent.

[[Autonomy]]

[[Percept]]
[[Action]]
[[Agent Function]], [[Agent Program]], [[Agent Architecture]]
[[Performance Measure]]

[[PEAS]]

## For example:

- humans
- robots
- softbots
- thermostats

## Example: Vacuum-Cleaner World and Agent

Science Question: What is the [[Agent Function]]?
AI Question: What is the [[Agent Program]] and [[Agent Architecture]]?

[[Agent Program]] for a vacuum cleaner might look like this:

```
procedure Reflex−Vacuum−Agent [location,status] returns an action
	if status = Dirty then return Suck
	else if location = A then return Right
	else if location = B then return Left
```

Basically [[Table-Driven Agent]]
