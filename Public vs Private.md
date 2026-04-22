By default, all properties and methods in a class are _public_. That means that you can access them with the `.` operator:

```python
wall.height = 10
print(wall.height)
# 10
```

[Private](https://docs.python.org/3/tutorial/classes.html#tut-private) data members are a way to encapsulate logic and data _within a class definition_. To make a property or method private just prefix it with two underscores:

```python
class Wall:
    def __init__(self, armor, magic_resistance):
        self.__armor = armor
        self.__magic_resistance = magic_resistance

    def get_defense(self):
        return self.__armor + self.__magic_resistance

front_wall = Wall(10, 20)

# This results in an error
print(front_wall.__armor)

# This works
print(front_wall.get_defense())
# 30
```

We do this to make it _easier to use our class_. Now when another developer (or even ourselves) use the `Wall` class, they don't need to think about how `armor` and `magic_resistance` affect the `defense` of a `Wall`. In fact, we don't even allow them to access `armor` and `magic_resistance` directly by making them private with `__`.

They simply call the public `get_defense()` method and know that the correct value will be returned.

Note that you won't need to understand all the details behind this, but Python "private" members aren't _truly_ private. Python just changes their names with ["name mangling"](https://docs.python.org/3/reference/expressions.html#private-name-mangling) to make outside access less straightforward.