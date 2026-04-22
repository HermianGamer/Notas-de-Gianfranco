[[Python]] is a very dynamic language, which makes it difficult for the interpreter to enforce some of the safeguards that languages like [Go](https://go.dev/) do. That's why [[Encapsulation]] in Python is achieved mostly by [convention](https://en.wikipedia.org/wiki/Coding_conventions)rather than by _force_.

Prefixing methods and properties with a double underscore is a _strong_ suggestion to the users of your class that they shouldn't be touching that stuff. If a developer wants to break convention, [there are ways to get around](https://stackoverflow.com/questions/3385317/private-variables-and-methods-in-python) the double underscore rule.

```python
class Wall:
    def __init__(self, height):
        # the double underscore makes this a private property
        # but it's not strictly enforced, there are hacks to get around it
        self.__height = height

    def get_height(self):
        return self.__height
```