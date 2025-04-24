---
uni-module: "AI"
---

# Semantic Network

A semantic [[Network]] is a [[Gerichteter Graph|Directed Graph]] for representing knowledge.

Its nodes represent **objects** and **[[Concept|concepts]]** (which are classes of objects).
Its edges (called **links**) represent relations between the nodes.

Links labeled _isa_ (inclusion, inclusion of [[Concept|concepts]]) and _inst_ (instance, [[Concept]] of membership) have a special meaning as they can propagate properties encoded by other links (see example).
We differnetiate between isa and inst to not mix up objects and [[Concept|concepts]], which are different things.

However links still dont have any meaning for a machine.

We can use [[Inference]] on semantic networks to derive new [[Concept|concepts]] and relations from the existing ones.

If
$$A \stackrel{\text { isa }}{\longrightarrow} B \stackrel{R}{\longrightarrow} C$$
or
$$A \stackrel{\text { inst }}{\longrightarrow} B \stackrel{R}{\longrightarrow} C$$
then we can derive a relation
$$A \stackrel{\text { R }}{\longrightarrow} C$$

We differnetiate between two [[Teilgraph|Subgraphs]] of a semantic network:

- [[Terminology]]
- [[Assertion]]

To make semantic networks work in computers we have to get away from the graphical representation and use some kind of linear notation. We could for example use functions (links) with arguments (nodes) to represent a [[Graph]]. Can be implemented in [[ProLog]].

Rewriting this a bit more gives something that looks like [[First-Order Predicate Logic]].

First-order deduction as process model, gives inheritenc for free, why??? #question

## Example

Question one could ask: Does Jack have wings?

![[Bildschirm­foto 2023-01-31 um 16.27.35.png]]

We can use Property Inheritence to answer this question:

- Jack is an instance of a robin
  - robin is a bird
    - bird has wings
- thus Jack has wings

So we see that semantic networks actually have more **implicit** knowledge/information in them than explicitely written down.
