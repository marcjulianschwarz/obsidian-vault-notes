These are some rules or principles I want to follow for all of my coding projects. Of course they should not be applied blindly but they give a good starting point.

## General

- Prefer easy over complex!
- Prefer simple side-effect free functions over complex objects
	- See [[Speculative Generalization]]
- Avoid logical complexity
	- No deeply nested ifs
	- Use early returns
- Avoid premature optimisation
- Increase Cohesion
	- Stuff that belongs together should be together (domain)
- Decrease Coupling

## Functions

- clear input and output types 
- readable
- concise
- efficient
- short -> focusing each on one task 

## Refactoring

- Do not refactor to an atomic level 
	- A function is **allowed** to do more than one thing
	- A function must not be small
- When in doubt, parameterize

## Abstraction

- Absence of structure is more structured than bad structure
- Encapsulate at the level of modules and do this as much as possible
	- makes it easier to merge/rebase feature branches
- Prefer commenting sections over extracting them
- Let data be data
- Let actions be actions
- Do not mix data with actions
	- create functions for actions 
	- if you create objects for data, then do not let them have methods 
- Prefer [[Dependency Injection]] and composition instead of inheritance
- Prefer immutable objects where possible
- No changing of global state 
- The architecture should be layered 
	- the lower levels operate on primitive operations and data structures while at the higher level, there should be a simpler API

## Git 

- do regular git pulls for the main branch and rebase feature branches on top
- make feature branch naming consistent by linking to an issue number and/or including the ticket type
- prefer squash commits when having lots of unnecessary commits 

