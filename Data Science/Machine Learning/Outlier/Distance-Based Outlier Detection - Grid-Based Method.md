---
uni-module: "KDD"
---

# Distance-Based Outlier Detection - Grid-Based Method

Works in a smiliar way to the [[Distance-Based Outlier Detection - Nested Loop Method]] but it tries to reduce the amount of loops by grouping multiple [[Entity|Data Objects]] into cells.

## Create a grid

- Divide data space into a multidimensional grid
- Each cell has diagonal length $\frac{r}{2}$
- Each cell has length $\frac{r}{2\sqrt{ l }}$ where $l$ is the dimension of the dataset
- There are Level 1 cells which have $d(c,y)\leq r$
- There are Level 2 cells which have $d(c, y)\geq r$

A grid will look like this when the objects in cell $C$ have to be classified:
![[Bildschirmfoto 2022-10-15 um 14.56.07.png]]

## Cell Pruning Rules

If
$$a+b_1>\lceil\pi n\rceil$$
then every object in $C$ is not an [[Outlier]].

If
$$\text { If } a+b_1+b_2<\lceil\pi n\rceil+1$$
then all objects in $C$ are outliers.

For all other cases the objects have to be checked individually. For example with the [[Distance-Based Outlier Detection - Nested Loop Method]].
