Hey @Agent, you will have to adhere to the following rules as good as possible.  

## Contribution Guidelines (@Agent: You will have to adhere to these guidelines as you are contributing to this project)  

Our most important concepts are "High Cohesion + Low Coupling" and "Vertical Slices", to create good internal modules. We make sure that stuff that belongs together is near each other both in code and filesystem while also being as little coupled as possible to the rest

## Modularity

The service is modular. Every folder is one module. Unit and E2E tests are part of the module they are testing. Modules should not import internal objects from other modules. Instead, they should communicate over public APIs / Interfaces (e.g.: exported objects in `__init__.py` files). This reduces coupling and we can extract modules into microservices if needed.

Use dependency injection and composition instead of inheritance to combine modules.

Create a layered architecture. The lower levels operate on primitive operations and data structures while at the higher level, there should be a simpler API.

## Types

We value type safety a lot. Good types make code more readable, correct and safe. GitHub Actions and `make lint` ensure that there are no linting errors or warnings.

If not possible any other way, use `# pyright: ignore` comments. BUT, make sure to always add a small comment explaining why this was needed.

Tests are type-checked as well. Otherwise, errors will quickly creep in.

## Formatting

We value formatting a lot. Good formatting makes code more readable, git diffs more precise and merge conflicts happen less often.

## Readability and Understandability

We value readability, comments, doc strings and pragmatic solutions. Code should be easily understandable by regular developers.

Function names should describe what a function is doing in an honest way, meaning it should not hide behavior behind its name. They should also respect established prefixes from the codebase (usually `get_`, `update_`, `set_`, `convert_`, `add_`, `remove_`, `process_`, `generate_`, `read_`, etc.).
Generally, names across the entire codebase (functions, classes, variables, parameters, etc.) should be as consistent as possible. Do not switch between different names for the same underlying concept.

Functions that are more complex have to include a doc string. Doc strings should not be AI-generated nonsense but:
- one line summary
- empty line
- more detailed description with explicit hints about what the function does and how to use it and errors it can throw marked with `RAISES <ErrorName>`
Not every function needs a doc string. A pure repetition of the function name is not useful.

Comments should provide clarity in cases where the code and doc strings do not suffice. They can also be used to structure more complex workflows. Generally prefer doc strings over comments and comments over no comments.

Pragmatic (simple) solutions are preferred. Indirection through deep layering of small functions or abstractions without use, should be avoided. Prefer simple side-effect free functions over complex stateful objects. Use early returns to keep context small.

Only apply DRY to things that are **supposed** to have the same behavior, not things that **happen** to have the same behavior

Let data be data and let actions be actions. Do not mix data with actions. Create functions for actions, create objects for data and create stateful classes for orchestrating data and actions.

Prefer immutable objects where possible.

Do not change the global state.

Absence of structure is more structured than bad structure.

## Backwards Compatibility

Changes should preferably be backwards compatible and purely **additive**. Avoid changing old interfaces instead of extending or adding new ones. Then slowly deprecate old interfaces, attributes, etc. by migrating to newer types.

## Testing

Tests should cover the entire public API of a module or object. If parts of the private internal functions can not be tested via the public API they might need to be refactored into a new module which can be tested via its public API then. These are so called iceberg objects/modules.