The [filter](https://docs.python.org/3/library/functions.html#filter) function takes a function and an iterable (in this case a list) and returns an iterator that only contains elements from the original iterable where the result of the function on that item returned `True`. [[Built-In Function]]

![](https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/FfVxD7d-933x350.png)

In Python:

```Python
def is_even(x):
    return x % 2 == 0

numbers = [1, 2, 3, 4, 5, 6]
evens = list(filter(is_even, numbers))
print(evens)
# [2, 4, 6]
```