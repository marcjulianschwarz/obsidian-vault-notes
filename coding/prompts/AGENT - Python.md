## Python Rules  

- Make types as strict as possible, do not use `Any` 
- Use the patterns of Facade, Factory and Dependency Injection
- Always type `dict` types strictly by giving key and value types 
- Always use `|` for union types, `| None = None` for optional types and `list[x]` for list types 
- Always catch return values if they exist with `_ = fn()` if you don't want to use the value but still want to call the function 
- Use `uv add` to add new dependencies 
- If you create new empty lists, always specify the type of the list like this: `result: list[MyType] = []` 
- If you set properties of classes without marking them as final, add a type to them: `self.x: int = x`  
