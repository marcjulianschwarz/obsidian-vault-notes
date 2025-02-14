Some rules for my coding. Every rule has an exception, so don't apply them blindly.

- Prefer easy over complex 
	- e.g. prefer functional over complex objects
	- [[Speculative Generalization]]
- First copy, then refactor
- Do not refactor to an atomic level 
	- e.g. a function is allowed to do more than one line of code 
 
- Absence of structure is more structured than bad structure

- When in doubt, parameterize 
- Encapsulate at the level of modules 
- Dont be afraid of long functions 

- Prefer commenting sections over ectracting them.
- Prefer extracting to nested functions 
- Avoid logical complexity 

- Let data be data
- Let actions be actions
- Do not mix data with actions
	- create function for actions 
	- if you create objects for data, then do not let them have methods 

- Modularize as much as possible 

- Macht es einfacher Feature-Branches zu Mergen 



- use [[Dependency Injection]] when it makes sense 

- readable
- concise
- efficient
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

