---
uni-module: AI
---
# Spam Detection

[[N Gram Model]] on word and character level similar to [[Language Identification]] by applying [[Bayes Formel|Bayes Rule]]

$$\underset{c \in\{\text { spam, ham }\}}{\operatorname{argmax}}(P(\boldsymbol{c} \mid \boldsymbol{m})) \underset{\boldsymbol{c} \in\{\text { spam, ham }\}}{\operatorname{argmax}}(P(\boldsymbol{m} \mid \boldsymbol{c}) P(\boldsymbol{c}))$$

