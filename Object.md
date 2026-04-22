So if a class is a new custom type, what's an object? Objects are just [instance](https://stackoverflow.com/questions/20461907/what-is-meaning-of-instance-in-programming)s of a [[class]].

Yeah I know, "instance" is another fancy programming word. It just means "an example of" or "a specific case of". For example, "Lane is an instance of a human" or "My Chemical Romance is an instance of a band".

For example:

```python
health = 50
# health is an instance of an integer type
aragorn = Soldier()
# aragorn is an instance of the Soldier class type
```

Each new instance of a class is an "object".

## Example

```py
class Archer:
    health = 40
    arrows = 10

# Create several instances of the Archer class
legolas = Archer()
bard = Archer()

# Print class properties
print(legolas.health) # 40
print(bard.arrows) # 10
```