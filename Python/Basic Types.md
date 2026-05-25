  
To add a type hint to a variable declaration, put a colon after the variable name, then the type. This comes _before_ the equals sign and the value:

```py
character_name: str = "Sir Galahad"
character_level: int = 7
character_health: float = 72.5
has_magic: bool = True
```

_The values work the exact same way they did before._ In fact, when it comes to simple variable declarations like this, you don't actually _need_ the hint. In this example:

```py
character_health = 72.5
```

Because `character_health` is assigned a value of `72.5`, your tooling can _infer_ that it's a `float`. That said, if you also want to _see_ the type name, you can optionally add it.