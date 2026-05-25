It's possible to type-hint a container with _just_ the container type:

```py
items: list = ["Black Firebomb", "Titanite Chunk"]
```

This says `items` is a list, but it doesn't tell us what _kind of values_ go inside! Assuming you know what's inside, best to be specific:

```py
items: list[str] = ["Black Firebomb", "Titanite Chunk"]
```

That said, bare container type hints aren't _wrong_. Sometimes you really _don't know_ what types of values a container will hold, or the specific type hint would be too complicated to be useful. You'll see that occasionally with `dict`s. Just give clear type hints whenever possible!