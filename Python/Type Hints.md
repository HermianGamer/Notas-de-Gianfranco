  
Some functions accept [numbers](https://docs.python.org/3/library/stdtypes.html#numeric-types-int-float-complex) as arguments; others accept [strings](https://docs.python.org/3/library/stdtypes.html#text-sequence-type-str). Some return [lists](https://docs.python.org/3/library/stdtypes.html#sequence-types-list-tuple-range); others return [dictionaries](https://docs.python.org/3/library/stdtypes.html#mapping-types-dict), [booleans](https://docs.python.org/3/library/stdtypes.html#boolean-type-bool), or [`None`](https://docs.python.org/3/reference/datamodel.html#none).

When a program is small, you can _usually_ remember the types of your variables. But as programs grow, it's easy to forget:

- Is `level` an `int` or a `str`?
- Does `get_item()` always return an item name (`str`), or sometimes `None` if it can't find one?
- Is `inventory` a list of strings, or a dictionary of item counts?

[Type hints](https://docs.python.org/3/library/typing.html) let us write those expectations directly in our code:

```py
def get_damage(weapon: dict, level: int) -> int:
    return weapon["damage"] + (level * 2)
```

The `weapon: dict`, `level: int`, and `-> int` parts are type hints. They tell humans _and_code editors what kinds of values the function expects and returns.

Type hints _don't make Python stop being Python_. It's still a [dynamically typed](https://en.wikipedia.org/wiki/Type_system#Dynamic_type_checking_and_runtime_type_information) language, and it won't automatically reject the wrong value just because a type hint says so.

Type hints are for:

- Making code easier to read
- Helping your editor autocomplete and warn you about mistakes
- Making bugs easier to spot before running your code