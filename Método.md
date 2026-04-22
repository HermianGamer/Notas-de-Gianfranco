So you might be wondering _why_ classes are useful, they're like [dictionaries](https://docs.python.org/3/tutorial/datastructures.html#dictionaries)... but worse... Right?

Well, no. First of all, classes provide structure. The `class` definition says "hey, I have these specific properties". A dictionary is more powerful in the sense that you can store whatever you want in it, but that also makes it less clear _what on earth is in there_ at any given time.

_Another_ thing that makes classes useful is that they can have [methods](https://docs.python.org/3/tutorial/classes.html#method-objects)! A method is just a function that's tied directly to a class and has access to its properties. See the `take_damage` method here:

```python
class Soldier:
    health = 5

    # This is a method that reduces the
    # health of the soldier
    def take_damage(self, damage):
        self.health -= damage

soldier_one = Soldier()
soldier_one.take_damage(2)
print(soldier_one.health)
# prints "3"

soldier_two = Soldier()
soldier_two.take_damage(1)
print(soldier_two.health)
# prints "4"
```

# Methods Can Return

If a normal function doesn't return anything, it's typically not a very useful function. In contrast, methods often don't return anything because they can mutate (update) the properties of the object instead. That's exactly what we did in the last assignment.

However, they _can_ return values if you want! They're just functions with access to an object, after all. A common use case is a "getter" method that returns a calculated value based on the properties of the object.

```python
class Soldier:
    armor = 2
    num_weapons = 2

    def get_speed(self):
        speed = 10
        speed -= self.armor
        speed -= self.num_weapons
        return speed

soldier_one = Soldier()
print(soldier_one.get_speed())
# prints "6"
```   