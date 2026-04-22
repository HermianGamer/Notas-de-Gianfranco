```bash
which sh
```

The `which` command tells you the location in the [[Filesystem]] of an installed command line program. In this case, we're asking for the location of the `sh` (shell) program. Mine is located at `/bin/sh`.

2. [ ] Take a look at the contents of that file:

```bash
cat /bin/sh
```

Keep in mind, your `sh` program is a compiled executable, probably written in C. That's why when you try to view its contents with `cat`, you see... what you see.

A file with a `.sh` extension on the other hand is a [[Shell]] script. It's a text [[File]] that contains commands that will be interpreted and run by the `sh` program. They are both executable programs, but only one can be run without the help of another program.