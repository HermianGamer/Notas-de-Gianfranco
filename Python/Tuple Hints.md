Lists and sets _usually_ hold multiple values of the same type:

```py
inventory: list[str] = ["Black Knight Halberd", "Skull Lantern", "Notched Whip"]
```

But [tuples](https://docs.python.org/3/library/stdtypes.html#tuples) are a **small fixed group of values** where each _position_ has its own meaning. Because they're fixed, it's quite common for those values to be of different types. For example, a loot drop might have an item name and a quantity:

```py
drop: tuple[str, int] = ("Garnet Mark", 2)
```

`tuple[str, int]` means:

- There are two values in the tuple
- The first value is a string
- The second value is an integer

A tuple can have any number of values – though `2` and `3` are the most common. Here's an example representing a character's HP, MP, and stamina:

```py
stats: tuple[int, float, int] = (100, 42.5, 75)
```

The type hint `tuple[int, float, int]` tells us this is a three-value tuple with an integer, a float, and another integer.