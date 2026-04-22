The built in [`sys`](https://docs.python.org/3/library/sys.html) in [[Python]] module provides access to [command line arguments](https://en.wikipedia.org/wiki/Command-line_interface#Arguments) in the [[Terminal]]. In particular [`sys.argv`](https://docs.python.org/3/library/sys.html#sys.argv) is a list of [[Strings]] representing the [[Positional Arguments]] passed to the script. The first argument is the script name, the rest are the arguments.  
For example, `python3 main.py` will result in a `sys.argv` list that looks like this:

```py
print(sys.argv)
# Prints ['main.py']
```

And `python3 main.py books/frankenstein.txt` will result in a `sys.argv` list that looks like this:

```py
print(sys.argv)
# Prints ['main.py', 'books/frankenstein.txt']

print(len(sys.argv))
# Prints 2

print(sys.argv[0])
# Prints 'main.py'

print(sys.argv[1])
# Prints 'books/frankenstein.txt'
```


 exit the program with a status code of `1` using 
```
sys.exit(1)
```
