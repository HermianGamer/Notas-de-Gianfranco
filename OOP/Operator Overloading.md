Another kind of built-in [[Polymorphism]] in Python is the ability to override how an operator works. For example, the `+` operator works for built-in types like integers and strings.

```python
print(3 + 4)
# 7

print("three " + "four")
# three four
```

Custom classes on the other hand don't have any built-in support for those operators:

```python
class Point:
    def __init__(self, x, y):
        self.x = x
        self.y = y


p1 = Point(4, 5)
p2 = Point(2, 3)
p3 = p1 + p2
# TypeError: unsupported operand type(s) for +: 'Point' and 'Point'
```

But _we can add our own support_! If we create an `__add__(self, other)` method on our class, the Python interpreter will use it when instances of the class are being added with the `+` operator. The name of the second parameter (`other` in this example) is just a convention - you can use any valid parameter name. Here's an example:

```python
class Point:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def __add__(self, other):
        x = self.x + other.x
        y = self.y + other.y
        return Point(x, y)

p1 = Point(4, 5)
p2 = Point(2, 3)
p3 = p1 + p2
# p3 is (6, 8)
```

Now, when `p1 + p2` is executed, under the hood the Python interpreter just calls `p1.__add__(p2)`.