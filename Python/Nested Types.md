  
We've looked at relatively simple container types like `list[str]`, but they can get more complex when _one container holds another container_. That is, it's possible to have **nested container types**.

A dictionary, for example, could map each character's _name_ to their _list of spells_:

```py
character_spells: dict[str, list[str]] = {
    "Gandalf": ["Fireball", "Light"],
    "Frodo": ["Hide"],
}
```

We read `dict[str, list[str]]` from the outside in:

- It's a dictionary (`dict`)
- Each _key_ is a string (`str`)
- Each _value_ is a list of strings (`list[str]`)

In extreme cases, nested types can get _super_ confusing, but honestly it's less confusing than it would be _without_ the typing. For the time being, just know that type hints _can_ describe containers within containers.

Boots