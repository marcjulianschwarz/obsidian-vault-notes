---
uni-module: "XAI"

alias: ["Shadow Model", "Approximation Model", "Metamodel", "Response Surface Model", "Emulator"]
---

# Global Surrogate

> [!NOTE]+ Idea
> Train a simple [[Ante-Hoc|intrinsicly]] interpretable model to approximate the output of a more complex [[Black Box Model]].
> Use this simple model to explain the models descision (not the real world).

1. Selecte, create or sample an input dataset and generate predictions with the [[Black Box Model]]
2. Train the surrogate model on this data to match the predictions
3. Interpret the model
   1. Judge the relevance of the interpretation by the [[R-Squared]] error of the surrogate model. High error might lead to wrong explanations.

The sample selection plays a crucial role. Selecting samples only from one region of the feature space might lead to a local surrogate like [[Local Surrogate|LIME]] does on purpose.

## Example

Train a [[Decision Tree]] on the predictions of a [[Support Vector Machine]].

![[Bildschirmfoto 2023-07-12 um 11.01.25.png]]

> [!Check]+ Pros
>
> - flexible ([[Model-Agnostic]], [[Post-Hoc]])
> - intuitive
> - [[R-Squared]] to measure how good the interpretations can be

> [!Warning]+ Cons
>
> - conclusions only about the model, not the data
> - where should the [[R-Squared]] cut-off be?
> - how to choose a good subset of data?
