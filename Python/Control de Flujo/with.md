A [with](https://docs.python.org/3/reference/compound_stmts.html#with) block can be used to [open a file](https://docs.python.org/3/tutorial/inputoutput.html#reading-and-writing-files): abrir un [[File]]

```py
with open(path_to_file) as f:
    # do something with f (the file) here
```

_The `with` block will automatically close the file when the block is exited, cleaning up resources_.