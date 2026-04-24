The [.index](https://docs.python.org/3/tutorial/datastructures.html#more-on-lists) [[Lista]] [[Método]] is very useful when trying to determine the index of an element in a list.

```python
try:
    pos = my_list.index('banana')
    print(f"Index: {pos}")
except ValueError:
    print("Item not in list")
```
