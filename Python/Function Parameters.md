[Function parameters](https://docs.python.org/3/glossary.html#term-parameter) can have type hints too! The syntax is the same as variable type hints: put a colon after the parameter name, then the type.

```py
def greet_player(name: str):
    print(f"Welcome, {name}!")
```

When a function has multiple parameters, each one can have its own type hint:

```py
def add_gold(current_gold: int, found_gold: int):
    return current_gold + found_gold
```

While adding a type hint to a variable declaration like:

```py
character_health: float = 72.5
```

is considered a bit _redundant_ due to type inference, adding type hints to function parameters is _not_ redundant. If you don't add them, your tooling won't know what types the function expects, which makes autocomplete and error checking less effective.

>Hover your cursor over the `status` variable. See how the tooltip can show you that it's a string? That's what makes type hinting useful! Note that `name`, `level`, `health`, and `magic` are _all "unknown"_ because Python can't infer function parameter types without hints.

