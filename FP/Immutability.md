In [[Functional Programming]], we strive to make data _[immutable](https://en.wikipedia.org/wiki/Immutable_object)_. Once a value is created, it cannot be changed. _Mutable_ data, on the other hand, can be changed after it's created.

## Who Cares?

Immutable data is easier to think about and work with. When 10 different functions have access to the same variable, and you're debugging a problem with that variable, you have to consider the possibility that any of those functions could have changed the value.

When a variable is immutable, you can be sure that it hasn't changed since it was created. It's a helluva lot easier to work with.

_Generally speaking, immutability means fewer bugs and more maintainable code._