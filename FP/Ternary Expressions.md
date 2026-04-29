[Ternaries](https://book.pythontips.com/en/latest/ternary_operators.html) are a great way to reduce a series of [[Statements]], like an `if`/`else` block, to a single [[Expressions]].

When you first learned how to use conditional logic in Python, it probably looked like this:

```py
result = 0
if number % 2 == 0:
    result = number / 2
else:
    result = (number * 3) + 1
```

This code sets `result` to a dummy value like `0` (`None` would also work), then overwrites it with its "real" value based on the condition.

A ternary lets us do all that in one expression:

```py
result = number / 2 if number % 2 == 0 else (number * 3) + 1
```

Note that we also avoided mutating the `result` variable. Ternary expressions are good for maintaining [[Immutability]].

The syntax for a ternary in Python is:

```py
value_a if condition else value_b
```

This qualifies as an _expression_ because it's a single statement that _evaluates to a value_ – one of two values, depending on the condition.

## When to Use Ternaries

Ternary expressions are cool, but _don't overdo it_. If you're dealing with complex conditional logic, it's often easier to work with full `if`/`else` blocks than to try to nest ternaries inside each other.

```py
msg = (
    "Access granted"
    if (
        user.is_authenticated
        and (user.role == "admin" or (user.role == "editor" and not user.suspended))
    )
    else ("Access limited" if user.is_authenticated else "Access denied")
)
```