
El slicing sirve para recorrer una [[Lista]]. Por ejemplo:

```py
scores = [50, 70, 30, 20, 90, 10, 50]
# scores[inicio:fin:salto])
print(scores[1:5:2])
# Prints [70, 20]
```

Negative indices count from the end of the list. For example, `numbers[-1]` gives the last item in the list, `numbers[-2]` gives the second last item, and so on.
