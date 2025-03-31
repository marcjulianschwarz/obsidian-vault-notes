
These are some rules or principles I want to follow for all of my coding projects. Of course they should not be applied blindly but they give a good starting point.


## General

- Prefer easy over complex!
- Prefer simple side-effect free functions over complex objects
	- See [[Speculative Generalization]]
- Avoid logical complexity
	- No deeply nested ifs
	- Use early returns

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
- Use [[Dependency Injection]] and composition instead of inheritance

- prefer short functions focusing each on one task with clear input and output types 
- prefer composition over inheritance 
- prefer immutable objects where possible
- no changing global state 
- the architecture should be layered 
	- the lower levels operate on primitive operations and data structures while at the higher level, there should be a simpler API
- avoid premature optimization


## For Git 

- do regular git pulls from the main branch and merge or rebase them into your local feature branch 
	- this will make merging with main in the end a LOT easier 
- make feature branch naming consistent (link to an issue number)
- prefer squash commits when having lots of unnecessary commits 

