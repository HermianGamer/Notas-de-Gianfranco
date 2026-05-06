The [zip](https://docs.python.org/3/library/functions.html#zip) [[Built-In Function]] takes two iterables (in this case lists), and returns a _new_ iterable where each element is a [[Tuple]] containing one element from each of the original iterables.

```py
a = [1, 2, 3]
b = [4, 5, 6]

c = list(zip(a, b))
print(c)
# [(1, 4), (2, 5), (3, 6)]
```