_Expressions_ are a _subset_ of statements that _produce values_. _Evaluating an expression_ results in a _value_ that can be used in whatever way is needed. It can be assigned to a variable, returned from a [[Function]], etc.

```py
result = 2 + 2  # Arithmetic expression
length = len("hello")  # Function call expression
total_cost = len(items) * cost  # Multiple expressions combined into one
```

One thing that may surprise you is that, in most languages (including Python), _every function call is an expression_. When you call a function, it returns a value – whether or not you realize it or do anything with that value. Even if a Python function doesn't have a `return` statement, it still implicitly returns `None`. You can test this by assigning a `print` call to a variable:

```py
x = print("hello")  # hello
print(x)            # None
```

Sure enough: `print` – the first function that we all learn – technically returns a value.

[[Functional Programming]]