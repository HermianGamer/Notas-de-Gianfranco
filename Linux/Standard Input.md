

If there's a standard _output_, there must be a standard _input_, right?

["Standard Input"](https://en.wikipedia.org/wiki/Standard_streams#Standard_input_%28stdin%29), usually called "standard in" or "stdin", is the default place where programs _read_ their input. It's just a stream of data that programs can read from as they run.

All major programming languages provide a simple way to read from stdin. In Python, it's the `input` function:

```py
# execution stops until the user types
# something (in this case "Lane") and presses enter
name = input("What is your name? ")

print("Hello,", name)
# Hello, Lane
```

el comamdo para [[Shell]] es `read`
