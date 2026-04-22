Las [Tuples](https://docs.python.org/3/library/stdtypes.html#typesseq-tuple) o Tuplas son colecciones de datos ordenados y es inmutable. Es como una [[Lista]] pero de tamaño fijo. Las tuplas se crean con paréntesis. 

```py
my_tuple = ("this is a tuple", 45, True)
print(my_tuple[0])
# this is a tuple
print(my_tuple[1])
# 45
print(my_tuple[2])
# True
```

Es bueno guardar distintos tipos de datos en una tupla, ya que son cortas (de 2 a 3 items). Las tuplas de hecho se pueden guardar en una [[Lista]].

```py
my_tuples = [
    ("this is the first tuple in the list", 45, True),
    ("this is the second tuple in the list", 21, False)
]
print(my_tuples[0][0]) # this is the first tuple in the list
print(my_tuples[0][1]) # 45
print(my_tuples[1][0]) # this is the second tuple in the list
print(my_tuples[1][2]) # False
```

En caso se requiera una tupla de un solo elemento se hace asi:

```py
dog = ("Fido",)
```

Se le pueden copiar los datos a las tuplas para asignarles nombres.

```py
dog = ("Fido", 4)
dog_name, dog_age = dog
print(dog_name)
# Fido
print(dog_age)
# 4
```

Cuando retornas más de un valor en una función se retorna una tupla.