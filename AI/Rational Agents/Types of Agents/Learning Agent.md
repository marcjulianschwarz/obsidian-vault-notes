---
uni-module: "AI"
---

# Learning Agent

A [[Learning Agent]] is the most general form of an [[Rational Agent|Agent]] as it can be reduced to

- [[Simple Reflex Agent]]
- [[Model-based Reflex Agent]]
- [[Goal-based Agent]]
- or [[Utility-based Agent]]

It even uses these types of agents as a **performance element** which can improve the learning element.

It has a problem generator which suggests actions that are then rated by the performance element. It will then either run the ations or use some kind of feedback to change the learning element.

Another **external** performance standard can improve the learning element via critic.

## Schema

![[Bildschirm­foto 2022-12-07 um 18.51.21.png]]

## Example (Taxi Agent)

- Performance Element → controls the actual driving
- Critic → external information (e.g. from passengers)
- Learning Element → modifies Performance Element according to critic
- Problem Generator → experiments different actions
