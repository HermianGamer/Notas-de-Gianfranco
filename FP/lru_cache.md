[`lru_cache` from the `functools`](https://docs.python.org/3/library/functools.html#functools.lru_cache) [[Module]] is an example of a [[Decorator]] and an example of [[Memoization]].

`lru_cache` memoizes the inputs and outputs of the decorated function in a size-restricted dictionary. It speeds up repeated calls to a slow function with the same inputs. For instance, if the function reads from disk, makes network requests, or requires a lot of computation AND it is used repeatedly with the same inputs.

Here's an example from the Python documentation that perfectly illustrates how and why to use the `lru_cache` decorator:

```py
from functools import lru_cache

@lru_cache()
def factorial_r(x):
    if x == 0:
        return 1
    else:
        return x * factorial_r(x - 1)

factorial_r(10) # no previously cached result, makes 11 recursive calls
# 3628800
factorial_r(5)  # just looks up cached value result
# 120
factorial_r(12) # makes two new recursive calls, the other 11 are cached
# 479001600
```

Since the `factorial` function is recursive and the inputs are sequential numbers, it's called repeatedly with the same inputs. Without the cache, the function would be called 30 times. With `lru_cache`, the function is only called 13 times. While you don't often need to compute factorials, this example ties together how to use a decorator _and_ memoization _and_ recursion.

## Assignment