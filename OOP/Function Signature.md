A [[Functions]] signature (or [[Método]] signature) includes the name, inputs, and outputs of a function or method. For example, `hit_by_fire` in the `Human` and `Archer` classes have identical signatures.

```python
class Human:
    def hit_by_fire(self):
        self.health -= 5
        return self.health

class Archer:
    def hit_by_fire(self):
        self.health -= 10
        return self.health
```

Both methods have the same name, take no additional inputs, and return integers. If _any_ of those things were different, they would have different function signatures. Here are methods with _different_ signatures:

```python
class Human:
    def hit_by_fire(self):
        self.health -= 5
        return self.health

class Archer:
    def hit_by_fire(self, dmg):
        self.health -= dmg
        return self.health
```