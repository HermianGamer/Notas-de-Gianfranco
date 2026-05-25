"Map," "filter," and "reduce" are three commonly used [[Higher Order Function]] [higher-order functions](https://en.wikipedia.org/wiki/Higher-order_function) in [[Functional Programming]]. [[Built-In Function]]

In Python, the  [map](https://docs.python.org/3/library/functions.html#map) [[Function]] takes a function and an [iterable](https://docs.python.org/3/glossary.html#term-iterable) (in this case a list) as inputs. It returns an iterator that applies the function to every item, yielding the results.

![](https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/J5hKgxZ-885x300.png)

With `map`, we can operate on lists without using loops and nasty stateful variables. For example, given this code:

```py
def square(x):
    return x * x

nums = [1, 2, 3, 4, 5]
squared_nums = []
for num in nums:
    num_squared = square(num)
    squared_nums.append(num_squared)

print(squared_nums)
# [1, 4, 9, 16, 25]
```

We could use `map` instead, like this:

```py
def square(x):
    return x * x

nums = [1, 2, 3, 4, 5]
squared_nums = map(square, nums)

print(list(squared_nums))
# [1, 4, 9, 16, 25]
```

`map()` returns a "map object," so the [`list()` type constructor](https://docs.python.org/3/library/stdtypes.html#list) is needed to convert it back into a standard list.