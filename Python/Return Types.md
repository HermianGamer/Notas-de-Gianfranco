You can _also_ annotate the type that you expect a function to [return](https://docs.python.org/3/reference/simple_stmts.html#the-return-statement). When you know what types go into and come out of a function, you can (probably) use it without having to read every line of the function body. Return types come after the parameter list, before the colon:

```py
def add_gold(current_gold: int, found_gold: int) -> int:
    return current_gold + found_gold
```

The `-> int` means this function is _expected_ to return an integer.

**The syntax is a bit different** from type hints on variables and parameters: we use `->` instead of `:`, and there's no variable name before the type hint. This is because it doesn't really matter what name (if any) the function uses internally for the return value; we just care about the type.

Here's another example:

```py
def get_greeting(player_name: str) -> str:
    return f"Welcome, {player_name}!"
```

The `-> str` means this function is expected to return a string.