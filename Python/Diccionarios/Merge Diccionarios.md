Esta es una de las formas de mezclar dos [[Diccionario]]

def merge(dict1, dict2):
    merged = dict1
    for char_name in dict2:
        dict1[char_name] = dict2[char_name]
    return merged