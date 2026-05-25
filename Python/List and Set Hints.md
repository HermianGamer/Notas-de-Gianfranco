We've covered hints for **basic types** like `str`, `int`, `float`, and `bool`, but you can also add hints for **container types**: types that _hold other values_. For example:

- [`list`](https://docs.python.org/3/library/stdtypes.html#lists): mutable sequence of values
- [`set`](https://docs.python.org/3/library/stdtypes.html#set-types-set-frozenset): unordered collection of unique values
- [`dict`](https://docs.python.org/3/library/stdtypes.html#mapping-types-dict): collection of key-value pairs
- [`tuple`](https://docs.python.org/3/library/stdtypes.html#tuples): immutable sequence of values

When we type-hint a container, we specify what kind of container it is _and_ what type of values it contains. For example, a _list_ of _strings_ can be expressed as `list[str]`:

```py
inventory: list[str] = ["Iron Sword", "Healing Potion"]
```

The "contained" type goes in square brackets after the container type. Similarly, for a _set_ of _strings_, we would write `set[str]`:

```py
unique_items: set[str] = {"Iron Sword", "Healing Potion"}
```