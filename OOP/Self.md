[[Método]] are defined _within_ the `class` declaration. Their first parameter is always the instance of the class that the method is being called on. By convention, it's called ["self"](https://docs.python.org/3/glossary.html#term-method), and because `self` is a reference to the object, you can use it to read and update the properties of the object.

Notice that methods are called directly on an object instance using the dot operator:

```python
my_object.my_method()
```