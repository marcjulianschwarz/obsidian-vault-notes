---
uni-module: "KDD"

alias: "FPgrowth"
---

# Frequent Pattern Growth

Avoids explicit candidate generation (compared to [[A priori - Frequent Item Approach]]) and thus has a [[Depth-first search]] approach.

> [!NOTE] Major philosophy
> Grow long patterns from short ones using local frequent items only.
> For example restricting database to frequent item _abc_. Now local frequent item _d_ on restricted database will lead to frequent item _abcd_ on whole dataset.

## Method

### 1. Construct FP-tree from Transaction Database

1. Scan DB once to find frequent 1-[[Itemset]] based on `min_sup`
2. Sort frequent items in frequency-descending order → [[F-list]]
3. Scan DB again to construct [[FP-tree]]

### 2. Find Itemset p from its Conditional Pattern Base

- [[Frequent Item - Header Table]]
- [[Conditional Pattern Base]]
- [[Conditional FP-tree]]
- Recursion on Conditional FP-tree

## Scaling by Database Projection

Parallel Projection
Partition Projection

## Advantages

- Can use "Divide and Conquer" Approach
- Compressed DB using [[FP-tree]]
- No candidate generation and test needed → see [[A priori - Frequent Item Approach]]
- **No** repeated scans of the [[Datenbank|Database]]
