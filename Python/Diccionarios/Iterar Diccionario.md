Se puede iterar por los `keys` de un [[Diccionario]] así como se haría en una lista. Por defecto, al iterar lo que se devuelve es únicamente la `key`.
```py
fruit_sizes = {
    "apple": "small",
    "banana": "large",
    "grape": "tiny"
}

for name in fruit_sizes:
    size = fruit_sizes[name]
    print(f"name: {name}, size: {size}")

# name: apple, size: small
# name: banana, size: large
# name: grape, size: tiny
```

se pueden juntar distintos `keys` para ingresar cada vez mas adentro a un diccionario que tiene estructura tipo json:
```py
outer_dictionary["outer_key"]["inner_key"]
```

