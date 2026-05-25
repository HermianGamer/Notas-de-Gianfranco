We can simulate the shape of sum types in Python by using classes – like our `MaybeParsed`class with subclasses named `Parsed` and `ParseError`. That's better than nothing, but it's awkward.

The [type hints](https://docs.python.org/3/library/typing.html) system in modern Python offers a more direct way of describing a value that may be one type or another. We can use what's called a [union type](https://docs.python.org/3/library/stdtypes.html#union-type):

```py
def parse_document(doc_name: str, content: str) -> Parsed | ParseError:
    ...
```

The `Parsed | ParseError` annotation means, "This function returns either a `Parsed`value or a `ParseError` value." Crucially, the `|` ("or") operator lets us express that relationship without forcing both classes to inherit from the same parent class. `Parsed` and `ParseError` still need to be real types, but they don't need to belong to a shared class hierarchy.

A union type can list any number of possible types for a given value. One of the most common use cases is for _optional_ values like `str | None` – i.e., a value that may be a string, or may be `None` if the string isn't available yet or couldn't be retrieved.

In functional programming, union types are used constantly to make "this or that" situations explicit: _some_ value or _none_; a _result_ from a function or an _error_.

Python is still ultimately a dynamically typed language. The union type, like other type hints, is meant to help developers and their tools (code editors, type checkers). **It's not enforced at runtime.** But being able to document the shape of your data makes it easier to write robust programs.