  
Remember [[Function Transformation]]s where a [[Higher Order Function]] takes a function and returns a function with new behavior? [Python decorators](https://docs.python.org/3/glossary.html#term-decorator) are just [[Syntactic sugar]] around that. 

**Example:**

```py
def vowel_counter(func_to_decorate):
    vowel_count = 0
    def wrapper(doc):
        nonlocal vowel_count
        vowels = "aeiou"
        for char in doc:
            if char.lower() in vowels:
                vowel_count += 1
        print(f"Vowel count: {vowel_count}")
        return func_to_decorate(doc)
    return wrapper

@vowel_counter
def process_doc(doc):
    print(f"Document: {doc}")

process_doc("What")
# Vowel count: 1
# Document: What

process_doc("A wonderful")
# Vowel count: 5
# Document: A wonderful

process_doc("world")
# Vowel count: 6
# Document: world
```

The `@vowel_counter` line is "decorating" the `process_doc` function with the `vowel_counter` function. `vowel_counter` is called once when `process_doc` is defined with the `@` syntax, but the `wrapper`function that it returns is called every time `process_doc` is called. That's why `vowel_count` is preserved and printed after each time.

## It's Just Syntactic Sugar

Python decorators are just another (sometimes simpler) way of writing a higher-order function. These two pieces of code are _identical_:

### With Decorator

```py
@vowel_counter
def process_doc(doc):
    print(f"Document: {doc}")

process_doc("Something wicked this way comes")
```

### Without Decorator

```py
def process_doc(doc):
    print(f"Document: {doc}")

process_doc = vowel_counter(process_doc)
process_doc("Something wicked this way comes")
```


  
The [[Args and Kwargs]] syntax is great for decorators that are intended to work on functions with different [[Function Signature]].

## Example

The `log_call_count` function below doesn't care about the number or type of the decorated function's (`func_to_decorate`) arguments. It just wants to count how many times the function is called. However, it still needs to pass any arguments through to the wrapped function.

```py
def log_call_count(func_to_decorate):
    count = 0

    def wrapper(*args, **kwargs):
        nonlocal count
        count += 1
        print(f"Called {count} times")
        # The * and ** syntax unpacks the arguments
        # and passes them to the decorated function
        return func_to_decorate(*args, **kwargs)

    return wrapper
```


  
You can stack decorators, and you can use [[Currying]] with decorators.

```py
def to_uppercase(func):
    def wrapper(document):
        return func(document.upper())

    return wrapper

def get_truncate(length):
    def truncate(func):
        def wrapper(document):
            return func(document[:length])

        return wrapper

    return truncate

@to_uppercase
@get_truncate(9) # currying
def print_input(input):
    print(input)

print_input("Keep Calm and Carry On")
# prints: "KEEP CALM"
```

Observe that `to_uppercase` wrapped `get_truncate(9)`, and `get_truncate(9)` returned `truncate`which wrapped `print_input`, then `print_input` printed "KEEP CALM" from "Keep Calm and Carry On."