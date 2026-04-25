Corrés esto en la terminal:

bash

```bash
chflags hidden ~/Applicazioni ~/Filmati ~/Immagini ~/Musica ~/Pubblica
```

Si querés revertirlo en algún momento:

bash

```bash
chflags nohidden ~/Applicazioni ~/Filmati ~/Immagini ~/Musica ~/Pubblica
```

Después de correrlo, los [[Directory]]s desaparecen del Finder. Si no las ves desaparecer de inmediato, haz `Cmd + Shift + .` para asegurarte de que no estás en modo "mostrar archivos ocultos".

[[CLI]]
Funciona para ambos, directorios y [[File]]. Por ejemplo:

bash

```bash
chflags hidden ~/archivo.txt
```

Cualquier cosa que no quieras ver en el Finder lo podés ocultar así.