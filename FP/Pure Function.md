If you take nothing else away from this course, _please_ take this: **[Pure functions](https://en.wikipedia.org/wiki/Pure_function) are fantastic.** They have two properties: Pure [[Function]]

- They _always_ return the same value given the same arguments.
- Running them causes no side effects

In short: **pure functions don't do anything with anything that exists outside of their scope.**

Click to hide video

## Example of a Pure Function

```py
def find_max(nums):
    max_val = float("-inf")
    for num in nums:
        if max_val < num:
            max_val = num
    return max_val
```
## Example of an Impure Function

```py
# instead of returning a value
# this function modifies a global variable
global_max = float("-inf")

def find_max(nums):
    global global_max
    for num in nums:
        if global_max < num:
            global_max = num
```

[[Functional Programming]]