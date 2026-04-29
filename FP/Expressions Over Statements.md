  
Because [[Expressions]] always produce values, they're _reusable_ and _declarative_. You can compose expressions and nest them within each other – but you can't always do that with other kinds of statements. **[[Functional Programming]] encourages the use of expressions over [[Statements]] where possible,** because expressions tend to minimize side effects, and make the code easier to reason about. For example, a function that returns a sum is an expression:

```py
total = sum([1, 2, 3, 4])
```

We can get the same result with a loop, but that involves a series of statements:

```py
total = 0
for n in [1, 2, 3, 4]:
    total += n
```

Again, it's simple to combine expressions:

```py
print(sum([1, 2, 3, 4]) * 2)  # 20
```

But we can't really do the same thing with our series of statements:

```py
# This doesn't work!
print((
total = 0
for n in [1, 2, 3, 4]:
    total += n
) * 4)
```

Expressions tend to be _concise_ and _logically pure_. Some languages that are designed for functional programming, such as Haskell, actually treat _everything_ as an expression. In these languages, even control flow constructs like `if` and `case` are expressions that return values.

Boots


[[Statements]]