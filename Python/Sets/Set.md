[Sets](https://docs.python.org/3/tutorial/datastructures.html#sets) are _like_ Lists, but they are _unordered_ and they guarantee _uniqueness_. Only _ONE_ of each value can be in a set.

```py
fruits = {"apple", "banana", "grape"}
print(type(fruits))
# Prints: <class 'set'>

print(fruits)
# Prints: {'banana', 'grape', 'apple'}
```

## An Empty Set
Because the empty bracket `{}` syntax creates an empty dictionary, to create an _empty_ set, you need to use the `set()` function.

```py
fruits = set()
fruits.add("pear")
print(fruits)
# Prints: {'pear'}
```
