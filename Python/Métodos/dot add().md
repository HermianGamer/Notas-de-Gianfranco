es un [[Método]]
You can [`.add()`](https://docs.python.org/3/library/stdtypes.html#set.add) values to a [[Set]]. Think of `.add()` like `append` but for sets!

```py
fruits = {"apple", "banana", "grape"}
fruits.add("pear")
print(fruits)
# Prints: {'pear', 'banana', 'grape', 'apple'}
```

No error will be raised if you add an item already in the set, and the set will remain unchanged.