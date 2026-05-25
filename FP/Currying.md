Function [currying](https://en.wikipedia.org/wiki/Currying) is a specific _kind_ of [[Function Transformation]] where we translate a single function that accepts multiple arguments into _multiple_ [[Function]]s that each accept a _single_ argument.

This is a "normal" 3-argument function:

```py
box_volume(3, 4, 5)
```

This is a "curried" _series of functions_ that does the same thing:

```py
box_volume(3)(4)(5)
```

Here's another example that includes the implementations:

```py
def sum(a, b):
  return a + b

print(sum(1, 2))
# prints 3
```

And the same thing curried:

```py
def sum(a):
  def inner_sum(b):
    return a + b
  return inner_sum

print(sum(1)(2))
# prints 3
```

The `sum` function only takes a _single_ input, `a`. It returns a _new_ function that takes a single input, `b`. This new function when called with a value for `b` will return the sum of `a` and `b`. _We'll talk later about why this is useful._