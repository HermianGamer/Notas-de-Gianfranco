Los diccionarios en. Python se usan para guardar datos con una relación `key` -> `value`. Se accede a cada valor llamando a su respectiva `key`.
```py
# use curly braces
# add key-value pairs
car = {
  "brand": "Toyota",
  "model": "Camry",
  "year": 2019,
}
```

Debido a que los diccionarios dependen de las `key`s, cada `key` debe ser única. En caso se repitan, solo se tomara en cuenta solo el último `value` que usa la `key`.

A value is retrieved from a dictionary by specifying its corresponding key in square brackets. The square brackets look similar to indexing into a list.
```py
car = {
    "make": "Toyota",
    "model": "Camry"
}
print(car["make"])
# Prints: Toyota
```