While inheritance is the most _unique_ trait of [[Object Oriented Programming]], polymorphism is probably the most powerful. It also is _not_ particularly unique to [[class]]-based languages. Polymorphism is the ability of a variable, function or object to take on multiple forms.

- "poly" = "many"
- "morph" = "form"

For example, classes in the same hierarchical tree may have methods with the _same name and [signature](https://developer.mozilla.org/en-US/docs/Glossary/Signature/Function)_ but different implementations. Here's a simple example:

```python
class Creature():
    def move(self):
        print("the creature moves")

class Dragon(Creature):
    def move(self):
        print("the dragon flies")

class Kraken(Creature):
    def move(self):
        print("the kraken swims")

for creature in [Creature(), Dragon(), Kraken()]:
    creature.move()
# prints:
# the creature moves
# the dragon flies
# the kraken swims
```

Because all three classes have a `.move()` method, we can shove the objects into a single list, and call the same method on each of them, even though the _implementation_ (method body) is different.

This idea is sometimes referred to as "duck typing". If it looks like a duck, swims like a duck, and quacks like a duck, it's a duck. Or, in our example, if it has a `.move()` method, we can treat it like a `Creature`.

Poder usar el mismo [[Método]] en diferentes [[Instance]]s de distintas [[Class]]es, y que siempre funcione. No necesariamente deben de funcionar igual en todo tipo de clase, pero que siempre funcione.


The Greek roots of the word "polymorphism" are:

- "poly" means "many".
- "morph" means "to change" or "form".

Polymorphism in programming is the ability to present the same interface (function or method signatures) for many different underlying forms (data types).

A classic example is a `Shape` class that `Rectangle`, `Circle`, and `Triangle` can inherit from. Each has different underlying data:

- The circle needs its center point coordinates and radius
- The rectangle needs two coordinates for the top left and bottom right corners
- The triangle needs coordinates for the corners

Polymorphism is where each type is responsible for its own data and code, but still adheres to the same interface, in this case a simple method "signature":

```python
def draw_shape(self)
```

So now we can treat shapes as the **same** even though they are **different**. It hides the complexities of the difference behind a clean abstraction.

```python
shapes = [Circle(5, 5, 10), Rectangle(1, 3, 5, 6)]
for shape in shapes:
    print(shape.draw_shape())
```