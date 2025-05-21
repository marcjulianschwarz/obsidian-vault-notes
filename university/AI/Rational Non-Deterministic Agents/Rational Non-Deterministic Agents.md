# Rational Non-Deterministic Agents


> [!Warning] Rational != Perfect
> - rational is not omniscient (there can be very unlikely events in the future that are not *expected*)
> - rational is not clairvoyant ([[Percept]] may not supply all relevant information)
> - rational is not successful ([[Action]] outcomes may not be as expected)
 
- rational → exploration, learning, [[Autonomy]]
- Sources of uncertainty
	- Non-deterministic [[Action|Actions]]
	- [[Partially Observable Environment]] with unreliable sensors ([[Percept]])
	- Uncertainty about the domain behavior.

Specify [[PEAS]] to desing a rational agent for that exact specification. See the different types of [[Environment|Environments]] that an [[Rational Agent|Agent]] can act in.


## Agent Architectures based on Belief States

We now have a [[Partially Observable Environment]] with non-deterministic actions. The idea is to keep track of *all* possible states the world could be in via a [[Belief State]] in a [[Model-based Reflex Agent]].

In a [[Fully Observable Environment]], [[Deterministic Environment]] the [[Belief State]] is a singleton called [[World State]] and the [[Transition Model]] is a function from states and actions to states → a [[Transition Function]].

> [!Tip] (Recap) of World Models by Agent Type in a [[Fully Observable Environment|fully observable]] [[Deterministic Environment|deterministic environment]]: 
> - [[Search Problem]] based agents
>   - [[Goal-based Agent]] with [[World State]] = current state
>   - no [[Inference]]
>   - goal = goal state of [[Search Problem]]
> - [[Constraint Satisfaction Problem|CSP]] based agents
>   - [[Goal-based Agent]] with [[World State]] = [[Constraint Satisfaction Problem|Constraint Network]]
>   - [[Inference]] = constraint propagation ([[Forward Checking]], etc.)
>   - Goal = satisfy assignment
> - [[Logical System|Logic]] based agents
>   - [[Model-based Reflex Agent]] with [[World State]] = logical formula
>   - [[Inference]] = e.g. [[Davis Putnam Procedure|DPLL]] or [[Resolution Calculus|Resolution]]
> - [[Planning Task]] based agents
>   - [[Goal-based Agent]] with [[World State]] = [[Propositional Logic|PL0]]
>   - [[Transition Model]] = [[STRIPS]]
>   - [[Inference]] = state/plan space search
>   - Goal = Complete Plan

> [!Tip] New world models
> In a [[Fully Observable Environment|fully observable]] but [[Stochastic Environment|stochastic environment]] the [[Belief State]] must deal with a *set of possible states* and thus the [[Transition Function]] generalizes to a [[Transition Relation]].
> 
> In a [[Deterministic Environment|deterministic]] but [[Partially Observable Environment]] the [[Belief State]] must deal with a *set of possible states*. But we can use a [[Transition Function]]. We need a [[Sensor Model]] which predicts the influence of [[Percept|percepts]] on the [[Belief State]].
> 
> In a [[Stochastic Environment|stochastic]] and [[Partially Observable Environment]] we mix the two ideas → [[Sensor Model]] and [[Transition Relation]].

We now have *new world models*, so we also get new agent types:
- [[Probabilistic Agent]]
- [[Decision-Theoretic Agent]]

## Modeling Uncertainty

A set of _possible_ states is not enough, we also need a world model that estimates their likelihood.

We want to
- weigh alternatives 
- and express incomplete knowledge

We can do this with probabilities. However it is quite hard to correctly _assess_ probabilities using only statistics. We thus want to use Probabilistic Reasoning to assess difficult probabilities from easier ones.

**Acting under Uncertainty**

Goal → Possible Plans → Decision (use plan with highest probability of achieving goal)

Decision Theory = Utility Theory + Probability Theory

Maximize [[Expected Utility]].

→ [[Utility-based Agent]]
→ [[Decision-Theoretic Agent]]


See [[Probability Theory]]
See [[Bayesian Network]]

## Making Simple Decisions Rationally (in an episodic environment)

We can use a [[Bayesian Network]] to model the world and sensors. Based on the probabilities that we can get from the network we have to make decisions. For this we will be looking at [[Decision Theory]] and [[Utility-based Agent|Utility-based Agents]].

> [!blue-highlight] MEU principle for Rationality
> A [[Utility-based Agent]] is called rational iff it only chooses rational [[Action|Actions]] by maximizing the [[Expected Utility]].

We will treat the result of an action as a [[Zufallsvariable|Random Variable]].

**Rational Preferences**
It is hard to directly measure utility but we can let agents choose between two states. This is called [[Preferences]].
Now [[Ramseys Theorem]] defines how a utility function relates to the preferences. 

