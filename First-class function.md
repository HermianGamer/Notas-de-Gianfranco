- **First-class function:** A function that is treated like any other value ,[[Functions as Variables]].
## First-Class Example

```py
def square(x):
    return x * x

# Assign function to a variable
f = square

print(f(5))
# 25
