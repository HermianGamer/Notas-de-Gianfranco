# Complexity Quiz - Example 1
Consider the following code:

```python
# names is an array of strings
def get_name_at_index(names: list[str], i: int) -> str:
    return names[i]
```

# Complexity Quiz - Example 2

Consider the following code. It calculates the number of times a given number can be divided by `2` before becoming less than or equal to `1`.

```python
def naive_log2(x: int) -> int:
	count = 0
	while x > 1:
		x /= 2
		count += 1
	return count
```

# Complexity Quiz - Example 3

Consider the following function for two questions:

```python
#  halvedSections returns a list of lists.
#  For example, n=12 results in:
#    [
#       [0 1 2 3 4 5 6 7 8 9 10 11 12]
#       [0 1 2 3 4 5 6]
#       [0 1 2 3]
#       [0 1]
#    ]
def halved_sections(n: int) -> int:
    rows = []
    i = n
    while i > 0:
        col = []
        for j in range(i+1):
            col.append(j)
        rows.append(col)
        i //= 2
    return rows
```

It has a specific time complexity of:

`T(n) = O(n + n/2 + n/4 + ... 1)`

## Hint

This is a tricky one. You need to take into account the shrinking size of each successive list.

Boots