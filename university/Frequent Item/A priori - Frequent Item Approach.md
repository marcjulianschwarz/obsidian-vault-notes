---
uni-module: "KDD"
---

# A priori - Frequent Item Approach

> [!NOTE] Main Idea
> Supersets of infrequent [[Itemset|Itemsets]] should not be gernerated and tested.
>
> → [[Downward-Closure Property]]

## Method

- Scan [[Datenbank|Database]] to get 1-frequent-Itemsets
- Generate k+1 long candidates where each subset is frequent ([[Downward-Closure Property]])
- Test these against DB and discard infrequent [[Itemset|Itemsets]]
- Terminate when no further candidate can be generated.

## Example

![[Bildschirmfoto 2022-05-30 um 11.01.55.png]]

## Problems

- DB has to be scanned a lot of times.
- Count of candidates can get huge (exponential crossproduct).

[[Itemset|Itemsets]] can be stored in Hashtrees like this:

![[Bildschirmfoto 2022-05-30 um 11.13.39.png]]
