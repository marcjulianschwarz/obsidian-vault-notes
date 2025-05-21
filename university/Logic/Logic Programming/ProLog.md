---
uni-module: "AI"
---

# ProLog

A programming language that uses logic and control to do computations.

Its main idea is that you describe the whole world with a [[Knowledge Base (Prolog)]] and then ask questions about that world.

The [[Backchaining]] process uses a [[Depth-first search]] approach to query a [[Knowledge Base (Prolog)]]. If this process fails at any given point, it will backtrack to the last backtracking point that was set earlier.

This can easily result in infinite loops, which is ok, as this makes [[ProLog]] [[Turing Test|turing complete]].

## Syntax
- constants → lower-case strings
- variables → upper-case strings (or starting with \_)
- functions and predicates → applied to terms

A term is a

- variable
- constant
- function applied to terms

A literal is a

- constant
- predicate applied to terms

A ProLog program is a sequence of clauses

- facts of the form $I.$ where $I$ is a literal
- rules of the form $h:-b_{1},\dots,b_{n}$ where $h$ is called a **head literal** and the $b_{i}$ are called the body of the rule
  - $h$ is true if all $b_{i}$ are true

Facts and rules make up a [[Knowledge Base (Prolog)]] which can be queried. As the [[Knowledge Base (Prolog)]] is usually quite big and can even be infinite, logic programming languages only compute fragments of the base by need. This is done in a [[Depth-first search]] process.
Such a query can either return true/false when doing [[Backchaining]] or return a value when doing Answer Substitution where for all queriy variables the process accumulates the values by repeated Backchaining.

- and → `,`
- or → `;`


As there are no functions in [[ProLog]], we use a three-place predicate where the first two places are parameters and the last one is the output of the function.
This way we can define addition, multiplication and exponentiation:

```prolog
add(X, zero, X).
add(X, s(Y), s(Z)) :- add(X, Y, Z).

mult(X, zero, zero).
mult(X, s(Y), Z) :- mult(X, Y, W), add(X, W, Z)

expt(X, zero, s(zero)).
expt(X, s(Y), Z) :- expt(X, Y, W), mult(X, W, Z)
```

Fibonacci numbers

```prolog
fib(zero, zero).
fib(s(zero), s(zero)).
fib(s(s(X)), Y) :- fib(s(X), Z), fib(X, W), add(Z, W, Y).
```

For the Fibonacci example we could also use [[ProLog]]s internal arithmetics like this:

```prolog
fib(0, 0).
fib(1, 1).
fib(X, Y) :- D is X-1, E is X-2, fib(D, Z), fib(E, W), Y is Z+W
```

Functions that work on lists can be generated the same way.

## Cut Operator

The flexibility of [[ProLog]] programs often yield non-optimal algorithm [[Laufzeit|Running Times]]. We can thus use the **cut operator** to essentially prune parts of the program.
