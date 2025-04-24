---
uni-module: "KDD"

alias: ["Datasets", "Data", "Data Sets"]
---

# Dataset

A [[Dataset]] is made up of [[Entity|Data Objects]] which can have features with various [[Typen von Daten|types]].
## Types of Datasets

Datasets with one attribute are _univariate_. Datasets with more than one attribute are called [[Multivariate Dataset]], commonly given in a table

There is also bivariate and trivariate data but this description isn't being used a lot.

- Data Streams, sensor data
- [[Time Series Data]]
- [[Social Network]], [[Graph]]
- [[Hierarchy]]
- [[Relationenmodell]]
- Heterogeneous databases and legacy databases
- NoSQL
- Spatial Data (also spatial-temporal)
- Multimedia (video, etc.)
- Text (term [[frequency]] vectors) → [[Vocabulary|vocab]] with occureances for each word for every document → [[Natural Language Processing]]
- WWW
- [[Data Warehouse System - Architektur]]
- Transactional Database e.g. customer bought items for each customer (Pattern Mining, which articles are bought together)
- [[Data Matrix]] (without column names)

## Ordered Data:

- video
- [[Time Series Data]]
- sequential
- genetic sequence data

## Spatial, image, multimedia:

- maps
- image
- video


Also see [[Curse of Dimensionality]].


Proximity Measure for differenty attribute types:

- Nominal → [[Simple Matching Coefficient]], [[One-Hot-Encoding]]
- Ordinal → [[Integer Encoding]]
- Binary → [[Contingency table for binary data]]

[[Basic Statistical Descriptors]]

