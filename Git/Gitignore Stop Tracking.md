`.gitignore` solo ignora archivos que [[Git]] **todavía no conoce**. Si el archivo ya fue [[Commit]]ed anteriormente, Git lo sigue rastreando aunque lo pongas en el [[Gitignore]].

**La solución** es quitarlo del índice de Git sin borrarlo del disco:

[[rm]]
```bash
git rm --cached archivo.md
```

Luego hacés un commit:

```bash
git commit -m "dejar de rastrear archivo.md"
```

A partir de ahí, Git los va a ignorar correctamente aunque los modifiques.