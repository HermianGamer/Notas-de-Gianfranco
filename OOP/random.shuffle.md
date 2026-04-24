[[random]]

```python
import random

my_list = [1, 2, 3, 4, 5]
random.shuffle(my_list)
print(my_list)  # Output: e.g., [3, 1, 5, 2, 4]
```

Common Workarounds

- **Shuffle without modifying original**: Use `random.sample(x, k=len(x))` to return a _new_ shuffled list.
- **Shuffling Strings/Tuples**: Convert them to a list first, shuffle, and then convert back (e.g., using `''.join(list)` for strings).
- **Reproducibility**: Use `random.seed(n)` before shuffling to ensure the "random" order is the same every time you run the code (useful for debugging).