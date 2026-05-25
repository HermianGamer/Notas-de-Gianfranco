Sometimes we work with variables that [may or may not](https://docs.python.org/3/library/typing.html#typing.Optional) have an "actual value." For example, a character _might_ have a damage bonus, or they might not. If they _don't_, we can represent that lack of value with [`None`](https://docs.python.org/3/reference/datamodel.html#none).

The [`|` operator](https://docs.python.org/3/library/typing.html#typing.Optional) indicates that a value can be of multiple types:

```py
damage_bonus: int | None
```

That means `damage_bonus` can be either an integer (the bonus amount) _or_ `None`. For another example, a function might return a prepared spell if one is ready, or `None` if no spell is prepared:

```py
def get_prepared_spell(has_spell: bool) -> str | None:
    if has_spell:
        return "Fireball"

    return None
```