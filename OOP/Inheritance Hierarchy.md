There is no (technical) limit to how deeply we can nest an [[Inheritance]] tree. For example:

`Tiger` inherits from `Feline` inherits from `Animal` inherits from `LivingThing`.

That said, _be careful_! New programmers often get carried away. You should never think to yourself:

> "Well _most_ wizards are elves... so I'll just have `Wizard` inherit from `Elf`"

A good child class is a strict [subset](https://en.wikipedia.org/wiki/Subset) of its parent [[class]].