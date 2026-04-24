ejemplo para recordar sobre como ordenar una [[Lista]] de [[Diccionario]]s.


input: diccionario = `{"letra1": 3, "letra2": 1, "letra3": 8}`
output: lista = `[{"letra": "letra1", "num": 4}, {"letra": "letra2", "num": 1}, {"letra": "letra3", "num": 8}]`


```
def sort_on(items):
	return items["num"]
```
  
  
```
def sort_dictlist(dictlist):
	dictlist.sort(reverse=True, key=sort_on)
	return dictlist
```