We call a total ordering on states a value function. 

- standard lottery
- micromorts
- QALYs 
- money vs. utility


**Multi-Attribute Utility Function**
A utility function not on states directly but on states represented by sets of [[Zufallsvariable|Random Variables]] $X$ with domains $D$.

We can now label edges in a [[Bayesian Network]] with the influences calculates via [[Strict Dominance]] or [[Stochastic Dominance]]. 

Now we can construct a [[Decision Network]]. 


**The Value of Information**
- [[Value of Perfect Information]]
- [[Information Gathering Agent]]



- [[Temporal Probability Model]]
- [[Markov Decision Process]]
- [[Partially Observable MDP]]


## Machine Learning 

We need [[Machine Learning]] (learning) when 
- the designer of an agent lacks omniscience 
- the world is a [[Partially Observable MDP|POMDP]] with unknown [[Übergangsmatrix|Transition Model]] and [[Sensor Model]]

So we want to look at how [[Learning Agent|learning agents]] can use [[Inductive Learning]]. The computational [[Komplexitätsklassen|Complexity]] of the inductive learning problem is tied to the size of the Hypothesis Space. 

Large Hypothesis Space → High [[Komplexitätsklassen|Complexity]] but good solution
Small Hypothesis Space → Low [[Komplexitätsklassen|Complexity]] but bad solution

There are four main reasons why the estimated function might differ from the target function. 
- Realisability 
- [[Varianz|Variance]] in different subsets of the target function. We would need more data to get closer to it.
- Noise. When the target function is non-deterministic we can not perfectly approximate it 
- Computational [[Komplexitätsklassen|Complexity]]. When the [[Hypothesis Space]] is too large we have to approximate. 

## Statistical Learning

- [[Full Bayesian Learning]]
	- [[Maximum A Posteriori Learning|MAP Learning]]
	- [[Minimum Description Length Learning|MDL Learning]]
	- [[Maximum Likelihood Estimation|ML Learning]]

Now instead of having a fixed set of hypotheses we want to estimate a continuum of hypotheses $h_{\theta}$.
For simple [[Binomialverteilung|binomial]] models we can directly calculate the [[Likelihood]] from [[Independent Identically Distributed|IID]] observations 
$$
P\left(d \mid h_\theta\right)=\prod_{j=1}^N P\left(d_j \mid h_\theta\right)=\theta^c \cdot(1-\theta)^{\ell}
$$
Again, we can use the [[Log-Likelihood]] 
$$L(d \mid h):=\log _2(P(d \mid h))$$
to rewrite the product into a sum of logs
$$\begin{aligned}
L\left(d \mid h_\theta\right) & =\log _2\left(P\left(d \mid h_\theta\right)\right) \\
& =\sum_{j=1}^N \log _2\left(P\left(d_j \mid h_\theta\right)\right) \\
& =c \log _2(\theta)+\ell \log _2(1-\theta)
\end{aligned}
$$
Now we can use the [[Gradient]] to directly get the maximizing equation 
$$\frac{\partial}{\partial \theta}\left(L\left(d \mid h_\theta\right)\right)=\frac{c}{\theta}-\frac{\ell}{1-\theta}=0
$$

[[Naive Bayes Classifier]]


## Logic-based Learning 

In [[Logical System|Logic]] based inductive learning we try to learn a hypothesis $h$ that explains the classification of the examples given their description. We call 
$$h,\mathcal{D}\models \mathcal{C}$$
the **explanation constraint**, where $\mathcal{D}$ is the conjunction of the descriptions and $\mathcal{C}$ the [[Konjunktion|Conjunction]] of their classifications. 

A [[Decision Tree]] can also be represented by a [[First-Order Predicate Logic]] formula 
$$\forall e.\text{PositiveClass}(e)\Leftrightarrow A_1(e, v_1) \lor (A_1(e, v_2) \land A_2(e))\lor A_3(e) \lor \dots$$
where $e$ is an example that should be classified as positive when attribute one has value one or when attribute one has value two and attribute two is true or when attribute three is true. 
In all other cases the example is classified as negative. 

So we have a [[Disjunktion|Disjunction]] of all paths from the root to the positive leaves interpreted as [[Konjunktion|Conjunctions]] of the attributes on the path. 

So in theory we want to have [[Cummulative Development]] in learning.

There are three main approaches to this.
- [[Deductive Learning]]
	- [[Explanation-based Learning]]
	- [[Relevance-based Learning]]
- [[Knowledge-based Inductive Learning]]

There are three main modes of [[Inference]]
- [[Deduction]]
- [[Abduction]]
- [[Induction]]

- [[Inductive Logic Programming]]