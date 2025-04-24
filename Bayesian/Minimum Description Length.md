---
uni-module: AI
aliases:
  - MDL
  - MDL Hypothesis
  - Description Length
---
# Minimum Description Length

Let $h$ be a hypothesis from a [[Hypothesis Space]] $\mathcal{H}$ and $E$ a set of examples, then the description length of $(h,E)$ is computed a follows 

- encode the hypothesis as a turing machine program → count bits 
- count data bits 
	- correct prediciton → zero bit 
	- wrong prediction → bits in the size of the error 

MDL minimizes the total number of bits required. 

