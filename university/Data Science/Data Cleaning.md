---
uni-module: "KDD"
---

# Data Cleaning

## Data Discrepancy Detection

Errors in [[Dataset|data]] can be detected by checking:

- [[Metadaten|Metadata]]
- field overloading
- uniquness, consecutive and null rule
- Data Scrubbing (domain knowledge)
- Data Auditing (analyse data to find rules) → [[Korrelation|Correlation]], [[Clustering]] → [[Outlier|Outlier]]

## Incomplete / Missing data

Can happen due to:

- equipment malfunction
- inconcistency with other data
- misunderstanding → data not entered
- importance of data at time of recording
- missing history or missing changes of data

How to handle missing data?

- ignore the tuples with missing Data
- fill in values manually
- fill in values automatically → constant, [[Arithmetic Mean|mean]], inference based / most probable ([[Bayes Formel]] or Decision tree)

## Noisy Data

Can happen due to:

- faulty instruments
- data entry/transmission problem
- technology limitation
- inconcistency in naming conventions

How to handle noisy data?

- Binning → sort data, partition into bins, then smooth by bin [[Arithmetic Mean|mean]]/median/boundaries
- [[Regression]]
- [[Clustering]]
- Combine computer and human inspection ([[Outlier]])
