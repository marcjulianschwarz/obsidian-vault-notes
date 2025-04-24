---
uni-module: "AI"
---

# Table-Driven Agent

The idea for a table-driven [[Rational Agent|Agent]] would be to implement the [[Agent Function]] as a table where you can look up actions.

The [[Agent Program]] would look like this:

```js
function Table−Driven−Agent(percept) returns an action
	persistent table //a table of actions indexed by percept sequences
	var percepts  //a sequence, initially empty
	append percept to the end of percepts
	action := lookup(percepts, table)
return action
```

> [!WARNING] Problem
> A problem that can arise is that the table can get much too large. So even for $n$ binary [[Percept|percepts]] we would have $2^n$ rows in the table.
>
> How can we create this huge table?
>
> Not really intelligent anyways...
