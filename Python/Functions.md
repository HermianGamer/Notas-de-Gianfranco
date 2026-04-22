pass
continue
return

**`def`:** Declara la función.
**`return`:** Retorna un valor, finaliza la funcion.
**`yield`:** Retorna un valor.
**`yield`**Pausa la función y devuelve un valor.Convierte la función en un **generador**; se puede retomar luego.
**`pass`**No hace nada (marcador de posición).Se usa cuando la sintaxis exige algo pero no quieres ejecutar nada.

### `continue`

Imagina que estás procesando una lista de números. Si encuentras uno que no te sirve, usas `continue`. Esto hace que el programa **salte el resto del código del bucle actual** y pase directamente a la siguiente iteración.

### `break`

Es el botón de pánico. Si se cumple una condición, `break` **detiene el bucle por completo** y sale de él, continuando con la siguiente línea de código fuera del bucle.

- **`global`**: Le dice a la función que use una variable definida en el cuerpo principal del script, permitiéndote modificarla.
    
- **`nonlocal`**: Se usa en funciones anidadas (una función dentro de otra) para indicar que quieres modificar una variable de la función "padre".