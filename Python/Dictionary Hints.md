[Dictionaries](https://docs.python.org/3/library/stdtypes.html#mapping-types-dict) are container types too, but they map **keys** to **values**, so their type hints include _both_:

```py
item_counts: dict[str, int] = {
    "Wooden Arrow": 30,
    "Small Amethyst": 2,
}
```

The first type is for the keys; the second is for the values.

```py
dict[key_type, value_type]
```

So `dict[str, int]` means:

- The keys are strings
- The values are integers

>Not all types [can be used as dictionary _keys_](https://docs.python.org/3/glossary.html#term-hashable). The key types that you'll see most often are strings and integers. Dictionary _values_, on the other hand, can be any type.

