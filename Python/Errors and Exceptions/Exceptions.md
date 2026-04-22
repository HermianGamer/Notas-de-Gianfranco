Este es un tipo principal de [[Errors & Exceptions]].  el [[Python Interpreter]] te dice

Even if your code has the right syntax, however, it may still cause an error when an attempt is made to execute it. Errors detected during execution are called "exceptions" and can be handled gracefully by your code. You can even raise your own exceptions when bad things happen in your code.

Python uses a [try-except](https://docs.python.org/3/tutorial/errors.html#handling-exceptions) pattern for handling errors.

```py
try:
  10 / 0
except Exception:
  print("can't divide by zero")
```

The `try` block is executed until an exception is raised or it completes, whichever happens first. In this case, an exception is raised because division by zero is impossible. The `except` block is only executed if an exception is raised in the `try` block.

If we want to access the data from the exception, we use the following syntax:

```py
try:
  10 / 0
except Exception as e:
  print(e)

# prints "division by zero"
```

Wrapping potential errors in `try/except` blocks allows the program to handle the exception gracefully without crashing.

  
As seen in the example, you can also access the error using `as`, like this:

```py
except Exception as e:
    print(e)
```
