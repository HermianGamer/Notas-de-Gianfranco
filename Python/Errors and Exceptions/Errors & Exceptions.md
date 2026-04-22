Errors are NOT Bugs
  
We haven't covered classes and objects yet, which is what an `Exception` really is at its core.

En Python hay dos tipos principales de errores:
- [[Syntax Error]]
- [[Exceptions]]

para evitar los errores se usa el [[Try Except]]

siempre capturar el error mas especifico primero, sino no se llegara al otro. ejemplo de mala practica:
```py
try:
    nums = [0, 1]
    print(nums[2])
except Exception:
    print("An error occurred")
except IndexError:
    print("Index error")
```
