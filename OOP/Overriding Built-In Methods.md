  
Last but not least, let's take a look at some of the built-in [[Método]]s we can override in Python. While there isn't a default behavior for the arithmetic operators like we just saw, there _is_ a default behavior for **printing** a class instance:

```python
class Point:
    def __init__(self, x, y):
        self.x = x
        self.y = y


p1 = Point(4, 5)
print(p1)
# prints "<Point object at 0xa0acf8>"
```

That's not super useful! We probably want to see the fields!

Let's teach our `Point` class to print itself. The [`__str__`](https://docs.python.org/3/reference/datamodel.html#object.__str__) method (short for "string") lets us do just that. It takes no inputs but returns a string that will be printed to the console when someone passes an instance of the class to Python's `print()` function.

```python
class Point:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def __str__(self):
        return f"({self.x},{self.y})"

p1 = Point(4, 5)
print(p1)
# prints "(4,5)"
```

The [`__repr__`](https://docs.python.org/3/reference/datamodel.html#object.__repr__) method works similarly: the difference is that it's intended for use in debugging by developers, rather than in printing strings to end users.