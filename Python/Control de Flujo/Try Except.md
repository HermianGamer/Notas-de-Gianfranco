```py
try:
  10 / 0
except Exception:
  print("can't divide by zero")
```

```py
try:
  10 / 0
except Exception as e:
  print(e)

# prints "division by zero"
```