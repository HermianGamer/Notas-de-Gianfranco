  
Bash and Zsh both have [configuration files](https://en.wikipedia.org/wiki/Unix_shell#Configuration_files) that run automatically each time you start a new [[Shell]] session. These [[File]]s are used to set up your shell [[enviroment]]. They can be used to set up aliases, functions, and environment variables.


These files are located in your home directory (`~`) and are hidden by default. The [[ls]] command has a `-a` flag that will show hidden files:
## ls -a


```bash
ls -a ~
```

- If you're using Bash, `.bashrc` is probably the file you want to edit.
- If you're using Zsh, `.zshrc` is probably the file you want to edit or create if it doesn't yet exist.

Configuracion
hola que hace