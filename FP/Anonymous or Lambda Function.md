Anonymous [[Function]]s have _no name_, and in Python, they're called [lambda functions](https://docs.python.org/3/reference/expressions.html#lambda) after [lambda calculus](https://en.wikipedia.org/wiki/Lambda_calculus). Here's a lambda function that takes a single argument `x` and returns the result of `x + 1`:

```py
lambda x: x + 1
```

Notice that the [expression](https://docs.python.org/3/reference/expressions.html#expressions) `x + 1` is returned _automatically_, no need for a `return` statement. Compare that to how you'd normally write a function:

```py
def add_one(x):
    return x + 1
```

Because functions are just values, we can assign the function to a variable named `add_one`:

```py
add_one = lambda x: x + 1
print(add_one(2))
# 3
```

Lambda functions might _look_ scary, but they're still just functions. Because they simply return the result of an expression, they're often used for small, simple evaluations. Here's an example that uses a lambda to get a value from a dictionary:

```py
get_age = lambda name: {
    "lane": 29,
    "hunter": 69,
    "allan": 17
}.get(name, "not found")
print(get_age("lane"))
# 29
```


[[Functional Programming]]