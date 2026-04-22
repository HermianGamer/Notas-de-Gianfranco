We've already worked with both class variables and instance variables, but we haven't really talked about the difference.

## Instance Variables

Instance variables vary from object to object and are **declared in the constructor.** They're more common:

```python
class Wall:
    def __init__(self):
        self.height = 10 # instance variable (per object)

south_wall = Wall()
south_wall.height = 20 # only updates this instance of a wall
print(south_wall.height)
# prints "20"

north_wall = Wall()
print(north_wall.height)
# prints "10"
```

## Class Variables

Class variables are shared between instances of the same class and are **declared at the top level of a class definition**. They're less common:

```python
class Wall:
    height = 10 # class variable (shared across all instances)

south_wall = Wall()
print(south_wall.height)
# prints "10"

Wall.height = 20 # updates all instances of a Wall

print(south_wall.height)
# prints "20"
```

In other languages these types of variables are often called [static variables](https://en.wikipedia.org/wiki/Static_variable).

## Which Should I Use?

Generally speaking, _stay away from class variables_. Just like global variables, class variables are usually a bad idea because they make it hard to keep track of which parts of your program are making updates. However, it is important to understand how they work because you may see them in the wild.