como imprimir mensajes con el [[CLI]]
```bash
echo "Hello world"
```

```bash
$ echo Hello $name
Hello Lane
```
Unlike in Python, where you can just use a variable's _name_, in your shell you need to prefix the variable name with a `$` to _use_ it, else it would just print `name` instead of the value.