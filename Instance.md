Remember, an object is an "instance" of a [[Class]].

> In object-oriented programming, an instance is a concrete occurrence of any object... "Instance" is synonymous with "object" as they are each a particular value... "Instance" emphasizes the distinct identity of the object. The creation of an instance is called instantiation.
> 
> -- [Wikipedia](https://en.wikipedia.org/wiki/Instance_\(computer_science\))

I can create a `Wall` class (you can think of a class as a "blueprint" or a "template" for an object) with a [[Constructors]] function:

```py
class Wall:
    def __init__(self, depth, height, width):
        self.depth = depth
        self.height = height
        self.width = width
```

Then I can create three different "instances" of the class. Or, in other words, I can create three separate objects, each with their own properties independent of each other:

```python
wall_maria = Wall(1, 2, 3)
wall_rose = Wall(4, 5, 6)
wall_sina = Wall(9, 8, 7)
```